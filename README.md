:pacco: CONSEGNA
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.

:roccia: MILESTONE 1
Dopo aver creato il progetto ragionate sui componenti e cercate di ricalcare quanto visto nei live coding di oggi e venerdì.
Come dati utilizzate l'array in allegato. Potete incollarlo nel vostro data, oppure importare il file come visto oggi.
Avrete un componente padre (es. CardsList) che dichiara l'array nel data e vi cicla per passare il singolo dato al figlio (es. SingleCard) tramite le sue props.

:roccia: MILESTONE 2
Spostate i dati in questione in uno store.js, all'interno di un array che chiamerete ad esempio carte.
Il componente padre (es. CardsList) richiama store.carte e vi cicla per passare il singolo dato al figlio (es. SingleCard).
Vi chiederete cosa cambia rispetto a prima? Cosa ci guadagno? Nulla! Ma ci tornerà utile per bonus con axios :occhiolino:

:regalo: BONUS
Recuperate questi dati tramite una chiamata axios da effettuare al mount dell'applicazione.
Per oggi possiamo importare axios tramite CDN, come al solito.
Questa chiamata andrà a scrivere su store.carte che quindi dovrà essere dichiarato come array vuoto nello store.js
L'api da richiamare si trova qui.

:regalo: BONUS #2
L'indirizzo che vi ho fornito stampa solo le prime 10 carte. Se volessi visualizzare le prime 20 carte? Oppure le prime 20 carte a partire dalla 15esima? Guardate bene l'indirizzo e fate qualche prova :occhiolino:
Qui trovate anche la documentazione delle API se volete capire bene quali dati aspettarvi.


Parte 2
:pacco: CONSEGNA
Continuate a lavorare nella stessa repo di ieri. Oggi gli obiettivi sono:
richiamare le card tramite axios (per chi non avesse fatto il bonus di ieri)
aggiungere una select per filtrare i risultati in base all’archetipo

:roccia: MILESTONE 0
Assicuratevi di aver completato la consegna di ieri inclusi i bonus: dovrete avere le cards all'interno di un array dello store. Questo array va popolato grazie ad una chiamata axios fatta al caricamento di App.vue.

:roccia: MILESTONE 1
Aggiungete una select in pagina per scegliere l'archetipo.
La select dovrà essere direttamente in App.vue e non in un componente. :avviso:
Le options della select verranno popolate dinamicamente, grazie a un array contenente tutti gli archetipi.
Dove prendo gli archetipi? Con un'altra chiamata, sempre al caricamento di App.vue ma a questo endpoint. I dati vanno sempre nello store.

:roccia: MILESTONE 2
Quando l'utente seleziona un valore dalla lista, dovrete aggiornare la lista di cards che avete in store.
Vuol dire che effettuerete una chiamata alle API (simile a quella iniziale) ma con l'archetipo selezionato.
:regalo: BONUS
Creare un componente che mostri il numero totale di risultati ottenuti.