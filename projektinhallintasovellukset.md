# Projektinhallintasovellukset

Projektin läpinäkyvyys eri sidosryhmille voi kasvattaa luottamusta toimittajaan. Jos asiakkaalle tarjotaan pääsy projektinhallintasovellukseen, hänen on helpompi halutessaan ottaa enemmän vastuuta. Voi tietysti olla, ettei asiakas välttämättä käytä tätä mahdollisuutta. Sovellus ei korvaa muita kommunikointitapoja vaan lähinnä pyrkii helpottamaan tilanteen seuraamista asiakkaana. 

Käyttäjätarinat voidaan tarvittaessa pilkkoa pienempiin osiin, tehtäviksi. Tämä kannattaa erityisesti silloin jos käyttäjätarina on laaja. Teoriassahan hyvät käyttäjätarinat eivät ole tällaisia, mutta poikkeuksia tulee aina. Tärkeää on pohtia, minkälaisiin osiin tehtävät jakaa. Esimerkiksi tehtävän pilkkominen teknisiin toteutuksiin helpottaa varsinkin teknologian suhteen kokematonta ohjelmoijaa:

**Käyttäjätarina**: Käyttäjä voi lisätä muistiinpanon.
Jaetaan tämä alitehtäviksi:

- Toteuta tietokantataulu "note"
- Toteuta tallennusrajapinta "NoteService"
- Tee käyttöliittymä.

Näin tarkka jako voi kuitenkin usein olla täysin turhaa kokeneelle toteuttajalle. Pienille osille on kuitenkin helpompi antaa työmääräarvio. Huomaa taas, että valitse käytännöt tilanteen mukaan (ja käytännöt voi muuttaa myöhemmin paremmiksi).

Hyvä nyrkkisääntö on, että jos asian toteuttaa yhtä nopeasti kuin kirjaa, niin ei ehkä kannata lisätä sitä järjestelmään yksittäisenä tehtävänä vaan toteuttaa samantien. Mikromanagerointi voi nopeasti käydä työlääksi. Muista, että järjestelmän _on tarkoitus helpottaa työtä_, ei olla itse työ.

Erilaisia sovelluksia löytyy useita, mutta tässä pari ketteriin projekteihin sopivaa:

- [Jira (GreenHopper-lisäosalla)](http://www.atlassian.com/software/greenhopper/overview)
- [Agilefant](http://www.agilefant.org).