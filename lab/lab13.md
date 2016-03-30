## Chapter 13. User Manual

### Installation
Installing the POS Web Form is easy as it requires little work. To install, there are 5 steps.
- Make sure you can see all invisible Items. (Only required if copying files to different folder using a GUI. Important for .htaccess files)
- Copy all of the items into your web directory
- Modify the .htaccess in the page’s root folder. (ROOT/.htaccess)
- Modify the php-cgi.cgi file from ROOT/php-cgi to your server’s version of cgi.
- "chmod 755" -R the following directories
	- api
	- cgi-bin
	- frontend

### Form Sections Explained
- #### Student Info/Load
Students will fill out their information here. If they have previously saved a form, they can load their own by clicking on the load button. The password section is only required for saving. Therefore, you can load a form without a password, but you must have one to save.
#### Figure . Student Information Section
![student-information](img/student_information.png)
- #### Approved Transfer Credits
Students will select which type of graduate student they are. The max number of credits will change depending on which type they are. With that, they can start adding rows and adding classes. Note: the "Remove Row" button will remove the bottom-most row.
#### Figure . Approved Transfer Credits Section
![transfer-credit](img/transfer_credit.png)
- #### Foundational Corses
Students will chose whether they have to take the class (required) or they have had it waved. There are two buttons at the bottom allowing students to quickly set all the items as waived or required. 
#### Figure . Foundational Courses Section
![foundational_courses](img/foundational_courses.png)
- #### COEN Core
Students will be choosing whether or not they have had the core classes transferred or waived. If neither, they should leave the courses left as "required".
#### Figure . Computer Science and Engineering Core Section
![coen_core](img/coen_core.png)
- #### Track Courses
Students will fill out which courses they are planning on taking while a graduate student at Santa Clara University. Add and remove row work the same as the Approved Transfer Credits section.
#### Figure . Track Courses Section
![track_courses](img/track_courses.png)	
- #### Total Units, Save, Share, and Print
Students will be able to see their total amount of units at the bottom of the screen. Under it, there will be the options: save, share, and print. When you click save, their will be a pop-up stating whether or not saving was successful. When you click share, a pop-up will appear with a link to the printable form that you can send to anyone. Clicking on the print button will open up a new tab with the printable form. From there, you can print it out, save it as a PDF, etc.
#### Figure . Total Units Indicator and Save, Print, and Share Options
![save-share-print](img/save_share_print.png)
#### Figure . The Share Pop-up
![share](img/share.png)