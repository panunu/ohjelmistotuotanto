# Ohjelmistojen määrittely ja mallintaminen

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


UML, Unified Modeling Language, on _visuaalinen_ kieli, jota käytetään järjestelmien määrittelyyn, suunnitteluun ja dokumentointiin. UML on yleisesti tunnettu kuvausmenetelmä, jolla visualisoidaan pääasiassa oliopohjaisia järjestelmiä. UML:n perimmäinen tarkoitus on auttaa ymmärtämään järjestelmää pääosin teknisestä näkökulmasta. Yhtenäisen kielen tarkoitus on ohjata yksiselitteisyyteen. 

Tarvitseeko aina mallintaa?

Voiko mallintamisesta olla jotain haittaa?



## Käyttötapaus ja käyttötapauskaavio (Use Case)

Käyttötapauskaavion perustana toimii *käyttötapauskuvaus*. Käyttötapauskuvauksessa avataan toiminnallisuus sanallisesti. Käyttötapaukset ovatkin siis enemmän kirjoittamista, kuin kaavioiden avulla mallintamista.

Käyttötapausten kirjoittamisen avuksi on määritelty tietty rakenne, jossa kerrotaan esim. sidosryhmät ja lähtötilanne. Esimerkki tässä !!!!!
Esimerkkejä varsinaisista kaaviosta voi katsella esim. [tästä](http://www.uml-diagrams.org/use-case-diagrams-examples.html).

## Luokkakaavio (Class)

Luokkakaavio kuvaa oliopohjaisen järjestelmän luokkarakenteen määrittely/suunnittelutasolla. Esimerkiksi luokan metodit voidaan ilmaista pseudokoodilla ilman konkreettisia tyypityksiä. 

## Sekvenssikaavio (Sequence)

Sekvenssikaavio muodostaa yhdessä luokkakaavion kanssa yleisen tavan mallintaa olio-ohjelmia. Sekvenssikaaviolla mallinnetaan olioiden interaktioita viestien avulla, eli minkälaisia reaktioketjuja tietyt tapahtumat aiheuttavat. Käytännössä kaaviosta selviää, mitä muita metodeja jokin tietty metodi saattaa kutsua ja minkälaista tietoa näiden välillä liikkuu.
Tämä myös auttaa hahmottamaan riippuvuuksia eri luokkien välillä.

## Tilakaavio (State) ?

Tilakaaviota käytetään olion tai järjestelmän elinkaaren mallintamiseen. Tilakaaviossa kuvataan seuraavat asiat:

- Olion alkutila
- Olion tilamuutokset (jotka johtuvat ulkoisista tapahtumista).
