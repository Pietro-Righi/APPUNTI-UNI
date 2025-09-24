
## Radice di equazioni non lineari

Il metodo delle bisezioni è un metodo poco avanzato visto che si basa solo sul cambio di segno della funzione senza considerare il valore della funzione nei punti esaminati 

Esistono metodi piu avanzati come 
	-metodo delle corde
	-metodo delle secanti
	-metodo di newton

Questa famiglia di metodi si basa sul principio che , data una fuzione f(x) di cui vogliamo approssimare la radice a ,  costruiamo una successione {$x_n$} che converge alla radice a.
La successione è generata dall' uso di una retta passante per i punti { $x_n$  , $f(x_n)$ } e $x_{n+1}$ con pendenza  $q_n$ 


Un esempio puo essere :

Quindi trovare il processo che permette di calcolare $x_{n+1}$ partendo da $x_n$  (o il meccanismo che passa dall' iterazione n a n+1) 

Partendo dal valore $x_n$ calcoliamo il valore della funzione in quel punto f($x_n$) , e tracciamo una retta con una pendenza necessaria tale per cui tocchi l' asse x , quel punto diventerà il punto $x_{n+1}$ .

La pendenza verrà segnata come $q_n$ 
$$𝑥_{𝑛+1} = \frac{𝑥_𝑛 − 𝑓(𝑥_𝑛 )}{𝑞_n}$$
poniamo n >= 0


Ora vediamo i singoli metodi


### Metodo delle corde

Data una funzione f(x) definita dell' intervallo $[a,b]$ ,  con una pendenza costante  , quindi $q_n$  = $q$  è fisso per ogni n.

Definiamo corda la retta passante per i punti $(a,f(a))$ e $(b,f(b))$ che utilizzeremo per il calcolo delle radici

Dato un punto $x_n$ calcoliamo f($x_n$) e tracciamo una retta che passa per il punto $(x_n,f(x_n)$ con pendenza fissata $q_n$ , parallela alla retta formata da      $(a,f(a))$ e $(b,f(b))$  ,  il punto di intersezione con l' asse x di questa retta diventerà il punto $x_{n+1}$

la pendenza si calcola:
$$𝑞_n = q = \frac{𝑓(b) -  f(a)}{b-a}$$

quindi possiamo riscrivere la formula ricorsiva, utilizzando il metodo delle corde  ,  può essere scritta come :
$$𝑥_{𝑛+1} = \frac{𝑥_𝑛 − 𝑓(𝑥_𝑛 )}{𝑞_n} = 𝑥_{𝑛} - \frac{b − a}{𝑓(b) -  f(a)}*f(x_n) $$
per ogni n >=0

Questo metodo è un caso particolare visto che si utilizza il rapporto incrementale della funzione f nell' intervallo $[a,b]$ , che determina la sua pendenza costante


Ora presumiamo che il rapporto incrementale non sia fissato ma variabile , quindi la corda non mantiene una lunghezza costante , cosi facendo velocizziamo la convergenza del metodo verso la radice a

**Definizione**: con velocità di convergenza del metodo intediamo quanto velocemente di trovano le radici di una funzione  

La pendenza quindi si puo ricavare in due modi diversi :
	-Metodo delle secanti : utilizziamo il rapporto incrementale tra gli ultimi due punti calcolati , ottenendo un metodo che sfrutta informazioni aggiornate ad ogni iterazione
	-Metodo di newton: impiegando la derivata prima della funzione nel punto corrente generando cosi un metodo che utilizza la pendenza locale della funzione

### Metodo delle secanti

Un estensione del metodo delle corde , in cui la pendenza della retta non è fissa ma varia ad ogni iterazione.

Consideriamo una funzione arbitraria f(x) che interseca l' asse delle ascisse x in un punto a e ha due valori iniziali $x_{n-1}$ e $x_n$ , calcolando la pendenza locale  (in quel punto), della secante che passa per i punti    $(x_{n-1},f(x_{n-1}))$ e $(x_n,f(x_n))$  , poi si trova l' intersezione della secante , individuando il nuovo valore $x_{n+1}$ , che verrà utilizzato per calcolare il valore successivo e cosi via attraverso la seguente formula :

$$𝑞_n = q = \frac{𝑓(x_n) -  f(x_{n-1})}{x_n-x_{n-1}}$$
da cui otteniamo la formula iterativa :

$$𝑥_{𝑛+1} = \frac{𝑥_𝑛 − 𝑓(𝑥_𝑛 )}{𝑞_n} = 𝑥_{𝑛} - \frac{x_n-x_{n-1}}{𝑓(x_n) -  f(x_{n-1})}*f(x_n) $$

per ogni n >= 1
perche il metodo richiede 2 valori iniziali invece di 1 per calcolare la prima iterazione del metodo

### Metodo di Newton



