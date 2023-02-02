# Hello_Web

## Apache esimerkkisivu

Ennen kuin hyökkäsin päivittelemään esimerkkisivun sisältöä, lähdin päivittämään terminaalin kautta sisältöä ajantasalle. 
      $ sudo apt-get update
![Päivitys](https://user-images.githubusercontent.com/100162043/216265975-f4a06a91-4ad1-4e56-a982-0ea9bb22ef27.jpg)

Päivittelyn jälkeen lähdin muodostamaan esimerkkisivulle muutoksia. Tein alkuperäisen ohjeen mukaan ensin lisäämällä tekstin "Moi" sivustolle. 

      $ echo "Moi"|sudo tee /var/www/html/index.html
      
![Moi](https://user-images.githubusercontent.com/100162043/216267228-9bdb38ab-58df-4adb-93a5-d4f0d5935359.jpg)
![Moi localhost](https://user-images.githubusercontent.com/100162043/216267409-43802f85-0f62-4041-968e-022737c15a24.jpg)

Muutoksen tein samalla tavalla, mutta vaihdoin sisältöä. 

        $ echo "h5"|sudo tee /var/www/html/index.html
        
![h5](https://user-images.githubusercontent.com/100162043/216267611-0c51f288-8787-41ad-bb46-e56841f5a008.jpg)
![h5 localhost](https://user-images.githubusercontent.com/100162043/216267626-0bfdb76a-ebf6-4037-bd27-56bf7cb8bd07.jpg)

## Kotisivut toimimaan

Viime luennolla asiaa puitiinkin jo läpi, joten seuraavat komennot eivät ole uusia ja näissä ilmenikin olemassa olo ilmoituksia. 

![Curl](https://user-images.githubusercontent.com/100162043/216270108-76f364f1-b974-40ae-814a-e77d55a403ed.jpg)
![Indexmarkus](https://user-images.githubusercontent.com/100162043/216270145-bc3d4bd8-c208-46b1-8f84-d2e6cb2d93f0.jpg)

## Uusi käyttäjä

Tässä kohtaa joutuikin sitten etenemään tehtävänannon Vinkit kohtaan, josta löytyikin ohjeistusta kuinka lähdetään tuota uutta käyttäjää luomaan. Lähdin kirjaimellisesti vinkin mukaan luomaan tätä. 

        $ sudo adduser erkki
        
Tämän jälkeen täytin Erkille tiedot luontia varten ja lopuksi painoin Y. 

![Erikkiesimerkki](https://user-images.githubusercontent.com/100162043/216270830-93795dc0-a1ff-495e-a24f-be8cc4581ca2.jpg)

Kirjautuminen onnistuu joko perinteisesti painamalla Application välilehdestä Logout ja kirjautumalla erkin tiedoilla sisään, tai käyttämällä terminaalissa komentoa: 

        $ su erkki

![Kirjautuminen toisella käyttäjällä](https://user-images.githubusercontent.com/100162043/216271546-5a84a1d7-6e29-4baf-a88a-e492a04ace31.jpg)

Aloitan tekemällä myös Erkin käyttäjällä päivitykset. 

        $ sudo apt-get update
        
Tässä kohtaa huomasin, että Erkin käyttäjällä ei ole oikeuksia. 

![Erkillä ei oikeuksia](https://user-images.githubusercontent.com/100162043/216274295-4565866c-d91f-4cfb-b51d-01603e4d677c.jpg)

Tässä vaiheessa kirjauduin takaisin omalle käyttäjälle

        $ su markus

Ja asetin oikeudet Erkille seuraavalla komennolla ja samalla kirjauduin takaisin erkin käyttäjälle. 

        $ sudo adduser erkki sudo
        
![Erkille oikeudet kuntoon](https://user-images.githubusercontent.com/100162043/216274772-348b9b9d-ee22-4056-8204-42eb5694d38c.jpg)

Nyt kokeilen uudestaan päivittää erkin käyttäjällä ja huomaan että päivitys onnistuu. 

![Erkin onnistunut päivitys](https://user-images.githubusercontent.com/100162043/216275512-00989ff0-63df-47dc-94f4-7a3db24c0d1c.jpg)

Tässä vaiheessa teen täysin samalla tavalla kotisivujen luonnin kuten markus käyttäjälle alunperin. 

![erkki html](https://user-images.githubusercontent.com/100162043/216275952-cb7f286d-adf9-4b6e-8664-b3c7d099c43c.jpg)
![Erkin omat sivut](https://user-images.githubusercontent.com/100162043/216275995-8d35899e-bf0f-43a6-861f-3f3848396908.jpg)

Nyt toimii Erkin omat sivut!

## HTML5

Tätä osuutta varten lähdin googlettelemaan kuinka muokkailaan apachen kautta kotisivut. Sisällöllä ei ollut niinkään väliä, kunhan sain luotua tekstiä. Löysin lopulta youtube videon, jonka avulla loin seuraavalla tavalla seuraavan näköisen niin sanotun tervetuloa sivun. 

        $ sudo nano /var/www/html/index.html
        
![sudonano](https://user-images.githubusercontent.com/100162043/216277384-f3a46891-cdd6-4024-ad9b-545f14043eaa.jpg)

Komennon ja salasanan syötettyä aukesi seuraavanlainen ikkuna.

![Nano näkymä](https://user-images.githubusercontent.com/100162043/216277655-65828406-ed17-4640-bae7-ad6597ddbffc.jpg)

Tämän jälkeen täytin kuvan mukaisesti tekstikenttiin html pohjan ja loin tekstin sivustolle. 

![html sisältö](https://user-images.githubusercontent.com/100162043/216277711-28fbb5ca-42e5-46ab-8662-4e01bcca291a.jpg)

Syötettyäni päivitin selaimen localhost sivuston ja sain seuraavan tiedon sivustolle näkyviin. 

![Helloweb h5](https://user-images.githubusercontent.com/100162043/216277879-331fa41c-0115-409a-8c33-4e20ab6fcedf.jpg)

Lähteet: 
https://terokarvinen.com/
https://www.youtube.com/watch?v=YSSIm0g00m4
https://www.youtube.com/watch?v=_uZjqSyLWQM
Google


