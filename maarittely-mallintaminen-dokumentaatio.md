# Ohjelmistojen määrittely, mallintaminen ja dokumentointi

## Määrittely

Määrittelyssä lähdetään liikkeelle *asiakasvaatimusten selvittämisellä*. Kysymys kuuluukin: mitä asiakas tarvitsee? Ja tylsäähän se olisi, jos asiakas osaisi vastata tähän kysymykseen täydellisesti. Jokainen asiakas on erilainen.

> "In dealing with customers, you must understand that there are things they *want* and things they *need*." - Larry Bernstein

Määrittely on jatkuvaa ja orgaanista. Ideoita tulee ja menee projektin edetessä. On tärkeää, että oleelliset toiminnallisuudet saavat enemmän huomiota kuin satunnaiset päähänpistot. Tämän takia auttaa, jos *myös kehitystiimi ymmärtää asiakkaan liiketoimintaa*, jolloin heillä on mahdollisuus hahmottaa, mitä perimmäistä ongelmaa asiakkaan esittämällä vaatimuksella yritetään ratkaista. Jos ymmärretään ongelma, voidaan esittää siihen myös vaihtoehtoisia ratkaisuja (esim. ei toteuteta). [MoSCoW-metodia](http://en.wikipedia.org/wiki/MoSCoW_Method) ja vastaavia kysymyksiä voi käyttää apuna vaatimusten prioriteettien selvittämisessä. Yritä saada asiakas ymmärtämään, että vaatimukset, ehdotukset ja muutokset maksavat. Tämä auttaa välttymään ns. [feature creepiltä](http://en.wikipedia.org/wiki/Feature_creep).

Määrittelyvirhe voi tulla kalliiksi, ja virheen aiheuttama haitta eskaloituu sitä mukaa, mitä aikaisemmin virhe on tapahtunut ja mitä myöhemmin se on huomattu. Olen todennut wireframejen tai jopa prototyyppien olevan hyviä tapoja esittää onko asiakasvaatimus ymmärretty oikein. 

## UML

UML, Unified Modeling Language, on _visuaalinen_ kieli, jota käytetään järjestelmien määrittelyyn, suunnitteluun ja dokumentointiin. UML on yleisesti tunnettu kuvausmenetelmä, jolla visualisoidaan pääasiassa oliopohjaisia järjestelmiä. UML:n perimmäinen tarkoitus on auttaa ymmärtämään järjestelmää pääosin teknisestä näkökulmasta. Yhtenäisen, standardoidun kielen tarkoitus on ohjata _yksiselitteisyyteen_, eli UML:ää osaavien pitäisi ymmärtää kuvatut asiat samalla tavalla. 

UML:n tarkoitukseksi yleensä luonnetaan dokumentointi jälkikäteen tai suunnittelu etukäteen (jonka toteuttamisen voi ulkoistaa). Mutta sen sijaan, että dedikoitu UML-suunnittelija piirtäisi kiveenhakatut "ohjeet" ja antaisi ne ohjelmoijalle orjallisesti toteutettavaksi, kehittäjät voivat käyttää sitä itse UML:ää hyödyksi ideoidessaan. UML-kaavioita voi käyttää alustavien ideoiden hahmotteluun (jopa nopeammin kuin koodaamalla ja kokeilemalla) ja näin toivottavasti ohjata järjestelmää rakenteellisesti parempaan suuntaan.

UML voi olla osa dokumentaatiota. Järjestelmän muuttuessa dokumentaatiota pitää päivittää, tai muuten se vanhenee nopeasti, jonka jälkeen sen tuoma hyöty katoaa. Pahimmillaan vanhentunut dokumentaatio voi aiheuttaa väärinymmärryksiä ja turhaa työtä. Jos siis UML:llä kuvataan järjestelmän osia tai prosesseja (joskus hyvinkin spesifisesti) niin kaaviot on myös päivitettävä muutosten yhteydessä. Ja tämähän taas vaatii työtä. Kannattaakin harkita, kuinka tarkasti päättää järjestelmän osia mallintaa. Huomaa, että sama pätee dokumentaation myös yleisellä tasolla. 

Jos UML:n käytännöllisyys mietityttää, niin [tässä keskustelua aiheesta](http://stackoverflow.com/questions/18803/is-uml-practical).

### Käyttötapauskuvaus ja käyttötapauskaavio (Use Case Diagram)

[Käyttötapauskaavion](http://www.uml-diagrams.org/use-case-diagrams-examples.html) perustana toimii *käyttötapauskuvaus*. Käyttötapauskuvauksessa avataan toiminnallisuus sanallisesti. Käyttötapaukset ovatkin siis enemmän kirjoittamista, kuin kaavioiden avulla mallintamista. Käyttötapauskuvausten voisi sanoa olevan hyvin tarkasti kirjoitettuja käyttäjätarinoita (user story).

Käyttötapausten kirjoittamisen avuksi voidaan määritellä tietty rakenne (vaikka taulukkomuodossa), jossa kerrotaan [esim. esiehdot, kuvaus, sidosryhmät ja vaihtoehtoiset skenaariot](http://epf.eclipse.org/wikis/abrd/core.tech.common.extend_supp/guidances/examples/use_case_spec_CD5DD9B1.html).

### Luokkakaavio (Class Diagram)

[Luokkakaavio](http://www.uml-diagrams.org/class-diagrams-examples.html) kuvaa oliopohjaisen järjestelmän luokkarakenteen määrittely-/suunnittelutasolla. Esimerkiksi luokan metodit voidaan ilmaista pseudokoodilla ilman konkreettisia tyypityksiä. Luokkakaaviossa keskitytään rakenteen mallintamiseen yleisellä tasolla, josta selviää esim. seuraavat: 

- rajapinnat, perintä, kompositio ja muut vastaavat yhteydet
- attribuutit ja metodit
- nimeäminen.

Luokkakaavio voi auttaa rakenteellisesti järkevien OO-ratkaisujen hahmottelussa ja suunnittelussa.

### Sekvenssikaavio (Sequence Diagram)

[Sekvenssikaavio](http://www.uml-diagrams.org/sequence-diagrams-examples.html) muodostaa yhdessä luokkakaavion kanssa yleisen tavan mallintaa olio-ohjelmia. Sekvenssikaaviolla mallinnetaan olioiden interaktioita viestien avulla, eli minkälaisia reaktioketjuja tietyt tapahtumat aiheuttavat. Käytännössä kaaviosta selviää, mitä muita metodeja jokin tietty metodi saattaa kutsua ja minkälaista tietoa näiden välillä liikkuu.
Tämä myös auttaa hahmottamaan riippuvuuksia eri luokkien välillä.

### Tilakaavio (State Diagram)

[Tilakaaviota](http://www.uml-diagrams.org/state-machine-diagrams-examples.html) käytetään olion tai järjestelmän tilan ja elinkaaren kuvaamiseen. Kaaviosta selviää myös sallitut tilasiirtymät (esim. dokumentti voi siirtyä "luonnos"-tilasta "julkaistu"-tilaan) Tilakaaviossa kuvataan seuraavat asiat:

- Olion alkutila
- Olion tilamuutokset (jotka johtuvat ulkoisista tapahtumista).

### Aktiviteettikaavio (Activity Diagram)

[Aktiviteettikaavio](http://www.uml-diagrams.org/activity-diagrams-examples.html) muistuttaa tilakaavioita, mutta kuvaa prosesseja ja niissä tapahtumia peräkkäisiä tai rinnakkaisia toimintoja. Aktiviteettikaaviolla voidaan esimerkiksi ilmaista ostoprosessin tapahtumat.

## Dokumentointi

Ohjelmistojen tekemiseen kuuluu tärkeänä osana myös dokumentointi. Dokumentointikäytännöt vaihtelevat organisaation ja käytössä olevien menetelmien mukaan. Dokumenttien määrään vaikuttavat myös esim. projektin koko, tiimin koko ja laatujärjestelmät. Kriittisemmät järjestelmät noudattavat usein tiukempia prosesseja, jotka vaativat kattavampaa dokumentaatiota. Ohjelmistoprojektiin saattaa kuulua esim. seuraavia dokumentteja:

- projektisuunnitelma
- (toiminnallinen) määrittely
- tekninen määrittely
- testaussuunnitelma
- käyttöönottosuunnitelma
- ylläpito-ohje
- käyttöohje.

Seuraavaan listaan on koottu esimerkkejä erilaisista dokumenteista (niin koulu- kuin työelämästä).

- [Määrittelydokumentti](http://www.cs.tut.fi/~otm/harjoitukset/tupa-maarittelydokumentti.pdf): TuPa-tilanhallintajärjestelmä, esimerkki

- [Projektisuunnitelma](http://www.elka.fi/useruploads/files/Projektisuunnitelma_1.2.pdf): Arkistojärjestelmän suunnittelu ja prototyyppi

- [Tekninen suunnitelma (luonnos)](http://www.vm.fi/vm/fi/04_julkaisut_ja_asiakirjat/03_muut_asiakirjat/20101208Julkis/05_PERA_tekninen_maeaerittely_20101208.pdf): Julkishallinnon tietovarantojen yhteinen rajapintaratkaisu

- [Erilaisia dokumentteja](https://www.kanta.fi/fi/hl7) liittyen Kansallisen Terveysarkiston rajapintoihin (esim. eReseptin-rajapintamääritykset)