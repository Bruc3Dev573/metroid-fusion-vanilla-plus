# Metroid Fusion Vanilla+

[English](README.md) | Italiano

Una raccolta di modifiche grafiche e piccoli miglioramenti per la versione europea di Metroid Fusion. Cambia i colori e riduce le attese, senza modificare movimento, combattimento o progressione.

Adattamento europeo e verifiche di [Bruc3Dev573](https://github.com/Bruc3Dev573). L'italiano è già presente nel gioco originale e non è stato modificato.

## Download

La patch v1.0.0 e il relativo checksum sono nella pagina [Releases](https://github.com/Bruc3Dev573/metroid-fusion-vanilla-plus/releases).

## Cosa cambia

- Palette riviste per ambienti e personaggi, comprese le tute di Samus.
- Testi delle conversazioni di navigazione più rapidi.
- Transizioni delle porte più rapide, con la correzione per le distanze verticali dispari.
- Ascensori più rapidi.
- Possibilità di saltare l'introduzione di una nuova partita premendo Start. Senza premere Start, l'introduzione si svolge normalmente.

Non sono inclusi Better Suits Colours, salto dei dialoghi di Adam, salto ripetuto sulla stessa parete, salti bomba infiniti o sblocco delle porte. Non è la patch Redux completa. I colori sono quelli scelti dall'autore della ricolorazione, non un ripristino ufficiale.

## Screenshot

Immagini della ROM modificata, acquisite in BizHawk a 240 x 160 pixel.

| Introduzione in italiano | Dialoghi di navigazione |
|:---:|:---:|
| ![Introduzione in italiano](docs/screenshots/intro-italian.png) | ![Dialogo di navigazione in italiano](docs/screenshots/navigation-italian.png) |
| **Samus e la stazione** | **Terminale Habitation** |
| ![Samus e i colori della stazione](docs/screenshots/gameplay.png) | ![Samus accanto al terminale Habitation](docs/screenshots/habitation.png) |

## ROM richiesta

Serve una copia pulita di `Metroid Fusion (Europe) (En,Fr,De,Es,It)`. Le versioni USA e giapponese non sono compatibili.

| Proprietà | Valore |
|---|---|
| Codice gioco | `AMTP` |
| Revisione | `0` |
| Dimensione | `8388608` byte |
| CRC32 | `974e46ab` |
| SHA-1 | `cc46d54b70c1ee38c856ee6e58ec712136763389` |
| SHA-256 | `a024ef6fa8ff19444bc6c31a714eb6cab44464b39227fcd434e409fca1cd8198` |

## Installazione

1. Conserva una copia della ROM originale e verificane l'hash. Il formato IPS non controlla la ROM di partenza.
2. Applica [`metroid-fusion-vanilla-plus-eu-v1.0.0.ips`](patches/metroid-fusion-vanilla-plus-eu-v1.0.0.ips) con [Lunar IPS](https://fusoya.eludevisibility.org/lips/) o un altro programma compatibile. Salva il risultato in un nuovo file.
3. Confronta lo SHA-256 della ROM ottenuta con quello riportato sotto.
4. Avvia il gioco e scegli Italiano nel menu della lingua.

Applica questa sola IPS alla ROM pulita, senza altre patch già installate. La ROM risultante resta di 8 MiB.

| File | SHA-256 |
|---|---|
| Patch IPS | `03f15ebaf6939ad58c4c977113866d29b0a751a400685f1c0064d8365dc0f728` |
| ROM modificata | `fd211f006f81ef2ce3ea09de94831a4a1b33b2e87702618fa6c18b1eedf11312` |

Gli stessi dati, insieme allo SHA-1 della ROM risultante, sono in [`release.json`](release.json).

## Verifiche

La ricostruzione della patch e la sua applicazione alla ROM pulita producono lo stesso risultato. Sono stati controllati il testo rapido, le transizioni delle porte e gli ascensori, comprese le distanze dispari che causavano problemi nella modifica originale delle porte.

In BizHawk sono stati provati l'introduzione completa, il salto con Start in due momenti diversi, due passaggi attraverso le porte e un percorso in ascensore. Nei casi confrontati, il salvataggio dopo l'introduzione era identico a quello del gioco originale. Il terminale Habitation è stato osservato in uno scenario predisposto per la verifica, senza riprodurre scomparse durante il ciclo inattivo.

Non è stata completata una partita intera e non sono state eseguite prove su GBA fisico o MiSTer. I test non coprono ogni stanza o evento del gioco.

## Crediti

- **Piggy Chan!**: [Color Palette Improvement](https://www.romhacking.net/hacks/8122/), la ricolorazione di ambienti, personaggi e tute.
- **ShadowOne333**: [porting europeo di Color Palette Improvement](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/ColorImprovement/color_improvement_eur.asm), usato come base per i colori.
- **SpineShark**: [Fast Text](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/misc.asm#L114-L126).
- **Jumzhu**: [Faster Door Transitions](https://metroidconstruction.com/resource.php?id=414).
- **somerando/caauyjdp**: [correzione delle distanze dispari per Faster Door Transitions](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/faster_door_transitions.asm).
- **interdpth**: [Faster Elevators](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/faster_elevators.asm), conservata nei sorgenti Redux con il porting di ShadowOne333.
- **ShadowOne333 e yohann**: modifica e ricerca originali sul [salto dell'introduzione con Start](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/misc.asm#L4-L6), prese come riferimento. Il codice per la versione europea è un'implementazione dedicata.
- **[Bruc3Dev573](https://github.com/Bruc3Dev573)**: integrazione europea, codice EU per saltare l'introduzione, strumenti di build, verifiche e preparazione della patch.
- **Nintendo**: gioco, grafica e testi originali.

I link portano alle schede delle patch o al loro codice specifico. Per Fast Text e Faster Elevators il riferimento disponibile è il sorgente della singola modifica, non una scheda Romhacking.net separata. I sorgenti Redux usati sono quelli del commit `e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a`.

## Licenze e attribuzione

La documentazione originale e le note di integrazione sono di Bruc3Dev573, © 2026, e sono disponibili con licenza [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Se le riutilizzi, cita l'autore, collega [questo progetto](https://github.com/Bruc3Dev573/metroid-fusion-vanilla-plus) e la licenza, e indica le modifiche apportate.

Le hack mantengono i propri crediti e le condizioni originali. Sono inclusi il [README originale di Redux](docs/Metroid-Fusion-Redux-README.txt), la [GPLv3](docs/Metroid-Fusion-Redux-LICENSE.txt) e [`NOTICE`](NOTICE). La licenza della documentazione non copre il gioco o la grafica degli screenshot.

Progetto amatoriale non ufficiale e senza garanzia. È necessaria una copia legittima del gioco. Non sono incluse ROM, salvataggi o emulatori.
