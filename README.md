# Jerzy RPi Audio Lab

Osobne projekty audio na Raspberry Pi 4B, uruchamiane z **osobnych kart microSD**. Ten katalog nie ingeruje w działający Jerzy MultiFX i HeadRush Core.

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
