# FRec: Modellazione della Fatica dell’Utente nei Sistemi di Raccomandazione Sequenziali

Questo repository contiene una riproduzione semplificata del modello proposto nel paper:

> **FRec: Modeling User Fatigue for Sequential Recommendation**  
> *Nian Li, Xinyue Zhao, Yuhang Chen, Pengjie Ren, Zhaochun Ren, Jun Ma, Maarten de Rijke*  
> [arXiv:2405.11764](https://arxiv.org/abs/2405.11764)

## 📌 Obiettivo

FRec è un modello di raccomandazione sequenziale progettato per affrontare il problema della **"fatica dell’utente"**, ovvero la perdita di interesse verso contenuti troppo simili raccomandati consecutivamente.

Il modello combina:
- Modellazione **sequenziale** delle interazioni utente-item;
- Un componente di **penalizzazione della ripetizione** (modulo di fatica);
- Una **funzione di perdita con regolarizzazione** per evitare raccomandazioni ridondanti.

---

## 🧱 Architettura del Modello

Il modello è strutturato come segue:

- **Embedding Layer**: trasforma ID di item in vettori numerici.
- **GRU / RNN Layer**: cattura la sequenza temporale delle interazioni.
- **Fatigue Layer**: calcola una penalizzazione per item recentemente già visti.
- **Dense Layer**: produce le predizioni finali sul prossimo item da raccomandare.

---

## 📂 Struttura del Progetto


## 📊 Dataset consigliati

I dataset usati nel paper originale non sono pubblici, ma FRec può essere testato su dataset aperti:

- [MovieLens 1M](https://grouplens.org/datasets/movielens/1m/)  
- [Amazon Reviews Dataset](https://nijianmo.github.io/amazon/index.html)  
- [RetailRocket Dataset](https://www.kaggle.com/datasets/retailrocket/ecommerce-dataset)

Troverai gli script di preprocessing nella cartella `data/`.

---

## 🚀 Come iniziare

### 1. Clona il repository
```bash
git clone https://github.com/tuo-utente/frec-riproduzione.git
cd frec-riproduzione
