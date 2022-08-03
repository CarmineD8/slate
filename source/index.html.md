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
const int dim = 10;

void stampaMatrice(int a[dim][dim]){
    for (int i=0;i<dim;i++){
        for (int j=0;j<dim;j++){
            cout << a[i][j] << " ";
        }
        cout << endl;
    }
}

int main(){
   int tabelline[dim][dim];
   for (int i=0;i<dim;i++){
        for (int j=0;j<dim;j++){
            tabelline[i][j]=(i+1)*(j+1);
        }
   }
   stampaMatrice(tabelline);
   return 0;
}
```
> L'esecuzione del programma ha come risultato:

```cpp
1 2 3 4 5 6 7 8 9 10
2 4 6 8 10 12 14 16 18 20
3 6 9 12 15 18 21 24 27 30
4 8 12 16 20 24 28 32 36 40
5 10 15 20 25 30 35 40 45 50
6 12 18 24 30 36 42 48 54 60
7 14 21 28 35 42 49 56 63 70
8 16 24 32 40 48 56 64 72 80
9 18 27 36 45 54 63 72 81 90
10 20 30 40 50 60 70 80 90 100
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
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
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
const int dim = 4;

int trovamax(int a[], int dim){
    int index_max = 0;
    for (int i=1;i<dim;i++){
        if (a[i]>a[index_max]){
            index_max=i;
        }
    }
    return index_max;
}

int main(){
   int a[dim][dim];
   int riga_max;
   int colonna_max;
   int sommarighe[dim]={0};
   int sommacolonne[dim]={0};

   cout << "Riempi una matrice quadrata 4 x 4 con numeri interi: " << endl;
   for (int i=0;i<dim;i++){
        cout << "Riga " << i+1 <<": ";
        for (int j=0;j<dim;j++){
            cin >> a[i][j];
        }
   }
   for (int i=0;i<dim;i++){
        for (int j=0;j<dim;j++){
            sommarighe[i]=sommarighe[i]+a[i][j];
            sommacolonne[i]=sommacolonne[i]+a[j][i];
        }
   }
    riga_max = trovamax(sommarighe, dim);
    colonna_max = trovamax(sommacolonne, dim);

    cout << "La riga con la somma piu' alta e' la : " << riga_max+1 << endl;
    cout << "La colonna con la somma piu' alta e': " << colonna_max+1 << endl;

   return 0;
}
```
> L'esecuzione del programma ha come risultato:

```cpp
Riempi una matrice quadrata 4 x 4 con numeri interi:
Riga 1: 1 2 3 4
Riga 2: 5 6 7 8
Riga 3: 2 3 4 5
Riga 4: 3 4 5 6
La riga con la somma piu' alta e' la : 2
La colonna con la somma piu' alta e': 4
```
Scrivere un programma che chieda all'utente di inserire i valori di una matrice 4x4 e trovi la riga e la colonna con somma più alta. 

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
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
#include <ctime>
#include <cstdlib>

using namespace std;

int main(){
    srand(time(NULL));
    int dim;
    int sum_sup=0, sum_inf=0;
    cout << "Inserisci la dimensione della matrice: ";
    cin >> dim;
    int a[dim][dim];
    for (int i=0;i<dim;i++){
        for (int j=0;j<dim;j++){
            a[i][j]=rand()%20;
            cout << a[i][j] << " ";
        }
        cout << endl;
    }
    for (int i=0;i<dim;i++){
        for (int j=i+1;j<dim;j++){
            sum_sup=sum_sup+a[i][j];
            sum_inf=sum_inf+a[j][i];
        }
    }
    if (sum_sup > sum_inf){
        cout << "La somma degli elementi della matrice triangolare superiore e' piu' alta" << endl;
    }
    else if (sum_sup < sum_inf){
        cout << "La somma degli elementi della matrice triangolare inferiore e' piu' alta" << endl;
    }
    else{
        cout << "Le due somme sono uguali" << endl;
    }
   return 0;
}
```
> L'esecuzione del programma ha come risultato:

```cpp
Inserisci la dimensione della matrice: 4
16 14 0 1
5 10 13 19
9 6 5 9
10 19 6 16
La somma degli elementi della matrice triangolare superiore e' piu' alta
```
Creare un programma che chieda all'utente di inserire la dimensione di una matrice, la riempia con numeri random, la stampi e verifichi se la somma delle celle sopra la diagonale principale sia maggiore o minore della somma delle celle sotto la diagonale principale. 

<aside class="notice">
Usando indici diversi si possono calcolare le due somme nello stesso ciclo for.
</aside>

<aside class="notice">
Con le matrici, se la dimensione non è nota in fase di compilazione, non posso utilizzare funzioni. Vedremo poi alcune soluzioni con i puntatori che permettono di superare questo limite.
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


### [Assignment 6_5] - Ordinamento con Insertion Sort

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

void insertionSort(int arr[], int dim){
    for (int i=1;i<dim;i++){
        int insertionpoint = i;
        int temp = arr[i];
        for (int j=i-1;j>=0;j--){
            if(arr[j]>arr[i])
                 insertionpoint = j;
        }
        for (int j=i-1;j>=insertionpoint;j--){
            arr[j+1]=arr[j];
        }
        arr[insertionpoint]=temp;
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
    insertionSort(arr,dim);
    cout << "Ecco l'array con numeri ordinati: ";
    stampaArr(arr,dim);
}
```
> L'esecuzione del programma ha come risultato:

```cpp
Inserisci la dimensione dell'array: 50
Ecco l'array con numeri random: [91, 9, 1, 13, 45, 46, 3, 79, 28, 75, 26, 89, 59, 87, 42, 93, 56, 52, 67, 1, 17, 47, 75, 99, 90, 54, 51, 64, 5, 49, 79, 38, 18, 90, 50, 90, 92, 26, 54, 82, 0, 37, 95, 31, 13, 27, 33, 35, 83, 48]
Ecco l'array con numeri ordinati: [0, 1, 1, 3, 5, 9, 13, 13, 17, 18, 26, 26, 27, 28, 31, 33, 35, 37, 38, 42, 45, 46, 47, 48, 49, 50, 51, 52, 54, 54, 56, 59, 64, 67, 75, 75, 79, 79, 82, 83, 87, 89, 90, 90, 90, 91, 92, 93, 95, 99]
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
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Settima esercitazione - File

### [Esercizio 7_0] - Lettura e scrittura su file

```cpp
#include <iostream>
#include <fstream>

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
    fstream ingr, usc1, usc2;
    ingr.open("ciao.txt", ios::in);
    usc1.open("vocali.txt", ios::out);
    usc2.open("consonanti.txt", ios::out);
    char a;
    while(!ingr.eof()){
        ingr >> a;
        if(isalpha(a)>0){
            if (controllo_vocale(a)==1){
                usc1 << a;
            }
            else{
                usc2 << a;
            }
        }
    }
    ingr.close();
    usc1.close();
    usc2.close();

    ingr.open("vocali.txt", ios::in);
    usc1.open("vocali.txt", ios::app);
    usc1 << endl;
    while(!ingr.eof()){
        ingr >> a;
        if (isalpha(a)==2){
            a = a - 32;
            usc1 << a;
        }
        else{
            a = a + 32;
            usc1 << a;
        }
    }
}

```

> L'esecuzione del programma ha come risultato:

```cpp
I nuovi file sono stati generati
```

Scrivere un programma che prende in input un file "ciao.txt" e crea due file chiamati "consonanti.txt" e "vocali.txt" in cui ci sono rispettivamente solo le consonanti o le vocali presenti nel file "ciao.txt".
Se il file "ciao.txt" contiene il testo "prova a fare l'esercizio", il file consonanti conterrà "prvfrlsrcz" mentre quello vocali conterrà "oaaaeeeiio".

Una volta creati i due file "consonanti.txt" e "vocali.txt", riapriamo il file vocali.txt, e aggiungiamo al testo già scritto, lo stesso testo invertendo lettere maiuscole con minuscole

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


### [Esercizio 7_1] - Lettura da file

```cpp
#include <fstream>
#include <iostream>

using namespace std;

int main()
{
    fstream fin("input.txt", ios::in);
    char a, a_back, c;
    cout << "inserisci il carattere ";
    cin >> c;
    int contatore1 =0;
    int contatore2 =0;
    if(!fin){
        cout << "Errore nell'apertura del file" << endl;
        return -1;
    }

    while(!fin.eof()){
        a=' ';
        fin >> a;
        if(c == a){
            contatore1++;
            if(a == a_back){
                contatore2++;
            }
        }
        a_back=a;
    }

    fin.close();
    cout << " Il carattere "<< c <<" e' presente "<<  contatore1 <<" volte" << endl;
    cout <<" Il carattere "<< c <<" e' presente per due volte consecutive "<<  contatore2 <<" volte";
}

```

> L'esecuzione del programma ha come risultato:

```
inserisci il carattere c
 Il carattere c e' presente 5 volte
 Il carattere c e' presente per due volte consecutive 2 volte
```

Scrivere un programma che ricevuto in ingresso un file chiamato "input.txt" e un carattere digitato da tastiera dall'utente restituisca tramite la console quante volte quel carattere compare in generale, e quante volte compare per due volte consecutive nel file "input.txt".

<aside class="notice">
Prima di tentare di leggere o scrivere un file, è sempre una buona idea verificare che sia aperto con successo. Si può verificare con if(!fin).
</aside>

<aside class="notice">
E' buona norma chiudere lo stream con la funzione close prima di uscire dal programma.
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

### [Esercizio 7_2] - Scrittura su file

```cpp
#include <fstream>
#include <iostream>

using namespace std;

int main()
{
    fstream fout("output.txt", ios::out);
    char a, a_back=' ';
    cout << "Inserisci i caratteri da scrivere nel file. Inserisci 0 per andare a capo, 00 per uscire" << endl;
    if (!fout){
        cout << "Errore nell'apertura del file " << endl;
        return -1;
    }
    while (1){
        cin >> a;
        if(a=='0')
        {
            if(a_back=='0')
                break;
            else
                fout << endl;
        }
        else{
            fout << a;
        }
        a_back = a;
    }
    fout.close();
}
```

> L'esecuzione del programma ha come risultato:

```
Inserisci i caratteri da scrivere nel file. Inserisci 0 per andare a capo, 00 per uscire
Dopo questa frase vado a capo
0
Chiudo il programma
00
```

Scrivere un programma che memorizza nel file "output.txt" quanto viene passato dall'utente via tastiera (un carattere per volta), andando a capo quando viene passato uno 0 (zero) e chiudendo il file e il programma quando vengono passati due zeri consecutivi.


<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

### [Esercizio 7_3] - File e array

```cpp
#include <fstream>
#include <iostream>

using namespace std;

int main()
{
    fstream fin("input.txt", ios::in);
    fstream fout("output.txt", ios::out);
    char c;
    int contaoccorrenze['z'-'a'+1]={0};
    if(!fin || !fout){
        cout << "Problema nell'apertura del file!" << endl;
        return -1;
    }

    while(!fin.eof()){
        c=' ';
        fin >> c;
        if((c>='a')&&(c<='z')) //se c è una lettera minuscola
        {
            int posizione=c-'a'; //individuo il numero progressivo della lettera nell'alfabeto
            contaoccorrenze[posizione]++; //conto uno in più per quella lettera
        }
        if((c>='A')&&(c<='Z')) //se c è una lettera maiuscola faccio la stessa cosa
        {
            int posizione=c-'A';
            contaoccorrenze[posizione]++;
        }
    }
    fin.close();

    for(int i=0;i<26;i++)
    {
        c='a'+i;
        fout<<c<<": "<<contaoccorrenze[i]<<endl;
    }
    fout.close();

    cout << "Il file e' stato generato!" << endl;
}

```

> L'esecuzione del programma ha come risultato:

```cpp
Il file e' stato generato!
```

Creare un programma che ricevuto in ingresso un file chiamato "input.txt" crei in uscita un file chiamato "output.txt" formato da tante righe quante sono le lettere dell'alfabeto e per ogni riga viene riportata una lettera e quante volte quella lettera compare nel file "input.txt".

<aside class="notice">
E' possibile creare un array di 26 interi, relativo ai contatori per le 26 lettere. Andando a leggere un carattere, è possibile incrementare l'elemento dell'array in posizione corretta utilizzando la codifica ascii.
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

## Ottava esercitazione - Strutture

### [Esercizio 8_0] - Strutture

```cpp
#include <iostream>

using namespace std;

struct libro
{
    int pagine;
    int codice;
    float costo;
};

libro inserisciLibro()
{
    libro l;
    cout << "inserisci il numero di pagine: ";
    cin >> l.pagine;
    cout << "inserisci il codice: ";
    cin >> l.codice;
    cout << "inserisci il costo: ";
    cin >> l.costo;
    return l;
}

void confrontaScambia(libro &la,libro &lb)
{
    if(la.costo/la.pagine>lb.costo/lb.pagine)
    {
        libro ltemp=la;
        la=lb;
        lb=ltemp;
    }
}

void stampaLibro(libro l)
{
    cout << "pagine " << l.pagine << " ";
    cout << "codice " << l.codice << " ";
    cout << "costo " << l.costo << " " << endl;
}

int main()
{
  libro l1,l2,l3;
  l1=inserisciLibro();
  l2=inserisciLibro();
  l3=inserisciLibro();
  confrontaScambia(l1,l2);
  confrontaScambia(l1,l3);
  confrontaScambia(l2,l3);
  stampaLibro(l1);
  stampaLibro(l2);
  stampaLibro(l3);
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Il file e' stato generato!
```

Creare la struttura libro, in cui ogni libro ha un codice numerico (numero intero) che lo caratterizza, un numero di pagine e un costo. Si memorizzino i dati di tre libri e si calcoli il costo medio per pagina dei libri e si stampino i dati dei tre libri in ordine crescente di costo per pagina.

Implementare l'esercizio utilizzando tre funzioni, inserisciLibro, confrontaScambia, stampaLibro.

<aside class="notice">
C++ permette di passare strutture come parametri attuali alle funzioni sia per valore sia per riferimento.
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

### [Esercizio 8_1] - Array di Strutture

```cpp
#include <iostream>
#include <fstream>
#include <cstring>

using namespace std;

const int dim = 256;

struct libro
{
    char titolo[dim];
    char autore[dim];
    char prezzo[dim];
    char pagine[dim];
};

int main()
{
  fstream fin("libri.txt", ios::in);
  if(!fin){
    cout << "Errore nell'apertura del file" << endl;
    return -1;
  }

  char temp[dim];
  int conta = -1;
  while(!fin.eof()){
    fin.getline(temp,dim,'\n');
    conta++;
  }
  libro inventario[conta];
  fin.close();
  fin.open("libri.txt", ios::in);
  int i = 0;
  while(!fin.eof()){
    fin.getline(inventario[i].titolo,dim,',');
    fin.getline(inventario[i].autore,dim,',');
    fin.getline(inventario[i].pagine,dim,',');
    fin.getline(inventario[i].prezzo,dim,'\n');
    i++;
  }
  fin.close();
  cout << "Di quale libro vuoi avere info?" << endl;
  cin.getline(temp, dim, '\n');

  int found = 0;
  for(int i=0;i<conta;i++){
    if (strcmp(temp,inventario[i].titolo) == 0){
        cout << "Il libro e' presente nel catalogo" << endl;
        cout << "Il suo autore e': " << inventario[i].autore << endl;
        cout << "Il libro ha " << inventario[i].pagine << " pagine" << endl;
        cout << "Il libro costa " << inventario[i].prezzo << endl;
        found = 1;
        break;
    }
  }
  if (found == 0){
    cout << "Il libro non e' in catalogo" << endl;
  }
}
```

> L'esecuzione del programma ha come risultato:

```cpp
Di quale libro vuoi avere info?
Il giovane Holden
Il libro e' presente nel catalogo
Il suo autore e':  J.D. Salinger
Il libro ha  225 pagine
Il libro costa  15
```

Scrivere un programma che prenda in ingresso un file di testo che descrive l'inventario di una libreria, con quattro campi: titolo del libro, autore, pagine, costo (vedi slide per l'esempio).

Il programma chiede quindi all'utente di inserire il titolo di un libro, restituendo le altre informazioni (autore, pagine, costo) se il libro e' presente nell'inventario.

<aside class="notice">
Nel caso di uno stream in lettura, è possibile usare la funzione getline per modificare il carattere terminatore della stringa.
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

### [Assignment 8_2] - Struttura Persona

```cpp
#include <iostream>

using namespace std;

const int dim = 256;

struct persona
{
    char nome[dim];
    int altezza;
    int eta;
    int peso;
};

int main()
{
  int num = 3;
  persona persone[num];
  for (int i=0;i<num;i++){
    cout << "inserisci il nome della persona " << i+1 << ": ";
    cin >> persone[i].nome;
    cout << "inserisci l'altezza: ";
    cin >> persone[i].altezza;
    cout << "inserisci l'eta': ";
    cin >> persone[i].eta;
    cout << "inserisce il peso: ";
    cin >> persone[i].peso;
  }
  int alt_max = 0;
  int eta_min = 0;
  for (int i=1;i<num;i++){
    if(persone[i].altezza > persone[alt_max].altezza){
        alt_max = i;
    }
    if(persone[i].eta < persone[eta_min].peso){
        eta_min = i;
    }
  }

  cout << "La persona piu' alta e': " << persone[alt_max].nome << endl;
  cout << "La persona piu' giovane e': " << persone[eta_min].nome << endl;
}

```

> L'esecuzione del programma ha come risultato:

```cpp
inserisci il nome della persona 1: Massimo
inserisci l'altezza: 170
inserisci l'eta': 31
inserisce il peso: 72
inserisci il nome della persona 2: Jane
inserisci l'altezza: 165
inserisci l'eta': 26
inserisce il peso: 57
inserisci il nome della persona 3: Mike
inserisci l'altezza: 160
inserisci l'eta': 23
inserisce il peso: 65
La persona piu' alta e': Massimo
La persona piu' giovane e': Mike
```

Il programma definisce una struct persona con campi nome, età, altezza e peso.
Successivamente, chiede all'utente di inserire i dati di tre persone. 
Infine, restituisce il nome della persona più alta e della persona più giovane.

<aside class="notice">
E' possibile risolvere l'esercizio con un array di strutture persona, o utilizzando tre struct persona. Utilizzando gli array, è però più semplice risalire alla persona più alta e quella più giovane.
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

### [Assignment 8_3] - Array di strutture e file

```cpp
#include <fstream>
#include <iostream>

using namespace std;

struct data
{
    int giorno;
    int mese;
    int anno;
};

int main()
{
    int dim = 5;
    data arrayDate[dim];
    fstream fin("date.txt", ios::in);
    for(int i=0;i<dim;i++)
    {
        fin>>arrayDate[i].giorno;
        fin>>arrayDate[i].mese;
        fin>>arrayDate[i].anno;
    }
    fin.close();

    data oggi;
    cout<<"inserisci la data di oggi ";
    cin>>oggi.giorno>>oggi.mese>>oggi.anno;

    int maggiorenni=0;
    for(int i=0;i<dim;i++)
    {
        if(oggi.anno-arrayDate[i].anno>18)
        {
            maggiorenni++;
        }
        else
        {
            if(oggi.anno-arrayDate[i].anno==18)
            {
                if(oggi.mese-arrayDate[i].mese>0)
                {
                    maggiorenni++;
                }
                else
                {
                    if(oggi.mese-arrayDate[i].mese==0)
                    {
                        if(oggi.giorno-arrayDate[i].giorno>=0)
                        {
                            maggiorenni++;
                        }
                    }
                }
            }
        }
    }

    cout<<"ci sono "<<maggiorenni<<" maggiorenni";
}

```

> L'esecuzione del programma ha come risultato:

```cpp
inserisci la data di oggi 14 12 2021
ci sono 3 maggiorenni
```

Il programma definisce una struct data che memorizza giorno, mese e anno.
Legge poi dal file input.txt 5 date di nascita (in ogni riga del file ci saranno giorno, mese e anno separati da spazi), fa inserire all'utente la data odierna e verifica quante date di nascita corrispondono a maggiorenni.

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Nona esercitazione - Puntatori

### [Esercizio 9_1] - Introduzione
```cpp
#include <iostream>
using namespace std;

int main()
{
#include <iostream>
using namespace std;

int main()
{
    // Dichiarazioni
    int a = 0; int b = 0;
    int c1 = 0; int c2 = 0; int c3 = 0; int c4 = 0;
	int& r = a;
    int* pa = &a; int* pb = &b;
    int** ppa = &pa;
    // Un puntatore a costante si può anche assegnare l'indirizzo di una variabile,
    // Ma non é vero il contrario: l'indirizzo di una costante può essere assegnato solo a un puntatore a costante.
    // In altre parole il C++ accetta conversioni da puntatore a variabile a puntatore a costante, ma non viceversa.
    const int* pca = &a;

    // Lettura di a e b
    cout << "Inserire due numeri interi: ";
	cin >> a >> b;

    // Stampa di a e b
    cout << "Hai inserito i seguenti valori: ";
	cout << *pa << " e " << *pb << endl;

    // Stampa dei valori dei puntatori pa e pb
    cout << "I puntatori pa e pb valgono: " << pa << " e " << pb << endl;

    // Stampa del valore di ppa
    cout << "Il puntatore a puntatore ppa vale: " << *ppa << endl;

    // Stampa a video del valore puntato dal puntatore puntato da ppa
    cout << "Valore della variabile puntata dal puntatore al quale punta ppa: " << **ppa << endl;

    // Stampa del valore puntato dal puntatore a costante
    cout << "Il valore puntato dal puntatore a costante ppc vale: " << *pca << endl;

    // Assegnamenti
    c1 = *pa;
    c2 = **ppa;
    c3 = *pca;
    c4 = r;
    cout << "Le variabili c1, c2, c3 e c4 hanno i seguenti valori: " << endl;
    cout << "c1: " << c1 << endl;
    cout << "c2: " << c2 << endl;
    cout << "c3: " << c3 << endl;
    cout << "c4: " << c4 << endl;

        // Svolgimento di operazioni su a
    a += 3;
    cout << "a adesso vale " << a << endl;
    *pa += 3;
    cout << "a adesso vale " << a << endl;
    **ppa += 3;
    cout << "a adesso vale " << a << endl;
    r += 3;
    cout << "a adesso vale " << a << endl;

    // Assegnamento di pa e ripetizione delle operazioni precedenti
    a = c1;
    pa = pb;
    a += 3;
    cout << "a adesso vale " << a << endl;
    *pa += 3;
    cout << "a adesso vale " << a << endl;
    **ppa += 3;
    cout << "a adesso vale " << a << endl;
    r += 3;
    cout << "a adesso vale " << a << endl;
    cout << "b adesso vale " << b << endl;

    // *pca += 5;
    // Non compila perché non posso modificare una variabile puntata da un puntatore a costante

	return 0;
}


```

Si scriva un programma C++ che operi come segue:

- Dichiari due variabili a e b di tipo intero e le inizializzi a zero.
- Dichiari quattro variabili c1, c2, c3 e c4 di tipo intero e le inizializzi a zero.
- Dichiari la variabile r di tipo riferimento ad intero e le assegni la variabile a.
- Dichiari le variabili puntatore pa e pb che puntino alle variabili a e b e la variabile puntatore ppa che punti al puntatore pa.
- Dichiari il puntatore a costante pca che punti alla variabile a.
- Legga da tastiera i valori di a e b e stampi a video i valori inseriti utilizzando i puntatori pa e pb.
- Stampi a video i valori di pa e pb. Che cosa viene stampato?
- Stampi a video il valore puntato da ppa. Che cosa viene stampato?
- Stampi a video il valore puntato dal puntatore al quale ppa punta. Che cosa viene stampato?
- Stampi a video il valore puntato da pca. Che cosa viene stampato?
- Assegni a c1 il valore puntato da pa, a c2 il valore puntato dal puntatore al quale punta ppa, a c3 il valore puntato da pca e a c4 il valore di r. Stampi quindi a video i valori di c1, c2, c3 e c4. Che cosa viene stampato? Perché?
- Sommi 3 ad a e stampi a video il valore di a; sommi 3 al valore puntato da pa e stampi a video il valore di a; sommi 3 al valore puntato dal puntatore al quale punta ppa e stampi a video il valore di a; sommi 3 a r e stampi a video il valore di a. Quale è l'effetto di queste operazioni sul valore della variabile a? Perché accade ciò che osserviamo nelle stampe dei valori di a dopo ciascuna operazione?
- Assegni ad a il valore di c1 e a pa il valore di pb e ripeta le operazioni le quattro operazioni svolte al punto precedente. Al termine stampi a video anche il valore di b. Che cosa è successo?  Perché accade ciò che osserviamo nelle stampe dei valori di a dopo ciascuna operazione e nella stampa finale del valore di b?
- Che cosa succederebbe se si provasse a sommare 5 al valore puntato dal puntatore pca?

<aside class="notice">
 Un puntatore a costante si può anche assegnare l'indirizzo di una variabile. Ma non é vero il contrario: l'indirizzo di una costante può essere assegnato solo a un puntatore a costante. In altre parole il C++ accetta conversioni da puntatore a variabile a puntatore a costante, ma non viceversa.
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

### [Assignment 9_2] - Aritmetica dei puntatori
```cpp
#include <iostream>
using namespace std;

int main(){

	const int dim = 20;
	int a[dim];
	int n = 0;

	for (int* p = a; p < (a + dim); p++)
		*p = 0;

    	// Acquisizione e verifica dell'input
	do {
		cout << "Inserire un numero intero compreso tra 3 e 5: ";
		cin >> n;
		if (n < 3 || n > 5)
			cout << "Attenzione: il numero deve essere compreso tra 3 e 5" << endl;
	} while (n < 3 || n > 5);

	for (int* p = a + n; p < (a + dim); p += n)
		*p = 1;

		// Stampa a video
	cout << "a = {";
	for (int* p = a; p < (a+dim); p++)
		cout << *p << ", ";
    cout << "\b\b}" << endl;

    char* pc;
	for (pc = (char*)a; pc < (char*)(a + dim); pc += 4)
		*pc = 10;
	cout << "a = {";
	for (int* p = a; p < (a+dim); p++)
		cout << *p << ", ";
    cout << "\b\b}" << endl;
    // Utilizzando un puntatore a char ci si sposta nell'array byte per byte.
	// Si può quindi modificare separatamente ciascuno dei 4 byte che compongono un numero
	// intero di tipo int. Il valore 10 viene quindi assegnato al quarto byte di ciascun
	// numero intero a[i] che pertanto diventa 0x0000000A (in rappresentazione esadecimale).
	// Tutti gli elementi di a assumono quindi valore pari a 10.

    for (pc = (char*)a; pc < (char*)(a + dim); pc += 2)
		*pc = 10;
	cout << "a = {";
	for (int* p = a; p < (a+dim); p++)
		cout << *p << ", ";
    cout << "\b\b}" << endl;
    // In questo caso il valore 10 viene assegnato al secondo e al quarto byte di ciascun
	// numero intero a[i] che pertanto diventa 0x000A000A (in rappresentazione esadecimale).
	// Tutti gli elementi di a assumono quindi valore pari a 655370.
}

```

Si scriva un programma C++ che operi come segue:

- Dichiari un array a di 20 numeri interi.
- Utilizzando l'aritmetica dei puntatori, inizializzi a zero tutti gli elementi dell'array a. 
- Chieda all'utente di inserire da tastiera un numero intero n compreso tra 3 e 5. Nel caso in cui il numero inserito non sia compreso in tale intervallo, il programma continuerà a chiedere all'utente di operare l'inserimento finché non venga inserito un numero compreso nell'intervallo richiesto.
- Utilizzando l'aritmetica dei puntatori, assegni il valore 1 a tutti gli elementi dell'array a il cui indice è pari al numero n inserito dall'utente o è un suo multiplo intero. 
-Stampi a video l'array a così modificato e termini.

Per approfondire:

- Dichiarare un puntatore a carattere pc e scandire l'array a utilizzando l'aritmetica dei puntatori applicata al puntatore pc. L'incremento di pc ad ogni iterazione sarà pari a 4. Inoltre, ad ogni iterazione si assegnerà il valore 10 all'elemento puntato da pc. Al termine della scansione, stampare a video l'array a così modificato. Che cosa viene stampato? Perché? Ripetere ora le operazioni sopra descritte, applicando ad ogni iterazione un incremento di pc pari a 2. Al termine della scansione, stampare nuovamente a video l'array a. Che cosa viene stampato? Perché?

<aside class="notice">
Utilizzando un puntatore a char ci si sposta nell'array byte per byte. Si può quindi modificare separatamente ciascuno dei 4 byte che compongono un numero intero di tipo int. Il valore 10 viene quindi assegnato al quarto byte di ciascun numero intero a[i] che pertanto diventa 0x0000000A (in rappresentazione esadecimale).Tutti gli elementi di a assumono quindi valore pari a 10.
</aside>

<aside class="notice">
Nel secondo caso, il valore 10 viene assegnato al secondo e al quarto byte di ciascun numero intero a[i] che pertanto diventa 0x000A000A (in rappresentazione esadecimale). Tutti gli elementi di a assumono quindi valore pari a 655370.
</aside>

<aside class="notice">
Attenzione: per poter compilare il programma così modificato occorre convertire esplicitamente i puntatori ad int in puntatori a char.
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

### [Assignment 9_3] - Passaggio di puntatori a funzione
```cpp
#include <iostream>
using namespace std;

void swap(int* a, int* b, int* c)
{
	int tmp = *b;
	*b = *a;
	*a = *c;
	*c = tmp;
}

void swap_2(int& a, int& b, int& c)
{
	int tmp = b;
	b = a;
	a = c;
	c = tmp;
}

int main ()
{
	int x, y, z;
	cout << "Inserire tre numeri interi" << endl;
	cout << "Primo numero: ";
	cin >> x;
	cout << "Secondo numero: ";
	cin >> y;
	cout << "Terzo numero: ";
	cin >> z;
	cout << endl;

	swap(&x, &y, &z);

	cout << "I valori ruotati sono" << endl;
	cout << "Primo numero: " << x << endl;
	cout << "Secondo numero: " << y << endl;
	cout << "Terzo numero: " << z << endl;
	cout << endl;

	// Parte 2
	swap_2(x, y, z);
	cout << "I valori ancora ruotati sono" << endl;
	cout << "Primo numero: " << x << endl;
	cout << "Secondo numero: " << y << endl;
	cout << "Terzo numero: " << z << endl;
	cout << endl;

	return 0;
}

// Se non si vogliono utilizzare i puntatori si può usare il passaggio per riferimento.
// In C++, in realtà, è consigliabile utilizzare il passaggio per riferimento
// anziché il passaggio per puntatore che deriva dal vecchio C.

```

Si scriva la funzione C++ swap che riceva come parametri i puntatori a tre numeri interi a, b e c e ne ruoti i valori, ovvero: a b viene assegnato il valore di a, a c viene assegnato il valore di b e ad a viene assegnato il valore di c. Si scriva quindi un programma C++ per verificare il corretto funzionamento della funzione. Il programma chiederà all'utente di immettere da tastiera tre numeri interi, chiamerà la funzione swap per ruotarne i valori e stamperà a video il risultato.

Esempio: se a vale 3, b vale 5 e c vale 10, dopo la chiamata alla funzione si avrà che a varrà 10, b varrà 3 e c varrà 5. 

Se non si volessero utilizzare i puntatori come si potrebbe re-implementare la funzione? Per verificarlo, scrivete una funzione swap_2 che scambi i valori senza usare i puntatori e utilizzatela nel programma sviluppato. Confrontate il codice dell'implementazione con i puntatori e di quella senza i puntatori. In che cosa si differenziano?

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


### [Assignment 9_4] - Puntatori e Matrici
```cpp
#include <iostream>
using namespace std;

const int dim = 3;

void righe_negative(int A[dim][dim], int* b[dim])
{
	for (int** parr = b; parr < (b + dim); parr++)
		*parr = NULL;

	int somma = 0; int** pb = b;
	for (int* p = &A[0][0]; p < &A[0][0] + (dim * dim); p += dim) {
		for (int* q = p; q < (p + dim); q++)
			somma += *q;
		if (somma < 0) {
			*pb = p;
			pb++;
		}
		somma = 0;
	}
}


int main()
{
	int matrice[dim][dim];
	int* prighe[dim];

	cout << "Inserire gli elementi di una matrice A (" << dim << " x " << dim << ")" << endl;
	for (int i = 0; i < dim; i++)
		for (int j = 0; j < dim; j++) {
			cout << "Elemento A[" << i << "][" << j << "]: ";
			cin >> matrice[i][j];
		}
	cout << endl;

	righe_negative(matrice, prighe);

	cout << "Righe con somma negativa:" << endl;
	int k = 0;
	while (prighe[k] != NULL && k < dim) {
		for (int h = 0; h < dim; h++)
			cout << *prighe[k]++ << " ";
		cout << endl;
		k++;
	}
	if (k == 0) cout << "Nessuna";
	cout << endl;



	return 0;
}

```

Si scriva la funzione C++ righenegative che riceva come parametri una matrice A di n righe e n colonne (n è dichiarato come una costante intera all'inizio del programma) e un array di puntatori a numeri interi b. L'array b è costituito anche esso dallo stesso numero costante n di elementi e la funzione lo inizializza in modo tale che tutti gli elementi siano NULL. La funzione scandirà la matrice A riga per riga ed inserirà nell'array b i puntatori alle righe per le quali la somma degli elementi risulta essere un numero negativo. Si scriva quindi un programma C++ per verificare il corretto funzionamento della funzione: il programma chiederà all'utente di immettere da tastiera gli elementi della matrice A, chiamerà la funzione righe_negative e stamperà a video le righe la cui somma degli elementi è un numero negativo.

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Decima esercitazione - Puntatori e Allocazione Dinamica della Memoria

### [Esercizio 10_1] - Puntatori a funzione
```cpp
#include <iostream>
using namespace std;

int maggiore(int a, int b)
{
	return a > b;
}

int minore(int a, int b)
{
	return a < b;
}

void scambia(int& a, int& b) 
{
	int t = a;
	a = b;
	b = t;
}

void bubble_sort(int v[], int n, int (*pf)(int, int))
{
	for (int i = n - 1; i >= 0; i--)
		for (int j = 0; j < i; j++)
			if (!(*pf)(v[j], v[j + 1]))
				scambia(v[j], v[j + 1]);
}

int main() 
{
	const int dim = 10;
	int w[dim];
	cout << "Inserire " << dim << " numeri interi: " << endl;
	for (int i = 0; i < dim; i++) {
		cout << "Valore " << i + 1 << ": ";
		cin >> w[i];
	}
	int scelta = 0;
	do {
		cout << "Come si vogliono ordinare i dati? " << endl;
		cout << "1 - In senso crescente" << endl;
		cout << "2 - In senso decrescente" << endl;
		cin >> scelta;
		switch (scelta) {
		case 1:
			bubble_sort(w, dim, minore);
			break;
		case 2:
			bubble_sort(w, dim, maggiore);
			break;
		default:
			cout << "Errore: scegliere 1 o 2" << endl;
		}
	} while (scelta != 1 && scelta != 2);
	cout << "Dati ordinati: " << endl << "{ ";
	for (int i = 0; i < dim - 1; i++)
		cout << w[i] << ", ";
	cout << w[dim - 1] << " } " << endl;
	return 0;
}
```

Si modifichi la funzione C++ bubbleSort, che implementa l'algoritmo di ordinamento BubbleSort, facendo in modo che possa gestire ordinamenti in senso crescente e decrescente. A tale scopo, la funzione bubbleSort riceverà come parametri un array di numeri interi v, la sua dimensione n e un puntatore pf a una funzione che riceva come parametri due numeri interi e restituisca come valore di ritorno un numero intero. La funzione puntata da pf restituisce 1 se l'ordine degli interi è corretto rispetto all'ordinamento prescelto e 0 altrimenti. Quindi la funzione bubbleSort chiamerà la funzione puntata da pf, passandole come parametri gli elementi v[j] e v[j + 1] dell'array v e li scambierà se la chiamata alla funzione puntata da pf restituirà 0.

Per implementare l'ordinamento nei due sensi avete le seguenti funzioni C++:- La funzione maggiore che riceva come parametri due numeri interi a e b e restituisca 1 se a è maggiore di b e zero altrimenti.- La funzione minore che riceva come parametri due numeri interi a e b e restituisca 1 se a è minore di b e zero altrimenti.

Si scriva, infine, un programma C++ che dichiari un array w di 10 numeri interi, chieda all'utente di inserirne i valori da tastiera, chieda all'utente di scegliere se desidera ordinare gli elementi di w in senso crescente o decrescente, chiami la funzione bubbleSort passando a pf la funzione maggiore nel caso di ordinamento decrescente e la funzione minore nel caso di ordinamento crescente e stampi a video il valore degli elementi dell'array ordinato.

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


### [Esercizio 10_2] - Allocazione dinamica della memoria
```cpp
#include <iostream>
using namespace std;

int maggiore(int a, int b) {
    return a > b;
}

int minore(int a, int b) {
    return a < b;
}

void scambia(int& a, int& b) {
    int t = a;
    a = b;
    b = t;
}

void bubble_sort(int v[], int n, int (*pf)(int, int)) {
    for (int i = n - 1; i >= 0; i--)
        for (int j = 0; j < i; j++)
            if (!(*pf)(v[j], v[j + 1]))
                scambia(v[j], v[j + 1]);
}

int main() {
    int n = 0;
    cout << "Quanti numeri si vogliono inserire? ";
    cin >> n;
    if (n <= 0)
        return -1;
    
    int* p = new int[n];
    if (p == NULL)
        return -1;
    
    for (int k = 0; k < n; k++) {
        cout << "Inserire il " << k + 1 << ".o numero della sequenza: ";
        cin >> p[k];
    }
    
    int scelta = 0;
    do {
        cout << "Come si vogliono ordinare i dati? " << endl;
        cout << "1 - In senso crescente" << endl;
        cout << "2 - In senso decrescente" << endl;
        cin >> scelta;
        switch (scelta) {
            case 1:
                bubble_sort(p, n, minore);
                break;
            case 2:
                bubble_sort(p, n, maggiore);
                break;
            default:
                cout << "Errore: scegliere 1 o 2" << endl;
        }
    } while (scelta != 1 && scelta != 2);
    
    cout << endl << "La sequenza ordinata e': " << endl;
    for (int s = 0; s < n; s++)
        cout << p[s] << " ";
    cout << endl;
    
    delete[] p;
    
    return 0;
}

```
Provate a implementare nuovamente il programma utilizzando la funzione bubbleSort sviluppata nell'esercizio 10_1, ma chiedendo all'utente di specificare quanti numeri costituiscono la sequenza. In questo caso, il programma riempirà l'array con i valori non ordinati inseriti dall'utente, chiederà all'utente se desidera operare un ordinamento in senso crescente o decrescente, chiamerà opportunamente la funzione bubbleSort e stamperà a video l'array ordinato.

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

### [Esercizio 10_3] - Puntatori a strutture
```cpp
#include <iostream>
#include <cmath>
using namespace std;

double prodotto_scalare(double* x, double* y, int n)
{
	double somma = 0;
	double* q = y;
	for (double* p = x; p < (x + n) && q < (y + n); p++) {
		somma += *p * *q;
		q++;
	}
	return somma;
}

// Implementazione alternativa, inserendo l'intera applicazione 
// dell'aritmetica dei puntatori nell'istruzine for
double prodotto_scalare_2(double* x, double* y, int n)
{
	double somma = 0;
	for (double* p = x, *q = y; p < (x + n) && q < (y + n); p++, q++)
		somma += *p * *q;
	return somma;
}

// Implementazione che calcola anche la distanza e restuisce
// l'output in una struttura passata come parametro di uscita
struct risultati {
	double prodotto;
	double distanza;
};

// Parte 2
void prodotto_scalare_e_distanza(double* x, double* y, int n, risultati* r)
{
	double somma = 0.0;
	double somma_quadrati = 0.0;
	double* q = y;
	for (double* p = x; p < (x + n) && q < (y + n); p++) {
		somma += *p * *q;
		somma_quadrati = (*p - *q) * (*p - *q);
		q++;
	}
	r->prodotto = somma;
	r->distanza = sqrt(somma_quadrati);
}

int main ()
{
	const int dim = 5;
	double a[dim], b[dim];

	cout << "Inserire due array, a e b, di " << dim << " numeri reali" << endl;
	for (int k = 0; k < dim; k++) {
		cout << "Inserire a[" << k << "]: ";
		cin >> a[k];
		cout << "Inserire b[" << k << "]: ";
		cin >> b[k];
	}
	cout << endl;

	cout << "Il prodotto scalare di: " << endl << "a = {" << a[0];
	for (int i = 1; i < dim; i++)
		cout << ", " << a[i];
	cout << "}" << " e" << endl << "b = {" << b[0];
	for (int j = 1; j < dim; j++)
		cout << ", " << b[j];
	cout << "}" << " e' " << prodotto_scalare(a, b, dim) << endl;
	cout << endl;
	
	// Parte 2
	risultati ris;
	prodotto_scalare_e_distanza(a, b, dim, &ris);
	cout << "Il prodotto scalare di: " << endl << "a = {" << a[0];
	for (int i = 1; i < dim; i++)
		cout << ", " << a[i];
	cout << "}" << " e" << endl << "b = {" << b[0];
	for (int j = 1; j < dim; j++)
		cout << ", " << b[j];
	cout << "}" << " e' " << ris.prodotto << endl;
	cout << "La distanza tra gli stessi due array vale " << ris.distanza << endl;
	cout << endl;
	
	return 0;
}

```

Si scriva la funzione C++ prodotto_scalare che riceva come parametri il puntatore px al primo elemento di un array di numeri reali, il puntatore py al primo elemento di un array di numeri reali e la dimensione comune n dei due array (un numero intero). Utilizzando l'aritmetica dei puntatori, la funzione dovrà scandire i due array e calcolarne il prodotto scalare, restituito come valore di ritorno (un numero reale). Si scriva quindi un programma C++ per verificare il corretto funzionamento della funzione. Il programma chiederà all'utente di immettere da tastiera i valori per i due array, chiamerà la funzione prodotto_scalare e ne stamperà a video il valore di ritorno.

Esempio: se l'array puntato da px vale {1.0, 3.0, 2.5, 0.0, 1.2} e l'array puntato da py vale {2.0, 1.0, 2.0, 3.8, 10.0} (si ha quindi n = 5), la funzione restituisce il valore del prodotto scalare dei due array, ovvero: 1.0 × 2.0 + 3.0 × 1.0 + 2.5 × 2 + 0.0 × 3.8 + 1.2 × 10.0 = 22.0.

Per fare di più: calcolare anche la distanza tra gli array puntati da px e da py e restituire, come parametro di uscita (anziché come valore di ritorno) una struttura che contenga due campi, il prodotto scalare e la distanza calcolati dalla funzione (due numeri reali). Modificare poi il programma di prova in modo che stampi entrambi i valori restituiti dalla funzione.

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

### [Esercizio 10_4] - Concatenamento e Ordinamento
```cpp
#include <iostream>
using namespace std;

int* append(int* pa, int* pb, int na, int nb) {
    int* p = NULL;
    if ((na + nb) > 0) {
        p = new int[na + nb];
        if (p != NULL) {
            int* p1 = pa; int* p2 = pb; int* p3 = p;
            while ((p1 < (pa + na)) || (p2 < (pb + nb)))
                if ((*p1 < *p2) && (p1 < (pa + na)))
                    *p3++ = *p1++;
                elif ((*p2 >= *p1) && (p2 < (pb + nb)))
                    *p3++ = *p2++;
        }
    }
    return p;
}

int check(int* pa, int n) {
    int* p = pa + 1;
    while (p < (pa + n)) {
        if (*p < *(p - 1))
            return 0;
        p++;
    }
    return 1;
}

void BubbleSort (int v[], int n) {
    int i, j, tmp;
    for (i = n - 1; i > 0; i--)
        for (j = 0; j < i; j++)
            if (v[j] > v[j+1]) {
                tmp = v[j];
                v[j] = v[j+1];
                v[j+1] = tmp;
            }
}

int main() {
    int n1 = 0;
    cout << "Primo array: quanti elementi si vogliono inserire? ";
    cin >> n1;
    if (n1 <= 0) return -1;
    int* p1 = new int[n1];
    if (p1 == NULL)
        return -1;
    for (int k = 0; k < n1; k++) {
        cout << "Inserire il " << k + 1 << ".o elemento del primo array: ";
        cin >> p1[k];
    }

    int n2 = 0;
    cout << "Secondo array: quanti elementi si vogliono inserire? ";
    cin >> n2;
    if (n2 <= 0) return -1;
    int* p2 = new int[n2];
    if (p2 == NULL)
        return -1;
    for (int h = 0; h < n2; h++) {
        cout << "Inserire il " << h + 1 << ".o elemento del primo array: ";
        cin >> p2[h];
    }
    BubbleSort(p1, n1);
    BubbleSort(p2, n2);
    int* p3 = append(p1, p2, n1, n2);

    for (int* p = p3; p < (p3 + n1 + n2); p++)
        cout << *p << " ";
    cout << endl;

    if (check(p3, n1 + n2))
        cout << "L'array e' ordinato! " << endl;

    delete[] p1;
    delete[] p2;
    delete[] p3;

    return 0;
}

```


Si scriva la funzione C++ append che concateni due array di numeri interi ordinati in senso crescente. La funzione riceve come parametri i puntatori a due array di numeri interi pa e pb e le loro dimensioni na e nb (due numeri interi) e restituisce come valore di ritorno il puntatore a un array di numeri interi. Si suppone che gli array puntati da pa e pb siano già ordinati in senso crescente. La funzione allocherà dinamicamente un array di (na + nb) elementi e vi copierà gli elementi degli array puntati da pa e pb in modo tale che l'array risultante sia a sua volta ordinato in senso crescente. La funzione restituirà infine il puntatore all'array risultante. Sarà responsabilità del programma chiamante deallocare la memoria allocata dalla funzione.

Si scriva quindi un programma C++ per verificare il corretto funzionamento della funzione. Il programma chiederà all'utente di immettere da tastiera le dimensioni nx e ny di due array di numeri interi, allocherà dinamicamente gli array e chiederà all'utente di inserire i valori per entrambi gli array. Il programma utilizzerà quindi l'algoritmo BubbleSort per ordinare entrambi gli array, chiamerà la funzione append e stamperà a video l'array concatenato risultante. Perché è più efficiente utilizzare la funzione append piuttosto che copiare semplicemente gli elementi dei due array di partenza nell'array risultante e poi utilizzare nuovamente BubbleSort sull'array risultante?

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Undicesima esercitazione - Allocazione Dinamica della Memoria, Funzioni Ricorsive e Template di Funzioni

### [Esercizio 11_1] - Allocazione Dinamica della Memoria
```cpp
#include <iostream>
using namespace std;

const int dim = 30;

struct oggetto{
    char nome[dim];
    double prezzo;
};

int main(){
    int num;
    cout << "Per favore, inserisci il numero di oggetti da inserire nell'inventario: " << endl;
    cin >> num;
    oggetto* object = new oggetto[num];
    if (object == NULL)
        return -1;
    for (oggetto* p = object; p < object+num;p++){
        cout << "Per favore, inserisci il nome dell'oggetto: " << endl;
        fflush(stdin);
        cin.getline(p->nome, dim,'\n');
        cout << "Per favore, inserisci il prezzo dell'oggetto: " << endl;
        cin >> p->prezzo;
    }
    char test;
    while(1){
        cout << "Vuoi inserire un altro oggetto? (s/n)" << endl;
        cin >> test;
        if (test =='n')
            break;
        oggetto* bigger_object = new oggetto[++num];
        if (bigger_object == NULL)
            return -1;
        oggetto* q =object;
        for (oggetto* p = bigger_object; p < bigger_object+num;p++){
            if (p<bigger_object+num-1){
                *p = *q;
                q++;
            }
            else{
                cout << "Per favore, inserisci il nome dell'oggetto: " << endl;
                fflush(stdin);
                cin.getline(p->nome, dim,'\n');
                cout << "Per favore, inserisci il prezzo dell'oggetto: " << endl;
                cin >> p->prezzo;
            }
        }
        delete [] object;
        object = bigger_object;
    }
    cout << "Ecco il tuo inventario: " << endl;
    for (oggetto* p = object; p < object+num;p++){
        cout << "Nome oggetto: " << p->nome << endl;
        cout << "Prezzo oggetto: " << p->prezzo << endl;
    }
    delete [] object;
return 0;
}

```
Creare una struttura per memorizzare l'inventario di un magazzino (nome oggetto, prezzo)

Scrivere il codice per far inserire N oggetti dall'utente, dove N è un numero a scelta dall'utente

Stampare l'inventario finale.


In aggiunta: Dopo aver fatto inserire un numero iniziale di oggetti, date la possibilità all'utente di inserire ulteriormente oggetti nell'inventario, finché non decide esplicitamente di uscire dal programma. Per fare questo, avrete bisogno di riallocare la memoria (creare una nuova struttura dati più grande, ricopiando i dati dal precedente array e facendo inserire i nuovi dati dall'utente)


<aside class="notice">
Provate ad usare l'aritmetica dei puntatori per gestire il riempimento dell'array e la stampa.

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


### [Esercizio 11_2] - Funzioni ricorsive
```cpp
#include <iostream>
using namespace std;

int potenza(int base, int esponente) {
	if (esponente > 0)
		return base * potenza(base, esponente - 1);
	else
		return 1;
}

double potenza2(int base, int esponente) {
	if (esponente > 0)
		return base * potenza2(base, esponente - 1);
	else if (esponente < 0)
		return (1.0 / base) * potenza2(base, esponente + 1);
	else
		return 1;
}

int main()
{
	int n = 0;
	int m = 0;
	char c = 'n';

	do {
		cout << "Inserire il valore della base: ";
		cin >> m;
		cout << "Inserire il valore dell'esponente: ";
		cin >> n;
		if (n >= 0)
			cout << m << " elevato alla " << n << " vale " << potenza(m, n) << endl;
		else
			cout << m << " elevato alla " << n << " vale " << potenza2(m, n) << endl;
		cout << endl;
		do {
			cout << "Continuare (s/n)? ";
			cin >> c;
			if (c != 's' && c != 'n')
				cout << "Attenzione: inserire s oppure n";
		} while (c != 's' && c != 'n');
	} while (c == 's');

	return 0;
}
```

Si scriva in C++ una funzione ricorsiva che, dati due numeri interi M ed N ricevuti come parametri, verifichi che N sia positivo o nullo (altrimenti, se N è negativo, la funzione termina restituendo -1), calcoli e restituisca come valore di ritorno la potenza M elevato a N (un numero intero). Si scriva quindi un programma C++ per verificare il corretto funzionamento della funzione. Il programma chiederà all'utente di inserire una tastiera due numeri interi, chiamerà la funzione e stamperà a video il suo valore di ritorno. Le operazioni si ripeteranno finché l'utente lo desidera.

Estendere poi la funzione in modo che possa ricevere un esponente negativo. In tal caso, la funzione restituirà il valore M elevato a (-N) = 1 / M^N.


<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


### [Esercizio 11_3] - Template di funzioni
```cpp
#include <iostream>
#include <cstring>
using namespace std;

template <typename T>
int contaDistinti2(T a[], int n, double f[]) {
	int c = 1;
	f[0] = 1.0 / n;
	for (int i = 1; i < n; i++) {
		f[i] = 1.0 / n;
		int t = 0;
		for (int j = 0; j < i; j++)
			if (a[j] == a[i]) {
				f[j] += 1.0 / n;
				f[i] += 1.0 / n;
				t = 1;
			}
		if (t == 0)
			c++;
	}
	return c;
}

int main()
{
	const int dim = 10;
	int v[dim] = { 0 };
	double w[dim] = { 0.0 };
	char s[dim] = "";
	double fr1[dim] = { 0 };
	double fr2[dim] = { 0 };
	double fr3[dim] = { 0 };

	char c = 'n';
	do {
		cout << "Inserire i valori per un array di " << dim << " numeri interi" << endl;
		for (int i = 0; i < dim; i++) {
			cout << "Inserire il valore in posizione " << i + 1 << ": ";
			cin >> v[i];
		}
		cout << "Inserire i valori per un array di " << dim << " numeri reali" << endl;
		for (int i = 0; i < dim; i++) {
			cout << "Inserire il valore in posizione " << i + 1 << ": ";
			cin >> w[i];
		}
		cout << "Inserire una stringa di " << dim << " caratteri" << endl;
		cin >> s;
		int l = strlen(s);
		cout << "Numero di elementi distinti: " << endl;
		cout << "Per l'array di numeri interi: " << contaDistinti2(v, dim, fr1) << endl;
		cout << "Frequenze degli elementi: {";
		for (int i = 0; i < dim - 1; i++)
			cout << fr1[i] << ", ";
		cout << fr1[dim - 1] << "}" << endl;
		cout << "Per l'array di numeri reali: " << contaDistinti2(w, dim, fr2) << endl;
		cout << "Frequenze degli elementi: {";
		for (int i = 0; i < dim - 1; i++)
			cout << fr2[i] << ", ";
		cout << fr2[dim - 1] << "}" << endl;
		cout << "Per la stringa di caratteri: " << contaDistinti2(s, l, fr3) << endl;
		cout << "Frequenze degli elementi: {";
		for (int i = 0; i < dim - 1; i++)
			cout << fr3[i] << ", ";
		cout << fr3[dim - 1] << "}" << endl;
		do {
			cout << "Desideri continuare (s/n)? ";
			cin >> c;
			if (c != 's' && c != 'n')
				cout << "Inserire s oppure n" << endl;
		} while (c != 's' && c != 'n');
	} while (c == 's');

	return 0;
}	
```

Si scriva il template di funzione C++ contaDistinti che riceva come parametri un array a di elementi di tipo T e la sua dimensione n (un numero intero), calcoli e restituisca come valore di ritorno il numero di elementi distinti contenuti nell'array a (un numero intero).
Si scriva quindi un programma per verificare il corretto funzionamento del template di funzione. Il programma chiederà all'utente di inserire da tastiera i valori per un array di 10 numeri interi, per un array di 10 numeri reali e per una stringa contenente al massimo 9 caratteri, chiamerà contaDistinti per ciascuno dei tre array e stamperà a video i tre valori di ritorno. Tali operazioni potranno essere ripetute finché l'utente lo desidera.

<aside class="notice">
Nota: per conoscere la dimensione effettiva della stringa inserita dall'utente, si può usare la funzione strlen disponibile nella libreria cstring.
</aside>

<aside class="notice">
Esempio: dato l'array a = {1, 3, 5, 6, 5, 2, 1, 5, 3, 6} (n = 10), la funzione restituirà 5. L'array a contiene cioè 5 valori distinti (per la precisione si tratta dei valori: 1, 2, 3, 5, 6). 
</aside>


Estendere poi il template di funzione contaDistinti in modo che riceva come parametro un ulteriore array f di numeri reali, della stessa dimensione dell'array a. La funzione assegnerà a ciascun elemento di f la frequenza del corrispondente elemento di a. La frequenza di un elemento di un array è definita come il numero di volte in cui l'elemento compare nell'array diviso per la dimensione dell'array. Nel caso dell'esempio di prima, l'array f sarà dunque il seguente: 

f = {0.2, 0.2, 0.3, 0.2, 0.3, 0.1, 0.2, 0.3, 0.2, 0.2}.

 L'elemento 1 compare cioè 2 volte su 10, l'elemento 3 compare 2 volte su 10, l'elemento 5 compare 3 volte su 10 e così via.

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Dodicesima esercitazione - Introduzione alle classi. Ancora puntatori e funzioni ricorsive

### [Esercizio 12_1] - Introduzione alle classi
```cpp
#include <iostream>
using namespace std;

// Classe rilevamento
class rilevamento {
public:
	rilevamento();
	rilevamento(double t, double p);
	rilevamento(double dati[2]);
	rilevamento(const rilevamento& r);
	void stampa_rilevamento();
private:
	double _temperatura;
	double _pressione;
};

 rilevamento::rilevamento()
{
	_temperatura = 0.0;
	_pressione = 0.0;
	cout << "Questo e' il costruttore di default" << endl;
}

 rilevamento::rilevamento(double t, double p)
{
	_temperatura = t;
	_pressione = p;
	cout << "Questo e' il costruttore con parametri" << endl;
}

 rilevamento::rilevamento(double dati[2])
{
	_temperatura = dati[0];
	_pressione = dati[1];
	cout << "Questo e' il costruttore con parametri" << endl;
}

 rilevamento::rilevamento(const rilevamento& r)
{
	_temperatura = r._temperatura;
	_pressione = r._pressione;
	cout << "Questo e' il costruttore di copia" << endl;
}

void rilevamento::stampa_rilevamento()
{
    cout << "Rilevamento: temperatura = "
		 << _temperatura << " C, pressione = "
		 << _pressione << " hPa" << endl;

}

int main()
{
	cout << "Parte 1: " << endl;
	rilevamento r1;
	r1.stampa_rilevamento();

	cout << "Parte 2: " << endl;
	rilevamento r2(15.0, 1060.0);
	r2.stampa_rilevamento();

	cout << "Parte 3: " << endl;
	double ril[2] = {20.0, 1065.0};
	rilevamento r3(ril);
	r3.stampa_rilevamento();

        cout << "Parte 4: " << endl;
	rilevamento r4(r1);
	r4.stampa_rilevamento();

    return 0;
}


```

Allo scopo di gestire l'acquisizione di dati da un sensore meteorologico che rileva la temperatura (misurata in gradi Celsius) e la pressione (misurata in hPa) dell'aria, si sviluppi in C++ la classe rilevamento avente i seguenti attributi: un numero reale _temperatura e un numero reale _pressione. Si implementino, inoltre, i seguenti metodi:

- Il costruttore di default che inizializzi a zero entrambi gli attributi. A scopo didattico, aggiungere nel corpo del costruttore la stampa a video del seguente messaggio: "Questo e' il costruttore di default della classe rilevamento".
 
- Un costruttore con parametri che riceva in ingresso (ovvero come parametri) due numeri reali t e p e inizializzi l'attributo _temperatura al valore di t e l'attributo _pressione al valore di p. Per semplicità, si assuma che i valori assunti da t e da p siano sempre validi. A scopo didattico, aggiungere nel corpo del costruttore la stampa a video del seguente messaggio "Questo e' il primo costruttore con parametri della classe rilevamento".

- Un costruttore con parametri che riceva in ingresso (ovvero come parametri) un array dati di due numeri reali e inizializzi l'attributo _temperatura al valore del primo elemento dell'array dati e l'attributo _pressione al valore del secondo elemento dell'array dati. Per semplicità, si assuma che i valori assunti dagli elementi dell'array dati siano sempre validi. A scopo didattico, aggiungere nel corpo del costruttore la stampa a video del seguente messaggio "Questo e' il secondo costruttore con parametri della classe rilevamento".

- Il costruttore di copia.  A scopo didattico, aggiungere nel corpo del costruttore la stampa a video del messaggio "Questo e' il costruttore di copia della classe rilevamento."

- La funzione stampa_rilevamento che stampi a video i valori degli attributi secondo il seguente formato:
"Rilevamento: temperatura = x C, pressione = y hPa" dove al posto di x e y vengono sostituiti i valori correnti degli attributi _temperatura e _pressione, rispettivamente. La funzione non restituisce alcun valore di ritorno.


Si scriva, infine, la funzione main che operi come segue:

- Dichiari un oggetto r1 di tipo rilevamento, stampando i valori di temperatura e pressione;

- Dichiari un oggetto r2 di tipo rilevamento, inizializzandolo con i valori 20.0 per la temperatura e 1000.0 per la pressione, stampando i valori di temperatura e pressione;

- Dichiari un array ril di due numeri reali, inizializzi i due elementi di ril rispettivamente ai valori 15.0 e 1010.0, stampando i valori di temperatura e pressione;

- Dichiari un oggetto r4 di tipo rilevamento, inizializzandolo come copia di r1, stampando i valori di temperatura e pressione;

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>



### [Esercizio 12_2] - Array di Puntatori a funzione
```cpp
#include <iostream>
#include <cmath>
using namespace std;

// restituisce true se e solo se n è numero primo
bool NumeroPrimo(int n) {
	int i=2, lim=(int)sqrt(n);
	bool primo = true;
	while (primo && (i <= lim)) {
		primo = !(n % i == 0);
		i++;
		}
	return(primo);
}

// restituisce la somma dei quadrati dei primi n numeri primi
long sommaquadratiprimi(int n) {
	int i=3, j=0, sommatoria=0;
	while (j <= n) {
		if (NumeroPrimo(i)) {
			sommatoria += i*i;
			j++;
		}
		i++;
	}
	return sommatoria;
}

// restituisce la somma dei cubi dei primi n numeri primi
long sommacubiprimi(int n) {
	int i=3, j=0, sommatoria=0;
	while (j <= n) {
		if (NumeroPrimo(i)) {
			sommatoria += i*i*i;
			j++;
		}
		i++;
	}
	return sommatoria;
}

int main() {
	int scelta, n;
	long(*vettpuntfunz[])(int) = {sommaquadratiprimi, sommacubiprimi};
	cout << "0 per calcolare la somma dei quadrati\n"
	     << "1 per calcolare la somma dei cubi\n";
	cin >> scelta;
	cout << "per quanti primi numeri primi?\n";
	cin >> n;
	cout << vettpuntfunz[scelta](n) << endl;
	return 0;
}
```

Scrivere un programma in c++ in grado di effettuare la somma dei quadrati o dei cubi degli n numeri primi (dove n è un numero inserito dall'utente, che può anche scegliere se effettuare la somma dei quadrati o dei cubi).

<aside class="notice">
Utilizzate un array di puntatori di funzioni.
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


### [Esercizio 12_3] - Puntatori e Matrici
```cpp
#include <iostream>
#include <ctime>
using namespace std;


bool MatriceSimmetrica(int mat[][2], int rig, int col) {
	for (int i=0; i<rig; i++)
		for (int j=0; j<col; j++)
			if (*(*(mat + i) + j) != *(*(mat + j) + i))
                return false;
    return true;
}

void RiempiMatrice(int mat[][2], int rig, int col) {
	srand(time(NULL));
	for (int i=0; i<rig; i++)
		for (int j=0; j<col; j++) *(*(mat + i) + j) = rand() % 3;
}

void StampaMatrice(int mat[][2], int rig, int col) {
	for (int i=0; i<rig; i++) {
		for (int j=0; j<col; j++) cout << *(*(mat + i) + j) << ' ';
		cout << endl;
	}
}

int main() {
    int matrice[2][2];
	RiempiMatrice(matrice,2,2);
	StampaMatrice(matrice,2,2);
	if (MatriceSimmetrica(matrice, 2, 2)) {
		cout << "Simmetrica" << endl;
	}
	else {
		cout << "Asimmetrica" << endl;
	}
return 0;
}
```

Scrivere un programma in c++ che decida se una matrice di numeri interi è simmetrica. 

Utilizzare una funzione di tipo bool, che riceva come input una matrice di interi, il suo numero di righe e quello delle colonne, e decida se la matrice è simmetrica

Un'altra funzione che generi la matrice in maniera casuale

Un'altra funzione che stampi la matrice

Nel main, chiamate la seconda e la terza funzione con n_righe = 2 e n_colonne = 2, e poi controllate se la matrice è simmetrica o meno

<aside class="notice">
Passare le matrici come puntatori e utilizzare l'aritmetica dei puntatori!
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

### [Esercizio 12_4] - Funzioni ricorsive
```cpp
#include <iostream>
#include <cstring>
using namespace std;

bool pal(char const *s, int cmin, int cmax) {
	if (cmin == cmax) 
		return true; // lunghezza dispari
	if (cmin == cmax-1) {         // lunghezza pari
		if (*(s+cmin) == *(s+cmax)) 
		    return true;
		else 
		    return false;
	}
	if (*(s+cmin) == *(s+cmax)) 
	    return pal(s, cmin+1, cmax-1);
	else 
	    return false;
}

bool palindroma(char const *s) {
	if(pal(s, 0, strlen(s)-1)) 
	    return true;
	else 
	    return false;
}

int main() {
	char stringa[100];
	cin >> stringa;
	if (palindroma(stringa)) 
	    cout <<"Palindroma";
	else 
	    cout <<"NON Palindroma";
}
```

- Scrivere una funzione ricorsiva che restituisca true se e solo se le viene passata come argomento una parola palindroma

- Nella funzione main, acquisire una parola e controllare che sia palindroma o meno

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
