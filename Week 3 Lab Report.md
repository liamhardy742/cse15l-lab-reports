# The command that I will be choosing is grep.  
## The four options I will be researching are -rl, -cv, -n, and -i.
  
  

## The first option is -rl, which is a combination of the -r and -l options. This recursively searches the directory given as a command line argument (from the -r part), and prints the file names of the files that are found to contain the command line argument that grep is searching for (from the -l part).  
This option and it's use/description was sourced from [https://man7.org/linux/man-pages/man1/grep.1.html](https://man7.org/linux/man-pages/man1/grep.1.html)  
    
  
The first example is:
![Image](/LabReportThreeScreenshots/-rl1.png)
In this example, the command grep -rl "Hello" ./written_2 is searching all of the files in the written_2 directory recursively for the String "Hello", and returns the file names that contain the String. This is useful if you want to easily search an entire directory for files that contain a specific string and easily know the name and path of those files.

The second example is:
![Image](/LabReportThreeScreenshots/-rl2.png)
In this example, the command grep -rl "goodness" ./written_2 is searching all of the files in the written_2 directory recursively for the String "goodness", and returns the file names that contain the String. This is useful if you want to easily search an entire directory for files that contain a specific string and easily know the name and path of those files.
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
## The second option is -cv, which is a combination of the -c and the -v options. This prints the count of the files found (from the -c part), where the files found are files where no match is found (from the -v part).  
This option and it's use/description was sourced from [https://man7.org/linux/man-pages/man1/grep.1.html](https://man7.org/linux/man-pages/man1/grep.1.html)  
  
  
The first example is:
![Image](/LabReportThreeScreenshots/-cv1.png)
In this example, grep -cv "a" ./written_2/travel_guides/berlitz1/HistoryIndia.txt returns the number of lines in the txt file that do no contain the String "a". This option is useful for knowing how many lines do not contain a specific String in a txt file.

The second example is:
![Image](/LabReportThreeScreenshots/-cv2.png)
In this example, grep -cv " " ./written_2/travel_guides/berlitz1/HistoryIndia.txt returns the number of lines in the txt file that do no contain the String " ". This option is useful for knowing how many lines do not contain a specific String in a txt file.
\\  
\\
\\
\\
\\
\\
\\
\\
\\
\\

## The third option is -n, which modifies the output so that the user can see the line number that the match appears on for each of the files found.  
This option and it's use/description was sourced from [https://man7.org/linux/man-pages/man1/grep.1.html](https://man7.org/linux/man-pages/man1/grep.1.html)  
  
  
The first example is:
![Image](/LabReportThreeScreenshots/-n1.png)
In this example, grep -n "goodness" ./written_2/non-fiction/OUP/Kauffmen/ch8.txt is used to find all of the lines in the txt file that contain the String "goodness". In this case, there is 1 line that is printed out. This option is useful because it prints out the lines containing the String, and tell the user the line in the txt file where the String is.

The second example is:
![Image](/LabReportThreeScreenshots/-n2.png)
In this example, grep -n "birds" ./written_2/travel_guides/berlitz2/Bermuda-WhereToGo.txt is used to find all of the lines in the txt file that contain the String "birds". In this case, there are 3 lines that are all printed out. This option is useful because it prints out the lines containing the String, and tell the user the line in the txt file where the String is.
\\
\\
\\
\\
\\
\\
\\
\\
\\
\\

## The fourth option is -i which performs a normal grep search but ignores the case of the matching string it is looking for. For example, when looking for "CaliforniA", "california" would be found as a match.
This option and it's use/description was sourced from [https://man7.org/linux/man-pages/man1/grep.1.html](https://man7.org/linux/man-pages/man1/grep.1.html)  
  
  
The first example is:
![Image](/LabReportThreeScreenshots/-i1.png)
In this example, grep -i "california" ./written_2/travel_guides/berlitz2/California-WhatToDo.txt finds all of the lines in the txt file that contain the String "california" without regard to the case sensitivity of the String. These lines are then printed out. This is useful for when you are searching for a String file but don't care about uppercase versus lowercase, for example if you don't care if a word appears at the beginning or in the middle of a sentence.

The second example is:
![Image](/LabReportThreeScreenshots/-i2.png)
In this example, grep -i "nevada" ./written_2/travel_guides/berlitz2/California-WhatToDo.txt finds all of the lines in the txt file that contain the String "nevada" without regard to the case sensitivity of the String. These lines are then printed out. This is useful for when you are searching for a String file but don't care about uppercase versus lowercase, for example if you don't care if a word appears at the beginning or in the middle of a sentence.
