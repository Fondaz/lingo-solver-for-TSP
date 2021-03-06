# lingo-solver-for-TSP
Lingo script for solving an example of [Travelling Salesman Problem](https://en.wikipedia.org/wiki/Travelling_salesman_problem) using the Constraints Generation exact method.

~~A Java implementation for this problem using NN and Christofides (heuristic techniques) is HERE.~~

## Index
1. [Contents of the Repository](https://github.com/Fondaz/lingo-solver-for-TSP#contents-of-the-repository)
2. [How To Run It](https://github.com/Fondaz/lingo-solver-for-TSP#how-to-run-it)
3. [The Excel File](https://github.com/Fondaz/lingo-solver-for-TSP#the-excel-file)
4. [The Example](https://github.com/Fondaz/lingo-solver-for-TSP#the-example)


## Contents of the Repository
1. `STSP Generazione Dei Vincoli (Solution Report).lgr` - Output of the script.
2. `STSP Generazione Dei Vincoli (Solution Report).txt` - Output of the script.
3. `STSP Generazione Dei Vincoli.lg4` 	                - The Lingo program.
4. `STSP.xlsx`                                          - The Excel file used for input and output.

[![Back To Top](https://user-images.githubusercontent.com/11947833/33139581-fed0ece6-cfad-11e7-8147-cf4f3b3cd34a.png)](https://github.com/Fondaz/lingo-solver-for-TSP#lingo-solver-for-tsp)

## How To Run It
1. Download the repository.
2. Run the lingo file `STSP Generazione Dei Vincoli.lg4`.
3. The result can be found in `STSP.xlsx`.

[![Back To Top](https://user-images.githubusercontent.com/11947833/33139581-fed0ece6-cfad-11e7-8147-cf4f3b3cd34a.png)](https://github.com/Fondaz/lingo-solver-for-TSP#lingo-solver-for-tsp)

## The Excel File
This file cointans 6 tables: 2 for input, 3 for output, 1 for info.
* [input] *\"Larghezza di banda tra le città (Mb/s)\"* = \"Band width between the cities (Mb/s)\".
* [input] *\"Tempo di trasmissione (ms)\"* = \"Transmission Time(ms)\" (calcolated from the table above).
* [output] *no name* = the routes between cities chosen by the algorithm.
* [output] *\"Funzione Obiettivo\"* = \"Goal Function\".
* [output] *\"Ordine di visita delle città\"* = \"Visit order of the cities\".
* [info] *\"Distanza fra Città (km)\"* = \"Distance between Cities (km)\".

La tabella \"Band width between the cities\" contiene la capacità massima della linea nel tratto che va dalla città nella riga a quella nella colonna. Questi dati vengono utilizzati per il calcolo del tempo di trasmissione da città a città (2° tabella). La formula utilizzata è MTU/(\"larghezza di banda\"\*1000). MTU, cioè Maximum Transmission Unit, è la dimensione massima in byte di un pacchetto dati che può essere inviato attraverso un protocollo di comunicazione in una rete di telecomunicazioni. Questa tabella verrà quindi utilizzata come input dal solver lingo per dare un peso a ciascun ramo del grafo.

Una volta terminato il programma, la soluzione (il costo minimo per compiere un ciclo) verrà stampata nella cella \"Goal Function\". In output si troveranno anche una tabella binaria con gli 1 in corrispondenza del percorso scelto (riga->colonna) e una tabella con una sola riga (\"Visit order of the cities\"), con la lista delle città e un numero da 1 a 11 che indica l'ordine con cui quelle città sono state visitate.

La tabella \"Distance between Cities (km)\" è stata utile per stimare la topografia della regione.


![WorkInProgress](https://spiegareSignificatoTabelle)

[![Back To Top](https://user-images.githubusercontent.com/11947833/33139581-fed0ece6-cfad-11e7-8147-cf4f3b3cd34a.png)](https://github.com/Fondaz/lingo-solver-for-TSP#lingo-solver-for-tsp)


## The Example

![WorkInProgress](https://spiegareIlProblemaDescrivendolo.pnghttps://help.github.com/articles/basic-writing-and-formatting-syntax/#headings)
[![Back To Top](https://user-images.githubusercontent.com/11947833/33139581-fed0ece6-cfad-11e7-8147-cf4f3b3cd34a.png)](https://github.com/Fondaz/lingo-solver-for-TSP#lingo-solver-for-tsp)
