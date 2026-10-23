# Jerzy RPi Audio Lab

Osobne projekty audio na Raspberry Pi 4B, uruchamiane z **osobnych kart microSD**. Ten katalog nie ingeruje w działający Jerzy MultiFX i HeadRush Core.

## Jerzy MultiFX v0.4 — najnowszy projekt własny

**Kod źródłowy jest podłączony jako [submodule projects/JerzyMultiFX](projects/JerzyMultiFX)**, wskazujące na wersję rozwojową 0.4 w repo JerzyMemoryDelay. Po `git clone --recurse-submodules` można rozwijać całość w ramach laboratorium RPi.

- Dwa silniki: gitara z 13 modułami efektów i samogeneratywny BassAmbient (bas/pady/Krell).
- CAB/IR Loader z dwoma IR WAV na końcu toru gitary, **przed wspólnym mikserem**.
- MIDI Learn dla efektów, syntezatora i miksera, sterowanie dotykowe iPhone/iPad.
- Instalacja testowa v0.4: osobne usługi i panel `http://10.42.0.1:8092/` — **nie rusza działającej karty v0.2**.

[Dokumentacja v0.4 i instalacja offline](docs/MULTIFX4.md) · [PR rozwojowy](https://github.com/jurekbak71-dev/JerzyMemoryDelay/pull/4)

## Sprzęt docelowy
- Raspberry Pi 4 Model B (64-bit, gdy projekt obsługuje Linux)
- HeadRush Core jako USB Audio, już sprawdzony z ALSA/JACK w Jerzy MultiFX
- Konfiguracja bez monitora, o ile oprogramowanie na to pozwala: Windows + SSH; iPhone / iPad jako panel webowy
- Priorytet: bez dodatkowych zakupów i lutowania

## Kolejność eksperymentów
1. **CARD-01 PiPedal** — gitara, LV2, IR/NAM, telefon/tablet.
2. **CARD-02 Zynthian** — instrumenty, soundfonty, sekwencery, MIDI i webconf.
3. **CARD-03 Patchbox OS / MODEP / Orac** — modularny pedalboard i środowiska generatywne; UWAGA na wiek obrazu.
4. **CARD-04 CamillaDSP** — konwolucja, korekcja i matryce routingu.
5. **CARD-05 MiniDexed** — 8 syntezatorów DX7, ale nie gwarantujemy zgodności z HeadRush USB Audio.
6. **CARD-06 Pure Data / SuperCollider** — generatywna muzyka i eksperymentalne DSP.

**CARD-00 to działająca karta Jerzy MultiFX. Zachować jako wzorzec; nie nadpisywać.**

## Zasada jednej karty = jedno środowisko
- Każdy system flashujemy na oddzielną kartę microSD.
- Nie instalujemy nowych projektów na karcie produkcyjnego MultiFX.
- Przed zmianą karty: poprawnie wyłączyć RPi, odłączyć zasilanie, przełożyć kartę i uruchomić.
- Po flashowaniu każda karta wymaga własnej konfiguracji sieci, SSH i ewentualnie audio.
- Działający wcześniej adres `10.42.0.1` i hotspot `Jerzy-MultiFX` nie są automatycznie dziedziczone przez inne dystrybucje.
- HeadRush Core sprawdzony w **naszym** systemie; z innymi systemami wymaga testu ALSA/JACK.

Szczegóły w [PROJECTS.md](PROJECTS.md), [docs/HARDWARE.md](docs/HARDWARE.md) i podfolderach `sd-cards/`.

## Repozytoria źródłowe
Zamiast kopiować do tego repo pełen kod innych autorów, zapisujemy oficjalne linki, instrukcje, konfiguracje i wyniki testów. Kod projektu zewnętrznego pozostaje w upstream, zgodnie z licencją.

## Stan
Katalog i plan techniczny. Żadna karta oprócz istniejącej Jerzy MultiFX nie została przez ten szablon przygotowana ani przetestowana.
