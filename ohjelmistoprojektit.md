# Ohjelmistoprojektit

Ohjelmistoprojektit lähtevät usein liikkeelle siitä, että esim. asiakas pyytää tarjousta kilpailutuksen yhteydessä. Oikeastaan projekti alkaakin jo tässä vaiheessa, koska tarjouksen antaminen ei ole yksiselitteistä, vaan vaatii asiakkaan kanssa tehtävää alustavaa määrittelytyötä. Tasapainottelua vaatii se, osallistuako kilpailutukseen (eli onko voittaminen edes realistista), koska (järkevän) tarjouksen laatiminen vaatii resursseja.

## Hinnoittelusta

Projekteihin sovellettavia hinnoittelumalleja on yhtä paljon kuin projekteja, mutta mainittakoon silti muutama yleispätevä esimerkki:

- Tuntiveloitus
- Kiinteä hinta (fixed)
- Tavoitehinta (target).

**Tuntiveloituksessa** hinta riippuu projektiin käytetystä työmäärästä (tunneista). Taloudellinen riski onkin asiakkaalla, koska ei voida olla varmoja, haluaako toimittaja palvella asiakasta parhaansa mukaan, vai laskuttaa mahdollisimman paljon.

**Kiinteähintaisessa** projektissa riski on toimittajalla. Toisaalta sillä on mahdollisuus tehdä hyvin voittoa siinä tapauksessa, että projekti valmistuu huomattavasti oletettua nopeammin. Muutospyynnöt kuitenkin yleensä muuttavat hintaa. Paha virhe on tehdä kiinteähintainen sopimus ketterässä projektissa.

**Tavoitehinta** saattaa olla usein realistinen vaihtoehto. Projektin hinnalle asetetaan raja, esim. 100 000 €. Jos laskutettavan työn tuntien kokonaishinta ylittää tämän 100 000 €:n rajan, ylimenevä työ laskutetaan esim. omakustannehintaan (sopimuksesta riippuen).

## Onnistumisia?

Projektin onnistumista voidaan mitata esim. seuraavilla tavoilla:

1. Hyöty (esim. liiketaloudellinen)
2. Aikataulu
3. Budjetti.

Miksi sitten niin useat ohjelmistoprojektit epäonnistuvat jollain tasolla (usein aikataulu tai budjetti)? Jos tarkastellaan ohjelmistoprojektien tilastoja (esim. [IT Cortex](http://www.it-cortex.com/Stat_Failure_Rate.htm)), luvut ovat harmillisen huonoja. Joku voisi väittää yhden yleisen tekijän olevan alan nuori ikä (esim. verrattuna rakennusalaan), jonka takia vakiintuneita käytäntöjä (ns. kansanoppia) ei ole ehtinyt muodostua (prosessien kypsyyttä voi arvioida esim. [CMM eli Capability Maturity Model](http://en.wikipedia.org/wiki/Capability_Maturity_Model)). Yleensä myös oletetaan, että ohjelmistoja rakennetaan samalla tavalla kuin taloja.

> "We are still in the infancy of naming what is really happening on software development projects." - Alistair Cockburn

Ohjelmistokehittäjien lisääminen projektiin (varsinkin loppuvaiheessa) harvoin parantaa sen edistymistahtia (kts. [Brookin laki](http://en.wikipedia.org/wiki/Brooks's_law)). Uusi tekijä tarvitsee aina perehdytystä, ja kestää aina hetkensä, ennen kuin omaksuu tiimille vakiintuneet työskentelymetodit. Myöskin kehittäjien väliset mahdolliset kommunikointipolut moninkertaistuvat nopeasti (tätä voidaan kuvata [seuraavalla graafilla](http://en.wikipedia.org/wiki/Complete_graph)). Tiukkaa aikataulua ei siis paikata henkilömäärän kasvattamisella. Pahimmassa tapauksessa tämä johtaa siihen, että aikataulun lisäksi myös budjetti ylitetään.

Ohjelmistotyö ja -projektit ovat pitkälti kompleksisuuden hallintaa. Yksi tapa helpottaa monimutkaisten asioiden hahmottamista on jakaa ne pienempiin osakokonaisuuksiin. Ehkä tästä voisi olla hyötyä myös ohjelmistoprojekteissa?

## Arviointi (työmäärät)

Työmäärien arviointi tai projektin valmistuspäivämäärän ennustaminen on vaikeaa. Dilemma onkin, että projektin alkuvaiheessa pitäisi jo olla tiedossa paljon projektiin menee resursseja (vaikka lopputuote voi olla vielä kohtuullisen tuntematon)! Wikipediassa on listattuna [muutamia sovelluskehitykseen liittyviä arviointimenetelmiä](http://en.wikipedia.org/wiki/Cost_estimation_in_software_engineering).

Eräs tapa arvioida valmistumisajankohta ketterissä projekteissa on laskea projektin vauhtia (velocity). Tämä perustuu siihen, että seurataan iteraatiossa toteutuneiden työmäärien (eli esim. tuntien, Story Pointtien tai kompleksisuuksien) keskiarvoa. Näin saadaan jonkinlainen arvio siitä, paljonko saadaan aikaiseksi yhdessä iteraatiossa. Tästä voidaan laskea projektin valmistumiseen tarvittavien iteraatioiden (ja ajan) määrä jakamalla kokonaistyömäärä lasketulla vauhdilla, sekä hahmottaa riittääkö asetettu budjetti.

Erään tutkimuksen mukaan [vähemmillä arvioilla saadaan ennustettua tarkempi lopputulos](http://softwaredevelopmenttoday.blogspot.de/2012/07/a-better-way-to-predict-project-release.html). Kannattaa suhtautua tuloksiin  varauksella, mutta mielestäni ihan mielenkiintoinen esimerkki arviointien arvaamattomuudesta.

## Muuta

Timo Lehtimäen *Ohjelmistoprojektit käytännössä* -kirjassa käsitellään ohjelmistoprojekteihin liittyviä aiheita mukavan rennosti, mutta asiallisesti. Suosittelen lukemaan varsinkin siinä tapauksessa, jos projektien johtaminen, tai minkälaisiin haasteisiin siinä törmää, saattaa kiinnostaa.

> "All projects are different, but you have to treat each one with care. Sometimes you get to build a luxury yacht; other times, it’ll be a rowboat. You still have to make sure the thing doesn’t spring a leak." - Stefan G. Bucher