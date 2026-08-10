# Řecko 2026

Plán cesty jako jedna statická HTML stránka. Osobní projekt, nesouvisí s prací.

## Jak to funguje

- `index.html` je celý web (jeden soubor, žádný build, žádné závislosti).
- Hosting: GitHub Pages, deploy z větve `main`.
- Každý `git push` do `main` = do ~1 minuty je změna živá na URL.

## Publikace změny

```
git add -A && git commit -m "popis zmeny" && git push
```

## Poznámky

- Stránka je mobile-first — hlavní čtecí zařízení je telefon.
- Podporuje světlý i tmavý režim podle nastavení telefonu.
- URL je veřejná (neuhádnutelná, ale bez hesla). Nedávat sem čísla dokladů,
  rezervační kódy s osobními údaji, ani nic, co nemá být venku.
