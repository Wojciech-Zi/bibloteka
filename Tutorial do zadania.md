# 📘 Tutorial UPROSZCZONY: Biblioteka Miejska - HTML i CSS

## 🎯 Ten tutorial jest dla Ciebie!
Nie martw się jeśli programowanie jest trudne. Zrobimy to **małymi krokami**. Każdy krok jest **prosty**.

---

## 📂 KROK 1: Stwórz folder

### Co zrobić:

1. Otwórz folder gdzie trzymasz zadania
2. **Prawy przycisk myszy** → `Nowy` → `Folder`
3. Nazwij folder: `zadanie_treningowe_01`
4. **Otwórz ten folder**

✅ **Sprawdź:** Widzisz pusty folder o nazwie `zadanie_treningowe_01`?

---

## 🖼️ KROK 2: Wrzuć obrazki

### Co zrobić:

1. Znajdź 3 obrazki z archiwum:
   - `logo.png`
   - `tlo.jpg`
   - `ikona.png`

2. **SKOPIUJ** wszystkie 3 do folderu `zadanie_treningowe_01`

3. Otwórz program do zmiany rozmiaru obrazka (np. Paint)

4. Otwórz `ikona.png`

5. Zmień rozmiar na: **24 na 24** (bardzo mały!)

6. Zapisz

✅ **Sprawdź:** W folderze widzisz 3 obrazki?

---

## 📝 KROK 3: Stwórz 3 puste pliki

### Co zrobić:

W folderze `zadanie_treningowe_01` stwórz **3 nowe pliki**:

1. **Prawy przycisk** → `Nowy` → `Dokument tekstowy`
2. Zmień nazwę na: `biblioteka.html`
3. Powtórz i stwórz: `lista.html`
4. Powtórz i stwórz: `style.css`

✅ **Sprawdź:** Widzisz 3 pliki + 3 obrazki = razem 6 rzeczy w folderze?

---

## 🏗️ KROK 4: Podstawa HTML

### Otwórz plik `biblioteka.html` w Notatniku

### Przepisz dokładnie:

```html
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <title>Biblioteka Miejska - Katalog</title>
    <link rel="icon" href="ikona.png" type="image/png">
    <link rel="stylesheet" href="style.css">
</head>
<body>

</body>
</html>
```

### 🤔 Co to znaczy?

Wyobraź sobie że budujesz dom:

- `<!DOCTYPE html>` = "To jest nowoczesny dom" (HTML5)
- `<html lang="pl">` = "W tym domu mówimy po polsku"
- `<head>` = Dach domu (niewidoczne rzeczy, ale ważne)
- `<meta charset="UTF-8">` = "Używamy polskich liter: ą, ę, ć"
- `<title>` = Nazwa na karcie przeglądarki
- `<link rel="icon">` = Mała ikonka na karcie
- `<link rel="stylesheet">` = "Będę używał kolorów z pliku style.css"
- `<body>` = Wnętrze domu (to co ludzie widzą)

### 💾 ZAPISZ (Ctrl + S)

✅ **Sprawdź:** Kliknij 2 razy na `biblioteka.html` - otwiera się w przeglądarce?

---

## 🎨 KROK 5: Pomalujmy stronę na ZIELONO

Zanim zaczniemy budować, **najpierw** nauczymy się malować!

### Otwórz plik `style.css`

### Przepisz:

```css
/* To jest komentarz - nie robi nic, tylko wyjaśnia */

/* Malujemy całą stronę */
body {
    background-color: lightgreen;
}
```

### 💾 ZAPISZ (Ctrl + S)

### Otwórz `biblioteka.html` w przeglądarce

✅ **Sprawdź:** Strona jest jasnozielona? 

- **TAK** = Świetnie! CSS działa! 
- **NIE** = Sprawdź czy plik `style.css` jest w tym samym folderze

---

## 🧱 KROK 6: Budujemy NAGŁÓWEK

### Wróć do `biblioteka.html`

### Między `<body>` i `</body>` wpisz:

```html
<body>

    <header>
        <h1>BIBLIOTEKA MIEJSKA - KATALOG ONLINE</h1>
        <img src="logo.png" alt="logo biblioteki">
    </header>

</body>
```

### 🤔 Co to znaczy?

- `<header>` = Pudełko na górze (nagłówek)
- `<h1>` = Największy napis
- `<img src="">` = Obrazek

### 💾 ZAPISZ i ODŚWIEŻ przeglądarkę (F5)

✅ **Sprawdź:** Widzisz napis i logo?

---

## 🎨 KROK 7: Malujemy nagłówek na CIEMNO

### Wróć do `style.css`

### Zmień `body` i dodaj `header`:

```css
/* Teraz strona będzie biała */
body {
    background-color: white;
    margin: 0;
    padding: 0;
}

/* Nagłówek ciemnozielony */
header {
    background-color: #2C3E50;
    color: white;
    text-align: center;
    padding: 20px;
}

/* Logo mniejsze */
header img {
    max-width: 120px;
}
```

### 🤔 Co to znaczy?

- `background-color` = kolor tła
- `#2C3E50` = ciemnozielony (kod koloru)
- `color: white` = białe litery
- `text-align: center` = tekst na środku
- `padding: 20px` = odstęp wewnątrz (jak rama obrazu)
- `max-width: 120px` = logo nie większe niż 120 pikseli

### 💾 ZAPISZ i ODŚWIEŻ (F5)

✅ **Sprawdź:** Nagłówek jest ciemnozielony z białymi literami?

---

## 📦 KROK 8: Czym jest FLEXBOX?

### 🎁 Analogia z zabawkami:

Wyobraź sobie że masz **pudełko** i 2 zabawki:
- 🚗 Samochodzik
- 🎾 Piłka

**BEZ Flexbox:** Zabawki się sypią, spadają, są w bałaganie

**Z Flexbox:** Zabawki stoją ładnie **OBOK SIEBIE** jak na półce

### To jest Flexbox - układa rzeczy OBOK SIEBIE!

```
┌─────────────────────┐
│  🚗      🎾        │  ← Flexbox układa obok siebie
└─────────────────────┘
```

---

## 📋 KROK 9: Menu z lewej strony

### Wróć do `biblioteka.html`

### POD `</header>` dodaj:

```html
    <div class="container">
        
        <aside>
            <h2>MENU</h2>
            <ul>
                <li>Katalog</li>
                <li>Nowości</li>
                <li>Promocje</li>
                <li>Kontakt</li>
            </ul>
        </aside>

    </div>
```

### 🤔 Co to znaczy?

- `<div class="container">` = Duże pudełko (na menu i treść)
- `<aside>` = Małe pudełko (menu z lewej)
- `<ul>` = Lista (ul = Unordered List)
- `<li>` = Jeden punkt na liście

### 💾 ZAPISZ i ODŚWIEŻ (F5)

✅ **Sprawdź:** Widzisz "MENU" i 4 punkty?

---

## 🎨 KROK 10: Malujemy menu

### Wróć do `style.css`

### Na końcu pliku dodaj:

```css
/* Główne pudełko - użyjemy Flexbox */
.container {
    display: flex;
}

/* Menu z lewej - ciemne */
aside {
    background-color: #34495E;
    color: white;
    width: 20%;
    padding: 15px;
    min-height: 600px;
}

/* Nagłówek w menu */
aside h2 {
    color: white;
}

/* Lista - bez kropek */
aside ul {
    list-style: none;
    padding: 0;
}

/* Punkty na liście */
aside li {
    padding: 10px;
    margin: 5px 0;
}

/* Gdy najedziemy myszką */
aside li:hover {
    background-color: #1ABC9C;
    cursor: pointer;
}
```

### 🤔 Co to znaczy?

**display: flex** = "Ułóż rzeczy OBOK SIEBIE jak zabawki na półce"

```
PRZED Flexbox:          PO Flexbox:
┌──────────┐            ┌────┬─────────┐
│  Menu    │            │Menu│ Treść   │
├──────────┤            │    │         │
│  Treść   │            │    │         │
└──────────┘            └────┴─────────┘
```

- `width: 20%` = Menu zajmuje 20% szerokości
- `list-style: none` = bez kropek przed punktami
- `:hover` = gdy najedziemy myszką

### 💾 ZAPISZ i ODŚWIEŻ (F5)

✅ **Sprawdź:** 
- Menu jest z lewej, ciemne?
- Gdy najeżdżasz na punkty, zmieniają kolor?

---

## 📰 KROK 11: Główna część (prawa strona)

### Wróć do `biblioteka.html`

### POD `</aside>` (ale PRZED `</div>`) dodaj:

```html
        <main>
            
            <article>
                <h2>NOWOŚCI W BIBLIOTECE</h2>
                <p>W tym miesiącu polecamy nowe pozycje z działu literatury faktu oraz beletrystyki. Zapraszamy do zapoznania się z naszą ofertą i rezerwacji interesujących tytułów online.</p>
                <a href="lista.html">Zobacz pełną listę →</a>
            </article>

        </main>
        
    </div>
```

### 🤔 Jak to wygląda teraz?

```
┌────────────────────────┐
│      NAGŁÓWEK          │
├────────┬───────────────┤
│  MENU  │  ARTYKUŁ      │
│        │  (nowości)    │
└────────┴───────────────┘
```

### 💾 ZAPISZ i ODŚWIEŻ (F5)

✅ **Sprawdź:** Tekst pojawił się **OBOK** menu (z prawej)?

---

## 🎨 KROK 12: Malujemy artykuł

### Wróć do `style.css`

### Na końcu dodaj:

```css
/* Prawa strona - zajmuje resztę miejsca */
main {
    width: 80%;
}

/* Artykuł - ze zdjęciem */
article {
    background-image: url('tlo.jpg');
    background-size: cover;
    color: #2C3E50;
    min-height: 250px;
    padding: 30px;
    font-size: 120%;
}

/* Link */
article a {
    color: #E74C3C;
    font-weight: bold;
    text-decoration: none;
}

/* Link gdy najedziemy */
article a:hover {
    text-decoration: underline;
}
```

### 🤔 Co to znaczy?

- `width: 80%` = Zajmuje 80% szerokości (menu ma 20%, więc razem 100%)
- `background-image: url()` = Obrazek w tle
- `background-size: cover` = Obrazek wypełnia całe miejsce
- `text-decoration: none` = link bez podkreślenia
- `text-decoration: underline` = link z podkreśleniem

### 💾 ZAPISZ i ODŚWIEŻ (F5)

✅ **Sprawdź:** 
- Widzisz zdjęcie w tle artykułu?
- Link jest czerwony?

---

## 📚 KROK 13: Dodajemy 4 pudełka z kategoriami

### Wróć do `biblioteka.html`

### W `<main>`, POD `</article>` dodaj:

```html
            <div class="categories">
                
                <section>
                    <h3>DZIECI</h3>
                    <ul>
                        <li>Bajki</li>
                        <li>Komiksy</li>
                        <li>Edukacja</li>
                    </ul>
                </section>

                <section>
                    <h3>MŁODZIEŻ</h3>
                    <ul>
                        <li>Fantasy</li>
                        <li>Sci-Fi</li>
                        <li>Romans</li>
                    </ul>
                </section>

                <section>
                    <h3>DOROŚLI</h3>
                    <ul>
                        <li>Biografie</li>
                        <li>Kryminał</li>
                        <li>Reportaż</li>
                    </ul>
                </section>

                <section>
                    <h3>NAUKA</h3>
                    <ul>
                        <li>Historia</li>
                        <li>Przyroda</li>
                        <li>Medycyna</li>
                    </ul>
                </section>

            </div>
```

### 🤔 Co mamy?

4 pudełka (`<section>`) - każde ma:
- Tytuł (`<h3>`)
- Listę książek (`<ul>` i `<li>`)

### 💾 ZAPISZ i ODŚWIEŻ (F5)

✅ **Sprawdź:** Widzisz 4 sekcje jedna POD drugą?

---

## 🎨 KROK 14: Malujemy 4 pudełka - FLEXBOX znowu!

### Wróć do `style.css`

### Na końcu dodaj:

```css
/* Kontener na 4 pudełka - FLEXBOX! */
.categories {
    display: flex;
    flex-wrap: wrap;
    padding: 20px;
    gap: 20px;
}

/* Jedno pudełko */
section {
    background-color: #ECF0F1;
    border: 2px solid #BDC3C7;
    border-radius: 8px;
    padding: 15px;
    width: 45%;
    min-height: 180px;
    transition: 0.3s;
}

/* Pudełko gdy najedziemy */
section:hover {
    background-color: #1ABC9C;
    box-shadow: 5px 5px 10px grey;
    transform: scale(1.05);
}

/* Tytuł w pudełku */
section h3 {
    text-align: center;
    color: #E74C3C;
    letter-spacing: 2px;
}

/* Lista w pudełku */
section ul {
    list-style: square;
    margin-left: 20px;
}
```

### 🤔 Co to znaczy?

**display: flex** = Ułóż pudełka obok siebie!

**flex-wrap: wrap** = Gdy się nie mieszczą, przejdź do nowej linii (jak tekst)

```
Pudełko 1   Pudełko 2
Pudełko 3   Pudełko 4
```

- `width: 45%` = Każde pudełko 45% szerokości (2 zmieszczą się obok)
- `gap: 20px` = Odstęp między pudełkami
- `border-radius: 8px` = Zaokrąglone rogi
- `transform: scale(1.05)` = Powiększ trochę (105%)
- `transition: 0.3s` = Zmiana płynna (przez 0.3 sekundy)

### 💾 ZAPISZ i ODŚWIEŻ (F5)

✅ **Sprawdź:** 
- Pudełka są OBOK SIEBIE (2 górne, 2 dolne)?
- Gdy najeżdżasz, powiększają się i zmieniają kolor?

---

## 🦶 KROK 15: Stopka na dole

### Wróć do `biblioteka.html`

### NA SAMYM KOŃCU, POD `</div>` (ale PRZED `</body>`) dodaj:

```html
    <footer>
        <img src="ikona.png" alt="książka">
        Biblioteka Miejska | ul. Główna 15<br>
        Telefon: 123-456-789
    </footer>

</body>
</html>
```

### 💾 ZAPISZ i ODŚWIEŻ (F5)

---

## 🎨 KROK 16: Malujemy stopkę

### Wróć do `style.css`

### Na końcu dodaj:

```css
/* Stopka - ciemnozielona */
footer {
    background-color: #2C3E50;
    color: white;
    text-align: center;
    padding: 15px;
    font-size: 90%;
}

/* Obrazek w stopce */
footer img {
    vertical-align: middle;
    margin-right: 10px;
}
```

### 💾 ZAPISZ i ODŚWIEŻ (F5)

✅ **Sprawdź:** Stopka jest na dole, ciemnozielona?

---

## 📄 KROK 17: Dodatkowa strona

### Otwórz plik `lista.html`

### Przepisz:

```html
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <title>Lista nowości</title>
</head>
<body>
    <p>Pełna lista nowości - strona w przygotowaniu</p>
</body>
</html>
```

### 💾 ZAPISZ

✅ **Sprawdź:** Kliknij link "Zobacz pełną listę" - otwiera się nowa strona?

---

## 📝 KROK 18: Ostatni plik

### Utwórz plik `przeglądarka.txt`

### Wpisz w nim nazwę swojej przeglądarki:

```
Google Chrome
```
(lub Firefox, lub Edge - jaką używasz)

### 💾 ZAPISZ

---

## 🎉 GOTOWE! Sprawdź wszystko!

### ✅ Checklist - co powinieneś widzieć:

1. **Nagłówek (góra)**
   - Ciemnozielony
   - Biały napis "BIBLIOTEKA MIEJSKA - KATALOG ONLINE"
   - Logo

2. **Lewa kolumna (20%)**
   - Ciemna
   - "MENU"
   - 4 punkty
   - Punkty zmieniają kolor gdy najeżdżasz

3. **Prawa kolumna (80%)**
   - Artykuł ze zdjęciem w tle
   - Tytuł "NOWOŚCI W BIBLIOTECE"
   - Tekst
   - Czerwony link

4. **4 pudełka (2 górne, 2 dolne)**
   - Jasne tło
   - Zaokrąglone rogi
   - Gdy najeżdżasz: powiększają się, zmieniają kolor, mają cień

5. **Stopka (dół)**
   - Ciemnozielona
   - Mała ikonka książki
   - Adres i telefon

---

## 🐛 Najczęstsze problemy

### ❌ Menu NIE jest z lewej, jest na górze

**Powód:** Brakuje `display: flex` dla `.container`

**Sprawdź w CSS:**
```css
.container {
    display: flex;  ← To MUSI być!
}
```

---

### ❌ Pudełka są jedno POD drugim, nie obok

**Powód 1:** Brakuje `display: flex` dla `.categories`

**Powód 2:** `width` pudełek jest za duży

**Sprawdź w CSS:**
```css
.categories {
    display: flex;      ← To MUSI być!
    flex-wrap: wrap;    ← To też!
}

section {
    width: 45%;         ← Maksymalnie 48%!
}
```

---

### ❌ Nie widzę obrazków

**Rozwiązanie:**
1. Wszystkie obrazki MUSZĄ być w folderze `zadanie_treningowe_01`
2. Nazwy DOKŁADNIE: `logo.png`, `tlo.jpg`, `ikona.png`
3. Bez wielkich liter! Nie `Logo.png` tylko `logo.png`

---

### ❌ Strona jest brzydka, bez kolorów

**Rozwiązanie:**
1. Sprawdź czy plik `style.css` jest w folderze `zadanie_treningowe_01`
2. Sprawdź czy w HTML jest: `<link rel="stylesheet" href="style.css">`
3. Naciśnij Ctrl+F5 (twardy reload)

---

## 📊 Co to jest Flexbox - podsumowanie

### Prosty schemat:

```
BEZ FLEXBOX:
┌──────────┐
│ Element1 │
├──────────┤
│ Element2 │
└──────────┘

Z FLEXBOX (display: flex):
┌──────────┬──────────┐
│ Element1 │ Element2 │
└──────────┴──────────┘
```

### Flexbox to jak PÓŁKA na książki!
- Książki stoją **OBOK SIEBIE**
- Gdy się nie mieszczą, spadają na niższą półkę (`flex-wrap: wrap`)

---

## 📁 Twój folder powinien mieć:

```
📁 zadanie_treningowe_01/
    📄 biblioteka.html       ← Główna strona
    📄 lista.html            ← Dodatkowa strona
    📄 style.css             ← Kolory i układy
    📄 przeglądarka.txt      ← Nazwa przeglądarki
    🖼️ logo.png             ← Logo
    🖼️ tlo.jpg              ← Tło
    🖼️ ikona.png            ← Mała ikonka (24x24)
```

---

## 💪 Pamiętaj!

1. **Małe kroki** - nie rób wszystkiego naraz
2. **Zapisuj często** - Ctrl + S
3. **Testuj często** - F5 (odśwież)
4. **Czytaj powoli** - nie śpiesz się
5. **Proś o pomoc** - jeśli coś niejasne

### Każdy programista kiedyś się uczył! 

**Ty też potrafisz!** 🌟