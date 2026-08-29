# Læringsti: Hvorfor svinger bestandene i den boreale skogen?

Dette prosjektet er en interaktiv læringssti om bestandssvingninger hos smågnagere og skogsfugl i den boreale skogen i Fennoskandia.

Læringsstien tar for seg blant annet:

- den alternative byttedyrhypotesen (APH)
- predasjon og ovenfra-og-ned-regulering
- blåbær, plantekvalitet og nedenfra-og-opp-regulering
- klima, temperatur og snøforhold
- tidsforsinkelser og synkrone bestandssvingninger
- forskningsfigurer og refleksjonsoppgaver

## Mappestruktur

Prosjektet kan organiseres slik:

```text
prosjekt/
├── index.html
├── README.md
├── .nojekyll
└── images/
    ├── art_tiur.png
    ├── art_roy.png
    ├── art_orrhane.png
    ├── art_orrhone.png
    ├── art_rype.png
    ├── art_rodrev.png
    ├── art_mar.png
    ├── art_rugde.png
    ├── modul1_ims2013_fig2.png
    ├── modul1_selas2006_fig1.png
    ├── modul1_wegge2022_fig1.png
    ├── modul2_selas2000_fig4.png
    ├── modul2_selas2021_fig2.png
    ├── modul3_selas2011_fig1.png
    └── modul3_hjeljord_loe2022_fig1.png
```

Det kan finnes flere bilder i `images/` enn de som er vist i eksemplet.

## Viktig om bilder

HTML-filen bruker relative bildestier, for eksempel:

```html
<img src="images/art_tiur.png">
```

Derfor må mappen `images` ligge på samme nivå som `index.html`, og filnavnene må stemme nøyaktig.

På GitHub og andre Linux-baserte servere skilles det mellom store og små bokstaver. For eksempel er:

```text
art_tiur.png
```

og

```text
Art_Tiur.png
```

to forskjellige filnavn.

## De 7 nøkkelfigurene

Læringsstien bruker sju obligatoriske forskningsfigurer:

### Modul 1 – predasjon / APH

1. `modul1_ims2013_fig2.png`
2. `modul1_selas2006_fig1.png`
3. `modul1_wegge2022_fig1.png`

### Modul 2 – blåbær / plantekvalitet

4. `modul2_selas2000_fig4.png`
5. `modul2_selas2021_fig2.png`

### Modul 3 – klima / syntese

6. `modul3_selas2011_fig1.png`
7. `modul3_hjeljord_loe2022_fig1.png`

Hvis en figur skal byttes ut, kan den nye PNG-filen få nøyaktig samme filnavn. Da trenger ikke HTML-koden å endres.

## Hva er `.nojekyll`?

`.nojekyll` er en tom fil som kan ligge i rotmappen til prosjektet.

Den forteller GitHub Pages at nettstedet skal publiseres som vanlige statiske filer uten behandling med Jekyll.

Filstrukturen blir for eksempel:

```text
index.html
README.md
.nojekyll
images/
```

`.nojekyll` trenger ikke inneholde noe.

## Åpne siden lokalt

Du kan åpne `index.html` direkte i en nettleser.

For full testing er det ofte bedre å bruke en lokal webserver, særlig dersom prosjektet senere får funksjoner som krever at siden kjøres via HTTP.

Eksempel med Python:

```bash
python -m http.server 8000
```

Åpne deretter:

```text
http://localhost:8000
```

## Publisering med GitHub Pages

En enkel måte å publisere læringsstien på er:

1. Opprett et GitHub-repository.
2. Last opp `index.html`.
3. Last opp hele `images/`-mappen.
4. Legg til den tomme `.nojekyll`-filen.
5. Åpne repositoryets **Settings**.
6. Gå til **Pages**.
7. Velg publisering fra ønsket branch, vanligvis `main`.
8. Velg rotmappen `/ (root)`.
9. Lagre innstillingene.

Når GitHub Pages er aktivert, vil `index.html` fungere som startsiden.

## Før publisering

Kontroller spesielt:

- at `index.html` ligger i rotmappen
- at `images/` er lastet opp
- at alle bildefilnavn er riktige
- at store og små bokstaver i filnavn stemmer
- at ingen bilder fortsatt bruker lokale filstier fra egen datamaskin
- at siden fungerer på både mobil og datamaskin
- at alle kildehenvisninger og fotokrediteringer er med

## Innhold og kilder

Læringsstien bygger på forskningsstudier om blant annet smågnagere, skogsfugl, predasjon, blåbær og klima.

Kildehenvisninger og DOI-lenker finnes i selve læringsstien.

## Lisens og bilder

Kontroller at du har nødvendig tillatelse til å publisere fotografier, omtegnede forskningsfigurer og annet materiale før nettstedet gjøres offentlig tilgjengelig.

Fotokrediteringer bør beholdes sammen med bildene.
