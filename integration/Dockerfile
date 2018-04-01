# Build stage
FROM microsoft/dotnet:2-sdk AS build-env
 # - generic folder name
WORKDIR /integration  

# restore
COPY integration.csproj .
RUN dotnet restore

# copy src
COPY . .
ENTRYPOINT [ "dotnet", "test" ]