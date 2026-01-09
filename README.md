# 🧠 ExcelNeuralNet: Rete Neurale Multistrato in Pure Formule

Questo progetto dimostra che Excel non è solo un software per tabelle, ma un motore di calcolo Turing-completo capace di ospitare un'**Intelligenza Artificiale (Deep Learning)** senza l'ausilio di script (VBA) o librerie esterne (Python/TensorFlow).

Il modello è un **Percevitore Multistrato (MLP)** progettato per il riconoscimento di pattern grafici (OCR) su una griglia 5x5.

---

### 🏗️ Architettura del Sistema
La rete segue una struttura classica **25-5-2**:
1.  **Input Layer (25 neuroni):** Riceve i pixel della griglia 5x5 (0 per bianco, 1 per nero).
2.  **Hidden Layer (5 neuroni):** Uno strato intermedio che estrae caratteristiche astratte (linee, curve, angoli).
3.  **Output Layer (2 neuroni):** Classifica l'input in due categorie (es. Numero "0" e Numero "1").

---

### ⚙️ Come Funziona (Il Motore Matematico)

#### 1. Forward Propagation (Il Calcolo)
Ogni neurone della rete esegue due operazioni:
*   **Somma Pesata:** Moltiplica ogni input per un "Peso" specifico e aggiunge un "Bias".
    *   Formula Excel: `MATR.PRODOTTO(Input; Pesi) + Bias`
*   **Funzione di Attivazione (Sigmoide):** Schiaccia il risultato in un intervallo tra 0 e 1 per simulare l'attivazione biologica di un neurone.
    *   Formula Excel: `=1 / (1 + EXP(-Valore))`

#### 2. Apprendimento (Backpropagation tramite Risolutore)
A differenza delle IA tradizionali che usano l'algoritmo di *Stochastic Gradient Descent*, questo modello sfrutta il **Motore Risolutore GRG Non Lineare** di Excel:
*   **Obiettivo:** Minimizzare l'errore quadratico medio (MSE) tra l'output della rete e il target desiderato.
*   **Variabili:** Il Risolutore modifica migliaia di volte i Pesi e i Bias finché la rete non "impara" a riconoscere i pattern corretti.

---

### 🛠️ Componenti del Progetto
*   **Foglio "Display":** L'interfaccia utente dove si disegna il numero. La formattazione condizionale trasforma i numeri in pixel neri.
*   **Foglio "Allenamento":** Il set di dati di addestramento. Contiene gli esempi che la rete ha usato per imparare.
*   **Foglio "Pesi":** Il vero "cervello". Qui sono memorizzati i valori numerici che determinano il comportamento della rete.

---

### 📈 Possibili Evoluzioni
*   Espansione a 10 neuroni di output per riconoscere tutte le cifre da 0 a 9.
*   Implementazione della funzione di attivazione **ReLU** per velocizzare l'addestramento.
*   Aumento della risoluzione della griglia a 10x10.

---
**Autore:** SaveaWolf02
**Data:** Gennaio 2026
**Tecnologie:** Excel, Algebra Matriciale, Ottimizzazione Non Lineare.
