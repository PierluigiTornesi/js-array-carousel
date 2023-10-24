**Consegna:**
Dato un array contenente una lista di cinque immagini, creare un carosello come nello screenshot.
In allegato troverete markup con il codice html e css già fatti.

**MILESTONE 1**
Rimuoviamo tutto il markup statico e inseriamo tutte le immagini dinamicamente servendoci dell'array fornito e un semplice ciclo for che concatena un template literal.
Tutte le immagini saranno nascoste, tranne la prima, che avrà una classe specifica che la renderà visibile.
Al termine di questa fase ci ritroveremo con lo stesso slider stilato nella milestone 1, ma costruito dinamicamente attraverso JavaScript.

**MILESTONE 2**
Al click dell'utente sulle frecce, il programma cambierà l’immagine attiva, che quindi verrà visualizzata al posto della precedente.

**BONUS:**
Aggiungere il **ciclo infinito** del carosello. Ovvero se è attiva la prima immagine e l'utente clicca la freccia per andare all’immagine precedente, dovrà comparire l’ultima immagine dell’array e viceversa.

**Prima di partire a scrivere codice:**
Non lasciamoci spaventare dalla complessità apparente dell'esercizio, ma analizziamo prima, come abbiamo fatto sempre, cosa ci potrebbe aspettare.

**Consigli del giorno:**
1. Scriviamo sempre prima per punti il nostro algoritmo in italiano per capire cosa vogliamo fare
2. Al momento giusto (ihihhi starà a voi capire quale) rispondete a questa domanda: "Quanti cicli servono?"



### SOLUZIONE

**SLIDER**
1. Inserire le immagini dinamicamente
2. Al click sul pulsante up, mostrare l'immagine successiva
3. Al click sul pulsante down, mostrare l'immagine precedente

### Implementazione

**Dati**
Array di immagini    

**Logica**
1. Ciclo for per scrivere dinamicamente tutte le immagini contenenti dall'array
2. Mostrare le immagini
    1. La prima immagine sará visibile sin da subito grazie alla classe active
    2. Una volta cambiata immagine questa classe verrá tolta all'immagine attuale e passata a quella successiva o precedente, a seconda della freccia cliccata
3. Al click sulla freccia up:
    1. Se non ci troviamo all'ultima immagine : 
        1. Togliere la classe active per far sparire l'immagine attuale
        2. Incrementare l'indice
        3. Aggiungere la classe active per far apparire l'immagine successiva
    2. Altrimenti se ci troviamo all'ultima ricominciamo da capo: 
        1. Togliere la classe active per far sparire l'immagine attuale
        2. Impostare l'indice alla prima immagine dell'array
        3. Aggiungere la classe active per far apparire la prima immagine 

4. Al click sulla freccia down : 
    1. Se non ci troviamo alla prima immagine : 
        1. Togliere la classe active per far sparire l'immagine attuale
        2. Decrementare l'indice
        3. Aggiungere la classe active per far apparire l'immagine successiva
    2. Altrimenti se ci troviamo alla prima torno all'ultima 
        1. Togliere la classe active per far sparire l'immagine attuale
        2. Impostare l'indice all'ultima immagine
        3. Aggiungere la classe active per far apparire l'ultima immagine   