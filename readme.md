# 2web_mm_voz — materiály na hodiny webu (teen‑friendly)

V tomto repozitári nájdeš všetko, čo budeme používať na webových hodinách: osnovu, úlohy a kopu starterov (hotové kostry HTML/CSS), z ktorých môžeš rovno stavať.

## Čo tu je
- `kurikulum-html-css.md` — čo sa učíme počas roka (10 mesiacov)
- `ulohy-html-css.md` — databáza úloh (každý mesiac 5 mini + 5 väčších)
- `starters/` — očíslované priečinky 01–10 podľa mesiacov s mini projektmi
	- `base/` — spoločné štýly a vzorová stránka (skip link, landmarky, utility)
	- `01-september/ … 10-jun/` — konkrétne startery ku cvičeniam
- `zdroje-design-to-code.md` — kde nájdeš hotové dizajny (PNG/Figma) a style guide-y

## Ako začať (rýchlo)
1) Vyber si mesiac a starter, napr. `starters/02-oktober/landmarks-template/`.
2) Otvor `index.html` (ideálne cez Live Server, aby sa zmeny hneď zobrazovali).
3) Upravuj HTML a CSS. Lokálne štýly už importujú `../../base/styles.css`.

Tip: Neprepíš originál. Duplikuj priečinok starteru a pomenuj si ho, napr. `landmarks-template-jan-novak`.

### Spustenie (2 možnosti)
- VS Code Live Server: klikni pravým na `index.html` → „Open with Live Server“.
- Alebo cez terminál (voliteľne):

```bash
# v koreňovom priečinku starteru
python3 -m http.server 5500
# otvor v prehliadači: http://localhost:5500
```

## Ako budeme pracovať s úlohami
- Každá úloha má v `ulohy-html-css.md` Zameranie, Zadanie, Postup, Očakávaný výstup a Checklist.
- K väčšine úloh existuje vhodný starter. Použi ho a doplň obsah/štýl podľa zadania.
- Odovzdanie: učiteľ povie presný spôsob (napr. zip, classroom, branch). Kým nie, duplikuj starter a ulož do repozitára pod jasným názvom.

## Pravidlá pomenovania a poriadok
- malými písmenami, bez medzier → `moj-projekt`, nie `Moj Projekt`.
- jasné názvy súborov → `index.html`, `styles.css`, `img/hero.jpg`.
- žiadne obrovské obrázky (optimalizuj veľkosti, použite `srcset/picture` v pokročilejších mesiacoch).

## Mini „Definition of Done“ (pred odovzdaním)
- HTML:
	- máš landmarky (`header`, `nav`, `main`, `footer`), jeden `h1`, logickú hierarchiu nadpisov
	- odkazy majú zmysluplný text (nie „klikni sem“)
	- obrázky majú `alt`
- CSS:
	- mobile‑first, nič nepretečie horizontálne
	- viditeľný `:focus-visible` pre odkazy/tlačidlá, kontrast čitateľný
	- používaš premenné (aspoň farby), medzery konzistentné
- Obsah:
	- texty dávajú zmysel, nič nie je placeholder typu „Lorem ipsum“ (ak zadanie nehovorí inak)

## Keď sa zasekneš
1) Skontroluj konzolu (Errors v DevTools).
2) Vráť sa k zadaniu a checklistu v `ulohy-html-css.md`.
3) Porovnaj s `starters/base/index.html` a `base/styles.css` (či niečo nechýba).
4) Skús minimal repro: dočasne vyhoď všetko, nechaj len problémovú časť.
5) Požiadaj o pomoc: popíš krok, ktorý zlyháva, a čo si už skúšal(a).

## Nástroje, ktoré používame
- VS Code + Live Server (okamžitý náhľad)
- Prehliadač DevTools (Elements, Styles, Accessibility, Lighthouse)
- Google Fonts, Heroicons/RemixIcon (podľa zadania)

## FAQ
- „Nezobrazuje sa mi CSS.“ → Skontroluj cestu k súboru, alebo či máš `@import "../../base/styles.css";` v `styles.css`.
- „Prečo nevidím skip link?“ → Je viditeľný pri fokuse. Stlač TAB hneď po načítaní stránky.
- „Ako tablet layout, keď dizajn dal len mobil/desktop?“ → medzi nimi pridaj breakpoint a dodrž hierarchiu veľkostí/medzier.

---

Chceš bonus výzvy priamo s dizajnom (PNG/Figma + style guide)? Pozri `zdroje-design-to-code.md` a vyber si challenge. 😉
