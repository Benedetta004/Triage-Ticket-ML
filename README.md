# Progetto di tesi Università Pegaso_ a.a 2025/2026_ Pw. 18_ Tema n.5_ Triage Ticket ML _ 0312300558
# Titolo: Sistema smistamento ticket

Nel presente repository è raccolta tutta la documentazione relativa all'elaborato, dedicato alla progettazione e allo sviluppo di un sistema per lo smistamento automatizzato dei ticket tramite la tecnica del Machine Learning. 

La traccia proposta dall'Ateneo richiede lo sviluppo di un prototipo minimale in grado di analizzare il testo di un ticket e di prevederne automaticamente:

- la _categoria_: quindi smistare tra gli uffici Amministrazione, Tecnico e Commerciale
- la _priorità_: tra alta, media e bassa

I tre componenti essenziali di questo progetto sono:

- _Dataset Sintetico_ : creato tramite un codice comporto da ticket brevi con lessico tipico delle categorie a cui fa riferimento   e etichette di priorità. Partendo da un template in formato .json e esportato in file .csv.
- _Pipeline Machine Learning_ : tramite preprocessing del testo, trasformazione tramite TF-IDF e l'addestramento di modelli di      classificazione basati sulla Logistic Regression.
- _Dashboard_ : interfaccia grafica sviluppata in Python, che permette di classificare un singolo ticket o batch da file .csv

# Requisiti

Per eseguire il progetto sono stati utilizzati:

- Python 3.14.4
- requirements.txt
- Visual Studio Code e Jupyter

# Indicazioni
Lo Script Script_Generazione_dataset_sintetico.py genera i seguenti output .csv, presenti nella cartella "Dataset utilizzati":

- dataset_ticket_mix.csv : contiene l'elenco dei ticket generati;
- dataset_ticket_test.csv : contiene i ticket da utilizzare per il test;
- dataset_ticket_train.csv : contiene i ticket da utilizzare per l'addestramento;
- dataset_ticket_valid.csv: contiene i ticket da utilizzare per la validazione.

Poiché la traccia dell'elaborato richiede la realizzazione di un prototipo riproducibile, per generare nuovi dataset bisognerà posizionare nella stessa cartella lo script Script_generazione_dataset_sintetico.py e il file tickets.json. 
La generazione di nuovi dataset risulterà diversa da quella utilizzata nell'elaborato in quanto lo script genera automaticamente nuove varianti.

##_ATTENZIONE!_ E' molto importante non modificare il nome del template .json.

# Addestramento Logistic Regression
Per il presente elaborato, sono stati realizzati e addestrati due modelli di Logistic Regression:

- ##Classificatore per categorie: addestrato per indirizzare ogni ticket nella categoria corretta tra Amministrazione,         Tecnico e Commerciale;
- ##Classificatore per priorità: addestrato per assegnare a ogni ticket una priorità tra alta, media e bassa.

Per entrambi i modelli sono stati realizzati utilizzando una pipeline che gestisce sia la trasformazione del testo in valori numerici, ma anche la classificazione tramite Logistic Regression. 
Per ripetere la fase di addestramento e valutare i modelli è possibile copiare i codici dei Notebook Jupiter. 

##N.B: Per addestrare i modelli sono stati utilizzati i dataset presenti nella cartella Dataset utilizzati/.

# Dashboard
Lo script che fa riferimento alla Dashboard è disponibile nella sezione "main".
La Dashboard è stata realizzata in Python utilizzando la libreria Tkinter per la gestione dell'interfaccia grafica, e permette d'inserire i dati relativi a un ticket e di ottenere, tramite i modelli addestrati precedentemente, la previsione della categoria e della priorità.

Per utilizzare lo script, sono necessari requirements.txt e i file .pkl (elencati qui sotto) che dovranno essere posizionati nella stessa cartella dello script:

- Logistic_Regression_definitiva_categorie.pkl
- Logistic_Regression_definitiva_priorita.pkl

Per l'analisi batch, il file .csv deve contenere almeno le colonne title e body. In caso di dimenticanza, la dashboard segnala la presenza di colonne mancanti tramite un apposito messaggio. 
Al termine dell'elaborazione batch viene generato un nuovo file .csv contenente le previsioni effettuate, inoltre è anche possibile scegliere la posizione in cui salvare il file. 

Per qualsiasi necessità o chiarimenti relativi al progetto benedettamarcellabaruzzi@studenti.unipegaso.it

Cordiali saluti.
