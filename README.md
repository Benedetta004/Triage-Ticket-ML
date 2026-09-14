# Triage-Ticket-ML
# Progetto di tesi Università Pegaso_ a.a 2025/2026_ Pw. 18_ Tema n.5_ Triage Ticket ML _ 0312300558
# Titolo: Sistema smistamento ticket

Nel presente repository è raccolta tutta la documentazione relativa all'elaborato, dedicato alla progettazione e allo sviluppo di un sistema per lo smistamento automatizzato dei ticket tramite la tecnica del Machine Learning. 

La traccia proposta dall'Ateneo richiede lo sviluppo di un prototipo minimale in grado di analizzare il testo di un ticket e di prevederne automaticamente:

- la _categoria_: quindi smistare tra gli uffici Amministrazione, Tecnico e Commerciale
- la _priorità_: tra alta, media e bassa

I tre componenti essenziali di questo progetto sono:

- Dataset Sintetico: creato tramite un codice comporto da ticket brevi con lessico tipico delle categorie a cui fa riferimento   e etichette di priorità. Partendo da un template in formato .json e esportato in file .csv.
- Pipeline Machine Learning: tramite preprocessing del testo, trasformazione tramite TF-IDF e l'addestramento di modelli di      classificazione basati sulla Logistic Regression.
- Dashboard: interfaccia grafica sviluppata in Python, che permette di classificare un singolo ticket o batch da file .csv

# Requisiti

Per eseguire il progetto sono stati utilizzati:

- Python 3.14.4
- requirements.txt
- Visual Studio Code e Jupyter

# Indicazioni
Lo Script Script_Generazione_dataset_sintetico.py genera i seguenti output .csv:

- dataset_ticket_mix.csv : contiene l'elenco dei ticket generati;
- dataset_ticket_test.csv : contiene i ticket da utilizzare per il test;
- dataset_ticket_train.csv : contiene i ticket da utilizzare per l'addestramento;
- dataset_ticket_valid.csv : contiene i ticket da utilizzare per la validazione.

