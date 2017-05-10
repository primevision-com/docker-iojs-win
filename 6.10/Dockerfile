FROM microsoft/windowsservercore

ENV NPM_CONFIG_LOGLEVEL info  
ENV NODE_VERSION 6.10.3

RUN powershell -Command "Set-ItemProperty -Path 'HKLM:\SYSTEM\CurrentControlSet\Services\Dnscache\Parameters' -Name ServerPriorityTimeLimit -Value 0 -Type DWord"

RUN powershell -Command "Invoke-WebRequest https://nodejs.org/dist/v$($env:NODE_VERSION)/node-v$($env:NODE_VERSION)-x64.msi -UseBasicParsing -OutFile node.msi"

RUN msiexec.exe /q /i node.msi

CMD [ "node" ]