# Projekt Aplikacji Web

## 1. Informacje Ogólne

- **Stack:**
  - React (Vite / Tailwind CSS)
  - Node.js + Express
  - MySQL
  - WebSockets (`ws` lub `Socket.io`)
  - Docker & Docker Compose
  - GitHub (zgodne z Git Flow / Pull Requests)

- **Temat:**
  - **Dowolny temat**
  - Jeśli brakuje pomysłu, możemy pomóc w doborze odpowiedniego tematu.

- **Inne:**
  - **Bez AI:** Jako że projekt ma na celu sprawdzenie wiedzy oraz jest trywialny, raczej nie będzie mile widziane użycie AI.
  - **Czas:** Nie ma ograniczenia czasowego, ale bez zrobienia projektu nie można brać udziału w innych wydarzeniach i projektach koła.
  - **Inny stack:** Dopuszcza się użycie innego stacku, ale wtedy takie użycie musi być naprawdę dobrze uzasadnione (dlaczego, jakie są zalety, jakie wady) i odpowiednio zaprezentowane

## 2. Wymagania Funkcjonalne

### A. Moduł CRUD

System musi zawierać przynajmniej po jednym w pełni funkcjonującym endpoincie:

1. **Create:** Dodawanie nowego rekordu do bazy danych.
2. **Read:** Wyświetlanie listy wszystkich rekordów oraz szczegółów pojedynczego elementu.
3. **Update** Edycja istniejących danych.
4. **Delete** Usuwanie rekordu z bazy danych z potwierdzeniem.

### B. Moduł WebSocket

1. **Eventy:** Połączenie WebSocket musi informować urzytkownika w czasie rzeczywistym o modyfikacjach danych.
2. **Komponent strumieniowy:** Widok w aplikacji pokazujący aktualne zdarzenia lub wiadomości przesyłane natychmiastowo do wszystkich podłączonych użytkowników bez konieczności odświeżania strony.

## 3. Wymagania Niefunkcjonalne i Architektura

- **Konteneryzacja (Docker):**
  - Projekt musi uruchamiać się za pomocą **jednej komendy**: `docker-compose up --build`.
  - Oddzielne kontenery dla: Bazy danych (MySQL), Backendu (Express) oraz Frontend (React).

- **Struktura Repozytorium (GitHub):**
  - Czysty podział na katalogi `/frontend`, `/backend` oraz plik `docker-compose.yml` w głównym katalogu.
  - Obecność pliku `README.md` z instrukcją szybkiego startu.

## 4. Przygotowanie do Code Review, Obrony i Prezentacji

### A. Code Review (Na co zwrócić uwagę)

- **Bezpieczeństwo:** Walidacja danych wejściowych, unikanie SQL Injection.
- **Czysty kod:** Podział logiki na kontrolery i routing w Expressie, komponentowe podejście w Reacie.
- **Stan aplikacji:** Poprawna obsługa asynchroniczności oraz stanów ładowania i błędów w UI.
- **Dobre praktyki:** Kod powinien być napisany w duchu dobrych praktyk.

### B. Scenariusz Prezentacji i Obrony (5 minut)

1. **Prezentacja:** Jeśli ktoś chce, może przygotować prezentacje do przedstawienia swojego projektu i przedstawienia zarządowi. Jeśli użyto innego stacku, prezentacja jest wymagana.
2. **Obrona:** Omówienie kluczowych fragmentów kodu i konfiguracji Dockera, z pytaniami od zarządu.

## 5. TODO list

- [ ] **Faza 0: Przygotowanie środowiska**
  - [ ] Wybór tematu projektu.
  - [ ] Utworzenie repozytorium na GitHubie i wstępna struktura katalogów (`/frontend`, `/backend`).
  - [ ] Konfiguracja `docker-compose.yml`.

- [ ] **Faza 1: Backend & Baza Danych**
  - [ ] Połączenie aplikacji Express z bazą MySQL i utworzenie odpowiedniej tabeli.
  - [ ] Implementacja pełnego zestawu endpointów CRUD.

- [ ] **Faza 2: Komunikacja w czasie rzeczywistym (WebSocket)**
  - [ ] Konfiguracja serwera WebSocket.
  - [ ] Wysyłanie eventów do klientów przy zmianach w bazie danych.

- [ ] **Faza 3: Frontend**
  - [ ] Stworzenie interfejsu użytkownika.
  - [ ] Podpięcie klienta WebSocket do odbierania i dynamicznego wyświetlania zdarzeń.

- [ ] **Faza 4: Finał i Weryfikacja**
  - [ ] Przetestowanie uruchomienia całości przez `docker-compose up --build`.
  - [ ] Przygotowanie pliku `README.md` z instrukcją uruchomienia.
  - [ ] Ostateczny przegląd kodu (Code Review) przed obroną.
