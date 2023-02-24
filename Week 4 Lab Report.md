**1. Log into ieng6**  
  I typed "ssh cs15lwi23afd@ieng6.ucsd.edu" and then pressed `<enter>`
  ![Image](LapReportFourScreenshots/(1)SshIntoIeng6.png)
  
**2. Clone your fork of the repository from your Github account**  
  I typed "git clone https://github.com/liamhardy742/lab7" and then pressed `<enter>`
  ![Image](LapReportFourScreenshots/(2)GitCloneRepo.png)
  
**3. Run the tests, demonstrating that they fail**  
  I typed "cd l" and pressed `<tab>` and then pressed `<enter>`.
  I typed "javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java" (by copy pasting from the course website week 3) and then pressed `<enter>`.
  Then I typed "java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore" (By copy pasting from the course website) and typed a space and then L `<tab>` T `<tab>` j `<tab>` and then pressed `<enter>`
  ![Image](LapReportFourScreenshots/(3)RunningTestsTheyFail.png)
  
**4. Edit the code file to fix the failing test**  
  I typed "nano L" and then pressed `<tab>` and then typed ".j" and pressed `<tab>`. 
  Then I pressed `<enter>`. 
  Then I pressed `<control>` + `<shift>` + "-", and then typed "43" and pressed `<enter>`. 
  Then I pressed `<right arrow>` 12 times, pressed `<backspace>` and typed "2".
  Then I pressed `<control>` + "x", typed "y", and then pressed `<enter>`.
  ![Image](LapReportFourScreenshots/(4)EditFilesToFixBug.png)
  
**5. Run the tests, demonstrating that they now succeed**  
  I pressed `<up-arrow>` three times and then pressed `<enter>`.
  Then I pressed `<up-arrow>` three times again and pressed `<enter>`.
  ![Image](LapReportFourScreenshots/(5)RunningTestsSuccessfully.png)

**6. Commit and push the resulting change to your Github account (you can pick any commit message!)**  
  I typed "git add L" and pressed `<tab>`, typed ".j" and then pressed `<tab>`, and then pressed `<enter>`.
  Then I typed "git commit -m "Fixed an infinite loop bug on line 43"", and then typed "git push " and then "git@github.com:liamhardy742/lab7.git" (which I copied to clipboard via github).
  Then I pressed `<enter>`, and I was done with the task.
  ![Image](LapReportFourScreenshots/(6)gitAddCommitAndPush.png)
