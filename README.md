# Eesti Statistikaameti andmebaasi kasutamine Tableauga (Web Data Connector)

Tableau Web Data Connector (WDC) võimaldab ühenduda Eesti Statistikaameti andmebaasiga. Näidisrakenduse on kokku pannud Datafruit OÜ.

---
* Tableau WDC Eesti Statistikaameti API jaoks asub siin: [https://datafruit-public.github.io/statistikaamet.html](https://https://datafruit-public.github.io/statistikaamet.html)

## WDC kasutamine

#### Arvutis, kus on Tableau Desktop :desktop_computer:
1. Esilehelt -> Connect pane-> To a Server… > Web Data Connector.

![image alt text](https://github.com/datafruit-public/datafruit-public.github.io/blob/main/img/1.jpg)

2. Avanenud dialoogis sisesta järgmine URL: [https://datafruit-public.github.io/statistikaamet.html](https://datafruit-public.github.io/statistikaamet.html). Vajuta 'Enter'-klahvi.

![image alt text](https://github.com/datafruit-public/datafruit-public.github.io/blob/main/img/2.jpg)

3. Sisesta andmetabel ning mõõdik. Klõpsa "Get data"-nupul. Lisainfo [https://andmed.stat.ee/et/stat](https://andmed.stat.ee/et/stat). Juhul kui päring ei ole korrektne, siis Tableau veateadet ei kuva (Tableau jääb vastust ootama). Hetkel saab pärida andmeid, mis on esitatud **3 muutujaga**, kus var1=valdkond/omanikuliik, vms.; var2=mõõdik; var3=vaatlusperiood.

![image alt text](https://github.com/datafruit-public/datafruit-public.github.io/blob/main/img/3.jpg)

4. Andmed on nüüd laaditud Tableausse. Lohista andmemudelisse andmed.

![image alt text](https://github.com/datafruit-public/datafruit-public.github.io/blob/main/img/4.jpg)

5. Andmed on nüüd kasutamiseks ette valmistatud!

![image alt text](https://github.com/datafruit-public/datafruit-public.github.io/blob/main/img/5.jpg)

#### Nõuded
* Antud WDC vajab töötamiseks võrguühendust

Data flow:  Eesti Statistikaamet (REST API) <--> WDC (datafruit-public.github.io/statistikaamet) <--> Tableau Server/Desktop
* Andmed liiguvad Eesti Statistikaameti API-st otse Tableau Desktop/Server, Tableau Desktop/Server jaoks peab WDC (datafruit-public.github.io/statistikaamet) olema nähtav. 

###  Teadaolevad kitsaskohad
* Hetkel saab pärida andmeid, mis on esitatud **3 muutujaga**, kus var1=valdkond/omanikuliik, vms.; var2=mõõdik; var3=vaatlusperiood.
* Andmed laaditakse Tableausse stringidena (v.a mõõdiku väärtused), vajadusel tuleb andmetüüp manuaalselt korrigeerida (nt. vaatlusperiood andmestik).
* Statistikaameti API-le on seadistatud kasutamise piiranguid selles osas, kui palju päringuid ühelt ja samalt IP aadressilt teatud ajaühikus lubatakse.

### Tableau Web Data Connector
* Tableau juhend WDC-le [https://tableau.github.io/webdataconnector/docs/wdc_tutorial.html](https://tableau.github.io/webdataconnector/docs/wdc_tutorial.html)

## Viited
* [WDC näited](https://onlinehelp.tableau.com/current/pro/desktop/en-us/examples_web_data_connector.html )
* [WDC dokumentatsioon arendajale](http://tableau.github.io/webdataconnector/docs/)
* [Statistikaameti API juhend](https://andmed.stat.ee/abi/API-juhend.pdf)

## Arendus
* Kristian Allikmaa, kristian@datafruit.ee
* Soovid panustada arenduses? Suurepärane! Saada palun kiri: kristian@datafruit.ee.
* Leidsid vea :bug:? (https://github.com/datafruit-public/statistikaamet/issues)
