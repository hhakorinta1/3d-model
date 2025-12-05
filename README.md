# 3D-mallit – Kaksi riippuvaista dropdownia (GitHub Pages)

Tämä paketti sisältää **index.html**-sivun, jossa on **kategoria**- ja **malli**-dropdownit. Toisen dropdownin vaihtoehdot päivittyvät valitun kategorian mukaan, ja valinta vaihtaa `<model-viewer>`-komponentin `src`-polun.

## Rakenne
```
/ (root)
├─ index.html
├─ README.md
└─ models/            # lisää .glb-tiedostosi tänne (esim. talo_a.glb)
```

## Käyttöohjeet
1. Vie SketchUp-mallit **GLB**-muotoon.
2. Lataa `.glb`-tiedostot **models/**-kansioon (GitHubiin).
3. Avaa `index.html` ja päivitä **catalog**-objektiin kategoriat, näyttönimet ja polut, esim. `"models/talo_a.glb"`.
4. Julkaise GitHub Pagesissa:
   - Repo → **Settings → Pages** → Source: **Branch: main**, Folder: **root**.
   - Julkaistu URL on muotoa `https://USERNAME.github.io/REPO-NAME/`.

## Nuclino-upotus (responsiivinen)
Kopioi artikkeliin tämä koodi ja korvaa URL omallasi:
```html
<div style="position:relative; padding-bottom:75%; height:0; overflow:hidden;">
  <iframe src="https://USERNAME.github.io/REPO-NAME/"
          style="position:absolute; top:0; left:0; width:100%; height:100%; border:0;"
          allowfullscreen>
  </iframe>
</div>
```

## Vinkit
- Älä käytä Google Drivea `.glb`-lähteenä (CORS). Hostaa mallit samassa GitHub Pages -repossa.
- Polkujen tulee olla **suhteellisia** (esim. `models/talo_a.glb`).
- Jos näkymä on tyhjä, avaa selaimen kehittäjäkonsoli (F12) ja tarkista virheet (väärä polku tms.).
- Voit lisätä esikatselukuvan: `poster="polku/posteri.jpg"` `<model-viewer>`-elementtiin.
```

# Bonus: Lisää tyhjä tiedosto models/.gitkeep, jotta kansio näkyy repossa.
