# LearnMyLines

LearnMyLines to aplikacja wspierająca aktorów w nauce scenariusza na pamięć. Pomaga w efektywnym opanowaniu własnych kwestii oraz w oswojeniu się z dialogami partnerów poprzez interaktywne ćwiczenia.

## Główne funkcjonalności

- Importowanie scenariusza z pliku lub ręczne wpisanie tekstu Podział dialogu na kwestie aktora i partnerów 
- Tryb nauki polegający na ukrywaniu części tekstu i odsłuchiwaniu nagrań 
- Interaktywna symulacja dialogów z wirtualnym partnerem Historia sesji zapisująca postępy w nauce

## Technologie

- Projekt wykorzystuje następujące technologie Python framework Django 
- SQLite lub PostgreSQL jako baza danych 
- HTML i CSS jako podstawowy frontend

## Instalacja

- Aby uruchomić projekt lokalnie należy sklonować repozytorium i przejść do jego katalogu git clone https://github.com/twoje-repo/learnmylines.git cd LearnMyLines

- Następnie należy zainstalować wymagane zależności pip install -r requirements.txt

- Uruchomienie aplikacji python manage.py runserver

- Projekt można uruchomić w przeglądarce pod adresem http://127.0.0.1:8000/

## Plan implementacji

- Utworzenie podstawowych modeli w Django Obsługa scenariuszy z możliwością importowania i edycji 
- System nauki wykorzystujący tryb ukrywania i powtarzania tekstu 
- Interaktywna symulacja dialogów Optymalizacja wyglądu i funkcjonalności aplikacji

## Funkcjonalności aplikacji
 
- Importowanie scenariusza:
- Użytkownik zaczyna od dodania swojego pliku (.txt, .pdf, .docx).

- Aplikacja automatycznie rozpoznaje role i dzieli tekst na wypowiedzi poszczególnych postaci

- Użytkownik może edytować role i tekst, jeśli coś zostało źle rozpoznane

### Widok:
 "Dodaj scenariusz" → Wybierz plik → Załaduj → Przypisz role → Zapisz.

### Tryb nauki scenariusza
- Twoje kwestie są wyświetlane

- Kwestie partnerów są odtwarzane (np. w różnych emocjach: radość, złość, smutek)

### Możesz:

- Pauzować

- Przewijać

- Odtwarzać fragmenty wielokrotnie

- Wskaźnik postępu: np. "3/10 scen przećwiczonych"

### Widok:
 Start próby → Odtwarzanie partnerów → Mówisz swoją kwestię → Wskaźnik postępu.

### Analiza błędów
- Po zakończeniu próby aplikacja:

- Porównuje Twój tekst z oryginalnym scenariuszem

### Pokazuje:

- Pominięte słowa

- Zmiany w tekście

- Sugestie poprawy: np. "Uwaga na pomyłkę w 2. scenie"

### Widok:
- Podsumowanie po próbie → Lista błędów → Wskazówki

### Zadania emocjonalne
- Aplikacja proponuje: "Powiedz tę kwestię jakbyś był bardzo zdenerwowany",
"Spróbuj radośnie"

- Możesz ćwiczyć tę samą scenę w różnych wariantach emocji

- Zapis różnych emocjonalnych wersji do porównania

### Widok:
 - Wybór emocji → Ćwiczenie → Zapis prób.

### Historia sesji i zapis nagrań
- Wszystkie Twoje nagrania są zapisane

- Możesz:

- Odsłuchiwać wcześniejsze próby

- Przeglądać historię błędów

- Obserwować postępy w nauce

### Widok:
-  Lista nagrań → Wybierz nagranie → Odtwórz/Analizuj

###b Tryb symulacji dialogu
- Masz wirtualnego partnera, który:

- Mówi swoje kwestie w realistycznym tempie

- Reaguje na Twoje wypowiedzi

- Możesz ustawić:

- Szybsze lub wolniejsze tempo rozmowy

### Widok:
- Symulacja → Rozmowa z partnerem → Realistyczna scena

## EKRANY APLIKACJI — SZYBKIE SZKICE I PRZEJŚCIA

### Ekran powitalny / startowy
- Logo aplikacji + nazwa LearnMyLines

- Duży przycisk „Dodaj scenariusz”

- Link „Historia nagrań”

- Po kliknięciu:

 - „Dodaj scenariusz” → przejście do ekranu Import scenariusza

 - „Historia nagrań” → przejście do ekranu Historia sesji

### Import scenariusza
- Przycisk „Wybierz plik” (.txt / .pdf / .docx)

- Podgląd treści

- Rozpoznane role

- Pola edycji ról

- Przycisk „Zapisz i wybierz rolę”

- Po kliknięciu:

 - „Zapisz i wybierz rolę” → przejście do ekranu Wybór roli

### Wybór roli
- Lista ról z nazwami

- Podgląd tekstu dla każdej roli

- Przycisk „Wybieram tę rolę”

- Po kliknięciu:

 - „Wybieram tę rolę” → przejście do Ekranu ćwiczeń

### Ekran nauki (ćwiczenia)
- Twoje kwestie (tekst do przeczytania)

- Odtwarzacz kwestii partnerów (z emocjami)

- Przycisk „Start próby”

 - Pauza / Przewiń / Powtórz

- Przycisk „Zakończ próbę”

- Po kliknięciu:

 - „Zakończ próbę” → przejście do Ekranu analizy

### Ekran analizy błędów
- Twoje nagranie vs oryginał

- Lista różnic / pomyłek

- Sugestie poprawy

- Przycisk „Spróbuj ponownie” / „Zapisz próbę”

- Po kliknięciu:

 - „Spróbuj ponownie” → wraca do Ekranu nauki

 - „Zapisz próbę” → zapisuje i przechodzi do Historii

### Historia sesji
- Lista zapisanych prób

- Data, nazwa scenariusza

- Przycisk „Odtwórz”

-  Przycisk „Analiza błędów”

- Po kliknięciu:

 - „Odtwórz” → Odtwarza nagranie

 - „Analiza” → Pokazuje ponownie błędy

### Przejścia między ekranami:

 - Start ➝ Import scenariusza ➝ Wybór roli ➝ Ćwiczenie ➝ Analiza ➝ Historia

MUST HAVE (funkcje absolutnie niezbędne)
- Import scenariusza z pliku .txt

- Automatyczne rozpoznanie i edycja ról

- Wybór roli przez użytkownika

- Tryb nauki – wyświetlanie kwestii użytkownika

- Odtwarzanie kwestii partnerów (prosta wersja)

- Przycisk „Start próby” i „Zakończ próbę”

- Historia sesji – lista zapisanych prób

- Możliwość odtworzenia własnych nagrań

- Zapis prób

SHOULD HAVE (bardzo przydatne, ale niekonieczne)
- Obsługa plików .pdf i .docx

- Możliwość pauzowania i przewijania wypowiedzi

- Prosta analiza błędów – porównanie tekstu użytkownika z oryginałem

- Podgląd całej sceny / scenariusza

- Edycja scenariusza przed zapisaniem

- Możliwość ustawienia tempa wypowiedzi partnerów

COULD HAVE (miło byłoby mieć)
- Zadania emocjonalne – różne wersje tej samej kwestii

- Sugestie poprawy na podstawie analizy

- Porównanie nagrań w historii prób

- Wskaźnik postępu nauki (np. liczba scen opanowanych)

- Tryb symulacji dialogu z wirtualnym partnerem

- Rozpoznawanie mowy lub sterowanie głosowe

WON'T HAVE (na razie nie będzie)
- Rejestracja i logowanie użytkownika

- Tryb multiplayer – granie sceny z inną osobą

- Tłumaczenie scenariuszy na inne języki

- Automatyczne generowanie scenariuszy

### Ekran startowy (brak scenariuszy)
- Przycisk: Dodaj scenariusz

- Przejście do: Ekran importu scenariusza

- Przycisk: Historia prób

- Przejście do: Ekran historii

### Ekran importu scenariusza
- Wybór pliku (.txt / .pdf / .docx)

- Automatyczny podział na role

- Podgląd scenariusza

- Przypisanie roli użytkownika

- Przycisk: Zapisz i rozpocznij naukę

- Przejście do: Ekran nauki

### Ekran nauki
- Wyświetlenie kwestii użytkownika

- Odtwarzanie partnerów (domyślna emocja)

- Przycisk: Start próby

- Przycisk: Pauza / Wznów

- Przycisk: Zakończ i zapisz

- Przejście do: Ekran zakończenia sesji

### Ekran zakończenia sesji
- Informacja: Sesja zapisana

- Przycisk: Wróć do ekranu głównego

- Przejście do: Ekran główny

- Przycisk: Odtwórz nagranie

- Przejście do: Ekran historii (z odtworzeniem)

### Ekran historii sesji
- Lista nagrań (tytuł, data)

- Przycisk: Odtwórz

- Odtwarza próbę

- Przycisk: Analiza

- Pokazuje różnice między scenariuszem a wypowiedzią


## Plan implementacji aplikacji LearnMyLines – szczegóły techniczne
### Modele / klasy w projekcie
- Model Scenario (Scenariusz)
  - Pola:

     - id (UUID lub AutoField)

     - title (CharField) – nazwa scenariusza

     - uploaded_file (FileField) – oryginalny plik scenariusza (.txt, .pdf, .docx)

     - import_date (DateTimeField) – data dodania

     - raw_text (TextField) – pełny tekst scenariusza po imporcie

  - Metody:

     - parse_roles() – metoda do automatycznego rozpoznawania ról i podziału na kwestie

- Model Role (Rola postaci)
  - Pola:

     - id

     - scenario (ForeignKey do Scenario)

     - name (CharField) – nazwa roli (np. „Hamlet”, „Ofelia”)

     - is_user_role (BooleanField) – czy to rola wybrana przez użytkownika

- Model Line (Kwestia)
  - Pola:

     - id

     - role (ForeignKey do Role)

     - text (TextField) – tekst kwestii

     - order (IntegerField) – kolejność w scenariuszu

- Model Session (Sesja nauki)
  - Pola:

     - id

     - scenario (ForeignKey do Scenario)

     - user_role (ForeignKey do Role)

     - start_time (DateTimeField)

     - end_time (DateTimeField)

     - progress (IntegerField) – liczba przećwiczonych kwestii/scen

- Model Attempt (Próba wypowiedzi)
  - Pola:

     - id

     - session (ForeignKey do Session)

     - line (ForeignKey do Line) – kwestia ćwiczona w próbie

     - recording (FileField) – nagranie audio wypowiedzi użytkownika

     - error_analysis (JSONField) – wynik analizy błędów (np. pominięcia, zmiany)

     - emotion (CharField) – emocja, z którą ćwiczono kwestię (np. „radość”, „złość”)

     - timestamp (DateTimeField)

### Baza danych – schemat i relacje
- Scenario 1 - * Role

- Role 1 - * Line

- Scenario 1 - * Session

- Session 1 - * Attempt

 - Role (w Session) wskazuje rolę użytkownika

 - Attempt powiązane z konkretną kwestią i sesją

### Zewnętrzne biblioteki / API
- Przetwarzanie plików:

  - python-docx – do odczytu plików .docx

  - PyPDF2 lub pdfplumber – do odczytu plików .pdf

- Analiza tekstu i podział na role:

  - własne algorytmy oparte na regexach i heurystykach (np. rozpoznawanie wzorców „ROLA: tekst”)

- Nagrywanie i odtwarzanie audio:

  - HTML5 Web Audio API (frontend)

  - pydub lub ffmpeg (backend) do konwersji i obróbki nagrań

- Analiza błędów:

  - difflib (Python stdlib) do porównywania tekstów

- Frontend:

  - JavaScript (np. React lub czysty JS) do interaktywnego odtwarzania i sterowania nagraniami

- Opcjonalnie:

  - Text-to-Speech API (np. Google TTS) do generowania kwestii partnerów w różnych emocjach (future feature)

### Interakcje użytkownika
- Dodawanie scenariusza:

   - Użytkownik wybiera plik (.txt, .pdf, .docx)

   - System importuje tekst, automatycznie rozpoznaje role i kwestie

   - Użytkownik sprawdza i edytuje rozpoznane role i teksty

   - Zapisuje scenariusz i wybiera swoją rolę

- Tryb nauki:

   - Użytkownik widzi swoje kwestie wyświetlone na ekranie

   - Słyszy kwestie partnerów (odtwarzane audio z różnymi emocjami)

   - Steruje odtwarzaniem (pauza, przewijanie, powtórki)

   - Rozpoczyna i kończy próbę wypowiedzi

   - Po próbie widzi analizę błędów i sugestie

- Zadania emocjonalne:

   - Wybór emocji do ćwiczenia kwestii

   - Nagrywanie i zapisywanie różnych wersji emocjonalnych

- Historia sesji:

   - Przeglądanie listy nagrań i sesji

   - Odtwarzanie nagrań i analiza błędów

- Symulacja dialogu:

   - Rozmowa z wirtualnym partnerem, który odtwarza kwestie w realistycznym tempie

   - Możliwość zmiany tempa rozmowy

### Rozrysowanie mockupów (opis słowny)
- Ekran startowy
   - Logo + nazwa aplikacji

   - Duży przycisk „Dodaj scenariusz”

   - Link „Historia nagrań”

- Import scenariusza
   - Przycisk „Wybierz plik”

   - Podgląd tekstu ze scenariuszem

   - Lista rozpoznanych ról z możliwością edycji

   - Przycisk „Zapisz i wybierz rolę”

- Wybór roli
  - Lista ról z nazwami

   - Podgląd kwestii dla każdej roli

   - Przycisk „Wybieram tę rolę”

- Ekran nauki
   - Tekst własnych kwestii (wyświetlany)

   - Odtwarzacz kwestii partnerów (z kontrolkami: start, pauza, przewiń)

   - Przycisk „Start próby” i „Zakończ próbę”

   - Wskaźnik postępu

- Ekran analizy błędów
   - Porównanie tekstu oryginalnego i wypowiedzi użytkownika

   - Lista błędów i sugestii

   - Przycisk „Spróbuj ponownie” i „Zapisz próbę”

- Historia sesji
   - Lista nagrań z datami i nazwami scenariuszy

   - Przycisk „Odtwórz” i „Analiza”

- Tryb symulacji dialogu
   - Okno rozmowy z wirtualnym partnerem

   - Kontrolki zmiany tempa

   - Przycisk zakończenia symulacji

 
