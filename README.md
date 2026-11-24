# Arlecchino GM

Soundfont **General MIDI** in formato **SF3**: 128 strumenti (banco 0) e batteria standard (banco 128, kit 0).

Come il costume di Arlecchino è fatto di toppe di stoffe diverse, questo soundfont è composto da preset scelti uno per uno,
all'ascolto, fra sei soundfont liberi.

Arlecchino nasce come soundfont per [Canovaccio](https://github.com/badpenguin/canovaccio/), programma di notazione
musicale ed editor MIDI.


## Caratteristiche

- File: `Arlecchino-GM.sf3`, circa 47 MB.

- Campioni compressi in Ogg Vorbis.
  I campioni già compressi nelle sorgenti SF3 sono copiati così come sono, senza una seconda compressione.
  I campioni più corti di 4096 frame restano non compressi, perché Vorbis altera i cicli singoli brevissimi.

- Volumi allineati, strumento per strumento, a quelli di MuseScore General HQ.
  Le correzioni sono tarate per **FluidSynth**, che applica il generatore `initialAttenuation` con un fattore 0,4.
  Con altri sintetizzatori le correzioni risultano circa 2,5 volte più forti.

- I preset sono copiati senza modifiche ai suoni.
  Cambiano solo il nome (con la sigla della sorgente, es. `Rhodes EP - FR3`) e l'attenuazione per il volume.


## Compatibilità

Il formato SF3 è letto da FluidSynth 2.x, MuseScore e Polyphone; molti player che leggono solo SF2 non lo supportano.

Il file è stato verificato con **FluidSynth 2.3.4**: confronto nota per nota con la versione SF2 non compressa,
differenze sotto 1 dB su tutti i 129 preset.

L'SF3 contiene sia campioni compressi sia alcuni campioni brevi non compressi: FluidSynth lo gestisce,
altri lettori SF3 non sono stati provati.


## Uso

```bash
fluidsynth -a pulseaudio Arlecchino-GM.sf3 brano.mid
```


## Strumenti

`Orig.` è la posizione banco:programma del preset nella sorgente; `Vol. dB` è la correzione di volume applicata.

| Posto | Strumento GM            | Preset               | Sorgente                     | Orig. | Licenza             | Vol. dB |
|-------|-------------------------|----------------------|------------------------------|-------|---------------------|---------|
| 0:0   | Acoustic Grand Piano    | Yamaha Grand Piano   | Fluid R3 GM                  | 0:0   | MIT                 | -2.6    |
| 0:1   | Bright Acoustic Piano   | Bright Yamaha Grand  | Fluid R3 GM                  | 0:1   | MIT                 | -3.5    |
| 0:2   | Electric Grand Piano    | Electric Grand Piano | GeneralUser GS 2.0.3         | 0:2   | GeneralUser GS v2.0 | -1.9    |
| 0:3   | Honky-tonk Piano        | Honky Tonk           | Fluid R3 GM                  | 0:3   | MIT                 | -3.4    |
| 0:4   | Electric Piano 1        | Rhodes EP            | Fluid R3 GM                  | 0:4   | MIT                 | -3.4    |
| 0:5   | Electric Piano 2        | Legend EP 2          | Fluid R3 GM                  | 0:5   | MIT                 | -2.5    |
| 0:6   | Harpsichord             | Harpsichord          | Fluid R3 GM                  | 0:6   | MIT                 | -7.2    |
| 0:7   | Clavinet                | Clavinet             | MuseScore General HQ 0.2     | 0:7   | MIT                 | 0       |
| 0:8   | Celesta                 | Celesta              | Fluid R3 GM                  | 0:8   | MIT                 | -5.3    |
| 0:9   | Glockenspiel            | Glockenspiel         | Fluid R3 GM                  | 0:9   | MIT                 | -4.7    |
| 0:10  | Music Box               | Christmas Bells      | GeneralUser GS 2.0.3         | 12:10 | GeneralUser GS v2.0 | -5.4    |
| 0:11  | Vibraphone              | Vibraphone No Trem.  | GeneralUser GS 2.0.3         | 11:11 | GeneralUser GS v2.0 | -6.2    |
| 0:12  | Marimba                 | Marimba              | Fluid R3 GM                  | 0:12  | MIT                 | -3.8    |
| 0:13  | Xylophone               | Xylophone            | FluidR3Mono (MS General 0.1) | 0:13  | MIT                 | 0       |
| 0:14  | Tubular Bells           | Tubular Bells        | Fluid R3 GM                  | 0:14  | MIT                 | -3.5    |
| 0:15  | Dulcimer                | Dulcimer             | GeneralUser GS 2.0.3         | 0:15  | GeneralUser GS v2.0 | -2.9    |
| 0:16  | Drawbar Organ           | Tonewheel Organ      | GeneralUser GS 2.0.3         | 0:16  | GeneralUser GS v2.0 | -2.5    |
| 0:17  | Percussive Organ        | Percussive Organ     | GeneralUser GS 2.0.3         | 0:17  | GeneralUser GS v2.0 | 0       |
| 0:18  | Rock Organ              | Rock Organ           | GeneralUser GS 2.0.3         | 0:18  | GeneralUser GS v2.0 | -1.1    |
| 0:19  | Church Organ            | Pipe Organ           | GeneralUser GS 2.0.3         | 0:19  | GeneralUser GS v2.0 | 0       |
| 0:20  | Reed Organ              | Reed Organ           | MuseScore General HQ 0.2     | 0:20  | MIT                 | 0       |
| 0:21  | Accordion               | Italian Accordion    | MuseScore General HQ 0.2     | 8:21  | MIT                 | -1.2    |
| 0:22  | Harmonica               | Harmonica            | GeneralUser GS 2.0.3         | 0:22  | GeneralUser GS v2.0 | -1.5    |
| 0:23  | Tango Accordion         | Bandoneon            | GeneralUser GS 2.0.3         | 0:23  | GeneralUser GS v2.0 | -1.2    |
| 0:24  | Acoustic Guitar (nylon) | Nylon-String Guitar  | FreePats GM 2022-10-26       | 0:24  | CC0-1.0             | -4.4    |
| 0:25  | Acoustic Guitar (steel) | Steel-String Guitar  | FreePats GM 2022-10-26       | 0:25  | GPL-3.0++exc        | -11.0   |
| 0:26  | Electric Guitar (jazz)  | Jazz Guitar          | Fluid R3 GM                  | 0:26  | MIT                 | -5.4    |
| 0:27  | Electric Guitar (clean) | E. Guitar Clean      | FreePats GM 2022-10-26       | 0:27  | CC0-1.0             | -2.3    |
| 0:28  | Electric Guitar (muted) | Palm Muted Guitar    | MuseScore General HQ 0.2     | 0:28  | MIT                 | 0       |
| 0:29  | Overdriven Guitar       | Overdrive Guitar     | Fluid R3 GM                  | 0:29  | MIT                 | -7.2    |
| 0:30  | Distortion Guitar       | Feedback Guitar      | Fluid R3 GM                  | 8:30  | MIT                 | -9.1    |
| 0:31  | Guitar Harmonics        | Guitar Harmonics     | FluidR3Mono (MS General 0.1) | 0:31  | MIT                 | -1.0    |
| 0:32  | Acoustic Bass           | Acoustic Bass        | Fluid R3 GM                  | 0:32  | MIT                 | -1.1    |
| 0:33  | Electric Bass (finger)  | Electric Bass 1      | FreePats GM 2022-10-26       | 0:33  | GPL-3.0++exc        | -5.2    |
| 0:34  | Electric Bass (pick)    | Picked Bass          | Fluid R3 GM                  | 0:34  | MIT                 | -1.1    |
| 0:35  | Fretless Bass           | Fretless Bass        | GeneralUser GS 2.0.3         | 0:35  | GeneralUser GS v2.0 | -2.9    |
| 0:36  | Slap Bass 1             | Slap Bass 1          | GeneralUser GS 2.0.3         | 0:36  | GeneralUser GS v2.0 | -1.0    |
| 0:37  | Slap Bass 2             | Pop Bass             | Fluid R3 GM                  | 0:37  | MIT                 | 0       |
| 0:38  | Synth Bass 1            | Synth Bass 1         | GeneralUser GS 2.0.3         | 0:38  | GeneralUser GS v2.0 | -1.9    |
| 0:39  | Synth Bass 2            | Synth Bass 4         | Fluid R3 GM                  | 8:39  | MIT                 | -4.3    |
| 0:40  | Violin                  | Violin               | GeneralUser GS 2.0.3         | 0:40  | GeneralUser GS v2.0 | -3.0    |
| 0:41  | Viola                   | Viola                | Fluid R3 GM                  | 0:41  | MIT                 | -1.1    |
| 0:42  | Cello                   | Cello                | Fluid R3 GM                  | 0:42  | MIT                 | 0       |
| 0:43  | Contrabass              | Contrabass           | MuseScore General HQ 0.2     | 0:43  | MIT                 | 0       |
| 0:44  | Tremolo Strings         | Strings Tremolo      | MuseScore General HQ 0.2     | 0:44  | MIT                 | 0       |
| 0:45  | Pizzicato Strings       | Pizzicato Strings    | GeneralUser GS 2.0.3         | 0:45  | GeneralUser GS v2.0 | -6.1    |
| 0:46  | Orchestral Harp         | Orchestral Harp      | GeneralUser GS 2.0.3         | 0:46  | GeneralUser GS v2.0 | -3.4    |
| 0:47  | Timpani                 | Timpani              | Fluid R3 GM                  | 0:47  | MIT                 | +1.3    |
| 0:48  | String Ensemble 1       | Strings Fast         | MuseScore General HQ 0.2     | 0:48  | MIT                 | 0       |
| 0:49  | String Ensemble 2       | Strings Slow         | MuseScore General HQ 0.2     | 0:49  | MIT                 | 0       |
| 0:50  | Synth Strings 1         | Synth Strings 1      | FluidR3Mono (MS General 0.1) | 0:50  | MIT                 | 0       |
| 0:51  | Synth Strings 2         | Synth Strings 2      | FluidR3Mono (MS General 0.1) | 0:51  | MIT                 | 0       |
| 0:52  | Choir Aahs              | Ahh Choir            | Fluid R3 GM                  | 0:52  | MIT                 | -4.1    |
| 0:53  | Voice Oohs              | Ohh Voices           | Fluid R3 GM                  | 0:53  | MIT                 | -4.1    |
| 0:54  | Synth Voice             | Synth Voice          | GeneralUser GS 2.0.3         | 0:54  | GeneralUser GS v2.0 | +1.4    |
| 0:55  | Orchestra Hit           | Orchestra Hit        | GeneralUser GS 2.0.3         | 0:55  | GeneralUser GS v2.0 | -1.7    |
| 0:56  | Trumpet                 | Trumpet              | GeneralUser GS 2.0.3         | 0:56  | GeneralUser GS v2.0 | 0       |
| 0:57  | Trombone                | Trombone             | Fluid R3 GM                  | 0:57  | MIT                 | 0       |
| 0:58  | Tuba                    | Tuba                 | Fluid R3 GM                  | 0:58  | MIT                 | 0       |
| 0:59  | Muted Trumpet           | Muted Trumpet        | Fluid R3 GM                  | 0:59  | MIT                 | -3.6    |
| 0:60  | French Horn             | Solo French Horn     | GeneralUser GS 2.0.3         | 1:60  | GeneralUser GS v2.0 | -4.2    |
| 0:61  | Brass Section           | Brass Section        | Fluid R3 GM                  | 0:61  | MIT                 | -2.6    |
| 0:62  | Synth Brass 1           | Synth Brass 1        | GeneralUser GS 2.0.3         | 0:62  | GeneralUser GS v2.0 | 0       |
| 0:63  | Synth Brass 2           | Synth Brass 2        | GeneralUser GS 2.0.3         | 0:63  | GeneralUser GS v2.0 | -2.1    |
| 0:64  | Soprano Sax             | Soprano Sax          | Fluid R3 GM                  | 0:64  | MIT                 | -4.2    |
| 0:65  | Alto Sax                | Alto Sax             | Fluid R3 GM                  | 0:65  | MIT                 | -4.0    |
| 0:66  | Tenor Sax               | Tenor Sax            | Fluid R3 GM                  | 0:66  | MIT                 | -3.7    |
| 0:67  | Baritone Sax            | Baritone Sax         | Fluid R3 GM                  | 0:67  | MIT                 | -4.5    |
| 0:68  | Oboe                    | Oboe                 | Fluid R3 GM                  | 0:68  | MIT                 | -2.6    |
| 0:69  | English Horn            | English Horn         | Fluid R3 GM                  | 0:69  | MIT                 | -5.9    |
| 0:70  | Bassoon                 | Bassoon              | Fluid R3 GM                  | 0:70  | MIT                 | -2.2    |
| 0:71  | Clarinet                | Clarinet             | Fluid R3 GM                  | 0:71  | MIT                 | -6.2    |
| 0:72  | Piccolo                 | Piccolo              | Fluid R3 GM                  | 0:72  | MIT                 | -3.3    |
| 0:73  | Flute                   | Flute                | Fluid R3 GM                  | 0:73  | MIT                 | -3.0    |
| 0:74  | Recorder                | Recorder             | MuseScore General HQ 0.2     | 0:74  | MIT                 | 0       |
| 0:75  | Pan Flute               | Pan Flute            | Fluid R3 GM                  | 0:75  | MIT                 | -4.2    |
| 0:76  | Blown Bottle            | Bottle Chiff         | Fluid R3 GM                  | 0:76  | MIT                 | -4.2    |
| 0:77  | Shakuhachi              | Shakuhachi           | GeneralUser GS 2.0.3         | 0:77  | GeneralUser GS v2.0 | +3.0    |
| 0:78  | Whistle                 | Whistle              | GeneralUser GS 2.0.3         | 0:78  | GeneralUser GS v2.0 | -4.0    |
| 0:79  | Ocarina                 | Ocarina              | GeneralUser GS 2.0.3         | 0:79  | GeneralUser GS v2.0 | -2.0    |
| 0:80  | Lead 1 (square)         | Synth Square         | FreePats GM 2022-10-26       | 0:80  | CC0-1.0             | -6.0    |
| 0:81  | Lead 2 (sawtooth)       | Saw Lead             | GeneralUser GS 2.0.3         | 0:81  | GeneralUser GS v2.0 | 0       |
| 0:82  | Lead 3 (calliope)       | Calliope Lead        | FluidR3Mono (MS General 0.1) | 0:82  | MIT                 | -1.6    |
| 0:83  | Lead 4 (chiff)          | Chiffer Lead         | Fluid R3 GM                  | 0:83  | MIT                 | 0       |
| 0:84  | Lead 5 (charang)        | Charang              | MuseScore General HQ 0.2     | 0:84  | MIT                 | 0       |
| 0:85  | Lead 6 (voice)          | Solo Vox             | Fluid R3 GM                  | 0:85  | MIT                 | -1.1    |
| 0:86  | Lead 7 (fifths)         | 5th Saw Wave         | MuseScore General HQ 0.2     | 0:86  | MIT                 | 0       |
| 0:87  | Lead 8 (bass + lead)    | Bass & Lead          | MuseScore General HQ 0.2     | 0:87  | MIT                 | 0       |
| 0:88  | Pad 1 (new age)         | Fantasia 2           | GeneralUser GS 2.0.3         | 12:88 | GeneralUser GS v2.0 | +2.9    |
| 0:89  | Pad 2 (warm)            | Warm Pad             | Fluid R3 GM                  | 0:89  | MIT                 | -9.0    |
| 0:90  | Pad 3 (polysynth)       | Polysynth            | FluidR3Mono (MS General 0.1) | 0:90  | MIT                 | 0       |
| 0:91  | Pad 4 (choir)           | Space Voice          | MuseScore General HQ 0.2     | 0:91  | MIT                 | 0       |
| 0:92  | Pad 5 (bowed)           | Bowed Glass          | GeneralUser GS 2.0.3         | 0:92  | GeneralUser GS v2.0 | 0       |
| 0:93  | Pad 6 (metallic)        | Metal Pad            | GeneralUser GS 2.0.3         | 0:93  | GeneralUser GS v2.0 | +1.1    |
| 0:94  | Pad 7 (halo)            | Halo Pad             | GeneralUser GS 2.0.3         | 0:94  | GeneralUser GS v2.0 | 0       |
| 0:95  | Pad 8 (sweep)           | Sweep Pad            | GeneralUser GS 2.0.3         | 0:95  | GeneralUser GS v2.0 | 0       |
| 0:96  | FX 1 (rain)             | Ice Rain             | GeneralUser GS 2.0.3         | 0:96  | GeneralUser GS v2.0 | 0       |
| 0:97  | FX 2 (soundtrack)       | Soundtrack           | GeneralUser GS 2.0.3         | 0:97  | GeneralUser GS v2.0 | +2.5    |
| 0:98  | FX 3 (crystal)          | Crystal              | MuseScore General HQ 0.2     | 0:98  | MIT                 | 0       |
| 0:99  | FX 4 (atmosphere)       | Atmosphere           | GeneralUser GS 2.0.3         | 0:99  | GeneralUser GS v2.0 | 0       |
| 0:100 | FX 5 (brightness)       | Brightness           | GeneralUser GS 2.0.3         | 0:100 | GeneralUser GS v2.0 | -1.6    |
| 0:101 | FX 6 (goblins)          | Goblin               | Fluid R3 GM                  | 0:101 | MIT                 | 0       |
| 0:102 | FX 7 (echoes)           | Echo Drops           | GeneralUser GS 2.0.3         | 0:102 | GeneralUser GS v2.0 | 0       |
| 0:103 | FX 8 (sci-fi)           | Star Theme           | FluidR3Mono (MS General 0.1) | 0:103 | MIT                 | 0       |
| 0:104 | Sitar                   | Sitar                | Fluid R3 GM                  | 0:104 | MIT                 | -2.5    |
| 0:105 | Banjo                   | Banjo                | GeneralUser GS 2.0.3         | 0:105 | GeneralUser GS v2.0 | +1.7    |
| 0:106 | Shamisen                | Shamisen             | Fluid R3 GM                  | 0:106 | MIT                 | -3.4    |
| 0:107 | Koto                    | Taisho Koto          | GeneralUser GS 2.0.3         | 8:107 | GeneralUser GS v2.0 | +1.8    |
| 0:108 | Kalimba                 | Kalimba              | FluidR3Mono (MS General 0.1) | 0:108 | MIT                 | 0       |
| 0:109 | Bagpipe                 | Bagpipe              | FluidR3Mono (MS General 0.1) | 0:109 | MIT                 | 0       |
| 0:110 | Fiddle                  | Fiddle               | GeneralUser GS 2.0.3         | 0:110 | GeneralUser GS v2.0 | -7.0    |
| 0:111 | Shanai                  | Shenai               | Fluid R3 GM                  | 0:111 | MIT                 | -1.5    |
| 0:112 | Tinkle Bell             | Tinker Bell          | GeneralUser GS 2.0.3         | 0:112 | GeneralUser GS v2.0 | -1.8    |
| 0:113 | Agogo                   | Agogo                | GeneralUser GS 2.0.3         | 0:113 | GeneralUser GS v2.0 | -6.2    |
| 0:114 | Steel Drums             | Steel Drums          | GeneralUser GS 2.0.3         | 0:114 | GeneralUser GS v2.0 | -1.6    |
| 0:115 | Woodblock               | Woodblock            | Fluid R3 GM                  | 0:115 | MIT                 | -3.9    |
| 0:116 | Taiko Drum              | Taiko Drum           | GeneralUser GS 2.0.3         | 0:116 | GeneralUser GS v2.0 | -3.9    |
| 0:117 | Melodic Tom             | Melodic Tom          | GeneralUser GS 2.0.3         | 0:117 | GeneralUser GS v2.0 | -3.7    |
| 0:118 | Synth Drum              | Synth Drum           | GeneralUser GS 2.0.3         | 0:118 | GeneralUser GS v2.0 | +4.5    |
| 0:119 | Reverse Cymbal          | Reverse Cymbal       | GeneralUser GS 2.0.3         | 0:119 | GeneralUser GS v2.0 | +4.0    |
| 0:120 | Guitar Fret Noise       | Fret Noise           | MuseScore General HQ 0.2     | 0:120 | MIT                 | 0       |
| 0:121 | Breath Noise            | Breath Noise         | GeneralUser GS 2.0.3         | 0:121 | GeneralUser GS v2.0 | +11.6   |
| 0:122 | Seashore                | Seashore             | GeneralUser GS 2.0.3         | 0:122 | GeneralUser GS v2.0 | +1.2    |
| 0:123 | Bird Tweet              | Birds                | GeneralUser GS 2.0.3         | 0:123 | GeneralUser GS v2.0 | +8.7    |
| 0:124 | Telephone Ring          | Telephone            | Fluid R3 GM                  | 0:124 | MIT                 | -1.2    |
| 0:125 | Helicopter              | Helicopter           | MuseScore General HQ 0.2     | 0:125 | MIT                 | 0       |
| 0:126 | Applause                | Applause             | Fluid R3 GM                  | 0:126 | MIT                 | -1.4    |
| 0:127 | Gunshot                 | Gun Shot             | Fluid R3 GM                  | 0:127 | MIT                 | 0       |
| 128:0 | Batteria standard       | Standard             | Fluid R3 GM                  | 128:0 | MIT                 | -1.5    |


## Licenza

Il soundfont nel suo complesso è distribuito sotto **GNU GPL versione 3 o successiva, con l'eccezione FreePats**,
perché contiene due strumenti FreePats sotto GPL (0:25 Steel-String Guitar e 0:33 Electric Bass 1).

L'eccezione stabilisce che la musica composta usando questi suoni non ricade per questo sotto la GPL.

Il testo completo è in [`LICENSE`](LICENSE); l'eccezione è in
[`LICENSES/FreePats_GPL-exception.txt`](LICENSES/FreePats_GPL-exception.txt).

Le altre parti mantengono le proprie licenze, compatibili con la GPL, e le loro note di copyright devono restare incluse:

| File                                                                                   | Riguarda                      |
|----------------------------------------------------------------------------------------|-------------------------------|
| [`LICENSES/MIT_FluidR3-GM.txt`](LICENSES/MIT_FluidR3-GM.txt)                           | Fluid R3 GM (MIT)             |
| [`LICENSES/MIT_MuseScore-General-HQ.md`](LICENSES/MIT_MuseScore-General-HQ.md)         | MuseScore General HQ (MIT)    |
| [`LICENSES/MIT_FluidR3Mono.md`](LICENSES/MIT_FluidR3Mono.md)                           | FluidR3Mono (MIT)             |
| [`LICENSES/GeneralUser-GS_License-v2.0.txt`](LICENSES/GeneralUser-GS_License-v2.0.txt) | GeneralUser GS (licenza v2.0) |
| [`LICENSES/CC0-1.0_FreePats.txt`](LICENSES/CC0-1.0_FreePats.txt)                       | strumenti FreePats CC0        |


## Sorgenti e crediti

Preset usati per sorgente:

- Fluid R3 GM: 50
- GeneralUser GS 2.0.3: 49
- MuseScore General HQ 0.2: 16
- FluidR3Mono (MS General 0.1): 9
- FreePats GM 2022-10-26: 5


### Fluid R3 GM

Copyright © 2000-2002, 2008 Frank Wen; © 2008 Toby Smithe. Licenza MIT.

Costruito in parte da campioni di pubblico dominio e in gran parte da registrazioni dell'autore, con il contributo di
Suren M. Seron, Scott Hanan, Steve Aupperle, Chris Gillman, Alex Taubr, Chris Prola, Andrew Klenk, Winfried Hubbe,
Dylan, Tim, Gort, Uros Katic ed Ethan Winer.


### MuseScore General HQ 0.2

Distribuito con MuseScore 4 come `MS Basic.sf3`: <https://github.com/musescore/MuseScore/tree/main/share/sound>.

FluidR3 di Frank Wen © 2000-02; conversione mono (FluidR3Mono) di Michael Cowgill © 2014-17;
adattamento di S. Christian Collins © 2018-19; Temple Blocks di Ethan Winer © 2002;
Drumline Cymbals di Michael Schorsch © 2016. Licenza MIT.


### FluidR3Mono (MS General 0.1)

Dal repository di MuseScore. Frank Wen © 2000-2002, Michael Cowgill © 2014-17, S. Christian Collins © 2018. Licenza MIT.


### GeneralUser GS 2.0.3

© 1997-2025 S. Christian Collins, licenza GeneralUser GS v2.0.

Sito ufficiale e download: <https://www.schristiancollins.com/generaluser.php>.


### FreePats General MIDI 2022-10-26

Progetto FreePats: <https://freepats.zenvoid.org/SoundSets/general-midi.html>.

| Posto | Strumento                | Autore                       | Licenza                    |
|-------|--------------------------|------------------------------|----------------------------|
| 0:24  | Nylon-String Guitar      | Roberto (zenvoid.org)        | CC0 1.0                    |
| 0:25  | Steel-String Guitar      | FlameStudios (Gary Campion)  | GPL-3.0+ con eccezione     |
| 0:27  | Electric Guitar (clean)  | Roberto (zenvoid.org)        | CC0 1.0                    |
| 0:33  | Electric Bass (finger)   | FlameStudios (Gary Campion)  | GPL-3.0+ con eccezione     |
| 0:80  | Synth Lead 1 (square)    | Roberto (zenvoid.org)        | CC0 1.0                    |


## choices.json

Elenco delle scelte usate per assemblare il soundfont.

Per ogni posto indica la sorgente, la posizione originale del preset (`bank`, `prog`), la licenza
e la correzione di volume in dB (`db`).
