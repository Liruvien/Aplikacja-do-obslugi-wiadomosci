# Warsztat – Aplikacja do obsługi wiadomości

## Opis

Program konsolowy pozwalający wysyłać i odczytywać wiadomości między użytkownikami. 
Aplikacja wykorzystuje bibliotekę `argparse` do parsowania argumentów wprowadzonych przez użytkownika i wykonania odpowiednich akcji, takich jak wysyłanie wiadomości, listowanie wiadomości czy edytowanie wiadomości.

## Funkcjonalności

Aplikacja oferuje następujące funkcje:
- Wysłanie wiadomości do innego użytkownika.
- Wyświetlenie wszystkich wiadomości danego użytkownika.
- Sprawdzenie, czy użytkownik i hasło są poprawne przed wykonaniem akcji.

## Wymagania

Aplikacja wymaga następujących bibliotek: `argparse`, `psycopg2`, `clcrypto`.

## Instalacja aplikacji

1. Sklonuj repozytorium:
    ```bash
    git clone https://github.com/TwojeRepozytorium.git
    cd TwojeRepozytorium
    ```
## Uruchomienie aplikacji

# Przykładowe uruchomienie aplikacji:
    ```bash
    python app.py -u testuser -p testpassword -l
    ```
Aplikacja powinna być uruchamiana z linii poleceń z odpowiednimi argumentami. Argumenty do aplikacji są następujące:

- `-u`, `--username` – nazwa użytkownika, który chce wykonać akcję (np. wysłać wiadomość, wylistować wiadomości),
- `-p`, `--password` – hasło użytkownika, do autentykacji,
- `-t`, `--to` – nazwa użytkownika, do którego ma zostać wysłana wiadomość,
- `-s`, `--send` – treść wiadomości do wysłania,
- `-l`, `--list` – flaga do wylistowania wszystkich wiadomości użytkownika.

### Przykłady uruchomienia

- **Listowanie wiadomości**:
  Aby wyświetlić wszystkie wiadomości użytkownika, użyj następującego polecenia:
  ```bash
  python app.py -u username -p password -l
   ```
### Przykładowe wysyłanie wiadomości:
  ```bash
  python app.py -u testuser -p testpassword -t recipientuser -s "Test message"
   ```