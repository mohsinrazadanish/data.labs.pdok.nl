---
layout: story
title: Krimpgebieden
logo: /stories/krimp/logo.jpg
endpoint: https://data.labs.pdok.nl/sparql
output: leaflet
---


# Wat weten we over Krimp?
Krimpregio's en Verstedelijking zijn onderwerpen die maatschappelijk vol in de schijnwerpers staan. Het is een complex vraagstuk. Begin november 2017 vond de CBS/Kadaster Datathon plaats waarin een team van data specialisten van Kadaster en CBS aan de slag zijn gegaan met Linked Data. Samen met datajournalisten Frédérik Ruys en Stephan Okhuijsen is het thema Krimp gekozen voor deze data story.

## Wat zijn de Krimpregio's?
De krimpregio's die we in Nederland kennen zijn:

<div data-query
  data-query-sparql="krimpregionamen.rq">
</div>


## Waar zijn de Krimpregio's?

Allereerst zijn we benieuwd welke krimpregio's we eigenlijk hebben in Nederland, en hoe zijn die over Nederland verdeelt? Het resultaat laat zien dat er 9 krimpgebieden zijn vooral aan de landsgrenzen.

<div data-query
  data-query-sparql="krimpregios.rq">
</div>

## Bevolkingsopbouw

Krimpregio's zijn gebieden waar het aantal inwoners lager wordt. Maar hoe ziet de bevolkingsopbouw eruit? Ook vergrijsd? En weinig jeugd is de verwachting?

<div data-query
  data-query-output="gchart"
  data-query-sparql="leeftijdscategorien.rq">
</div>


<div data-query
  data-query-sparql="leeftijdscatWijk.rq">
</div>

## Bevolkingsopbouw in vergelijking
Hoe is de verhouding over de verschillende leeftijdsgroepen in krimpgebieden versus heel Nederland?
We bekijken het aan de hand van één krimpregio. Deze krimpregio kan in de query eenvoudig aangepast worden.

<div data-query
  data-query-output="gchart"
  data-query-sparql="leeftijdscatKrimpVsNL.rq">
</div>


## Mobiliteit in krimpregio's

Hoe is de mobiliteit in een krimpregio? We zijn geïnteresseerd in de afstanden tot bijvoorbeeld de afstand tot de oprit van een hoofdweg, treinstations, kinderdagverblijf, supermarkt en hoeveelheid auto's per huishouden. Eerst nemen
we voor alle gemeenten de gemiddelde afstanden tot enkele voorzieningen:

<div data-query data-query-sparql="mobiliteit1.rq"></div>

Daarna vergelijken we de gemiddelde afstand tot voorzieningen per
krimpgemeente tot het landelijk gemiddelde (over alle gemeentes): ‘🠋’
betekent dat de afstand korter is dan gemiddeld; ‘🠉’ betekent dat de
afstand larger is dan gemiddeld.

<div data-query data-query-sparql="mobiliteit2.rq"></div>


## Werk
Dat brengt ons eigenlijk automatisch bij het thema werk. Welk deel van de beroepsbevolking heeft een baan?

<div data-query
  data-query-sparql="arbeidsparticipatieKrimp.rq">
</div>

Wat is over heel Nederland het minimale en maximale arbeidsparticipatiepercentage?

<div data-query
  data-query-output="table"
  data-query-sparql="rangeArbeidsparticipatie.rq">
</div>

Hoe komen de krimpregio's uit de bus, vergeleken met het Nederlands gemiddelde?

<div data-query
  data-query-sparql="thematischeKrimp.rq">
</div>

Wat is het beeld over heel Nederland van de arbeidsparticipatie?

<div data-query
  data-query-sparql="thematischeArbeidspNl.rq">
</div>



## Energiepotentieel

De wijken waar de grootste mogelijkheden liggen op het verbeteren van
het verlies van energie in de woning, liggen die in een krimpgebied of
niet; relevante informatie voor het beleid op subsidies, of voor het
slopen van woningen in krimpgebieden.

Het gemiddelde theoretische besparingspotentieel wordt per gemeente
gerekend.  Dit besparingspotentieel ligt tussen €25 en €1.900 per
jaar.  Hieronder vragen we de thematische kaart op, waar blauw/koud
een laag, en rood/warm een hoog besparingspotentieel aanduidt.  (In de
query zit een comment ‘<code>#</code>’ die, wanneer verwijdert, het
precieze bedrag voor iedere gemeente laat zien.)

<div data-query data-query-sparql="energiepotentieel1.rq">
</div>

Als we het besparingspotentieel alleen voor de krimpregio's laten
zien, krijgen we de volgende kaart:

<div data-query data-query-sparql="energiepotentieel2.rq">
</div>

## Tot slot

De data is rijk...in de CBS/Kadaster datathon zijn meerdere datasets
omgezet naar Linked Data, maar een parel is toch wel de Wijken en
Buurten 2016 dataset.  Op https://facetcheck.triply.cc/ is een eerste
versie van de BuurtBrowser beschikbaar op basis van deze dataset.
