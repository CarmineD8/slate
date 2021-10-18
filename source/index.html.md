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

In questo corso, useremo [Code::Blocks](https://www.codeblocks.org/) per sviluppare i nostri programmi. Potete fare riferimento a queste slide [Prima Esercitazione](https://link-url-here.org) per alcune informazioni relative all'installazione dell'IDE.

# Esempi

## Esempi pratici - Prima esercitazione

### [Esercizio1_0] Programma "Hello World"


```cpp
#include <iostream>

int main() {
  // displays the string inside quotation
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


* `// Your First C++ Program`
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
Dobbiamo usare iostream per poter utilizzare std::cout
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
 

int main() {   
  
  ...
  ...
  
  return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
```

<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
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
 

int main() {   
  
  ...
  ...
  
  return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
```


<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
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
 

int main() {   
  
  ...
  ...
  
  return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
```


<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
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
 

int main() {   
  
  ...
  ...
  
  return 0;
}
```

> L'esecuzione del programma ha come risultato:

```cpp
```


<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>


