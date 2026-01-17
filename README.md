# 🎵 SpotyStream by alebirra - Overlay Spotify

**La guida completa per mostrare la musica che stai ascoltando nelle tue dirette streaming**

> 📺 Perfetto per streamer, YouTuber, podcaster e content creator

---

## 📖 Indice

1. [Cos'è SpotyStream](#cosè-SpotyStream)
2. [Cosa Ti Serve](#cosa-ti-serve)
3. [Setup Iniziale - Passo per Passo](#setup-iniziale---passo-per-passo)
4. [Come Configurare l'Overlay](#come-configurare-loverlay)
5. [Guida Completa alle Funzionalità](#guida-completa-alle-funzionalità)
6. [Aggiungere l'Overlay in OBS](#aggiungere-loverlay-in-obs)
7. [Preset](#-preset-preset-rapidi)
8. [Risoluzione Problemi](#risoluzione-problemi)
9. [Domande Frequenti (FAQ)](#domande-frequenti-faq)
10. [Contatti e Supporto](#contatti-e-supporto)

---

## Cos'è SpotyStream

SpotyStream è un **overlay grafico** che mostra in tempo reale la musica che stai ascoltando su Spotify durante le tue dirette streaming su piattaforme come Twitch, YouTube, Facebook Gaming, ecc.

**Cosa vedranno i tuoi spettatori:**
- 🎨 Copertina dell'album (come disco in vinile o card moderna)
- 🎵 Titolo della canzone
- 👤 Nome dell'artista
- ⏱️ Tempo trascorso / durata totale
- 📊 Barra di progresso della canzone
- ▶️ Stato di riproduzione (Playing / Paused)

**Perché è utile:**
- Rende le tue dirette più professionali
- I tuoi spettatori possono scoprire nuova musica
- Aggiunge un tocco visivo dinamico alle tue stream
- Completamente personalizzabile con oltre 50 opzioni

---

## Cosa Ti Serve

### 🔧 Software Necessario

1. **OBS Studio** (gratuito)
   - Download: https://obsproject.com/
   - Compatibile con Windows, Mac e Linux
   - È il programma per fare streaming

2. **Spotify** (account gratuito o Premium)
   - Download: https://www.spotify.com/
   - Deve essere installato sul PC (non basta il browser)

3. **Un Browser Web** (Chrome, Firefox, Edge, Safari, ecc.)
   - Per configurare l'overlay

### 📱 Account Necessari

1. **Account Spotify** (gratuito o Premium)
2. **Account Spotify Developer** (gratuito)
   - Serve per creare un'app che collega Spotify all'overlay
   - Non preoccuparti, è semplicissimo e lo spieghiamo passo per passo

---

## Setup Iniziale - Passo per Passo

### Fase 1: Creare l'App Spotify (IMPORTANTE - FAI QUESTO PER PRIMO)

Questa è la parte più importante. **Leggi con attenzione e segui ESATTAMENTE questi passaggi.**

#### Passo 1.1 - Accedi al Dashboard Spotify Developer

1. Apri il browser
2. Vai su: https://developer.spotify.com/dashboard
3. Clicca su **"Log In"** in alto a destra
4. Inserisci le credenziali del tuo account Spotify
5. Se ti chiede di accettare i termini di servizio, clicca su **"Accept"**

#### Passo 1.2 - Crea una Nuova App

1. Clicca sul pulsante verde **"Create app"** (o "Crea app")
2. Ti si aprirà un modulo. Compila così:

   **App name** (Nome app):
   ```
   SpotyStream Overlay
   ```
   *(puoi mettere il nome che vuoi, non cambia nulla)*

   **App description** (Descrizione app):
   ```
   Overlay per mostrare la musica in streaming
   ```
   *(anche qui, scrivi quello che vuoi)*

   **Website** (Sito web):
   ```
   https://alebirra.github.io/spotify-obs/
   ```
   *(metti questo esattamente come scritto)*

   **Redirect URI** (URI di reindirizzamento):
   ```
   https://alebirra.github.io/spotify-obs/overlay.html
   https://alebirra.github.io/spotify-obs/config.html

   ```
   ⚠️ **IMPORTANTE**: Devi scrivere ESATTAMENTE questi indirizzi, uno alla volta. Anche una lettera sbagliata e non funzionerà!
   
   Clicca sul pulsante **"Add"** o **"Aggiungi"** per confermare il Redirect URI.

   **Quale API usi?** (Which API/SDKs are you planning to use?):
   - Seleziona tutte le spunte

3. Leggi e accetta i termini di servizio spuntando la casella
4. Clicca su **"Save"** (Salva)

#### Passo 1.3 - Copia il Client ID

1. Dopo aver salvato, ti apparirà la schermata della tua app
2. Vedrai una scritta **"Client ID"** seguita da una serie di lettere e numeri
3. Clicca sul pulsante **"Copy"** (o sull'icona 📋) accanto al Client ID
4. Il Client ID è stato copiato! **NON CHIUDERE QUESTA PAGINA**, ti servirà tra poco

> 💡 **Nota**: Il Client ID è una specie di "password" che permette all'overlay di collegarsi al tuo account Spotify. Non condividerlo con nessuno!

---

### Fase 2: Configurare l'Overlay

Ora che hai il Client ID, configuriamo l'overlay!

#### Passo 2.1 - Apri il Configuratore

1. Apri una nuova scheda del browser
2. Vai su: https://alebirra.github.io/spotify-obs/config.html
3. Ti si aprirà una pagina con tantissimi controlli. 😊

#### Passo 2.2 - Collega Spotify

Nella pagina dell'overlay vedrai un box grigio con scritto **"Setup Required"** (Configurazione Richiesta).

1. **Trova il campo "Client ID"**
   - È il primo campo che vedi nel box grigio
   - Dice: "Paste your Spotify Client ID"

2. **Incolla il Client ID**
   - Clicca nel campo
   - Premi `Ctrl+V` (Windows/Linux) o `Cmd+V` (Mac) per incollare
   - Vedrai apparire la serie di lettere e numeri che hai copiato prima

3. **Salva il Client ID**
   - Clicca sul pulsante verde **"Save Client ID"**
   - Ti apparirà un messaggio: "Saved! Now click Connect to Spotify"

4. **Connetti a Spotify**
   - Clicca sul pulsante blu **"Connect to Spotify"**
   - Si aprirà una nuova pagina di Spotify che ti chiede di autorizzare l'app
   - Clicca su **"Accetta"** o **"Accept"**
   - Verrai reindirizzato alla pagina dell'overlay

5. **Verifica che Funzioni**
   - Apri Spotify sul tuo PC
   - Fai partire una canzone qualsiasi
   - Nella pagina dell'overlay dovresti vedere apparire la copertina, il titolo e l'artista!

🎉 **COMPLIMENTI! Hai collegato Spotify con successo!**

---

## Come Configurare l'Overlay

Ora che l'overlay è collegato a Spotify, possiamo personalizzarlo come vogliamo!

### L'Interfaccia del Configuratore

Il configuratore è diviso in **4 schede** (tab) nella parte sinistra:

1. **Basic** - Impostazioni base (dimensioni, layout, temi)
2. **Visual** - Effetti visivi (particelle, animazioni)
3. **Content** - Cosa mostrare (titolo, artista, barra progresso)
4. **Advanced** - Colori personalizzati e dettagli

Sulla destra vedrai la **Live Preview** (Anteprima dal vivo) che ti mostra in tempo reale come apparirà l'overlay.

---

## Guida Completa alle Funzionalità

### 📑 Tab 1: BASIC (Impostazioni di Base)

#### 🎯 Preset (Preset Rapidi)

I preset sono **configurazioni già pronte** che cambiano istantaneamente l'aspetto dell'overlay. Perfetti per iniziare!

Clicca su uno di questi pulsanti per provare:

- **Record** - Classico disco in vinile nero che gira
- **Card** - Copertina moderna stile carta
- **Bar** - Barra minimalista in basso
- **Stacked** - Tutto centrato e impilato
- **Lo-Fi** - Atmosfera rilassata e vintage
- **Cozy** - Caldo e accogliente
- **Ultra Minimal** - Solo il necessario

> 💡 **Consiglio**: Prova tutti i preset per vedere quale ti piace di più! Poi potrai personalizzarlo ulteriormente.

---

#### 🎨 Layout & Style (Disposizione e Stile)

**Layout** - Come è disposto l'overlay

Ogni layout cambia completamente l'aspetto:

- **Record (Vinyl)** - Disco in vinile classico che gira
  - *Perfetto per: Lo-fi, chill stream, atmosfera rilassata*
  
- **Card (Cover)** - Copertina album moderna come card
  - *Perfetto per: Streaming gaming, setup moderni*
  
- **Bar (Minimal)** - Barra orizzontale sottile
  - *Perfetto per: Occupare poco spazio, stream competitive*
  
- **Stacked (Center)** - Tutto centrato verticalmente
  - *Perfetto per: Schermi grandi, scene introduttive*
  
- **Compact (Mini)** - Versione compatta e piccola
  - *Perfetto per: Overlay discreto, gaming intenso*
  
- **Wide (Cinematic)** - Layout largo panoramico
  - *Perfetto per: Schermi ultrawide, video YouTube*
  
- **Split (Dual)** - Diviso in sezioni separate
  - *Perfetto per: Design creativi, layout multi-parte*
  
- **Floating (Overlay)** - Fluttuante in alto a destra
  - *Perfetto per: Sempre visibile ma discreto*
  
- **Corner (Tiny)** - Angolo piccolo e compatto
  - *Perfetto per: Il minimo indispensabile*
  
- **Ticker (Scroll)** - Scorrevole come ticker news
  - *Perfetto per: Fondo schermo, stile broadcast*

**Media Position** - Dove appare l'immagine/disco

- **Left** - Immagine a sinistra, testo a destra
- **Right** - Immagine a destra, testo a sinistra
- **Center** - Tutto al centro
- **Top** - Immagine sopra, testo sotto
- **Bottom** - Testo sopra, immagine sotto

**Theme** - Colori e atmosfera

Ogni tema ha una palette di colori unica:

- **Spotify** - Verde Spotify classico (#1DB954)
- **OBS Dark** - Scuro come OBS, colori freddi
- **Minimal** - Bianco e nero, super pulito
- **Neon** - Colori elettrici e brillanti
- **Gaming** - Rosso e verde gaming RGB
- **Lo-Fi** - Toni caldi, vintage, rilassante
- **Retro Wave** - Viola e rosa anni '80
- **Elegant** - Bianco e blu elegante
- **Cyberpunk** - Ciano e magenta futuristico
- **Sunset** - Arancione e rosa tramonto
- **Ocean** - Blu oceano rilassante
- **Forest** - Verde bosco naturale
- **Midnight** - Blu notte profondo
- **Aurora** - Verde aurora boreale
- **Gradient** - Sfumature arcobaleno
- **Monochrome** - Solo bianco e nero
- **Party** - Colori vivaci e festosi
- **Cozy** - Marrone e beige accogliente
- **Focus** - Colori tenui per non distrarre

**Accent Style** - Stile del colore principale

- **Solid** - Colore pieno normale
- **Glow** - Effetto bagliore luminoso
- **Gradient** - Sfumatura di colori
- **Pulse** - Pulsa al ritmo (effetto respiro)
- **Rainbow** - Cambia colori arcobaleno

---

#### 📐 Sizing & Positioning (Dimensioni e Posizionamento)

Qui personalizzi le dimensioni di ogni elemento. Ogni slider ha un indicatore che ti mostra il valore in tempo reale.

**Media Size** (Dimensione Disco/Copertina)
- Range: 120px - 360px
- Default: 200px
- *Più grande = più visibile, più piccolo = più discreto*

**Progress Height** (Altezza Barra Progresso)
- Range: 0px - 16px
- Default: 6px
- *0 = nascondi barra, 16 = barra molto spessa*

**Title Size** (Dimensione Titolo Canzone)
- Range: 14px - 64px
- Default: 24px
- *Più grande = più leggibile da lontano*

**Artist Size** (Dimensione Nome Artista)
- Range: 10px - 32px
- Default: 15px
- *Solitamente un po' più piccolo del titolo*

**Progress Width** (Larghezza Barra Progresso)
- Range: 50% - 100%
- Default: 100%
- *Puoi accorciare la barra per design minimal*

**Corner Radius** (Arrotondamento Angoli)
- Range: 0px - 24px
- Default: 16px
- *0 = angoli squadrati, 24 = molto arrotondato*

**Blur** (Sfocatura Sfondo)
- Range: 0px - 16px
- Default: 8px
- *Crea effetto vetro sfocato (glassmorphism)*

**Safe Padding** (Margine di Sicurezza)
- Range: 0px - 32px
- Default: 16px
- *Spazio tra contenuto e bordo*

**Title Outline** (Contorno Titolo)
- Range: 0px - 2px
- Default: 0px
- *Aggiunge contorno nero al testo per leggibilità*

**Text Alignment** (Allineamento Testo)
- **Auto** - Si adatta automaticamente al layout
- **Left** - Testo allineato a sinistra
- **Center** - Testo centrato
- **Right** - Testo allineato a destra

---

#### ⚙️ Behavior (Comportamento)

Questi interruttori attivano/disattivano funzionalità:

**Compact spacing** (Spaziatura Compatta)
- ☐ OFF = Spaziatura normale
- ☑ ON = Tutto più vicino e compatto
- *Attiva per risparmiare spazio*

**Spin while playing** (Gira Durante Riproduzione)
- ☐ OFF = Disco/copertina fermo
- ☑ ON = Disco gira come un vero vinile
- *Solo per layout Record, crea effetto realistico*

**Keep label upright** (Etichetta Sempre Dritta)
- ☐ OFF = Etichetta centrale gira col disco
- ☑ ON = Etichetta rimane sempre dritta
- *Solo per layout Record, più facile da leggere*

**Show tonearm** (Mostra Braccio del Giradischi)
- ☐ OFF = Nessun braccio
- ☑ ON = Mostra braccio del giradischi
- *Solo per layout Record, effetto realistico*

---

### 🎨 Tab 2: VISUAL (Effetti Visivi)

#### ✨ Visual Effects (Effetti Visuali)

Questi effetti aggiungono dinamismo all'overlay:

**Particle Effects** (Effetti Particelle)
- ☐ OFF = Nessuna particella
- ☑ ON = Particelle che fluttuano sullo sfondo
- *Crea atmosfera magica, leggero impatto performance*

**Color Breathing** (Respiro Colori)
- ☐ OFF = Colori statici
- ☑ ON = I colori pulsano lentamente
- *Effetto rilassante e ipnotico*

**Waveform Visualizer** (Visualizzatore Forma d'Onda)
- ☐ OFF = Nessuna forma d'onda
- ☑ ON = Mostra onde audio animate
- *Effetto molto dinamico, perfetto per musica elettronica*

**Album Blur Background** (Sfondo Sfocato Album)
- ☐ OFF = Sfondo normale
- ☑ ON = La copertina diventa sfondo sfocato
- *Crea effetto immersivo con i colori dell'album*

---

#### 🎬 Animations (Animazioni)

**Track Change Effect** (Effetto Cambio Canzone)

Quando cambia canzone, puoi scegliere un'animazione:

- **None** - Nessuna animazione, cambio istantaneo
- **Slide** - Scorre via e arriva la nuova
- **Fade** - Dissolvenza graduale
- **Bounce** - Rimbalza via e arriva la nuova
- **Zoom** - Si ingrandisce e rimpicciolisce
- **Flip** - Gira come una carta

**Animation Speed** (Velocità Animazione)
- Range: 0.5x - 2x
- Default: 1x
- *0.5x = lento e fluido, 2x = rapido e scattante*

---

### 📺 Tab 3: CONTENT (Contenuto)

#### 🎭 Elements (Elementi)

Decidi cosa mostrare e cosa nascondere:

**Status pill** (Pillola Stato)
- ☑ ON = Mostra "Playing" o "Paused"
- ☐ OFF = Nascondi stato
- *Utile per far capire se sei in pausa*

**Progress bar** (Barra Progresso)
- ☑ ON = Mostra barra di avanzamento
- ☐ OFF = Nascondi barra
- *Mostra quanto manca alla fine*

**Time stamps** (Indicatori Tempo)
- ☑ ON = Mostra "0:43 / 3:32"
- ☐ OFF = Nascondi tempo
- *Quanto è andata e quanto manca*

**Song title** (Titolo Canzone)
- ☑ ON = Mostra titolo
- ☐ OFF = Nascondi titolo
- *Quasi sempre vuoi questo ON*

**Artist name** (Nome Artista)
- ☑ ON = Mostra artista
- ☐ OFF = Nascondi artista
- *Quasi sempre vuoi questo ON*

**Next track** (Prossima Traccia)
- ☐ OFF = Non mostrare prossima canzone
- ☑ ON = Mostra "Next: [canzone]"
- *Utile per anticipare cosa sta per venire*

---

#### 📜 Text Behavior (Comportamento Testo)

**Auto-scroll** (Scorrimento Automatico)
- ☑ ON = Testo scorre se troppo lungo
- ☐ OFF = Testo viene tagliato
- *Attiva per vedere testi lunghi*

**Auto accent color** (Colore Automatico)
- ☐ OFF = Usa colore tema fisso
- ☑ ON = Colore si adatta alla copertina
- *Estrae colore dominante dall'album!*

**Marquee speed** (Velocità Scorrimento)
- Range: 10s - 30s
- Default: 18s
- *Quanto veloce scorre il testo troppo lungo*

---

### 🔧 Tab 4: ADVANCED (Avanzate)

#### 🎨 Colors (Colori)

**Color Mode** (Modalità Colore)
- **Auto (from theme)** - Usa colori del tema
- **Custom** - Personalizza ogni colore

Se scegli **Custom**, puoi cambiare:

**Accent Color** (Colore Principale)
- Il colore usato per evidenziare (barra progresso, pillola Playing)
- Clicca sul quadrato per aprire il selettore colore

**Text Color** (Colore Testo)
- Colore del titolo della canzone

**Muted Color** (Colore Secondario)
- Colore del nome artista e tempo

---

#### 🖌️ Typography (Tipografia)

**Font Family** (Famiglia Font)

- **System** - Font di sistema (veloce)
- **Inter** - Moderno e pulito
- **Rubik** - Arrotondato e friendly
- **Montserrat** - Professionale ed elegante
- **Poppins** - Geometrico e moderno
- **Fira Sans** - Tecnico e leggibile

---

#### 🌈 Effects (Effetti)

**Drop shadow** (Ombra)
- ☑ ON = Ombra sotto l'overlay
- ☐ OFF = Nessuna ombra
- *Aiuta a staccare l'overlay dallo sfondo*

---

#### 🎭 Background (Sfondo)

**Panel mode** (Modalità Pannello)

**Transparent** (Trasparente)
- ☐ OFF = Sfondo colorato
- ☑ ON = Completamente trasparente
- *Perfetto per overlay su gameplay*

Se NON trasparente:

**Panel color** (Colore Pannello)
- Scegli il colore dello sfondo
- Default: grigio scuro

**Panel opacity** (Opacità Pannello)
- Range: 0% - 100%
- Default: 72%
- *0% = invisibile, 100% = completamente opaco*

---

## Aggiungere l'Overlay in OBS

Ora che hai configurato l'overlay, è il momento di aggiungerlo in OBS!

### Passo 1: Copia l'URL Generato

1. Nel configuratore, guarda nella sezione **"Generated URL"** (in alto nella tab Basic)
2. Vedrai un lungo indirizzo che inizia con `https://...`
3. Clicca sul pulsante **"Copy URL"**
4. L'URL è stato copiato negli appunti!

> 💡 **Suggerimento**: L'URL contiene TUTTE le tue personalizzazioni. Salvalo in un file di testo per non perderlo!

### Passo 2: Apri OBS Studio

1. Avvia OBS Studio sul tuo computer
2. Scegli la **Scena** dove vuoi aggiungere l'overlay
   - Le scene sono nella casella "Scenes" in basso a sinistra
   - Se ne hai solo una, sarà già selezionata

### Passo 3: Aggiungi una Nuova Sorgente

1. Nella sezione **"Sources"** (Sorgenti) in basso
2. Clicca sul pulsante **"+"** (più)
3. Si apre un menu, scorri e trova **"Browser"** (Sorgente Browser)
4. Clicca su **"Browser"**

### Passo 4: Configura la Sorgente Browser

Ti si apre una finestra con diverse opzioni:

1. **Nome**:
   - Scrivi: `Spotify Now Playing`
   - (o quello che vuoi, è solo per riconoscerla)
   - Clicca **"OK"**

2. **URL**:
   - Clicca nel campo URL
   - Premi `Ctrl+V` (Windows/Linux) o `Cmd+V` (Mac)
   - Vedrai apparire il lungo indirizzo copiato prima
   - ⚠️ **IMPORTANTE**: Non modificare questo URL!

3. **Width** (Larghezza):
   - Seleziona quella più adatta alla tua grafica

4. **Height** (Altezza):
   - Seleziona quella più adatta alla tua grafica

5. **FPS** (Frame per secondo):
   - Lascia: `30`
   - (se hai un PC potente puoi mettere `60`)

6. **Altre opzioni**:
   - ☑ **"Shutdown source when not visible"** - Spunta questa
   - ☑ **"Refresh browser when scene becomes active"** - Spunta questa
   - Lascia tutto il resto com'è

7. Clicca **"OK"** in basso

### Passo 5: Posiziona l'Overlay

Ora vedrai l'overlay nella tua scena!

1. **Ridimensiona** (se necessario):
   - Clicca sull'overlay
   - Trascina gli angoli per ingrandire/rimpicciolire
   - Tieni premuto `Shift` mentre trascini per mantenere le proporzioni
   - Tieni premuto `Alt` per ritagliare l'overlay
   - Ricorda: puoi sempre cambiare la Larghezza e l'Altezza dalle impostazioni della Sorgente Browser
   
2. **Sposta**:
   - Clicca e trascina l'overlay dove vuoi
   - Posizioni comuni:
     - **Angolo in basso a sinistra** - Classico
     - **Angolo in basso a destra** - Alternativo
     - **Centro in alto** - Per intro/outro
     - **Angolo in alto** - Per layout ticker

3. **Ordine dei Layer**:
   - L'overlay dovrebbe essere SOPRA al gameplay/webcam
   - Nella lista Sources, trascinalo in alto per portarlo in primo piano
   - Più in alto nella lista = più in primo piano

### Passo 6: Test Finale

1. **Avvia Spotify** sul tuo PC
2. **Fai partire una canzone**
3. Guarda in OBS se l'overlay si aggiorna
4. ✅ Dovrebbe mostrare copertina, titolo e artista!

🎉 **CE L'HAI FATTA!** L'overlay è pronto per lo streaming!

---

## Risoluzione Problemi

### ❌ L'overlay non si vede in OBS

**Possibili cause e soluzioni**:

1. **L'URL non è stato copiato correttamente**
   - Soluzione: Torna al configuratore, clicca di nuovo "Copy URL"
   - In OBS, clicca destro sulla sorgente Browser → Proprietà → Incolla di nuovo l'URL

2. **La sorgente è sotto altri layer**
   - Soluzione: Nella lista Sources in OBS, trascina l'overlay in cima alla lista

3. **L'overlay è fuori schermo**
   - Soluzione: Clicca destro sulla sorgente → Transform → Fit to screen

4. **OBS non ha caricato la pagina**
   - Soluzione: Clicca destro sulla sorgente → Refresh

---

### ❌ L'overlay mostra "Setup Required"

**Causa**: Non hai collegato Spotify nella Sorgente Browser

**Soluzione**:
1. Apri OBS e clicca tasto destro sull'overlay, poi "Interagisci"
2. Segui la [Fase 1: Creare l'App Spotify](#fase-1-creare-lapp-spotify-importante---fai-questo-per-primo)
3. Incolla il Client ID e connetti Spotify

---

### ❌ L'overlay mostra "Not Playing"

**Possibili cause e soluzioni**:

1. **Spotify non è aperto**
   - Soluzione: Apri Spotify sul PC e fai partire una canzone

2. **Stai usando Spotify Web Player**
   - Problema: L'overlay funziona SOLO con l'app desktop Spotify
   - Soluzione: Scarica e installa Spotify da spotify.com

3. **Stai ascoltando su un altro dispositivo non supportato**
   - Problema: Spotify sta riproducendo su un altro dispositivo, non sul PC
   - Soluzione: Nel player Spotify, clicca sull'icona dispositivi e seleziona il PC

4. **L'account Spotify non è connesso**

---

### ❌ L'overlay non si aggiorna quando cambio canzone

**Possibili cause e soluzioni**:

1. **Il token di accesso è scaduto**
   - Può accadere, colpa di Spotify quei cialtroni
   - Soluzione: Reimposta l'overlay

2. **Spotify è in pausa da troppo tempo**
   - Soluzione: Metti play, aspetta 5 secondi, si aggiornerà

3. **Problemi di connessione**
   - Soluzione: Controlla la connessione internet

---

### ❌ L'overlay è troppo piccolo/grande in OBS

**Soluzione**:
1. Clicca sull'overlay in OBS
2. Trascina gli angoli per ridimensionare
3. Tieni premuto `Shift` per mantenere le proporzioni
4. Oppure: Clicca destro → Transform → Edit Transform → Cambia Scale

---

### ❌ La barra di progresso non è perfettamente sincronizzata

**Causa**: Questo è normale! La barra non si aggiorna in tempo reale.

**Soluzione**: Nessuna, è il comportamento normale per risparmiare risorse.

---

### ❌ Il testo è troncato/tagliato

**Possibili soluzioni**:

1. **Attiva Auto-scroll**
   - Tab Content → Text Behavior → Auto-scroll ☑ ON

2. **Aumenta la larghezza dell'overlay**
   - Tab Basic → Sizing & Positioning → Aumenta Media Size

3. **Riduci dimensione testo**
   - Tab Basic → Sizing & Positioning → Riduci Title Size e Artist Size

---

### ❌ L'overlay ha lag/scatti

**Possibili cause e soluzioni**:

1. **FPS troppo alti**
   - Soluzione: In OBS, proprietà sorgente → FPS: imposta a 30 invece di 60

2. **Troppi effetti attivi**
   - Soluzione: Disattiva Particles, Waveform, Color Breathing

3. **PC sovraccarico**
   - Soluzione: Chiudi programmi non necessari

---

### ❌ I colori sono sbagliati

**Soluzione**:
1. Tab Advanced → Colors → Color Mode: **Auto (from theme)**
2. Scegli un tema diverso
3. Oppure usa **Custom** e scegli i colori manualmente

---

### ❌ L'overlay funziona nel configuratore ma non in OBS

**Possibili cause**:

1. **URL sbagliato in OBS**
   - Soluzione: L'URL DEVE iniziare con `https://alebirra.github.io/...`
   - Verifica che non ci siano spazi o caratteri strani

2. **OBS non aggiornato**
   - Soluzione: Aggiorna OBS all'ultima versione
   - Download: https://obsproject.com/

3. **Firewall/Antivirus blocca OBS**
   - Soluzione: Aggiungi OBS alle eccezioni del firewall

---

## Domande Frequenti (FAQ)

### ❓ Serve Spotify Premium?

**No!** L'overlay funziona sia con account Spotify gratuito che Premium. L'unica differenza è che con l'account gratuito ci saranno le pubblicità, che verranno mostrate nell'overlay come "Advertisement" quando partono.

---

### ❓ Posso usare l'overlay su più PC contemporaneamente?

**Sì!** Puoi usare lo stesso Client ID su tutti i PC che vuoi. Basta copiare lo stesso URL su ogni PC.

---

### ❓ L'overlay funziona con altre piattaforme di streaming oltre Twitch?

**Sì!** L'overlay funziona su:
- Twitch
- YouTube
- Facebook Gaming
- TikTok Live
- Qualsiasi piattaforma che supporti OBS o StreamLabs OBS

---

### ❓ Posso cambiare l'overlay durante la diretta?

**Sì!** Hai due opzioni:

1. **Riconfigurare** - Vai sul configuratore, cambia le impostazioni, copia il nuovo URL, incollalo in OBS nelle proprietà della sorgente

2. **Più sorgenti** - Crea più sorgenti Browser in OBS con URL diversi, poi mostra/nascondi quella che ti serve

---

### ❓ L'overlay mostra anche le pubblicità?

**Sì**, se hai un account Spotify gratuito, quando parte una pubblicità l'overlay mostrerà "Advertisement" come titolo. È il comportamento normale.

---

### ❓ Posso modificare il codice dell'overlay?

**Sì!** Il progetto è open source su GitHub. Puoi:
- Scaricare il codice
- Modificarlo come vuoi
- Hostarlo sul tuo server
- Contribuire con modifiche al progetto originale

Repository: https://github.com/alebirra/spotify-obs

---

### ❓ Posso usare l'overlay offline?

**No**, l'overlay ha bisogno di connessione internet per:
- Comunicare con l'API Spotify
- Scaricare le copertine degli album
- Aggiornare lo stato della riproduzione

---

### ❓ Quanto impatta l'overlay sulle performance?

**Molto poco!** L'overlay è ottimizzato e usa circa:
- 30-50 MB di RAM
- 0-1% di CPU
- Trascurabile impatto su GPU

Se noti lag:
- Riduci FPS a 30
- Disattiva effetti visivi (particelle, waveform)
- Usa layout più semplici (Bar, Minimal)

---

### ❓ Posso mostrare Spotify e altre app musicali?

**No**, l'overlay funziona SOLO con Spotify perché usa specificamente le API di Spotify. Non è compatibile con:
- Apple Music
- YouTube Music
- Amazon Music
- Deezer
- Tidal

---

### ❓ Il Client ID scade?

**No**, il Client ID non scade mai. Una volta creato, puoi usarlo per sempre.

Quello che scade è il **token di accesso** (dopo alcune ore), ma si rinnova automaticamente quando ricarichi la pagina.

---

### ❓ Altri possono vedere cosa ascolto?

**Solo chi guarda la tua diretta!** L'overlay mostra la musica solo sul tuo stream. Non è visibile su Spotify o altrove.

---

### ❓ Posso nascondere canzoni specifiche?

**No**, l'overlay mostra tutto quello che suona su Spotify. Se non vuoi mostrare una canzone, devi:
- Mettere in pausa Spotify
- Oppure nascondere temporaneamente la sorgente in OBS (clicca sull'occhio 👁️)

---

### ❓ L'overlay funziona con playlist/podcast?

**Sì!** L'overlay mostra:
- ✅ Canzoni singole
- ✅ Album
- ✅ Playlist
- ✅ Podcast (mostra episodio e podcast name)
- ✅ Radio
- ❌ Podcast video (solo audio supportato)

---

### ❓ Posso vedere le statistiche di ascolto?

**No**, l'overlay si limita a mostrare cosa stai ascoltando. Non raccoglie o mostra statistiche. Per statistiche usa Spotify Wrapped o siti come Last.fm.

---

### ❓ Funziona su Mac/Linux?

**Sì!** L'overlay funziona su:
- ✅ Windows
- ✅ macOS
- ✅ Linux
- ✅ Qualsiasi sistema che può eseguire OBS Studio

---

### ❓ Posso tradurre l'overlay in altre lingue?

Al momento l'overlay mostra:
- "Playing" / "Paused" in inglese
- I nomi di canzoni/artisti come sono su Spotify

Se vuoi contribuire con una traduzione, contattami su Telegram!

---

## Contatti e Supporto

### 💬 Hai bisogno di aiuto?

**Telegram**: [@alebirra](https://t.me/alebirra)

Non esitare a contattarmi se:
- Qualcosa non funziona
- Hai domande o dubbi
- Vuoi proporre nuove funzionalità
- Hai trovato un bug
- Vuoi contribuire al progetto

### 🐛 Segnala un Bug

Se trovi un problema:
1. Descrivimi cosa non funziona
2. Dimmi che sistema operativo usi
3. Mandami uno screenshot se possibile
4. Dimmi quali passaggi hai seguito

### 💡 Richiedi una Funzionalità

Hai un'idea per migliorare l'overlay? Fammelo sapere! Sono sempre aperto a nuovi suggerimenti.

### 🤝 Contribuisci al Progetto

Il progetto è open source su GitHub:
**https://github.com/alebirra/spotify-obs**

Puoi:
- Segnalare bug
- Proporre miglioramenti
- Fare pull request con modifiche
- Tradurre in altre lingue
- Condividere preset interessanti

---

## 🎉 Conclusione

Congratulazioni per aver configurato SpotyStream! Ora hai un overlay professionale per mostrare la musica che ascolti durante le tue dirette.

**Ricorda**:
- ⭐ Sperimenta con i preset per trovare lo stile perfetto
- 🎨 Personalizza colori e dimensioni come preferisci  
- 📺 Testa tutto prima di andare live
- 💾 Salva l'URL generato per non perderlo
- 🔄 Aggiorna il token se l'overlay smette di funzionarsi ricaricando la pagina in OBS

### Ti è piaciuto SpotyStream?

- ⭐ Lascia una stella su [GitHub](https://github.com/alebirra/spotify-obs)
- 💬 Scrivimi su Telegram: [@alebirra](https://t.me/alebirra)
- 📺 Mostrami come usi l'overlay nelle tue stream!

---

**Buon Streaming! 🎵✨**

*Creato con ❤️ da [@alebirra](https://t.me/alebirra)*

---

## 📄 Licenza

Questo progetto è rilasciato sotto licenza MIT - sei libero di usarlo, modificarlo e condividerlo.

## 🙏 Ringraziamenti

- Spotify per le API
- La community di OBS Studio
- Tutti gli streamer che usano SpotyStream

---

*Ultima versione: Dicembre 2025*
*README versione: 2.0*
