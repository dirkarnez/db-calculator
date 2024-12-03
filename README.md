db-calculator
=============
db= 10log(p/pref)
### TODOs
- Gain to db (20 × log10(20) = 26 dB)
- Analog DB
  - pascal
  - voltage
    - dbV = 20 log(Vrms / 1V)
      - 0dBV = 1V (less than 0dBV = less than 1 V, vice versa)
  - dBSPL
  - dbu
- Digital DBs
  - dBFS (in daw, 0 to minus infinity)
    - DAW waveform uses -1 to 1 digital value
      - unitless amplitude, not DB*
      - we use float to store it
      - to be converted to dbFS for digital fader (amplitude 1 = dBFS = closest to digital clipping)
        - dBFS = 20log( (absolute value instantaneous amplitude) / 1)
          - absolute = signed and unsigned digital audio data values is declared in WAVE header, both takes same data size, therefore it does not matter
          
- [工具：VRMS/dBm/dBu/dBV计算器 | Analog Devices](https://www.analog.com/cn/resources/interactive-design-tools/dbconvert.html)
- http://www.onebandsystem.com/node/582
- log / linear

- [The decibel explained! dB SPL (sound pressure level) and dBFS - Ep. 02 - YouTube](https://www.youtube.com/watch?v=ERMrgyIMxdg) 
- dBm
- dbu
- dBTP
- dBov
dBO   