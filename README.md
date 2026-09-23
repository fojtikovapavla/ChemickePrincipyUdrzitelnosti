# Chemie ekosystémů — slide decky

Slide decky k přednáškám a seminářům kurzu *Chemické principy a udržitelnost*
(Sustainability Management, 1. ročník). Postavené jako statické HTML stránky
na [reveal.js](https://revealjs.com/) — žádný server ani sestavovací krok není
potřeba, stačí soubory nahrát na GitHub Pages (nebo otevřít lokálně).

## Struktura

```
index.html          rozcestník na všechny decky
prednaska-1.html     Blok 1 · Přednáška — Abiotické složky ekosystému
seminar-1.html        Blok 1 · Seminář — Abiotika v praxi
assets/css/theme.css  sdílený vzhled všech decků (barvy, typografie, komponenty)
```

Bloky 2–4 zatím nejsou rozpracované — na `index.html` jsou vidět jako
přehled plánovaných témat.

## Jak nahrát na GitHub Pages

1. Vytvořte na GitHubu nové repo (např. `chemie-ekosystemu`) a nahrajte do
   něj obsah této složky (přes web rozhraní „Add file → Upload files", nebo
   příkazovou řádkou):

   ```bash
   git init
   git add .
   git commit -m "Slide decky — blok 1"
   git branch -M main
   git remote add origin https://github.com/<váš-účet>/chemie-ekosystemu.git
   git push -u origin main
   ```

2. V repozitáři přejděte do **Settings → Pages**, u „Source" vyberte větev
   `main` a složku `/ (root)`, uložte.

3. Za pár desítek sekund bude web dostupný na
   `https://<váš-účet>.github.io/chemie-ekosystemu/`.

## Ovládání decku

- **Šipky / kliknutí / mezerník** — další/předchozí slide.
- **Klávesa `S`** — otevře samostatné okno s poznámkami pro přednášejícího
  (časování, doporučená facilitace, mylné představy studentů). Toto okno
  vidíte jen vy — promítané okno zůstává čisté, bez zamykání či PINu.
  Poznámky nejsou nikde skryté v běžném zobrazení stránky, jen v tomto
  odděleném okně řečníka.
- **Klávesa `F`** — fullscreen.
- U kvízových slidů v semináři (`seminar-1.html`) se možnosti odpovědí a
  vysvětlení objevují postupně kliknutím/šipkou (tzv. *fragments*) — funguje
  to jako klasické odkrývání odpovědí na promítání.

## Přidání dalšího bloku

Až budete mít obsah bloku 2, zkopírujte `prednaska-1.html` jako
`prednaska-2.html` (a obdobně pro seminář), nahraďte obsah `<section>` bloky
novým obsahem a přidejte odkaz do `index.html`. Vzhled (`assets/css/theme.css`)
zůstává společný pro všechny decky.

## Úprava vzhledu

Barvy, typografie a rozměry komponent (schémata, grafy, kvízy, karty úkolů)
jsou v `assets/css/theme.css` v proměnných na začátku souboru (`:root { ... }`)
— stačí změnit hodnotu tam a projeví se ve všech deckách najednou.
