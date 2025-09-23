
## Radici di equazioni non lineari

Data una funzione non lineare arbitraria che può anche essere un polinomio , possiamo trovare le **radici** 
-Definizione: quei valori , se esistono , per cui la funzione si annulla, anche detti zeri

Esempio : consideriamo f(x) funzione definita su un intervallo I della retta reale, quindi una **funzione reale di variabile reale** 
-Definizione : funzione che lavora con valori reali , che la variabile di input è anchì essa reale

L' obiettivo è determinare un valore alfa ( simbolo alfa ) dell' insieme I tale che f(alfa) = 0

Casi che possono accadere  se cerchiamo di trovare gli zeri :
-Non intersecano mai l' asse reale ( o asse x) quindi non possono esistere degli zeri (funzioni non lineari )

-La funzione ha più radici  (come nel caso di un polinomio di secondo grado con due soluzioni reali) 

-La funzione ha una sola soluzione nell' intervallo I (non esclude che possa avere altri zeri all' infuori dell' intervallo)


Soluzione per trovare gli zeri :
generare una successione di numeri reali X tale che al tendere di k all' infinito , il suo limite sia uguale ad alfa (il teorico zero della funzione)

Forma chiusa di un equazione : Una **forma chiusa** è una **formula finita e calcolabile**, scritta con **operazioni note**, **senza iterazioni** o **approssimazioni** ( esempio annotazioni infinite ) .

## Teorema degli zeri delle funzioni continue

Funzione continua: Una **funzione è continua** in un punto se **non ha "salti", "buchi" o "interruzioni"** in quel punto.



Parlando sempre nell' insieme reale:

Questo teorema afferma che, se una funzione 𝑓(𝑥) è continua in un intervallo chiuso [𝑎, 𝑏] e assume valori di segno opposto agli estremi, ovvero 𝑓(𝑎)𝑓(𝑏) < 0 allora esiste almeno un valore 𝛼 appartenente all’intervallo aperto (𝑎, 𝑏) tale che 𝑓(𝛼) = 0

In termini intuitivi, il teorema garantisce che, se 𝑓(𝑥) è continua e cambia segno tra [𝑎, 𝑏], allora deve necessariamente annullarsi almeno una volta all’interno dell’intervallo

## Metodo di bisezione

Consideriamo una funzione continua arbitraria 𝑓(𝑥) definita in maniera continua su un intervallo [𝑎, 𝑏], in cui avviene un cambio di segno, ovvero 𝑓(𝑎)𝑓(𝑏) < 0. Poniamo 𝑎1 = 𝑎 e 𝑏1 = 𝑏, ovvero consideriamo l'intero intervallo dato.
In questo modo stiamo inizializzando il nostro algoritmo prendendo gli estremi dell'intervallo. 
Introduciamo ora il punto medio dell’intervallo: 
𝑐1 = 𝑎1 + 𝑏1  / 2 .
Valutiamo qual è il segno di 𝑓(𝑐1 ), 𝑓(𝑎1 ) e 𝑓(𝑏1 ). 

Dopo aver valutato i segni di 𝑓(𝑐1 ), 𝑓(𝑎1 ) e 𝑓(𝑏1 ), scegliamo in maniera opportuna se restringere la ricerca della radice della funzione 𝑓 tra [𝑎1, 𝑐1] oppure tra [𝑐1, 𝑏1]. 
Supponiamo, ad esempio, che 𝑓(𝑎1 ) < 0 e 𝑓(𝑏1 ) > 0. Se 𝑓(𝑐1 ) > 0, questo significa che il cambio di segno avviene nell’intervallo (𝑎1, 𝑐1), quindi la radice 𝛼 si trova in questo sotto intervallo (𝑎1, 𝑐1). Restringiamo allora la ricerca della radice tra (𝑎1, 𝑐1) (caso A). Se invece 𝑓(𝑐1 ) < 0 (e quindi ha lo stesso segno di 𝑓(𝑎1 ) < 0), allora il cambio di segno avviene nell’intervallo (𝑐1, 𝑏1) (caso B). 
Supponendo di essere nel caso A, poniamo 𝑎2 = 𝑎1 e 𝑏2 = 𝑐1. Nel caso B, ovvero se ovvero 𝑓(𝑐1 )𝑓(𝑏1 ) < 0, la radice si trova tra (𝑐1, 𝑏1). In questo caso B, aggiorniamo gli estremi ponendo 𝑎2 = 𝑐1 e 𝑏2 = 𝑏1 e restringiamo la ricerca della zero all'intervallo (𝑐1, 𝑏1 ). Senza perdere di generalità, soffermiamoci sul caso B, e continuiamo ad applicare la formula di bisezione aggiornando l’intervallo e calcolando il nuovo punto medio 𝑐2 = 𝑎2 + 𝑏2 /  2 , che divide l’intervallo (𝑐1, 𝑏1 ) in due sotto intervalli (𝑐1, 𝑐2] ∪ [𝑐2, 𝑏1 ).
Continuiamo col processo di selezione del metodo di bisezione, aggiornando l’intervallo di ricerca della radice dove la funzione cambia segno e continuando a calcolare i punti medi (𝑐3, 𝑐4, …) degli intervalli selezionati. In altri termini, ripetendo questo processo iterativamente, ad ogni passo/iterazione 𝑘, generiamo una successione di numeri reali  𝑥𝑘 = 𝑐𝑘 = 𝑎𝑘 + 𝑏𝑘 /  2 , 𝑘 = 1,2,3, … 

che sono i punti medi degli intervalli che selezioniamo di volta in volta controllando dove avviene il cambio di segno della funzione 𝑓(𝑥) in esame. In altri termini, selezioniamo il nuovo intervallo dimezzando quello precedente e verificando in quale delle due metà avviene il cambio di segno. Generiamo così una successione di punti medi {𝑥𝑘} che al crescere di 𝑘 tenderà alla radice cercata lim 𝑘→∞ 𝑥𝑘 = 𝛼. Infatti, per costruzione, la radice della funzione 𝑓, indicata con 𝛼, è sempre contenuta nell'intervallo [𝑎𝑘, 𝑏𝑘] ad ogni iterazione 𝑘. Poiché la lunghezza degli intervalli [𝑎𝑘, 𝑏𝑘] si riduce progressivamente all'aumentare di 𝑘, il valore di 𝑥𝑘 = 𝑐𝑘 fornisce un’approssimazione sempre più precisa di 𝛼. Maggiore è il numero di iterazioni 𝑘, più accurata sarà l’approssimazione della radice 𝛼, attraverso i punti medi della successione.


|𝛼 − 𝑥𝑘| vuol dire il **valore assoluto** della **differenza tra** i due valori

la freccia vuol dire "tende" quindi il valore si avvicina a X ( in questo caso zero , man mano che il valore cresce)

|𝛼 − 𝑥𝑘| ⟶ 0 per 𝑘 → ∞

𝜖 indica un numero reale positivo piccolo 


Data la definizione del metodo della bisezione e semplificando la scrittura scriviamo : 
|𝛼 − 𝑥𝑘 | ≤  ( 𝑏𝑘 − 𝑎𝑘  / 2 )  =  ( 𝑏 − 𝑎 )   / ( 2^𝑘 ) .
Imponendo quindi la condizione 𝑏 − 𝑎 /  2^𝑘 ≤ 𝜖, possiamo ricavare una stima per 𝑘. A tale scopo applichiamo il logaritmo in base due ( visto che al denominatore delle divisione abbiamo un due ) a entrambi i membri della disequazione, ottenendo.

log2 ( 𝑏 − 𝑎 /  2^𝑘 ) ≤ log2 (𝜖)

che si riscrive 

k ≥ log2 (𝑏 − 𝑎) − log2 (𝜖)

che ci aiuta a trovare il numero minimo di iterazioni per il metodo di bisezione necessarie affinchè l' errore sia inferiore alla tolleranza desiderata