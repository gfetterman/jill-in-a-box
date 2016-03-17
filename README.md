# jill-in-a-box
Audio filtering for the Intan EVAL board ADC inputs

The Intan EVAL board ADC accepts 0 to +3.3V inputs. Jill-in-a-box takes audio signals (+/-3.3V), raises their zero to +1.15V, constrains their amplitude to fit between 0 and +3.3V, and applies a 10kHz anti-aliasing filter.

## Version history
* v1.2: anti-aliaising filter passive components changed from (10kOhm, 2000pF, 1000pF) to (40kOhm, 560pF, 270pF) to use more common components. Filter cutoff is still 10kHz. Specific changes:
  * R25, R26, R27, R28, R29, R30, R31, R32: were 10kOhm, now 39kOhm
  * C14, C18, C19, C21: were 1000pF, now 270pF
  * C13, C17, C20, C22: were 2000pF, now 560pF
* v1.1: added 2-pole Butterworth anti-aliasing filter, cutoff 10kHz, on each channel
* v1.0: first production version
