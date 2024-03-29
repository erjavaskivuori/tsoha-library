## Kirjasto / Library

[Link to the app](https://tsoha-library-8f8482201604.herokuapp.com/)

App only in Finnish for now.

Tietokantasovellukseni on luotu kirjaston käyttämiseen ja hallintaan.

Sovelluksella on seuraavat toiminallisuudet:

Kuka tahansa sivulla voi:
- Nähdä kaikki kirjastossa olevat kirjat
- Nähdä kirjan oman sivun, jossa on tarkempia tietoja kirjasta sekä sille annetut arvostelut
- Hakea kirjoja teoksen nimen, kirjailijan, kategorian tai julkaisuvuoden perusteella
- Luoda uuden tunnuksen

Käyttäjä voi:
- Kirjautua sisään ja ulos
- Lainata ja palauttaa kirjoja
- Antaa arvosteluja kirjoille
- Toivoa uusia kirjoja
- Katsella oman profiilin kautta omia lainauksia
- Poistaa oman käyttäjän, jolloin poistuu myös käyttäjän antamat arvostelut, lainaukset ja kirjatoiveet

Kirjaston työntekijä voi:
- Antaa arvosteluja kirjoille
- Lisätä ja poistaa kirjoja
- Nähdä kirjatoiveet ja toiveen esittäjän käyttäjänimen
- Nähdä lainassa olevat kirjat ja lainaajan käyttäjänimen
- Poistaa oman käyttäjän, jolloin poistuu myös käyttäjän antamat arvostelut


### Sovellusta voi testata seuraavien ohjeiden avulla:

1. Kloonaa repositorio

2. Luo hakemistoon .env-tiedosto, johon lisäät seuraavat muuttujat:
```
DATABASE_URL=postgresql:///user     # user tilalle oma psql-käyttäjänimi
SECRET_KEY=                         # luo oma secret key
```

3. Luo `schema.sql` mukaiset taulut komennolla:
```
psql < schema.sql
```

4. Asenna vaadittavat riippuvuudet komennolla:
```
pip install -r requirements.txt
```

5. Luo hakemistoon virtuaaliympäristö komennolla:
```
python3 -m venv venv
```

6. Aktivoi virtuaaliympäristö komennolla:
```
source venv/bin/activate
```

7. Käynnistä sovellus komennolla:
```
flask run
```
