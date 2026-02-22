# Dockerfile Server1
FROM ubuntu:22.04

RUN apt-get update && apt-get install -y \
    wget \
    apt-transport-https \
    dotnet-sdk-9.0 \
    && rm -rf /var/lib/apt/lists/*
WORKDIR /app
COPY . .

RUN dotnet build -c Release
ENTRYPOINT ["dotnet", "bin/Release/net9.0/Server0App.dll"]
