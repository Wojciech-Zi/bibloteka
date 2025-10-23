# ZADANIE TRENINGOWE NR 1
**Tworzenie i administrowanie stronami i aplikacjami internetowymi oraz bazami danych**

**Symbol kwalifikacji:** INF.03  
**Czas trwania:** 90 minut  
**Wersja:** Treningowa 01

---

## INSTRUKCJA DLA ZDAJĄCEGO

1. Przed rozpoczęciem pracy utwórz w swoim repozytorium folder o nazwie: **zadanie_treningowe_01**
2. Wszystkie pliki tego zadania zapisuj TYLKO w tym folderze
3. Sprawdź, czy masz dostęp do edytora zaznaczającego składnię
4. Zapoznaj się z treścią zadania. Masz na to 5 minut
5. Wykonaj samodzielnie zadanie egzaminacyjne
6. Po zakończeniu sprawdź poprawność działania witryny w przeglądarce
7. Zapisz nazwę przeglądarki w pliku `przeglądarka.txt`

**Powodzenia!**

---

## ZADANIE EGZAMINACYJNE

Wykonaj stronę internetową dla **Biblioteki Miejskiej**, wykorzystując edytor zaznaczający składnię.

### Pliki graficzne

W archiwum otrzymujesz następujące pliki:
- `logo.png` - logo biblioteki
- `tlo.jpg` - zdjęcie wnętrza biblioteki  
- `ikona.png` - ikona książki (wymaga przeskalowania)

---

## CZĘŚĆ I - Przygotowanie grafiki

Za pomocą edytora grafiki rastrowej wykonaj operacje:

- Plik `ikona.png` należy przeskalować do **dokładnych rozmiarów 24 px na 24 px**
- Zapisz przeskalowany plik pod tą samą nazwą

---

## CZĘŚĆ II - Struktura witryny internetowej

### Ilustracja 1. Wygląd strony w przeglądarce

![Wygląd strony](ilustracja_biblioteka.png)

```
╔═══════════════════════════════════════════════════════════╗
║    BIBLIOTEKA MIEJSKA - KATALOG ONLINE                    ║
║              [logo.png]                                    ║
╠═══════════╦═══════════════════════════════════════════════╣
║   MENU    ║                                               ║
║           ║        NOWOŚCI W BIBLIOTECE                   ║
║ ○ Katalog ║                                               ║
║ ○ Nowości ║   W tym miesiącu polecamy nowe pozycje...    ║
║ ○ Promocje║                                               ║
║ ○ Kontakt ║   [Link: Zobacz pełną listę →]               ║
║           ║                                               ║
║           ╠═══════════════════════════════════════════════╣
║           ║  ┌──────────────┐  ┌──────────────┐          ║
║           ║  │   DZIECI     │  │  MŁODZIEŻ    │          ║
║           ║  │              │  │              │          ║
║           ║  │ • Bajki      │  │ • Fantasy    │          ║
║           ║  │ • Komiksy    │  │ • Sci-Fi     │          ║
║           ║  │ • Edukacja   │  │ • Romans     │          ║
║           ║  └──────────────┘  └──────────────┘          ║
║           ║  ┌──────────────┐  ┌──────────────┐          ║
║           ║  │  DOROŚLI     │  │   NAUKA      │          ║
║           ║  │              │  │              │          ║
║           ║  │ • Biografie  │  │ • Historia   │          ║
║           ║  │ • Kryminał   │  │ • Przyroda   │          ║
║           ║  │ • Reportaż   │  │ • Medycyna   │          ║
║           ║  └──────────────┘  └──────────────┘          ║
╠═══════════╩═══════════════════════════════════════════════╣
║  [ikona.png] Biblioteka Miejska | ul. Główna 15          ║
║              Telefon: 123-456-789                         ║
╚═══════════════════════════════════════════════════════════╝
```

---

### Ilustracja 2. Układ semantycznych bloków HTML5

```
┌─────────────────────────────────────┐
│       Blok nagłówkowy              │
│         <header>                    │
├─────────────┬───────────────────────┤
│    Blok     │                       │
│    lewy     │    Blok główny       │
│   <aside>   │      <main>          │
│             │                       │
│             ├───────────────────────┤
│             │  Sekcja artykułu     │
│             │    <article>         │
│             ├───────────────────────┤
│             │ ┌─────┐  ┌─────┐    │
│             │ │Sek 1│  │Sek 2│    │
│             │ └─────┘  └─────┘    │
│             │ ┌─────┐  ┌─────┐    │
│             │ │Sek 3│  │Sek 4│    │
│             │ └─────┘  └─────┘    │
│             │    <section> x4      │
└─────────────┴───────────────────────┘
┌─────────────────────────────────────┐
│        Blok stopki                  │
│         <footer>                    │
└─────────────────────────────────────┘
```

---

## Cechy witryny

### Plik główny: `biblioteka.html`

**Struktura dokumentu:**
- Zapisana w języku HTML5
- Zadeklarowany polski język zawartości witryny
- Jawnie zastosowany właściwy standard kodowania polskich znaków
- Tytuł strony widoczny na karcie przeglądarki: **"Biblioteka Miejska - Katalog"**
- Plik `ikona.png` jako favicon widoczny na karcie przeglądarki
- Arkusz stylów w pliku `style.css` prawidłowo połączony z kodem strony

**Podział strony na bloki:**
- Podział strony na bloki zrealizowany za pomocą semantycznych znaczników bloków języka HTML5
- Układ bloków zgodny z **Ilustracją 2**

---

### Zawartość bloków

#### Blok nagłówkowy (`<header>`):
- Nagłówek pierwszego stopnia o treści: **"BIBLIOTEKA MIEJSKA - KATALOG ONLINE"**
- Obraz `logo.png` z tekstem alternatywnym **"logo biblioteki"**

#### Blok lewy - sidebar (`<aside>`):
- Nagłówek drugiego stopnia o treści: **"MENU"**
- Lista nieuporządkowana zawierająca 4 elementy:
  - Katalog
  - Nowości
  - Promocje
  - Kontakt

#### Sekcja artykułu (`<article>`) wewnątrz bloku głównego:
- Nagłówek drugiego stopnia o treści: **"NOWOŚCI W BIBLIOTECE"**
- Paragraf z tekstem: *"W tym miesiącu polecamy nowe pozycje z działu literatury faktu oraz beletrystyki. Zapraszamy do zapoznania się z naszą ofertą i rezerwacji interesujących tytułów online."*
- Odnośnik o treści **"Zobacz pełną listę →"** prowadzący do podstrony `lista.html`

#### Cztery sekcje kategorii (`<section>`) wewnątrz bloku głównego:

**Sekcja 1:**
- Nagłówek trzeciego stopnia: **"DZIECI"**
- Lista nieuporządkowana:
  - Bajki
  - Komiksy
  - Edukacja

**Sekcja 2:**
- Nagłówek trzeciego stopnia: **"MŁODZIEŻ"**
- Lista nieuporządkowana:
  - Fantasy
  - Sci-Fi
  - Romans

**Sekcja 3:**
- Nagłówek trzeciego stopnia: **"DOROŚLI"**
- Lista nieuporządkowana:
  - Biografie
  - Kryminał
  - Reportaż

**Sekcja 4:**
- Nagłówek trzeciego stopnia: **"NAUKA"**
- Lista nieuporządkowana:
  - Historia
  - Przyroda
  - Medycyna

#### Blok stopki (`<footer>`):
- Obraz `ikona.png` z tekstem alternatywnym **"książka"**
- Tekst: **"Biblioteka Miejska | ul. Główna 15"**
- W nowym wierszu tekst: **"Telefon: 123-456-789"**

---

### Plik dodatkowy: `lista.html`

Należy utworzyć plik `lista.html` zawierający:
- Podstawową strukturę HTML5
- W treści strony tekst: **"Pełna lista nowości - strona w przygotowaniu"**

---

## CZĘŚĆ III - Styl CSS witryny internetowej

### Plik: `style.css`

Styl CSS zdefiniowany jest w całości w zewnętrznym pliku o nazwie `style.css`

---

### Cechy formatowania CSS:

#### 1. Domyślne formatowanie wszystkich selektorów:
- Krój czcionki: **Verdana**
- Marginesy: **0**
- Wypełnienie (padding): **0**

#### 2. Element `body`:
- Zastosuj **CSS Grid** do utworzenia układu dwukolumnowego
- Kolumna lewa (sidebar): **20%** szerokości
- Kolumna prawa (main): **80%** szerokości

#### 3. Dla bloku nagłówkowego:
- Kolor tła: **#2C3E50**
- Kolor czcionki: **white**
- Wyrównanie tekstu: **do środka**
- Marginesy wewnętrzne: **20px**

#### 4. Dla obrazu logo w nagłówku:
- Maksymalna szerokość: **120px**
- Margines górny: **10px**

#### 5. Dla bloku lewego (sidebar):
- Kolor tła: **#34495E**
- Kolor czcionki: **white**
- Marginesy wewnętrzne: **15px**
- Minimalna wysokość: **600px**

#### 6. Dla listy w menu (sidebar):
- Styl listy: **none** (bez punktorów)
- Marginesy wewnętrzne elementów listy: **10px**
- Rozmiar czcionki: **110%**

#### 7. Dla elementów listy w menu przy najechaniu kursorem (`:hover`):
- Kolor tła: **#1ABC9C**
- Kursor: **pointer**

#### 8. Dla sekcji artykułu:
- Tło: obraz **tlo.jpg**
- Kolor czcionki: **#2C3E50**
- Minimalna wysokość: **250px**
- Marginesy wewnętrzne: **30px**
- Rozmiar czcionki: **120%**

#### 9. Dla odnośnika w artykule (`<a>`):
- Kolor: **#E74C3C**
- Pogrubienie: **bold**
- Dekoracja tekstu: **none** (brak podkreślenia)

#### 10. Dla odnośnika w artykule przy najechaniu (`:hover`):
- Dekoracja tekstu: **underline**
- Kolor: **#C0392B**

#### 11. Dla kontenera zawierającego 4 sekcje kategorii:
- Zastosuj **CSS Grid**: 2 kolumny, 2 wiersze
- Odstęp między elementami (gap): **20px**
- Marginesy wewnętrzne: **20px**

#### 12. Dla 4 sekcji kategorii:
- Kolor tła: **#ECF0F1**
- Obramowanie: **2px solid #BDC3C7**
- Zaokrąglenie rogów: **8px**
- Marginesy wewnętrzne: **15px**
- Minimalna wysokość: **180px**

#### 13. Dla sekcji kategorii przy najechaniu kursorem (`:hover`):
- Kolor tła: **#1ABC9C**
- Cień bloku: **5px 5px 10px #7F8C8D**
- Transform: **scale(1.05)**
- Transition: **0.3s**

#### 14. Dla nagłówków drugiego stopnia (`<h2>`):
- Kolor: **#2C3E50**
- Marginesy: **10px 0**

#### 15. Dla nagłówków trzeciego stopnia (`<h3>`):
- Kolor: **#2C3E50**
- Marginesy: **10px 0**

#### 16. Dla nagłówków trzeciego stopnia w sekcjach kategorii:
- Wyrównanie tekstu: **do środka**
- Kolor: **#E74C3C**
- Odstępy między literami: **2px**

#### 17. Dla list w sekcjach kategorii:
- Styl listy: **square**
- Marginesy lewe: **20px**

#### 18. Dla stopki:
- Kolor tła: **#2C3E50**
- Kolor czcionki: **white**
- Wyrównanie tekstu: **do środka**
- Marginesy wewnętrzne: **15px**
- Rozmiar czcionki: **90%**

#### 19. Dla obrazu w stopce:
- Wyrównanie pionowe: **middle**
- Margines prawy: **10px**

---

## Tabela 1. Semantic Elements in HTML5

| Tag | Description |
|-----|-------------|
| `<header>` | Specifies a header for a document or section |
| `<main>` | Specifies the main content of a document |
| `<aside>` | Defines content aside from the page content |
| `<article>` | Defines independent, self-contained content |
| `<section>` | Defines a section in a document |
| `<footer>` | Defines a footer for a document or section |
| `<nav>` | Defines navigation links |

---

## Tabela 2. CSS Grid Properties

| Property | Value | Description |
|----------|-------|-------------|
| `display` | `grid` | Defines a grid container |
| `grid-template-columns` | `20% 80%` | Defines columns width |
| `grid-template-columns` | `1fr 1fr` | Two equal columns |
| `grid-template-rows` | `auto auto` | Defines rows height |
| `gap` | `20px` | Space between grid items |

---

## Tabela 3. CSS Transform and Transition

| Property | Value | Description |
|----------|-------|-------------|
| `transform` | `scale(1.05)` | Scales element to 105% |
| `transition` | `0.3s` | Smooth transition in 0.3 seconds |
| `box-shadow` | `5px 5px 10px color` | Adds shadow to element |

---

## UWAGA

Po zakończeniu pracy:

1. Utwórz plik tekstowy o nazwie **`przeglądarka.txt`**
2. Zapisz w nim nazwę przeglądarki internetowej, w której weryfikowana była poprawność działania witryny
3. Umieść go w folderze `zadanie_treningowe_01`

---

## Lista plików do utworzenia:

W folderze `zadanie_treningowe_01` powinny znajdować się:

- [ ] `biblioteka.html` - główna strona witryny
- [ ] `lista.html` - podstrona
- [ ] `style.css` - arkusz stylów
- [ ] `logo.png` - plik graficzny (z archiwum)
- [ ] `tlo.jpg` - plik graficzny (z archiwum)
- [ ] `ikona.png` - plik graficzny przeskalowany do 24x24px
- [ ] `przeglądarka.txt` - nazwa użytej przeglądarki

---

## Czas przeznaczony na wykonanie zadania: 90 minut

## Ocenie będzie podlegać 3 rezultaty:
1. Przygotowanie grafiki
2. Zawartość witryny internetowej (struktura HTML)
3. Styl CSS witryny internetowej (formatowanie)

---

**KONIEC ZADANIA**