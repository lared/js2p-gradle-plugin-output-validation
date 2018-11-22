# Reproduction steps

0. ./gradlew clean -Dorg.gradle.warning.mode=all
0. ./gradlew generateJsonSchema2Pojo -Dorg.gradle.warning.mode=all
0. ./gradlew generateJsonSchema2Pojo -Dorg.gradle.warning.mode=all

The last step should produce the following warning during configuration:
```
> Task :generateJsonSchema2Pojo UP-TO-DATE
Registering invalid inputs and outputs via TaskInputs and TaskOutputs methods has been deprecated. This is scheduled to be removed in Gradle 5.0. A problem was found with the configuration of task ':generateJsonSchema2Pojo'.
 - Cannot write to file '/home/michal/js2p-gradle-plugin-output-validation/build/generated-sources/js2p' specified for property '$2' as it is a directory.
```

