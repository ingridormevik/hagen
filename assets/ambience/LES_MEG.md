# Lydlag i HAGEN V45

`ambience_v45.js` leser filene i denne mappen. Alle filene er valgfrie. En fil som mangler, blir bare stille.

**23. nov. 2026:** Lydene er lagt inn:
- over bakken: vind og fuktige fottrinn;
- fuglene: kattugle (3), rugde og nattravn;
- under jorda: knirk (3), drypp (3) og resonans;
- datasenteret: et ekte serverrom-opptak, som spiller sammen med naturlydene i Algoritme. I Glitch blir naturlydene selv glitchet.

Alle er CC0-feltopptak. Kilde, lisens, utsnitt og sjekksum står i `PROVENANCE.json`. Alle er merket «listened: false»: Claude kan ikke lytte, så utsnittene er valgt etter lydstyrkekurven. Ingrid lytter og bytter det som ikke er riktig. Rugde-opptaket har også en gransanger i seg, ifølge tittelen. Filene bygges på nytt med `project-review\_working\make_ambience.py`.

Bruk egne opptak der du har dem, ellers CC0-feltopptak. Ingen generert lyd. Summingen fra datasenteret skal også være et ekte opptak, for eksempel fra et serverrom. Før hver fil inn i `PROVENANCE.json`: kilde, lisens, lenke og hvilket utsnitt som er brukt.

Claude kan ikke lytte. Du velger utsnittene selv. Claude kan klippe dem, lage myke loop-punkter og jevne ut nivået (LUFS) med ffmpeg når du har valgt.

## Filnavn

Over bakken (lastes når hagens lyd vekkes):
- `surface_wind_leaves.mp3`: vind i løv, loop, 30-90 s
- `surface_steps_wet.mp3`: fuktige fottrinn i en jevn gangtakt, loop, 10-20 s (høres bare når man går)

Nattfuglene (`birds_v45.js`) roper fra der de sitter eller flyr. Lyden er plassert i rommet og blir svakere på avstand:
- `owl_call_1.mp3`, `_2`, `_3`: kattugle, for eksempel «hu-hu-huuu» og «ke-vikk», 2-6 s hver. Ugla roper med 30-90 s mellomrom.
- `woodcock_1.mp3`, `_2`: rugdetrekk (den lave knurringen og det skarpe «pissp»), 1-3 s.
- `nattravn`: `nightjar_churr.mp3`, nattravnens surring, 5-15 s. Bare om sommeren.
Mangler filene, er fuglene stille.

Under jorden (lastes når man går ned):
- `roots_creak_1.mp3`, `_2`, `_3`: treverk som knaker, enkeltlyder
- `roots_drips_1.mp3`, `_2`, `_3`: vanndråper, enkeltlyder
- `roots_resonance.mp3`: dempet resonans, loop

Lyd fra stedet lyset leder mot (lastes over bakken, plassert i rommet og svakere på avstand):
- `beacon_root.mp3`: lyden en rotinngang kaller med, loop. Mangler filen, brukes ditt eget `assets/listening_edition/roots.mp3`.
- `beacon_egg.mp3`: lyden et påskeegg (funn, Mélusines sølvspeil) kaller med, loop. Mangler filen, brukes `assets/listening_edition/distant.mp3`.

Flasken på havet (lastes når flasken starter):
- `sea_waves.mp3`: bølger, loop. Kandidat: Skarsvåg Fjordatmo (jensfelger, CC0), ikke lyttet ennå.
- `sea_hum.mp3`: svak mekanisk summing, loop. Går gjennom et lavpassfilter på 320 Hz.

Legg ikke havlyd også i `assets/threshold/sea.mp3`, ellers spilles havet dobbelt. `assets/threshold/song.mp3` er fortsatt plassen for din egen sang.

## Nivåer

Startnivåene står i `HAGEN.ambience.config.levels` og kan prøves i konsollen mens hagen kjører, for eksempel `HAGEN.ambience.config.levels.wind=.2`. Når du har funnet nivåer du liker, legger Claude dem inn i `ambience_v45.js`.
