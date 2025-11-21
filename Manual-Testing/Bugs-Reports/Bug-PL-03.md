**Tytuł**

Brak funkcjonalności wyszukiwarki oraz błąd wyświetlania stopki.

**Opis**

Moduł wyszukiwania w menu bocznym (hamburger menu) nie zwraca wyników wyszukiwania, jedynie przeładowuje stronę główną z parametrem w URL. 
Dodatkowo, w tym widoku ze stopki znika obowiązkowa informacja o reCAPTCHA i polityce prywatności.

**Priorytet**

P2 - Poważny

**Środowisko**

* Urządzenie: PC
* System operacyjny: Windows 11
* Przeglądarki: Chrome/Firefox

**Kroki do Reprodukcji**

* Otwórz stronę: https://drturowski.pl/
* Kliknij ikonę "MENU" w prawym górnym rogu.
* W polu wyszukiwania na dole paska bocznego wpisz dowolną frazę (np. "test") i naciśnij Enter.
* Przeskroluj stronę na sam dół do stopki.

**Rzeczywisty Rezultat**

Brak wyników wyszukiwania (wyświetla się strona główna z parametrem /?s=test).
W stopce brakuje tekstu: "Ta strona jest chroniona przez reCAPTCHA i Google Polityka prywatności i Warunki korzystania z usługi".

**Oczekiwany Rezultat**

Wyszukiwarka zwraca listę wyników pasujących do frazy LUB informację "brak wyników", a stopka (w tym informacje prawne) wyświetla się poprawnie.

[Screenshot](../../Assets/Screenshots/02-bug-screen.jpg)
