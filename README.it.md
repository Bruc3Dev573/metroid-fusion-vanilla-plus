# Metroid Fusion - Vanilla+ europeo

[English](README.md) | **Italiano**

Patch non ufficiale per la versione europea di *Metroid Fusion* su Game Boy Advance, con colori rivisti e alcune modifiche per ridurre i tempi di attesa.

Il gioco europeo contiene già l'italiano. Questa patch conserva i testi originali e non cambia movimento, combattimento o progressione.

## Download

Patch v1.0.0 e checksum sono nella pagina [Releases](https://github.com/Bruc3Dev573/metroid-fusion-vanilla-plus/releases). L'archivio `source.zip`, disponibile nella stessa pagina, contiene i file necessari per ricostruirla.

## Contenuto della patch

- **[Color Palette Improvement](https://www.romhacking.net/hacks/8122/)** di Piggy Chan!, con il [porting europeo](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/ColorImprovement/color_improvement_eur.asm) di ShadowOne333. Modifica le palette di ambienti e personaggi, comprese le tute di Samus.
- **[Fast Text](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/misc.asm#L114-L126)** di SpineShark. Velocizza il testo delle conversazioni di navigazione.
- **[Faster Door Transitions](https://metroidconstruction.com/resource.php?id=414)** di Jumzhu, con la [correzione delle distanze dispari](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/faster_door_transitions.asm) di somerando/caauyjdp.
- **[Faster Elevators](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/faster_elevators.asm)** di interdpth. Velocizza gli ascensori.
- **Salto dell'introduzione con Start**, implementato per la ROM europea da Bruc3Dev573 prendendo come riferimento la [modifica di Redux](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/misc.asm#L4-L6). Senza premere Start, l'introduzione si svolge normalmente.

La patch è unica e va applicata direttamente alla ROM pulita. Non include Better Suits Colours, salto dei dialoghi di Adam, salto ripetuto sulla stessa parete, salti bomba infiniti o sblocco delle porte. Non è Redux completo. La ricolorazione segue le scelte dell'autore, non è un ripristino ufficiale dei colori.

## ROM richiesta

| Proprietà | Valore atteso |
|---|---|
| Titolo | `Metroid Fusion (Europe) (En,Fr,De,Es,It)` |
| Codice gioco | `AMTP` |
| Revisione | `0` |
| Dimensione | `8388608` byte |
| CRC32 | `974e46ab` |
| SHA-1 | `cc46d54b70c1ee38c856ee6e58ec712136763389` |
| SHA-256 | `a024ef6fa8ff19444bc6c31a714eb6cab44464b39227fcd434e409fca1cd8198` |

Non applicare la patch alle versioni USA o giapponese, né a una ROM già modificata.

## Installazione

1. Verifica che la ROM corrisponda agli hash indicati sopra e conserva una copia dell'originale.
2. Applica [`metroid-fusion-vanilla-plus-eu-v1.0.0.ips`](patches/metroid-fusion-vanilla-plus-eu-v1.0.0.ips) con [Lunar IPS](https://fusoya.eludevisibility.org/lips/) o un altro programma compatibile. Salva il risultato in un nuovo file.
3. Confronta lo SHA-256 della ROM ottenuta con quello riportato sotto.
4. Avvia il gioco e scegli Italiano nel menu della lingua.

Il formato IPS non controlla la ROM di partenza. La ROM risultante resta di 8 MiB.

| File | SHA-256 |
|---|---|
| Patch IPS | `03f15ebaf6939ad58c4c977113866d29b0a751a400685f1c0064d8365dc0f728` |
| ROM modificata | `fd211f006f81ef2ce3ea09de94831a4a1b33b2e87702618fa6c18b1eedf11312` |

Gli hash sono riportati anche in [`release.json`](release.json) e nel file `.sha256` accanto all'IPS.

## Verifica

La ricostruzione della patch e la sua applicazione alla ROM pulita producono lo stesso risultato. Sono stati controllati testo rapido, porte e ascensori, comprese le distanze dispari che causavano problemi nella modifica originale delle porte.

In BizHawk sono stati provati l'introduzione completa, il salto con Start in due momenti diversi, due passaggi attraverso le porte e un percorso in ascensore. Nei casi confrontati, il salvataggio dopo l'introduzione era identico a quello del gioco originale. Il terminale Habitation è stato osservato in uno scenario predisposto per la verifica, senza riprodurre scomparse durante il ciclo inattivo.

I test sono mirati, non coprono una partita intera. Non sono state eseguite prove su GBA fisico o MiSTer.

Per segnalare problemi, usa le [Issues](https://github.com/Bruc3Dev573/metroid-fusion-vanilla-plus/issues) indicando hash della ROM, emulatore o core e punto del gioco. Non allegare ROM o salvataggi personali.

## Screenshot

Immagini della ROM modificata, acquisite in BizHawk a 240 x 160 pixel.

| Introduzione in italiano | Dialoghi di navigazione |
|:---:|:---:|
| ![Introduzione in italiano](docs/screenshots/intro-italian.png) | ![Dialogo di navigazione in italiano](docs/screenshots/navigation-italian.png) |
| **Samus e la stazione** | **Terminale Habitation** |
| ![Samus e i colori della stazione](docs/screenshots/gameplay.png) | ![Samus accanto al terminale Habitation](docs/screenshots/habitation.png) |

## Crediti

- **Bruc3Dev573:** integrazione europea, codice EU per saltare l'introduzione, strumenti di build, verifiche e preparazione della patch.
- **Piggy Chan!:** [Color Palette Improvement](https://www.romhacking.net/hacks/8122/).
- **ShadowOne333:** [porting europeo dei colori](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/ColorImprovement/color_improvement_eur.asm) e riferimento per il [salto dell'introduzione](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/misc.asm#L4-L6).
- **SpineShark:** [Fast Text](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/misc.asm#L114-L126).
- **Jumzhu:** [Faster Door Transitions](https://metroidconstruction.com/resource.php?id=414).
- **somerando/caauyjdp:** [correzione delle transizioni con distanza dispari](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/faster_door_transitions.asm).
- **interdpth:** [Faster Elevators](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/faster_elevators.asm).
- **yohann:** ricerca sul salto dell'introduzione, citata nei [crediti originali di Redux](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/ReadMe.md#credits).
- **Nintendo:** gioco, grafica e testi originali.

Per le modifiche senza una scheda separata verificata, i link portano al codice della singola patch. Le condizioni del materiale originale del progetto sono in [`NOTICE`](NOTICE). La [verifica delle licenze](docs/permissions.md) distingue le condizioni trovate dai permessi ancora da chiarire.

La verifica non consente di dichiarare chiarita ogni autorizzazione per la ridistribuzione pubblica della patch completa.

## Note legali

Progetto amatoriale non ufficiale e non commerciale, senza garanzia. Nintendo e gli autori originali delle patch non sono coinvolti in questa integrazione europea. È necessaria una copia legittima del gioco.

Il repository contiene patch, checksum, screenshot e documentazione. Non contiene ROM o salvataggi. Il codice per ricostruire la patch è fornito separatamente nella release. I crediti e la disponibilità dei sorgenti non sostituiscono eventuali autorizzazioni mancanti. I titolari dei diritti possono richiedere correzioni o rimozioni tramite GitHub Issues.
