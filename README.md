# Naarvan Riistamiehet ry — GitHubiin lisättävät tiedostot

Tässä kansiossa on yksi ainoa tiedosto, **index.html**, joka sisältää koko
sivuston (teksti + tyylit). Kuvat ja säännöt linkittyvät toistaiseksi suoraan
vanhalle nettisivut.fi-palvelimelle, joten mitään muuta ei tarvitse ladata —
sivu toimii heti kun tämä yksi tiedosto on GitHubissa.

## Näin saat sivun toimimaan (selaimen kautta, ei vaadi mitään asennuksia)

1. Mene osoitteeseen **github.com** ja kirjaudu sisään (tai luo tunnus, jos
   ei vielä ole).
2. Klikkaa oikeasta yläkulmasta **+** → **New repository**.
3. Anna nimeksi esim. `naarvanriistamiehet`, valitse **Public**, älä valitse
   mitään lisävalintoja (ei READMEa). Klikkaa **Create repository**.
4. Uuden, tyhjän repon sivulla klikkaa linkkiä **"uploading an existing
   file"**.
5. Raahaa tämän kansion **index.html**-tiedosto selaimeen (tai valitse se
   "choose your files" -painikkeesta).
6. Klikkaa alhaalta **Commit changes**.
7. Mene **Settings**-välilehdelle → vasemmalta **Pages**.
8. Kohdassa "Build and deployment" → **Source**: valitse **Deploy from a
   branch**. **Branch**: valitse **main**, kansio **/(root)**. Paina
   **Save**.
9. Odota 1–2 minuuttia. Sivu ilmestyy osoitteeseen:

   ```
   https://KAYTTAJATUNNUS.github.io/naarvanriistamiehet/
   ```

   (Näet tarkan osoitteen myös Pages-sivun yläreunassa, kun se on valmis.)

Tämä on täysin ilmainen eikä vaadi kuukausimaksuja.

### Vaihtoehto: git-komentorivillä

Jos käytät mieluummin komentoriviä vaiheiden 4–6 sijaan:

```
git init
git add index.html
git commit -m "Ensimmäinen versio kotisivuista"
git branch -M main
git remote add origin https://github.com/KAYTTAJATUNNUS/naarvanriistamiehet.git
git push -u origin main
```

## Sisällön muokkaaminen jatkossa

Kaikki teksti on `index.html`-tiedostossa. Voit muokata sitä suoraan
GitHubin selainmuokkaimella (avaa tiedosto repossa → kynäkuvake → muokkaa →
**Commit changes**) — sivu päivittyy automaattisesti parissa minuutissa.
Esim. uutisosio löytyy hakemalla tiedostosta `id="uutiset"`.

## Oma verkkotunnus (esim. naarvanriistamiehet.fi)

Ks. erilliset ohjeet, jotka annoin aiemmin (DNS-tietueet + Settings → Pages
→ Custom domain). Kysy uudelleen niin lähetän ne uudelleen tähän pakettiin.

## Kuvien ja PDF:ien siirtäminen omaan repoon myöhemmin (valinnainen)

Juuri nyt kuvat ja säännöt (PDF/ODT) haetaan suoraan vanhalta
nettisivut.fi-palvelimelta — sivu siis lakkaa näyttämästä niitä, jos vanha
Yhdistysavain-tili joskus suljetaan. Jos haluat täyden riippumattomuuden
vanhasta palvelusta, kerro niin teen tähän pakettiin myös `assets/`-kansion
ja latausskriptin, joilla kuvat ja tiedostot saa omaan repoon.
