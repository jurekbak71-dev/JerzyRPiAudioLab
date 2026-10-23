# Sprzęt, karty microSD i checklista

## Baza
- Raspberry Pi 4 Model B, zasilacz odpowiedni dla RPi4.
- HeadRush Core przez USB; w sprawdzonym Jerzy MultiFX urządzenie ALSA: `hw:CARD=Core,DEV=0`.
- W sprawdzonym Jerzy MultiFX: JACK 44.1 kHz, 64 frames, 3 periods; input `system:capture_1`; playback `system:playback_1/2`.
- Powyższe **nie** są bezpośrednio przenośne do innych obrazów OS.

## Karty
Zalecane: oddzielna karta A1/A2 32 GB lub 64 GB na każdy projekt; dla samplera z rozbudowaną biblioteką 64/128 GB. Nie formatuj karty produkcyjnej MultiFX.

## Bezpieczna procedura
1. Zanotuj nazwę aktualnej karty i zrób kopię zapasową, jeśli to karta ważna.
2. W Windows uruchom Raspberry Pi Imager i wskaż **właściwą** kartę, nie dysk systemowy.
3. Dla OS z dedykowanym obrazem wybierz obraz niestandardowy. Dla Linuxa użyj zalecanej wersji Raspberry Pi OS.
4. Ustaw SSH i sieć, jeśli obraz oferuje tę opcję. Własne dystrybucje nie zawsze stosują ustawienia z Imagera.
5. Po uruchomieniu każdej karty sprawdź: ping/SSH, wykrycie HeadRush przez `aplay -l`, parametry ALSA/JACK, dźwięk w obie strony, opóźnienia, obciążenie i XRUN.
6. Testuj na niskim poziomie wyjściowym, unikaj sprzężeń i przesterowania.
7. Przed przełożeniem karty: `sudo poweroff`, poczekaj na wyłączenie, odłącz zasilanie.

## Plan rejestru testów
W każdym `sd-cards/CARD-XX` zanotuj datę, obraz/wersję, URL, SHA256, audio, CPU, XRUN, opóźnienia, działanie po restarcie i wnioski.
