# Data Cleaning in Excel

- Course: [Axel The Analyst - Cleaning Data in Excel | Excel Tutorials for Beginners](https://www.youtube.com/watch?v=_jmiEGZ6PIY)
- Source file: [https://www.youtube.com/watch?v=_jmiEGZ6PIY](https://github.com/AlexTheAnalyst/Excel-Tutorial/blob/main/Data%20Cleaning%20Excel%20Tutorial.xlsx)

# Purpose
To get overview how analyst use Excel for data cleaning.

# Steps
1. Find if there are any duplicates
    - Data - Remove Duplicates
2. Cleaning President Column
    - UPPER/LOWER/
    - PROPER - each word starts with capital letter.
4. Cleaning Party Column
    - removing blank fields
    - Whig/Republican/Democrats - choosing one if several versions or correcting spelling mistakes.
    * Democrat - Republic - not familiar with history of USA - maybe this distinction is needed
6. Cleaning Vice Column
   - TRIM - cleans up the spaces before, between duplicate space, after
7. Cleaning Salary Column
    - As $ isn't useful in DB then changed the column to number.
8. Cleaning Date Columns
    - From text -> Short Date (dd.mm.yyyy).
9. At the moment I kept all columns. But as keeping the source file and actual working file separatly - probably columns A, C, G, E won't be needed in cleaned file.
-- After using Google Sheets made also following:
10. In Google Sheets trimmed in Prior Column "Democratic- Republican". Correcting hint dissappeared but it kept the space before "Republican". In Excel used CTRL+H and changed it to "Democratic-Republican".
11.     


# Lessons
1. PROPER is interesting finding. Upper/lower or something similar are used in different programming languages. But write every word in capital letter - you have to really search or know it because diffrent wording is there e.g. capitalize vs proper.
2. Finding and replacing strings can be very tricky. Column name or some part of word which does not need changing can be replacing without noticing. What fun to correct, yeaah!
3. The biggest lesson came actually after finishing tutorial. I uploaded it to **Google Sheets** and then I later opened it I saw next picture:

![Kuvatõmmis 2025-02-07 153015](https://github.com/user-attachments/assets/e3c069ba-c0a0-4a27-b46a-f8275833eca0)

- First time I noticed this <em>Cleanup section</em>. I do not know what caused this pop-up, but it can be also found <em>Data -> Data Cleanup</em>.
- Columns E/G can be ignored, because these are orignal columns, but rows 29-30 got my attention (marked yellow on the pic). Why Excel didn't remove one of them as duplicate? A little bit digging and the answer was in column E: spelling mistake in word "democratic" was the reason. As my flow was following: removing duplicates -> removing spelling mistakes ->  Excel coudn't remove because the rows were different.
**The Biggest Takeway**
-  Workflow should be: <em> remove duplicates -> manipulating strings (e.g. spelling mistakes, trimming, choosing on standard-word, replacing) -> remove duplicates once again </em>. 
-  If the dataset isn't big use different tools to control yourself.
  
