# dice-tracker
Ecco una bozza per il file `README.md` per il tuo progetto su GitHub. È strutturata per essere chiara, professionale e leggibile, ideale per documentare un'analisi statistica.

Puoi copiare e incollare questo contenuto direttamente nel file `README.md` della tua repository.

-----

# Analisi Statistica — Gioco dei Dadi

Questo repository contiene l'analisi statistica, le strategie ottimali e i dati storici relativi a un gioco di dadi basato su probabilità. Lo studio mira a identificare la strategia vincente per minimizzare il punteggio finale in un contesto di 4-6 giocatori.

## 🎲 Regole del Gioco

L'obiettivo è ottenere la somma più bassa possibile lanciando 3 dadi.

  - **Valori dei dadi:** {0, 1, 2, 3, 5, 6} (Nota: il valore 4 vale 0).
  - **Meccanica:**
    1.  Primo lancio: 3 dadi.
    2.  Rilancio: Dopo il primo lancio, è obbligatorio confermare almeno 1 dado; si possono rilanciare fino a 2 dadi.
    3.  Vincitore: Chi ottiene la somma più bassa.
  - **Variante:** Se il primo tiro totalizza 18, si vince automaticamente il turno.

## 🧠 Strategia Ottimale

L'analisi probabilistica definisce una "soglia critica" basata sul valore atteso di un dado (EV ≈ 2.83).

### Regole Operative

1.  **Soglia universale:** Rilancia qualsiasi dado che mostra 3, 5 o 6. Tieni i dadi con 0, 1 o 2.
2.  **Primo lancio:**
      - Se tutti i dadi mostrano ≤ 2: **FERMATI**.
      - Se uno o più dadi mostrano ≥ 3: tieni i valori ≤ 2 e rilancia gli altri.
3.  **Caso 2+2+2:** Anche se i dadi sono "alla media", la scelta statisticamente migliore è fermarsi (EV 6).

## 📊 Dati e Statistiche

L'analisi si basa su **145 turni reali** raccolti tra il 19/03/2026 e il 27/03/2026.

| Metrica                         | Valore                  |
| :------------------------------ | :---------------------- |
| **Media vincente globale**      | 2.117                   |
| **Mediana**                     | 2.0                     |
| **Probabilità di vittoria ≤ 2** | \~60% (con 4 giocatori) |
| **Probabilità di vittoria ≤ 1** | \~82% (con 4 giocatori) |

## 📈 Insight Chiave

  - **Il numero 2 è il benchmark:** È il punteggio vincente più frequente (37% dei casi). Arrivare a 2 è l'obiettivo minimo per essere competitivi.
  - **Trend di apprendimento:** I dati mostrano un trend decrescente nelle medie vincenti, segno che i giocatori stanno ottimizzando progressivamente la propria strategia.
  - **Asimmetria:** La distribuzione dei risultati è fortemente spostata verso il basso, confermando che il gruppo applica efficacemente le strategie di rilancio.

## 📂 Struttura del Repository

  - `/data`: Contiene i fogli di calcolo (`Dadi_Dice.xlsx`) con i dati grezzi dei turni.
  - `/docs`: Documentazione dettagliata delle analisi probabilistiche.

-----

*Analisi basata su 145 turni reali e calcolo probabilistico esatto su 216 combinazioni.*
