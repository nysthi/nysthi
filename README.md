# NYSTHI modules for VCV Rack 

![](https://raw.githubusercontent.com/nysthi/nysthi/master/images/nysthiCurrentSet6.png)

# MVerb

Reverb

# HiVerb

Reverb with high frequency tail.

# TwistedMVerb

Reverb with cv control of Mix, Density, LP Freq, Decay, Damping, Gain, and Freeze

# Logic

Boolean logic operations.

* white sockets: inputs
* black sockets: outputs

# Model 277

signal delay unit

https://www.modulargrid.net/u/buchla-277-

# NYStereoPhaser

Phaser

# NYStereoChorus

Chorus

# DualSignalDelayer

Top half can delay one signal and the bottom half can delay the other.

# Surveillance

Attenuator with one input and 10 different attenuated outputs

# NYEnvFollower

Envelope Follower

# LFOMultiPhase

LFO with 8 different phase outputs of the signal.

* morphing is activate via "discrete - morph" switch
* morphing is modulable via CV input and controllable via waveshape selector and modulation index

# 2 Channel MasterRecorder

Record 2 channels of audio to one 2 channel wav file. (Stereo)

# 4/8 MultiTrack Recorder

Record 8 channels of audio to one 8 channel wav file.

# Dual VU Meter

The top half is one VU Meter and the bottom half is another VU Meter

# DelayAttackHoldDecay EG

Also called complex DAHD

An envelope with cv in for almost every parameter.  Also has Output triggers at the bottom for the various stages.

# AttackDecay EG

Simple Attack Decay Envelope with a trigger button.

# complexSimpler

* the LFO is morphable (the lights give you the idea)
* ANTI-CLICK param, filter to remove clicks in sample start and ends points
  * the ANTI CLICK goes from 0 to 100 ms
* if GATED on, the sample will stop when TRIG/GATE is off
* ability to open WAV or AIFF files (PCM)

# QuadSimpler

* the son of SIMPLER, is a multi sample player with integrated stereo mixer
* 4 equivalent sample player with
  * LOAD sample button (load WAV or AIFF, PCM)
  * GATE mode (when in GATE mode the sample will play when the signal is HIGH and STOP when TRIG is LOW)
  * 1-SHOT
  * TRIG BTN (to start a sample manually, or GATE IT)
  * TRIG IN (to start a sample with a trig in signal or used in GATE mode)
  * STOP IN (a trign signal will stop the sample)
  * START will move the start point of the sample
  * FM CTRL from -2 to +2, by default is 1 and the input in FMIN/CV will be 1V/oct
  * FMIN/CV (to modulate frequency)
  * SPEED setting the base SPEED of the sample
  * PAN to place the sample in the stereo field
  * VOL volume of the smaple
  * OUT the direct OUT of the sample player
  * all the paramenters are repeated 4 times

* GLOBAL parameters is CHAIN IN of another mixer that will be summed to Channel L and R
* the idea is to have multiple QuadSimpler to have a BIG bank of samples

# Dica33

* filter module...
* very instable, but usable

# HotTuna

* the VU meter will give info about the note, the big black one text is the
* frequency (expressed as MIDINOTE TAG) we are targeting;
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

# SQUONK

it's a PROGRAMMER, STAGE sequencer, Sampler TRIGGER, freely inspired to [Serge TKB](http://www.serge-fans.com/wiz_seq.htm)

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

# SoyModelSOU

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

# SOU UTILS
---- perfect companion for the SOYMODELSOU, to scale ad create arabesque
---- Is 3 parts of 2 repeated sections
------ SCALER OFFSETTER 1 & 2 (2 section equivalents)
-------- ACCEPT AUDIO or CV SIGNAL IN
-------- SCALE for -2 to +2 times, the CV accepts from 0 to 10V and is scaled to 0->1 multiplied SCALE value
-------- scale function = SCALE or (if plugged in a CV) (SCALE * CVIN * 0.1 * 0.5);
-------- OFFSET from -10v to +10v
-------- OFFSET CV accepts any value
-------- final OFFSET FORMULA = clamp(OFFSET + OFFSET CV , -10, +10)
-------- output AUDIO or CV

------ OCTAVE FOLDER 1 & 2 (2 section equivalents)
------ for any voltage coming in IN OVER MAX will be subtracted 1.0 till is reported UNDER MAX
------ for any voltage coming in IN UNDER MIN will be added 1.0 till is reported OVER MIN
------ IS perfect to use with Quantized RV section N^2 of the SoyMODELSOU, to reports the voltage into certain octaves
-------- ACCEPT a SIGNALCV type typically
-------- MIN is set from 0 to 9V
-------- MAX is set from 1 to 10V
-------- if MAX is equal or less than MIN, is set to MIN + 1
-------- OUTPUT the FOLDED SIGNALCV

------ ASR 1 & 2 (2 section equivalents)
-------- is a 4 cells ASR
-------- accept SIGNALCV or AUDIO IN
-------- EVERY PULSE advance the content of the cells


-- VECTOR MIXER
---- is a mixer working in a 2d plane. the "joystick" position could be set by MOUSE, by X & Y position
---- and by AZIMUTH & MAGNITUDE. X & Y has precedence on AZI & MAGN that has precedence on MOUSE.
---- INPUT could be SIGNAL AUDIO or CV. The vector mixer is highly inspired to joystick and
---- vector functions of the Prophet VS.
---- Combined with JW XYPAd can emulate the 2D Vector Envelope too

