# Řecko 2026 — instrukce pro Claude Code

Osobní projekt dvou lidí (Honza a Klárka). Plán cesty do Řecka jako **jedna statická
HTML stránka**. Na repu pracují dva lidé, každý ze svého počítače, oba přes Claude Code.

Komunikuj česky.

## `index.html` je zdroj — edituje se ručně

Stránka kdysi vznikala z generátoru (`build_v4.py`), který měla Klárka u sebe. **Ten
generátor se ztratil** (ležel ve scratchpadu Claude Code session, která se smazala) a
nikdo ho nemá. Ověřeno 22. 8. 2026.

Z toho plyne:

- **`index.html` je teď jediný zdroj pravdy.** Edituje se ručně, přímo v repu.
- Starší pravidlo „needituj index.html, přepíše to generátor" **už neplatí** a nikdo
  se jím neřiďte — blokovalo by to práci bez důvodu.
- Pokud by někdo generátor někdy znovu postavil, tohle pravidlo se musí přepsat zpátky.

Vedle repa existuje ještě `~/Desktop/WORK/General/recko-balkan-2026/itinerar.html` —
verze s fotkami, ze které se tiskne PDF. **Je zamrzlá k 10. 8. 2026 a od webu se
rozešla.** Změny v `index.html` se do ní samy nepromítnou.

## Co to je

- `index.html` je jedna samostatná stránka — žádné závislosti, žádný framework,
  styly inline v `<style>` v hlavičce.
- Hosting: GitHub Pages, větev `main`, kořen repa.
- Živá adresa: https://fenneczech.github.io/recko-2026/
- Každý push do `main` se sám nasadí, živé je to do ~1 minuty.

## Pravidlo číslo jedna: pull před editací, push hned po ní

Celý web je jeden soubor a upravují ho dva lidé. Když si někdo nechá rozdělanou změnu
přes noc, skoro jistě vznikne konflikt.

**Před každou editací:**

```
git pull --rebase
```

**Hned po dokončení editace:**

```
git add -A && git commit -m "popis zmeny" && git push
```

Nenechávej necommitnuté změny ležet. Krátké commity, často.

Když `git pull --rebase` skončí konfliktem: konflikt vyřeš tak, že **zachováš obě
změny** (typicky jde o různé sekce plánu), a pokud si nejsi jistý, co je správně,
zeptej se uživatele — nepřepisuj cizí text podle svého odhadu.

## Hranice

- **Neber si stránku k celkové přestavbě**, pokud o to uživatel výslovně nepožádá.
  Struktura sekcí je společná dohoda dvou lidí, ne tvoje designové rozhodnutí.
- **Neměň cizí text jen proto, že bys ho napsal líp.** Uprav to, o co tě požádali.
- Stránka je **mobile-first** — hlavní čtecí zařízení je telefon. Nerozbíjej to
  širokými tabulkami ani pevnými šířkami.
- Drž podporu světlého i tmavého režimu (`prefers-color-scheme`).

## Soukromí

URL je **veřejná a bez hesla**. Kdokoli, kdo ji zná, stránku otevře.

Na stránku nepatří:

- rezervační kódy a čísla rezervací s osobními údaji
- čísla dokladů, pasů, karet
- adresy bydliště, telefonní čísla

Itinerář, tipy, orientační ceny, názvy hotelů a odkazy jsou v pořádku.
