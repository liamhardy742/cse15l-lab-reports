**1. Log into ieng6**  
  I typed "ssh cs15lwi23afd@ieng6.ucsd.edu" and then pressed `<enter>`  
    
  Pressing `<enter>` runs the command I typed and sshs into the ieng6 account.  
  ![Image](LapReportFourScreenshots/(1)SshIntoIeng6.png)
    
    
    
    
    
    
**2. Clone your fork of the repository from your Github account**  
  I typed "git clone https://github.com/liamhardy742/lab7" and then pressed `<enter>`  
    
  Pressing `<enter>` runs the command I typed and clones the git repository
  ![Image](LapReportFourScreenshots/(2)GitCloneRepo.png)
    
    
    
    
    
    
**3. Run the tests, demonstrating that they fail**  
  I typed "cd l" and pressed `<tab>` and then pressed `<enter>`.  
  Then I typed "javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java" (by copy pasting from the course website week 3) and then pressed `<enter>`.  
  Then I typed "java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore" (By copy pasting from the course website) and typed a space and then L `<tab>` T `<tab>` and then pressed `<backspace>` and `<enter>`.   
    
  Pressing `<tab>` the first time autocompleted the "cd l" to "cd lab7", and `<enter>` ran that command.  
  The next `<enter>` ran the command that compiled all of the java files preparing for testing.  
  Then, the next `<tab>` autocompleted "L" to "ListExamples", the `<tab>` after that autocompleted "ListExamplesT" to "ListExamplesTests.", which the `<backspace>` then turned into "ListExamplesTests".  
  The last `<enter>` ran the testers.
  ![Image](LapReportFourScreenshots/(3)RunningTestsTheyFail.png)
    
    
    
    
    
    
**4. Edit the code file to fix the failing test**  
  I typed "nano L" and then pressed `<tab>` and then typed ".j" and pressed `<tab>`.   
  Then I pressed `<enter>`.   
  Then I pressed `<control>` + `<shift>` + "-", and then typed "43" and pressed `<enter>`.   
  Then I pressed `<right-arrow>` 12 times, pressed `<backspace>` and typed "2".  
  Then I pressed `<control>` + "x", typed "y", and then pressed `<enter>`.  
  
  Pressing `<tab>` the first time autocompleted "nano L" to "nano ListExamples", and the second `<tab>` autocompleted "nano ListExamples.j" into "nano ListExamples.java", which was then run by the next `<enter>`.
  Pressing `<control>` + `<shift>` + "-" brought up a search bar to move to a given line, which I gave input as 43. Then pressing `<right-arrow>` 12 times brought me to the bug, where I could change the 1 to a 2 to fix the bug.  
  ![Image](LapReportFourScreenshots/(4)EditFilesToFixBug.png)
    
    
    
    
    
    
**5. Run the tests, demonstrating that they now succeed**  
  I pressed `<up-arrow>` three times and then pressed `<enter>`.  
  Then I pressed `<up-arrow>` three times again and pressed `<enter>`.  
  
  For the first `<up-arrow>` press, the command `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` was 3 back in my command history, so pressing `<up-arrow>` three times accessed it.  
  Pressing `<enter>` ran the command.  
  Then, the command `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` was 3 back in my command history, so pressing `<up-arrow>` three times accesssed it.  
  Pressing `<enter>` ran the command.  
  ![Image](LapReportFourScreenshots/(5)RunningTestsSuccessfully.png)
  
  
  
  
  
  
**6. Commit and push the resulting change to your Github account (you can pick any commit message!)**  
  I typed "git add L" and pressed `<tab>`, typed ".j" and then pressed `<tab>`, and then pressed `<enter>`.  
  Then I typed "git commit -m "Fixed an infinite loop bug on line 43"", pressed `<enter>`, and then typed "git push " and then "git@github.com:liamhardy742/lab7.git" (which I copied to clipboard via github).  
  Then I pressed `<enter>`, and I was done with the task.  
    
  The first `<tab>` autocompleted "git add L" to "git add ListExamples", the second `<tab>` autocompleted "git add ListExamples.j" to "git add ListExamples.java", and then `<enter>` ran that command. The next `<enter>` command ran the git commit command, and the one after that ran the git push command.
  ![Image](LapReportFourScreenshots/(6)gitAddCommitAndPush.png)
