# Analisi dei Requisiti


## Scopo del documento
Il seguente documento analizza il prodotto e il suo funzionamento, e si preoccupa di esplicitare tutte le caratteristiche che il sistema deve possedere per eseguire il suo scopo.
Ogni diversa iterazione tra un "utente" e il sistema è descritta in un caso d'uso, ad ogni caso d'uso descritto corrisponde un requisito che deve essere implementato nel sistema.


## Descrizione Prodotto
In questo esempio verrà descritto il funzionamento di una semplice applicazione per acquisti online in cui un utente, dopo essersi registrato, può inserire o rimuovere articoli dal carrello e procedere al pagamento.
Il proprietario del negozio può aggiungere o togliere articoli dall'applicazione.


## Attori
Un attore è una qualsiasi persona che si interfaccia con l'applicazione.
In questo caso possiamo riconoscere tre diversi tipi di attori:
* Utente non autenticato
* Utente autenticato
* amministratore

## Casi d'Uso

### CU1
Autenticazione

Attore: utente non autenticato  
precondizione: l'utente non è autenticato  
postcondizione: l'utente è autenticato  
scenario_1: l'utente è già registrato, inserisce il suo nome e la password e accede al suo account  
scenario_2: l'utente non è già registrato, allora entra sul form di registrazione   
  
estensioni: se i dati inseriti sono sbagliati viene restituita una risposta d'errore  

### CU1.1 
Registrazione

Attore: utente non autenticato  
precondizione: l'utente non è registrato  
postcondizione: l'utente è registrato  
scenario_1: l'utente sceglie nome e password e crea un account  


### CU2
Rimozione articolo

Attore: utente utenticato  
precondizione: il carrello contiene n elementi con n>0  
postcondizione: il carrello contiene n-1 elementi  
scenario: l'utente sceglie l'articolo che vuole rimuovere dal carrello e lo rimuove   

### CU3
L'amministratore rende disponibile un nuovo articolo

Attore: amministratore  
precondizione: l'articolo che si vuole inserire non è presente nel database dell'applicazione  
postcondizione: l'atricolo che si vuole inserire è presente  
scenario: l'amministratore inserisce i dati corrispondente all'articolo che vuole inserire e lo rende disponibile  
  
estensioni: se l'articolo è gia disponibile riceve un messaggio di errore  

## Tabella Requisiti

La seguente tabella contiente i codici di ogni requisito seguito da una descrizione, importanza e la fonte (cioè cosa ha scaturito la creazione del requisito).
il codice è composto nel modo seguente R|tipologia|codice_univoco|

tipologie:
* Funzionale= F
* Qualità= Q
* Vincolo= A
* Prestazionale = P
<pre>
CODICE    DESCRIZIONE       IMPORTANZA      FONTE  

RF1       autenticaz.       obbligatorio     CU1  
RF2       registraz.        obbligatorio     CU1.1  
RF3       rimozione         obbligatorio     CU2  
RF4       inserimento       obbligatorio     CU3  
RV1       usare python      desiderabile     Capitolato  
RQ1       pagamento cript.  obbligatorio     Capitolato  
RV2       file su github    obbligatorio     Decisione intern  
</pre>

