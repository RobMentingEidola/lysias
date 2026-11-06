# Lysias

Website met Griekse teksten van Lysias en Alpheios-hulp, in dezelfde opzet als
[Minerva](https://robmentingeidola.github.io/minerva/) en
[Livius](https://robmentingeidola.github.io/livius/).

- **index.html** — voorpagina
- **alpheios.html** — lijst met beschikbare teksten (wordt automatisch gevuld)
- **teksten/** — hier komen de Alpheios-bestanden
- **assets/** — afbeeldingen

## Een tekst posten

1. Open de tekst in de **Alpheios Alignment Editor**.
2. Kies **Export → HTML** (het volledige, zelfstandige bestand van ±3 MB).
3. Noem het bestand kort en zonder spaties, bijvoorbeeld `eratosthenes-1-2.html`.
4. Ga in deze repository naar de map `teksten/` en kies **Add file → Upload files**.
   Sleep het bestand erin en klik op **Commit changes**.

Klaar. De pagina zet het bestand er binnen ongeveer een minuut automatisch bij,
met de bestandsnaam als titel. Wil je een nette titel, ondertitel of regelnummer
in plaats van de bestandsnaam, voeg dan een regel toe aan `teksten/manifest.json`:

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

Alleen `bestand` is verplicht; de rest is optioneel. Bestanden zonder
manifest-regel verschijnen gewoon met een titel die van de bestandsnaam is
gemaakt.

## Publiceren

GitHub Pages publiceert automatisch vanaf de branch `main`, map `/`.
De site staat op https://robmentingeidola.github.io/lysias/.
