# Laatua tekniikoilla, konventioilla ja suunnittelumalleilla

Miksi ja miten tehdä siedettävää koodia, jota muutkin pystyvät ymmärtämään, eikä se hajoa käsiin? Kannattaa aloittaa pohdiskelu Uncle Bobin kohta jo 10 vuotta vanhalla, mutta silti pätevällä [vinkillä](http://www.artima.com/weblogs/viewpost.jsp?thread=51769).

## Laatu, ja miksi panostaa siihen

Laatu voi olla hyvinkin subjektiivinen käsite. Mitä laatu ohjelmistoissa on? Laadun hahmottamista helpottaa, jos sen jakaa esim. sisäisiin (kehittäjien kokemiin) ja ulkoisiin (asiakkaan kokemiin) laatutekijöihin. Tässä esimerkiksi yksi jaottelu, mitä nämä [sisäiset ja ulkoiset tekijät](http://www.ocoudert.com/blog/2011/04/09/what-is-software-quality/) voivat olla.

Puutteet ulkoisissa laatutekijöissä tulee usein esille esim. toiminnallisuuteen tai käyttöliittymään tyytymättömän asiakkaan muodossa, mutta sisäiset laatupuutteet saattavat vaania piilossa kauemmin; asiakas ei nimittäin ohjelmistokoodia tarkastele vaan vastuu on ohjelmistokehittäjillä. Nämä puutteet kuitenkin saattaa tulla myöhemmin esille eri muodoissa:

- virheiden määrä kasvaa
- muutokset toiminnallisuuksissa vievät aina vaan enemmän aikaa
- kustannukset kasvavat.

Laadun heikkeneminen voi johtua vaikka siitä, että oikaistaan ratkaisussa, jotta saadaan nopeasti jotain ulos. Tämä johtaa ns. [tekniseen velkaan](http://www.scrumalliance.org/articles/14-technical-debt-and-design-death). Tätä velkaa voi välttää tai vähentää esimerkiksi suunnittelulla, testien kirjoittamisella ja refaktoroinnilla.

Mitä sitten refaktorointi on? Martin Fowler on muotoillut asian seuraavanlaisesti: "Refactoring is the process of changing a software system in such a way that it does not alter the external behavior of the code yet improves its internal structure". Täältä löytyy myös poimintoja käsitteestä, ja mitä siihen kuuluu: [http://c2.com/cgi/wiki?WhatIsRefactoring](http://c2.com/cgi/wiki?WhatIsRefactoring).

> "When you feel the need to write a comment, first try to refactor the code so that any comment becomes unnecessary." - Martin Fowler 

## Code smells

Huonon koodin voi tunnistaa tarkkailemalla tiettyjä piirteitä. Nämä piirteet ovat yksinkertaisia, joten ne on helppo tunnistaa, mutta samalla niihin on helppo sortua. Suosittelen lukemaan seuraavan listan erilaisista "hajuista":
[http://www.codinghorror.com/blog/2006/05/code-smells.html](http://www.codinghorror.com/blog/2006/05/code-smells.html).

Tässä myös [käytännönläheinen presentaatio](http://www.youtube.com/watch?feature=player_embedded&v=wmgnFbsaPvo) samaisesta aiheesta (PHP:n viitekehyksessä). Ja jos haluat opetella kirjoittamaan nimenomaan huonoa koodia, niin tähänkin löytyy [ohjeistusta](http://thc.org/root/phun/unmaintain.html). Huonoa koodia kirjoittaessa kannattaa kuitenkin muistaa, että joku (vaikka sinä itse) joutuu [sitä myöhemmin tulkitsemaan](http://www.codinghorror.com/blog/2006/09/when-understanding-means-rewriting.html).

> "Any fool can write code that a computer can understand. Good programmers write code that humans can understand." - Martin Fowler

## Suunnittelumalleja, standardeja ja konventioita

Tämän otsikon alle on listattu muutamia järkeviä ajattelu- tai työskentelytapoja, jotka helpottavat laadun ylläpitämistä.

### DRY

Do not repeat yourself, eli älä toista itseäsi. Ei siis copypasta-koodia!

### Boyscout Rule

Partiolaisten sääntö: jätä leiripaikka siistimmäksi kuin mitä se oli tullessasi. Eli refaktoroi aikaisempaa koodia tarvittaessa.

### Single Responsibility Principle

Yhdellä luokalla on yksi vastuualue. Vältetään monoliitteja, tuhansien rivien pituisia luokkia, jotka tekevät puolet järjestelmän toiminnoista.

### Koodistandardit/-käytännöt

Yhdenmukaistetaan koodin ulkoasua (sisennökset, kommentointi, rakenteet) standardeilla. Esimerkkiä tästä: [PHP: PSR-2 coding style guide](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md) tai [Code conventions for Java](http://www.oracle.com/technetwork/java/javase/documentation/codeconvtoc-136057.html). 

### Suunnittelumallit

Olio-ohjelmoinnin maailmaan kuuluu yleisiä suunnittelumalleja (design patterns), joilla voidaan ratkaista erilaisia ongelmakohtia. Näitä voit tarkastella esim. seuraavista lähteistä:

- [http://c2.com/cgi/wiki?SoftwareDesignPatternsIndex](http://c2.com/cgi/wiki?SoftwareDesignPatternsIndex)
- [http://www.oodesign.com](http://www.oodesign.com)

### SOLID

Konsepti, joka koostuu tietyistä suunnittelumalleista, joilla pyritään vähentämään huonoa koodia: [http://en.wikipedia.org/wiki/Solid_(object-oriented_design)](http://en.wikipedia.org/wiki/Solid_(object-oriented_design)).

## Työskentelymetodit ja -tekniikat

### Pariohjelmointi (Pair programming)

Pariohjelmoinnissa kaksi ohjelmoijaa työskentelee saman tehtävän parissa, mutta käytössä on vain yksi näppäimistö. Toisen rooli  on varsinaisen koodin kirjoittaminen (driver), kun taas toinen keskittyy suurempiin linjoihin: mitä seuraavaksi, voisiko tämän ratkaista paremmin, löytyykö virheitä (navigator). Rooleja vaihdetaan sovituin väliajoin. Lisää aiheesta: [http://www2.yk.psu.edu/~sg3/cmpbd205/assign/week01/ACMarticlePairProgramming.pdf](http://www2.yk.psu.edu/~sg3/cmpbd205/assign/week01/ACMarticlePairProgramming.pdf).

### Koodin katselmointi (Code review)

> "A good developer should always want another dev to read his code, because that makes it possible for at least one of them to learn something" - Mario Fusco

Koodin katselmointi on hyvä tapa oppia. Katselmoinnilla voi yhtenäistää käytännöt nopeasti, joka on erityisen hyödyllistä varsinkin jos olette aloittaneet  projektin uudella ryhmällä. Katselmointi voi kuulua osaksi arkipäivän rutiinia (esim. Pull Requestien yhteydessä), tai tiimi voi varata katselmoinnille kiinteän yhteisen ajan. Katselmointia voi hyödyntää esimerkiksi siinä tapauksessa, kun haluaa kuulla mielipiteen toteutuksesta (kun vaikka tehdään hyvin olennaista tai laajaa toiminnallisuutta).

[http://www.codinghorror.com/blog/2006/01/code-reviews-just-do-it.html](http://www.codinghorror.com/blog/2006/01/code-reviews-just-do-it.html)

### TDD 

Testivetoinen kehitys. Yksinkertaistettuna tarkoittaa sitä, että aina aluksi kirjoitetaan testitapaus, jota vasten toteutetaan varsinainen tuotantokoodi. Näin varmistetaan, että ohjelma tekee sen mikä on testien mukaan tarkoitus.

### Pomodoro-tekniikka

Voi käyttää hyödyksi pariohjelmoinnissa, ja voi metodina auttaa saamaan asioita aikaiseksi: [http://en.wikipedia.org/wiki/Pomodoro_Technique](http://en.wikipedia.org/wiki/Pomodoro_Technique).