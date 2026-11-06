# Lysias

Website met Griekse teksten van Lysias en Alpheios-hulp, in dezelfde opzet als
[Minerva](https://robmentingeidola.github.io/minerva/) en
[Livius](https://robmentingeidola.github.io/livius/).

- **index.html** — voorpagina
- **alpheios.html** — lijst met beschikbare teksten
- **teksten/** — de Alpheios-bestanden (HTML) plus `manifest.json`
- **assets/** — afbeeldingen

## Een tekst posten

1. Open de tekst in de **Alpheios Alignment Editor**.
2. Kies **Export → HTML** (het volledige, zelfstandige bestand van ±3 MB).
3. Bewaar het als `teksten/<korte-naam>.html`, bijvoorbeeld `teksten/eratosthenes-1-2.html`.
4. Zet het bestand in de map `teksten/` van deze repository (via de website van GitHub
   kan dat met *Add file → Upload files*).
5. Voeg een regel toe aan `teksten/manifest.json`:

   ```json
   {
     "teksten": [
       {
         "bestand": "eratosthenes-1-2.html",
         "titel": "Tegen Eratosthenes 1.2",
         "ondertitel": "Lysias 1",
         "regels": "§ 2"
       }
     ]
   }
   ```

   `bestand` is verplicht; `titel`, `ondertitel` en `regels` zijn optioneel.

De pagina werkt de lijst bij zodra de wijziging is gepubliceerd (meestal binnen
een minuut).

## Publiceren

GitHub Pages publiceert automatisch vanaf de branch `main`, map `/`.
De site staat op https://robmentingeidola.github.io/lysias/.
