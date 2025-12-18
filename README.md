# Alignment notes on the venerable Datong ASP Automatic RF Speech Processor.

Note these apply to the metal box version, not the later "blue plastic box" version.

 
![datong](https://github.com/rszemeti/AmateurRadioNotes/assets/46870724/5c26d1f8-96a6-467c-a03f-78efc41d1735)

### PSU Check
Apply power, check consumption 15 to 20 mA  Check any of the Vs points for 6.1 to 6.2V
 
### Master oscillator. 
Check Pin 2 of  IC6 for clock, adjust L3 for roughly 60 kHz, not critical, but once set, leave it!
 
### Modulator balance.
Check TP1 (Pin 5, IC 4, or the convenient leg of the resistor near it) with a high-impedance (10x) oscilloscope and probe.  This is the modulator output.
No audio input, select 0dB switch to minimise input noise.  Adjust VR1 and VR2 to achieve modulator balance. Repeat until  minimised, some interaction. Less than 1mV peak to peak on TP1 is good.  

### RF Bandpass Filter
Apply 1 kHz tone, 1mV to the audio input, speech light should light. Threshold is ~ 0.5mV on "LO" setting, 150 mV on "HI" setting.
Set 100mV on signal generator and "LO" input, 6dB of clip on the push buttons
Adjust  L1 for max audio output with 3kHz audio input
Adjust L2 for max audio output with 300Hz audio input
 
Note that there does seem to be a pronounced "top end" slope, with greater output at 3kHz than at 300Hz.
 
### Output Levelling
Set 1kHz, 100mV and 30dB clip, note output level on scope.
Set 0dB clip, Adjust VR3 such that 0dB ouptut level is same as 30dB level. Going through the gains 0dB to 30dB switch by switch should produce the same level.
 
Output on the "hot" end of the output trimmer should be around 130mV pk-pk
 
Circuit diagram is here:  
[Datong_ASP_sch.pdf](https://github.com/rszemeti/AmateurRadioNotes/files/11781660/Datong_ASP_sch.pdf)
