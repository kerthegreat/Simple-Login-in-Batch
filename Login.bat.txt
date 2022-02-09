@echo off
chcp 65001 >nul
color 5
echo ██╗      ██████╗  ██████╗ ██╗███╗   ██╗
echo ██║     ██╔═══██╗██╔════╝ ██║████╗  ██║
echo ██║     ██║   ██║██║  ███╗██║██╔██╗ ██║
echo ██║     ██║   ██║██║   ██║██║██║╚██╗██║
echo ███████╗╚██████╔╝╚██████╔╝██║██║ ╚████║
echo ╚══════╝ ╚═════╝  ╚═════╝ ╚═╝╚═╝  ╚═══╝                             
echo.
set /p username=Enter User:
if %username% == anon goto pass
if not %username%==anon goto loginerror

:pass
set /p password=Password: 
if %password% == pass goto loading
if not %password% == pass loginerror

:loginerror
echo Error: Invalid Username or Password!
pause >nul
cls

::fake loading, u can remove this if you want

:loading
cls
echo connecting to server...
timeout /t 3 >nul
echo Connected to [122.122.122.122]
timeout /t 2 >nul
goto welcome

:welcome
cls
echo ██╗    ██╗███████╗██╗      ██████╗ ██████╗ ███╗   ███╗███████╗
echo ██║    ██║██╔════╝██║     ██╔════╝██╔═══██╗████╗ ████║██╔════╝
echo ██║ █╗ ██║█████╗  ██║     ██║     ██║   ██║██╔████╔██║█████╗  
echo ██║███╗██║██╔══╝  ██║     ██║     ██║   ██║██║╚██╔╝██║██╔══╝  
echo ╚███╔███╔╝███████╗███████╗╚██████╗╚██████╔╝██║ ╚═╝ ██║███████╗
echo  ╚══╝╚══╝ ╚══════╝╚══════╝ ╚═════╝ ╚═════╝ ╚═╝     ╚═╝╚══════╝                
echo.

echo Welcome %username%!
pause >nul