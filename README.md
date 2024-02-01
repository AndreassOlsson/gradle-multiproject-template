# Instructions
1. clone or fork repo
2. Make sure you have gradle 8.5 and java 21 installed
3. run $ gradle wrapper
4. run $ ./gradlew clean build

# Versions
Java 21, Gradle 8.5

# Structure
A gradle multi-project build with multiple subprojects

# Example usage
./gradlew :subproject_1:run
./gradlew :subproject_2:run

./gradlew :subproject_1:clean :subproject_1:build

Gradle's run task is mainly designed for non-interactive tasks and may not handle
console input directly. Fixed by adding standard in in build.gradle run task

The command gradle wrapper is used to create new (or update) gradle wrapper files.
It only overwrites the current files if we add --gradle-version X.Y.Z. We basically
dont need to use it.

If we run ./gradlew <task> at root then we trigger all subprojects