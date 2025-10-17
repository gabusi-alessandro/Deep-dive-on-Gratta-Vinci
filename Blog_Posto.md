# Blog Post

In questo articolo parleremo dei Gratta&Vinci, il più famoso e diffuso gioco d’azzardo off-line giocato dagli Italiani.

Prima di iniziare la nostra analisi volevo riportare alcuni dati più generici sul gioco d’azzardo, una piaga che, purtroppo, risulta essere sempre più diffusa. 

Nel 2024 sono stati 157 i miliardi di euro spesi dagli italiani nel gioco d’azzardo, una cifra in crescita rispetto ai 150 miliardi del 2023 e che purtroppo è prevista ancora al rialzo per il 2025 con una stima di 160 miliardi spesi. 

![image.png](attachment:0262faff-34a7-47fc-b014-ae4ca02ce2f9:image.png)

Per dare una misura a questi soldi spesi andiamo a confrontarli con altre spese, che risultano molto di più di valore ma purtroppo anche molto inferiori rispetto a quelle per il gioco d’azzardo. Infatti le spese nel gioco hanno superato di 20 miliardi le spese per la sanità nel 2024, e sono quasi il triplo delle spese per l’istruzione. 

![image.png](attachment:0f4987e8-9de9-44b3-91c4-efc1b1f10fa7:image.png)

Viene poi fatto notare come il gioco d’azzardo, nel 2024, ha prodotto 9.2 miliardi di gettito erariale.

Per via di questo conflitto di interessi che ha lo stato, tra il benessere dei propri cittadini e le proprie entrate, mi è venuta voglia di fare questa analisi. 

Infatti dopo una domanda della mia dentista (*”Con quale gratta e vinci ho più probabilità di vincere 1000 euro”*), ho iniziato a ricercare tutte le probabilità di vincita dei singoli Gratta&Vinci. Ma per non rendere la mia ricerca legata ad una domanda alquanto banale ho deciso di andare più a fondo.

*Ci tengo a sottolineare che ho riferito alla mia dentista quale fosse il gratta e vinci con la maggior probabilità di vincere almeno 1 000€, ma sottolineando ripetutamente quanto questa possibilità fosse bassa (0.1% per il gratta e vinci “migliore”, che è più del doppio superiore a quella del secondo migliore) e come il gioco fosse a valore atteso negativo e che lei si sarebbe dovuta aspettare di perdere (spoiler) il 30% dei suoi soldi se avesse giocato regolarmente.* 

Portando avanti la mia ricerca è nata una domanda alle quali tenevo a rispondere: 

- *Lo stato approfitta dell’ignoranza dei cittadini? Assegna quindi maggiori probabilità di perdita ai tagli più diffusi?*

Prima di rispondere a questa domanda però andiamo ad osservare quelle che sono le statistiche, dati alla mano, di questi Gratta e Vinci. 

![WsfVl-media-per-gruppo (3).png](attachment:bcdd1a17-dc77-48a9-9ebf-10d646d0c951:WsfVl-media-per-gruppo_(3).png)

Dalla tabella vediamo che se consideriamo la media tra tutti i gratta e vinci disponibili abbiamo una percentuale di vittoria del ≈13.5% con una perdita percentuale sul costo del biglietto (`(valore atteso - costo) / costo`) pari a ≈-28.5%. 

Se pesiamo i biglietti in base al numero di biglietti prodotti per taglio queste statistiche vanno ulteriormente a peggiorare. Infatti la percentuale di vittoria scende al 13.35% e la perdita percentuale sale al 29.3%.

Voglio far notare anche come queste percentuali, sia di vittoria che di perdita, non siano equamente distribuite tra i vari gruppi di prezzo. Considerando la percentuale di vittoria infatti abbiamo valori che vanno dal ≈10% al ≈26%, con i valori più bassi distribuiti nei tagli più piccoli e i valori più alti nei tagli più elevati. 

Possiamo vedere la stessa distribuzione anche per la perdita percentuale con valori tra il -40% e -18%, dove i valori più negativi (*maggiori perdite sul giocato*) si concentrano nei tagli piccoli mentre quelli meno negativi si trovano nei tagli più grossi. 

<aside>

*In figura i due diagrammi a barre per % Vittoria (a destra) e Perdità% (a sinistra) dove si può notare l’asimmetria di queste distribuzione rispetto al prezzo dei Gratta&Vinci*

</aside>

![image.png](attachment:1646c037-1861-4f5d-b4ae-a0e4a8678883:image.png)

![image.png](attachment:33e9925b-52d6-4f3c-8d5b-dd4008f4016d:image.png)

Per andare a quantificare questa distorsione ho calcolato o il **rapporto di correlazione** (η²), un indice normalizzato (0 ≤ η² ≤ 1) che misura la dipendenza in media. In questo modo possiamo avere una visione quantitativa oltre che grafica di quella che è la dipendenza tra il gruppo (*costo del biglietto*) e la percentuale di vittoria,  o la perdita percentuale. 

*Prima di andare a riportare i valori trovati, volevo descrivere quella che è l’interpretazione del rapporto di correlazione in modo da permettere a tutti di poter pesare i dati che riporterò in seguito.* 

 *Come ho detto in precedenza l’indice è normalizzato è quindi i suoi valori sono sempre compresi tra 0 e 1.* 

*→ L’indice vale 0 quando le medie di tutti i gruppi sono uguali tra loro. In tal caso diremo che la **dipendenza è minima***

*→ L’indice vale 1 quando i valori di un gruppo sono tutti uguali tra loro (quindi pari alla media del gruppo), ma i valori tra i gruppi sono invece diversi tra loro. In questo caso diciamo che la **dipendenza è massima***

I dati rilevati sono stati:

- 0.88 per la **perdita %**
- 0.71 per la **% Vittoria**

In entrambi i casi la dipendenza tra il gruppo ed il valore di queste due statistiche, che avevamo già rilevato sia dalla tabella che dal diagramma a barre, è confermata anche dal rapporto di correlazione η². Infatti avendo quest’ultimo un valore vicino ad 1 indica una **forte dipendenza in media**.

---

### CORRELAZIONE

Ora è il momento di concentrarsi sull’analisi della correlazione tra le caratteristiche prese in analisi, ovvero:  [Costo, Valore Atteso, Perdita %, % Vittoria, Moltiplicatore (`Vincita Massima / Costo`), Somma Biglietti Venduti].  

Per prima cosa andiamo a vedere graficamente queste correlazioni tra tutte le caratteristiche considerate per poi andare a valutare nello specifico alcuni dati interessanti. 

![Matrice di Correlazione](attachment:cfa04c77-d0ba-4e2b-b031-963604e04734:image.png)

Matrice di Correlazione

![Matrice di Determinazione](attachment:be000a0b-ad63-4814-9587-54eb2a829dba:image.png)

Matrice di Determinazione

Anche dai due grafici heatmap possiamo notaro quanto detto fin ora, infatti notiamo una correlazione tra la Perdita % e il Costo pari a 0.8 che indica una forte correlazione, possiamo quindi concludere che all’aumentare del costo diminuisce la Perdita % (*la correlazione è positiva perché anche la Perdita % aumenta, nel senso che assume valori meno negativi*). 

Lo stesso possiamo vedere con la % Vittoria, in questo caso avremo una correlazione meno marcata, 0.59, ma comunque rilevante. 

![Retta di Regressione & Grafico a Dispersione Costo / Perdita %](attachment:ddc52db4-4440-4532-8c84-d9f24e0d5b9f:image.png)

Retta di Regressione & Grafico a Dispersione Costo / Perdita %

![Retta di Regressione & Grafico a Dispersione Costo / % Vittoria](attachment:68dfe3f4-fa27-4a16-9ea3-af63047015dd:image.png)

Retta di Regressione & Grafico a Dispersione Costo / % Vittoria

Osservando la **matrice di correlazione** si possono notare anche altre correlazioni rilevanti che voglio analizzare in maniera più dettagliata: 

1.  **Costo & Moltiplicatore Max**: tra queste due categorie c’è una forte correlazione positiva, pari a 0.72. Questo ci indica che all’aumentare del costo del biglietto aumenta anche aumenta anche la “leva”. Giocando quindi tagli più elevati possiamo aspettare di vincere, in proporzione al costo del biglietto, potenzialmente più soldi (*inteso come vincita massima*). 
    
    ![image.png](attachment:ed6fa54c-5919-4583-8a35-2909640d3ed6:image.png)
    
2. **Costo & Somma dei Biglietti**: questa volta abbiamo un esempio di due categorie negativamente correlate, con un valore di -0.33. Perciò possiamo affermare che all’aumentare del costo del biglietto diminuiscono i biglietti stampati dallo stato (*ma questo lo vedremo meglio in seguito*)
3. **Perdita % e Moltiplicatore Max**: in questo caso si verifica una situazione che ci potevamo aspettare, conoscendo già la correlazione tra Costo e Perdita e Costo e moltiplicatore potevamo già dedurre che all’aumentare del Moltiplicatore Max diminuisce la Perdita%. Ora sappiamo anche il valore di questa correlazione che è pari a 0.73 (*o -0.73 se consideriamo la perdita in valore assoluto*)
    
    ![image.png](attachment:ed12a6bb-5f80-4959-94e5-218a5545ce06:image.png)
    

Arrivati a questo punto è il momento di dire qualcosa in più rispetto alla nostra domanda iniziale. 

Grazie alle correlazioni possiamo dire che all’aumentare del costo vengono prodotti sempre meno biglietti (*cor -0.33*). Biglietti che però si rivelano essere quelli con le caratteristiche migliori (*o meno peggiori visto che il valore atteso resta comunque negativo*), infatti i biglietti più costosi sono quelli che manifesta una minore **perdita %**  e una maggiore **leva** rispetto al costo del biglietto. 

Ragionando in questo senso potrebbe sembrare che lo Stato vada effettivamente a penalizzare quelli che sono i tagli più piccoli e più prodotti quindi teoricamente più diffusi. 

*Altra parentesi che devo fare riguarda proprio la scelta di utilizzare i biglietti prodotti per verificare quelli che sono i Gratta&Vinci più venduti. Infatti non avendo trovato fonti affidabili che fornivano la spesa per ogni gruppo di costo ho deciso di calcolare la somma dei biglietti prodotti per ogni gruppo, presupponendo che lo stato vada a produrre in quantità maggiore i biglietti che vende maggiormente.*

### GRUPPI DI COSTO

Questa era però una conclusione troppo superficiale, pertanto ho deciso di approfondire ulteriormente la mia ricerca. Sono quindi andato a rappresentare graficamente la distribuzione dei biglietti stampati in base al costo. 

![image.png](attachment:5975c741-b88a-4549-8ed1-f74565483a31:image.png)

Notiamo chiaramente come il taglio più diffuso in assoluto sia quella da 5€ seguito poi dai tagli di 3€, 10€ e 2€. 

Riguardando la tabella iniziale ci accorgiamo di come il taglio più diffuso abbiamo caratteristiche pressoché identiche alla media, come si può osservare dalla tabella:

![image.png](attachment:85ba9e0e-aaa3-4203-9199-334413aa961d:image.png)

Se invece osserviamo gli altri tagli diffusi notiamo come i tagli da 2/3€, hanno caratteristiche peggiori rispetto alla media, cosa che potevamo già dedurre dall’analisi della correlazione vista in precedenza. 

Per quanto riguarda l’altro gruppo molto diffuso invece abbiamo valori leggermente migliori rispetto alla media per la % Vittoria e un discreto miglioramento per la Perdita %, anche questo un fatto che ci potevamo aspettare dalla correlazione analizzata in precedenza.

Grazie a queste osservazioni possiamo dire che lo il Gratta&Vinci più prodotto in assoluto, quello da 5€, ha caratteristiche pressoché identiche alla media. Mentre gli altri tagli più diffusi hanno valori leggermente peggiori (2€ e 3€). 

Potrebbe effettivamente sembrare che lo stato vada quindi a “sfruttare” l’ignoranza dei cittadini che consumano in quantità minore i tagli con le caratteristiche migliori, o forse sarebbe meglio dire “*meno peggiori*”. I tagli da 15 e 25€ infatti risultano essere i tagli di gran lunga migliori in termini di % Vittoria, ma sono anche i meno prodotti in assoluto. 

Vedendo questi dati mi è sembrato che più che essere lo stato a sfruttare i cittadini sono i cittadini a giocare in maniera completamente irrazionale. 

Infatti sembra inspiegabile la scelta di giocare i Gratta&Vinci da 5€. A dire il vero è già irrazionale giocare un gioco a valore atteso negativo con la convinzione di riuscire a vincere dei soldi, ma chiudiamo un occhio su questo aspetto, anche se sarebbe in realtà il principale da prendere in considerazione.

Prima di questa digressione stavamo valutando la scelta di prediligere i Gratta&Vinci da 5€ rispetto a tutti gli altri. Per andare a valutarla ho pensato a quelli che potrebbero essere i motivi per cui una persona è portata a giocare, e sono riuscito a trovarne due:

1. **Provare piacere nel giocare**: non capisco il senso di questo, ma magari a qualcuno potrebbe piacere proprio l’azione del grattare il Gratta&Vinci, e in questo una persona con un minimo di senso critico andrebbe a scegliere il Gratta&Vinci meno costoso in assoluto in modo da poter grattare più biglietti possibili spendendo una cifra prestabilità, oppure quello con la minor Perdita % in modo da “sprecare” meno soldi possibili in proporozione alla spesa per soddisfare la propria voglio di gioco. Ma come si può notare dal grafico i biglietti da 0.5€ o 1€ (*meno costosi*) non rientrano tra i più venduti e nemmeno quello con la minore Perdita % (*biglietto da 20€*) vi rientra. 
2. **Cercare di diventare ricco**: quest’altro è un motivo più comprensibile, e credo anche più diffuso, per giocare, ma se questo fosse il vero motivo del giocatore allora questo dovrebbe andare a massimizzare una di queste caratteristiche:
    - **% Vittoria**: non penso di dover spiegare il motivo per cui una persona dovrebbe scegliere di massimizzare questa categoria, se il suo obiettivo fosse appunto quello di vincere.
        
        Andiamo ancora i volta a riprendere i dati della tabella per vedere come il biglietto che la massimizza è quello da 25€ (*26.22%*) seguito da quello da 15€ (*23.64%*).
        
        Guardando la distribuzione dei biglietti comprati però ci accorgiamo che questi siano i due tagli meno diffusi in assoluto.
        
    - **Moltiplicatore Max**: un altro valore che una persona che vuole “*diventare ricca”* dovrebbe cercare di massimizzare è il Moltiplicatore Max. Andiamo quindi ad osservare i dati per vedere quali sono i gruppi che rispettano questa richiesta:
        
        ![image.png](attachment:19296133-4c5a-4b3b-b862-77b9a5498836:image.png)
        
        Dalla tabella è chiaro riscontare che i tagli “*migliori*” sotto questo aspetto sono quelli da 20 e 25.
        

### CONCLUSIONE

Dalle ultime valutazioni effettuate ci accorgiamo di come una persona in base al suo obiettivo dovrebbe essere portata ad acquistare i biglietti meno costosi (*0.5 / 1€*) per poter acquistare più biglietti possibili, nel caso in cui il suo scopo sia solamente quello di grattare fisicamente il biglietto. 

Oppure una persona potrebbe essere portata ad acquistare i biglietti che presentano le caratteristiche migliori in termini di Perdita %, % Vittoria oppure Moltiplicatore Max, e questi sono i Gratta&Vinci da 15, 20 oppure 25€, che però riosservando ancora una volta il grafico risultano essere i meno venduti. 

![image.png](attachment:b353cc69-9adc-4092-a965-ac9f14a26d94:image.png)

Il taglio da 5€ si rivela quindi essere il più diffuso senza spiccare in nessuna delle caratteristiche, solamente rispecchiando la media tra i pessimi tagli piccoli e i *meno negativi* tagli grandi. E a meno che i 5€ non siano la cifra esatta per la quale una persona è portata a non accettare maggiori perdite (*in valore assoluto ma non in percentuale*) in cambio di migliori caratteristiche la scelta di comprare un gratta e vinci da 5€ si rivela essere totalmente insensata, se non per seguire la moda nell’acquistare i nomi più popolari di questo (*pessimo, aggiungo io*) gioco. 

### FONTI

- https://www.ilsole24ore.com/art/giochi-italiani-puntano-653-miliardi-e-stato-ne-incassa-92-AHtUFdJB
- https://giocoresponsabile.info/statistiche-del-gioco/
- Dati:

https://docs.google.com/spreadsheets/d/1J9_jIcilzc8dFKPDT-3xjvC7_UOkXmkBhnURGe0aJvg/edit?usp=sharing

- https://colab.research.google.com/drive/1k3bPaoQu13drrg_mMVriZPu-O2GhoOhc → **Codice**
- https://www.datawrapper.de/
