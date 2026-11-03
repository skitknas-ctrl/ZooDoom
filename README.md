# ZooDoom

Ett pusselspel som blandar klassiska **Zookeeper**-matcha-tre-mekaniken med dagens
"rädda kungen"-spel: ett flöde av sten eller vatten pressar på mot en figur i knipa,
och den enda vägen undan är genom brädet du spelar på.

## Spelidé

- Högst upp står en kung, riddare eller prinsessa i en kammare. Sten (eller vatten,
  lava, sand …) väller in och kommer att krossa/dränka figuren om flödet inte får
  rinna undan.
- Under kammaren ligger ett Zookeeper-liknande bräde fullt av djurbrickor.
- Spelaren byter plats på två intilliggande brickor för att skapa rader om tre eller
  fler likadana djur. Matchade brickor försvinner och lämnar tomrum.
- Tomrummen bildar kanaler. Flödet söker sig nedåt/sidledes genom varje öppning det
  hittar – precis som fallande sand – och rinner ut i botten.
- Banan är klarad när tillräckligt mycket av flödet runnit undan utan att nå figuren.
  Misslyckas spelaren fylls kammaren och figuren går under.

## Spelmekanik (planerad)

- Fysik för flödet: enkel cellautomat ("falling sand") som uppdateras varje tick.
- Brädet: rutnät (t.ex. 8×8) med 6–7 djursorter, kaskadfall efter varje match.
- Hinder: stenblock, låsta brickor och is som kräver flera matchningar.
- Hjälpmedel: bomb, radsprängare och "dränering" som öppnar en hel kolumn.
- Svårighetsgrad: hur snabbt flödet rinner, hur många drag/sekunder spelaren har och
  hur långt det är från kammaren till utloppet.
- Banor: slumpgenererade utifrån regler, med stigande svårighet.

## Teknik

Spelet är skrivet i HTML5/Canvas (`index.html`, inga beroenden) och körs antingen
direkt i webbläsaren eller inuti en tunn Android-app (WebView) som byggs av
GitHub Actions. Inga annonser, ingen spårning, ingen nätverksåtkomst.

- Webbversion: aktivera GitHub Pages för grenen `main` → `https://skitknas-ctrl.github.io/zoodoom/`
- Android: GitHub Actions bygger en test-APK vid varje push till `main` och publicerar
  den som utgåvan `0.1.0-test.<byggnummer>`. Senaste bygget finns alltid här:

      https://github.com/skitknas-ctrl/ZooDoom/releases/latest/download/zoodoom-debug.apk

  Med Obtainium: lägg till `https://github.com/skitknas-ctrl/ZooDoom`, inga extra inställningar behövs.

## Licens

Beslutas innan första release (troligen MIT eller GPL-3.0 för F-Droid).
