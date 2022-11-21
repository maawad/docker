# FROM --platform=windows/amd64 mcr.microsoft.com/windows/servercore:ltsc2022
FROM --platform=windows/amd64 mcr.microsoft.com/windows/servercore:ltsc2019

LABEL maintainer="Muhammad Awad <mawad@ucdavis.edu>"

# Uses dism.exe to install the IIS role.
RUN dism.exe /online /enable-feature /all /featurename:iis-webserver /NoRestart

RUN powershell.exe -Command Start-Process c:\vcredist_x86.exe -ArgumentList '/quiet' -Wait

CMD [ "cmd" ]