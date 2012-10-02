# Versiohallinta

Versiohallinta on lähes välttämätön arkipäivän työväline, ja sitä käytetään kaikissa vakavasti otettavissa ohjelmistoalan yrityksissä. Versiohallinta helpottaa *samanaikaista työskentelyä samojen tiedostojen kanssa*. Versiohallinta toimii samalla myös yksinkertaisena varmuuskopiointimetodina.

## Miksi versiohallintaa tarvitaan

Versiohallinta ratkaisee useita (varsinkin tiimityössä ilmeneviä) ongelmia. Pari yksinkertaista esimerkkiä:

1. Ohjelmoija A tekee muutoksen
2. Ohjelmoija B haluaa uusimman version projektista.

**Ongelma**: mistä saada uusimmat tiedostot, ja mistää tietää mitkä tiedostot ovat muuttuneet?

**Tai**

1. Ohjelmoija A muokkaa tiedostoja 1 ja 2
2. Ohjelmoija B tekee myös muutoksia tiedostoon 2 (ja vielä samanaikaisesti)
3. Molemmat haluavat jakaa muutoksensa muille.

**Ongelma**: mitkä muutokset pitää säilyttää ja mitkä niistä ovat uusimpia?

## Git

Git on vuonna 2005 julkaistu (hajautettu) versiohallintajärjestelmä. Git kehitettiin Linuxin kernelin muutosten hallitsemiseksi, ja Gitin kehittämisen aloitti itse Linus Torvalds. Jos haluat tietää enemmän Gitin taustasta (tai et ole ennen kuullut hänen puheitaan), niin voit tutustua [seuraavaan Torvaldsin presentaatioon Googlella](http://www.youtube.com/watch?v=4XpnKHJAok8). Versiohallinnasta ja Gitistä voi lukea tai katsella jälkimmäisen dokumentaatiosivuilta: [http://git-scm.com/documentation](http://git-scm.com/documentation).

## Käsitteitä

### Repository

Repository on "varasto", jossa lähdekoodi on säilötty yhdessä versiohallintaan liittyvien tietojen (esim. historia) kanssa.

### Commit

Versiohallinta seuraa muutoksia tiedostojen sisällössä (jopa merkkitasolla). Muutosten jälkeen ohjelmoija haluaa hyväksyä muutokset (change-set). Silloin tehdään ns. commit. Commit sisältää nämä muutokset, ja järkevän viestin siitä, mitä muutokset saivat aikaan. Commit lisää muutokset projektin lähdekoodin ns. aikajanalle (branchiin).

### Branch

Oletuksena kaikki commitit, eli muutokset, lisätään ns. master-branchiin (haara). Näitä brancheja voi olla useita samanaikaisesti (esim. oma branch, kun teet uutta toiminnallisuutta), jolloin muutokset eivät vaikuta kuin aktiiviseen branchiin. Branchit voi yhdistää (merge) muihin brancheihin (yleensä takaisin masteriin).

## Branching

Ohjelmistotyössä usein törmäät tilanteeseen, jossa et ole ihan varma, miten ongelma kannattaisi teknisesti ratkaista. Tämän takia on tärkeää, että voit kokeilla toteuttamista ja palata helposti takaisin lähtötilanteeseen. Toisaalta jos toteutus onnistuukin, haluat jakaa sen muille.

Tämä helpottuu ns. branching-ajattelulla, jonka Git tekee helpoksi. Sen sijaan, että toteutuskokeilun jälkeen vain peruuttaisit kaikki muutokset (jolloin menetät ne kokonaan), voit aloittaa toiminnallisuuden toteuttamisen omassa branchissaan (oksa tai haara). Luot oman branchin, joka ei vaikuta ns. masteriin (päähaara, johon kaikki muutokset oletusarvoisesti menee). Nyt voit omassa branchissasi tehdä muutoksia ja commitoida normaalisti. Jos toteutus onnistuu, voit liittää nämä commitit masteriin. Jos toteutus ei onnistu (tai muuten vaan haluat tehdä jotain muuta), niin valitset vain aktiiviseksi branchiksi masterin. Huom. voit myös jakaa oman branchisi muille. Näin muut pääsevät tarkastelemaan toteutustasi vaihtamalla heidän aktiivisen branchin sinun branchiksi. Tarkastelun jälkeen he voivat vaihtaa takaisin siihen branchiin, jossa olivat olleet aikaisemmin.

Lisää ajatuksia ja branchien käyttötarkoituksia löytyy [täältä](http://nvie.com/posts/a-successful-git-branching-model/). Myös Martin Fowler on blogannut aiheesta [feature branching](http://martinfowler.com/bliki/FeatureBranch.html). 

## Github

Github on palvelu, jossa voit hostata projektejasi. Julkisia repositoryja voit tehdä rajattomasti. Opiskelijoille on myös tarjolla ilmainen micro-plan, joka oikeuttaa viiteen privaattiin repositoryyn: [https://github.com/edu](https://github.com/edu).

Github on hyvä paikka säilöä esim. koulu- tai harrasteprojektit. Samalla teet hyvän vaikutuksen työhaastattelussa, kun sinulla on mahdollisuus näyttää koodiesimerkkejä.