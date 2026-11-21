# Media Voti

App (PWA) per inserire i voti di ogni materia, vedere la media aggiornata, il grafico dell'andamento nel tempo e quale voto serve alla prossima verifica per arrivare alla media desiderata.

## File

- `index.html` – l'app
- `manifest.webmanifest` – nome, colori e icone dell'app installabile
- `sw.js` – service worker: rende l'app disponibile offline
- `icons/` – icone (SVG sorgente + PNG 192/512, maskable, Apple)

## Installarla sul telefono

Per essere installabile la PWA deve essere servita via **HTTPS** (aprire il file direttamente non basta).
Il modo più semplice è GitHub Pages: *Settings → Pages → Deploy from a branch* e scegli il branch.

- **Android (Chrome):** apri il link → pulsante **⬇ Installa** nell'app, oppure menu ⋮ → *Installa app*.
- **iPhone (Safari):** apri il link → *Condividi* → *Aggiungi alla schermata Home*.

## Dove finiscono i dati

I voti sono salvati sul dispositivo (localStorage) e restano anche chiudendo l'app o spegnendo il telefono.
Usa **Esporta** ogni tanto per avere un backup (e **Importa** per ripristinarlo o spostarlo su un altro dispositivo).

## Aggiornare l'app

Dopo aver modificato i file, aumenta la versione in `sw.js` (`media-voti-v1` → `media-voti-v2`) così i telefoni scaricano la nuova versione.
