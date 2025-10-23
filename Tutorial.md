# 📘 Tutorial: Jak zbudować stronę "Biblioteka Miejska" - HTML i CSS

## 🎯 Dla kogo jest ten tutorial?
Ten tutorial jest dla Ciebie! Pokażę Ci **krok po kroku**, jak zrobić stronę dla biblioteki. Nie śpiesz się. Czytaj spokojnie. 

---

## 📂 Krok 1: Przygotuj folder i pliki

### Co musisz zrobić:

1. **Otwórz swoje repozytorium** (główny folder z zadaniami)
2. **Stwórz NOWY folder** o nazwie: `zadanie_treningowe_01`
3. **Wszystkie pliki** z tego zadania wrzucaj TYLKO do tego folderu!

### Dlaczego to ważne?
Każde zadanie w osobnym folderze = **porządek** = łatwiej znaleźć pliki!

```
📁 Moje_Repozytorium/
    📁 zadanie_treningowe_01/  ← TU PRACUJESZ!
        📄 (tutaj będą Twoje pliki)
```

---

## 🖼️ Krok 2: Przygotuj obrazki

### Co masz z archiwum:
- `logo.png` - logo biblioteki
- `tlo.jpg` - zdjęcie biblioteki
- `ikona.png` - obrazek książki

### Co musisz zrobić:

1. **Skopiuj wszystkie 3 obrazki** do folderu `zadanie_treningowe_01`
2. **Otwórz program do edycji grafiki** (np. GIMP, Paint.NET, Photoshop)
3. **Otwórz plik `ikona.png`**
4. **Zmień rozmiar** na dokładnie: **24 piksele × 24 piksele**
5. **Zapisz** plik (nadpisz stary)

### 💡 Wskazówka:
- W GIMP: `Obraz` → `Skaluj obraz` → wpisz 24 i 24
- W Paint.NET: `Obraz` → `Zmień rozmiar` → wpisz 24 i 24

---

## 📄 Krok 3: Utwórz puste pliki

W folderze `zadanie_treningowe_01` utwórz **3 nowe pliki**:

1. `biblioteka.html` - główna strona
2. `lista.html` - dodatkowa strona
3. `style.css` - style

### Jak utworzyć plik?
- Prawy przycisk myszy → `Nowy` → `Dokument tekstowy`
- Zmień nazwę (razem z rozszerzeniem!)

---

## 🏗️ Krok 4: Szkielet HTML (biblioteka.html)

### Zacznij od podstawy:

```html
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <title>Biblioteka Miejska - Katalog</title>
</head>
<body>

</body>
</html>
```

### 🔍 Co tu mamy?
- `<!DOCTYPE html>` = To jest HTML5
- `lang="pl"` = Strona po polsku
- `charset="UTF-8"` = Polskie znaki będą działać (ą, ę, ć...)
- `<title>` = Nazwa na karcie przeglądarki

---

## 🔗 Krok 5: Dodaj favicon i CSS

### W sekcji `<head>` dodaj dwie linijki:

```html
<head>
    <meta charset="UTF-8">
    <title>Biblioteka Miejska - Katalog</title>
    <link rel="icon" href="ikona.png" type="image/png">
    <link rel="stylesheet" href="style.css">
</head>
```

### 🔍 Co to robi?
- `rel="icon"` = Mała ikonka na karcie przeglądarki
- `rel="stylesheet"` = Podłączamy plik ze stylami CSS

---

## 🏛️ Krok 6: Budujemy strukturę - 5 głównych bloków

### Nasza strona ma 5 części:

```
1. NAGŁÓWEK       (na samej górze)
2. MENU Z LEWEJ   (lewa kolumna)
3. GŁÓWNA CZĘŚĆ   (prawa kolumna)
4. STOPKA         (na samym dole)
```

### Zacznij od nagłówka w `<body>`:

```html
<body>

    <!-- BLOK 1: NAGŁÓWEK -->
    <header>
        <h1>BIBLIOTEKA MIEJSKA - KATALOG ONLINE</h1>
        <img src="logo.png" alt="logo biblioteki">
    </header>

</body>
```

### ✅ Zapisz i otwórz w przeglądarce!
- Powinieneś zobaczyć: napis i obrazek (jeśli logo.png jest w folderze)

---

## 📋 Krok 7: Menu z lewej strony

### Dodaj menu POD nagłówkiem:

```html
    <!-- BLOK 2: MENU Z LEWEJ -->
    <aside>
        <h2>MENU</h2>
        <ul>
            <li>Katalog</li>
            <li>Nowości</li>
            <li>Promocje</li>
            <li>Kontakt</li>
        </ul>
    </aside>
```

### 🔍 Co to jest?
- `<aside>` = Blok boczny (semantyczny znacznik HTML5)
- `<ul>` = Lista nieuporządkowana (bez numerów)
- `<li>` = Jeden element listy

---

## 📰 Krok 8: Główna część - artykuł

### Dodaj główną część POD menu:

```html
    <!-- BLOK 3: GŁÓWNA CZĘŚĆ -->
    <main>
        
        <!-- ARTYKUŁ -->
        <article>
            <h2>NOWOŚCI W BIBLIOTECE</h2>
            <p>W tym miesiącu polecamy nowe pozycje z działu literatury faktu oraz beletrystyki. Zapraszamy do zapoznania się z naszą ofertą i rezerwacji interesujących tytułów online.</p>
            <a href="lista.html">Zobacz pełną listę →</a>
        </article>

    </main>
```

### 🔍 Co tu mamy?
- `<main>` = Główna treść strony
- `<article>` = Artykuł (sekcja z nowościami)
- `<a href="">` = Link do innej strony

---

## 📚 Krok 9: Cztery kategorie książek

### W tym samym `<main>`, POD artykułem dodaj:

```html
        <!-- KONTENER NA 4 SEKCJE -->
        <div class="categories">
            
            <!-- SEKCJA 1: DZIECI -->
            <section>
                <h3>DZIECI</h3>
                <ul>
                    <li>Bajki</li>
                    <li>Komiksy</li>
                    <li>Edukacja</li>
                </ul>
            </section>

            <!-- SEKCJA 2: MŁODZIEŻ -->
            <section>
                <h3>MŁODZIEŻ</h3>
                <ul>
                    <li>Fantasy</li>
                    <li>Sci-Fi</li>
                    <li>Romans</li>
                </ul>
            </section>

            <!-- SEKCJA 3: DOROŚLI -->
            <section>
                <h3>DOROŚLI</h3>
                <ul>
                    <li>Biografie</li>
                    <li>Kryminał</li>
                    <li>Reportaż</li>
                </ul>
            </section>

            <!-- SEKCJA 4: NAUKA -->
            <section>
                <h3>NAUKA</h3>
                <ul>
                    <li>Historia</li>
                    <li>Przyroda</li>
                    <li>Medycyna</li>
                </ul>
            </section>

        </div>
        
    </main>
```

### 🔍 Co to robi?
- `<div class="categories">` = Kontener na 4 pudełka
- `<section>` = Jedno pudełko z kategorią
- Mamy 4 sekcje = 4 pudełka

---

## 🦶 Krok 10: Stopka (na samym dole)

### Na końcu, POD `</main>` dodaj stopkę:

```html
    <!-- BLOK 4: STOPKA -->
    <footer>
        <img src="ikona.png" alt="książka">
        Biblioteka Miejska | ul. Główna 15<br>
        Telefon: 123-456-789
    </footer>

</body>
</html>
```

### 🔍 Co to jest?
- `<footer>` = Stopka strony
- `<br>` = Przejście do nowej linii

---

## ✅ Krok 11: Sprawdź HTML

### Twój pełny plik `biblioteka.html` powinien mieć:

```
<!DOCTYPE html>
<html lang="pl">
<head>
    ← meta, title, link (favicon), link (css)
</head>
<body>
    <header>
        ← h1, img
    </header>
    
    <aside>
        ← h2, ul z 4 li
    </aside>
    
    <main>
        <article>
            ← h2, p, a
        </article>
        
        <div class="categories">
            <section> ← h3, ul z 3 li </section>
            <section> ← h3, ul z 3 li </section>
            <section> ← h3, ul z 3 li </section>
            <section> ← h3, ul z 3 li </section>
        </div>
    </main>
    
    <footer>
        ← img, tekst
    </footer>
</body>
</html>
```

### 💾 ZAPISZ plik!

---

## 📄 Krok 12: Mała strona (lista.html)

### Utwórz prosty plik `lista.html`:

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

### 💾 ZAPISZ plik!

---

## 🎨 Krok 13: Teraz STYLE! (style.css)

### Otwórz plik `style.css` i zacznij pisać:

---

### CZĘŚĆ 1: Podstawy dla wszystkich elementów

```css
/* Dla wszystkich elementów */
* {
    font-family: Verdana;
    margin: 0;
    padding: 0;
}
```

### 🔍 Co to robi?
- `*` = wszystkie elementy
- `font-family` = czcionka
- `margin: 0` = bez marginesów zewnętrznych
- `padding: 0` = bez marginesów wewnętrznych

---

### CZĘŚĆ 2: Układ strony (CSS Grid)

```css
/* Układ całej strony - 2 kolumny */
body {
    display: grid;
    grid-template-columns: 20% 80%;
}
```

### 🔍 Co to robi?
- `display: grid` = używamy siatki CSS Grid
- `20% 80%` = lewa kolumna 20%, prawa 80%

---

### CZĘŚĆ 3: Nagłówek

```css
/* Nagłówek - ciemnozielony */
header {
    background-color: #2C3E50;
    color: white;
    text-align: center;
    padding: 20px;
    grid-column: 1 / 3;
}

/* Logo w nagłówku */
header img {
    max-width: 120px;
    margin-top: 10px;
}
```

### 🔍 Co to robi?
- `grid-column: 1 / 3` = nagłówek zajmuje OBIE kolumny
- `background-color` = kolor tła
- `text-align: center` = tekst na środku

---

### CZĘŚĆ 4: Menu z lewej (sidebar)

```css
/* Menu z lewej - ciemnoniebieski */
aside {
    background-color: #34495E;
    color: white;
    padding: 15px;
    min-height: 600px;
}

/* Lista w menu */
aside ul {
    list-style: none;
}

/* Elementy listy */
aside li {
    padding: 10px;
    font-size: 110%;
}

/* Gdy najedziemy myszką */
aside li:hover {
    background-color: #1ABC9C;
    cursor: pointer;
}
```

### 🔍 Co to robi?
- `list-style: none` = bez punktorów
- `:hover` = gdy najedziemy myszką
- `cursor: pointer` = zmienia kursor na rękę

---

### CZĘŚĆ 5: Artykuł z nowościami

```css
/* Artykuł - ze zdjęciem w tle */
article {
    background-image: url('tlo.jpg');
    color: #2C3E50;
    min-height: 250px;
    padding: 30px;
    font-size: 120%;
}

/* Link w artykule */
article a {
    color: #E74C3C;
    font-weight: bold;
    text-decoration: none;
}

/* Link gdy najedziemy */
article a:hover {
    text-decoration: underline;
    color: #C0392B;
}
```

### 🔍 Co to robi?
- `background-image: url()` = obrazek w tle
- `text-decoration: none` = bez podkreślenia
- `text-decoration: underline` = z podkreśleniem

---

### CZĘŚĆ 6: Kontener na 4 sekcje

```css
/* Kontener - siatka 2x2 */
.categories {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: auto auto;
    gap: 20px;
    padding: 20px;
}
```

### 🔍 Co to robi?
- `1fr 1fr` = dwie równe kolumny
- `gap: 20px` = odstęp między elementami

---

### CZĘŚĆ 7: Cztery sekcje (pudełka)

```css
/* Sekcje - jasne pudełka */
section {
    background-color: #ECF0F1;
    border: 2px solid #BDC3C7;
    border-radius: 8px;
    padding: 15px;
    min-height: 180px;
    transition: 0.3s;
}

/* Sekcje gdy najedziemy */
section:hover {
    background-color: #1ABC9C;
    box-shadow: 5px 5px 10px #7F8C8D;
    transform: scale(1.05);
}

/* Nagłówki H3 w sekcjach */
section h3 {
    text-align: center;
    color: #E74C3C;
    letter-spacing: 2px;
}

/* Listy w sekcjach */
section ul {
    list-style: square;
    margin-left: 20px;
}
```

### 🔍 Co to robi?
- `border-radius` = zaokrąglone rogi
- `box-shadow` = cień
- `transform: scale(1.05)` = powiększenie o 5%
- `transition` = płynna animacja

---

### CZĘŚĆ 8: Nagłówki H2 i H3

```css
/* Nagłówki */
h2, h3 {
    color: #2C3E50;
    margin: 10px 0;
}
```

---

### CZĘŚĆ 9: Stopka

```css
/* Stopka - ciemnozielona */
footer {
    background-color: #2C3E50;
    color: white;
    text-align: center;
    padding: 15px;
    font-size: 90%;
    grid-column: 1 / 3;
}

/* Obrazek w stopce */
footer img {
    vertical-align: middle;
    margin-right: 10px;
}
```

### 🔍 Co to robi?
- `grid-column: 1 / 3` = stopka zajmuje obie kolumny
- `vertical-align: middle` = obrazek wyrównany w środku

---

## 💾 Krok 14: Zapisz CSS!

### Twój plik `style.css` powinien mieć 9 części:
1. ✅ Podstawy (*)
2. ✅ Układ body
3. ✅ Header
4. ✅ Aside (menu)
5. ✅ Article
6. ✅ .categories
7. ✅ Section
8. ✅ h2, h3
9. ✅ Footer

---

## 🧪 Krok 15: TESTUJ!

### Co zrobić:

1. **Otwórz `biblioteka.html`** w przeglądarce (kliknij 2 razy)
2. **Sprawdź czy widzisz:**
   - ✅ Ciemnozielony nagłówek z logo
   - ✅ Ciemne menu z lewej
   - ✅ Artykuł ze zdjęciem w tle
   - ✅ 4 pudełka obok siebie (2 w górze, 2 na dole)
   - ✅ Ciemnozieloną stopkę

3. **Najedź myszką:**
   - Na elementy menu → zmienia się kolor?
   - Na pudełka → powiększają się i zmieniają kolor?
   - Na link → pojawia się podkreślenie?

---

## 🐛 Coś nie działa? Sprawdź!

### ❌ Problem: Strona wygląda brzydko (bez kolorów)

**Możliwe przyczyny:**
- Plik `style.css` NIE jest w tym samym folderze co `biblioteka.html`
- W HTML brakuje linii: `<link rel="stylesheet" href="style.css">`
- Literówka w nazwie pliku (sprawdź wielkie/małe litery!)

**Rozwiązanie:**
- Upewnij się że oba pliki są w `zadanie_treningowe_01`
- Sprawdź czy w `<head>` jest link do CSS

---

### ❌ Problem: Menu i treść są POD sobą, nie OBOK

**Możliwe przyczyny:**
- Brakuje `display: grid;` w CSS dla `body`
- Brakuje `grid-template-columns: 20% 80%;`

**Rozwiązanie:**
- Sprawdź czy w CSS masz:
```css
body {
    display: grid;
    grid-template-columns: 20% 80%;
}
```

---

### ❌ Problem: Nie widzę obrazków

**Możliwe przyczyny:**
- Obrazki są w INNYM folderze
- Nazwy plików są źle napisane
- Ikona nie jest 24x24 px

**Rozwiązanie:**
- Wszystkie obrazki MUSZĄ być w `zadanie_treningowe_01`
- Nazwy DOKŁADNIE: `logo.png`, `tlo.jpg`, `ikona.png`

---

### ❌ Problem: 4 pudełka są jedno pod drugim, nie 2x2

**Możliwe przyczyny:**
- Brakuje CSS Grid dla `.categories`

**Rozwiązanie:**
- Sprawdź czy masz:
```css
.categories {
    display: grid;
    grid-template-columns: 1fr 1fr;
}
```

---

### ❌ Problem: Pudełka nie powiększają się gdy najeżdżam

**Możliwe przyczyny:**
- Brakuje `section:hover` w CSS

**Rozwiązanie:**
- Dodaj:
```css
section:hover {
    transform: scale(1.05);
    transition: 0.3s;
}
```

---

## 📋 Krok 16: Ostatnie rzeczy

### Utwórz plik `przeglądarka.txt`:

1. **Utwórz nowy plik tekstowy** w folderze `zadanie_treningowe_01`
2. **Nazwij go:** `przeglądarka.txt`
3. **Wpisz w nim** nazwę przeglądarki, której używałeś (np. "Google Chrome", "Firefox", "Edge")
4. **Zapisz**

---

## ✅ Checklist - Lista kontrolna

Zaznacz ✅ gdy zrobisz:

**PLIKI I FOLDER:**
- [ ] Utworzyłem folder `zadanie_treningowe_01`
- [ ] Wszystkie pliki są W ŚRODKU tego folderu
- [ ] Przeskalowałem `ikona.png` do 24x24 px

**HTML - biblioteka.html:**
- [ ] Dodałem `<!DOCTYPE html>`
- [ ] Dodałem `lang="pl"`
- [ ] Dodałem `<meta charset="UTF-8">`
- [ ] Dodałem tytuł: "Biblioteka Miejska - Katalog"
- [ ] Dodałem favicon (ikona.png)
- [ ] Podłączyłem CSS (style.css)
- [ ] Utworzyłem `<header>` z H1 i logo
- [ ] Utworzyłem `<aside>` z menu (H2 + UL z 4 LI)
- [ ] Utworzyłem `<main>`
- [ ] W main jest `<article>` (H2 + P + A)
- [ ] W main jest `<div class="categories">`
- [ ] W categories są 4 `<section>` (każda z H3 + UL)
- [ ] Utworzyłem `<footer>` z obrazkiem i tekstem

**HTML - lista.html:**
- [ ] Utworzyłem plik lista.html
- [ ] Dodałem podstawową strukturę HTML5
- [ ] Dodałem tekst "Pełna lista nowości - strona w przygotowaniu"

**CSS - style.css:**
- [ ] Dodałem style dla `*` (Verdana, margin 0, padding 0)
- [ ] Dodałem `display: grid` dla body
- [ ] Dodałem style dla `header`
- [ ] Dodałem style dla `header img`
- [ ] Dodałem style dla `aside`
- [ ] Dodałem style dla `aside ul` i `aside li`
- [ ] Dodałem `:hover` dla `aside li`
- [ ] Dodałem style dla `article`
- [ ] Dodałem style dla `article a`
- [ ] Dodałem `:hover` dla `article a`
- [ ] Dodałem `display: grid` dla `.categories`
- [ ] Dodałem style dla `section`
- [ ] Dodałem `:hover` dla `section`
- [ ] Dodałem style dla `section h3`
- [ ] Dodałem style dla `section ul`
- [ ] Dodałem style dla `h2, h3`
- [ ] Dodałem style dla `footer`
- [ ] Dodałem style dla `footer img`

**TESTY:**
- [ ] Otworzyłem stronę w przeglądarce
- [ ] Nagłówek jest ciemnozielony
- [ ] Menu jest z lewej, ciemne
- [ ] Artykuł ma tło ze zdjęcia
- [ ] 4 pudełka są obok siebie (2x2)
- [ ] Menu zmienia kolor gdy najeżdżam
- [ ] Pudełka powiększają się gdy najeżdżam
- [ ] Link ma podkreślenie gdy najeżdżam
- [ ] Stopka jest na dole, ciemnozielona

**DOKUMENTACJA:**
- [ ] Utworzyłem plik `przeglądarka.txt`
- [ ] Zapisałem nazwę przeglądarki

---

## 📁 Twój folder powinien wyglądać tak:

```
📁 zadanie_treningowe_01/
    📄 biblioteka.html
    📄 lista.html
    📄 style.css
    📄 przeglądarka.txt
    🖼️ logo.png
    🖼️ tlo.jpg
    🖼️ ikona.png (24x24px)
```

---

## 💡 Wskazówki na koniec

1. **Zapisuj często** - Ctrl + S po każdej zmianie
2. **Odświeżaj przeglądarkę** - F5 po każdej zmianie
3. **Sprawdzaj małe kroki** - nie pisz wszystkiego naraz
4. **Czytaj komunikaty** - jeśli coś nie działa, przeglądarka może pokazać błąd
5. **Porównuj z zadaniem** - czy Twoja strona wygląda podobnie do opisu?

---

## 🎓 Pamiętaj!

- Każdy blok HTML ma swoje znaczenie (header, aside, main, footer)
- CSS Grid to potężne narzędzie do układania elementów
- Efekty `:hover` sprawiają że strona jest interaktywna
- Dobra organizacja plików = mniej problemów

**Nie poddawaj się! Każdy błąd to szansa na naukę!** 💪

---

## 🆘 Potrzebujesz pomocy?

### Gdzie szukać odpowiedzi:
1. Przeczytaj jeszcze raz instrukcję
2. Sprawdź czy wszystkie pliki są we właściwym folderze
3. Sprawdź czy nie masz literówek
4. Porównaj swój kod z wymaganiami w zadaniu

**Powodzenia!** 🍀