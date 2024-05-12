# Analýza ... medzi členmi kongresu Spojených štátov Amerických
```
Veda o sieťach, 2024
Roderik Antol, Tomáš Belák, Adam Lopaška, František Václav Man
```

## Popis siete
Naša sieť popisuje rečnícke prejavy politikov Kongresu Spojených štátov. V sieti máme 219 kongresmanov (vrcholov) a 764 hrán - spomenutí iného kongresmana vo svojom prejave. Hrany sú orientované, váhované a graf obsahuje násobné hrany a slučky. Váha hrany závisí od charakteru spomenutia - kladné spomenutie/súhlas má váhu `1` a negatívne spomenutie/nesúhlas má váhu `-1`. 

<!Naša sieť obsahuje 219 vrcholov - členov kongresu. Hrany reprezentujú, či a ako sa spomínajú vo svojich rečiach. Hrany sú orientované a ováhované. Orientácia je samozrejmá, kongresman A spomína kongresmana B. Váha hrany môže byť kladná - vo svojej reči podporuje kongresmana B alebo záporná - oponuje mu/nesúhlasí s ním. Sieť môže obsahovať násobné hrany - niekoho môžem spomenúť viackrát, a slučky - spomínam sám seba. Všetkých hrán je 764.>

![Vizualizácia celej siete. Červené hrany majú negatívnu váhu, zelené váhy pozitívnu.](images/net.png)

## Výskumná otázka 1: štruktúra siete a detekcia komunít
Priemerný stupeň vrcholov siete je `6.98`. Teda za sledované obdobie, jeden kongresman vo svojich rečiach spomenie skoro 7 ďalších kongresmanov. 

Našu sieť sme si rozdelil na dve podsiete, podľa váh na hranách. Takto sme dostali dve nové siete, ktoré môžeme vidieť nižšie na grafe. Vľavo je sieť zložená z kladných hrán, vpravo zo záporných hrán. V prvom riadku sú obe siete s rovnakým rozložením vrcholov, a v druhom riadku sú vrcholy usporiadané tak, aby susediace vrcholy blízko seba.

![](images/subnets.png)

Vlastnosti podsietí:
|                  | Kladná sieť | Záporná sieť |
|------------------|-------------|--------------|
| Modularita       | 0.609       |  0.72        |
| Hustota          | 0.019       |  0.023       |
| Priemerný stupeň | 3.925       |  2.206       |
| Počet komunít    | 8           | 13           |

## Výskumná otázka 2: analýza centralít

## Výskumná otázka 3: analýza "selfmentions"

## Výskumná otázka 4:

## Záver

## Zdroje/citácie
```
@MISC{konect:2018:convote,
    title = {Congress votes network dataset -- {KONECT}},
    month = jan,
    year = {2018},
    url = {http://konect.cc/networks/convote}
}

@inproceedings{konect:convote,
	author = {Matt Thomas and Bo Pang and Lillian Lee},
	title = {Get the Out Vote: Determining Support or Opposition from
                  Congressional Floor-Debate Transcripts},  
	booktitle = {Proc. Conf. on Empir. Methods in Nat. Lang. Process.},
	pages = {327--335},
	year = {2006},
}

@inproceedings{konect:convote,
	author = {Matt Thomas and Bo Pang and Lillian Lee},
	title = {Get the Out Vote: Determining Support or Opposition from
                  Congressional Floor-Debate Transcripts},  
	booktitle = {Proc. Conf. on Empir. Methods in Nat. Lang. Process.},
	pages = {327--335},
	year = {2006},
}


@inproceedings{konect,
	title = {{KONECT} -- {The} {Koblenz} {Network} {Collection}},
	author = {Jérôme Kunegis},
	year = {2013},
	booktitle = {Proc. Int. Conf. on World Wide Web Companion},
	pages = {1343--1350},
	url = {http://dl.acm.org/citation.cfm?id=2488173},
	url_presentation = {https://www.slideshare.net/kunegis/presentationwow},
	url_web = {http://konect.cc/},
	url_citations = {https://scholar.google.com/scholar?cites=7174338004474749050},
}

@inproceedings{konect,
	title = {{KONECT} -- {The} {Koblenz} {Network} {Collection}},
	author = {Jérôme Kunegis},
	year = {2013},
	booktitle = {Proc. Int. Conf. on World Wide Web Companion},
	pages = {1343--1350},
	url = {http://dl.acm.org/citation.cfm?id=2488173},
	url_presentation = {https://www.slideshare.net/kunegis/presentationwow},
	url_web = {http://konect.cc/},
	url_citations = {https://scholar.google.com/scholar?cites=7174338004474749050},
}
```