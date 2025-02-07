# Data Cleaning in Excel

- Course: [Axel The Analyst - Cleaning Data in Excel | Excel Tutorials for Beginners](https://www.youtube.com/watch?v=_jmiEGZ6PIY)
- Source file: [https://www.youtube.com/watch?v=_jmiEGZ6PIY](https://github.com/AlexTheAnalyst/Excel-Tutorial/blob/main/Data%20Cleaning%20Excel%20Tutorial.xlsx)
- Cleaned file: https://1drv.ms/x/c/315a2e7b2c65925e/EZ1sU5PuxwJDv__HNrjtVloBFru5VaN7D2KIFiX85ABspA?e=PTKMbA

# Purpose
To get an overview how analyst uses Excel for data cleaning.

# Steps
1. Find if there are any duplicates
    - <em>Data -> Remove Duplicates</em>.
2. Cleaning the President column
    - UPPER/LOWER
    - PROPER - each word starts with a capital letter.
4. Cleaning the Party column
    - Removing blank fields
    - Whig/Republican/Democrats - choosing one version or correcting spelling mistakes.
    * Democrat - Republic - not familiar with history of USA - maybe this distinction is needed
6. Cleaning the Vice column
   - TRIM - cleans up the spaces before, between duplicate spaces, and after
7. Cleaning the Salary column
    - Since $ isn't useful in DB, changed the column to a number.
8. Cleaning the Date columns
    - Format to Short Date (dd.mm.yyyy).
10. At the moment I kept all columns. But as keeping the source file and actual working file separatly - probably columns A, C, G, E won't be needed in cleaned file.

-- After using Google Sheets, I changed following:

11. In Google Sheets, trimmed in the Prior column "Democratic- Republican". Correcting hint dissappeared, but it kept the space before "Republican". In Excel, I used CTRL+H and changed it to "Democratic-Republican".
12. And there was also encoding problem in Prior column:
    
![image](https://github.com/user-attachments/assets/bca54a55-7ba4-4e12-99db-f811b8121b96)

There are several solutions to do it. I exported the .csv file, saved it in VSCode as .xls. Then uploaded in the desktop version of Excel again. The program opened the Export Wizard:
- Choose the UTF-8 encoding.
- Check the checkmark to mark column headers are in file.
- And choose the correct delimiter. In my case ";".



# Lessons
1. PROPER is an interesting finding. Upper/lower or something similar is used in different programming languages. But writing every word with first capital letter - you have to really search or know it because different wording is used e.g. capitalize vs proper.
2. Finding and replacing strings can be very tricky. Column name or some part of word which does not need changing can be replaced without noticing. What fun to correct, yeah!
3. The biggest lesson came actually after finishing tutorial. I uploaded it to **Google Sheets** and I later opening it, I saw next picture:

![Kuvatõmmis 2025-02-07 153015](https://github.com/user-attachments/assets/e3c069ba-c0a0-4a27-b46a-f8275833eca0)

- First time I noticed this <em>Cleanup section</em>. I do not know what caused this pop-up, but it can also be found <em>Data -> Data Cleanup</em>.
- Columns E/G can be ignored, because these are orignal columns, but rows 29-30 got my attention (marked yellow on the pic). Why did not Excel remove one of them as a duplicate? A little bit digging and the answer was in column E: a spelling mistake in word "democratic" was the reason. As my flow was following: removing duplicates -> removing spelling mistakes ->  Excel coudn't remove because the rows were different.
-  The workflow should have been: <em> remove duplicates -> manipulating strings (e.g. spelling mistakes, trimming, choosing on standard-word, replacing) -> remove duplicates once again </em>. 
-  If the dataset is not big use different tools to cross-check yourself.
  
