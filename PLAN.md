# Kadr — zdjęcia i opisy produktów dla sprzedawców (brief po recenzji)

Robocza nazwa: **Kadr** (krótka, polska, łatwa do zapamiętania; alternatywy: Wystaw.to, FotoSprzedaj, Studio Sprzedawcy).

## 1. Co zostaje bez zmian
- Grupa docelowa: małe sklepy Allegro/Erli, sprzedawcy Vinted/OLX, rękodzielnicy.
- Rdzeń produktu: zdjęcie z telefonu → białe tło pod Allegro + aranżacja + tytuł/opis/parametry.
- Przewaga: polski język, opisy pod wyszukiwarkę Allegro, BLIK, obsługa po polsku.
- Kanały: TikTok „przed/po”, grupy FB sprzedawców, SEO, darmowe narzędzie zbierające rejestracje.

## 2. Co poprawiłem (błędy i sprzeczności w oryginale)

1. **Sprzeczność: „od początku SaaS” vs „wersja ręczna na start”.**
   Rozwiązanie: *concierge MVP*. Od pierwszego dnia klient używa tej samej strony i formularza
   co docelowy SaaS (upload, wybór stylu, płatność BLIK). Z tyłu obróbkę robimy ręcznie
   (Photoroom + LLM) i każdy wynik sprawdza człowiek. Klient nie widzi różnicy, a my uczymy się,
   co psuje się najczęściej. Automatyzację włączamy stopniowo, bez zmiany frontu.

2. **„Koszt API to grosze” — nieprecyzyjne.** Realne koszty jednostkowe (2026, orientacyjnie):
   usuwanie tła 0,05–0,20 zł; aranżacja generatywna 0,15–0,40 zł; opis z LLM poniżej 0,05 zł.
   Pakiet „Sklep” (200 zdjęć + 200 opisów) kosztuje nas ok. 20–60 zł, marża 40–80 % po
   prowizji operatora płatności. Nadal dobrze, ale nie „grosze”. Przy darmowym planie
   limit 3 zdjęć jest kluczowy, żeby nie dopłacać do botów.

3. **Wirtualna przymierzalnia na Vinted — ryzyko, nie „duża wartość”.**
   Regulamin Vinted wymaga zdjęć rzeczywistego przedmiotu i karze za zdjęcia mylące kupujących.
   Zdjęcie ubrania „na modelce AI” może zostać uznane za wprowadzające w błąd. Dodatkowo od
   2 sierpnia 2026 obowiązuje art. 50 AI Act (oznaczanie treści generowanych przez AI,
   w tym syntetycznych osób). Decyzja: przymierzalnia schodzi do fazy 3, tylko jako
   **zdjęcie dodatkowe** z automatycznym oznaczeniem „wizualizacja AI”, nigdy jako zdjęcie główne.

4. **Wymagania Allegro dla zdjęcia głównego — doprecyzowane.**
   Białe tło, produkt wypełnia kadr, bez znaków wodnych, napisów i ramek, minimum 500 px,
   zalecane 2560 px dłuższy bok, maks. 16 zdjęć w ofercie. Narzędzie ma eksportować gotowy
   kwadrat 2560×2560 JPG, bo to najczęstszy błąd małych sprzedawców.

5. **Tytuł do 75 znaków — prawda, ale to za mało.** Allegro liczy też *parametry*
   (marka, model, kolor, rozmiar, stan) i to one decydują o pozycji w filtrach.
   Generator musi oddawać tytuł + listę parametrów pod kategorię + opis, nie sam tytuł.

6. **Kolejność „Pierwszych kroków” — zmieniona.** „Przy 20+ płacących zbuduj narzędzie”
   odwleka automatyzację o miesiące. Nowy plan niżej (pkt 5).

## 3. Co dodaję od siebie

- **Zestaw „Oferta w 60 sekund”**: z jednego zdjęcia robimy komplet 5 ujęć
  (główne na białym tle, 2 aranżacje, zbliżenie detalu, kadr z wymiarami), bo Allegro
  premiuje oferty z wieloma zdjęciami. Sprzedajemy komplet, nie pojedyncze zdjęcie.
- **Gwarancja prawdziwego produktu**: tryb pracy, w którym AI *nie wolno* zmieniać kształtu,
  koloru, logo ani śladów użytkowania. Podmieniamy wyłącznie tło i światło. To argument
  sprzedażowy („bez reklamacji”) i zabezpieczenie prawne (prawo konsumenckie, dyrektywa Omnibus).
- **Eksport do Allegro przez API** (faza 2): jeden klik „wystaw” z gotowymi zdjęciami,
  tytułem, parametrami i opisem. Dla sklepów: CSV do Erli, BaseLinker, WooCommerce.
- **Darmowe narzędzie lead-magnet**: generator tytułów Allegro (licznik 75 znaków,
  podpowiedzi parametrów) działający bez logowania. Pobiera e-mail przy zapisie wyniku.
- **Program partnerski** dla twórców TikTok/YouTube o sprzedaży na Vinted/Allegro
  (20 % prowizji przez 6 miesięcy) i dla agencji Allegro Ads.
- **Mierniki od dnia 1**: aktywacja (pierwsze przetworzone zdjęcie), konwersja darmowy→płatny
  (cel 5 %), koszt API na zdjęcie, churn miesięczny (cel < 8 %), NPS po 10 zdjęciach.
- **Hosting w UE i usuwanie zdjęć po 30 dniach** — RODO, a dla rękodzielników ochrona wzorów.

## 4. Cennik (bez zmian w kwotach, doprecyzowana zawartość)

| Plan      | Zawartość                                                      | Cena        |
|-----------|----------------------------------------------------------------|-------------|
| Darmowy   | 3 zdjęcia ze znakiem wodnym, 3 tytuły                          | 0 zł        |
| Na start  | 30 zdjęć + 30 opisów, bez abonamentu, ważne 12 mies.           | 29 zł       |
| Sklep     | 200 zdjęć + 200 opisów/mies., komplety 5 ujęć, eksport Allegro | 99 zł/mies. |
| Pro       | 1000 zdjęć/mies., masowe przetwarzanie (ZIP, 50 naraz), API    | 249 zł/mies.|

Płatności: BLIK, karta, Przelewy24 (Stripe obsługuje BLIK w Polsce). Faktura VAT automatycznie.

## 5. Plan 4 tygodni (poprawiony)

- **Tydzień 1** — strona + formularz + płatność; 10 znajomych sprzedawców dostaje komplet za darmo w zamian za opinię i zdjęcia „przed/po” do TikToka.
- **Tydzień 2** — concierge MVP: pakiety „Na start” sprzedawane w grupach FB; obróbka ręczna, każda oferta sprawdzona ręcznie pod regulamin Allegro.
- **Tydzień 3** — automatyzacja usuwania tła i opisów (API), kolejka zadań, kredyty. Darmowy generator tytułów jako lead-magnet.
- **Tydzień 4** — abonamenty Sklep/Pro, masowy upload, pierwsze 3 filmy TikTok, 2 artykuły SEO.
- Decyzja po 4 tygodniach: ≥ 20 płacących i konwersja ≥ 3 % → budujemy eksport do Allegro API. Mniej → zmieniamy kanał, nie produkt.

## 6. Technologia (rekomendacja)

- Front: statyczna strona (HTML/CSS/JS) na Cloudflare Pages lub Vercel — szybko, tanio, dobre SEO.
- Backend (faza 2): Supabase (auth, baza, storage w UE) + funkcje serverless; kolejka zadań.
- Obrazy: API usuwania tła (Photoroom / remove.bg) + model generatywny do aranżacji z maską produktu (inpainting tła, produkt nietknięty).
- Teksty: API modelu językowego z systemowym promptem pod Allegro (75 znaków, parametry, zakazane słowa, bez superlatyw niemożliwych do udowodnienia).
- Płatności: Stripe (BLIK, karta) lub Przelewy24.

## 7. Ryzyka i jak je ograniczamy

| Ryzyko | Mitygacja |
|---|---|
| AI zmienia wygląd produktu → reklamacje, blokady kont | tryb „tylko tło”, maska produktu, kontrola wizualna w MVP, komunikat w produkcie |
| Zmiana regulaminu Allegro/Vinted ws. treści AI | monitoring regulaminów co miesiąc, oznaczanie wizualizacji, przymierzalnia tylko jako zdjęcie dodatkowe |
| AI Act art. 50 (od 08.2026) | automatyczny znacznik na wizualizacjach z osobami, informacja w opisie |
| Konkurencja globalna (Photoroom, Pixelcut, Claid) | nisza PL: Allegro-parametry, BLIK, faktury, eksport do Allegro/Erli/BaseLinker |
| Koszty API przy darmowym planie | twardy limit 3 zdjęć, znak wodny, weryfikacja e-mail |
