---
title: Coding Playground

language_tabs: # must be one of https://git.io/vQNgJ
  - cpp

toc_footers:
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>
  - <a>Logo made by Diesmo16</a>
includes:
  

search: true

code_clipboard: true
---

# Introduzione

Benvenuti alla pagina git di Fondamenti di Informatica! Qui verranno presentate tutte le soluzioni proposte degli esercizi visti a lezione. Buon divertimento!!


# Tutorial 

In questo corso, useremo [Code::Blocks](https://www.codeblocks.org/) per sviluppare i nostri programmi. 
Potete fare riferimento a queste slide: [Prima Esercitazione](https://unigeit-my.sharepoint.com/:b:/g/personal/704272_unige_it/EVUAOSkD7dJBtoSrFx7FiEUBLBUF43pr3kkd-YwuY85h_Q?e=EZlMjE) per tutte le informazioni relative all'installazione dell'ambiente di sviluppo, alla creazione di un progetto, alla compilazione e all'esecuzione dei file sorgenti.

# Esercitazioni

## Esercitazione - Prima esercitazione

### [Esercizio1_0] Programma "Hello World"


```cpp
#include <iostream>

int main() {
  // stampa a schermo la stringa tra virgolette
  std::cout << "Hello, World!";
  return 0;
}
```

> Il risultato dell'esecuzione del programma è:

```shell
Hello, World!
```

E' il classico esempio, che trovate quando inizializzate un progetto in Code::Blocks

Ma come funziona?


* `// stampa a schermo la stringa tra virgolette`
  In C++, ogni linea di codice che inizia con `//` è un commento. I commenti servono solo a far capire meglio il codice a tutti coloro che lo leggono (compreso il programmatore stesso che lo ha scritto!).
  E' completamente ignorato dal compilatore C++-
* `#include <iostream>`
  `#include` è una direttiva per il preprocessore, usata per includere file nel nostro programma. In questo esempio, serve ad includere il contenuto del file iostream. 
  In particolare, questo ci serve per usare  le librerie standard di I/O di C++, che oltre a mettere alle istruzioni C scanf e printf, mette a disposizione del programmatore anche un nuovo sistema di gestione delle operazioni di I/O piu' adatto alla programmazione orientata agli oggetti. 
  Per adesso, ricordatevi di aggiungere `#include <iostream>` se volete usare cout per stampare qualcosa sul terminale.
* `int main() {...}`
  Ogni programma in C++ deve avere la funzione `main()`. Le parentesi graffe indicano l'inizio e la fine della funzione. L'esecuzione del codice inizia da questa funzione. 
* `std::cout << "Hello World!";`
  `std::cout` stampa il contenuto all'interno delle virgolette. Deve essere seguito dall'operatore `<<` seguito da una stringa di testo ("Hello World!", nell'esempio).
* `return 0;`
   Lo statement `return 0;` è l'istruzione che termina la funzione main().

<aside class="notice">
Dobbiamo includere iostream per poter utilizzare std::cout
</aside>

<aside class="notice">
Nota: `;` va sempre inserito per indicare la fine di un'istruzione.
</aside>

<br>

### [Esercizio1_1] Programma per sommare due numeri


```cpp
#include <iostream>

int main()
{
    int number1, number2;
    std::cout << "Inserire un numero intero: ";
    std::cin >> number1;
    std::cout << "Inserire un altro numero intero: ";
    std::cin >> number2;

    int somma = number1 + number2;
    std::cout << "La somma dei due numeri e': " << somma << std::endl;
    return 0;
}

```

> L'esecuzione del programma ha come risultato:

```cpp
Inserire un numero intero: 5
Inserire un altro numero intero: 7
La somma dei due numeri e': 12
```

In questo esempio, gli interi immessi dall'utente sono memorizzati in una variabile.
Ad una terza variabile intera viene assegnata la somma dei due numeri. 
Infine, quest'ultima variabile viene stampata a schermo.
 

<aside class="notice">

Nel caso di variabili con nomi composti, usate la convenzione camelCase. Usate nomi di funzioni e variabili con la lettera minuscola.
</aside>

<br>
<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br> 
<br>


### [Assignment1_2] Creare un programma in c++ che chieda all'utente di inserire cinque interi e ne stampi a terminale la media (approssimandola ad intero)


```cpp
#include <iostream>

using namespace std;

int main()
{
    int num1, num2, num3, num4, num5, media;
    cout << "Ciao! Inserisci il primo numero: ";
    cin >> num1;
    cout << "Grazie! Ora un secondo numero: ";
    cin >> num2;
    cout << "Bene. Inserisci il terzo numero: ";
    cin >> num3;
    cout << "Andiamo alla grande. Ancora un numero: ";
    cin >> num4;
    cout << "Ci siamo quasi. Inserisci l'ultimo numero: ";
    cin >> num5;
    media = (num1 + num2 + num3 + num4 + num5)/5;
    cout << "Grazie! La media dei 5 numeri immessi e' " << media << endl;
    return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Ciao! Inserisci il primo numero: 30
Grazie! Ora un secondo numero: 20
Bene. Inserisci il terzo numero: 10
Andiamo alla grande. Ancora un numero: 15
Ci siamo quasi. Inserisci l'ultimo numero: 30
Grazie! La media dei 5 numeri immessi e' 21
```

L'esercizio non presenta particolari difficoltà rispetto ai precedenti. Si noti che la variabile "media" è un intero; la divisione tra interi restituisce come risultato il quoziente della divisione.

<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>

### [Assignment1_3] Creare un programma in c++ che chieda all'utente di immettere la lunghezza (intera) di due cateti di un triangolo rettangolo e stampi a terminale il quadrato dell'ipotenusa. 



```cpp
#include <iostream>

using namespace std;

int main()
{
    int cateto1, cateto2, quadratoIpotenusa;
    cout << "Ciao! Inserisci la lunghezza di un cateto: ";
    cin >> cateto1;
    cout << "Grazie! Inserisci la lunghezza del secondo cateto: ";
    cin >> cateto2;
    quadratoIpotenusa = cateto1 * cateto1 + cateto2 * cateto2;
    cout << "Il quadrato dell'ipotenusa e' pari a " << quadratoIpotenusa << endl;
    return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Ciao! Inserisci la lunghezza di un cateto: 3
Grazie! Inserisci la lunghezza del secondo cateto: 4
Il quadrato dell'ipotenusa e' pari a 25
```

Il programma sfrutta gli operatori di moltiplicazione e di somma.


<aside class="notice">

Si noti che l'elevazione a potenza di un numero può essere effettuata anche sfruttando l'operatore pow, con la sintassi std::pow (base, esponente). In questo caso deve però essere incluso anche l'header cmath

</aside>

<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br> 


### [Assignment1_4] Creare un programma in c++ che chieda all'utente di immettere due interi, divida il primo numero per il secondo, e stampi a terminale il quoziente e il resto

```cpp
#include <iostream>

using namespace std;

int main()
{
    int num1, num2, quoziente, resto;
    cout << "Ciao! Inserisci il primo numero: ";
    cin >> num1;
    cout << "Grazie! Inserisci un altro numero: ";
    cin >> num2;
    quoziente = num1 / num2;
    resto = num1 % num2;
    cout << "La divisione tra i due numeri ha come quoziente " << quoziente <<
        " e come resto " << resto << endl;
    return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Ciao! Inserisci il primo numero: 63
Grazie! Inserisci un altro numero: 10
La divisione tra i due numeri ha come quoziente 6 e come resto 3
```
La divisione implementata tra interi da come risultato un quoziente e un resto. Gli operatori algebrici in C++ possono dare un solo risultato per volta, per cui per il calcolo della divisione tra int ci sono due operatori: l'operatore quoziente / e l'operatore modulo %. 

Il simbolo / serve per il calcolo del quoziente della divisione intera tra due valori interi. 

Il simbolo % serve per il calcolo del resto (o quoto) della divisione tra due valori.

<aside class="notice">

Lo stesso simbolo '/' in C++ si usa anche nelle divisioni tra numeri con la virgola, non importa se siano essi float o double, e numeri con la virgola e numeri interi.

</aside>

<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


### [Assignment1_5] Realizzare un convertitore Euro -> Lire, utilizzando come fattore di conversione l'intero costante 1936.


```cpp
#include <iostream>

using namespace std;

int main()
{
    int euro, lire;
    const int conv = 1936;
    cout << "Ciao! Inserisci il prezzo in euro: ";
    cin >> euro;
    lire = euro * conv;
    cout << "Il prezzo immesso equivale a " << lire << " lire!" << endl;
    return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Ciao! Inserisci il prezzo in euro: 10
Il prezzo immesso equivale a 19360 lire!
```

Come il nome stesso suggerisce, const rende la variabile intera a cui è applicata immutabile. L'uso più ovvio è quello della definizione di valori costanti che rimangono immutati per l'intera esecuzione del programma.

Data l'immutabilità di una variabile const, la sua inizializzazione deve essere contestuale alla dichiarazione. Ad esempio il frammento seguente genererà un errore di compilazione:

`const double phi; phi = 1.6180339887; // errore`

<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br> 


## Esercitazione - Seconda esercitazione

### [Esercizio2_0] Risolutore di equazioni di secondo grado

```cpp
#include <iostream>
#include <cmath>

using namespace std;

int main()
{
    //risolutore di equazioni di secondo grado
    double a, b, c;
    double root1, root2;
    cout << "Inserisci i coefficienti dell'equazione di secondo grado: ax^2 + bx + c = 0" << endl;
    cin >> a >> b >> c;
    if (a == 0){
        if (b == 0) {
            if (c==0)
                {
                // se i tre coefficienti sono 0, qualsiasi valore di x risolve l'equazione
                cout << "L'equazione ha infinite soluzioni" << endl;
                }
            else
                {
                // l'equazione è di tipo c = 0, con c!=0.
                cout << "L'equazione non ha soluzione" << endl;
                }
            }
        else{
            // risolviamo l'equazione di primo grado
            root1 = -c/b;
            cout << "L'equazione ha una soluzione reale: x = " << root1 << endl;
        }
    }
    else {
        if ((pow(b,2)-4*a*c)>=0){
            root1 = (-b - sqrt(pow(b,2)-4*a*c))/(2*a);
            root2 = (-b + sqrt(pow(b,2)-4*a*c))/(2*a);
            if (root1==root2){
                cout << "L'equazione ha due soluzione reali e coincidenti: x = " << root1 << endl;
            }
            else{
                cout << "L'equazione ha due soluzione reali distinte: x = " << root1 << " e x = "
                    << root2 << endl;
            }
        }
        else{
            // se il discriminante è minore di zero, l'equazione non ha soluzioni reali
            cout << "L'equazione non ha soluzioni reali!" << endl;
            return 0;
        }
    }
    return 0;
}
```
> L'esecuzione del programma ha come risultato:

```cpp
Inserisci i coefficienti dell'equazione di secondo grado: ax^2 + bx + c = 0
4
12
6
L'equazione ha due soluzione reali distinte: x = -2.36603 e x = -0.633975
```

Il programma prevede l'utilizzo di istruzioni condizionali e variabili di tipo double per esplorare tutti i possibili casi da valutare per la soluzione di un'equazione di secondo grado.

<aside class="notice">

Uno degli errori più comuni per chi inizia a programmare consiste nel confondere l'operatore assegnamento (=) con l'operatore di uguaglianza (==). L'assegnamento (=) è utilizzato per assegnare un valore ad una variabile. L'operatore di uguaglianza (==) è utilizzato per verificare se due variabili hanno lo stesso valore.

</aside>

<aside class="notice">

In particolare nel caso di programmi più complessi, può essere utile inserire dei commenti nel codice, per aumentarne la leggibilità. Uno dei possibili modi di farlo è utilizzare '//'

</aside>

<aside class="notice">

<p>math.h VS cmath.</p>

La libreria C++ include le stesse definizioni di quella C, con le seguenti differenze:

- Ogni header ha lo stesso nome di quello utilizzato in C, ma con un prefisso "c" e nessuna estensione. Per esempio, l'equivalente in C++ dell'header stdlib.h e cstdlib.

- Ogni elemento della libreria è definito nel namespace std.

Raccomandiamo l'uso di cmath quando si usa il C++.

</aside>


E' possibile esplorare le librerie C++ [qui](http://www.cplusplus.com/reference/)

<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


### [Assignment2_1] Programma che controlla l'immissione di una password

```cpp

#include <iostream>

int main()
{
  ...
  return 0;
}

```

> L'esecuzione del programma ha come risultato:

```cpp
```

Creare un programma che fa inserire all'utente 4 caratteri e verifica che ci sia almeno una lettera minuscola, una maiuscola e una cifra. Utilizzare l'operatore condizionale if.


<aside class="notice">

Il valore ASCII dei caratteri minuscoli va da 97 to 122

</aside>

<aside class="notice">

Il valore ASCII dei caratteri maiuscoli va da 65 to 90

</aside>

<aside class="notice">

Il valore ASCII delle cifre va da 48 a 57.

</aside>


[Qui](https://www.oppo.it/tabelle/tabella_ascii.htm) potete trovare una tabella riassuntiva.

<br>
<br>
<br>

### [Assignment2_2] Programma che controlla l'immissione di una vocale

```cpp

#include <iostream>

int main()
{
  ...
  return 0;
}

```

> L'esecuzione del programma ha come risultato:

```cpp
```

Creare un programma che fa inserire all'utente un carattere, e verifica che il carattere immesso sia una vocale o meno, utilizzando lo statement "switch".

<aside class="notice">

Se nessuna delle etichette ha un valore corrispondente a quello dell'espressione, il flusso viene rediretto all'etichetta opzionale default, se presente.

</aside>

<br>
<br>
<br>
<br>
<br>
<br>
<br>

### [Assignment2_3] Convertitore lire - euro / euro - lire

```cpp

#include <iostream>

int main()
{
  ...
  return 0;
}

```

> L'esecuzione del programma ha come risultato:

```cpp
```

Creare un programma che chieda all'utente se vuole immettere un valore in euro o in lire, acquisisca il valore dall'utente e restituisca il valore convertito nell'altra valuta.

<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

### [Assignment2_4] Calcolatore di stagione

```cpp

#include <iostream>

int main()
{
  ...
  return 0;
}

```

> L'esecuzione del programma ha come risultato:

```cpp
```

Scrivere un programma che chieda all'utente di immettere due interi, relativi al giorno e al mese, e restituisca la stagione corrispondente. Utilizzare sia l'operatore switch che if.

<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

