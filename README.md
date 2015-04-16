YouTrack Worklog Viewer
=======================

# About this software
YouTrack is a commercial issue tracker created by [Jetbrains](https://www.jetbrains.com/youtrack/) where you also have the possibility to log your time spent on each individual issue/task. Unfortunately, if you are like me and don't book your time right away, there is limited options to get an overview of how much time you have already booked on every single day of the week (addressed in [this issue](https://youtrack.jetbrains.com/issue/JT-29224)).

With this tool you can now overcome this issue. It let's you create your personal time tracking report as depicted in this screenshot

![Screenshot of the report](https://raw.githubusercontent.com/pbauerochse/youtrack-worklog-viewer/master/screenshot.png) (*Issues column has been obfuscated for the screenshot*)

## How does it work?
You simply enter the URL to your YouTrack installation, and your own login data at the settings screen, select the reporting range in the main window and click on the "Download worklogs" button. That's it!

## FAQ

**What are the requirements?**

*You need to have Java 8 installed. The application has been tested with a Java version >= 1.8.0_25 on a Mac and Linux computer. Also you need an account to the YouTrack installation you want to access, with the right to create a time report*

**How do I start the application?**

*Simply open up your terminal/console and start the application with `java -jar youtrack-worklog-viewer-1.1.jar` or right click the file and select `Open with...` and then select the path to your java executable*

**Where are the settings stored?**

*The worklog viewer creates a file in your user home directory with the name `youtrack-worklog.properties`. All your settings are in there. Though - or because - it is a plain text file, your YouTrack password will not be stored in cleartext, instead it will be encrypted before storing it in that file. Please note: even though the password is encrypted, it is not impossible for anyone with access to your computer to decrypt the password*

**Which YouTrack versions are supported?**

*Since I only have access to a YouTrack 6 installation, this tool has only been tested on that version. I can not guarantee, that it will work with any other version*

**How does the tool get the data from YouTrack?**

*The application logs on to your YouTrack installation using the regular YouTrack API and the data provided by you in the settings screen. It then creates a temporary time report and downloads it as .csv file. The data in that file is being processed and displayed in the main window. After retrieving the data, the temporarily created report will be deleted to prevent polluting your reports section*

**What reporting options are available?**

*You can create a report for the current week, previous week, current month and previous month. You can also enter your daily work hours to adjust the time format (e.g. 9 booked hours will be presented in an 8 hour workday with `1d 1h` and in an 9 hour workday with `1d`)*  