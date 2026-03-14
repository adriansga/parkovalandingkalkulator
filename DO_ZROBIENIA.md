# DO ZROBIENIA — Parkova Hotel Strona
**Data:** 14.03.2026 | Wykonaj przed opublikowaniem strony

---

## 🔴 KRYTYCZNE (przed publikacją)

### 1. Google Analytics 4 — zastąp ID
**Plik:** `index.html` → linia ~19
```
Znajdź:   G-XXXXXXXXXX
Zastąp:   Twoim prawdziwym ID (np. G-ABC123XYZ)
```
**Jak zdobyć:** analytics.google.com → Utwórz konto → Strumień danych → skopiuj Measurement ID

---

### 2. Facebook Pixel — zastąp ID
**Plik:** `index.html` → linia ~29
```
Znajdź:   XXXXXXXXXXXXX
Zastąp:   Twoim prawdziwym ID piksela (16 cyfr)
```
**Jak zdobyć:** business.facebook.com → Events Manager → Pixel → Ustawienia → skopiuj Pixel ID

---

### 3. Formspree — skonfiguruj formularz kontaktowy
**Plik:** `index.html` → wyszukaj: `FORMSPREE_ID`
```
Znajdź:   https://formspree.io/f/FORMSPREE_ID
Zastąp:   https://formspree.io/f/TwójKod (np. xpwdrgkj)
```
**Jak zdobyć:**
1. Wejdź na formspree.io
2. Zarejestruj się za darmo
3. Utwórz nowy formularz → wpisz email docelowy
4. Skopiuj Form ID (8 znaków po /f/)
5. Darmowy plan: 50 zgłoszeń/miesiąc

---

### 4. Polityka Prywatności — utwórz plik
**Plik:** `polityka-prywatnosci.html` (w tym samym folderze co index.html)

Minimalne wymagania RODO:
- Kto jest administratorem danych (Rezydencja Parkova, Gierłoż 2)
- Jakie dane zbierasz (imię, telefon, email)
- W jakim celu (odpowiedź na zapytanie, rezerwacja)
- Jak długo przechowujesz (sugestia: 12 miesięcy)
- Prawa użytkownika (dostęp, usunięcie, sprzeciw)
- Kontakt: biuro@rezydencjaparkova.pl

Możesz wygenerować przez: iubenda.com lub termsandconditions.org

---

### 5. Regulamin — utwórz plik
**Plik:** `regulamin.html` (w tym samym folderze co index.html)

Minimalne wymagania:
- Zasady rezerwacji i anulowania
- Polityka płatności i zaliczek
- Check-in / check-out godziny
- Zasady pobytu zwierząt
- Odpowiedzialność za szkody

---

## 🟡 WAŻNE (w ciągu tygodnia po publikacji)

### 6. Konwertuj obrazy na WebP
Obecny format: PNG (wolniejsze ładowanie)
Zalecany format: WebP (30-80% mniejszy rozmiar)

**Narzędzia (darmowe):**
- squoosh.app — przeciągnij PNG, eksportuj jako WebP, jakość 80%
- cloudconvert.com — konwersja batch

**Pliki do konwersji:**
```
img/01_slider_glowne.png → 01_slider_glowne.webp
img/02_obiekt.png        → 02_obiekt.webp
img/03_galeria.png       → 03_galeria.webp
img/04_pokoj.png         → 04_pokoj.webp
img/05_zdj2.png          → 05_zdj2.webp
img/06_zdj4.png          → 06_zdj4.webp
img/07_zdj5.png          → 07_zdj5.webp
```

Po konwersji zaktualizuj nazwy plików w index.html (`.png` → `.webp`).

---

### 7. Utwórz sitemap.xml
**Plik:** `sitemap.xml` (w głównym folderze strony, obok index.html)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://rezydencjaparkova.pl/</loc>
    <lastmod>2026-03-14</lastmod>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
</urlset>
```

---

### 8. Utwórz robots.txt
**Plik:** `robots.txt` (w głównym folderze strony)

```
User-agent: *
Allow: /
Disallow: /backup/
Sitemap: https://rezydencjaparkova.pl/sitemap.xml
```

---

### 9. Zgłoś stronę do Google Search Console
1. Wejdź na search.google.com/search-console
2. Dodaj właściwość: rezydencjaparkova.pl
3. Zweryfikuj przez Google Analytics (jeśli GA4 już działa) lub plik HTML
4. Prześlij sitemap.xml

---

## ⚪ DO ROZWAŻENIA (opcjonalne)

### 10. Opublikuj prawdziwe opinie
Strona ma 6 przykładowych opinii. Warto je zastąpić prawdziwymi lub
uzupełnić o widżet Booking.com / Google Reviews.

### 11. Sprawdź numer telefonu w kalkulatorze
Kalkulator grupowy pokazuje tel: +48 886 120 501. Potwierdź, że to właściwy numer dla zapytań grupowych.

### 12. Dodaj favicon
Utwórz plik `favicon.ico` lub `favicon.png` i dodaj do `<head>`:
```html
<link rel="icon" type="image/png" href="favicon.png">
```

### 13. Test formularza po podłączeniu Formspree
Wyślij testowe zapytanie i sprawdź czy email dochodzi na biuro@rezydencjaparkova.pl

### 14. Test na telefonie
Sprawdź:
- [ ] FAB (pulsujący telefon) widoczny i klikalny
- [ ] Sticky CTA na dole działa
- [ ] Formularz kontaktowy działa
- [ ] Kalkulator grupowy działa
- [ ] Hamburger menu otwiera się i zamyka
- [ ] Mapa ładuje się poprawnie

---

## KOLEJNOŚĆ DZIAŁAŃ

```
1. Formspree (5 min) → formularz zacznie zbierać leady
2. Google Analytics (10 min) → dane od pierwszej wizyty
3. Facebook Pixel (10 min) → możliwość reklam
4. Polityka Prywatności (30 min) → wymagane prawnie
5. Regulamin (30 min) → wymagane prawnie
6. robots.txt + sitemap.xml (5 min) → SEO
7. Google Search Console (15 min) → indeksowanie
8. Konwersja obrazów WebP (1h) → szybkość
```

---

**Kontakt do dewelopera:** biuro@rezydencjaparkova.pl
