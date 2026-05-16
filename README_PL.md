# 🎬 MovieApp

Nowoczesna, responsywna aplikacja do odkrywania i wyszukiwania filmów stworzona z użyciem React i Vite. Odkrywaj popularne filmy, szukaj swoich ulubionych i poznaj nowe produkcje z pięknym interfejsem opartym na Tailwind CSS.

## ✨ Funkcjonalności

- **🔍 Inteligentne Wyszukiwanie Filmów** - Wyszukuj filmy z debounce'owanymi wynikami w czasie rzeczywistym
- **📈 Filmy Popularne** - Odkryj, co jest popularne w tym tygodniu dzięki śledzeniu popularności
- **🎨 Nowoczesny Interfejs** - Piękny, responsywny design zbudowany za pomocą Tailwind CSS
- **⚡ Szybka Wydajność** - Zoptymalizowana dzięki Vite do błyskawicznego developmentu i buildów
- **💾 Historia Wyszukiwań** - Śledzi i wyświetla najczęściej wyszukiwane filmy
- **📱 W Pełni Responsywna** - Działa bezproblemowo na urządzeniach stacjonarnych, tabletach i telefonach
- **🔄 Aktualizacje w Czasie Rzeczywistym** - Debounce'owane wyszukiwanie dla płynnego doświadczenia użytkownika

## 🛠️ Stos Technologiczny

- **Framework Frontendowy**: React 19.2.6
- **Narzędzie Build**: Vite 8.0.12
- **Style**: Tailwind CSS 4.3.0 z pluginem Vite
- **Backend**: Appwrite (BaaS)
- **Dane Filmowe**: The Movie Database (TMDB) API
- **Jakość Kodu**: ESLint ze wsparciem dla React hooks
- **Narzędzia**: react-use dla custom hooks

## 📋 Wymagania Wstępne

Przed rozpoczęciem upewnij się, że masz zainstalowane:

- Node.js (wersja 16 lub wyższa)
- npm lub pnpm jako menedżer pakietów

## 🚀 Szybki Start

### 1. Klonuj Repozytorium

```bash
git clone https://github.com/twojausername/MovieApp.git
cd MovieApp/vite-project
```

### 2. Zainstaluj Zależności

```bash
npm install
# lub
pnpm install
```

### 3. Konfiguracja Zmiennych Środowiskowych

Skopiuj plik template i dodaj swoje kredencjały API:

```bash
# Skopiuj plik template
cp .env.example .env.local
```

Teraz otwórz `.env.local` i zastąp wartości placeholderów swoimi rzeczywistymi kredencjałami API:

```env
VITE_TMDB_API_KEY=twoj_klucz_api_tmdb
VITE_APPWRITE_ENDPOINT=twoj_endpoint_appwrite
VITE_APPWRITE_PROJECT_ID=twoj_id_projektu
VITE_APPWRITE_DATABASE_ID=twoj_id_bazy_danych
VITE_APPWRITE_COLLECTION_ID=twoj_id_kolekcji
```

> **Ważne**: 
> - Plik `.env.local` jest dodany do `.gitignore` i **nigdy** nie powinien być zatwierdzony w repozytorium
> - Każdy deweloper musi stworzyć swój własny plik `.env.local` z jego kredencjałami
> - Nigdy nie udostępniaj `.env.local` ani nie wklejaj kredencjałów do `.env.example`

### 4. Uruchom Serwer Deweloperski

```bash
npm run dev
# lub
pnpm dev
```

Aplikacja będzie dostępna na `http://localhost:5173`

## 📦 Dostępne Skrypty

```bash
# Uruchom serwer deweloperski z Hot Module Replacement (HMR)
npm run dev

# Zbuilduj na produkcję
npm run build

# Podgląd production build'u lokalnie
npm run preview

# Uruchom ESLint do sprawdzenia jakości kodu
npm run lint
```

## 🎯 Struktura Projektu

```
vite-project/
├── src/
│   ├── components/
│   │   ├── MovieCard.jsx       # Komponent karty pojedynczego filmu
│   │   ├── Search.jsx          # Komponent pola wyszukiwania
│   │   └── Spinner.jsx         # Komponent loadera
│   ├── assets/                 # Zasoby statyczne
│   ├── App.jsx                 # Główny komponent aplikacji
│   ├── appwrite.js             # Funkcje bazy danych Appwrite
│   ├── main.jsx                # Punkt wejścia aplikacji
│   ├── index.css               # Globalne style
│   └── App.css                 # Styl główny aplikacji
├── public/                     # Pliki statyczne (hero.png)
├── index.html                  # Szablon HTML
├── vite.config.js             # Konfiguracja Vite
├── eslint.config.js           # Konfiguracja ESLint
├── package.json               # Zależności projektu
└── .env.local                 # Zmienne środowiskowe (utwórz lokalnie)
```

## 🔌 Integracja API

### TMDB API

Aplikacja pobiera dane filmów z The Movie Database (TMDB) API:

- **Endpoint Popularne**: `/trending/movie/week` - Pobiera popularne filmy
- **Endpoint Wyszukiwania**: `/search/movie` - Wyszukuje filmy według zapytania
- **Endpoint Odkryj**: `/discover/movie` - Pobiera popularne filmy

### Integracja Appwrite

Używa Appwrite jako usługę backendową do:

- Śledzenia statystyk wyszukiwań i częstotliwości
- Przechowywania i pobierania popularnych wyszukiwań
- Utrzymywania danych historii wyszukiwań

> **Uwaga**: Wymaga prawidłowej konfiguracji `.env.local` z ważnymi kredencjałami Appwrite

## 🎨 Style

Projekt używa **Tailwind CSS** do stylowania utility-first z komponentami niestandardowymi:

- **Sekcja Hero**: Efekty gradientu tekstu i obrazy banerów
- **Siatka Filmów**: Responsywne układy kart
- **Pasek Wyszukiwania**: Zaokrąglone pole wejścia ze stanami fokusu
- **Stany Ładowania**: Animacje loadera

## 🐛 Obsługa Błędów

Aplikacja zawiera niezawodną obsługę błędów dla:

- Nieudanych żądań do TMDB API
- Problemów z połączeniem internetowym
- Scenariuszy bez wyników wyszukiwania
- Błędów bazy danych Appwrite

## 🚀 Wdrożenie

### Zbuilduj na Produkcję

```bash
npm run build
```

Generuje zoptymalizowany build produkcyjny w folderze `dist/`.

### Opcje Wdrożenia

- **Vercel** - Rekomendowane dla projektów React/Vite
- **Netlify** - Świetna integracja CI/CD
- **GitHub Pages** - Darmowy hosting statyczny
- **Dowolny Host Statyczny** - Obsługuje konfigurację routingu SPA

**Ważne**: Zawsze ustaw zmienne środowiskowe w ustawieniach platformy wdrożeniowej. Nigdy nie zatwierdzaj `.env.local` ani żadnych plików zawierających klucze API.

## 📚 Dodatkowe Zasoby

- [Dokumentacja React](https://react.dev)
- [Dokumentacja Vite](https://vitejs.dev)
- [Dokumentacja Tailwind CSS](https://tailwindcss.com)
- [Dokumentacja TMDB API](https://www.themoviedb.org/settings/api)
- [Dokumentacja Appwrite](https://appwrite.io/docs)

## 🤝 Wkład w Projekt

Wkład w projekt jest mile widziany! Oto jak możesz pomóc:

1. Utwórz fork repozytorium
2. Utwórz branch funkcji (`git checkout -b feature/niesamowita-funkcja`)
3. Zatwierdź zmiany (`git commit -m 'Dodaj niesamowitą funkcję'`)
4. Wyślij do branch'a (`git push origin feature/niesamowita-funkcja`)
5. Otwórz Pull Request

## 📄 Licencja

Ten projekt jest licencjonowany na warunkach MIT License - zobacz plik LICENSE po szczegóły.

## 👨‍💻 Autor

Stworzono z ❤️ przez [Twoje Imię]

## 📞 Pomoc i Wsparcie

Jeśli masz pytania lub potrzebujesz pomocy, otwórz issue na GitHub lub skontaktuj się z zespołem deweloperskim.

---

**Miłego poszukiwania filmów! 🍿🎬**
