# Versiohallinta

- Mikä
- Miksi
- Commitit
- Branchit
- Feature Branching
- Distributed
- Git
- Github

Versiohallinta on lähes välttämätön arkipäivän työväline, ja sitä käytetään  kaikissa vakavasti otettavissa ohjelmistoalan yrityksissä. Versiohallinta helpottaa ryhmän samanaikaista työskentelyä samojen tiedostojen kanssa. Voisi myös sanoa, että se toimii samalla myös yksinkertaisena varmuuskopiointivälineenä.

## Git

Git on Linus Torvaldsin aloittama vuonna 2005 julkaistu versiohallintajärjestelmä. Git kehitettiin Linuxin kernelin muutosten hallitsemiseksi. Jos haluat tietää enemmän Gitin taustasta (tai et ole ennen kuullut hänen puheitaan), niin voit tutustua [seuraavaan Torvaldsin presentaatioon Googlella](http://www.youtube.com/watch?v=4XpnKHJAok8).

## Miksi versiohallintaa tarvitaan

Versiohallinta ratkaisee useita (varsinkin tiimityössä esille tulevia) pieniä, mutta tärkeitä ongelmia. Esimerkkeinä:

1. Ohjelmoija A tekee muutoksen
2. Ohjelmoija B haluaa uusimman version projektista.

**Ongelma**: mistä saada uusimmat tiedostot, ja mistää tietää mitkä tiedostot ovat muuttuneet?

**Tai**

1. Ohjelmoija A muokkaa tiedostoja 1 ja 2
2. Ohjelmoija B tekee myös muutoksia tiedostoon 2 (ja vielä samanaikaisesti).

**Ongelma**: mitkä muutokset pitää säilyttää ja mitkä niistä ovat uusimpia?

## Branching

Ohjelmistotyössä usein törmäät tilanteeseen, jossa et ole ihan varma, miten ongelma kannattaisi teknisesti ratkaista. Tämän takia on tärkeää, että voit kokeilla toteuttamista ja palata helposti takaisin lähtötilanteeseen. Toisaalta jos toteutus onnistuukin, haluat jakaa sen muille.

Käsitteet: branch, master, (feature-branch)

Tämä helpottuu ns. branching-ajattelulla, jonka Git tekee helpoksi. Sen sijaan, että toteutuskokeilun jälkeen vain peruuttaisit kaikki muutokset (jolloin menetät ne kokonaan), voit aloittaa toiminnallisuuden toteuttamisen omassa branchissaan (oksa tai haara). Luot oman branchin, joka ei vaikuta ns. masteriin (päähaara, johon kaikki muutokset oletusarvoisesti menee). Nyt voit omassa branchissasi tehdä muutoksia ja commitoida normaalisti. Jos toteutus onnistuu, voit liittää nämä commitit masteriin. Jos toteutus ei onnistu (tai muuten vaan haluat tehdä jotain muuta), niin valitset vain aktiiviseksi branchiksi masterin. Huom. voit myös jakaa oman branchisi muille. Näin muut pääsevät tarkastelemaan toteutustasi vaihtamalla heidän aktiivisen branchin sinun branchiksi. Tarkastelun jälkeen he voivat vaihtaa takaisin siihen branchiin, jossa olivat olleet aikaisemmin.

