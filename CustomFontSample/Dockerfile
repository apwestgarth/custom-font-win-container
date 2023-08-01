#Depending on the operating system of the host machines(s) that will build or run the containers, the image specified in the FROM statement may need to be changed.
#For more information, please see https://aka.ms/containercompat 

FROM mcr.microsoft.com/dotnet/framework/aspnet:4.8-windowsservercore-ltsc2019
# If building on a Windows 11/Windows Server 2022 host could use smaller WS2022 image
# FROM mcr.microsoft.com/dotnet/framework/aspnet:4.8-windowsservercore-ltsc2022
ARG source
WORKDIR /inetpub/wwwroot
COPY ${source:-obj/Docker/publish} .
RUN ${source:-obj/Docker/publish/InstallFont.ps1}
