# GraalVMTestApplication
 
How to use the 'org.springframework.experimental.aot' plugin?
 
## Description:

I'm trying spring native, I used graalvm：

```shell
D:\project\graalTest>java --version
openjdk 17.0.5 2022-10-18
OpenJDK Runtime Environment GraalVM CE 22.3.0 (build 17.0.5+8-jvmci-22.3-b08)
OpenJDK 64-Bit Server VM GraalVM CE 22.3.0 (build 17.0.5+8-jvmci-22.3-b08, mixed mode, sharing)
```

If I don't add the org.springframework.experimental.aot plug-in, everything is fine, and the binary file can be compiled.

If I add the org.springframework.experimental.aot plugin, the gradle build fails

```shell
PS D:\project\graalTest> .\gradlew build

FAILURE: Build failed with an exception.

* Where:
Build file 'D:\project\graalTest\build.gradle' line: 6

* What went wrong:
An exception occurred applying plugin request [id: 'org.springframework.experimental.aot', version: '0.12.1']
> Failed to apply plugin 'org.springframework.experimental.aot'.
   > Cannot add a SourceSet with name 'aotTest' as a SourceSet with that name already exists.

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 665ms

```
