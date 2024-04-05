# a) OverTheWire

## Level 0

Avasin terminaalin ja otin ssh yhteyden sivuun bandit.labs.overthewire.org ja porttiin 2220 käyttäjällä bandit0.

![eka](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/f8c35e37-d80a-4bdc-9adb-85f3309713fd)

Sivu kysyi salasanaa ja annoin bandit0, joka kerrottiin Overthewire sivun ohjeissa. Pääsin sisään

![toka](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/3a0a14a2-fe65-4246-ad68-edcdf9ad9703)

## Level 1

Ohjeissa kerrottiin salasanan olevan readme tiedostossa. Annoin ls komennon ja löysin kyseisen tiedoston. Avasin tiedoston cat komennolla ja salasana ilmestyi.

![kolmas](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/98787ed5-f98b-4f62-b343-9b3880ed8ec0)

Annoin exit komennon ja kirjauduin ulos, otin yhteyden bandit1 ja annoin äsken löytämäni salasanan ja pääsin sisälle bandit1.

![nelj](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/4f472d32-fdc1-46b7-a0db-c5eab582047b)

![vis](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/02ecdff9-1937-4828-850e-14521a34bc2b)

Annoin taas ls komennon ja löysin tiedoston -, koska cat komento ei toiminut annoin ./- komennon ja se avasi tiedoston ja löysin salasanan jolla pääsen level 2.

![ku](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/a6fc7f36-ce62-4c76-94e6-c19ee87e38e4)

![se](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/93677efd-3c03-4d1a-ab91-981cfa099cff)

# b) Asenna webgoat

Ensiksi asensin javan ja enabloin muurin.

![asjava](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/e0a22fe5-53e0-408d-be07-04ab0c02adee)

![tuli](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/70cbcf5c-f2c8-4c3d-af66-72edce4cce50)

Seuraavaksi latasin ja ajoin Webgoatin

![webgoat](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/d318fbe6-5f9f-46bc-bf0d-c7b18442c370)

Menin selaimessa Webgoatin sivulle http://localhost:8080/WebGoat/ ja rekistöröidyin sinne ja sain luotua käyttäjän.

![rekk](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/791201b3-6b07-4293-80e3-9b0d12ed9ea6)

![sisä](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/fe319bde-09f5-4f26-a6bd-23437d22d0cb)

# c) http basics ja developer tools

## HTTP Basics

Aloitin HTTP basics tehtävän, luen ensimmäisen sivun ja siirryin toiselle sivulle ja syötin nimeni. Se kääntyi väärin päin.

![jo](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/d692a195-b9e8-4e2c-abfa-fbd0929a2650)

Menin seuraavaan tehtävään ja HTTP komento oli POST ja klikkasin sivua oikella hiiren näppäimellä ja valitsi inspect, näin aukesi developer tools. Siellä käytin hakusanaa magic ja löysin magic number kohdan ja sieltä numeron 78.

![lop](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/9f681a58-0223-43b4-b147-0c25796a1c9b)

## Developer tools

Luin tietoa developer toolsista ja pääsin ensimmäiseen tehtävään. Siinä piti avata developer tools ja käyttää konsolia. kirjoitin konsoliin komennon webgoat.customjs.phoneHome() ja sain vastaukseen oikean numeron.

![numero](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/9ff71234-48b6-4398-8fc8-ea8c8251e47d)

Seuraavaksi luin lisää tietoa developer toolsin eri valikoista. Menin network tabiin ja painoin go painiketta. Feediin ilmestyi paketteja ja valitsin niistä ensímmäisen joka oli POST tyyppinen. Selailin sitä läpi ja kohdassa Request törmäsin numeroon, jonka syötin tehtävän vastauskenttään ja tehtävä meni oikein.

![oik](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/d362a615-9658-4a3e-9ea7-566ccd86607c)

# d) Portswigger

Menin Portswigger sivustolle https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data ja rekistöröidyin sivustolle ja pääsin labiin sisään. Labissa pitää muokata sivuston osoitekenttää ja ottaa selvää löytyykö sivulta piilotettua dataa. Klikkasin accessories kategoriaa ja osoitekenttä muuttui tällaiseksi https://0a2a00bc04bded8d80017bef00770059.web-security-academy.net/filter?category=Accessories. Poistin Accessories kohdan ja lisäsin siihen annetun tiedon '+OR+1=1-- ja huomasin, että sivustolle ilmestyi enemmän tuotteita kuin siinä oli kategoriassa kaikki. Tällä sain 8 tuotetta lisää näkyviin. 

![Screenshot_2024-04-05_13-17-54](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/cb34a370-8d51-4e90-bd2e-e0b20cd60dc6)

# e) Virtuaalikone

Asensin vagrantilla linuxin ja kirjauduin siihen sisään ja asensin nmapin.

![vkone](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/bd8623e2-3162-443f-bb0d-838e1365e09c)

![sisä](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/af21a4f6-930c-4316-ae87-03888c323142)

![nmap](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/6a02c45b-1cf7-4016-8d44-181df3481c3a)

# f) Porttiskannaa 1000 porttia

Käytin hostname -i komenota selvittääkseni koneenin osoitteen, tämän jälkeen porttiskannasin portit 1-1000 omalta koneeltani ja huomasin, että portti 22 on auki ssh varten ja loput suljettu.

![Screenshot_2024-04-05_14-15-31](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/a8e6149e-42aa-465a-997a-67ea272d7e11)

# g) Porttiskannaa kaikki portit

Seuraavaksi skannasin koneeni kaikki portit. Huomasin että se tosiaan kävi läpi kaikki olemassa olevat portit joita oli noin 65 000. Lopputulos ei muuttunut vaan edelleen portti 22 on auki ssh varten.

![kaik](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/a6946e8e-055b-4c10-8d34-21504f398552)

# h) nmap -A

nmap -A komento tekee porttiskannauksen lisäksi sen, että se kertoo kohteen käytössä olevan käyttöjärjestelmän.

![A](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/e98d98e6-a033-4b80-9d6b-b892148af6e7)

# i) Apache

Asensin apache2 serverin ja ajoin nmap -A komennon uudelleen. Huomasin nyt että apache serveri oli ilmestynyt tulosteeseen. Se käyttää porttia 80 http varten.

![asen](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/74d768dc-914a-45b4-94cc-89a8893282a4)

![näk](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/d451db85-8bc5-4edb-9f5c-864eab058d07)

# k) overthewire level 2-10

## Level 2

Otin ssh yhteyden bandit2, annoin löytämäni salasanan ja pääsin sisälle, ls komennolla sain esiin tiedoston spaces in this directory, se ei auennut pelkällä cat komennolla, sain sen auki lisää mällä "" siihen. Sain level 3 salasanan

![3](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/b7ce3b9b-98ce-47f4-99ce-70621278ab77)

## Level 3

Otin ssh yhteyden bandit3, annoin äsken löytämäni salasanan ja pääsin sisään, ls komennolla sain esiin inhere kansion, menin cd:llä sisään ja ls -a komennolla sain esiin piilotetut tiedostot. Sain level 4 salasanan.

![4](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/a7882462-1f42-4663-8c87-1a61efc3b44c)

## Level 4

Otin ssh yhteyden bandit4, annoin äsken löytämäni salasanan ja pääsin sisään, ls komennolla sain esiin inhere kansion, menin cd:llä sisään ja ls komennolla sain esiin aivan liia paljon kansioita käydäkseni ne manuaalisesti läpi, kun niissä oli vielä sisällä monia tiedostoja, joten käytin komentoa  . Sain level 5 salasanan.

![5](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/9958ff89-9762-4e13-a42e-3d08008b8c5d)

## Level 5

Otin ssh yhteyden bandit5, annoin äsken löytämäni salasanan ja pääsin sisään, ls komennolla sain esiin inhere kansion, menin cd:llä sisään ja ls komennolla sain esiin monia aivan liian monia kansioita joiden sisällä oli taas lisää tiedostoja, näitä olisi aivan mahdoton käydä manuaalisti läpi, joten ajoin komennon find . -readable -size 1033c ! -executable ja sieltä paljastui kansio ja tiedosto joka vastasi juuri määrittelemiäni kriteerejä, eli maybehere07 kansio ja sieltä tiedosto file2, käytin cat maybehere07/.file2 komentoa ja sain level 6 salasanan.

![oik](https://github.com/JoonasKal/Tunkeutumistestaus/assets/104196551/ba1ec4e2-ceae-4667-a2d8-f837ddb53820)


# Lähteet: 

https://overthewire.org/wargames/bandit/bandit0.html Luettu 5.4.2024

https://terokarvinen.com/2024/eettinen-hakkerointi-2024/ Luettu 5.4.2024

https://terokarvinen.com/2020/install-webgoat-web-pentest-practice-target/ Luettu 5.4.2024

https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data Luettu 5.4.2024
