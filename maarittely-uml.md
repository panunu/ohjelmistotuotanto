# Ohjelmistojen määrittely, mallintaminen ja dokumentointi

- Minkälaisia speksejä
- Esimerkkejä?
- Kokemuksia
- Kokemusten perusteella hyväksi todetut määrittelytavat
-- wireframet
-- sanasto
-- business-logiikka
-- ei yhtä oikeata totuutta
-- ei lukkoonlyötyä (huom. iteratiivisuus)
-- kommunikointi
- Traditionaalinen: iso organisaatio, iso projekti, vesiputousmalli
- Tulevaisuuden trendi: pienet organisaatiot, fokusoidut projektit, iteratiivisuus, haukataan pienempiä palasia
- Eksaktin määrittelyn tarve vähenee
- Dokumentaation ylläpito
- Erilaiset mallintamisen menetelmät
- Miksi/milloin mallintaa, erilaiset yritykset/organisaatiorakenteet

## Määrittely

Määrittelyssä lähdetään liikkeelle *asiakasvaatimusten selvittämisellä*. Kysymys kuuluukin: mitä asiakas tarvitsee? Ja tylsäähän se olisi, jos asiakas osaisi vastata tähän kysymykseen täydellisesti. Jokainen asiakas on erilainen.

> "In dealing with customers, you must understand that there are things they *want* and things they *need*." - Larry Bernstein

Täytyy muistaa, että määrittely on jatkuvaa ja orgaanista. Ideoita tulee ja menee projektin edetessä. On tärkeää, että oleelliset toiminnallisuudet saavat enemmän huomiota kuin satunnaiset päähänpistot. Tämän takia auttaa, jos *myös kehitystiimi ymmärtää asiakkaan liiketoimintaa*, jolloin heillä on mahdollisuus hahmottaa, mitä perimmäistä ongelmaa asiakkaan esittämällä vaatimuksella yritetään ratkaista. Jos ymmärretään ongelma, voidaan esittää siihen myös vaihtoehtoisia ratkaisuja (esim. ei toteuteta). [MoSCoW-metodia](http://en.wikipedia.org/wiki/MoSCoW_Method) ja vastaavia kysymyksiä voi käyttää apuna vaatimusten prioriteettien selvittämisessä. Yritä saada asiakas ymmärtämään, että vaatimukset, ehdotukset ja muutokset maksavat. Tämä auttaa välttymään ns. [feature creepiltä](http://en.wikipedia.org/wiki/Feature_creep).

http://www.cs.tut.fi/~otm/harjoitukset/tupa-maarittelydokumentti.pdf

## UML

UML, Unified Modeling Language, on _visuaalinen_ kieli, jota käytetään järjestelmien määrittelyyn, suunnitteluun ja dokumentointiin. UML on yleisesti tunnettu kuvausmenetelmä, jolla visualisoidaan pääasiassa oliopohjaisia järjestelmiä. UML:n perimmäinen tarkoitus on auttaa ymmärtämään järjestelmää pääosin teknisestä näkökulmasta. Yhtenäisen, standardoidun kielen tarkoitus on ohjata yksiselitteisyyteen, eli UML:ää osaavien pitäisi ymmärtää kuvatut asiat samalla tavalla. 

UML:n tarkoitukseksi yleensä luonnetaan dokumentointi jälkikäteen tai suunnittelu etukäteen (jonka toteuttamisen voi ulkoistaa). Mutta sen sijaan, että joku toinen UML-suunnittelija piirtää kiveenhakatut "ohjeet" ja antaa ne ohjelmoijalle orjallisesti toteutettavaksi, kehittäjät voivat käyttää sitä itse hyödyksi. UML-kaavioita voi käyttää alustavien ideoiden hahmotteluun (jopa nopeammin kuin koodaamalla ja kokeilemalla) ja näin ehkä ohjata järjestelmää rakenteellisesti parempaan suuntaan.

UML voi olla osa dokumentaatiota. Järjestelmän muuttuessa dokumentaatiota pitää päivittää, tai muuten se vanhenee nopeasti, jonka jälkeen sen tuoma hyöty katoaa. Pahimmillaan vanhentunut dokumentaatio voi aiheuttaa väärinymmärryksiä ja turhaa työtä. Jos siis UML:llä kuvataan järjestelmän osia tai prosesseja (joskus hyvinkin spesifisesti) niin kaaviot on myös päivitettävä muutosten yhteydessä. Ja tämähän taas vaatii työtä. Kannattaakin harkita, kuinka tarkasti päättää järjestelmän osia mallintaa. Huomaa, että sama pätee dokumentaation myös yleisellä tasolla.

### Käyttötapaus ja käyttötapauskaavio (Use Case)

Käyttötapauskaavion perustana toimii *käyttötapauskuvaus*. Käyttötapauskuvauksessa avataan toiminnallisuus sanallisesti. Käyttötapaukset ovatkin siis enemmän kirjoittamista, kuin kaavioiden avulla mallintamista. Käyttötapauskuvausten voisi sanoa olevan hyvin tarkasti kirjoitettuja käyttäjätarinoita (user story).

Käyttötapausten kirjoittamisen avuksi on määritelty tietty rakenne, jossa kerrotaan esim. sidosryhmät ja lähtötilanne. Esimerkki tässä !!!!!
Esimerkkejä varsinaisista kaaviosta voi katsella esim. [tästä](http://www.uml-diagrams.org/use-case-diagrams-examples.html).

### Luokkakaavio (Class)

Luokkakaavio kuvaa oliopohjaisen järjestelmän luokkarakenteen määrittely/suunnittelutasolla. Esimerkiksi luokan metodit voidaan ilmaista pseudokoodilla ilman konkreettisia tyypityksiä. Luokkakaaviossa keskitytään rakenteen mallintamiseen yleisellä tasolla, josta selviää esim. seuraavat: 

- rajapinnat, perintä, kompositio ja muut vastaavat yhteydet
- attribuutit ja metodit
- nimeäminen.

### Sekvenssikaavio (Sequence)

Sekvenssikaavio muodostaa yhdessä luokkakaavion kanssa yleisen tavan mallintaa olio-ohjelmia. Sekvenssikaaviolla mallinnetaan olioiden interaktioita viestien avulla, eli minkälaisia reaktioketjuja tietyt tapahtumat aiheuttavat. Käytännössä kaaviosta selviää, mitä muita metodeja jokin tietty metodi saattaa kutsua ja minkälaista tietoa näiden välillä liikkuu.
Tämä myös auttaa hahmottamaan riippuvuuksia eri luokkien välillä.

### Tilakaavio (State) ?

Tilakaaviota käytetään olion tai järjestelmän elinkaaren mallintamiseen. Tilakaaviossa kuvataan seuraavat asiat:

- Olion alkutila
- Olion tilamuutokset (jotka johtuvat ulkoisista tapahtumista).
