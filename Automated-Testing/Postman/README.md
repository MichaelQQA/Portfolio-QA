#  Trello API Tests - CRUD Operations (Postman)

Zbiór automatycznych testów weryfikujących pełny cykl życia **Tablicy** w Trello API. Testy zostały zaprojektowane do uruchamiania w środowisku **Postman Collection Runner**.

##  Scenariusz Testowy 

Testy następują po sobie w sekwencji, wykorzystując dane przekazane między żądaniami:

1.  **GET Board:** Pobiera dane wszystkich tablic i sprawdza poprawność statusu (`200`).
2.  **POST Create Board:** Tworzy nową tablicę i zapisuje jej ID do zmiennej kolekcji (`boardID`). 
3.  **Weryfikacja POST:** Sprawdza poprawność kodu statusu (`200`), typu danych (`string`) oraz zgodność tytułu (`name`) z wartością wejściową.
4.  **PUT Update Board:** Edytuje tablicę o zapisanym `boardID`, zmieniając tytuł i opis.
5.  **Weryfikacja PUT:** Sprawdza poprawność kodu statusu (`200`) i zgodność nowego tytułu (`name`) oraz opisu (`desc`) z wartościami edytowanymi.
6.  **DELETE Board:** Sprawdza poprawność kodu statusu (`200`) i usuwa tablicę o zarejestrowanym (`boardID`).
7.  **GET Verification:** Próbuje pobrać usunięty zasób, oczekując kodu błędu (`404 Not Found`), co potwierdza skuteczne usunięcie.

##  Wymagane Zmienne 

Zmienne autoryzacyjne (`Key`, `Token`) muszą być ustawione w aktywnym środowisku aby zachować bezpieczeństwo.
(Pozostałe zmienne **Variables** są zainportowane w collections)

| Zmienna | Typ | Opis |
| :--- | :--- | :--- |
| `baseUrl-1.0` | Environment | Bazowy URL API Trello (np. `https://api.trello.com/1`) |
| **`Key`** | **Environment/Secret** | Klucz API do autoryzacji Trello. |
| **`Token`** | **Environment/Secret** | Token Access Token do autoryzacji Trello. |

---

##  Instrukcja Uruchomienia w Postmanie

1.  **Import Kolekcji:** W Postmanie, zaimportuj plik `./collections/Trello-Boards-crud.json`.
2.  **Import Środowiska:** Zaimportuj plik `./environments/Test-postman-environment.json`.
3.  **Uzupełnienie Sekretów:** W aktywnym środowisku, ręcznie uzupełnij pola **`Key`** i **`Token`** swoimi prywatnymi kluczami Trello.
4.  **Uruchomienie:** Użyj przycisku **Runner** i wybierz zaimportowaną kolekcję razem ze środowiskiem. Testy muszą być uruchamiane w kolejności.
