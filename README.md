# Naarvan Riistamiehet ry — kotisivut

Yksinkertainen, täysin staattinen sivusto (ei tietokantaa, ei kuukausimaksuja).
Sopii hostattavaksi ilmaiseksi GitHub Pagesilla.

## 1. Lataa kuvat ja dokumentit talteen

Sivu käyttää kuvia ja PDF/ODT-tiedostoja, jotka ovat toistaiseksi vanhalla
nettisivut.fi/Yhdistysavain-palvelimella. Lataa ne omalle koneelle ennen
ensimmäistä committia:

```
chmod +x download-assets.sh
./download-assets.sh
```

Tämä täyttää kansiot `assets/images/` ja `assets/docs/`. Jos haluat käyttää
muita/parempia kuvia, korvaa tiedostot samoilla tiedostonimillä tai muokkaa
`index.html`:n kuvapolkuja.

## 2. Luo GitHub-repo ja julkaise sivu

1. Luo GitHub-tunnus, jos sinulla ei vielä ole (github.com).
2. Luo uusi **julkinen** repositorio, esim. nimellä `naarvanriistamiehet` (Ei
   READMEa/lisenssiä valittuna, koska ne on jo tässä kansiossa).
3. Aja tässä kansiossa (korvaa `KAYTTAJATUNNUS` omalla GitHub-tunnuksellasi):

   ```
   git init
   git add .
   git commit -m "Ensimmäinen versio kotisivuista"
   git branch -M main
   git remote add origin https://github.com/KAYTTAJATUNNUS/naarvanriistamiehet.git
   git push -u origin main
   ```

4. Mene repositorion **Settings → Pages**.
5. Kohdassa "Build and deployment" valitse **Source: Deploy from a branch**,
   Branch: **main**, kansio **/(root)**. Tallenna.
6. Odota pari minuuttia — sivu ilmestyy osoitteeseen:

   ```
   https://KAYTTAJATUNNUS.github.io/naarvanriistamiehet/
   ```

Tämä on täysin ilmainen, pysyvästi, eikä vaadi minkäänlaista ylläpitomaksua.

## 3. (Valinnainen) Oma verkkotunnus

Jos haluat esim. `naarvanriistamiehet.fi` github.io-osoitteen sijaan:

1. Osta verkkotunnus haluamaltasi rekisteröijältä (esim. Louhi.net, Zoner,
   tai muu .fi-verkkotunnuksia myyvä palvelu). Hinta on tyypillisesti
   n. 10–15 €/vuosi.
2. Lisää verkkotunnuksen DNS-asetuksiin CNAME-tietue, joka osoittaa
   osoitteeseen `KAYTTAJATUNNUS.github.io`.
3. Lisää sama verkkotunnus repositorion **Settings → Pages → Custom domain**
   -kenttään.

## Sisällön päivittäminen jatkossa

Kaikki sisältö on yhdessä `index.html`-tiedostossa. Tekstien, tapahtumien ja
uutisten muokkaaminen onnistuu millä tahansa tekstieditorilla — etsi oikea
kohta tiedostosta (esim. `id="uutiset"`), muokkaa ja tee uusi commit + push.
Sivu päivittyy automaattisesti parissa minuutissa.

Uuden kuvan lisääminen galleriaan: kopioi kuvatiedosto kansioon
`assets/images/`, ja lisää `index.html`:n `id="kuvia"`-osioon uusi rivi
kuvan tiedostonimellä.

## Kansiorakenne

```
index.html              Koko sivu (yksi tiedosto: HTML + CSS)
assets/images/           Kuvat (galleria + etusivun taustakuva)
assets/docs/              Säännöt ja metsästyssäännöt (PDF/ODT)
download-assets.sh       Skripti vanhan sivun kuvien/dokumenttien lataamiseen
```
