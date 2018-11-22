# Reproduction steps

0. `./gradlew clean -Dorg.gradle.warning.mode=all`
0. `./gradlew generateJsonSchema2Pojo -Dorg.gradle.warning.mode=all`
0. `./gradlew generateJsonSchema2Pojo -Dorg.gradle.warning.mode=all`

The last step should produce the following error during configuration:
```
> Task :generateJsonSchema2Pojo FAILED

FAILURE: Build failed with an exception.

* What went wrong:
A problem was found with the configuration of task ':generateJsonSchema2Pojo'.
> Cannot write to file '<redacted>/js2p-gradle-plugin-output-validation/build/generated-sources/js2p' specified for property '$2' as it is a directory.

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 0s
2 actionable tasks: 1 executed, 1 up-to-date
```

