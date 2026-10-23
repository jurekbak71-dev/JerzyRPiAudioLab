# CARD-05 — MiniDexed: ośmiokrotny syntezator FM DX7

Źródło: https://github.com/probonopd/MiniDexed

## Co jest ciekawe
MiniDexed uruchamia się bez Linuxa (bare metal), może oferować do 8 niezależnych instancji Dexed FM i ładować banki DX7 `.syx`.

## Typ karty
Osobna karta FAT32 z plikami firmware z oficjalnego wydania MiniDexed; nie jest to standardowe Raspberry Pi OS.

## Bardzo ważne
Nie zakładaj, że HeadRush Core USB Audio zadziała. Oficjalne instrukcje wyróżniają PWM (jack słuchawkowy), HDMI i I2S. USB Audio wymaga indywidualnego sprawdzenia wersji/patchy i nie jest zagwarantowane.

## Dodatkowy sprzęt
Najprostszy start: HDMI audio lub wyjście 3,5 mm z RPi (słabsza jakość), klawiatura MIDI USB do grania; bez MIDI można sięgnąć po pliki demonstracyjne i narzędzia banków.
