# NYSTHI modules for VCV Rack 

![](https://github.com/nysthi/nysthi/blob/master/images/allmodules20180830.png)

Modules:
1. [Reverbs](readme.md#reverbs)
   - [MVerb](readme.md#mverb)
   - [TwistedMVerb](readme.md#twistedmverb)
   - [PLATEVERB](readme.md#plateverb) 
   - [DISSONANTVERB](readme.md#dissonantverb)  
2. [Delays](readme.md#delays)
   - [DualSignalDelayer](readme.md#dualsignaldelayer)
   - [NYECHOECOECO](readme.md#nyechoecoeco)
   - [Model 277](readme.md#model-277)
   - [XATTO TIME](readme.md#xatto-time)
3. [Recorders](readme.md#recorders)
   - [2 Channel MasterRecorder](readme.md#2-channel-masterrecorder)
   - [4/8 MultiTrack Recorder](readme.md#4-8-multitrack-recorder)
4. [Logic](readme.md#logic.)
   - [Logic](readme.md#logic)
5. [Modulation](readme.md#modulation)
   - [NYStereoPhaser](readme.md#nystereophaser)
   - [NYStereoChorus](readme.md#nystereochorus)
6. [Control Voltage](readme.md#control-voltage)
   - [Surveillance](readme.md#surveillance)
   - [CONST ADD MULT](readme.md#const-add-mult)
7. [Envelopes](readme.md#envelopes)
   - [NYEnvFollower](readme.md#nyenvfollower)
   - [AttackDecay EG](readme.md#attackdecay-eg)
   - [DelayAttackHoldDecay EG](readme.md#delayattackholddecay-eg)
   - [DX7ENVELOPE](readme.md#dx7envelope)
   - [8 ATTACK DECAY](readme.md#8-attack-delay)
8. [Oscillators](readme.md#oscillators)
   - [LFOMULTIPHASE](readme.md#lfomultiphase)
   - [DEEPNOTE](readme.md#deepnote)
9. [Visuals and Monitoring](readme.md#visuals-and-monitoring)
   - [Single VU Meter](readme.md#single-vu-meter)
   - [Dual VU Meter](readme.md#dual-vu-meter)
   - [HotTuna](readme.md#hottuna)
   - [SPECTRAL](readme.md#spectral)
10. [Samplers](readme.md#samplers)
   - [complexSimpler](readme.md#complexsimpler)
   - [QuadSimpler](readme.md#quadsimpler)
11. [Filters](readme.md#filters)
   - [Dica33](readme.md#dica33)
   - [4DCB](readme.md#4dcb)
12. [Sequencing](readme.md#Sequencing)
   - [SQUONK](readme.md#squonk)
13. [Source of Uncertainty](readme.md#source-of-uncertainty)
   - [SoyModelSOU](readme.md#soymodelsou)
   - [SOU UTILS](readme.md#sou-utils)
14. [Mixing and Panning](readme.md#mixing-and-panning)
   - [VECTOR MIXER](readme.md#vector-mixer)
   - [QUAD PANNER](readme.md#quad-panner)
15. [Clocks](readme.md#clocks)
   - [TIMEX](readme.md#timex)
   - [CLOCK MULTIPLIER](readme.md#clock-multiplier)
16. [Quantizers](readme.md#quantizers)
   - [SCALA QUANTIZER](readme.md#scala-quantizer)
   - [QUAD SIMPLER SLICER QUANTIZER](readme.md#quad-simpler-slicer-quantizer)
   - [EQUAL DIVISION QUANTIZER](readme.md#equal-division-quantizer)
   
---
   
## Reverbs
### MVerb

VCV RACK port of the [mverb](https://github.com/martineastwood/mverb)

### TwistedMVerb

MVerb with cv control of Mix, Density, LP Freq, Decay, Damping, Gain, and Freeze

### HiVerb

a mutation of the MVERB using HIPASS filtering

### PLATEVERB

it's a new reverb based on the famous Dattorro paper. Was tweaked to adapt it to every samplerate and to add Early reflections. The tail is very smooth!

There is no control for the roomsize, you need to work on the decay

PARAMS
* EARLY REFLECTIONS MIX: ER are 2 8 tap fractional delay lines with 16 differents times. the mix is a
balance between incoming signal and the reflections
* PREDELAY from 0 tp 400 msecs
* PREDELAY MIX, balance from previous stage and the delayed signal
* BANDWIDTH is the frequency passed
* DECAY the control of the tail (feedback)
* DAMPING
* WET-DRY balance between input and effect
* BOOST from 0 to 2.0 to push up or down the signal if needed
* FREEZE (triggable too) freeze the effect with the infinite decay

## DISSONANTVERB

it's a modification of the PLATEVERB inserting 2 pitchshifter in the feedback loop

the effect is quite dramatic (and soundtrackable)

* DISSONANCE1 controls the shifting of the first DISSONATOR (CV controllable)
* DISSONANCE1 MIX controls balance between original signal and shifted signal
* DISSONANCE2 controls the shifting of the second DISSONATOR (CV controllable)
* DISSONANCE2 MIX controls balance between original signal and shifted signal
   * DISSONANCE1 and DISSONANCE2 have different curves: smoother the 1, larger range the 2
* all the other parameters are PLATEVERB equivalent

---

## Delays

### DualSignalDelayer

Top half can delay one signal and the bottom half can delay the other.

### NYECHOECOECO
a virtual BINSON Echorec homage, with 6 play HEADS

PARAMETERS:
* SPEED to trim the speed of the disc (the speed is expressed in cm/s)
   * a SPEED of about 12 cm/s is exactly 1 round per second
* Each Play Head: 
   * can be activated by BUTTON (on the HEAD) or by TRIG
   * has a trimming function (to virtual move the headform -20% to +20% around the disc)
   * has a display for the current delay
   * has a volume (for the delay mixed)
   * has a TAP out TAP in (so you can process a delayed signal and insert it back in the chain)
* THE SWELL is activated deactivating the ERASE HEAD
   * THE SWELL pot controls from ECHO to infinite feedback (beware)
* DRY - WET is a mix from original input signal and the processed signal
* INPUT and OUTPUT have both a gain control
* INPUT has a simulated OCCHIO magico: if the 2 wings connect in the center, signal is clipping

### Model 277

signal delay unit inspired by [Buchla 277](https://www.modulargrid.net/u/buchla-277-)

### XATTO TIME

4 delays which can accept audio or CV
* delay from 0.01 msecs to 9999.99 msecs
* click and drag to set PRECISE timing
* no filtering in the signal path
* there are 2 IN, the IN2 is controlled by an attenenverter (to create feedbacks)
* every delay is clockable and tempo is computed with the tempo detector
   * the detected tempo is multiplied by a factor from 1 to 99

---

## Recorders

### 2 Channel MasterRecorder

Record 2 channels of audio to one 2 channel wav file. (Stereo)

### 4/8 MultiTrack Recorder

Record 8 channels of audio to one 8 channel wav file.

---

## Logic.
### Logic

Boolean logic operations.

* white sockets: inputs
* black sockets: outputs

---

##Modulation
### NYStereoPhaser

Phaser

### NYStereoChorus

Chorus

---

## Control Voltage
### Surveillance

Attenuator with one input and 10 different attenuated outputs

### CONST ADD MULT
is a QUAD PRECISE constant, ADDER, MULTIPLIER.
* "A IN" is OPERATOR 1
* "B IN" is OPERATOR 2
* "B OUT" is a CHAIn out of the OPERATOR 2
* the DISPLAY is the value and can be set precisely using MOUSE drag
   * the MOUSE dragging is positional, the more you are on the left, the more faster the value is updated
   * B value can be set precisely til 0.0001 steps
* right clik will reset to 0
* "A + B" output is the sum of A + B. if A is missing, is 0 + B
* "A x B" output is the product of A x B. if A is missing, is 0 x B

---

## Envelopes
### NYEnvFollower

a classic Envelope Follower with :

* GAIN IN (multiply the incoming signal form 1 to 10)
* ATTACK time (from 0.5 to 250 msecs)
* RELEASE time (from 0.5 to 250 msecs)
* SCALE multiply the signal for -20v to 20v
* OFFSET add to the signal from (-20v to 20v)
* DELAY ENV delays the generated signal from 0 to 200msecs
* ENVELOPE OUT the generated signal
* DELAY SIGNAL delays the original signal from 0 to 200 msecs
* SIGNAL OUT the original signal in, shifted by DELAY SIGNAL
* OSZI (oscilloskope) ON/OFF button (to spare cpu time!)
* SCALE gain of the signal and time

### AttackDecay EG

A standard Envelope with some Buchla 281 features

### DelayAttackHoldDecay EG

Also called complex DAHD

An envelope with cv in for almost every parameter.  Also has Output triggers at the bottom for the various stages.

### DX7ENVELOPE

emulation of the 4 rates 4 levels DX7 operator envelope

### 8 ATTACK DECAY

an 8 channel version of the AttackDecay EG

---

## Oscillators
### LFOMultiPhase

LFO with 8 different phase outputs of the signal.

* morphing is activate via "discrete - morph" switch
* morphing is modulable via CV input and controllable via waveshape selector and modulation index

### DEEPNOTE

An attempt to create a THX sound type generator

* there are 4 classes of frequencies
   * freq one is spread on 5 octeves
   * freq 2 on 6 octaves
   * freq 3 and4 on low mid and high
* there are PAN animators and SPECTRUM animators (and AMPLI animators too)
* **this will consume on my MAC about 50% of the resources, so best use is to record it, alone...**

---

## Visuals and Monitoring
### Single VU Meter

VU Meter with context menu-controllable RMS and PEAK HOLD Timing

### Dual VU Meter

The top half is one VU Meter and the bottom half is another VU Meter

### HotTuna

the VU meter will give info about the note, the big black one text is the frequency (expressed as MIDINOTE TAG) we are targeting;
* starts to become GREEN when is at less than 4 % deviation
* and RED when there is less than 0.5% of deviation
* the TUNER works on SIGNALs (vco inputs, or any signal you want)
* and with VOLTAGES (translated interanally in frequencies) + the offset given by the OCTAVE
* POT (goes from -2 to +2 octaves)
* the IN SIGNAL input has priority (if both are used)
* add TUNE "A = " param (so you can tune to "432Hz" now")
* added TUNE reference OSCILLATOR
* DO RE MI mode
* INSTABILYT light (the background will become lighed RED if reading is invalid)
* IF FREQ not recognized, goes to ZERO

### SPECTRAL
a real time spectrograph wannabe
* is using very very little of CPU
* explore different visualizations and windowing functions using the contextual menu

---

## Samplers
### complexSimpler

* the LFO is morphable (the lights give you the idea)
* ANTI-CLICK param, filter to remove clicks in sample start and ends points
  * the ANTI CLICK goes from 0 to 100 ms
* if GATED on, the sample will stop when TRIG/GATE is off
* ability to open WAV or AIFF files (PCM)

### QuadSimpler

the son of SIMPLER, is a multi sample player with integrated stereo mixer
* GLOBAL parameters is CHAIN IN of another mixer that will be summed to Channel L and R
* the idea is to have multiple QuadSimpler to have a BIG bank of samples

---

## Filters
### Dica33

* filter module...
* very unstable, but usable

### 4DCB

a 4 times DC BLOCK filter, current sample rate aware
* needed to avoid unwanted Direct Current build up a the end of a module


---

## Sequencing
### SQUONK

it's a PROGRAMMER, STAGE sequencer, Sampler TRIGGER, freely inspired by [Serge TKB](http://www.serge-fans.com/wiz_seq.htm)

12 steps with 11 lines of programming

* line 1: TRIG IN: will select the stage triggered
* line 2: STAGE: is the stage selector by button. when in sequencer mode the current step will light up
* line 3: 5X: voltage multiplier for A B C D E channels
* line 4: A: CV channel from 0 to 2 volts
* line 5: B: CV channel from 0 to 2 volts
* line 6: C: CV channel from 0 to 2 volts
* line 7: D: CV channel from -1 to 1 volts
* line 8: E: CV channel from -1 to 1 volts
* line 9: MODE: TRIG mode; if bright yellow, CV and TRIG out, if dark yellow, only CV out, if black step is jumped
* line 10: REP: if the sequencer is clocked will retrig the step from 1 to 8 times (subdivisions) (ratcheting)
* line 11: TRIG OUT: single PULSE out when the stage is selected

Bottom Section

* SEL knob: will select the current stage
* SEL CV input: selection of stage using CV (0 -> 10v)
* CLK IN CLK OUT: to clock the sequencer (and output the same clock to other devices)
* UP TRIG and BUTTON: if ON the sequence will go UP (normally is DOWN)
* RND btn: if light up the next stage is randomized
* OUTS A B C D E are the CV outs of the sequencer
* ROT knob, from -5 to +5, is the number of steps the yellow channel will rotate jump and rotate if in sequencer mode
* LAST trig out: PULSE out when last step is reached
* TRIG (global): current stage TRIG out (with repetitions if any)
* CHAIN A B C D E and CHAIN TRIG are useful when chaining many SQUONKs (to have just one connection for the CV and TRIGs)
* START STOP RESET: sequencer status controls by BUTTON or by TRIG
* RANDOMIZE ALL: must be pressed with COMMAND KEY (too dangerous!)

## Source of Uncertainty
### SoyModelSOU

IS an imitation of the FLUCTUATING, QUANTIZED and STORED voltages sections of the [Buchla 266 Source of Uncertainty](https://www.modulargrid.net/u/buchla-266-)

FLUCTUATING RANDOM VOLTAGES 1
* control TIME via CV and KNOB: from 0.05 to 50 sampling per seconds
* OUTS: SMOOTH, HARD (the sampled voltage), PULSE ( when HARD > 0.5)

FLUCTUATING RANDOM VOLTAGES 2
* control TIME via CV and KNOB from 0.05 to 50 sampling per seconds
* has a different smoothing function that can be controlled via CV
* OUTS: SMOOTH, HARD (the sampled voltage), PULSE (when HARD > 0.5)

QUANTIZED RANDOM VOLTAGES
* 2 sections: 2^n and n+1, where N is form 1 to 6 (established via CV and KNOB)
* the n+1 distribution is a Triangular distribution (like throwing 2 dice)
* n+1 are in 1V jumps
* 2^n are in 1/12V jumps

STORED RANDOM VOLTAGES
* Random with SKEWING function (CV controllable) to have more events in LOW MID or HIGH ranges

### SOU UTILS
perfect companion for the SOYMODELSOU, to scale and create arabesque (Is 3 parts of 2 repeated sections)
	
SCALER OFFSETTER 1 & 2 (2 section equivalents)
* ACCEPT AUDIO or CV SIGNAL IN
* SCALE for -2 to +2 times, the CV accepts from 0 to 10V and is scaled to 0->1 multiplied SCALE value
* scale function = SCALE or (if plugged in a CV) (SCALE * CVIN * 0.1 * 0.5);
* OFFSET from -10v to +10v
* OFFSET CV accepts any value
* final OFFSET FORMULA = clamp(OFFSET + OFFSET CV , -10, +10)
* output AUDIO or CV

OCTAVE FOLDER 1 & 2 (2 section equivalents)
* for any voltage coming in IN OVER MAX will be subtracted 1.0 till is reported UNDER MAX
* for any voltage coming in IN UNDER MIN will be added 1.0 till is reported OVER MIN
* IS perfect to use with Quantized RV section N^2 of the SoyMODELSOU, to reports the voltage into certain octaves
* ACCEPT a SIGNALCV type typically
* MIN is set from 0 to 9V
* MAX is set from 1 to 10V
* if MAX is equal or less than MIN, is set to MIN + 1
* OUTPUT the FOLDED SIGNALCV

ASR 1 & 2 (2 section equivalents)
* is a 4 cells ASR
* accept SIGNAL CV or AUDIO IN
* EVERY PULSE advance the content of the cells

---

## Mixing and Panning
### VECTOR MIXER
The vector mixer is highly inspired to joystick and vector functions of the Prophet VS. Combined with JW XYPAd, can emulate the 2D Vector Envelope as well
* the "joystick" position could be set by MOUSE, by X & Y position
and by AZIMUTH & MAGNITUDE. 
* X & Y has precedence on AZI & MAGN that has precedence on MOUSE.
* INPUT could be SIGNAL AUDIO or CV. 


# QUAD PANNER
is an old style sound source placement using a quadraphonic system, and implements some of the functionalities of a single channel of the Buchla 227e

position of the source can be established with MOUSE, or by X and Y Position, or by AZIMUTH and MAGNITUDE, or by SWIRL (a la 227e)
* the SWIRL is internal LFO that rotates the sound source for teh 4 outputs, with RATE and AMPLI (is the MAGNITUDE, again...)

X & Y positioning takes precendece on SWIRL that takes precendece on setting AZIMUTH (and MAGNITUDE) and on the mouse
* PANNING is LINEAR and becomes EQUAL POWER PANNING when the flag is activated.
* Activating the flag INFINITE DISTANCE CENTER, the center becomes an AUDIO BLACK HOLE - the audio disappear if the magnitude approximates to ZERO

---

## Clocks
### TIMEX

a CLOCK using the standard unix time functions and representing current HOUR (of your computer)

data represented and outputs:

* current HOUR + RAMP representing current HOUR in a day in 0-10v scale + PULSE when DAY changes
* current MINUTE + RAMP representing current MINUTE in a HOUR in 0-10v scale + PULSE when HOUR changes
* current SECOND + RAMP representing current SECOND in a MINUTE in 0-10v scale + PULSE when MINUTE changes
* current 1/10 of SECOND + RAMP representing current 1/10 in a SECOND in 0-10v scale + PULSE when SECOND changes
* current 1/100 of SECOND + RAMP representing current 1/100 in 1/10 in 0-10v scale + PULSE when 1/10 of SECOND changes

ALARMS (2):
- to set the alarm, click and drag on the display
- to ARM the ALARM, press the ON-OFF button
- when current time HITS the ALARM set, a PULSE is generated and a GATE activated, and the ALARM is set to OFF

COUNTERS (2):
* to set the counter, click and drag on the TARGET display
* to activate the counter, press the ON-OFF button
* to run the counter, connect a PULSE to the PULSE IN, if ON the counter will start to COUNT
* if the COUNTER is ON and COUNTER hits the TARGET a PULSE is GENERATE from PULSE OUT and the COUNT is set to 0

### CLOCK MULTIPLIER

CLK IN accept a clock (or a LFO )
* the GREEN LED indicates that the TIME computer is in a stable state

CLK OUTs
* the RED display is the time multiplier from 0.01 to 99.9999, and is a DRAGGABLE display for precise value inputs


---

## Quantizers
### SCALA QUANTIZER
Outputs a quantized voltage based on .SCL files ([Scala files](http://www.huygens-fokker.org/scala/))
* Select a scale using the contextual menu

new scales can be added using the contextual menu "ADD NEW SCL File..."
* the scales are stored in the "Rack/plugins/nysthi/res/microtuning/scala_scales/" directory. feel free to add and remove as needed

the GREEN DISPLAY shows:
* ROW 1: the octave and the degree in the octave: for example "3-7" means degree 7 of octave 3
* ROW 2: the octava and the original ratio or value in the original file
* ROW 3: current value in Hz (assuming C4 is 261.63 Hz)
* ROW 4: current quantized voltage being output

the OCTAVE DISPLAY DRAGGABLE let's you move the octave from -2 to +2 for the quantization

the TUNE DISPLAY DRAGGABLE let's you move from -.99 to +.99 the current voltage value

### QUAD SIMPLER SLICER QUANTIZER
4 quantizers, where 10v is divided from 1 to 99 slices, and IN VOLTAGE is quantized to the closest
* perfect to use with simpler: load a LOOP and set to 16 or 8 slices
* use an SOU as Voltage source!

### EQUAL DIVISION QUANTIZER
Inspired by [discussions with Kent, Edward and Scott](https://www.facebook.com/groups/vcvrack/permalink/171694843490668/)

It is a grid created using the formula  "Nth root of X" where N is the first field and X the second field
* You can use any REAL number, so you can have for example a scale  63.333ed1.6666  (63+1/3ed5/3)
*  both N and X fields are draggable editable

the midi map mode, maps the midi notes (scaled 0.083333) to first 127 degree of the current scale

the pure quantize mode, quantize to the closest voltage of the grid

TUNING and OCTAVE work the same as in Scala

examples:
* N = 12 and X = 2 is the standard western 12th root of 2 )equal tempered) scale
* N = 25 and X = 5 gives you the Stockhausen's 25ed5 scale
