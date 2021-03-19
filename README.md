# windows-containers

Reference:  https://docs.microsoft.com/en-us/virtualization/windowscontainers/quick-start/set-up-environment?tabs=Windows-Server

Install-Module -Name DockerMsftProvider -Repository PSGallery -Force
Need to answer Y

Install-Package -Name docker -ProviderName DockerMsftProvider
Need to answer A

Restart-Computer -Force

This tag works
docker pull mcr.microsoft.com/windows/nanoserver:1809

You don't really need to specify cmd.exe

docker run -it --name=nano --rm mcr.microsoft.com/windows/nanoserver:1809 cmd.exe

Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

