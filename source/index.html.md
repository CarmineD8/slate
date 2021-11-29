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

## Prima esercitazione - "Hello World" e variabili intere

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


## Seconda esercitazione - Char, float e double - Statement if e switch

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

using namespace std;

int main()
{
    char a ,b, c, d;
    cout << "Inserisci una password di quattro caratteri:" << endl;
    cin >> a >> b >> c >> d;
    int minuscolo = (a>=97 && a<= 122) || (b>=97 && b<= 122) || (c>=97 && c<= 122) || (d>=97 && d<= 122);
    int maiuscolo = (a>=65 && a<= 90) || (b>=65 && b<= 90) || (c>=65 && c<= 90) || (d>=65 && d<= 90);
    int cifra = (a>=48 && a<= 57) || (b>=48 && b<= 57) || (c>=48 && c<= 57) || (d>=48 && d<= 57);

    if (minuscolo && maiuscolo && cifra){
        cout << "Password OK!" << endl;
    }
    else{
        cout << "La password non va bene" << endl;
    }

    return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Inserisci una password di quattro caratteri:
P4ss
Password OK!
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

<aside class="notice">
Gli operatori logici possono essere utili per raggruppare alcune condizioni e evitare l'utilizzo di operatori condizionali in cascata.
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

### [Assignment2_2] Programma che controlla l'immissione di una vocale

```cpp
#include <iostream>

using namespace std;

int main()
{
    char a;
    cout << "Inserisci una lettera, grazie!" << endl;
    cin >> a;
    switch (a){
        case 'a':
        case 'A':
        case 'e':
        case 'E':
        case 'i':
        case 'I':
        case 'o':
        case 'O':
        case 'u':
        case 'U':
            cout << "Hai inserito una vocale!" << endl;
            break;
        default:
            cout << "Non hai inserito una vocale!" << endl;
            break;
    }
    return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Inserisci una lettera, grazie!
I
Hai inserito una vocale!
```

Creare un programma che fa inserire all'utente un carattere, e verifica che il carattere immesso sia una vocale o meno, utilizzando lo statement "switch".

<aside class="notice">

Se nessuna delle etichette ha un valore corrispondente a quello dell'espressione, il flusso viene rediretto all'etichetta opzionale default, se presente.

</aside>

<aside class="notice">

Usando l'operatore switch, può essere utile raggruppare i casi insieme, ma bisogna fare attenzione alla leggibilità del codice.

</aside>

<aside class="notice">

Lettere maiuscole e minuscole hanno codifiche ASCII diverse, e vanno quindi considerate come casi separati.

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
<br>
<br>
<br>
<br>

### [Assignment2_3] Convertitore lire - euro / euro - lire

```cpp
#include <iostream>

using namespace std;

int main()
{
    double num, num_conv;
    char a;
    cout << "Convertitore Euro-Lire / Lire-Euro" << endl;
    cout << "Premi l per convertire un valore da euro a lire, " <<
            "e per convertire un valore da lire a euro" << endl;
    cin >> a;
    if (a == 'l'){
        cout << "Inserisci la cifra in euro: ";
        cin >> num;
        num_conv = num * 1936.27;
        cout << "La cifra in lire e' " << num_conv << endl;
    }
    else if (a == 'e'){
        cout << "Inserisci la cifra in lire: ";
        cin >> num;
        num_conv = num / 1936.27;
        cout << "La cifra in euro e' " << num_conv << endl;
    }
    else {
        cout << "La lettera immessa e' sbagliata!" << endl;
    }
    return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Convertitore Euro-Lire / Lire-Euro
Premi l per convertire un valore da euro a lire, e per convertire un valore da lire a euro
e
Inserisci la cifra in lire: 20000
La cifra in euro e' 10.3291
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

### [Assignment2_4] Calcolatore di stagione

```cpp
#include <iostream>

using namespace std;

int main()
{
    int giorno, mese;
    cout << "Inserisci il giorno e il mese dell'anno" << endl;
    cin >> giorno >> mese;
    switch (mese){
        case 1:
        case 3:
        case 5:
        case 7:
        case 8:
        case 10:
        case 12:
            if (giorno >31 || giorno <0){
                cout << "La data e' sbagliata!";
                return 0;
            }
            break;
        case 4:
        case 6:
        case 9:
        case 11:
            if (giorno >30 || giorno <0){
                cout << "La data e' sbagliata!";
                return 0;
            }
            break;
        case 2:
            if (giorno >29 || giorno <0){
                cout << "La data e' sbagliata!";
                return 0;
            }
            break;
        default:
            cout << "Questo mese non esiste!";
            return 0;
    }
    switch (mese){
        case 1:
        case 2:
            cout << "Inverno!";
            break;
        case 4:
        case 5:
            cout << "Primavera";
            break;
        case 7:
        case 8:
            cout << "Estate";
            break;
        case 10:
        case 11:
            cout << "Autunno";
            break;
        case 3:
            if (giorno >=20)
                cout << "Primavera";
            else
                cout << "Inverno";
            break;
        case 6:
            if (giorno >=21)
                cout << "Estate";
            else
                cout << "Primavera";
            break;
        case 9:
            if (giorno >=22)
                cout << "Autunno";
            else
                cout << "Estate";
            break;
        case 12:
            if (giorno >=21)
                cout << "Inverno";
            else
                cout << "Autunno";
            break;
    }
    return 0;
}

```

> L'esecuzione del programma ha come risultato:

```cpp
Inserisci il giorno e il mese dell'anno
29 2
Inverno!
```

Scrivere un programma che chieda all'utente di immettere due interi, relativi al giorno e al mese, e restituisca la stagione corrispondente. Utilizzare sia l'operatore switch che if.

<aside class="notice">

Nella soluzione proposta, viene usato due volte l'operatore switch: la prima volta per calcolare l'esattezza della data, la seconda volta per calcolare la stagione. 

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

## Terza esercitazione - Cicli while, do-while e for

### [Esercizio 3_0] Calcolatrice do-while

```cpp
# include <iostream>

int main()
{
  char op;
  float num1, num2;
  char flag = 'y';

  do {

    std::cout << "Inserisci l'operazione: ( es: 3 + 5): ";
    std::cin >> num1 >> op >>  num2;

    switch(op)
    {
      case '+':
        std::cout << num1+num2 << std::endl;
        break;

      case '-':
        std::cout << num1-num2 << std::endl;
        break;

      case '*':
        std::cout << num1*num2 << std::endl;
        break;

      case '/':
        if (num2 == 0){
          std::cout << "Errore! Non posso dividere per 0" << std::endl;
          break;
        }
        std::cout << num1/num2 << std::endl;
        break;

      default:
        std::cout << "Errore! Questo operatore non e' supportato";
        break;
    }

    std::cout << "Premi y per continuare, qualsiasi altra lettera per uscire ";
    std::cin >> flag;

  } while (flag == 'y');

  std::cout << "Esco dal programma";

  return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Inserisci l'operazione: ( es: 3 + 5): 12 / 0
Errore! Non posso dividere per 0
Premi y per continuare, qualsiasi altra lettera per uscire y
Inserisci l'operazione: ( es: 3 + 5): 12 / 10
1.2
Premi y per continuare, qualsiasi altra lettera per uscire y
Inserisci l'operazione: ( es: 3 + 5): 7 * 8
56
Premi y per continuare, qualsiasi altra lettera per uscire n
Esco dal programma
```

Il programma consente all'utente di inserire due numeri e un'operazione, e stampa a terminale il risultato dell'operazione. Una volta eseguita l'operazione, il programma chiede all'utente se continuare o interrompere. Nel primo caso, chiede nuovamente di inserire numeri e operazione.

<aside class="notice">

Il ciclo do-while esegue il corpo dell'iterazione almeno una volta, ma il ciclo viene ripetuto solo se la condizione è verificata.

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


### [Esercizio 3_1] Calcolatore di numeri primi

```cpp
# include <iostream>

using namespace std;

int main()
{
    int num, primo;
    do{
        cout << "Inserisci un numero intero maggiore di 1: " ;
        cin >> num;
    } while (num <1);
    cout << "I numeri primi compresi tra 0 e il numero immesso sono: ";
    for (int i=2; i<=num; i++){
        primo = 1;
        for (int j=i-1; j>1; j--){
            if (i%j==0){
                primo = 0;
            }
        }
        if (primo == 1){
            cout << i << " ";
        }
    }
  return 0;
}
```
> L'esecuzione del programma ha come risultato:

```cpp
Inserisci un numero intero maggiore di 1: 1000
I numeri primi compresi tra 0 e il numero immesso sono: 2 3 5 7 11 13 17 19 23 29 31 37 41 43 47 53 59 61 67 71 73 79 83 89 97 101 103 107 109 113 127 131 137 139 149 151 157 163 167 173 179 181 191 193 197 199 211 223 227 229 233 239 241 251 257 263 269 271 277 281 283 293 307 311 313 317 331 337 347 349 353 359 367 373 379 383 389 397 401 409 419 421 431 433 439 443 449 457 461 463 467 479 487 491 499 503 509 521 523 541 547 557 563 569 571 577 587 593 599 601 607 613 617 619 631 641 643 647 653 659 661 673 677 683 691 701 709 719 727 733 739 743 751 757 761 769 773 787 797 809 811 821 823 827 829 839 853 857 859 863 877 881 883 887 907 911 919 929 937 941 947 953 967 971 977 983 991 997
```

Il programma chiede all'utente di inserire un numero, e calcola tutti i numeri primi compresi tra zero e il numero immesso.

<aside class="notice">

I cicli possono essere anche annidati, ossia possiamo avere un ciclo for (o while) all'interno di un altro ciclo for (o while)

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
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

### [Assignment 3_2]  Programma per stampare un pattern

```cpp
#include <iostream>

using namespace std;

int main()
{
    int num;
    cout << "Ciao! Inserisci un numero: ";
    cin >> num ;

    for (int i=0; i < num; i++){
        for (int j=0; j<num; j++){
            cout << "*";
        }
        cout << endl;
    }
    return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Ciao! Inserisci un numero: 8
********
********
********
********
********
********
********
********
```

Sviluppare un programma che chieda all'utente un numero e stampi a terminale un pattern predefinito a seconda del numero inserito. 

<aside class="notice">

Con piccole modifiche nei cicli for, si possono ottenere pattern diversi.

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

### [Assignment 3_3] Programma per calcolare numeri pari e dispari

```cpp
#include <iostream>

using namespace std;

int main()
{
    int num;
    int contapari = 0;
    int contadispari = 0;

    do{
        cout << "Ciao! Inserisci un numero intero maggiore di zero (-1 per uscire): ";
        cin >> num ;
        if (num == -1) {
            cout << "Grazie! " << endl;
        }
        else if (num <= 0){
            cout << "Numero non valido" << endl;
        }
        else if(num%2==0){
            contapari++;
        }
        else{
            contadispari++;
        }
    }while(num !=-1);

    cout << "Hai immesso " << contapari << " numeri pari!" << endl;
    cout << "Hai immesso " << contadispari << " numeri dispari!" << endl;



    return 0;
}

```

> L'esecuzione del programma ha come risultato:

```cpp
Ciao! Inserisci un numero intero maggiore di zero (-1 per uscire): 10
Ciao! Inserisci un numero intero maggiore di zero (-1 per uscire): 4
Ciao! Inserisci un numero intero maggiore di zero (-1 per uscire): 8
Ciao! Inserisci un numero intero maggiore di zero (-1 per uscire): 3
Ciao! Inserisci un numero intero maggiore di zero (-1 per uscire): 7
Ciao! Inserisci un numero intero maggiore di zero (-1 per uscire): -1
Grazie!
Hai immesso 3 numeri pari!
Hai immesso 2 numeri dispari!
```
Scrivere un programma che permetta all'utente di inserire una serie di numeri positivi interi, finché non viene inserito il valore -1: a quel punto, il programma dice quanti numeri pari e dispari sono stati immessi. (hint: usare un ciclo do - while)

<aside class="notice">

Il ciclo do-while può essere molto utile per descrivere in forma compatta iterazioni che sicuramente si devono ripetere almeno una volta.

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

### [Assignment 3_4] Programma per calcolare il numero di cifre di un numero

```cpp
#include <iostream>

using namespace std;

int main()
{
    int num;
    int contacifre = 0;

    do {
    cout << "Inserire un numero intero maggiore di zero: ";
    cin >> num;
    } while (num<=0);

    while(num>0){
        num=num/10;
        contacifre++;
    }

    cout << "Il numero immesso ha " << contacifre << " cifre!" << endl;

    return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Inserire un numero intero maggiore di zero: -5
Inserire un numero intero maggiore di zero: 15623
Il numero immesso ha 5 cifre!

```

Scrivere un programma che chieda all'utente di inserire un numero intero e calcoli di quante cifre è composto (hint: usare un ciclo while).

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

## Quarta esercitazione - Funzioni. Passaggio di parametri per valore e per riferimento

### [Esercizio 4_0] Programma per contare vocali e consonanti in una frase. 

```cpp
#include <iostream>

using namespace std;

int controllo_vocale (char carattere){
    int ritorno;
   switch (carattere){
        case 'a':
        case 'A':
        case 'e':
        case 'E':
        case 'i':
        case 'I':
        case 'o':
        case 'O':
        case 'u':
        case 'U':
            ritorno = 1;
            break;
        default:
            ritorno = 0;
            break;
    }
    return ritorno;
}


int main()
{
    char a;
    int conta = 0;
    int contavocali = 0;
    int contaconsonanti = 0;
    cout << "Inserisci una frase, metti il punto quando hai finito: ";
    while (1){
        cin >> a;
        if (a == '.')
            break;
        if (controllo_vocale(a))
            contavocali++;
        else
            contaconsonanti++;
        conta++;
    }

    cout << "Hai inserito " << conta << " lettere, di cui " <<
    contavocali << " vocali e " << contaconsonanti << " consonanti." << endl;
}

```

> L'esecuzione del programma ha come risultato:

```cpp
Inserisci una frase, metti il punto quando hai finito: faccio una prova per vedere se funziona.
Hai inserito 33 lettere, di cui 16 vocali e 17 consonanti.

```

Il programma consente all'utente di inserire una frase, e stampa a terminale il numero totale di caratteri, di vocali e di consonanti.

Possiamo riutilizzare parte del codice già sviluppato nell'esercitazione 2, per verificare se una lettera è una consonante o una vocale.

<aside class="notice">

L'istruzione break permette di terminare un ciclo iterativo, saltando alla prima istruzione fuori dal ciclo.

</aside>

<aside class="notice">

Utilizzare funzioni permette di riutilizzare codice già sviluppato in precedenza, e di rendere il codice più leggibile nella funzione main.

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

### [Esercizio 4_1] Riduzione di frazioni

```cpp
#include <iostream>

using namespace std;

void riduco(int& num, int& den){
    int minimo, mcd;
    if(num>den)
        minimo=num;
    else
        minimo=den;
    for (int i=1;i<=minimo;i++){
        if ((num%i==0) && (den%i==0)){
            mcd=i;
        }
    }
    num=num/mcd;
    den=den/mcd;
}

int main()
{
    int num1, num2, den1, den2;
    char op1, op2;
    cout << "Inserisci due frazioni:" << endl;
    cin >> num1 >> op1 >> den1;
    cin >> num2 >> op2 >> den2;
    riduco(num1, den1);
    riduco(num2, den2);
    cout << "La prima frazione si puo' ridurre a: " << num1 << op1 << den1 << endl;
    cout << "La seconda frazione si puo' ridurre a: " << num2 << op2 << den2 << endl;
    return 0;
}

```

> L'esecuzione del programma ha come risultato:

```cpp
Inserisci due frazioni:
2/12
27/63
La prima frazione si puo' ridurre a: 1/6
La seconda frazione si puo' ridurre a: 3/7
```

Il programma chiede all'utente di inserire due frazioni, e le riduce ai minimi termini.

In questo esercizio, voglio usare una funzione per effettuare la riduzione delle funzioni ai minimi termini. In questo caso può essere utile passare i parametri per riferimento, così da modificare anche i valori di numeratore e denominatore nella nostra funzione main.

<aside class="notice">

Con il passaggio di parametri per riferimento, alla funzione viene passato l'indirizzo e non il valore dell'argomento. Questo approccio richiede meno memoria rispetto alla chiamata per valore, e soprattutto consente di modificare il valore delle variabili che sono ad un livello di visibilità esterno alla funzione.

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

### [Assignment 4_2] Calcolo del numero di cifre

```cpp

#include <iostream>

using namespace std;

int contacifre (int a){
    int cifre = 0;
    while(a!=0){
        a=a/10;
        cifre++;
    }
    return cifre;
}

int main()
{
    int num;
    int cifre = 0;
	cout << "Inserisci numeri interi. Puoi uscire dal programma inserendo -1: " << endl;
	do {
        cin >> num;
        if (num == 0 || num == -1)
            continue;
        else
            cifre = cifre + contacifre (num);
	} while(num!=-1);
	cout << "Hai inserito un totale di: " << cifre << " cifre! " << endl;
	return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Inserisci numeri interi. Puoi uscire dal programma inserendo -1:
154
-23
212
-1
Hai inserito un totale di: 8 cifre!
```

Scrivere un programma che chieda all'utente di inserire dei numeri interi, finché l'utente non inserisce -1 (per uscire dal ciclo).

A quel punto, il programma stampa il numero di cifre totale immesso dall'utente.

Hint: usare un ciclo while (o do-while) per gestire l'inserimento dei numeri

Hint: usare una funzione per contare il numero di cifre di ogni numero inserito (vedi Assignment 3_4)

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

### [Assignment 4_3] Calcolo di minuti e secondi

```cpp
#include <iostream>

using namespace std;

int timeconv (int& minuti, int& sec, int& ms){
    sec = ms/1000;
    minuti = sec/60;
    sec = sec%60;
    ms = ms%1000;
}

int main()
{
    int ms1, ms2;
    int sec1, sec2;
    int min1, min2;
    cout << "Inserisci un tempo in millisecondi: ";
    cin >> ms1;
    while (ms1 <0){
        cout << "Per favore, inserisci un numero positivo: ";
        cin >> ms1;
    }
    cout << "Inserisci un altro tempo in millisecondi: ";
    cin >> ms2;
    while (ms2 <0){
        cout << "Per favore, inserisci un numero positivo: ";
        cin >> ms2;
    }
    timeconv(min1, sec1, ms1);
    timeconv(min2, sec2, ms2);
    if (min1 == min2){
        cout << "I tempi immessi corrispondono agli stessi minuti!" << endl;
    }
    cout << min1 << " minuti, " << sec1 << " secondi, " << ms1 << " millisecondi" << endl;
    cout << min2 << " minuti, " << sec2 << " secondi, " << ms2 << " millisecondi" << endl;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Inserisci un tempo in millisecondi: 100500
Inserisci un altro tempo in millisecondi: 110050
I tempi immessi corrispondono agli stessi minuti!
1 minuti, 40 secondi, 500 millisecondi
1 minuti, 50 secondi, 50 millisecondi
```

Creare un programma che, dopo aver chiesto all'utente di inserire due tempi dati in millisecondi, restituisca per entrambi l'equivalente in termini di minuti, secondi, millisecondi, e controlli se corrispondono agli stessi minuti.

Hint: usare una funzione passando i parametri per riferimento.

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
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

### [Assignment 4_4] Differenza tra maggiore e minore

```cpp
#include <iostream>

using namespace std;

double trovaminimo (double a1, double a2, double a3){
    double minimo;
    if (a1 < a2){
        if (a1 < a3)
            minimo = a1;
        else
            minimo = a3;
    }
    else {
        if (a2 < a3)
            minimo = a2;
        else
            minimo = a3;
    }
    return minimo;
}

double trovamassimo (double a1, double a2, double a3){
    double massimo;
    if (a1 > a2){
        if (a1 > a3)
            massimo = a1;
        else
            massimo = a3;
    }
    else {
        if (a2 > a3)
            massimo = a2;
        else
            massimo = a3;
    }
    return massimo;
}

double differenza (double a1, double a2, double a3){
    double minimo, massimo, diff;
    minimo = trovaminimo (a1, a2, a3);
    massimo = trovamassimo (a1, a2, a3);
    diff = massimo - minimo;
    return diff;
}

int main()
{
    double num1, num2, num3;
    cout << "Inserisci tre numeri: " << endl;
    cin >> num1 >> num2 >> num3;
    cout << "La differenza tra il numero piu' grande e il piccolo e': " << differenza(num1, num2, num3);
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Inserisci tre numeri:
43
76
-14
La differenza tra il numero piu' grande e il piccolo e': 90
```

Scrivere un programma che chieda all'utente di inserire tre numeri (non necessariamente interi), e restituisca la differenza tra il numero più grande e il numero più piccolo immesso dall'utente. 

Hint: E' possibile creare una funzione che restituisca la differenza dei tre numeri, e a sua volta chiami una funzione per il calcolo del massimo, e una per il calcolo del minimo.

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
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Quinta esercitazione - Array e Stringhe

### [Esercizio 5_0] Scambio degli elementi di un array

```cpp
#include <iostream>

using namespace std;

void ordina_array(double arr[], int dim){
    double minimo = arr[0];
    int index_min = 0;
    double massimo = arr[0];
    int index_max = 0;
    for (int i=1;i<dim;i++){
        if (arr[i]<minimo){
            minimo=arr[i];
            index_min = i;
        }
        if (arr[i] > massimo){
            massimo = arr[i];
            index_max = i;
        }
    }
    double temp = arr[index_min];
    arr[index_min] = arr[index_max];
    arr[index_max] = temp;
}

int main()
{
    int dim;
    cout << "Di quanti elementi vuoi che sia l'array? ";
    cin >> dim;
    double arr[dim];
     cout << "Per favore, inserisci " << dim << " numeri: ";
    for (int i=0;i<dim;i++){
        cin >> arr[i];
    }
    ordina_array (arr, dim);
    cout << "Grazie. Ecco la lista di numeri con massimo e minimo invertiti: ";
    for (int i=0;i<dim;i++){
        cout << arr[i] << " ";
    }
}

```
> L'esecuzione del programma ha come risultato:

```cpp
Di quanti elementi vuoi che sia l'array? 4
Per favore, inserisci 4 numeri:  13 4 2 -5
Grazie. Ecco la lista di numeri con massimo e minimo invertiti: -5 4 2 13
```

Creare un programma che chieda all'utente di inserire dei numeri, li inserisca in un array, e scambi il numero minore con il maggiore.

<aside class="notice">
L'intero dim viene acquisito dall'utente e utilizzato in tutti i cicli for. Una eventuale modifica di questo intero potrebbe causare errori in runtime.
</aside>

<aside class="notice">
L'array viene sempre passato ad una funzione per riferimento.
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

### [Esercizio 5_1] Lettere in rima
```cpp
#include <iostream>
#include <cstring>

using namespace std;

int main()
{
    const int dim = 256;
    int contarima = 0, len1, len2, len;
    char stringa1[dim], stringa2[dim];
    cin.getline(stringa1, dim, '\n');
    cin.getline(stringa2, dim, '\n');
    len1 = strlen(stringa1);
    len2 = strlen(stringa2);

    if (len1 < len2)
        len = len1;
    else
        len = len2;

    for (int i=1; i<=len; i++){
        if(stringa1[len1-i]==stringa2[len2-i])
            contarima++;
        else
            break;
    }
    cout << "Le lettere che fanno rima sono: " << contarima << endl;
}
```
> L'esecuzione del programma ha come risultato:

```cpp
proviamo con questa frase
questo esercizio di base
Le lettere che fanno rima sono: 3
```

Creare un programma che chieda all'utente di inserire due stringhe, e conti il numero di lettere che "fanno rima", ovvero il numero di lettere uguali in fondo alle due stringhe.

<aside class="notice">
Per lavorare con le stringhe, è necessario includere l'header cstring.
</aside>

<aside class="notice">
La funzione cin.getline permette di acquisire una stringa fino a che l'utente immette il carattere passato come terzo argomento della funzione.
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
<br>
<br>
<br>
<br>
<br>

### [Assignment 5_2] Programma che riempie un array di interi con numeri random.

```cpp
#include <iostream>
#include <ctime>
#include <cstdlib>

using namespace std;


int main()
{
    srand(time(NULL));
    int dim;
    cout << "Inserisci la dimensione dell'array: ";
    cin >> dim;
    int arr[dim];
    for (int i=0;i<dim;i++){
        arr[i]=rand()%100;
    }
    cout << "Ecco l'array con numeri random: [";
     for (int i=0;i<dim;i++){
        cout << arr[i] << ", ";
    }
    cout << "\b\b]";
    return 0;
}
```
> L'esecuzione del programma ha come risultato:

```cpp
Inserisci la dimensione dell'array: 5
Ecco l'array con numeri random: [0, 73, 66, 69, 19]
```

Creare un programma che, dopo aver chiesto all'utente di inserire la dimensione di un array, li riempia con interi random compresi tra 0 e 99.

<aside class="notice">
Potete utilizzare la funzione rand() per generare un intero random. Per limitarlo tra 0 e 99, basta considerare il modulo della divisione per 100:   rand()%100;
</aside>

<aside class="notice">
Per far sì che rand() sia realmente random, devo inizializzare il «seed» della funzione in maniera casuale. Posso farlo con: srand(time(NULL));
</aside>

<aside class="notice">
Per poter usare le funzioni rand e time, dovete includere anche gli header ctime e cstdlib.
</aside>

<aside class="notice">
Il carattere speciale '\b' torna indietro di uno spazio.
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

### [Assignment 5_3] Moltiplicazione di array

```cpp
#include <iostream>

using namespace std;

void moltiplica_array(int arr1[], int arr2[], int arr_ris[], int dim){
    for (int i=0;i<dim;i++){
        arr_ris[i]=arr1[i]*arr2[i];
    }

}

int main()
{
    int dim;
    cout << "Inserisci la dimensione degli array: ";
    cin >> dim;
    int arr1[dim], arr2[dim], arr_ris[dim];
    cout << "Inserisci gli elementi del primo array: ";
    for (int i=0;i<dim;i++){
        cin >> arr1[i];
    }
    cout << "Inserisci gli elementi del secondo array: ";
    for (int i=0;i<dim;i++){
        cin >> arr2[i];
    }
    moltiplica_array(arr1, arr2, arr_ris, dim);
    cout << "L'array finale e': [";
    for (int i=0;i<dim;i++){
        cout << arr_ris[i] << ", ";
    }
    cout << "\b\b]";

    return 0;
}
```
> L'esecuzione del programma ha come risultato:

```cpp
Inserisci la dimensione degli array: 2
Inserisci gli elementi del primo array: 2 4
Inserisci gli elementi del secondo array: 4 8
L'array finale e': [8, 32]
```

Creare un programma che, dopo aver chiesto all'utente di inserire la dimensione e gli elementi di due array, li moltiplichi tra di loro e stampi il risultato finale. Utilizzare una funzione per moltiplicare gli array.

<aside class="notice">
Non è possibile moltiplicare direttamente gli array. E' necessario utilizzare un ciclo for.
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

### [Assignment 5_4] Inversione di array

```cpp
#include <iostream>

using namespace std;

void inverti_array(int arr[], int dim){
    int arr_temp[dim];
    for (int i=0;i<dim;i++){
        arr_temp[i]=arr[dim-1-i];
    }
    for (int i=0;i<dim;i++){
        arr[i]=arr_temp[i];
    }
}

int main(){
    int dim;
    cout << "Inserisci la dimensione dell'array: ";
    cin >> dim;
    int arr[dim];
    cout << "Inserisci gli elementi dell' array: ";
    for (int i=0;i<dim;i++){
        cin >> arr[i];
    }
    inverti_array(arr, dim);
    cout << "Ecco l'array invertito: [";
        for (int i=0;i<dim;i++){
        cout << arr[i] << ", ";
    }
    cout << "\b\b]";
    return 0;
}
```
> L'esecuzione del programma ha come risultato:

```cpp
Inserisci la dimensione dell'array: 3
Inserisci gli elementi dell' array: 3 6 9
Ecco l'array invertito: [9, 6, 3]
```

Creare un programma che, dopo aver chiesto all'utente di inserire la dimensione e gli elementi di un array, lo inverta e stampi il risultato finale. Utilizzare una funzione per l'inversione dell'array.

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

### [Assignment 5_5] Numero di doppie in una stringa

```cpp
#include <iostream>
#include <cstring>

using namespace std;

int main(){
   const int dim = 256;
   int len, j=0, contadoppie =0;
   char stringa1[dim], stringa2[dim], stringa_res[dim];
   cout << "Inserisci due frasi: " << endl;
   cin.getline(stringa1, dim, '\n');
   cin.getline(stringa2, dim, '\n');
   strcat(stringa1, " ");
   strcat(stringa1,stringa2);
   len = strlen(stringa1);
   for (int i=0;i<len;i++){
        if ((isalpha(stringa1[i])>0) || stringa1[i]==' '){
            stringa_res[j]=stringa1[i];
            j++;
        }
   }
   stringa_res[j]='\0';
   len = strlen(stringa_res);
   for (int i=0;i<len-1;i++){
        if(stringa_res[i]==stringa_res[i+1])
            contadoppie++;
   }
   cout << "Il numero di doppie e': " << contadoppie;
}



```
> L'esecuzione del programma ha come risultato:

```cpp
Inserisci due frasi:
questa e' una prova. Inserisco due frasi!!!!!
Per contare il numero di doppie. Saranno 11?
Il numero di doppie e': 2
```
Creare un programma che chieda all'utente di inserire due stringhe, le concateni, elimini tutti i caratteri non alfabetici, e conti il numero di doppie contenute nella stringa complessiva.


<aside class="notice">
Per concatenare due stringhe potete usare la funzione strcat(s,t).
</aside>

<aside class="notice">
Per vedere se un carattere è effettivamente una lettera dell'alfabeto, è possibile usare la funzione isalpha(c). La funzione restituisce 1 se è una lettera maiuscola, 2 se è una lettera minuscola, 0 se non è un carattere alfabetico.
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
<br>
<br>
<br>
<br>
<br>
<br>

## Sesta esercitazione - Array Bidimensionali - Ordinamento Array

### [Esercizio 6_0] - Moltiplicazione tra Matrici

```cpp
#include <iostream>

using namespace std;

const int dim = 3;

void riempiMatrice(int a[dim][dim]){
   for (int i=0;i<dim;i++){
        cout << "Riga " << i+1 << ": ";
        for (int j=0;j<dim;j++){
            cin >> a[i][j];
        }
   }
}

void stampaMatrice(int a[dim][dim]){
    for (int i=0;i<dim;i++){
        for (int j=0;j<dim;j++){
            cout << a[i][j] << " ";
        }
        cout << endl;
    }
}

void prodottoMatrici(int a[dim][dim], int b[dim][dim], int c[dim][dim]){
    for (int i=0;i<dim;i++){
        for (int j=0;j<dim;j++){
            c[i][j]=0;
            for (int k=0;k<dim;k++){
            c[i][j]=c[i][j] + a[i][k]*b[k][j];
            }
        }
    }
}


int main(){
   int a[dim][dim], b[dim][dim], c[dim][dim];

   cout << "Inserisci tutti gli elementi della matrice A: " << endl;
   riempiMatrice(a);
   cout << "La prima matrice e': " << endl;
   stampaMatrice(a);

   cout << "Inserisci tutti gli elementi della seconda matrice B: " << endl;
   riempiMatrice(b);
   cout << "La seconda matrice e': " << endl;
   stampaMatrice(b);

   prodottoMatrici(a, b, c);
   cout << "La matrice prodotto e': " << endl;
   stampaMatrice(c);
}

```
> L'esecuzione del programma ha come risultato:

```cpp
Inserisci tutti gli elementi della matrice A:
Riga 1: 1 2 3
Riga 2: 4 5 6
Riga 3: 7 8 9
La prima matrice e':
1 2 3
4 5 6
7 8 9
Inserisci tutti gli elementi della seconda matrice B:
Riga 1: 2 3 4
Riga 2: 3 4 5
Riga 3: 4 5 6
La seconda matrice e':
2 3 4
3 4 5
4 5 6
La matrice prodotto e':
20 26 32
47 62 77
74 98 122
```

Scriviamo un programma che chieda all'utente di inserire gli elementi due matrici quadrate di dimensione 3, e ne calcoli il prodotto.

<aside class="notice">
Anche gli array bidimensionali vengono sempre passati per riferimento.
</aside>

<aside class="notice">
Per implementare il prodotto tra matrici posso utilizzare tre cicli for annidati!
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
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

### [Esercizio 6_1] - Ordinamento con Algoritmo Selection Sort

```cpp
#include <iostream>
#include <ctime>
#include <cstdlib>

using namespace std;

void riempiArrRandom(int arr[], int dim){
    for (int i=0;i<dim;i++){
        arr[i]=rand()%100;
    }
}

void stampaArr(int arr[], int dim){
    cout << "[";
    for (int i=0;i<dim;i++){
        cout << arr[i] << ", ";
    }
     cout << "\b\b]\n";
}

void selectionSort(int arr[], int dim){
    for (int i=0;i<dim;i++){
        int indiceminimo = i;
        for(int j=i+1;j<dim;j++){
            if(arr[j]<arr[indiceminimo]){
                indiceminimo = j;
            }
        }
        int temp = arr[i];
        arr[i]=arr[indiceminimo];
        arr[indiceminimo]=temp;
    }
}

int main(){
    srand(time(NULL));
    int dim;
    cout << "Inserisci la dimensione dell'array: ";
    cin >> dim;
    int arr[dim];
    riempiArrRandom(arr, dim);
    cout << "Ecco l'array con numeri random: ";
    stampaArr(arr,dim);
    selectionSort(arr,dim);
    cout << "Ecco l'array con numeri ordinati: ";
    stampaArr(arr,dim);
}
```
> L'esecuzione del programma ha come risultato:

```cpp
Inserisci la dimensione dell'array: 100
Ecco l'array con numeri random: [62, 12, 10, 36, 4, 96, 82, 11, 73, 17, 3, 87, 42, 3, 2, 37, 4, 56, 38, 13, 96, 38, 76, 37, 73, 46, 67, 53, 55, 3, 62, 6, 54, 25, 67, 27, 71, 31, 74, 99, 15, 90, 40, 40, 18, 96, 12, 12, 14, 54, 43, 37, 67, 74, 18, 6, 97, 32, 38, 65, 32, 45, 71, 43, 19, 32, 85, 10, 69, 9, 59, 64, 39, 67, 21, 32, 54, 87, 69, 58, 60, 33, 68, 19, 9, 85, 90, 94, 76, 78, 79, 71, 25, 61, 55, 84, 85, 74, 1, 99]
Ecco l'array con numeri ordinati: [1, 2, 3, 3, 3, 4, 4, 6, 6, 9, 9, 10, 10, 11, 12, 12, 12, 13, 14, 15, 17, 18, 18, 19, 19, 21, 25, 25, 27, 31, 32, 32, 32, 32, 33, 36, 37, 37, 37, 38, 38, 38, 39, 40, 40, 42, 43, 43, 45, 46, 53, 54, 54, 54, 55, 55, 56, 58, 59, 60, 61, 62, 62, 64, 65, 67, 67, 67, 67, 68, 69, 69, 71, 71, 71, 73, 73, 74, 74, 74, 76, 76, 78, 79, 82, 84, 85, 85, 85, 87, 87, 90, 90, 94, 96, 96, 96, 97, 99, 99]
```

L' idea di base di questo algoritmo è semplice: si cercano successivamente i minimi dell'array.
Questo algoritmo "divide" di fatto l'array in due parti, la prima ordinata e le seconda non-ordinata, inizialmente la prima parte non conterrà alcun elemento.
L'algoritmo continuerà a cercherà il minimo tra gli elementi della parte non-ordinata e lo scambierà con il primo elemento della parte non ordinata, andando così ad aumentare di uno la dimensione della parte ordinata.
L'algoritmo termina quando la parte non-ordinata contiene un solo elemento, che sarà il massimo dell'array, e quindi l'array sarà completamente ordinato.

<aside class="notice">
Come l'algoritmo BubbleSort, la complessità computazione di quest'algoritmo è O(n^2)
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

### [Assignment 6_2] - Matrice Tabelline

```cpp
#include <iostream>

using namespace std;

int main(){
   [...]
   return 0;	
}
```
> L'esecuzione del programma ha come risultato:

```cpp
```
Memorizzare in un array bidimensionale 10 x 10 la tavola pitagorica, (quella delle tabelline!), e stampare il contenuto della matrice (nella prima riga si dovrà trovare la tabellina del 1: 1 2 3 4 5 6 7 8 9 10).

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

### [Assignment 6_3] - Somme righe e colonne

```cpp
#include <iostream>

using namespace std;

int main(){
   [...]
   return 0;	
}
```
> L'esecuzione del programma ha come risultato:

```cpp
```
Scrivere un programma che chieda allutente di inserire i valori di una matrice 4x4 e trovi la riga e la colonna con somma più alta. 

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


### [Assignment 6_4] - Triangolare superiore e inferiore

```cpp
#include <iostream>

using namespace std;

int main(){
   [...]
   return 0;	
}
```
> L'esecuzione del programma ha come risultato:

```cpp
```
Creare un programma che chieda allutente di inserire la dimensione di una matrice, la riempia con numeri random, la stampi e verifichi se la somma delle celle sopra la diagonale principale sia maggiore o minore della somma delle celle sotto la diagonale principale. 

<aside class="notice">
Usando indici diversi di cicli for si possono calcolare le due somme
</aside>

<aside class="notice">
Con le matrici, se la dimensione non è nota in fase di compilazione, non posso utilizzare funzioni. Vedremo poi alcune soluzioni con i puntatori che permettono di superare questo limite.
</aside>

<br>
<br>
<br>
<br>
<br>



### [Assignment 6_5] - Ordinamento con Insertion Sort

```cpp
#include <iostream>

using namespace std;

int main(){
   [...]
   return 0;	
}
```
> L'esecuzione del programma ha come risultato:

```cpp
```
Provare a scrivere un programma che implementi l'ordinamento di un array con algoritmo Insertion Sort. L'insertion Sort è un algoritmo di ordinamento che utilizza lo stesso metodo che un essere umano usa per ordinare le sue carte in mano. 

L'algoritmo ha bisogno di due cicli for, uno più esterno su tutti gli elementi dell'array, quello più interno per calcolare il nuovo indice in cui inserire l'elemento. 

Il passo successivo consiste nel far scorrere in avanti gli elementi dell'array, e inserire finalmente l'elemento nella posizione «corretta»

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


