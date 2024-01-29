# Utilisation de l'image .NET SDK pour la construction
FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build-env

WORKDIR /app

# Copie du fichier projet et restauration des dépendances
COPY Worker.csproj .
RUN dotnet restore

# Copie des autres fichiers du projet et publication
COPY . .
RUN dotnet publish -c release -o out

# Image runtime .NET pour l'exécution
FROM mcr.microsoft.com/dotnet/runtime:7.0

WORKDIR /app

# Copie des fichiers publiés depuis l'étape de construction
COPY --from=build-env /app/out .

# Point d'entrée du conteneur
ENTRYPOINT ["dotnet", "Worker.dll"]