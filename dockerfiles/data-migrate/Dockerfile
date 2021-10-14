FROM mcr.microsoft.com/dotnet/core/sdk:3.1-buster AS build
RUN dotnet tool install --global dotnet-ef --version 3.1.2
ENV PATH="${PATH}:/root/.dotnet/tools"

WORKDIR /src
COPY ["MySqlDotnetCore/MySqlDotnetCore.csproj", "MySqlDotnetCore/"]
COPY . .
WORKDIR "/src/MySqlDotnetCore"
CMD ["dotnet", "ef","database", "update"]

