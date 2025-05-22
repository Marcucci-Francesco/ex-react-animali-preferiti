EX - Animali preferiti
===
Il tuo collega, probabilmente distratto da un gatto o un pappagallo, ha creato una pagina HTML statica invece di utilizzare React come richiesto. La pagina è già online, quindi non possiamo rifarla da zero. Ora tocca a te trasformarla in una meraviglia interattiva usando React, direttamente all’interno del documento HTML. Segui le milestone e dimostra che anche un errore può diventare un’opportunità per brillare!
## Consegna
1. Milestone 1: Inserire un Componente React
- Monta un componente React all’interno dell’elemento con classe .lista-animali.
- Il componente deve includere:
Un elemento <details> con titolo "Animali", che contiene:
Una lista <ul> statica che viene creata a partire da un array di stringhe (animals) dove ciascuna stringa rappresenta il nome di un animale.
Obiettivo: Mostrare la struttura base della lista di animali con un <details> che può essere espanso o contratto.
2. Milestone 2: Aggiungere Animali Casuali
- Trasforma l’array animals usando useState (l’array è inizialmente vuoto).
- Aggiungi un bottone "Aggiungi Animale" sopra il <details>.
- Cliccando il bottone, un animale casuale viene aggiunto alla lista.
- Usa un array predefinito per scegliere casualmente:
const animalsChoices = ["Cane", "Gatto", "Pappagallo", "Cavallo", "Panda"];
- L’animale selezionato deve essere aggiunto all’interno della lista <ul> come <li>.
Obiettivo: L’utente può vedere gli animali aggiunti dinamicamente nella lista.
3. Milestone 3: Usare una Modale per Aggiungere Animali
- Espandilo affinché:
La vecchia prop content può essere usata per passare un componente qualsiasi.
Un nuovo div in fondo alla modale contiene il bottone Annulla e un nuovo bottone Conferma.
Una nuova prop onConfirm si aspetta una funzione per gestire l’azione di conferma.
- Sostituisci l’aggiunta casuale dell’animale con una modale interattiva:
Cliccando il bottone "Aggiungi Animale," si apre una modale.
La modale include un input di testo (passato al prop content) per inserire il nome di un animale.
Conferma: Aggiunge l’animale alla lista e chiude la modale.
Annulla: Chiude la modale senza modificare la lista.
## Bonus 
1. Bonus: Utilizzare l'API per Creare Card
- Utilizza l'API:
/animals?search=[animalName]
per effettuare una ricerca dell'animale basata sul contenuto dell'input: 
Sostituisci [animalName] con il valore inserito dall'utente.
Assicurati di gestire lo stato di caricamento mentre l'API è in fase di risposta (mostra un messaggio come "Caricamento...").
- Dal primo risultato restituito dall'array (se presente), crea un oggetto che abbia queste proprietà:
name: Il nome dell'animale.
description: La descrizione dell'animale (o un messaggio predefinito come "Descrizione non disponibile" se manca).
image: L'immagine dell'animale (usa un'immagine di default se non è disponibile).
- Aggiungi l'oggetto alla lista degli animali e visualizzalo come una card, con:
Titolo: Il nome dell'animale.
Immagine (se presente).
Descrizione.
- Gestione degli errori:
Se la ricerca non restituisce risultati, informa l'utente con un messaggio di errore. (es.: "Nessun animale trovato")
Mostra un messaggio in caso di problemi di rete o altri errori. (es.: "Errore durante la ricerca dell'animale")
Obiettivo: Permetti agli utenti di aggiungere animali specifici utilizzando l'API per ottenere informazioni, mostrando eventuali errori in modo chiaro.
