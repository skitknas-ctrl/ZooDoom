# ZooDoom

Ett pusselspel som blandar klassiska **Zookeeper**-matcha-tre-mekaniken med dagens
"rädda kungen"-spel: ett flöde av sten eller vatten pressar på mot en figur i knipa,
och den enda vägen undan är genom brädet du spelar på.

## Spelidé

- Högst upp hänger en vinstklocka (som på börsen). Den ringer och pengar – mynt och
  sedlar – regnar ner i en vattenbassäng.
- I en grotta ovanför bassängen står en inburad arbetare och pumpar vatten ur sin
  fängelsehåla; vattnet forsar ut genom ett rör i sidan av spelet.
- Mynten samlas på hög på bassängens botten och trycker upp vattennivån. När vattnet
  når arbetarens haka släpper han pumpen och trampar vatten; når det cellens tak
  drunknar han och spelet är förlorat.
- Under bassängen ligger en Zookeeper-liknande spelplan (10×8) med färgade stenblock.
  Bassängens golv täcker vänstra halvan, så vattnet kommer bara in via högra halvans
  överkant. Under högra halvan finns ett golv och en halvvägg går upp till mitten,
  så vattnet måste fylla högra halvan, rinna över väggen och ut genom vänstra halvans
  botten.
- Spelaren byter plats på två intilliggande block för att få tre eller fler i rad.
  Matchade block försvinner för gott och tomrummen blir kanaler för vattnet.
- Vänstra halvan är låst (grå) tills högra halvan är rensad till en inställbar
  procent.
- Under spelplanen ligger ett lyxigt kontor där Krösus sitter vid sitt skrivbord
  med myntstaplar. Banan är vunnen när tillräckligt många liter runnit ner i kontoret.

## Hjälpmedel och inställningar

- Hammare (tar bort ett block), bomb (3×3) och blanda om.
- Kugghjulet: procentkrav för upplåsning, myntregnets takt, inläckage, pumpens
  kapacitet, mål i liter, stigande svårighet och om block får skjutas in i tomrum.

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
