## Lab5 Report
# Using bash scipt in lab4. 
To achieve the commands with bash script, we need to first login to our ieng6 account by normal method. Then, two bash scripts are needed. The following codes should appear in the first bash script. 

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



**Where I struggled**: Inside nano, I have to use buttoms like control, enter, and direction arrows. I tried to search online but did not find a way that can run these inside bash. 


Then the second bash script contains the following codes 

```
CPATH='.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar'
cd lab7
javac -cp $CPATH *.java
java -cp $CPATH org.junit.runner.JUnitCore ListExamplesTests
git add .
git commit -m 'f'
git push
```
The second bash script check if the code passed all the Junit tests. Eventually, the script add, commit and push the updated version to github repo.
To run the two bash script, just use command `bash scriptName.sh`, where scriptName is the name of the bash script. 

In summary, the commands should look something like this:

```
ssh myaccount@ieng6.ucsd.edu
bash scriptOne.sh
nano ListExamples.java
%Then manually change the bug in nano
bash scriptTwo.sh
```



