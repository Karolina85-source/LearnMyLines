LearnMyLines

LearnMyLines to aplikacja wspierająca aktorów w nauce scenariusza na pamięć. Pomaga w efektywnym opanowaniu własnych kwestii oraz w oswojeniu się z dialogami partnerów poprzez interaktywne ćwiczenia.

Główne funkcjonalności

Importowanie scenariusza z pliku lub ręczne wpisanie tekstu Podział dialogu na kwestie aktora i partnerów Tryb nauki polegający na ukrywaniu części tekstu i odsłuchiwaniu nagrań Interaktywna symulacja dialogów z wirtualnym partnerem Historia sesji zapisująca postępy w nauce

Technologie

Projekt wykorzystuje następujące technologie Python framework Django SQLite lub PostgreSQL jako baza danych HTML i CSS jako podstawowy frontend

Instalacja

Aby uruchomić projekt lokalnie należy sklonować repozytorium i przejść do jego katalogu git clone https://github.com/twoje-repo/learnmylines.git cd learnmylines

Następnie należy zainstalować wymagane zależności pip install -r requirements.txt

Uruchomienie aplikacji python manage.py runserver

Projekt można uruchomić w przeglądarce pod adresem http://127.0.0.1:8000/

Plan implementacji

Utworzenie podstawowych modeli w Django Obsługa scenariuszy z możliwością importowania i edycji System nauki wykorzystujący tryb ukrywania i powtarzania tekstu Interaktywna symulacja dialogów Optymalizacja wyglądu i funkcjonalności aplikacji

Funkcjonalności aplikacji
 
1. Importowanie scenariusza
Użytkownik zaczyna od dodania swojego pliku (.txt, .pdf, .docx).

Aplikacja automatycznie rozpoznaje role i dzieli tekst na wypowiedzi poszczególnych postaci.

Użytkownik może edytować role i tekst, jeśli coś zostało źle rozpoznane.

Widok:
 "Dodaj scenariusz" → Wybierz plik → Załaduj → Przypisz role → Zapisz.

2. Tryb nauki scenariusza
Twoje kwestie są wyświetlane.

Kwestie partnerów są odtwarzane (np. w różnych emocjach: radość, złość, smutek).

Możesz:

Pauzować

Przewijać

Odtwarzać fragmenty wielokrotnie

Wskaźnik postępu: np. "3/10 scen przećwiczonych".

Widok:
 Start próby → Odtwarzanie partnerów → Mówisz swoją kwestię → Wskaźnik postępu.

3. Analiza błędów
Po zakończeniu próby aplikacja:

Porównuje Twój tekst z oryginalnym scenariuszem.

Pokazuje:

Pominięte słowa

Zmiany w tekście

Sugestie poprawy: np. "Uwaga na pomyłkę w 2. scenie".

Widok:
 Podsumowanie po próbie → Lista błędów → Wskazówki.

4. Zadania emocjonalne
Aplikacja proponuje:

"Powiedz tę kwestię jakbyś był bardzo zdenerwowany."

"Spróbuj radośnie!"

Możesz ćwiczyć tę samą scenę w różnych wariantach emocji.

Zapis różnych emocjonalnych wersji do porównania.

Widok:
 Wybór emocji → Ćwiczenie → Zapis prób.

5. Historia sesji i zapis nagrań
Wszystkie Twoje nagrania są zapisane.

Możesz:

Odsłuchiwać wcześniejsze próby.

Przeglądać historię błędów.

Obserwować postępy w nauce.

Widok:
 Lista nagrań → Wybierz nagranie → Odtwórz/Analizuj.

6. Tryb symulacji dialogu
Masz wirtualnego partnera, który:

Mówi swoje kwestie w realistycznym tempie.

Reaguje na Twoje wypowiedzi.

Możesz ustawić:

Szybsze lub wolniejsze tempo rozmowy.

Widok:
 Symulacja → Rozmowa z partnerem → Realistyczna scena.

EKRANY APLIKACJI — SZYBKIE SZKICE I PRZEJŚCIA

1. Ekran powitalny / startowy
 Logo aplikacji + nazwa LearnMyLines

 Duży przycisk „Dodaj scenariusz”

 Link „Historia nagrań”

Po kliknięciu:

 „Dodaj scenariusz” → przejście do ekranu Import scenariusza

 „Historia nagrań” → przejście do ekranu Historia sesji

2. Import scenariusza
 Przycisk „Wybierz plik” (.txt / .pdf / .docx)

 Podgląd treści

 Rozpoznane role

 Pola edycji ról

 Przycisk „Zapisz i wybierz rolę”

Po kliknięciu:

 „Zapisz i wybierz rolę” → przejście do ekranu Wybór roli

3. Wybór roli
 Lista ról z nazwami

 Podgląd tekstu dla każdej roli

 Przycisk „Wybieram tę rolę”

Po kliknięciu:

 „Wybieram tę rolę” → przejście do Ekranu ćwiczeń

4. Ekran nauki (ćwiczenia)
 Twoje kwestie (tekst do przeczytania)

 Odtwarzacz kwestii partnerów (z emocjami)

 Przycisk „Start próby”

 Pauza / Przewiń / Powtórz

 Przycisk „Zakończ próbę”

Po kliknięciu:

 „Zakończ próbę” → przejście do Ekranu analizy

5. Ekran analizy błędów
 Twoje nagranie vs oryginał

 Lista różnic / pomyłek

 Sugestie poprawy

 Przycisk „Spróbuj ponownie” / „Zapisz próbę”

Po kliknięciu:

 „Spróbuj ponownie” → wraca do Ekranu nauki

„Zapisz próbę” → zapisuje i przechodzi do Historii

6. Historia sesji
 Lista zapisanych prób

 Data, nazwa scenariusza

 Przycisk „Odtwórz”

 Przycisk „Analiza błędów”

Po kliknięciu:

„Odtwórz” → Odtwarza nagranie

„Analiza” → Pokazuje ponownie błędy

Przejścia między ekranami:

 Start ➝ Import scenariusza ➝ Wybór roli ➝ Ćwiczenie ➝ Analiza ➝ Historia

MUST HAVE (funkcje absolutnie niezbędne)
Import scenariusza z pliku .txt

Automatyczne rozpoznanie i edycja ról

Wybór roli przez użytkownika

Tryb nauki – wyświetlanie kwestii użytkownika

Odtwarzanie kwestii partnerów (prosta wersja)

Przycisk „Start próby” i „Zakończ próbę”

Historia sesji – lista zapisanych prób

Możliwość odtworzenia własnych nagrań

Zapis prób

SHOULD HAVE (bardzo przydatne, ale niekonieczne)
Obsługa plików .pdf i .docx

Możliwość pauzowania i przewijania wypowiedzi

Prosta analiza błędów – porównanie tekstu użytkownika z oryginałem

Podgląd całej sceny / scenariusza

Edycja scenariusza przed zapisaniem

Możliwość ustawienia tempa wypowiedzi partnerów

COULD HAVE (miło byłoby mieć)
Zadania emocjonalne – różne wersje tej samej kwestii

Sugestie poprawy na podstawie analizy

Porównanie nagrań w historii prób

Wskaźnik postępu nauki (np. liczba scen opanowanych)

Tryb symulacji dialogu z wirtualnym partnerem

Rozpoznawanie mowy lub sterowanie głosowe

WON'T HAVE (na razie nie będzie)
Rejestracja i logowanie użytkownika

Tryb multiplayer – granie sceny z inną osobą

Tłumaczenie scenariuszy na inne języki

Automatyczne generowanie scenariuszy

1. Ekran startowy (brak scenariuszy)
Przycisk: Dodaj scenariusz

Przejście do: Ekran importu scenariusza

Przycisk: Historia prób

Przejście do: Ekran historii

2. Ekran importu scenariusza
Wybór pliku (.txt / .pdf / .docx)

Automatyczny podział na role

Podgląd scenariusza

Przypisanie roli użytkownika

Przycisk: Zapisz i rozpocznij naukę

Przejście do: Ekran nauki

3. Ekran nauki
Wyświetlenie kwestii użytkownika

Odtwarzanie partnerów (domyślna emocja)

Przycisk: Start próby

Przycisk: Pauza / Wznów

Przycisk: Zakończ i zapisz

Przejście do: Ekran zakończenia sesji

4. Ekran zakończenia sesji
Informacja: Sesja zapisana

Przycisk: Wróć do ekranu głównego

Przejście do: Ekran główny

Przycisk: Odtwórz nagranie

Przejście do: Ekran historii (z odtworzeniem)

5. Ekran historii sesji
Lista nagrań (tytuł, data)

Przycisk: Odtwórz

Odtwarza próbę

Przycisk: Analiza

Pokazuje różnice między scenariuszem a wypowiedzią


Licencja
Projekt jest przeznaczony wyłącznie do użytku prywatnego

Kontakt

W przypadku pytań proszę o kontakt na e-mail karolinaficht@wp.pl
 
