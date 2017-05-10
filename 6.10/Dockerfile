FROM windowsservercore

ENV NPM_CONFIG_LOGLEVEL info  
ENV NODE_VERSION 6.10.3

RUN powershell -Command "wget -Uri https://nodejs.org/dist/v%NODEJS_VERSION%/node-vNODEJS_VERSION%-x64.msi -OutFile node.msi -UseBasicParsing"

RUN msiexec.exe /q /i node.msi

CMD [ "node" ]