
Code:
```
#set -e

# Grading Script viariables
CP=".:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar"

SCORE=0
ERROR=0
TESTS=2

# Clean up repo
rm -rf student-submission

# Clone student repo
git clone $1 student-submission
if [ $? -ne 0]; then
        echo"Clone unsuccessful!"
        exit 1
fi

# Check if ListExamples.java exists
if [ -f "student-submission/ListExamples.java" ]; then
  echo "found it with -f!"
else
  echo "file not found"
  exit 1
fi

# Copy test file into directory
cp TestListExamples.java student-submission/
echo "Copy file into directory"
mkdir student-submission/lib
cp lib/* student-submission/lib
cp *.java student-submission

# Go into the directory
cd student-submission/

# Compile student code
echo "compiling file"
javac -cp $CP *.java
java -cp $CP org.junit.runner.JUnitCore ListExamples > results.txt

#Grade
if [ $? -eq 0 ]; then
    SCORE=100
else
    echo "$(<results.txt)"

    # I learn to use head and tail and how to get the scores from the person for lab 9.
    # aphuanh004

    cat results.txt | head -n 2 | tail -n 1 > grading.txt
    ERROR=$(grep -o 'E' grading.txt | wc -l | xargs)
    SCORE=$(( 100 - ($ERROR * 100 / $TESTS) ))
fi

# Print the student's grade
echo "Grade: $SCORE"
```
I have trouble with opening the webpage in "http://ieng6-203.ucsd.edu:4001". <br/>
I think it is because that I am not using school Wifi, but I am in TEXAS right now so I cannot.<br/>
I also cannot run it on a local host because I have a windows computer, so it is not working for me.<br/>
The following are those running on the terminal instead of the server.<br/>
![](lab-5-screenshots/Grade1.png)
![](lab-5-screenshots/Grade2.png)
![](lab-5-screenshots/Grade3.png)

For https://github.com/ucsd-cse15l-f22/list-methods-compile-error,
`rm -rf student-submission` has no output or error. <br/>
`git clone $1` has no output. The error is "Cloning into 'student-submission'...".<br/>

```
if [ $? -ne 0]; then
        echo"Clone unsuccessful!"
        exit 1
fi
```
The exit code is 0. <br/>

```
if [ -f "student-submission/ListExamples.java" ]; then
  echo "found it with -f!"
else
  echo "file not found"
  exit 1
fi
```
The exit code is 0.<br/>

`cp TestListExamples.java student-submission/` has no output or error.<br/>
```
cp lib/* student-submission/lib
cp *.java student-submission
```
Has no output or error. <br/>
`cd student-submission/` has no output or error. <br/>
```
javac -cp $CP *.java
java -cp $CP org.junit.runner.JUnitCore ListExamples > results.txt
```
standard error is "ListExamples.java:15: error: ';' expected
        result.add(0, s)
                        ^
1 error"
standard output is"FAILURES!!!
Tests run: 1,  Failures: 1
Grade: 50
[cs15lfa22fd@ieng6-203]:list-examples-grader:445$ bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-compile-error
Cloning into 'student-submission'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
grade.sh: line 17: [: missing `]'
found it with -f!
Copy file into directory
compiling file
ListExamples.java:15: error: ';' expected
        result.add(0, s)
                        ^
1 error
JUnit version 4.13.2
.E
Time: 0.002
There was 1 failure:
1) initializationError(org.junit.runner.JUnitCommandLineParseResult)
java.lang.IllegalArgumentException: Could not find class [ListExamples]
        at org.junit.runner.JUnitCommandLineParseResult.parseParameters(JUnitCommandLineParseResult.java:100)
        at org.junit.runner.JUnitCommandLineParseResult.parseArgs(JUnitCommandLineParseResult.java:50)
        at org.junit.runner.JUnitCommandLineParseResult.parse(JUnitCommandLineParseResult.java:44)
        at org.junit.runner.JUnitCore.runMain(JUnitCore.java:72)
        at org.junit.runner.JUnitCore.main(JUnitCore.java:36)
Caused by: java.lang.ClassNotFoundException: ListExamples
        at java.net.URLClassLoader.findClass(URLClassLoader.java:387)
        at java.lang.ClassLoader.loadClass(ClassLoader.java:418)
        at sun.misc.Launcher$AppClassLoader.loadClass(Launcher.java:352)
        at java.lang.ClassLoader.loadClass(ClassLoader.java:351)
        at java.lang.Class.forName0(Native Method)
        at java.lang.Class.forName(Class.java:348)
        at org.junit.internal.Classes.getClass(Classes.java:42)
        at org.junit.internal.Classes.getClass(Classes.java:27)
        at org.junit.runner.JUnitCommandLineParseResult.parseParameters(JUnitCommandLineParseResult.java:98)
        ... 4 more

FAILURES!!!
Tests run: 1,  Failures: 1"
