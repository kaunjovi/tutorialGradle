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

```
$ gradle helloWorld
:helloWorld
Hello world from gradle.

BUILD SUCCESSFUL

Total time: 0.633 secs
```

### Make the task default and call gradle without mentioning task name. 

```
defaultTasks 'helloWorld'
...
```

```
$ gradle
:helloWorld
Hello world from gradle.

BUILD SUCCESSFUL

Total time: 0.647 secs
```


### [Gradle with Android](http://www.vogella.com/tutorials/AndroidBuild/article.html)

  - ??

### [Gradle with AndroidStudio](https://developer.android.com/studio/build/build-variants.html)

  - ?? 

### References 

  - https://spring.io/guides/gs/gradle-android/
  - https://examples.javacodegeeks.com/core-java/gradle/gradle-hello-world-tutorial/
  - 
