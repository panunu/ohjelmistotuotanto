# Laatu: tekniikat, konventiot, suunnittelumallit

Miksi ja miten tehdä siedettävää koodia, jota muutkin pystyvät ymmärtämään, eikä se hajoa käsiin? Kannattaa aloittaa pohdiskelu Uncle Bobin kohta jo 10 vuotta vanhalla, mutta silti pätevällä [vinkillä](http://www.artima.com/weblogs/viewpost.jsp?thread=51769).

## Miksi

- design debt
- luet enemmän kuin kirjoitat
- laatu
- ongelmat

Legacyn määritelmä?

- tasapainottelu vanhan järjestelmän refaktoroinnin kanssa

## Code smells


> Any fool can write code that a computer can understand. Good programmers write code that humans can understand. - Martin Fowler

- hajuisa koodi
http://www.codinghorror.com/blog/2006/05/code-smells.html

- nimeäminen
- pitkät metodit
- copy-pasta koodi

> When you feel the need to write a comment, first try to refactor the code so that any comment becomes unnecessary. - Martin Fowler 

- varo överinoudattamista!

Kuinka kirjoittaa huonoa koodia: http://thc.org/root/phun/unmaintain.html

## Suunnittelumalleja, standardeja ja konventioita

### DRY

### Partiolaissääntö (Boyscout Rule)

### PSR-0, -1 ja -2

Samoja Java-maailmassa?

### Single Responsibility Principle

### MVC

### Dependency Injection

### Domain-driven design



## Työskentelymetodit ja -tekniikat

### Craftmanship

### Pariohjelmointi (Pair programming)

### Pomodoro-tekniikka

### TDD 

Painotus design-puolelle.

### Koodin katselmointi (Code review)

> "A good developer should always want another dev to read his code, because that makes it possible for at least one of them to learn something" - Mario Fusco

Koodin katselmointi on hyvä tapa oppia. Katselmoinnilla voi yhtenäistää käytännöt nopeasti, joka on erityisen hyödyllistä varsinkin jos olette aloittaneet  projektin uudella ryhmällä. Katselmointi voi kuulua osaksi arkipäivän rutiinia (esim. Pull Requestien yhteydessä), tai tiimi voi varata katselmoinnille kiinteän yhteisen ajan. Katselmointia voi hyödyntää esimerkiksi siinä tapauksessa, kun haluaa kuulla mielipiteen toteutuksesta (kun vaikka tehdään hyvin olennaista tai laajaa toiminnallisuutta).

[http://www.codinghorror.com/blog/2006/01/code-reviews-just-do-it.html](http://www.codinghorror.com/blog/2006/01/code-reviews-just-do-it.html)
