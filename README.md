# workshop

## NAGLOWEK

Aplikacja konsolowa .NET stworzenia podczas laboratorium.

## Uruchomienie komendy

\`\`\`bash
dotnet run
\`\`\`

## Kontakt

Zespół: Warsztat Programisty
Autor: Student

## Continuous Integration

Projekt jest automatycznie sprawdzany przez GitHub Actions.

### Uruchamianie

Workflow uruchamia się po:

- Push do gałęzi `main`.
- Pull request do gałęzi `main`.
- Ręcznym uruchomieniu (`workflow_dispatch`).

### Konfiguracja

- Projekt: `workshop.csproj`
- .NET: `10.0.x`
- Konfiguracja: `Release`
- Runner: `ubuntu-latest`

### Automatyczne kontrole

1. Sprawdzenie struktury repozytorium (plik projektu i README.md).
2. Przywracanie zależności (`dotnet restore`).
3. Budowanie projektu (`dotnet build`).
4. Publikowanie aplikacji (`dotnet publish`).
5. Przesyłanie artefaktu.
6. Uruchomienie aplikacji (`dotnet run`).

### Artefakty

- Nazwa: `app-${{ github.sha }}`
- Lokalizacja: `./artifacts/app`
- Czas przechowywania: 7 dni.

### Logi i artefakty

Wyniki dostępne są w repozytorium GitHub w zakładce **Actions**. Logi znajdują się w szczegółach poszczególnych kroków, a artefakty na dole strony uruchomienia workflow.
