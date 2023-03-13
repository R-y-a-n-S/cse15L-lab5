## Lab5 Report
# Using bash scipt in lab4. 
To achieve the commands with bash script, we need to first login to our ieng6 account by normal method. Then, two bash scripts are needs. The following codes should appear in the first bash script. 

```
CPATH='.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar'
git clone git@github.com:R-y-a-n-S/lab7.git
cd lab7
javac -cp $CPATH *.java
java -cp $CPATH org.junit.runner.JUnitCore ListExamplesTests
cd ..
```

The first bash script clone the repository and run Junit tests to find that there is bugs. 
Since I did not figure out how to use nano in bash, I have to correct the bugs mannually. 
Then the second bash script just contains the following codes 

```
CPATH='.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar'
cd lab7
javac -cp $CPATH *.java
java -cp $CPATH org.junit.runner.JUnitCore ListExamplesTests
git add .
git commit -m 'f'
git push
```
The second bash script check if the code passed all the Junit tests and update the correct version of code in github
To run the two bash script, just use `bash scriptName.sh`



