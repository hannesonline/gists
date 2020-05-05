Cleaning up git branch
======================
    git reflog expire --expire-unreachable=now --all
    git gc --prune=now
Prüfen: `git fsck --lost-found`

Quelle: https://stackoverflow.com/questions/3765234/

Firefox: Drag & Drop-Fehler
===========================
    Firefox mit dem Kommando -no-deelevate starten
Quelle: https://support.mozilla.org/de/kb/windows-administrator-starterprozess-fehler-loesen

Office 2013 auf Win 10 schließt nach dem Öffnen wieder
======================================================
HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Common

Klicke den Schlüssel "Common" auf der linken Seite mit der rechten Maustaste an und wähle den Eintrag "Neu, Schlüssel". Gebe den Namen **Graphics** ein.

Klicke den Schlüssel "Graphics" auf der linken Seite mit der rechten Maustaste an und wähle den Eintrag "Neu, DWORD-Wert (32-bit)Schlüssel". Gebe den Namen **DisableHardwareAcceleration** ein. Klicke anschließend auf diesen neuen Wert "DisableHardwareAcceleration" und gebe den Wert 1 ein.

From: https://answers.microsoft.com/de-de/msoffice/forum/all/x/28e060ee-cb4d-4c5b-a024-81e583e1be9a

How do I turn off security warning in Firefox?
==============================================
![](https://media.prod.mdn.mozit.cloud/attachments/2017/03/15/14783/f743a72e2eb03169e0b7f83734312248/Insecure_Password_Console_Contextual_sm.png)
`security.insecure_field_warning.contextual.enabled`

Logon screensaver
=================
    [HKEY_USERS\.DEFAULT\Control Panel\Desktop]
    "SCRNSAVE.EXE"="C:\\Windows\\System32\\scrnsave.scr"
    "ScreenSaveActive"="1"
    "ScreenSaveIsSecure"="0"
    "ScreenSaveTimeOut"="10"

Configuring Apache
==================
    Alias /meinewelt "C:/Workspace/meinewelt"
    <Directory "C:/Workspace/meinewelt">
    	Require all granted
    	AllowOverride All
    </Directory>
    
    # PHP: Go for the Thread Safe version because Non Thread Safe does not have Apache DLL.
    LoadModule php7_module "C:/Program Files/PHP/php7apache2_4.dll" 
    AddType application/x-httpd-php .php
    PHPIniDir "C:/Program Files/PHP"

