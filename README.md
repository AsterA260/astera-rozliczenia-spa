# AsterA · Rozliczenia SPA (Thai Maliwan)

Narzędzie do rozliczeń dobowych i rentowności dwóch SPA: **Zwierzyniecka** i **Szewska**.
Jeden samowystarczalny plik `index.html` — bez instalacji, bez serwera, bez zewnętrznych bibliotek.

---

## Co potrafi

**Koła dobowe (2 SPA)** — każdy dzień miesiąca to węzeł na tarczy. Klikasz dzień, otwiera się rozliczenie:

- skany z Bookiera (Rzut 1 — rezerwacje/specyfikacja, Rzut 2 — zestawienie),
- lista transakcji: godzina · klient · metoda · kwota,
- 12 metod płatności (jak w Bookierze, bez Groupona, plus *Inne / napiwki*),
- sumy metod — wpisywane ręcznie albo przeliczane z transakcji,
- **raport dobowy**, **bony sprzedane**, kasetka, uwagi,
- **Różnica = (Obrót usług + Bony sprzedane) − Raport dobowy** → gdy 0, wszystko się spina.

**Rentowność (koła miesięcy)** — pełny P&L per SPA:

- koszty stałe: pracownicy (ze składowymi wynagrodzenia), ZUS/PIT/CIT/VAT/księgowy, tel/prąd/gaz, lokale,
- koszty zmienne (QMS, proszki, inne),
- przychód zaciągany automatycznie z kół dobowych (z możliwością korekty),
- próg rentowności, średnia cena masażu, prognoza końca miesiąca, porównanie do poprzedniego miesiąca.

**Narzędzia (ikony u góry)**

| Ikona | Funkcja |
|---|---|
| ✏️ | edycja nazw SPA |
| 🤖 | Agent — wypełnianie dnia z 2 zrzutów Bookiera (JSON) |
| 🛰️ | Kopilot — meldunki: ETA do rentowności, spadek średniej ceny, niezgodności, dni bez rozliczenia |
| Σ | podsumowanie miesiąca |
| 🏦 | weryfikacja konta (Planeta Pay / PayU / przelewy) |
| 💾 | kopia zapasowa i przywracanie |
| 🇵🇱 / 🇹🇭 | język: polski / tajski |

Dodatkowo: 🌌 galaktyka roku (klik w miesiąc na wyświetlaczu) i **Ogród Maliwan** — kwiat za każde 10 minut pracy.

---

## ⚠️ Gdzie są dane (przeczytaj, zanim zmienisz adres!)

Dane zapisują się **w przeglądarce**, osobno **dla każdego adresu**.
Wersja z pliku (`file:///…`) i wersja z linku (`https://…`) to dla przeglądarki **dwa różne miejsca** — dane **nie przeniosą się same**.

**Przy przejściu na link zrób tak:**

1. W starej wersji: **💾 → Zrób kopię zapasową** (pobierze plik `kopia_rozliczenia_RRRR-MM-DD.json`).
2. Otwórz nowy link.
3. **💾 → Przywróć z pliku** → wskaż tę kopię. Wszystko wraca.

**Rób kopię regularnie** (np. przy zamknięciu miesiąca). Wyczyszczenie danych przeglądarki = utrata rozliczeń.
Kopie zapasowe zawierają dane klientów — **trzymaj je poza repo** (są w `.gitignore`).

---

## Uruchomienie

Otwórz `index.html` w przeglądarce. To wszystko.

## Wdrożenie (link dla Maliwan)

Repo jest prywatne. Link publikujemy przez darmowy hosting statyczny (np. Netlify), który potrafi budować z prywatnego repo.
Każdy `git push` = automatyczna aktualizacja linku.

---

*Narzędzie pomocnicze — nie zastępuje kasy fiskalnej ani ewidencji księgowej. Służy do kontroli i porównania z raportem dobowym.*
