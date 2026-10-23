# Jerzy MultiFX 0.4 — Guitar / BassAmbient / CAB IR / MIDI Learn

Główne źródło: [projects/JerzyMultiFX](../projects/JerzyMultiFX) — submodule śledzący gałąź development v0.4. Kod źródłowy jest w oryginalnym repozytorium [JerzyMemoryDelay](https://github.com/jurekbak71-dev/JerzyMemoryDelay/tree/feature/jerzy-multifx-v04-dual-ir-midi) i nie jest kopiowany/dublowany.

Kluczowe elementy v0.4:
- 13 wtyczek .so ARM64 z v0.3;
- dwa równoległe silniki audio: gitara FX i oryginalny natywny BassAmbient (base, pady, Krell);
- dwukanałowy CAB/IR Loader oparty na FFT, A/B, WAV, filtr LF/HF;
- wspólny mikser stereo i wyjście HeadRush Core;
- przypisywanie kontrolerów przez MIDI Learn i zapisywanie mapowań;
- telefon/tablet: 5 czytelnych kart, suwaki i przyciski dotykowe;
- usługi v0.4 na osobnej karcie RPi / port 8092, bez naruszania działającej v0.2.

Dokładna instrukcja offline, parametry, testy i zastrzeżenia:
[README v0.4](https://github.com/jurekbak71-dev/JerzyMemoryDelay/blob/feature/jerzy-multifx-v04-dual-ir-midi/deploy/multifx4/README.md).

## Klonowanie głównego repo

```sh
git clone --recurse-submodules https://github.com/jurekbak71-dev/JerzyRPiAudioLab.git
```

Sam ZIP GitHuba z repozytorium nadrzędnego **nie zawiera plików submodule**. Aby zrobić instalację offline, pobierz bezpośrednio ZIP gałęzi źródłowej MultiFX v0.4 z repo JerzyMemoryDelay.

Na działającej karcie MicroSD **CARD-00 Jerzy MultiFX v0.2 nic nie zmieniamy bez testów**.
