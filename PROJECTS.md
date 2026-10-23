# Analiza projektów audio na RPi 4B

| Projekt | Co daje | System / karta | HeadRush Core USB | Sterowanie | Priorytet |
|---|---|---|---|---|---|
| PiPedal | Efekty gitarowe LV2, IR, modelowanie NAM | Raspberry Pi OS + instalacja aplikacji | Możliwe, **do zweryfikowania** | Panel WWW na telefonie | 1 |
| Zynthian | Multisyntezator, sampler, MIDI, sekwencer, looper | Własny obraz ZynthianOS | Obsługa USB audio przewidziana, **konfiguracja/test** | Webconf i interfejs zdalny | 2 |
| Patchbox OS + MODEP | Modułowa pedalboard LV2 | Własny obraz Patchbox OS | Obsługa USB w instalatorze, **test** | Panel WWW MODEP | 3 |
| Patchbox OS + Orac | Wirtualny modularny instrument, generatywne patche | Jak wyżej, osobna karta opcjonalna | **Test** | MIDI/OSC zależne od patcha | 3 |
| CamillaDSP | FIR/IR, EQ, zwrotnice, routingi i korekcja pomieszczenia | Raspberry Pi OS + instalacja | ALSA/JACK dostępne, **test** | CamillaGUI WWW | 4 |
| MiniDexed | Osiem silników FM typu DX7 | Bare metal (bez Linuxa), zawartość boot na SD | **Nie zakładać kompatybilności USB Audio**; zalecane HDMI / PWM / I2S | MIDI USB, opcjonalnie panel | 5 |
| Pure Data / SuperCollider | Krell, ambient, synteza generatywna, DSP | Raspberry Pi OS lub Patchbox OS | Możliwe pod JACK, **test** | OSC/MIDI/skrypty | 6 |

## Wiarygodne źródła

- PiPedal: https://rerdavies.github.io/pipedal/ oraz https://github.com/rerdavies/pipedal
- Zynthian: https://zynthian.org/ i konfiguracja bez dedykowanego hardware: https://wiki.zynthian.org/index.php/No_Hardware_Build
- Patchbox OS: https://blokas.io/patchbox-os/ i https://blokas.io/patchbox-os/docs/
- Orac: https://github.com/TheTechnobear/Orac
- MiniDexed: https://github.com/probonopd/MiniDexed
- CamillaDSP: https://www.camilladsp.com/
- Pure Data: https://puredata.info/
- SuperCollider: https://supercollider.github.io/

## Ważne zastrzeżenia

- Oficjalny obraz Patchbox OS dostępny w sprawdzonej dokumentacji miał datę **17.05.2022**. To stara podstawa systemowa; weryfikować aktualizacje i zgodność przed wykorzystaniem w internecie.
- MiniDexed działa bez jądra Linux i jego urządzenia audio **nie są automatycznie** takie same jak dla ALSA/JACK; działający HeadRush Core w Jerzy MultiFX nie dowodzi zgodności z MiniDexed.
- PiPedal jest instalowaną aplikacją na zgodnym Linuxie, **nie** uniwersalnym obrazem karty do flashowania.
- Zynthian jest osobnym systemem i może wymagać początkowego monitora/klawiatury lub właściwej konfiguracji sieci do pracy headless.
- Wszystkie nowe systemy to oddzielne konfiguracje Wi-Fi, adresu IP, użytkownika, haseł, SSH i urządzenia audio.
- Pełny koszt CPU/latencja na RPi 4B nie jest znany przed praktycznymi testami.
