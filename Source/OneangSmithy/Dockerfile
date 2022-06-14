#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM mcr.microsoft.com/dotnet/aspnet:3.1
COPY . /app
WORKDIR /app
#COPY ["Startup.cs", "/SSL/bundle.pfx"]
ENV ASPNETCORE_URLS http://*:8778;https://*:8779
ENV ASPNETCORE_HTTPS_PORT=8779
ENV ASPNETCORE_Kestrel__Certificates__Default__Password=z0mk1n9
ENV ASPNETCORE_Kestrel__Certificates__Default__Path=/SSL/bundle.pfx

EXPOSE 8778
EXPOSE 8779

ENTRYPOINT ["dotnet", "OneangSmithy_Server.dll"]