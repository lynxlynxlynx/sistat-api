# SISTAT-API
### JSON API [podatkovnega portala SI-STAT](http://pxweb.stat.si/pxweb/dialog/statfile2.asp) Staističnega urada Republike Slovenije.

## About
Spletna aplikacija Statističnega urada Republike Slovenije SI-STAT, ki je razdeljena po tematskih področjih, omogoča iskanje in prenos objavljenih statističnih podatkov. Te je mogoče prikazati v tabeli ali prenesti v obliki različnih datotek (txt, csv, px, xls, htm).
SISTAT-API po zgledu [Eurostat-a](http://ec.europa.eu/eurostat/web/sdmx-web-services/rest-sdmx-2.1), omogoča prenos podatkov preko spletne aplikacije SI-STAT v JSON-STAT formatu. Več o formatu najdete na tej povezavi: [https://json-stat.org](https://json-stat.org).

## Uporaba
1. Na spletni strani [aplikacije SI-STAT](http://pxweb.stat.si/pxweb/dialog/statfile2.asp) poiščete področje in sklop podatkov, ki jih želite uporabiti.
2. Sestavite API klic:
    * __URL__ - [http://sistat.sebenik.com/](http://sistat.sebenik.com/)
    * __GET parametri:__
      * __ma__ - parameter, katerega vrednost najdete v spletnem naslovu izbranega sklopa podatkov (obvezen parameter)
      * __path__ - parameter, katerega vrednost najdete v spletnem naslovu izbranega sklopa podatkov (obvezen parameter)
      * __dimenzija*__ - parametri s katerimi označimo izbrane dimenzije in vrednosti v tabelah. Ime parametra pišemo z malimi črkami, presledke pa nadomestimo s podčrtajem '\_'. Vrednosti posameznega parametra pišemo kakor so prikazane v tabelah na spletni strani. V primru izbire večjega števila vrednosti posamezne dimenzije, le te ločimo z vejico ','. Če želimo izbrati vse vrednosti posamezne dimenzije lahko namesto naševanja vseh, za vrednost dimenzije napišemo _'all'_, če želimo izbrati zgolj prvo vrednost dimenzije lahko napišemo _'first'_ ali _'last'_, če želimo izbrati zgolj zadnjo vrednost dimenzije. (Glej primer.)
3. Struktura odgovora je v [JSON-STAT](https://json-stat.org) formatu. Vsebuje naslednja polja:
    * __version__ - označuje vezijo JSON-STAT formata ([ref](https://json-stat.org/format/#version))
    * __class__ - označuje razred odgovora. Odgovor SISTAT-API-ja je vedno dazreda 'dataset' ([ref](https://json-stat.org/format/#class))

## Primeri

## Licenca

## Avtor
Žiga Šebenik [ziga@sebenik.com](mailto:ziga@sebenik.com)
