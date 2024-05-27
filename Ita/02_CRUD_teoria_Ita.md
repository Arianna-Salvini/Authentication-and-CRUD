# Schema operazioni CRUD:

### 1. Create:
1. ***Routing***:
    definire le rotte per gestire la creazione di un nuovo tecord nel database

2. ***Controller***:
    creare un metodo nel controllor per gestire la logica di creazione del nuovo record

3. ***Form***:
    creare un form HTML per raccogliere i dati necessari per il nuovo record

4. ***Validazione***:
    definire le regole di validazione pe rgarantire che i dati inseriti nel form siano corretti

5. ***Salvataggio***:
    Nel controller, salvare i nuovo record nel database utilizzando il metodo appropriato

6. ***Risposta***:
    reindirizza l'utente a una pagina di conferma o mostra un messaggio di successo


### 2. R - Read:
1. ***Routing***: 
    Definire una route per recuperare i dati dal database e visualizzarli.

2. ***Controller***: 
    Creare un metodo nel controller per recuperare i dati dal database.

3. ***Modello***: 
    Utilizzare il modello corrispondente per interrogare il database e recuperare i dati desiderati.

4. ***Vista***: 
    Creare una vista per visualizzare i dati recuperati.

5. ***Presentazione***: 
    Utilizzare il linguaggio di template Blade per presentare i dati nella vista.


### 3. U - Update:
1. ***Routing***: 
    definire una route per gestire l'aggiornamento di un record esistente nel database.

2. ***Controller***: 
    creare un metodo nel controller per gestire la logica di aggiornamento del record.

3. ***Form***: 
    creare un form HTML precompilato con i dati del record esistente.

4. ***Validazione***:
    definire le regole di validazione per garantire che i dati inseriti nel form siano corretti.

5. ***Aggiornamento***:
    nel controller, aggiornare il record nel database utilizzando il modello appropriato.

6. **Risposta**:
    reindirizzare l'utente a una pagina di conferma o mostrare un messaggio di successo.


### 4. D - Delete:
1. ***Routing***: 
    definire una route per gestire l'eliminazione di un record esistente nel database.

2. ***Controller***: 
    creare un metodo nel controller per gestire la logica di eliminazione del record.

3. ***Conferma***: 
    chiedere all'utente conferma prima di eliminare il record. (BEST PRACTICE)

4. ***Eliminazione***: 
    nel controller, eliminare il record dal database utilizzando il modello appropriato.

5. ***Risposta***: 
    reindirizzare l'utente a una pagina di conferma o mostrare un messaggio di successo.