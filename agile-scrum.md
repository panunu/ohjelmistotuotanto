# Ketterät menetelmät: Scrum

## Agile

Agilen, eli ketterien menetelmien, ajatukset perustuvat n. 10 vuotta sitten Utahissa koottuun manifestiin. Manifestin luonnissa oli mukana nimekkäitä ohjelmistoalan guruja. Ketterien projektien perusajatuksena on keskittyminen itse tuotteeseen ja sitä kehittäviin ihmisiin sen sijaan, että pääpaino olisi projektin prosessien pyörittämisessä. Manifestiin voi tarkemmin tutustua osoitteessa [http://agilemanifesto.org](http://agilemanifesto.org), joka on käännetty myös suomeksi.

Miksi muuten ketterät menetelmät ovat ylipäätään syntyneet? Selityksenä voi olla esimerkiksi turhautuneisuus byrokratiaan ja raskaisiin prosesseihin. Vaikka käytettiin paljon energiaa projektin kehittämiseen, koettiin, ettei asiakas saanut rahoillensa vastinetta, eikä tiimikään ollut tyytyväinen tulokseensa. Tärkeinä tekijöinä [manifestin periaatteista](http://agilemanifesto.org/iso/fi/principles.html) nouseekin esille arvon tuottaminen asiakkaalle ja tiimin kompetenssin ja prosessien jatkuva kehittäminen.

## Scrum

Scrum tarjoaa viitekehyksen projektien pyörittämiseen, ottamatta kuitenkaan tarkemmin kantaa toteutustapoihin tai -tekniikoihin (toisin kuin esimerkiksi Extreme Programming, XP). Vaikka Scrum saattaa alkuun vaikuttaa vähän hankalalta uusien käsitteiden takia, niin käytännössä prosessi pyörii kohtuullisen luonnollisesti.

### Työvälineet

Scrum sisältää seuraavanlaisia [käsitteitä tai vaiheita](http://upload.wikimedia.org/wikipedia/commons/5/58/Scrum_process.svg):

- User Story
- Product Backlog
- Sprint
- Sprint Backlog
- Potentially Shippable Product.

**User Story** (käyttäjätarina) on yksi järjestelmän toiminnallisuuksista kuvattuna lauseena, jonka asiakas ymmärtää (ei siis sisällä teknistä jargonia). Esimerkki käyttäjätarinasta:

"Opettaja voi hyväksyä ilmoittautuneen opiskelijan kurssille"

Eli toisinsanoen käyttäjätarina kuvaa _kuka tekee ja mitä_, sekä joskus myös _miksi_ (eli mikä hyöty tästä toiminnosta seuraa). Tuotteella on siis useita käyttäjätarinoita, jotka koostamalla voi hahmottaa, minkälainen ohjelmisto oikein on kyseessä. Kaikki käyttäjätarinat kuuluvat **Product Backlogiin**. Tämä on asiakkaan ns. toivomuskaivo, jossa listataan kaikki asiakkaan haluamat toiminnallisuudet (yleensä käyttäjätarinoiden muodossa). Product Backlog on hyvä pitää ajankohtaisena. Tämä sisältää sen, että Backlogin käyttäjätarinoita prioritisoidaan, ja tarkistetaan, että käyttäjätarinat ovat ylipäätään enää ajankohtaisia, ja muutetaan niitä tarvittaessa ([Backlog Grooming](http://www.agilejournal.com/articles/columns/column-articles/2647-grooming-the-product-backlog)).

**Sprint** on iteraatio, ajallisesti määritelty jakso, joka on pituudeltaan tyypillisesti esim. 1-2 viikkoa. Jokaiselle Sprintille määritetään **Sprint Backlog**, joka sisältää Product Backlogista valittuja käyttäjätarinoita. Sprintin aikana on tarkoitus toteuttaa nämä Sprint Backlogissa olevat käyttäjätarinat.

Sprintin lopussa syntyy osa ohjelmistoa, **Potentially Shippable Product**, joka ideaalitilanteessa voidaan viedä suoraan tuotantoon. Näin iteraation aikana toteutettu toiminnallisuus alkaa tuottamaan heti lisäarvoa asiakkaalle.

### Palaverit

Scrumiin kuuluu seuraavat palaverit:

- Sprint Planning
- Daily Scrum
- Sprint Review
- Retrospective.

**Sprint Planning** pidetään jokaisen iteraation alussa. Tämän aikana suunnitellaan esim. sprintin pituus ja mitä tehdään. Yleensä myös viimeistään tässä vaiheessa käydään läpi, ovatko työstettäväksi valitut käyttäjätarinat määritelty tarpeeksi hyvin. 

**Daily Scrum** on päivittäinen lyhyt (n. 10-15 min) tilannepäivitys tiimin jäsenten kesken. Huomaa, että tähän ei osallistu projektin ulkopuoliset henkilöt häiritsemään. "Kokous" pidetään seisten (jotta kokous todellakin pysyy lyhyenä), ja jokainen kertoo vuorollaan kolme seuraavaa asiaa:

1. Mitä olen tehnyt viimeksi
2. Mitä tulen tekemään seuraavaksi
3. Onko esteitä/hidasteita/ongelmia.

Pidemmät keskustelut on tarkoitus pitää dailyn ulkopuolella.  Joskus daily saattaa tuntua turhauttavalta, mutta kannattaa käyttää tämä hetki hyödyksi. Sen aikana voit hetkeksi hengähtää, ja keskittyä pohtimaan mitä kannattaisi tehdä seuraavaksi.

**Sprint Review:n** aikana esitellään sprintin aikana toteutetut toiminnallisudeet asiakkaalle (eli demo itse tuotteesta), eikä pidetä tuotteen kannalta epärelevantteja kalvosulkeisia. Palaverin yhteydessä Product Owner yleensä myös hyväksyy tehdyt toiminnallisuudet.

**Retrospective** (latinaksi _retrospectare_, eli "katso taakse"), pidetään sprintin lopuksi. Sen aikana tarkastellaan kriittisesti edellistä sprinttiä ja yritetään parantaa prosesseja seuraavaa iteraatiota varten. Vinkkejä retrospektiivin pitämiseen löytyy vaikka [täältä](http://blog.scrumphony.com/2012/09/inject-purpose-into-retrospectives/).

### Roolit

Scrumissa on kolme roolia:

- Scrum-tiimi
- Scrum Master
- Product Owner.

**Scrum-tiimi** koostuu tietysti toteuttajista. Yleensä tiimin koko on 7 ± 2, ottaen tietysti huomioon, että pieneen projektiin ei tarvitse välttämättä näin montaa ohjelmistokehittäjää. Mutta jos kehittäjämäärä menee tämän rajan yli, voi harkita projektin jakamista pienempiin osiin (useammalle tiimille).

**Scrum Master** toimii "palvelijana" (ns. servant leader) tiimille. Hänen tehtävänään on esimerkiksi ratkaista mahdolliset ongelmatilanteet (impediments); asiat, jotka häiritsevät tiimin tuottavuutta. 

**Product Owner** on asiakas, tai asiakkaan edustaja. Vaatimuksena on, että Product Ownerin hallitsee edustamansa liiketoiminnan. Hänen tehtävänään on päättää mitä tällä hetkellä ja seuraavaksi työstetään. Priorisointi onkin yksi hänen tärkeimmistä tehtävistään. Product Owner voi järjestää toteutettavat toiminnallisuudet esim. arvioidun ROI:n (Return On Investment) perusteella. Hänen kauttaan yleensä hyväksytetään iteraation aikana syntynyt lopputulos.

Lisää Scrumista voi ja kannattaa lukea esim. [Scrum Guidesta](http://www.scribd.com/doc/44447453/Scrum-Guide-Fi). Tässä myös [hyvä kooste Scrumin termeistä](http://www.scrumalliance.org/articles/39-glossary-of-scrum-terms).

### Scrum-tehtävätaulu (Kanban-taulu)

[Tehtävätaulun](http://upload.wikimedia.org/wikipedia/commons/1/1b/Scrum_task_board.jpg) tarkoitus on helpottaa sprintin aikana suoritettavien tehtävien seurantaa. Taululle lisätään sprintin käyttäjätarinat/toiminnallisuudet Post-it -lapuilla. 

Taulussa on muutamia, projektikohtaisesti määritettäviä pystypalkkeja, esim.:

1. Not started
2. In progress
3. Testing
4. Done.

Nämä kolumnit kuvaavat käyttäjätarinan tämänhetkistä tilaa. Käyttäjätarina etenee taululla vaakatasossa yhden vaiheen kerrallaan.  

Fyysisen taulun ongelmaksi muodostuu kuitenkin mahdollinen läpinäkymättömyys sidosryhmille, joka taas on vastoin Agilen periaatteita. Myöskin ylläpidettävyys hankaloituu nopeasti, kun tehtävien määrä taululla kasvaa. Ratkaisuna tähän on erilaiset Scrumiin soveltuvat ohjelmistot, kuten [Agilefant](http://www.agilefant.org) tai [Jira](http://www.atlassian.com/software/jira/overview).

## Maailma on nyt pelastettu, kiitos Agilen?

Huomioitavaa on, että **ei ole olemassa** yhtä tiettyä menetelmää (ns. silver bullet), joka soveltuu kaikkiin projekteihin ja ratkaisee jokaisen ongelman, vaan menetelmät kannattaa harkita projekti- tai tiimikohtaisesti (sama pätee teknologiavalintoihin). Jos haluat tietää, miten ketteryys toimii oikeassa maailmassa, niin tässä esim. Microsoftin tekemä [tutkielma Agile-kokemuksistaan](http://research.microsoft.com/pubs/56015/agiledevatms-esem07.pdf).

