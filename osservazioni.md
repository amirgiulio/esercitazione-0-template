Componenti (Amir Giulietti, Gianmaria Giacco, amirgiulio, giacco2263606):

URL del repository condiviso: https://github.com/amirgiulio/esercitazione-0-template.git

Chi ha usato la tastiera nello step 1 e nello step 2: Un po' entrambi per entrambi gli step non avevamo capito.

Compilate insieme le osservazioni e discutete le risposte: entrambi dovete saper spiegare le prove svolte.



Passaggio 1 — Hello World: compilazione ed esecuzione
Comando di compilazione: gcc -std=c17 -Wall -Wextra -Wpedantic hello.c -o hello ./hello

Comando di esecuzione e risultato osservato:./hello

Che cosa ho capito su sorgente ed eseguibile: la sorgente e la parte di codice in questo caso scritta da noi su emacs, mentre l'esegubile è il codice tradotto in binario che il compilatore è in grado appunto di eseguire direttamente

Output richiesto e comportamento del programma prima della modifica: Il codice non da errori di compilazioni ma non stampa nulla poichè manca il printf

Esito dopo la modifica e spiegazione della correzione: che il programma stampa la frase richiesta

Passaggio 1 — Git
Quali file ho incluso nel commit e perché: hello.c in quanto modificato rispetto alla versione presente sul browsers e  osservazioni.md.

Come ho verificato che la versione provata sia presente su GitHub: con il comando " git log --oneline -5" eseguito da terminale viene fornito un codice alfanumerico, che deve poi essere confrontato nel browsers con il codice associato all'ultima versione caricata nel repository. Se coincidono la versione è presente su github

Che cosa ho osservato prima e dopo git pull, e perché non serve un nuovo clone: Dopo il git pull è possibile vedere dal terminale le modifiche effettuate dal browsers, non è necessario effettuare il nuovo clone in quanto quei file sono gia presenti nel nostro computer ma necessitano solo di essere aggiornati.

Passo 2 — Eco: prima prova
Argomenti passati, comando e risultato: Argomenti passati: Hello 42 3.14; Comando eseguito: ./programma Hello 42 3.14; Risultato ottenuto: Hello 42 3.140000

Che cosa posso concludere: Le funzioni atoi e atof hanno convertito  gli argomenti nei rispettivi tipi dati numerici (int e double).

Step 2 — Eco: seconda prova


Argomenti passati, comando e risultato: 

Passo 2 — Risultato ed errori

Argomenti passati, comando e risultato:Argomenti passati: testo 12 3.14; Comando eseguito: ./programma testo 12 3.14; Risultato ottenuto: testo 12 3.140000


Che cosa ho capito su testo, conversioni e stampa: gli elementi di argv non sono già numeri:
Gli elementi dell'array argv sono sempre stringhe di caratteri (tipo char *). Anche se l'utente inserisce "12" o "3.14", il programma li riceve inizialmente come testo. Per poterli utilizzare come numeri in calcoli o formattarli correttamente, è necessario convertirli esplicitamente in tipi numerici (int, double) usando funzioni come strtol e strtod (o atoi e atof). La printf userà poi i corrispondenti identificatori.


Previsioni per l'esecuzione con argomenti validi e per quella con dodici: Con argomenti validi (es. "testo 12 3.14"): Il programma converte correttamente i valori numerici, li stampa sullo standard output e termina con "dodici" al posto di un numero (es. "testo dodici 3.14"): Le funzioni di conversione falliscono (poiché "dodici" contiene lettere e non cifre). Il programma rileva l'errore, stampa un messaggio di errore esplicito su stderr e termina interrompendo l'esecuzione.


Contenuto dei messaggi nel terminale e dei codici di uscita osservati: Caso argomenti errati (es. ./programma testo dodici 3.14) e messaggio su stderr: "Il secondo argomento deve essere un intero in base 10 con codice di uscita (exit code): 2. Nel caso con numero di argomenti errato (es. ./programma testo 12) il messaggio su stderr: "Uso: ./programma TESTO INTERO REALE" con codice di uscita (exit code): 2


Come un controllo automatico può riconoscere un errore:
Un sistema di correzione o controllo automatico riconosce un errore valutando due aspetti principali: IL primo codice di uscita che verifica il valore restituito dal programma (es. echo $?). Se il codice è diverso da 0 (in questo caso 2), il controllo sa che si è verificato un errore. E poi con il flusso di errore standard (stderr) con cui il controllo cattura l'output del programma inviato a stderr invece che a stdout e lo confronta con il messaggio di errore atteso.

Fase 2 — Parametri e calcolo fisico


Passaggio 2 — Git
Come riconosco nella cronologia i commit dei due step:

Come ho verificato che la versione finale sia presente su GitHub:




Verifica commit completata con successo da GitHub







