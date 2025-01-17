# FRONTEND

## Descrizione

Questo documento serve a pianificare il frontend del progetto, dalla base alle cose più complesse.

Il frontend sarà composto da:

---

## Route 1: Home

### 1. HOME | DESIGN
Pagina vetrina della concessionaria, e possibilità di ricerca per marche e/o modello e/o caratteristiche dell'automobile.

La home sarà composta da:
- **Navbar**
- **Filtri**
- **Macchine**: quindi da utilizzare il GET per prendere i dati delle macchine migliori

### 2. BASIC FILTERS | LOGIC 
All'invio del filtraggio l'utente verrà riportato alla pagina dei filtraggi.
Filtri di base per la home:

#### PRESTAZIONI:
- Cilindrata
- Tipo di carburante
- Potenza (Kw)
- Cambio

#### GENERALI:
- Marca
- Modello
- Anno di produzione
- Tipo di veicolo
- Prezzo
- Garanzia
- Classe ambientale
- Disponibilità
- Immagine del veicolo

#### STRUTTURA:
- Colore
- Larghezza
- Lunghezza
- Peso
- Numero posti
- Numero porte

### 3. Click su una macchina | DESIGN
Paginazione per le macchine: dovrà mostrare i dettagli e gli optional della macchina selezionata. I dettagli della macchina verrà passato tramite props da home così da non dover fare un altro fetch e verrà inserito un bottone per rendirizzare l'utente alla casella di posta dove potrà contattare la concessionaria.

---

## Route 2: Sign in / Sign up

### 1. Sign in / Sign up | DESIGN and LOGIC
Paginazione form per login e registrazione (con redirect in home per l'utente registrato) conterrà i campi:
- Email*
- Password*
- Nome*
- Cognome*
- Data di nascita*
- Genere
- Numero di telefono
- Indirizzo

Saranno dei POST per la registrazione e per il login. Invieranno un JSON con i dati per la registrazione e per il login, e poi avranno un token per la sessione.

Questo token da parte di frontend dovrà essere salvato in un cookie o in localStorage, mentre il backend lo salva in un database. Quando si farà il logout, il cookie o localStorage dovranno essere svuotati e mandare un POST per il logout che cancelli il token dal database.

### 2. Utente Registrato | DESIGN
La Home dovrà mostrare in più:
- **Navbar**
- Le macchine salvate nei preferiti
- La casella di posta

---

## Route 3: Backoffice | DESIGN
La Home dovrà mostrare:
- **Navbar**
- Lista Macchine
- La casella di posta generale
- Aggiungere una Macchina

## Route 3.1: Add/Edit Cars | DESIGN
- Mostrare il form per aggiungere una macchina
- Mostrare il form per modificare una macchina
- Bottone per eliminare una macchina

## Route 3.2: Cars Messages | DESIGN
- Mostrare la macchina cliccata
- Mostrare i messaggi della macchina
- Casella di posta generale

Se sei il proprietario puoi:
- Eliminare un messaggio
- Visualizzare i messaggi
