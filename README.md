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
  - **dbu**
- Digital DBs
  - dBFS (in daw, 0 to minus infinity)
    - DAW waveform uses -1 to 1 digital value
      - unitless amplitude, not DB*
      - we use float to store it
      - to be converted to dbFS for digital fader (amplitude 1 = dBFS = closest to digital clipping)
        - dBFS = 20log( (absolute value instantaneous amplitude) / 1)
          - absolute = signed and unsigned digital audio data values is declared in WAVE header, both takes same data size, therefore it does not matter
            - `char` = 0 - 255 = 8 bit = 1 byte = FF
            - 24 bit = 4 `char`s
            - sine wave to 24 bit signed .wav = `casted to 4 char`(`sine wave output in signed decimal float with value less than 1` * `max amplitude which is calculated by 2^ 24 bitdepth` - 1)
            - PCM is bascially digital output from ADC (10bit ADC = 0 - 1023)

- [工具：VRMS/dBm/dBu/dBV计算器 | Analog Devices](https://www.analog.com/cn/resources/interactive-design-tools/dbconvert.html)
- http://www.onebandsystem.com/node/582
- log / linear
- dBm
- dbu
- dBTP
- dBov
dBO   

### Tutorials
- [Line level - Wikipedia](https://en.wikipedia.org/wiki/Line_level)
- [Audio normalization explained: a complete guide to balanced sound](https://waves-system.com/en/actualites/audio-normalization/)
- [WAV Files: File Structure, Case Analysis and PCM Explained](https://www.videoproc.com/resource/wav-file.htm)
- [The decibel explained! dB SPL (sound pressure level) and dBFS - Ep. 02 - YouTube](https://www.youtube.com/watch?v=ERMrgyIMxdg)
- https://assets.wavescdn.com/pdf/plugins/vu-meter.pdf
- [常用音频单位简介：dBSPL、dBm、dBu、dBV、dBFS-CSDN博客](https://blog.csdn.net/u010538116/article/details/80762816)
- [mic in、line in&line out、speaker out、headphone out　区别_mic in和line in line out-CSDN博客](https://blog.csdn.net/u010538116/article/details/80386813)
