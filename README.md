# tutorialGradle

Tutorial for Gradle. 

```
$ pwd 
/Users/parthabhattacharjee/git/tutorialGradle
```

### Is Gradle already installed? 

  - We have gradle version 3 already installed. 

```
$ gradle --v

------------------------------------------------------------
Gradle 3.4.1
------------------------------------------------------------

Build time:   2017-03-03 19:45:41 UTC
Revision:     9eb76efdd3d034dc506c719dac2955efb5ff9a93

Groovy:       2.4.7
Ant:          Apache Ant(TM) version 1.9.6 compiled on June 29 2015
JVM:          1.8.0_31 (Oracle Corporation 25.31-b07)
OS:           Mac OS X 10.11.6 x86_64

```

### What are the default, out of the box gradle tasks available? 

```
$ gradle tasks 
:tasks

------------------------------------------------------------
All tasks runnable from root project
------------------------------------------------------------

Build Setup tasks
-----------------
init - Initializes a new Gradle build. [incubating]
wrapper - Generates Gradle wrapper files. [incubating]

Help tasks
----------
buildEnvironment - Displays all buildscript dependencies declared in root project 'tutorialGradle'.
components - Displays the components produced by root project 'tutorialGradle'. [incubating]
dependencies - Displays all dependencies declared in root project 'tutorialGradle'.
dependencyInsight - Displays the insight into a specific dependency in root project 'tutorialGradle'.
dependentComponents - Displays the dependent components of components in root project 'tutorialGradle'. [incubating]
help - Displays a help message.
model - Displays the configuration model of root project 'tutorialGradle'. [incubating]
projects - Displays the sub-projects of root project 'tutorialGradle'.
properties - Displays the properties of root project 'tutorialGradle'.
tasks - Displays the tasks runnable from root project 'tutorialGradle'.

To see all tasks and more detail, run gradle tasks --all

To see more detail about a task, run gradle help --task <task>

BUILD SUCCESSFUL

Total time: 0.753 secs
```

### Add a simple helloWorld task. 

#### file:build.gradle 

```
task helloWorld {
  doLast {
   println 'Hello world from gradle.'
  }
}
```
  - Now run it. 

```
$ gradle helloWorld
:helloWorld
Hello world from gradle.

BUILD SUCCESSFUL

Total time: 0.633 secs
```
  
  - You could make it quiet. 

```
$ gradle -q helloWorld 
Hello world from gradle.
```

### Make the task default and call gradle without mentioning task name. 

```
defaultTasks 'helloWorld'
...
```

  - You dont have to mention the name of the task to run it. 

```
$ gradle -q 
Hello world from gradle.
```

### [Run on virtual device](http://stackoverflow.com/questions/4974568/how-do-i-launch-the-android-emulator-from-the-command-line)

  - You need to have android sdk installed in your machine. 

```
$ android -h

       Usage:
       android [global options] action [action options]
       Global opti...
```

  - Create a avd 

```
android create avd --name Default --target android-24 --abi default/x86_64
```
  
  - Check that the AVD is successfully created. 
  
```
$ android list avd 
Available Android Virtual Devices:
    Name: Default
    Path: /Users/parthabhattacharjee/.android/avd/Default.avd
  Target: Android 7.0 (API level 24)
 Tag/ABI: default/x86_64
    Skin: WVGA800
``` 

  - Run the emulator 

```
$ emulator -avd Default
Creating filesystem with parameters:
    Size: 69206016
    Block size: 4096
    Blocks per grou

```

### Watch the logs. 

```
adb logcat
```



### [Gradle with Android](http://www.vogella.com/tutorials/AndroidBuild/article.html)

  - ??

### [Gradle with AndroidStudio](https://developer.android.com/studio/build/build-variants.html)

  - ?? 



### References 

  - https://spring.io/guides/gs/gradle-android/
  - https://examples.javacodegeeks.com/core-java/gradle/gradle-hello-world-tutorial/
  - https://medium.com/google-developers/instant-run-how-does-it-work-294a1633367f
