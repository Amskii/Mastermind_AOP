# Mastermind_AOP

Aihe C Peli: Mastermind

Säännöt: Pelissä on koodintekijä ja koodinmurtaja. Koodintekijän tehtävä on valita neljä värillistä nappia, jotka laitetaan tiettyyn järjestykseen. Värit ja niiden järjestys on koodinmurtajalta salainen tieto. Koodinmurtajan tehtävä on yksi arvaus kerrallaan arvata oikeat värit ja niiden oikea järjestys. JOkaisella arvauksella koodinmurtaja saa koodintekijältä tiedon, kuinka monta koodinmurtajan valitsemista väreistä on oikein ja moniko niistä on oikealla paikalla. Tämä ilmaistaan mustilla ja valkoisilla pienillä napeilla. Jokaista oikeassa paikassa olevaa oikeaa värillistä nappia kohden, koodinmurtaja saa mustan pikkunapin. Jokaista oikean väristä, mutta väärässä paikassa olevaa värillistä nappia kohden, koodinmurtaja saa valkoisen pikkunapin.

Ratkaisuperiaate: Koodintekijän koodia verrataan koodinmurtajan arvaukseen. Ensiksi katsotaan, onko ratkaisu täysin sama. Jos ei, niin nappeja verrataan järjestyksessä koodinmurtajan arvaukseen. Ensiksi katsotaan ovatko sekä sijanti että väri oikein, ja jos löytyy sama, arvaus merkataan tarkastetuksi. Jos sama väri löytyy samasta indeksistä, annetaan musta pikkunappi merkiksi oikeasta sijainnista. Tämän jälkeen arvaus merkitään läpikäydyksi, eli Nappi-olean boolean-tyyppinen muttuuja "tarkastettu" vaihdetaan "true". Jos sijainti ei ole oikea, verrataan muihin arvauksen indekseihin, jos vastaavuus löytyy, annetaan valkoinen pikkunappi ja merkataan arvaus läpikäydyksi, samalla boolean-metodilla.

Kun koodimurtaja tekee arvauksen, hän syöttää värejä joista tehdään Nappi-olioita. Jokaista Nappi-oliota luodessa tarkastetaan, että väri on hyväksyttävä. Neljän hyväksytyn värin jälkeen niitä vastaavat neljä Nappi-oliota muodostavat neljästä Nappi-oliosta koostuvan Rivi-olion. Tämän jälkeen kutsutaan metodia, joka vertaa Rivi-tyyppistä ratkaisua viimeisimpään arvaukseen, ja palauttaa kaksialkoisen kokonaislukulistan, joista ensimmäinen merkitsee mustien nappien määrää ja toinen valkoisten nappien määrää. Kun saadaan vihje, tarkistetaan onko se neljä mustaa ja nolla valkoista (eli ratkaisu ja arvaus täsmäävät), jos on niin peli päättyy. Jos ei, pyydetään syöttämään uusi arvaus tiettyyn ylärajaan asti. Jos yläraja tulee täyteen, eikä oikeaa ratkaisua ole tullut, peli päättyy koodinmurtajan häviöön.
Erilliset tiedostot sekä ohjelman tilan tallentamiseen, high score-listan sekä ajan että arvausten määrän tallentamiseen, sekä arvausten tallentamiseen. Ajanotto: joko pelin alussa lähtee laskuri käyntiin, johon lisätään sekunnin välein aikaa, tai sitten lasketaan erotus tietokoneen kellonajoista pelin alussa ja lopussa.
Vaikeusasteen valinta: Pelin alussa voi valita pelin vaikeustason esim. kolmesta vaihtoehdosta, joilla tulee eri määrä nappeja ja eri määrä värivaihtoja niille.
Virheenmahdollisuus: Etenkin kohdassa, jossa koodinmurtaja syöttää arvauksen, tulee laittaa try-catcheja virheistä palautumiseksi. Ohjelma voisi tallentaa koko ajan ohjelman tilaa tiedostoon, ja jos ohjelman sulkee, sitä pystyy jatkamaan edellisestä tilasta.

Oliot ja niiden muuttujat:
Nappi - enum Vari; boolean Tarkastettu
Rivi - ArrayList Nappi-olioita, joihin kiinnitetty myös tieto siitä, mitkä vihjeet se sai vertailussa

Metodit:
Ratkaisun ja arvauksen vertailumetodi
