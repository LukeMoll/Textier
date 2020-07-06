# Textier
_Low-cost mechanical macro pad_


## Known issues
### "Blackpill" board
 - STM32F411CE only has two USB endpoints - not enough for CircuitPython's MSC & CDC in addition to HID and/or AUDIO (MIDI)
     - Can remove MSC and use [ampy](https://github.com/scientifichackers/ampy) instead
 - Some LED IO shared with optional flash memory footprint
 - Wide DSA profile keycaps conflict with the blackpill board edge when fully inserted in socket
 
Mostly solved by [greenpill](https://github.com/Stary2001/greenpill)

### Blackpill CircuitPython port
 - `rotaryio` [not implemented in STM port](https://github.com/adafruit/circuitpython/issues/2544)
 - `C15` shown as "in use" when try to construct `NeoPixel(board.C15, 9)`
