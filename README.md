# 🎮 Khub

**Khub è il tuo launcher personale per videogiochi: tutti i tuoi giochi in un unico posto, con statistiche, instant replay, controller e tanto altro.**

Invece di aprire Steam, Epic Games e mille collegamenti diversi, apri Khub e trovi tutto lì: scegli un gioco, lo avvii, e Khub si occupa di tenere il conto di quanto giochi.

---

## ✨ A cosa serve

- 📚 **Raccogliere tutti i giochi** (Steam, Epic Games, Xbox, Ubisoft, `.exe` e collegamenti) in una sola libreria
- ⏱️ **Tenere traccia del tempo di gioco** in automatico
- 📊 **Vedere le statistiche**: ore giocate, giochi più giocati, grafici per giorno/settimana/mese
- 🎬 **Salvare gli ultimi secondi di gioco** con l'*Instant Replay* (come un replay istantaneo)
- 🕹️ **Usare il controller** (anche PS4/PS5) e la modalità *Big Picture* dal divano
- 🎁 **Guadagnare XP e livelli** mentre giochi, sbloccando colori, sfondi e regali

---

## 🧩 Cosa puoi fare con Khub

| Funzione | Cosa fa |
|---|---|
| **Libreria** | Tutti i tuoi giochi con copertine, ricerca, filtri (genere, piattaforma, stato, voto) e vista a griglia o lista |
| **Sincronizza** | Trova da solo i giochi installati e li aggiunge alla libreria |
| **Aggiungi gioco** | Aggiungi a mano qualsiasi gioco o programma |
| **Collezioni e preferiti** | Segna i preferiti con la stella e crea le tue collezioni |
| **Statistiche** | Tempo totale, giochi più giocati, confronto tra periodi, backlog (giochi mai avviati) |
| **La tua storia / Wrapped** | Un riepilogo annuale in stile *Spotify Wrapped* della tua vita da giocatore, da salvare e condividere |
| **Consigli** | Ti suggerisce cosa giocare dopo, in base ai tuoi generi preferiti |
| **Casuale** | Non sai cosa giocare? Lascia scegliere al caso |
| **Instant Replay** | Salva con un tasto gli ultimi secondi di gioco (serve ffmpeg, Khub aiuta a installarlo) |
| **Soundboard** | Fai partire suoni con una combinazione di tasti |
| **Controller** | Usa Khub col gamepad, con modalità **Big Picture** pensata per il divano |
| **Profilo e livelli** | Più giochi, più XP: sali di livello e riscuoti il regalo giornaliero |
| **Regali** | Mostra i giochi gratis del momento su Epic Games |
| **Discord** | Mostra sul tuo profilo Discord che stai usando Khub o a cosa stai giocando |
| **Personalizzazione** | Colori, sfondi, temi e lingua (🇮🇹 Italiano / 🇬🇧 English) |
| **Tutorial** | Un giro guidato all'avvio per scoprire tutte le funzioni |

> 🔒 I tuoi dati restano **sul tuo PC**: non viene inviato nulla online.

---

## 📁 I file del progetto

| File | A cosa serve |
|---|---|
| `Khub.pyw` | Il programma principale: avvia tutto (contiene il "motore" di Khub) |
| `index.html` | L'interfaccia principale (libreria, statistiche, impostazioni, Big Picture, ecc.) |
| `panel.html` | Il pannello dell'Instant Replay |
| `player.html` | Il lettore video per guardare i replay salvati |

> ⚠️ Tieni questi file **tutti nella stessa cartella**.

---

## 🚀 Come installarlo

### Requisiti
- **Windows** (consigliato: alcune funzioni, come l'Instant Replay, funzionano solo su Windows)
- **Python 3.9 o più recente** → [python.org](https://www.python.org/downloads/)

### Passaggi

1. **Scarica** questo repository (pulsante verde **Code → Download ZIP**) e scompattalo.
2. Apri il terminale nella cartella e installa le librerie:

   ```bash
   pip install pywebview
   ```

3. *(Facoltativo)* per le funzioni extra:

   ```bash
   pip install pillow pystray pypresence psutil hidapi
   ```

   | Libreria | Serve per |
   |---|---|
   | `pillow` | Copertine dei giochi |
   | `pystray` | Ridurre Khub nella barra delle applicazioni |
   | `pypresence` | Mostrare l'attività su Discord |
   | `psutil` | Riconoscere i giochi in esecuzione |
   | `hidapi` | LED del controller PlayStation |

4. **Avvia Khub** con doppio clic su `Khub.pyw` (si apre senza finestra nera), oppure:

   ```bash
   python Khub.pyw
   ```

Alla prima apertura parte un **tutorial** che ti mostra come usare il programma. 👋

---

## 🛠️ Come creare l'`.exe` *(facoltativo)*

Se vuoi un unico file eseguibile senza dover installare Python, puoi usare PyInstaller:

```bash
pip install pyinstaller
pyinstaller --noconsole --onefile --add-data "index.html;." --add-data "panel.html;." --add-data "player.html;." Khub.pyw
```

L'eseguibile si troverà nella cartella `dist`.

---

## 💾 Dove vengono salvati i dati

Libreria, statistiche e impostazioni sono salvate in una cartella fissa sul tuo PC (file `game_hub_data.json`), così **non perdi nulla** anche se sposti o aggiorni il programma.

---

## 🔄 Aggiornamenti

Khub può controllare da solo se è disponibile una nuova versione su GitHub e aggiornarsi.

---

## ❓ Problemi comuni

- **Non si apre** → controlla di aver installato `pywebview` e che i 4 file siano nella stessa cartella.
- **L'Instant Replay non funziona** → serve *ffmpeg*: Khub ti guida nell'installazione dalle Impostazioni.
- **Su Discord non compare nulla** → attiva "Condividi la mia attività" nelle impostazioni di Discord e in Khub.
- **Mancano delle librerie** → in *Impostazioni → Componenti* Khub rileva quelle mancanti e le installa con un clic.

---

## 🤝 Contribuire

Hai un'idea o hai trovato un bug? Apri una **Issue** o una **Pull Request**: ogni aiuto è benvenuto!

---

## 📜 Licenza

Aggiungi qui la licenza che preferisci (es. MIT).

---

<p align="center">Fatto con ❤️ da <b>K3KK09</b></p>
