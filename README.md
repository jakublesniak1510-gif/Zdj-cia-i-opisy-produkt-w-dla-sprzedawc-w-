# Kadr — zdjęcia i opisy produktów dla sprzedawców

Sprzedawca wgrywa zdjęcie produktu z telefonu i dostaje:
- zdjęcie główne na białym tle zgodne z wymaganiami Allegro (2560×2560),
- aranżacje (blat, łazienka, natura) i komplet 5 ujęć,
- tytuł do 75 znaków, parametry Allegro i opis.

Strona jest statyczna (HTML/CSS/JS, bez buildu). Narzędzia demo działają w przeglądarce, zdjęcia nie są nigdzie wysyłane.

## Struktura

| Ścieżka | Co zawiera |
|---|---|
| `index.html` | Strona główna: studio demo (audyt zdjęcia, kadr 2560×2560, wycinanie tła AI w przeglądarce, aranżacje), generator i sprawdzanie tytułów, generator opisów, kalkulator oszczędności, porównanie, cennik, FAQ |
| `blog/` | Poradnik SEO: 3 artykuły + lista (`blog/index.html`) |
| `og-image.png`, `assets/og-template.html` | Grafika do udostępniania w social mediach i jej źródło |
| `favicon.svg` | Ikona strony |
| `robots.txt`, `sitemap.xml`, `404.html` | Pliki techniczne hostingu |
| `PLAN.md` | Zrecenzowany plan biznesowy: poprawki, dodatki, cennik, plan 4 tygodni, ryzyka |

## Uruchomienie

Lokalnie: `python3 -m http.server 8000` w katalogu repozytorium i otwórz `http://localhost:8000` (wycinanie tła AI wymaga http, nie `file://`).
Hosting: wrzuć repozytorium na Cloudflare Pages, Vercel, Netlify lub GitHub Pages.

## Przed publikacją pod własną domeną

1. Zamień placeholder `https://ZMIEN-NA-DOMENE.pl/` w `sitemap.xml`, `robots.txt` i w nagłówkach stron (`canonical`, `og:url`).
2. Ustaw bezwzględny adres `og:image` (Facebook i LinkedIn nie akceptują względnego).
3. Podłącz formularz e-mail do narzędzia do leadów (Formspree, MailerLite, Supabase); dziś adresy zapisują się tylko w przeglądarce użytkownika.
4. Podmień linki Regulamin / Polityka prywatności / Kontakt w stopce.

## Następne kroki biznesowe

Zobacz sekcję „Plan 4 tygodni” w `PLAN.md`.
