# Test-driven development

Test-driven development (eli testivetoinen kehitys) ei sinänsä ole uusi tekniikka, mutta se on vasta viime vuosina saavuttanut valtavirran huomion. TDD:n periaate on yksinkertainen: ennen varsinaista koodia aloitetaan kirjoittamalla yksikkötesti. Testi määrittää, miten testattavan funktion tai metodin olisi tarkoitus toimia. Tämän jälkeen kirjoitetaan sen verran ohjelmakoodia, että saadaan testi menemään läpi. Viimeiseksi voidaan refaktoroida koodia siistimmäksi. Muista tarkistaa, että testi menee vielä läpi refaktoroinnin jälkeen.

Kerrataan vielä:

1. Testitapauksen kirjoittaminen
2. Ohjelmakoodin kirjoittaminen
3. Refaktorointi.

Kyseinen useasti toistettava iteraatio kannattaa pitää mahdollisimman lyhyenä. Jos yhdestä testitapauksesta tulee liian laaja, voi olla vaikea kirjoittaa vaadittava ohjelmakoodi, joka läpäisee testin. Jos taas yksittäinen testitapaus pidetään yksinkertaisena, mahdollisen virheen paikantaminen testin toteuttavasta ohjelmakoodista on huomattavasti helpompaa.

TDD vaatii, että koodisi tulee olla helposti testattavaa, joka taas ohjaa järkeviin rakenteellisiin ratkaisuihin. Tämän takia joskus puhutaankin test-driven *designista*. Merkittävä suunnittelumalli, johon testattavuus perustuu, on Dependency Injection (eli vapaasti suomennettuna riippuvuuksien injektointi). Tämä tarkoittaa sitä, että jos jokin toiminnallisuus on riippuvainen toisesta (esimerkiksi käytetään jotakin luokkaa hyödyksi), annetaan toiminnallisuudelle riippuvuus parametrina sen sijaan, että määriteltäisiin tämä riippuvuus toiminnallisuuden yhteydessä (esim. uusi ilmentymä luokasta new-avainsanalla). DI mahdollistaa sen, että testattaessa voimme vähentää tarvittavien riippuvuuksien määrää antamalla parametrina ns. väärennöksen oikean toteutuksen sijasta. Kyseinen tekniikka tunnetaan nimellä "mocking". Erilaisten "mockien" erot on tiivistetty hyvin Martin Fowlerin kirjoituksessa ["Mocks aren't stubs"](http://martinfowler.com/articles/mocksArentStubs.html).

Täytyy muistaa, että testit tuovat lisää ylläpidettävää koodia projektiin, joka yhtälailla vaatii suunnittelua ja refaktorointia. TDD lähtökohtaisesti ohjaa siihen, että kaikki koodi tulee testattua (test-**driven**). Mutta yksi tärkeä (eikä ollenkaan yksiselitteinen) kysymys mielestäni onkin, kannattaako kaikkea testata? Suosittelen lukemaan [seuraavan keskustelun](http://stackoverflow.com/questions/153234/how-deep-are-your-unit-tests/153565#153565) aiheesta, jossa on mukana nimekkäitäkin TDD-konkareita, kuten Kent Beck. Kannattaa myös miettiä, minkä tason testeihin panostaa. Martin Fowler esittää [kirjoituksessaan](http://martinfowler.com/bliki/TestPyramid.html) eritasoisten testien hyötyjä ja haittoja.

## Miksi?

Mitä hyötyjä TDD sitten tuo? Listaan tähän muutaman:

1. Koodi tulee oletusarvoisesti testattua
2. Testit vähentävät bugeja
3. Testit varmistavat, ettei toiminnallisuus hajoa muutosten yhteydessä
4. Rajapinnat muodostuvat järkevämmiksi melkein itsestään
5. Spesifikaatio tulee evaluoitua (jos herää kysymyksiä, määrittelyssä on parannettavaa)
6. Toiminnallisuus dokumentoidaan testitapauksilla
7. Julkaistavaa (shippable) koodia, ei legacya
8. Mielenrauhaa.

TDD:n omaksuminen vaatii oman aikansa ja siksi kannattaakin alkaa harjoittaa sitä esimerkiksi koulu- tai harrasteprojekteissa, joissa kokeilut ovat riskittömiä. Myös muiden kirjoittamien testien lukeminen voi olla hyödyksi alkuvaiheessa, jotta hahmottaa, minkälaisia testejä kannattaa suunnilleen kirjoittaa. Esimerkiksi Lasse Koskelan Test Driven -kirjassa käsitellään TDD:n teoriaa syvemmin ja esitellään realistisia testitapauksia (Javan viitekehyksessä). Vaihtoehtoinen lähestymistapa seurata testikoodin laatua, on verrata sitä huonoihin esimerkkeihin. James Carr on koonnut kyseisten esimerkkien, anti-patterneiden, [katalogin](http://blog.james-carr.org/2006/11/03/tdd-anti-patterns/). 

Filosofisia, yleismaailmallisia neuvoja testauksesta voi lukea  ["The Way of Testivuksesta"](http://www.agitar.com/downloads/TheWayOfTestivus.pdf).