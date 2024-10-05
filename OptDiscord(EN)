@ECHO OFF
:menu
color 0F
cls
echo (Discord. lxt3z_)
echo ------------------------------------
echo             MENU
echo ------------------------------------
echo 1. Garbage Cleaning
echo 2. Removing unnecessary languages
echo 3. Install OpenASAR
echo 4. Disable Discord
echo 5. Enable Discord
echo 6. Disable Auto-Update Discord
echo 7. Exit
echo ------------------------------------
set /p choice="Select a menu item (1-7): "

if "%choice%"=="1" goto cleanup
if "%choice%"=="2" goto remove_languages
if "%choice%"=="3" goto install_openasar
if "%choice%"=="4" goto shutdown_discord
if "%choice%"=="5" goto start_ds
if "%choice%"=="6" goto autoupdate_off
if "%choice%"=="7" exit

goto menu

rem Garbage Cleaning
:cleanup
C:\Windows\System32\TASKKILL.exe /f /im Discord.exe > nul 2> nul
color 0F
cls 
echo Garbage Cleaning...
setlocal

set "directory=%USERPROFILE%\AppData\Local\Discord\app-*"
set "roamingDir=%USERPROFILE%\AppData\Roaming\discord"

rem Local\Discord
del "%directory%\vulkan-1.dll" 2>nul
del "%directory%\vk_swiftshader_icd.json" 2>nul
del "%directory%\Discord.sig" 2>nul

rem Roaming\discord
rmdir /s /q "%roamingDir%\GPUCache" 2>nul
rmdir /s /q "%roamingDir%\Cache" 2>nul
rmdir /s /q "%roamingDir%\DawnWebGPUCache" 2>nul
rmdir /s /q "%roamingDir%\DawnGraphiteCache" 2>nul
rmdir /s /q "%roamingDir%\CrashPad" 2>nul
rmdir /s /q "%roamingDir%\component_crx_cache" 2>nul
rmdir /s /q "%roamingDir%\VideoDecodeStats" 2>nul
del "%USERPROFILE%\AppData\Local\discord\*.log" /s /q

color 0A
cls
echo Cleaning is complete.
pause
goto menu

rem Delete Language
:remove_languages
color 0F
cls
echo Removing unnecessary languages...
taskkill /IM discord.exe /F
setlocal enabledelayedexpansion
set "directory=C:\Users\lxt3z\AppData\Local\Discord\app-*\locales"
set "files_removed=0"
for %%F in ("%directory%\*") do (
    if /I not "%%~nxF"=="en.pak" (
        del "%%F"
        set /a files_removed+=1
    )
)

set "remaining_files=0"
for %%F in ("%directory%\*") do (
    if /I not "%%~nxF"=="ru.pak" (
        set /a remaining_files+=1
    )
)

cls
color 0A
cls

if !remaining_files! equ 0 (
    echo All languages have been successfully deleted.
) else (
    color 0C
    cls
    echo Some languages could not be found and deleted!
)
color 0F
pause
goto menu

rem Install OpenASAR
:install_openasar
color 0F
echo Intsalling OpenASAR...
taskkill /IM discord.exe /F
C:\Windows\System32\TASKKILL.exe /f /im Discord.exe > nul 2> nul
color 0F
cls
echo Intsalling OpenASAR...
copy /y "%localappdata%\Discord\app-*\resources\app.asar" "%localappdata%\Discord\app-*\resources\app.asar.backup" > nul 2> nul
if exist "%localappdata%\Discord\app-*\resources\_app.asar" copy /y "%localappdata%\Discord\app-*\resources\_app.asar" "%localappdata%\Discord\app-*\resources\app.asar.backup" > nul 2> nul
if exist "%localappdata%\Discord\app-*\resources\app.asar.orig" copy /y "%localappdata%\Discord\app-*\resources\app.asar.orig" "%localappdata%\Discord\app-*\resources\app.asar.backup" > nul 2> nul

powershell -Command "Invoke-WebRequest https://github.com/GooseMod/OpenAsar/releases/download/nightly/app.asar -OutFile \"$Env:LOCALAPPDATA\Discord\app-*\resources\app.asar\"" > nul 2> nul

if exist "%localappdata%\Discord\app-*\resources\app.asar" powershell -Command "Invoke-WebRequest https://github.com/GooseMod/OpenAsar/releases/download/nightly/app.asar -OutFile \"$Env:LOCALAPPDATA\Discord\app-*\resources\app.asar\"" > nul 2> nul
if exist "%localappdata%\Discord\app-*\resources\app.asar" powershell -Command "Invoke-WebRequest https://github.com/GooseMod/OpenAsar/releases/download/nightly/app.asar -OutFile \"$Env:LOCALAPPDATA\Discord\app-*\resources\app.asar\"" > nul 2> nul
if exist "%localappdata%\Discord\app-*\resources\app.asar" powershell -Command "Invoke-WebRequest https://github.com/GooseMod/OpenAsar/releases/download/nightly/app.asar -OutFile \"$Env:LOCALAPPDATA\Discord\app-*\resources\app.asar\"" > nul 2> nul
if exist "%localappdata%\Discord\app-*\resources\app.asar" powershell -Command "Invoke-WebRequest https://github.com/GooseMod/OpenAsar/releases/download/nightly/app.asar -OutFile \"$Env:LOCALAPPDATA\Discord\app-*\resources\app.asar\"" > nul 2> nul
if exist "%localappdata%\Discord\app-*\resources\app.asar" powershell -Command "Invoke-WebRequest https://github.com/GooseMod/OpenAsar/releases/download/nightly/app.asar -OutFile \"$Env:LOCALAPPDATA\Discord\app-*\resources\app.asar\"" > nul 2> nul
if exist "%localappdata%\Discord\app-*\resources\app.asar" powershell -Command "Invoke-WebRequest https://github.com/GooseMod/OpenAsar/releases/download/nightly/app.asar -OutFile \"$Env:LOCALAPPDATA\Discord\app-*\resources\app.asar\"" > nul 2> nul
if exist "%localappdata%\Discord\app-*\resources\app.asar" powershell -Command "Invoke-WebRequest https://github.com/GooseMod/OpenAsar/releases/download/nightly/app.asar -OutFile \"$Env:LOCALAPPDATA\Discord\app-*\resources\app.asar\"" > nul 2> nul
if exist "%localappdata%\Discord\app-*\resources\app.asar" powershell -Command "Invoke-WebRequest https://github.com/GooseMod/OpenAsar/releases/download/nightly/app.asar -OutFile \"$Env:LOCALAPPDATA\Discord\app-*\resources\app.asar\"" > nul 2> nul
if exist "%localappdata%\Discord\app-*\resources\app.asar" powershell -Command "Invoke-WebRequest https://github.com/GooseMod/OpenAsar/releases/download/nightly/app.asar -OutFile \"$Env:LOCALAPPDATA\Discord\app-*\resources\app.asar\"" > nul 2> nul
if exist "%localappdata%\Discord\app-*\resources\_app.asar" powershell -Command "Invoke-WebRequest https://github.com/GooseMod/OpenAsar/releases/download/nightly/app.asar -OutFile \"$Env:LOCALAPPDATA\Discord\app-*\resources\_app.asar\"" > nul 2> nul
if exist "%localappdata%\Discord\app-*\resources\app.asar.orig" powershell -Command "Invoke-WebRequest https://github.com/GooseMod/OpenAsar/releases/download/nightly/app.asar -OutFile \"$Env:LOCALAPPDATA\Discord\app-*\resources\app.asar.orig\"" > nul 2> nul
color 0A
cls
echo OpenASAR has been successfully installed!!
pause
goto menu

rem Disable Discord
:shutdown_discord
color 0F
echo Disabling Discord...
tasklist | findstr /I "discord.exe" >nul

if errorlevel 1 (
    color 0C
    cls
    echo Discord not started!
    pause
    goto menu
)
taskkill /IM discord.exe /F
color 0A
echo Discord successfully stopped!
pause
goto menu

:start_ds
cls
color 0F
echo Checking the status Discord...

tasklist | findstr /I "Discord.exe" >nul
if not errorlevel 1 (
    color 0C
    cls
    echo Discord already launched!
    pause
    goto menu
)
cls
echo Starting Discord...
start "" "%localappdata%\Discord\Update.exe" --processStart Discord.exe > nul 2> nul
color 0A
cls
echo Discord successfully launched!
pause
goto menu


:autoupdate_off
setlocal
color 0F
cls

set "filePath=C:\Users\lxt3z\AppData\Local\Discord\app-*\resources\build_info.json"
set "tempFile=%TEMP%\build_info_temp.json"

copy "%filePath%" "%tempFile%" >nul

powershell -Command "(Get-Content '%filePath%') -replace '\"newUpdater\": true', '\"newUpdater\": false' | Set-Content '%filePath%'"

fc "%tempFile%" "%filePath%" >nul
if errorlevel 1 (
    color 0A
    cls
    echo Auto-updates have been successfully turned off! ✅
) else (
    color 0C
    cls
    echo Auto-updates have not been disabled! ❌
)

del "%tempFile%" >nul
cls
goto menu
