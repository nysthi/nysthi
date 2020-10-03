#**v1.0.16 (2020-10-04)**  


## SIMPLICITER  
*	bug: crash caused by peak slice mode (issue #309)
*	add some new EDIT contextual menu 
	*	`UNDO (REDO) last (disruptive) edit`:  to be used to recover previous situation after doing an edit on samples
	*	 `Do Espen Storø trick (for no clicks in looping samples)`   
	for cut in the middle swith the 2 parts and xfade: the idea is to obtain non clicking drone loops but someone for sure is going to use in other creative ways
	* `Do mega random chopping and mix`  amusing command to `destroy the intelligibility` of any speech sample ! (magic!)
	* `Fade IN and OUT, LINEAR and EXP`
	
* add a new contextual menu `"Use START and STOP value smoothers"` because some people may prefer the old way when stopping (and starting) was not fading out (or fading in) but maintining the last DC ouput

## COMPLEX SIMPLER  
*	bug: was not saving the connected file if the file was drag&drop
*	bug: start was delayed becasue the anticlick was not inited
 
## QUADSIMPLER
*	bug: start was delayed becasue the anticlick was not inited

## CONFUSING SIMPLER
*	bug: start was delayed becasue the anticlick was not inited


## Heads-up on Anti-click (in various samplers)
the more is high the more delay is introduced



## **v1.0.15 (2020-09-22)**  

## SIMPLICITER  
*   setup a smoother for the start and stop (to avoid clicks, after introducing the "avoid DC signal if stopped"

## AMBUANCE  
*	bug: repaired unexpected result when signal was hard right panned (thanks Peter Vos)

## BZ-MAPPER
*  added dragging quantized (if press SHIFT key before dragging, nodes will be quantized in 0.5 volts steps)
*  remember that dragging with COMMAND/WINDOW key means "precise dragging"

## BZ-ENVELOPE
*	it's a simple Envelope with no sustain, brother of BZ-MAPPER  
* 	can use the expanders as the BZ-MAPPER (BZ-XPAND and BZ-XPANDXPAND)  
*  there are 2 to 6 nodes (and 1 to 5 Control Points)
*  nodes are persistent (when switching, module will remember previous settings)
*  from contextual menu it's possible to set 4 durations  
	*	from 0.001 to 0.100 seconds  
	*	from 0.100 to 1.000 seconds  
	*	from 1.000 to 10.00 seconds  
	*	from 10.00 to 60.00 seconds
* the knob "duration" will set the precise value between the min and max of the range
* the duration knob acts in exponential mode
* the BZ-ENVELOPE can be looped
* BZ-ENVELOPE is fully POLY
* the TRIG IN accepts from 1 to 16 channels
* the TAP TRIG let you activate on demand the ENVELOPE
* the EOC (End of Cycle) is a pulse emitted at the end of every cycle (in loop mode too)
* the ENV-OUT is the poly out and can output in 2 ranges
	* -5 to 5V range
	* 0 TO 10V range
* Voltage range is changed using the contextual menu on the Display (where the range is presented)
* the Zoom of vertical of the screen is set using the contextual menu on the left in the ZOOM area
* dragging is quantized if SHIFT key is pressed before dragging: nodes will be quantized in 0.5 volts steps
*  dragging with COMMAND/WINDOW key means "precise/slow dragging"



#**v1.0.14 (2020-09-15)**

# MUSICALBOX  
*	added drag playhead pressing ALT left (hard move of playhead with granular play)
* 	added drag playhead pressing ALT right (smooth move of playhead with granular play)
*  added drag playhead pressing SHIFT (scratch move of playhead, with pitch accelerations)
*    bug: was not respecting the -6 tp +6 OCTAVEs range

# MUSICALBOX2  
*    bug: was not respecting the -6 tp +6 OCTAVEs range

## SIMPLICITER
*	added drag playhead pressing ALT left (hard move of playhead with granular play)
* 	added drag playhead pressing ALT right (smooth move of playhead with granular play)
*  added drag playhead pressing SHIFT (scratch move of playhead, with pitch accelerations)
*  Fade In-Out smoothers, max 2000 samples, controlled by anticlick knob
*  Fade In can be ON or OFF, with linear or exp functions
*  Fade Out can be ON or OFF, with linear or exp functions
*	added XFADE between start and Reversed samples at the end, max 1 sec or 44100 samples
* XFADE can be ON or OFF, it's controlled by the anticlick knob
* removed the use of AUTOMATIC cache  
  *  loaded files are always load from their current position (if they still exist)
  *  if a recording or an append is done, saving the file will connect the sampler to the saved file
* increased range for OCTAVES, now from -6 to +6
  
## COMPLEX SIMPLER
* removed the use of AUTOMATIC cache  
  *  loaded files are always load from their current position (if they still exist)
  *  if a recording or an append is done, saving the file will connect the sampler to the saved file

## CONFUSING SIMPLER
* removed the use of AUTOMATIC cache  
  *  loaded files are always load from their current position (if they still exist)
  *  if a recording or an append is done, saving the file will connect the sampler to the saved file

## QUAD SIMPLER
* removed the use of AUTOMATIC cache  
  *  loaded files are always load from their current position (if they still exist)

## SUSSUDIO
*	added drag playhead pressing ALT left (hard move of playhead with granular play)
* 	added drag playhead pressing ALT right (smooth move of playhead with granular play)
*  added drag playhead pressing SHIFT LEFT (scratch move of playhead, with pitch accelerations)
*  added drag playhead pressing SHIFT RIGHT (scratch move of ALL the playheads, with pitch accelerations)
*  Fade In-Out smoothers, max 2000 samples, controlled by anticlick knob
*  Fade In can be ON or OFF, with linear or exp functions
*  Fade Out can be ON or OFF, with linear or exp functions
*	added XFADE between start and Reversed samples at the end, max 1 sec or 44100 samples
* XFADE can be ON or OFF, it's controlled by the anticlick knob

## QUADPANNER
*   added CV source mode (from contextual menu "uses 10V if no input")
*   feature request: added GATE output when touching the area: to be used as controller

## VECTORMIXER
*   moved lowpass output to context menu
*   feature request: added GATE output when touching the area: to be used as controller

## GRANTUNISMO + HOTTUNA
* 	feature request: added midi note + cents deviation  

## BZMAPPER
*  debug poly mode  

## SOYMODELSOU  
*  debug halt when changing sample rate  

## TZOP   
*  debug FINE tuning (now correctly doing -1 -> +1 semitone)

## TZEN
* debug the disappearing ADSR when a module was on the left  
  (now only a TZOP or µEN on the left, witha TZEN at their left can influence it)   

## ETCHASKETCHOSCOPE
*  feature request: add filter for "Max drawable vector length"
 
## SIMPLER TAPE CONTROL
*  form a Pyer Cllrd idea  
*  a tool that tries to imitate the use of Reel to Reel studio tape machine  using the SPEED input in the various Nysthi Sampler
*  it works as an expander directly in Simpliciter and Confusing Simpler but using the AUX out can be connected to any other sample like Complex Simpler, Sussudio, Musical Box, Musical Box 2
*  parameters and commands
*  TAP CONTROL to START and STOP the machine
*  TRIG IN to START and STOP the machine
*  GATE IN to START when HIGH annd STOP when LOW the machine
*  WOW control + INPUT (they work as SUM), visually is represented by an OFF-CENTER rotation
*  INERTIAL control + INPUT (they work as SUM). Tries to simulate the inertia of Reels
*    
*	machine controls:
* 		BACKWARD + TRIG in
* 	 	FORWARD + TRIG in
* 		Half speed BACKWARD + TRIG in
* 	 	Half speed FORWARD + TRIG in
* 		Double speed BACKWARD + TRIG in (via contextual menu, the speed will be 4x)
* 	 	Double speed FORWARD + TRIG in (via contextual menu, the speed will be 4x)
* 	  SELECT by CV (midi note from 0 to 5 of any octave, for example C3 will be "Double speed BACKWARD", C#3 --> BACKWARD, D3 --> Half speed BACKWARD, D#3 --> Half speed FORWARD, E3 --> FORWARD, F3 --> Double speed FORWARD)
* 	  NEXT will select next speed
* 	  PREV will select prev speed
* 	  RND will select a random speed between the 6
*		
*	 IN & OUTs:
*	 MOD IN : any voltage entering in will be added to the "AUX OUT"
*	 CLICK OUT: sound output for the clicking buttons like real tape machine
*	 HOLD OUT, it's the GATE of the current status of the TAPE machine, to sync with other MACHINEs
*	 AUX OUT is the total of all internal calculation to be applied to the speed pf the samplers

BEWARE that if you connect it directly to a SPEED in connection in a sampler, on that sampler SPEED must be set to ZERO and SPEED CV IN VCA (if present) must be set to MAX



## TZVU
*	module request
*  wonderful UI from Pyer Cllrd!
*  vu meter utils, imitating the EMS synthi VU METER (signal checker)  
	contains a sensibility control from 4 msecs to 1000 msecs
	can be switched to 0 to 10v or -5 to 5v range

## TZMX
*   an Operator Poly Mixer to be used to compose DX7 style algorithms



#**v1.0.13 (2020-06-10)**

## POLYRECORDER
## POLYRECORDER64
*	debug: discovered an undersized counter (overflowing with files bigger than 4gb on Win10)

## AMBUANCE
*	[feature request] add remove original signal from WET path, using contextual menu  

  
  
#**v1.0.12 (2020-06-02)**

## DX7 ENVELOPE
*   [BUG] Repair the POLY behaviour: correct initialization

*   emulation of the 4 rates 4 levels DX7 operator envelop
*   values are like in DX7 from 0 to 1
*   rates are from super SLOW to hyper FAST
*   levels are from 0 to MAX
*   added SCALE (from -1 to 1) and OFFSET (-10 to +10)
*   2 inner VCA to control Audio Stereo signals
*   TRIG (Attack Release) mode or GATED (level 1, level 2 level3SUSTAIN, level 4)
*   TRIG CHAIN to control more DXEnvelopes with same trig or gate signal
*   TRIG GATE button
*   LED to signal the trig or gate status
*   fully POLY based on the GATE input number of channels
*   fully poly for the 2 VCA 1 and 2 (32 vcas)
*   added INVERTED OUTPUT (-SIGNAL)

## DOPPLAB
*	[FEATURE REQ] add REVERSE mode

*	it's a doppler simulator
	*	click with right mouse-button to add point
	*	click on points to move them
	*	click on point with right button to remove it
        
    
	***PARAMETERS***
*	IN and OUT stereo mode
*	ZOOM to scale the grid from 0.25x to 4x
	*	every single square in the grid represent 10 meters
*	SOUND SOURCE SPEED is the base speed of the source moving on the path, is expressed in Km/h
*	SPEED CV accept Voltages from 0 to 10v, the out is limited by the attenuator and summed to SOUND SOURCE SPEED
*	START activates the sound source on the path resetting to the START position
*	STOP-CONT can STOP and CONTINUE the source moving on the path
*	RESET rest the source to the START position
*	LOOP if ON the source will loop on the path
*	REVERSE if ON th movement of the source is reversed on the path
*	PITCH SHIFT if OFF removes the pitch shift effect
*	BINAURAL if OFF considers the 2 delay lines representing the ears as equivalent
*	BINAURAL if ON intracranial delay is computed for evey position in space of the source
*	VOLUME ATTEN if OFF removes the effect of the volume attenuation due to the distance source-listener
*	SHOW INFO if ON shows informations about :
	*	complete path length
	*	instantaneous speed of the moving sound source
	*	traveled distance by the moving sound source
	*	distance of the source from the listener
	*	relative speed "moving sound source - listener"


## QUAD SIMPLER
## COMPLEX SIMPLER
## CONFUSING SIMPLER
## SIMPLICITER
*	[FEATURE REQ] add "Autoplay on LOAD" command from MENU
	* 	if ON (by default) the sampler will play, on LOAD
	*	if OFF a START command (or a trig) is needed


## TUNATHOR
*	[FEATURE REQ] add tuning ranges via contextual menu

##	SCALEOFFSET
*	[FEATURE REQ] let the offset go from -10 to +10
*	[FEATURE REQ] give one decimal more of resolution

## POLYRECORDER
## POLYRECORDER64
*	[FEATURE REQ] add export by separated tracks if WAV
*	exported can be mono or stereo
*	[FEATURE REQ] add grouping of exported separated tracks in a single directory

## AMBUANCE
*	it's a reverb based on GigaVerb
*  added stereo mode
*  you can edit presets in the ambuance.presets file

## µOP
*	remodulated some params
*	better shaping of feedback param
*  it's now POLY
*  it's an EXPANDER, you can build fast dx7style algorithms  
	when is carrier a PURPLE light is ON at the TOP-RIGHT  
	when is modulator a BLUE light is ON at the TOP-LEFT  
	
	when connected as expander, 
	the modulator receives CV voltage from the carrier  
	(the voltage can be overridden via DETACH in context menu, yellow light on)
	the modulator sends the output to LIN FM IN to the carrier 
	 
	 
## µEN µENVELOPE
*   fully polyphonic, for all ports  
*   polyphony depends on polyphonic GATE/TRIG in  
*   added 1sec 10secs 100secs time ranges  
  
    
## POLY ADSR - POLYATTACKDECAYSUSTAINRELEASE
*   fully polyphonic, for all ports  
*   polyphony depends on polyphonic GATE/TRIG in  
*   add EXPONENTIAL mode from contextual menu  
  
    
## TZOP
*	is the µOP big brother with all feature exposed
* 	it's a pure SINE VCO to be used for FM
*  full POLY 16 voices  

	PARAMETERS
	
	YELLOW DISPLAY: Set base frequency (can be reset using contextual menu)  
		same rules as in LFOMultiphase, you can write `120 bpm` for example  
	  
	CV-IN: poly CV in 1V/Octave  
	RATIO: the RATIO applied to the tuning system  
	DETACH: if used as expander/carrier, to detach the INCOMING TUNING  
	  
	OCT: set the Octave  
	SEMI: Semitone  
	FINE: +- 1 semitone  
	SYNC: input to reset the phase. The phase will be reset to the curret PHASE ctrl value  
	CLKIN: applying a clock it's possible to set a frequency using an external device  
	  
	PHASE: to set start phase  
	(via contextual menu it's possbile to add some  
	PRE-PHASE variation to the 16 voice to give more movement)  
	PHASE CV IN + PHASE CV VCA: to control phase using external CV   
	EXP FM IN + EXP FM IN VCA: to modulate pitch, exponential way  
	  
	MOD INDEX: modulation index base  
	MOD INDEX CV + VCA: to modulate the MOD INDEX  
	  
	LINEAR FM INPUTS (1 to 5): lin fm inputs... 5 because dx7 op have 5 IN...  
	
	FEEDBACK: feedback level; there are 2 types of feedback, switchable using contextual menu  
	FEEDBACK CV + VCA: to modulate the FEEDBACK  
	
	OUT CV + VCA + LEVEL: it's an output level controlled via CV + VCA  
	OUT: the OUTPUT   
	
*  it's an EXPANDER, you can build fast dx7 algorithms  
	when is carrier a PURPLE light is ON at the TOPRIGHT  
	when is modulator a BLUE light is ON at the TOPLEFT  
	
	when connected as expander, 
	the modulator receives CV voltage from the carrier  
	(the voltage can be overridden via DETACH in context menu, yellow light on)
	the modulator sends the output to LIN FM IN to the carrier 

	
## TZEN  
*  it's a standard ADSR, very similar to PolyADSR but AUTO chainable with TZOP, to make dx7 algorithms FAST
* with STEREO VCA  
  
  
  
**v1.0.11 (2020-03-08)**

# BZ-MAPPER
*       solve bug: was not loading correctly the NODES informations


**v1.0.10 (2020-03-07)**

# SIMPLICITER
*       added menu to set xfade time between REC and PLAY buffers (from 0 to 2 seconds max)

# CONFUSING SIMPLER
*       added menu to set xfade time between REC and PLAY buffers (from 0 to 2 seconds max)

# HOTTUNA
*       add "USE BEMOLLE" (USE ♭) mode. When ON, bemolle (♭) are presented instead of Diesis (#)

# GRAN TUNISMO
*       add "USE BEMOLLE" (USE ♭) mode. When ON, bemolle (♭) are presented instead of Diesis (#)

# POLYRECORDER
*       Added "CONSOLIDATE TRACKS after REC" mode.
        If active, during the postprocessing all the tracks with empty content will be removed

# POLYRECORDER64
*       Added "CONSOLIDATE TRACKS after REC" mode.
        If active, during the postprocessing all the tracks with empty content will be removed

# MUSICALBOX2
*       add the contextual menu to allow WAV files bigger than 2MB

# BZ-MAPPER
*       Bezier based function mapper module, POLY
        from 2 to 6 nodes, with memory
        nodes can be CV controlled using the expanders
        can be used as waveshaper for any type of signal (beware of aliasing at audio rate)
        if touch to the left with a LFOMultiphase or µOP becomes and oscillator

# BZ-XPAND
*       right EXPANDER for BZ-MAPPER, to control using CV all the Nodes and Control Points

# BZ-XPANDXPAND
*       right EXPANDER for BZ-XPAND, to add scale and offset for all the CV in

# ETCHASKETCHOSCOPE
*       add the R G B inputs, they accept from 0 to 10 volts and they are active only if all 3 are plugged
        (they are at the bottom left)


**v1.0.9 (2019-12-17)**

# SIMPLICITER
---- some graphic cleaning
---- the speed display will display negatives in red (over a dark gray)
---- debug a crash happening modifying slices number
---- added an highlight mode to the fields to understand better whne in KF mode and in SLICE mode
---- add smoothing when there is a transition between REC and PLAY

-- CONFUSING SIMPLER
---- add smoothing when there is a transition between REC and PLAY

-- MASTER RECORDER 2
---- added saving in MP3 format (stereo, VBR, bitrate from 160 to 320)
---- Added new autosave strategy (similar to VCV-Recorder)
---- removed autosave button
---- the start button will trig a choose file the first time OR
    if the AUTO ENUMERATE FROM CONTEXTUAL MENU IS OFF
---- If the AUTO ENUMERATE is ON, if you want to change name of the file you should use
    the "CHOOSE destination file..." contextual menu
---- changed strategy for saving whne closing the app

-- POLYRECORDER
---- Added new autosave strategy (similar to VCV-Recorder)
---- removed autosave button
---- the start button will trig a choose file the first time OR
    if the AUTO ENUMERATE FROM CONTEXTUAL MENU IS OFF
---- If the AUTO ENUMERATE is ON, if you want to change name of the file you should use
    the "CHOOSE destination file..." contextual menu
---- changed strategy for saving whne closing the app

-- POLYRECORDER64
---- Added new autosave strategy (similar to VCV-Recorder)
---- removed autosave button
---- the start button will trig a choose file the first time OR
    if the AUTO ENUMERATE FROM CONTEXTUAL MENU IS OFF
---- If the AUTO ENUMERATE is ON, if you want to change name of the file you should use
    the "CHOOSE destination file..." contextual menu
---- changed strategy for saving whne closing the app

-- QUADPANNER
---- inverted Y axis
---- corrected OFFSET for AZIMUTH (not clamping but rotating)
---- added labels... :D

-- MULTIVOLTIMETRO
---- RED tapper for the reset min/max

-- MUSICALBOX1
---- bug: persistence of BUSY MODE is now corrected

-- JIRA JIRA ECHO
---- add anticlick filter to the on-off head selectors
---- add bypass button and pulse input

-- HOTTUNA
---- add LOW FREQUENCIES MODE. In this mode the detector can dectect precisely
    between 8Hz (!!) and around 1100Hz

-- GRAN TUNISMO
---- add LOW FREQUENCIES MODE. In this mode the detector can dectect precisely
   between 8Hz (!!) and around 1100Hz

-- DUAL DUAL LPG
---- changed selector for filter (just a graphic thing): now is an (EASY) tapper

v1.0.8 (2019-11-10)

All compiled against 1.1.6 Rack version

-- POLYRECORDER64
---- added 32 bit float saving
---- added 32 bit float RAW PCM saving
---- vastly improved real time saving
---- the yellow led is active when any module is doing postprocessing

-- POLYRECORDER
---- added 32 bit float saving
---- added 32 bit float RAW PCM saving
---- vastly improved real time saving
---- the yellow led is active when any module is doing postprocessing

-- MASTER RECORDER 2
---- added 32 bit float saving
---- added 32 bit float RAW PCM saving
---- vastly improved real time saving

-- SEVENSEAS
---- debug missing PW when non multithreaded
---- add 1024 and 2048 processing blocks
---- add tightloop context menu. If set tries to imitate the version 1.0.5 sleeping time of the extra thread

-- POLYSEVENSEAS
---- add tightloop context menu. If set tries to imitate the version 1.0.5 sleeping time of the extra thread

-- CONVOLVZILLA
---- debug a CRASH happening pressing reset button
---- add tightloop context menu. If set tries to imitate the version 1.0.5 sleeping time of the extra thread

-- MUSICALBOX1
---- added a contextual menu for a new MODE: "NAME MORE VISIBLE". (to give more punch to the text visibility)

-- THE SQUONK
---- small visual defect (contextual menu for randomize "x5" items )


v1.0.7 (2019-11-07)

-- RXG100ChanB
---- multithread tuning

-- RXG100ChanA
---- multithread tuning

-- SMASHMASTER
---- multithread tuning

-- RODENT V2
---- multithread tuning

-- MAGISTER FUZZ
---- multithread tuning

-- CONVOLVZILLA
---- multithread tuning

-- S.A.M.
---- multithread tuning

-- SEVEN SEAS
---- multithread tuning

-- POLY SEVEN SEAS
---- multithread tuning

-- SUSSUDIO
---- multithread tuning
---- faster samples switch if in memory

-- MUSICALBOX
---- multithread tuning
---- faster samples switch if in memory

-- MUSICALBOX2
---- multithread tuning
---- faster samples switch if in memory

-- VECTORMIXER
---- bug: inverted Y output
---- add flag to use -5v to +5v ranges
---- changed play mode to have more "ENVELOPE" functionality:
        a new TRIG/PLAY/RUN will restart the animator

-- ETCHASKETCHOSCOPE
----- inverted the default mode to LOW power

-- POLY AttackDecay
---- bug solved: the DECAY was wrongly mapped (to the attack... ). Now is ok

-- SIMPLICITER
---- bug in slice selection when using CV, sometimes was a multiple of a slice. Corrected

-- JANNEKER TIMED
---- add GATE out
        it's up during a SCENE
        and the JANNEKER must be ACTIVE and NOT RECORDING
        the GATE goes down when the TRIGGER E-O-SCENE is UP (un msec)

-- INTERLEAVER
---- a new module to translate between poly stereo interleaved and dual poly LEFT and RIGHT POLY
---- can translate both directions (max POLY left and right are 8 channels, for obvious resons)

-- POLYRECORDER
---- debugging the 24 bits saving
---- new graphic
---- removed the TRIG outs
---- the START act as STOP too

-- POLYRECORDER64
---- 64 tracks recorder
---- new module to waste your hard disk space faster


v1.0.6 (2019-10-16)

-- VECTORMIXER
---- changed range to smoother from 0.5-0.999 to 0.25-0.999, default to 0.5
---- feature request: added contextual menu for behaviour of XY positions inputs when animator is running
    modes are,
        a) X-Y positions inputs if connected have always priority
        b) X-Y positions inputs if connected are summed to the animator if running
        c) Animator if running have priority on X-Y positions inputs
---- add polyphony to channel A B C D LEFT and RIGHT
    the polyphony in output is computerd using the channel in input with max polyphony
    the polyphony in output is assigned to
    OUT signal A
    OUT signal B
    OUT signal C
    OUT signal D
    OUT signal X
    OUT signal Y
    OUT MIXED SIGNAL LEFT
    OUT MIXED SIGNAL RIGHT
---- debug the KEYFRAMER now interpolates correctly between the last and first step, if in LOOP
    If not in loop the joysticks stops at the last KEYFRAME
    the full time of the animation is intended for a LOOPED KEYFRAME animation

---- reminder on the AUTORECORDER
    if you set AUTOREC KFs ON KEyframes will be automatically added during dragging, respecting
the NEXT KF time field: for example if you set to 0.10 means a keyframe every 100 msecs will be saved

---- Removed the automatic editing of current keyframe: was too confusing


-- 4MIX 8MIX 16MIX
---- debug mode: changed all smoothers now you can drag at any speed the faders and the PANs you won't hear anymore clicks! :)

-- SEVEN SEAS
---- add smoothers on value dragging (and on screen dragging) to avoid zippering noises

-- POLY SEVEN SEAS
---- add smoothers on value dragging (and on screen dragging) to avoid zippering noises

-- QUAD PANNER
---- add smoothers on value dragging (and on screen dragging) to avoid zippering noises

-- µSQ2
---- changed freq to 0.25->8 range (15 to 480 bpm)

-- µSQ1
---- changed freq to 0.25->8 range (15 to 480 bpm)
---- changed steps to 16th (before were quarter)

-- ETCHASKETCHOSCOPE
---- an XY scope visualizer
---- inputs and parameters
----- X IN, SCALE and OFFSET
----- Y IN, SCALE and OFFSET
----- Fade time
----- Beam focus
----- in the contextual menu
------- exchange green and blue beam
------- use less power (and less resolution
--------- show vectors
--------- show points
----- show axis
----- show grid


-- SCALEOFFSET
---- simple scaler, offsetter poly
---- SCALE from  -4x to +4x, with IN CV and VCA
---- OFFSET from -9.9 V to +9.9 V, with IN CV and VCA

-- SQUONK
---- add more filter on RANDOMIZE, via contextual menu
---- It's possible now to randomize OR not:
------ DIRECTION
------ x10 Multiplier
------ MODE


v1.0.5 (2019-09-18)

-- MUSICALBOX
---- bug the module was losing reference to files after second opening


v1.0.4 (2019-09-16)

-- LFOMULTIPHASE2
---- same as LFOMULTIPHASE but with a different subdivision in  0º, 60º, 120º, 180º, 240º, 300º phases
---- many old chorus effects from string machines (solina, logan string melody) have the same type of subdivision
 (0º, 120º, 240º)

-- THE CAGE
---- add full 16 voices POLYPHONY if using quantizer input/output
---- add ACTIVE/NONACTIVE button stage

-- PEPPER
---- feature request: inizialize will empty all the fields (not the Keyframes)
(keyframes could be deleted all using delete all)

-- SIMPLICITER
---- bug: speed knob remains red when using dual click as default:
moved to an always blue knob
---- bug: when modulating random was not respecting the "unipolar" "inverted" flags
---- add better selection handling by mouse: now it's possible to move start and end
    and both at the same time if COMMAND/WINDOWS Key is pressed

-- CONFUSING SIMPLER
---- bug: when modulating random was not respecting the "unipolar" "inverted" flags

-- VECTORMIXER
---- added smoother for mouse controls, from contextual menu is possible to set the smoothing of the action
    from 0.5 (FAST and CLICKY) to 0.999 (super super SLOW and SMOOOOOOOTH). Defaul is 0.9

-- NYECHOECOECO
---- used some new disk created by Tugrikyan (OTK) (community)

-- PHASOR HARMONIC VCO
---- add Hammond B3 harmonics mode

-- SUSSUDIO
---- new 6 heads sample player with KF animator for selection
---- uses DRAG and DROP for fast action
---- it contains a folder scanner to intercept all the playable files
---- the changes between samples are super fast (and coming from a separate thread)
---- the same for the computation of the visuals
---- controls for every single head are:
------ ACTIVE (TRIG and TAP) to activate deactivate the playhead
------ GATED (ON-OFF): if the start is used as GATE IN
------ CYCLED (ON-OFF): if the selection should repeat
------ PLAY-START (TRIG/GATE in and TAP): to (re)start the playhead
------ PAUSE-CONTINUE (TRIG in and TAP): to stop and continue from current position
------ START: CV IN and KNOB: to move the START of the selection
------ END: CV IN and KNOB: to move the end of the selection
------ SPEED: CV IN + VCA + SPEED KNOB. from -2 to +2x
------ OCT: octave knob
------ CV: 1v/oct voltage CV IN (to use selection cromatically)
------ EOC: End of Cycle pulse out
------ CV + VCA: to assign a dynamic action
------ VOL: single playhead volume
------ OUTPUT LEFT and RIGHT, single playhead out
-------- when connected, are escluded from GLOBAL mix
------ PAN: place the sound in the stereo field

-------------------------
---- global controls:
------ WAVE zoom vertical
------ ANTICLICK (filter to remove clicks at the start and the end)
------ GLOBAL SPEED: CV IN + VCA + SPEED knob: the settings are applied to all playheads
------ GLOBAL OUT: VOLUME + total LEFT + total RIGHT
-------------------------
---- SAMPLE SELECT AREA:
------ BY MIDI CV: the first seleted sample is C3 voltage 0 (C#3 will select the second sample, and so on)
------ PREV (TRIG and TAP) select PREV sample in the list
------ NEXT (TRIG and TAP) select NEXT sample in the list
-------------------------
---- KEYFRAMER:
------ it's the classic keyframer used in SIMPLICITER, in this case is
    storing informations for all 6 playheads

-- QUAD SIMPLER
---- feature request: add a command via contextual menu, named "Exclude Connected SAMPLES from MIX"
    to exclude single connected samples from the main mix

-- SAM
---- ADVICE: Jon (https://github.com/nysthi/nysthi/issues/239) adviced me and you
    that if the SAM module is very stressed can crash (or enter in the infinite spinning ball mode)
    beware of this anomality that I can't correct because seems related to some obscure part of
    the original ported code !

-- MUSICALBOX
---- new 8 multi sample sample player
---- uses DRAG and DROP for fast action
---- it contains a folder scanner to intercept all the playable files (x 8)
---- the changes between samples are super fast (and coming from a separate thread)
---- the same for the computation of the visuals
---- controls for every single head are:
------ ACTIVE (TRIG and TAP) to activate deactivate the playhead
------ GATED (ON-OFF): if the start is used as GATE IN
------ CYCLED (ON-OFF): if the selection should repeat
------ PLAY-START (TRIG/GATE in and TAP): to (re)start the playhead
------ PAUSE-CONTINUE (TRIG in and TAP): to stop and continue from current position
------ START: CV IN and KNOB: to move the START of the selection
------ END: CV IN and KNOB: to move the end of the selection
------ SPEED: CV IN + VCA + SPEED KNOB. from -2 to +2x
------ OCT: octave knob
------ CV: 1v/oct voltage CV IN (to use selection cromatically)
------ EOC: End of Cycle pulse out
------ CV + VCA: to assign a dynamic action
------ VOL: single playhead volume
------ OUTPUT LEFT and RIGHT, single playhead out
-------- when connected, are escluded from GLOBAL mix
------ PAN: place the sound in the stereo field
------ SAMPLE SELECT BY MIDI CV: the first seleted sample is C3 voltage 0 (C#3 will select the second sample, and so on)
------ SAMPLE SELECT PREV (TRIG and TAP) select PREV sample in the list
------ SAMPLE SELECT NEXT (TRIG and TAP) select NEXT sample in the list

---- global controls:
------ WAVE zoom vertical
------ ANTICLICK (filter to remove clicks at the start and the end)
------ GLOBAL SPEED: CV IN + VCA + SPEED knob: the settings are applied to all playheads
------ GLOBAL OUT: VOLUME + total LEFT + total RIGHT


-- MUSICALBOX2
---- new 16 multi sample sample player
---- all samples are coming form the same directory
---- uses DRAG and DROP for fast action
---- it contains a folder scanner to intercept all the playable files (x 16)
---- the changes between samples are super fast
---- the same for the computation of the visuals
---- controls for every single head are:
------ ACTIVE (TRIG and TAP) to activate deactivate the playhead
------ GATED (ON-OFF): if the start is used as GATE IN
------ CYCLED (ON-OFF): if the selection should repeat
------ PLAY-START (TRIG/GATE in and TAP): to (re)start the playhead
------ PAUSE-CONTINUE (TRIG in and TAP): to stop and continue from current position
------ START: CV IN and KNOB: to move the START of the selection
------ END: CV IN and KNOB: to move the end of the selection
------ SPEED: CV IN + VCA + SPEED KNOB. from -2 to +2x
------ OCT: octave knob
------ CV: 1v/oct voltage CV IN (to use selection cromatically)
------ EOC: End of Cycle pulse out
------ CV + VCA: to assign a dynamic action
------ VOL: single playhead volume
------ OUTPUT LEFT and RIGHT, single playhead out
-------- when connected, are escluded from GLOBAL mix
------ PAN: place the sound in the stereo field
------ SAMPLE SELECT BY MIDI CV: the first seleted sample is C3 voltage 0 (C#3 will select the second sample, and so on)
------ SAMPLE SELECT PREV (TRIG and TAP) select PREV sample in the list
------ SAMPLE SELECT NEXT (TRIG and TAP) select NEXT sample in the list

---- global controls:
------ WAVE zoom vertical
------ ANTICLICK (filter to remove clicks at the start and the end)
------ GLOBAL SPEED: CV IN + VCA + SPEED knob: the settings are applied to all playheads
------ GLOBAL OUT: VOLUME + total LEFT + total RIGHT

-- 4HANDS
---- bug in the portamento when value are bigger than 0.92, rescaled
---- added a new scale mode for portamento, giving more time between 0.00 and 0.30 values
    by default now the new scale mode is active;
    there is a contextual menu to access the old scale mode

-- GATETRIGMERGER
---- it's a simple utility to merge TRIGs or GATEs
---- it't composed by 4 time the same function it's an OR for all channels
    (sometimes you want to combine many trigs coming from a singles steps of a sequencer)

-- POLY LPG
---- new style courtesy of PYER


v1.0.3 (2019-07-15)

-- bug of the shifting ports in the mixers


v1.0.2 (2019-07-14)

# **THE CAGE**

## MULTI FUNCTION DEVICE

It is a SQUONK cousin

they share the same number of lines and the GATE, PULSE and BRIDGE Lines

It is essentially a Quantizer with FREE settings of the comparators' voltages

it's a 12 stages (and 13 voltages comparators)


when a STAGE is selected, if nothing is plugged in the QUANTIZER INPUT
these events are going to happen:

*    the STAGE BRIDGE is closed (and data can travese the BRIDGE
*    a GATE is ON for that stage
*    a PULSE is emitted for that stage (1 msec)
*    the Switch One to MANY is outputting from the Bridge OUT from that stage
*   (if the BRIDGE IN is unconnected)
*   the Switch Many to ONE is outputting the current BRIDGE IN to the SWITCH GLOBAL OUT
*   the current selected voltage is presented to the QUANTIZED OUTPUT
*   the GLOBAL GATE is set to HIGH

A stage can be selected with:

*        a) using TAP on the stage
*        b) a pulse coming in for that stage
*       c) if a CV select is connected, the CV is quantized as MIDI note and wrapped
*   selecting the corrispondent STAGE
*       d) if a TRIG/CLOCK is coming in the advancer/sequencer
*       e) if a TAP is done on the advancer/sequencer

if the stage is selected using the TRIG/CLOCK, the LAST STAGE line is valid

*    the last stage is selected TAPPING on the desired LAST STAGE
*     the function advancer/sequencer, can have 3  modes: FORWARD, BACKWARD, RANDOM


the function advancer/sequencer can be synced with RESET to other sequencers

if a cable is connected to the QUANTIZER INPUT THE CAGE works in quantizer mode

*    can quantize both CV and AUDIO signal
*    a quantized signal, activates (or not, depends on wrapping mode) a STAGE
*    if NOT WRAPPED the quantizer works only in the range between the FIRST and LAST VOLTAGE COMPARATOR

if WRAPPED is doing full quantazing with OCTAVE wrapping


-- PEPPER
---- a TEXT compation for JOOPER, to take notes about the execution
---- complete with scene manager
---- of course can be used for many other "textual" jobs


-- 4MIX 8MIX 16MIX
---- ADD full POLY from channel 1 for VOLUME, PAN, SOLO and MUTE
---- added POLY OUT from POST OUT channel 1
    to minimize the cabling when doing submixing with send and returns;
    the number of POLYphony is via contextual menu
    (max 4 ,8 or 16, depends on the mixer)
---- BUG: the contextual menu attenuator were disabled if a mono signal was attached to the inputs...


-- JOOPER
---- feature request: ADD context menu to activate/deactivate AUTOLOAD mode for PREV-NEXT scene
---- feature request: if you press reset and you are in MULTIPLEXER mode all the IN and all the OUT will be DEACTIVATED
---- feature request: the CV select is now MIDI related; SCENE 1 will be selected with MIDI NOTE C3 (-1Volts)
    and C#3 will select SCENE 2 (-0.916Volts) and so on.
    Of course the max selectable scene is the 127 - 36 = 91 scenes
    The old style SELECT mode is reactivable using CONTEXTUAL MENU


-- HOTTUNA
---- added LOW power mode in automatic


-- GRAN TUNISMO
---- added LOW power mode in automatic


-- TUNATHOR
---- added LOW power mode in automatic


-- PITCH2VOLTAGE
---- changed detector (testing a faster detector)


-- UNNYSTHIPLEASURESGRAPHER
---- bug in the new v1 because of the zoom levels, solved
---- new visualization mode (more centered and JD)


-- SIMPLICITER
---- bug "playback restart after pause is not deterministic SOLVED"
---- bug "Simpliciter does not restore last slice automatically in certain conditions SOLVED"
---- bug: respect the LOADED audio file sampling rate
---- bug: correct draggin on samples if in TRIMMED mode
---- bug: correct timing of slices created in TRIMMED mode
---- bug: can open now VCVRecorder WAV files
---- bug: after recording, reapply the current speed to the new recorded snippets
---- feature request: implemented multiple load via DRAG and DROP
    you can drop a folder and all the Audio file will be imported/appended
    you can drop a bunch of file audio and all the Audio file will be imported/appended
    if you use the WINDOW KEY (CMD on MAC) during the DRAG and DROP, ALL will be APPENDED
---- feature request: the CV select for the SLICE SEQUENCER is now MIDI related;
    SLICE 1 will be selected with MIDI NOTE C3 (-1Volts)
    and C#3 will select SLICE 2 (-0.916Volts) and so on. of course the max selectable slice is 127 - 36 = 91 slices
    The old style SELECT mode is reactivable using CONTEXTUAL MENU
---- ADD START and LENGHT mode for selections
---- ADD RECORD with prefixed time of recording (to capture live events)
    must be activated via MAIN contextual menu, and from the contextual menu
    is possible to set from 0.5 to 120 seconds max


-- COMPLEX SIMPLER
---- bug: respect the LOADED audio file sampling rate
---- bug: can open now VCVRecorder WAV files


-- CONFUSING SIMPLER
---- bug: respect the LOADED audio file sampling rate
---- bug: can open now VCVRecorder WAV files


-- QUAD SIMPLER
---- bug: respect the LOADED audio file sampling rate
---- bug: can open now VCVRecorder WAV files


-- LFO MULTIPHASE
---- feature request: added -10v to +10v BIPOLAR mode (activable via contextual menu)


-- JANNEKER
---- bug: DELETE with BACKSPACE and DELETE key, now working


-- µSQ2
---- bug: DELETE with BACKSPACE and DELETE key, now working


-- µOP
---- bug: OCTAVE is back in the range fromn -8 to +8 octave


- AD (AttackDecay) + complexDAHD + POLY AttackDecay + POLY DelayAttackHoldDecay
---- bug: when decay was at MAX (1) the module was not correctly reinited at reload time


-- MULTIVOLTIMETRO
---- add MIN MAX detector mode
---- add reset PEAK - MIN - MAX via PULSE IN or TAP


-- POLY DelayAttackHoldDecay
---- bug, missing EOA EOD EOH EOC pulses if the input was not POLY



v1.0.1 (2019-06-23)

-- SEVEN SEAS
---- solved a bug: default bank was not mantained if moved from a computer to another

-- POLY SEVEN SEAS
---- solved a bug: default bank was not mantained if moved from a computer to another
---- added SWARMING
---- added POLY stereo OUT

-- complexSIMPLER + confusingSIMPLER + quadSimpler
---- add a BUSY mode activable using contextual menu.
    when BUSY a TRIG to start will be accepted ONLY if not playing
    (that means that if the AUDIO is LOOPED will be never accepted till is STOPPED by TRIG or TAP)

-- 4MIX 8MIX 16MIX
---- added POLY mode for channel 1 LEFT: useful for spreding voices in stereo field
---- added POLY via Channel 1 LEFT or RIGHT, the MIXING is STEREO POLY if both source on CHAN 1 LEFT and CHAN 2 LEFT are POLY

-- FIXED VOLTAGE SOURCE
---- added selectable POLY mode via contextual menu (the POLY is always via channel 1)
---- gate now respect the POLY mode (always in channel 1)




v1.0.0 (2019-06-19)

finally full port of everything

-- ALL MODULES
---- all the pulse out are 1 msec long

-- ALL ENVELOPES (AD DAHD ADSR and multiples)
---- debugged a wrong behaviour in the SCALE param when negative and back positive

-- SQUONK
---- feature request: added CV + VCA to control ROTATION of the ENDPOINT
---- add GATE line: the gate will be up to 10v when the stage is selected
---- add BRIDGE IN/OUT, when the STAGE is selected, the BRIDGE is connected
---- add OVERRIDE A Channel (OVER A) when the STAGE is selected,
    if the current OVER A is connected, will substitute the output of A channel

-- MASTER RECORDER 1, MONORECORDER, MASTER RECORDER 2, MULTITRACK RECORDER
---- feature request: added input attenuation via context menu (0dB, - 6dB, -12dB, -24dB)
---- feature request: if the name of the patch exists, prepend it to the autosaving files
    or to the proposed filenames

-- 4HANDS
---- feature request: added dragging displays with WIN-KEY modifier (CMD-KEY for MAC)
    when dragging on value display with the modifier, the dragging will set the value for all the values in the same category
    for example, if you drag on one of the "PORTAMENTO" value with the modifier and the value is set to 0.80
    all 10 PORTAMENTOs will be set to 0.80 (in real time).
    Same applies for the 10 VOLTAGE A and for the 10 VOLTAGE B values

-- TUNATHOR
---- debug: solved the semitone mode that was never finishing the calibration
---- debug: solved the problem of the ADDED +3V when was in MAP mode (@Steve...)
---- feature request: maintain and save last mapping, to be reused and reused
    (works also if you save the preset!)

-- 4MIX 8MIX 16MIX
---- feature request: added global input (valid for every channel) attenuation via context menu (0dB, - 6dB, -12dB, -24dB)
---- feature request: added MASTER limiter via context menu, with NO LIMITS, HARD LIMIT +0dB, +3dB, +6dB, and SOFT LIMIT at +0dB and +3dB
---- bug: corrected the right click behaviour on channels

-- CONVOLVZILLA
---- added a DEFAULT ON DC block filter on the output: the filter can be set OFF using contextual menu
---- solved a crash when changing block size

-- FIXED VOLTAGE SOURCE
---- added, GATE control
    if gate is connected, and the input [is high | receives >=10V], the output becomes active, otherwise 0.0V
    if gate is not connected, the output is always active.
---- added GLOBAL sum VOLTAGE
    is always the sum of al valid voltages (gated or not gated)
---- the GLOBAL is controlled by a GLOBAL GATE
---- added context menu for prefilling,
    with semitones sequence,
    voltages from -6
    voltages from 0
    doubling voltages from 0.0625
    doubling voltages from 1
    some math constants: π, 2π, e, √2, 1/√2, φ
---- added POLY mode output to channel 1 (all 16 channels are exported in a poly cable)

-- COMPLEXSIMPLER
---- add a contextual menu to activate NEGATIVE CV for NEGATIVE frequencies

-- metaAARDVARK
---- feature request: add SYNC/RESET activable via TAP or SYNC PULSE IN.
    An OUT is provided to make sync chains

-- QUAD SIMPLER SLICER QUANTIZER
---- bug solved: now considering also last step; example
     if you have 10v in 2 slices, before was considering only 0.0V and 5.0V, missing the
     final step 10v
---- bug solved: the value choosen is the closest one, not the lowest one; till this version
     if you had a 10v sliced in 2 (0, 5, 10), if an incoinng value was 3.33, the slicer quantizer
    would choose 0v as resul. With this version teh 5v will be choosen (the closest to the grid)
---- feature request: is possible using the contextual menu to slice not only 10volts, but also
    1, 2, 3, 4, 5, 6, 7, 8, 9 volts

-- SEVEN SEAS
---- added a default GLOBAL bank automatically loaded when a NEW Seven Seas is created
    default bank lives in `nysthi/res/sevenseas/sevenseas_default.wav`
    so everyone can change it and create a new default
---- removed the "removing clipping ends when importing arbitrary source files" mod: was buggy

-- POLYRECORDER
---- a new recorder able to record from 1 to 16 channels WAV files using the POLY port

-- POLY SEVEN SEAS
---- added 16 voices polyphony, currently NO SWARM in POLY mode

-- GRAPHIC METER
---- added POLY mode input to channel 1 (all 16 channels are imported in a poly cable)
    the poly mode can be overridden using single channels entry
---- added POLY mode output to channel 1 (all 16 channels are exported in a poly cable)

-- MULTIVOLTIMETRO
---- added POLY mode input to channel 1 (all 16 channels are imported in a poly cable)
the poly mode can be overridden using single channels entry
---- added POLY mode output to channel 1 (all 16 channels are exported in a poly cable)

-- POLY SEVEN SEAS
---- polyphonic seven seas, 16 voices available

-- POLY AttackDecay
---- a copy of the AttackDecay but POLY
---- added POLY mode via TRIG input and ENV OUT
---- All CV in are poly aware

-- POLY DelayAttackHoldDecay
---- a copy of the DelayAttackHoldDecay but POLY
---- added POLY mode via TRIG input and ENV OUT
---- added POLY mode via VCA IN and OUT (for the 2 VCA)
---- All CV in are poly aware

-- POLY ADSR
---- a new fresh ADSR, Polyphonic
---- parameters:
---- A "Attack" from 0 to 1, default 0, cv controllable (time are from 0 to 1 sec, to 10 sec, to 100 secs use context menu)
---- D "Decay" from 0 to 1, default 0.1, cv controllable (time are from 0 to 1 sec, to 10 sec, to 100 secs use context menu)
---- S "Sustain" from 0 to 1, default 0.5, cv controllable (where 1 is the max level)
---- R "Release" from 0 to 1, default 0.5, cv controllable (time are from 0 to 1 sec, to 10 sec, to 100 secs use context menu)
---- LIN-EXP from 0 to 1, default 0.5, cv controllable (0 is very linear to 1 very exponential)
---- SCALE from -2 to +2, default 1, cv controllable (scale of the output with inversion and auto offset)
---- ZERO, ON-OFF, defaut OFF. if ON, any new gate will restart the ADSR from 0, if OFF a RE-GATE will restart from current value
---- BUSY, ON-OFF, defaut OFF. if ON, any new gate will be acceptend only if ADSR is stable in IDLE mode
---- GATE, Polyphonic GATE, with TAP, GATE-IN, and GATE-OUT copy (to make chains)
---- VCA1, Polyphonic VCA, with VCA-IN, atenuverter, from -2 to +2, default 1.0, and VCA-OUT
---- VCA2, Polyphonic VCA, with VCA-IN, atenuverter, from -2 to +2, default 1.0, and VCA-OUT
---- ENVELOPE CHAIN IN - OUT, ENVELOPE-CV-IN will be summed to the ENVELOPE OUT, first OUT, is the INVERTED OUT (or -ENVELOPE SIGNAL)
    second OUT is ENVELOPE OUT (+ light)
---- End OF Attack EOA, End OF Decay EOD, End OF Sustain EOS, End OF Release (EOR or EOC...) are POLYPHONIC pulses out representing the end
    of particular stage. Can be used to make intricate sync combinations

-- SCALA QUANTIZER
---- the main input is POLYPHONIC (and so the main output). 16 channels

-- EQUAL DIVISION QUANTIZER
---- the main input is POLYPHONIC (and so the main output). 16 channels

-- DX7 ENVELOPE
---- fully POLY based on the GATE input number of channels
---- fully poly for the 2 VCA 1 and 2 (32vcas)
---- added INVERTED OUTPUT (-SIGNAL)

-- MICROTONAL HOST HELPER
---- the module comes from an Andrew Belt idea under Warren Burt proposal (https://www.facebook.com/groups/vcvrack/permalink/344906862836131/)
---- as the VST host is using always quantized voltages with this module we try to send microtonal
    differentials using the pitch bend.
    We send microtonal differentials for +-12 semitones and for +- 1 semitone pitch bend
---- INPUT and OUPUTS
---- QUANTIZED INPUT: the voltage coming from a quantizer, like SCALA, EDO, SCALAR (anything)
---- QUANTIZED 1/12v OUTPUT: the quantized in the standard grid of 0.083 volts per semitone, to be sent as CV to the VST HOST
---- PITCH BEND +- 12 SEMITONES, to assign as PB to the VST HOST if the PB is set to +- 12 semitones
---- PITCH BEND +- 1 SEMITONE, to assign as PB to the VST HOST if the PB is set to +- 1 semitone

-- POLY LPG
---- it's just one of the b208 dual dual LPG expanded and used in polyphonic mode
---- the CV IN is polyphonic too

-- JIRA JIRA ECHO
---- feature request: added a GATE simulating a finger on disk

-- NYECHOECOECO
---- feature request: added a GATE simulating a finger on disk

-- SIMPLICITER
---- direct son of confusing Simpler,
    Pyer Cllrd was moved by compassion and threw me his ideas, about it, in SVG form
    (he is the author of the design and all SVGs)
---- added all the PEAK functions.

-- CONST ADD MULT
---- POLY mode added (the TRIG is always MONO)

-- SOU UTILS
---- POLYPHONIC for SCALER, OFFSETTER, OCTAVE FOLDER, ASR 1 and ASR2
---- removed USELESS OVERFLOW in ASR1 and ASR2
---- currently if nothing is plugged in ASR 2 INPUT ASR1 and ASR2 are united in a unique ASR 8 steps


v0.6.42 (2019-02-25)

-- GRAPHIC METER

---- add pass thru outputs to insert it in a chain


-- MULTIVOLTIMETRO

---- add pass thru outputs to insert it in a chain


-- JIRA JIRA ECHO

---- exposed the inner LowPass filter: cutoff freq goes from 500Hz to 8kHz (added IN CV too)
---- boosted volume for summed nodes
---- add an all gray disk for people don't want running disks (check in
    YOURRACKINSTALL/plugins/nysthi/res/shapes/ and substitute the JIRAJIRADISK.svg)


-- EQUAL DIVISION QUANTIZER

---- change the input field, from DRAG displays to EDIT, WRITE and SET displays
---- now 0 VOLTS-IN  will always correspond to a 0.0 VOLTS-OUT (added an auto offset when changing scale)
---- removed a possible crash cause (a connected input at 0 volts can crash it on restart)
---- add correct refresh of the panel and internal if the scale is changed on the fly


-- CLOCK MULTIPLIER

---- solved a case of a non-initialized timer


v0.6.41 (2019-02-18)


-- JIRA JIRA ECHO

----is the 0.6.40 NYECHOECOECO version...
(
    ---- add full stereo support
    ---- add ON/OFF buttons for single HEADS repetitions (for the feedback repeat/swell function)
    ---- Decouple repeats and simple echo: (you can have a simple echo repetition and no swell/feedback)
    ---- the TAP-IN inputs are now correctly feedback in swell mode
    ---- added BIAS to simulate hysteresis of magnetic disc, when erase is OFF
        (the more high current bias the more is recorded on top of old recorded data)
}


-- NYECHOECOECO

--- is back to the previous functionalities (for people having it in patches)



v0.6.40 (2019-02-17)


-- NYECHOECOECO

---- add full stereo support
---- add ON/OFF buttons for single HEADS repetitions (for the feedback repeat/swell function)
---- Decouple repeats and simple echo: (you can have a simple echo repetition and no swell/feedback)
---- the TAP-IN inputs are now correctly feedback in swell mode
---- added BIAS to simulate hysteresis of magnetic disc, when erase is OFF
(the more high current bias the more is recorded on top of old recorded data)


-- CLOCK MULTIPLIER

---- add RESET trig input
---- add ACTIVE trig input + TAP: if not ACTIVE no CLOCKs are generated
---- add new mode via context menu: if TRIG IN is unconnected, TRIG OUTs can be muted


-- QUAD PANNER

---- inverted the Y input to be used correctly with Vector Mixer in "joystick or envelope mode"


-- EQUAL DIVISION QUANTIZER

---- add new style of quantizer grid (user can still use previous grid switching it with contextual menu)
---- solved a bug when the quantizer was switching to "non in GRID voltages" (thanks JIM!)


-- BIVIO

---- add CHAIN OUT TRIG (to reuse the TRIG IN and easily chain it to the other TRIG or INPUTS)
---- add "routing probability mode" the probability  (using context menu)
in this new mode for the probability to go to A or to B
the starting position is not important
if the probability is at 5%, 19 times out of 20 will switch to A, always
---- the standard mode remain "switching probability mode"
is the probability to move from the current position
so the history is important,
for example if you are on B
and probability is at 5% means the only 1 times out of 20 (on average) the bivio switches to A
(and viceversa)


-- ELSKER

---- Added one shot mode: if active, the GLOBAL TRIG in will be valid only one time
and after the use the RESET button must be used to RESET the ONE SHOT mode
---- Added clock timing: the time of the clock in input is computed and used as timebase
for the GATE and DELAY operations.
If ELSKER is timed, the field represents multiple of the base time
there is: a CLOCK input, a display showing the frequency of the clock and
a display showing the time differential between pulses of the clock
---- Added Randomization to durations and delays: random is function of the current value in the field
for example if the field contains 0.123 seconds, the random can generate a new value that in the
200% range of the current value (in this case from 0.001 to 0.246.
if the delay is 0.000 the range will be considered 0.010
---- Added GLOBAL RESET TAP-TRIG. When hitting it every programmed gate will immediately stop
---- MIN time for delay is 0.000 so now can be also instantaneous on TRIG


-- LOGIC

---- added contextual menu to switch VOLTAGE levels between 5v and 10v
becomes perfect to do all thing related to GATES :D



v0.6.39 (2019-01-26)


-- ELSKER (the MULTITRIGDELAYER)

---- it's a 12 trig/gate delay
---- with a common global TRIG, or single TRIG
---- parameters
---- GLOBAL TRIG/TAP to activate all the ACTIVE delayers at the same time
---- single delayer
---- TRIG/TAP to start the delay
---- ACTIVATE TAP/TRIG to ACTIVATE/DEACTIVATE the delayer
---- DELAY draggable display: from 1 msec to 999 seconds: time to wait
---- DURATION draggable display: from 1 msec to 999 seconds: length of delayed gate
	(gate ON is 10 Volts)
---- GATE out is the GATE trig out the yellow LED will indicate current VOLTAGE status


-- EXPIRED TIME

---- IT's a BIG screen ELAPSED time TIMER, to check the monitor far away
---- timer counts: Hours, minutes, seconds and msecs
---- parameters
---- START-CONTINUE TRIG/TAP, the TRIG/TAP is output also as PULSE OUT to sync more devices
---- RESET TRIG/TAP, the TRIG/TAP is output also as PULSE OUT to sync more devices
	will reset the timer to 0
---- ALARMs section:
---- there are 3 alarms with Settable Hours Min and Sec. The ALARM will output a PULSE out when the timer HIT that TIME


-- P2V

---- an attempt for a more dedicated Pitch to Voltage module
---- (the same used in HotTuna, but tuned more for Real Time action)
---- the voltage detected is transformed with base C4 (261.63HZ) --> 0.0 Volts
---- parameters
---- Signal IN (the signal to processed) SIGNAL OUT (to chain out the processed signal)
---- Voltage out section:
---- VOLTAGE OCTAVE OFFSET, from -4 to +4 octaves
---- VOLTAGE SEMITONE OFFSET, from -11 to +11 semitones
---- VOLTAGE FINE OFFSET, a single semitone movement
---- VOLTAGE SMOOTHING to smooth the voltage out
---- VOLTAGE OUT, the detected VOLTAGE


-- GRAN TUNISMO

---- having had requests for a big display tuner
---- it's like HOTTUNA, but with less features, more precise
---- big screen for people needing to work far from screen
---- red glowing means wrong detections


-- BIGNUMBER

---- feature request: added a contextual menu "PULSE IN DECREMENT MODE"  (on - off)
---- now can go in DECREMENT mode


-- HOT TUNA

---- added a "bobin" filter to the needle (more smooth)


-- BIVIO

---- feature request
---- added a contextual menu to choose if the UNSELECTED output (for BIVIO1 and BIVIO2)
    should output LAST VOLTAGE (kind of sample & hold), or 0 VOLTAGE


-- TIMEX

---- improved PULSEs: They are now on the edge
---- PULSEs for 10thOSec, sec, min, hour and day, will happen exactly when the counter reset


-- MONORECORDER, MASTER RECORDER 2, MULTITRACK RECORDER

---- feature request
---- added the concept of chosen ARMED file
---- using the contextual menu is possible to choose a POTENTIAL destination file that
    will be used next recording time.
---- the ARMED file is valid ONLY for one recording
---- beware that the AUTOSAVE win always... (if active)



v0.6.38 (2019-01-19)

-- DUAL DUAL LPG

---- this is the continue of the 208 wanna be serie
---- the code is all based on the
---- http://research.spa.aalto.fi/publications/papers/dafx13-lpg/DAFx2013-LPG.pdf
---- thanks to Julian Parker and Stefano D’Angelo !
---- I have done classic optimizations to minimize operations
---- I've added also 3 Vactrol response models (actionable using contextual menu)
---- the 3 response are always a little variations, every new instance will be little bit different
---- it's 2 times the section you have in the 208
----
---- PARAMETERS (for a single LPG)
---- red knobs selector for only VCA mode, VCA + LP mode, only LP mode
---- if in "only LP mode" there is the RESO knob that act on the signal
---- for a real 208, the RESO should be full CCW (but I like to use it!)
---- IN for the signal to be filtered (will come from complex VCO)
---- OUT for the filtered signal to be sent to other modules
---- the slider to the LEFT is the VCA for the incoming CV coming in from the BLACK socket
---- the black socket is just under
---- the slider on the right is the base level of action on the LPG


-- TUNATHOR

---- a tool to map voltages for shaky voltages situations
---- is composed of 2 parts the CALIBRATOR and MAPPED QUANTIZER
---- is better to use VCO in Sinusoid mode or Triangular mode
---- supported frequencies are from 30Hz to 5000Hz
---- the CALIBRATOR hear the incoming signal of the TARGET VCO and try to detect the frequency
---- when pressing START CALIBRATION button is trying to map voltages to
traversing from C1 to C7 octaves
---- using contextual menu it's possible to set up mapping mode to OCTAVE or SEMITONE
    (depends on the requested precision)

---- parameters and commands:
----
---- CALIBRATOR SECTION
---- CALIBRATION VOLTAGE OUT to be connected to the CV IN of the target VCO
---- TARGET FREQ: when in CALIBRATION ACTIVE MODE presets the current target frequency
---- CALIBRATION SIGNAL IN: the input for the target VCO frequency detection
---- DETECTED FREQ: is the display for the detected frequency
---- DEVIATION: when in CALIBRATION ACTIVE MODE displays the deviation from the searched frequency
---- START CALIBRATION: is the button to start the CALIBRATION procedure
----
---- MAPPED PLAY MODE section
---- MAP IS AVAILABLE light, will be ON if a MAP is available in memory
---- IN VOLTAGE: incoming voltage to be mapped
---- OUT VOLTAGE: mapped voltage to be used with CV in of the target VCO


-- FIXED VOLTAGE SOURCE
---- 16 Fixed voltage source, text editable

-- MULTIVOLTIMETRO
---- 16 High precision voltmeters, 99999 counts
---- can work also as PEAK detector using the contextual menu

-- GRAPHIC METER
---- 16 METERS to visualize voltages
---- the contextual menu lets you set 1 volt, 10 volts, or 100 volts scale
---- via contextual menu it's possible to set unipolar mode (only positive values are considered)
---- via contextual menu it's possible to set abs mode (negative incoming values are multiplied by -1)

-- µSEQ2 (microSequencer2)
---- corrected some defaults when right clicking on fields
    defaults with right clicks are

    NOTE : C2
    CV2: 1.00
    GATE: 25%
    LENGHT:  1/16

-- BIGNUMBER
---- feature request: add RESET to the nex clock IN (uses the contextual menu)
---- the display will present the status

-- DUAL (208) ENVELOPE
---- solved  bug for an unstable situation receiving trigs at startup of a patch


v0.6.37 (2018-12-28)

-- CONVOLVZILLA
---- DISFUNCTIONALCONVOLVZILLA is named now CONVOLVZILLA
---- added EARLY REFLECTIONS with a DRY-WET MIX pot; EARLY REFLECTIONS are computed before entering PREDELAY stage
---- added PREDELAY with DRY-WET MIX pot and a msecs Pt. Msecs are from 1 to 400, PREDELAY is computed before entering first ALL PASSES smoothers

-- NYECHOecoeco
---- solve a crash on win
---- corrected some timing when switching to slow mode

-- SMASHMASTER (+ RODENT V2 + other distortion)
---- improved memory mode for low memory situation/pressure on win

-- SQUONK
---- added selective RANDOMIZE for CV LINES A B C D E and REP (via contextual menu)


v0.6.36 (2018-12-20)

-- 4MIX 8MIX 16MIX
---- bug: mute not visible if set when in SOLO with SOLO in another channel
---- add special context menu command: "POST OUT won't SOLO"
	when ON, the POST out will OUTPUT the signal also if there is a SOLO in other channels

-- DISFUNCTIONALCONVOLVZILLA for brevity DISFUNCTIONACONVOLVZILL
---- bug for duplicate symbol on WINDOWS

-- SAM
---- add a limit to the sample/voice rebuilder


v0.6.35 (2018-12-19)

-- DUAL (208) ENVELOPE
---- it's a copy of the 208 envelope, 2 times
---- controls (from top):
---- GATE/TRIG IN (+TAP) (is the PULSE IN to start the Envelope)
    is a GATE IN if in "sustained" mode and a TRIG IN if in "transient" mode""
---- EndOFCycle Pulse OUT (+LED): a 1 msec PULSE is coming out every time the cycle is closed
    can be used to retrig the envelope to have an LFO/VCO
---- SUST - TRANS radio button to setup the mode in sustained or transient
---- ENV OUT is the output of the ENVELOPE (+ orange LED). Value goes from 0v to 10v
---- sliders
---- ATTACK from 2 msecs to 10 secs, CV controllable
---- DURATION, only working if in transient mode, is the time the ENV stays to 10v
    when the ATTACK phase is finished
    time goes from 2 msecs to 10 secs
---- DECAY from 2 msecs to 10 secs, CV controllable

-- DUAL (208) RND (+DUAL INVERTER)
---- is a 2 section of 4 RANDOM uncorrelated values changed by the TRIG IN (+TAP)
---- mini section with DUAL INVERT signals (to invert the ENV, for example)

v0.6.34 (2018-12-16)

-- BOH!NGLER
---- MAH !? Mistery module

-- DUAL PULSER
---- it's a copy of the 208 pulser, 2 times
---- controls are simple
---- parameters and views from TOP:
---- TRIG IN (TAP) to start a PULSE (the pulse will be emitted at end of the timer
---- SELF TRIG, if ON the PULSER will pulse itself at the end of the timer (enters in LOOP mode)
---- CV VCA slider is the VCA for the CV (BLACK INPUT port): used to modify timing using CV coming in
---- TIMER slider form 2 msecs to 10 seconds (exact replica of the curve and timing)
---- BLACK input, is the CV in for the CV VAC left SLIDER
---- LED and RED output, is the PULSE OUT at the end of the timer

-- DUAL FIVE STEPS
---- it's a copy of the 208 simple 5 steps sequencer, 2 times
---- controls are simple
---- parameters and views from TOP:
---- Number of stage, with DRAG display (from 2 to 5 steps)
---- RESET TAP and TRIG In (this is present in the original only using the external connector)
---- the RESET can be assigned to the next clock coming in using the contextural menu
---- the PULSEQ buttons are ON-OFF buttons. if ON that stage will emit a pulse when traversed
---- the LEDs for the current stage played
---- 5 slider 0v to 10v to set the stage voltage
---- PULSE IN (+TAP) is the clock IN input
---- PULSE OUT, is the PULSE OUT of the CURRENT STAGE, if the STAGE has the PULSEQ button ON
---- CV OUT is the output CV for the current stage

-- QUADSIMPLER
---- add a contextual menu to activate NEGATIVE CV for NEGATIVE frequencies

-- 4MIX 8MIX 16MIX
---- add value display to PAN
---- add value display to CHANNEL VOLUME
---- add value display to MAIN VOLUME
---- add BIG VALUE display on DRAG for PAN and CHAN VOLUME and MAIN VOLUME

-- CLOCK MULTIPLIER
---- add DIVIDER explicit mode
---- the DIVIDER mode is common for all 3 clock MULT/DIV ers
---- the DIVIDER MODE is actived clicking on the "DIVIDER MODE" TAP button
---- until now the division was done multiply for number less than 1.0, for example to divide by 2
    you had to multiply for 0.5000 or to have a divide by 3 you had to multiply by 0.3333
    now you can activate the DIVIDER mode and set 2.0 and 3.0
---- renamed (visually) CLOCK MULT DIV

-- SCALA QUANTIZER
---- shorted names of scalas in the contextual menu
---- support for voltage offset when in MIDIMAP mode

-- EQUAL DIVISION QUANTIZER
---- support for voltage offset when in MIDIMAP mode

-- JANNEKER
---- changed pulse out time from 0.1 msecs to 1 msec

-- JANNEKER TIMED
---- changed pulse out time from 0.1 msecs to 1 msec

-- DISFUNCTIONALCONVOLVZILLA for brevity DISFUNCTIONACONVOLVZILL
---- solved a crash when creating a new patch

v0.6.33 (2018-12-02)

-- SAM
---- solved very stupid bug: I had the CV inputs for PITCH, MOUTH and THROAT commented out!

-- 02NAGOL
---- improvements:
---- the STOP is now STOP-CONTINUE
---- added ONE SHOT MODE
---- added TIME RATE
------ the red display is draggable editable
------ a CV can control the current time rate
------ the CV is multiplied by the VCA
------ the green display shows the REAL time rate applied to the NAGOL player
------ the formula for a single step TIME is
            APPLIED TIME = TIME_OF_THE_STEP * clamp(TIME_RATE + ABS(CV) * 0.2 * VCA, 0.01, 999)
---- added CV addressing a single CV can select one of the N steps of the NAGOL

4MIX 8MIX 16MIX
---- add POST outputs LEFT and RIGHT for single channel
---- the POST outputs are activated via context menu


v0.6.32 (2018-11-28)

-- 02NAGOL
---- is a CSV file reader and player
---- pressing START all the VALUES will be presented at the ports,
    with correct timing expressed by the column MSECS
---- if the TRIG TO ADVANCE is active, the advance is triggered using PULSEs

-- LOGAN20
---- same as LOGAN but with 20 values
---- to be more compatible with 4Hands

-- LOGAN
---- CSV logger with 6 values
---- the CSV is a Comma Separated Values file, that can be opened as spreadsheet
---- first line of the output are the titles: TICKS, MSECS, + VALUES titles
---- titles for single channels can be edited
---- if AUTOSAVE is ON, a file name "logan1_DATE_SOMENUMBERS.csv" will be automatically saved in the RACK directory
---- is AUTOSAVE is OFF a dialog will be presented
---- SAVING starts tapping the START button (or triggering it)
---- SAVING ends tapping the END button (or triggering it)
---- a contextual menu will let you choose the granularity of the saving
----- every sample, every 10 samples, every 100 samples, every 1000 samples, every 10000 samples
---- if LOG on TRIG input is occupied, saves will happen every time a PULSE is received

v0.6.31 (2018-11-25)

-- SAM
---- it's a FIRST attempt to port from another port to C of the S A M speech synth
    for CBM64 https://github.com/s-macke/SAM
    manuals are here  http://www.apple-iigs.info/newdoc/sam.pdf
---- can use normal input or phonetic input
---- all inner orginal params are respected
---- legends:
---- on top there is a FIELD in classivc BLUE CBM64, it's the input field/text
---- if you are rendering normal text max 90~100 characters will be rendered
---- if you are rendering phonetics text could be longer
---- if in PHONETIC mode the color are inverted
---- the flag SINGING activates the inner modulation of the Speech synth
---- when the ERROR RED LED is highlited means there is an error in the PHONETIC parsing
---- SPEED PITCH MOUTH THROAT are inner SAM controls, please refer to the manual
---- every variation for this paramenter will be rendered adter a stop and start
    (or at the end of a loop if looping)

-- AttackSustainRelease16, AttackSustainRelease8, AttackSustainRelease4
----- multiple Attack (Sustain) Release envelope with some common control, repeated 16, 8 or 4 times
----- legenda:
----- ATTACK from 0 to 1
----- ATTACK CV (formula (IN voltage value / 5)
----- RELEASE from 0 to 1
----- RELEASE CV (formula (IN voltage value / 5)
----- LIN-EXP control
----- SCALE with inversion, from -2 to +2, default 1
----- TAP to trig/gate manually
----- TRIG/GATE input
----- AR_MODE ON/OFF, if ON works with a trig and RELEASE will be activated ASA the ATTACK finishes,
    if OFF, and THE GATE is UP the SUSTAIN will be held
---- BUSY ON/OFF, if ON, an new retrigger can happen only if the ADSR is in stable/idle mode (not running)
---- ZERO ON/OFF, if ON, witha new retrigger, the ASR will start always from the ZERO value
    (and not from current ENV out value)
---- LOOP ON/OFF, if ON and the AR_MODE is ON, the AR will autoretrig at the EOC
---- EOA End of Attack pulse OUT (with a small guide led)
---- EOR End of Release pulse OUT (with a small guide led)
---- VCA in (simple vca connected to the envelope)
---- VCA out (simple vca connected to the envelope)
---- ENV OUT the output of the Eenvelope signal (with a small guide led)
---- UNITY_MIX ON/OFF, if ON the ASR ENV OUT is summed to the other ASR ENV OUt with UITY_MIX ON,
    and value is presented to the GLOBAL UNITY MIX ENV OUT output
--- global controls:
---- ATTACK from 0 to 1
---- ATTACK CV (formula (IN voltage value / 5)
---- RELEASE from 0 to 1
---- RELEASE CV (formula (IN voltage value / 5)
----- LIN-EXP control
---- SCALE with inversion, from -2 to +2, default 1
---- global TAP to trig/gate manually
---- global TRIG/GATE input
---- global VCA in (simple vca connected to the unity mix envelopes)
---- global VCA out (simple vca connected to the unity mix envelopes)
---- global ENV OUT output of unity mix

-- DEEPNOTE
---- add CV to control TIME: formula is: abs(incoming VOLTAGE) * 10 (min 0.001 max 999. secs)
---- add CV to control FREQ1 FREQ2 FREQ3 FREQ4: formula is: abs(incoming VOLTAGE) * 10 (min 0.001 max 100.00 Hz)

-- CONST ADD MULT
---- add DO OPERATION on PULSE (4 channels)
---- if the PULSE is active (connected) the operation is executed only on PULSE IN

-- TIMEX
---- feature request; add (2 times) CV RAMP OUT to the counters: formula is: (CURRENT_COUNT / TARGET_COUNT) * 10.0 (volts)
---- for example if TARGET_COUNT is 5, the RAMP value will output 0.0 2.0 4.0 6.0 8.0

-- 4MIX 8MIX adn 16MIX
---- add anticlick filter on MUTE/UNMUTE

-- BRIDGES
---- Add GLOBAL RESET command TAP and TRIG (both bridges are reset)
---- Add single bridge RESET command TAP and TRIG
---- Add ONE SHOT MODE (if status changes, must be reset)
---- Add red LED to show if the ONE SHOT MODE was consumed (to be reset)

-- JOOPER
---- bug: reset was not correctly resetting if in DUAL EXCLUSIVE MODE
---- Add titles for scenes

-- µOP
---- added missing LEGENDA parts in the contextual menu

-- µSQ2
---- default duration to 1/16

-- 4HANDS
---- Add global PORTA CV in + VCA
---- Add RANDOM command to randomize current scene
---- Add titles for scenes

-- BIVIO
---- Add GLOBAL RESET command TAP and TRIG (all 3 bivios are reset)
---- Add single bivio RESET command TAP and TRIG
---- Add ONE SHOT MODE (if status changes, must be reset)
---- Add red LED to show if the ONE SHOT MODE was consumed (to be reset)

-- SEVEN SEAS
---- removing clipping ends when importing arbitrary source files

-- JANNEKER
---- bug: pulse count at startup not inited
---- feature request: if in RECORDING mode, when press ADD, the ADD is happening on the next PULSE in
---- feature request: add input by keypad
---- ADDING a CHEAT SHEET to use it with the KEYBOARD
---- TO use the keyboard your mouse must be placed on top of the JANNEKER
------ "PAGE DOWN" go to the next scene
------ "PAGE UP" go to previous scene
------ "ESCAPE" reload current scene removing current alterations
------ "OPTION/WINDOWKEY `P`" will reset current scene, all scenes will be deleted
------ "OPTION/WINDOWKEY `A`" will add current scene to the scenes list
------ "ENTER (keypad)" add a stage with current values at the end of the sequence
------ "RETURN" (or "OPTION/WINDOWKEY `ENTER (keypad)`") update current stage with current onscreen values
------ "I" insert a stage with current values before the current stage of the sequence
------ "DECIMAL POINT (keypad)" reset current pulse count entering value to 1
------ "+" adds 1 to the current pulses value
------ "-" subtract 1 to the current pulses value
------ "OPTION/WINDOWKEY `-`" will delete current scene, and remove it from list
------ "OPTION/WINDOWKEY `+`" add a stage with current values at the end of the scenes (same as "ENTER (keypad)")
------ 0 1 2 3 4 5 6 7 8 9 are used to entering data
-------- values for modes are:
-------- PULSECOUNTmode from 1 to 9999


-- JANNEKER TIMED
---- BUG: can't move target time! (sorry forgot to set editable the DISPLAY!)
---- BUG: saved times were all aligned to seconds (now is really 0.001 seconds resolution)
---- ADD SCENE works only if in (RECORD & ACTIVE) or not in RECORD mode (to help automated recorders)
---- increased time resolution now from 0.001 to 999.999 seconds
---- add time scale
---- some UI changes

-- SCALA QUANTIZER
---- dealing with scala files with spurious chars at the end (\r )


v0.6.30 (2018-10-26)

-- JANNEKER TIMED
---- ADD REC mode
---- the idea is to help during composition
---- if REC mode is ON and ACTIVE is  target time will advance automatically
---- when hitting ADD (scene), the target time is sotred and a new time is inited to 0.0
---- solved a crash

-- JANNEKER
---- ADD REC mode
---- the idea is to help during composition
---- if REC mode ON and ACTIVE ON incoming pulse will increment (or decrement)
    current PULSES for scene
---- when ADD scene if in REC mode, target PULSES becomes 1 again
---- solved a crash

-- SEVEN SEAS
---- BUG: drag and drop was not working if dragging a single bank: corrected
---- ADD REC mode: in rec mode, wavetables are filled in real time with incoming data
when last sample is hit, the record mode goes automatically OFF
---- ADD SAVE all BANKS in an unique file: useful if you do bank compositions to reload fast

-- RXG100ChanB
---- multithreaded

-- RXG100ChanA
---- multithreaded

-- SMASHMASTER
---- multithreaded

-- RODENT V2
---- multithreaded

-- MAGISTER FUZZ
---- multithreaded
---- wrong params assinged to chan 2: corrected

-- TIMEX
---- removed unprecise 1/100 counter
---- added trigs IN to RESET for COUNTERS
---- added trigs IN to START/STOP  ALARMs
---- changed style of counters (more usable)

-- CONFUSINGSIMPLER
---- crash when moving from win to mac

-- COMPLEXSIMPLER
---- crash when moving from win to mac

-- QUADSIMPLER
---- crash when moving from win to mac

v0.6.29 (2018-10-23)

-- SEVEN SEAS
---- smoothing parameters in the audio thread and improved performances
---- wrong normalize after loading big file corrected


v0.6.28 (2018-10-22)

-- RXG100ChanB
---- Port of Valdemar Erlingsson VST RXG100 module
---- RXG100 - An emulation of the Randall RG100 preamp, channel B.
---- stereo adaptation, with some tweaking to improve performances and levels
---- added all the CV and PULSE inputs to make it MODULAR
88

-- RXG100ChanA
---- Port of Valdemar Erlingsson VST RXG100 module
---- RXG100 - An emulation of the Randall RG100 preamp, channel A.
---- stereo adaptation, with some tweaking to improve performances and levels
---- added all the CV and PULSE inputs to make it MODULAR
87

-- MONORECORDER
---- the mono version of the master recorder ;)
---- someone asked for it, so you can create multiple syncronized stems
86

-- SMASHMASTER
---- Port of Valdemar Erlingsson VST SMASHMASTER module
---- An emulation of the Marshall Shred Master stomp box.
---- stereo adaptation, with some tweaking to improve performances and levels
---- added all the CV and PULSE inputs to make it MODULAR
85

-- RODENT V2
---- Port of Valdemar Erlingsson VST RODENT V2 module
---- An emulation of the ProCo Rat stomp box, including several "mods".
---- stereo adaptation, with some tweaking to improve performances and levels
---- added all the CV and PULSE inputs to make it MODULAR
84

-- MAGISTER FUZZ
---- Based on Valdemar Erlingsson VST Mr Fuzz module
---- An emulation of the Maestro MFZ-1 Fuzz (Diode based version).
---- stereo adaptation, with some tweaking to improve performances and levels
---- added all the CV and PULSE inputs to make it MODULAR
83

-- JANNEKER TIMED
---- it's a time director/scene coordinator PULSE sequencer
---- it's the same as the JANNEKER, but uses real time as duration of the scene
---- instead of END OF PULSES there is an END OF SCENE
    there is a pulse OUT when the time for the current scene
    is finished, advancing to the next scene
82

-- JANNEKER
---- the pulse sequencer/coordinator
---- companion for JOOPER and for 4HANDS
---- with JANNEKER you can set KEYFRAMES/SCENES of different pulses duration
---- Every scene has its own duration in pulses
---- there is PULSE out every time a SCENE is changed
---- there is a PULSE out every time the complete sequence is executed
---- PARAMENTERS:
---- ACTIVE TAP/TRIG JANNEKER will advance on PULSES
---- LOOP TAP if ON the sequence is always repeated
---- EOL (End of Loop) will output a PULSE when the sequence is finished
---- EOP (END OF PULSES) will output a pulse when a single SCENE is finished
---- PULSES display/editable is the count of pulses for curent SCENE
---- CURRENT PULSE display of the current count of pulses for the current SCENE
---- DECR -1 decrement the current count of pulses (sequence can go backward too)
---- INCR +1 increment the current count of pulses
---- SCENE display is the curren count of scenes
---- CURRENT SCENE (editable) is the current in action scene
---- RESET TAP/TRIG will reset CURRENT SCENE to 1 (if there are scenes)
---- PREV TAP/TRIG will go and load CURRENT SCENE - 1
---- NEXT TAP/TRIG will go and load CURRENT SCENE + 1
---- ADD TAP/TRIG will add a scene at the end of scenes with current set PULSES
---- LOAD TAP/TRIG will load the current scene to the screen (PULSE are updated)
---- UPDATE TAP/TRIG will update current store scene from the screen
---- DELETE TAP/TRIG will delete current scene
---- DELETE ALL TAP/TRIG will delete all scenes
81

-- BIVIO
---- it's a triple gate with random path choice
---- BIVIO 1 and BIVIO 2 are the same: 1 INPUT and 2 OUTPUTS
---- BIVIO 3 is a 2 INPUTS and 1 OUTPUT
---- a pulse will switch the output (or the input) with probability
---- probability goes from 0% (will never switch from current status)
    to 100% (will always switch)
80

-- BRIDGES
---- it's a DUAL CONTROLLABLE GATE
---- parameters:
---- IN and OUT with GREEN LED signaling the GATE is ACTIVE
---- GATE MODE button, if ON the GATE input is used, if OFF the PULSE input is used
---- if GATE ON button, if GATE MODE ON the button to activate the GATE
---- GATE IN activator, if GATE MODE is ON, if VOLTS are under 1 volt, GATE is OFF, if Volts are over 9 volts, GATE is ON
---- TAP - TRIG pulse, if GATE MODE is OFF, a PULSE ACTIVATE the GATE, and another one DEACTIVATE it
---- the TAP TRIG has probabilty for 0 (never happen) to 1 : evey PULSE/TRIG are used

---- the SMOOTH paramenter is common to BOTH gates, neede to avoid clicking in FAST ON OFF Gating

---- from contextual menu you can set:
---- INVERT BRIDGE MODE (all the logic are inverted: the GATE are OFF when signaling is ON...)
---- RETURN LAST VALUE if ON a GATE that is OFF is not returning ZERO,
but is freezed to the last VALUE (can be exploited as Sample & Hold ;) )
79

-- SEVEN SEAS
---- Yet Another Wavetable Oscillator YAWO
---- is 64 banks, 64 waves, 256 samples STEREO VCO
---- with MORPH and SWARM modes
---- compatible with Waveedit, Morphing Terrarium, Piston Honda mk3
---- with 3 level of interpolation (check contextual menu)
---- You can use drag and drop to load BANKS
---- you can drag and drop files or directories
---- (try to download all the table from the users from waveedit (https://waveeditonline.com))
---- https://waveeditonline.com/wav-files.zip
---- or you can build your wavetables using http://synthtech.com/waveedit
---- PARAMETERS
---- CV IN 1v/oct
---- FINE tuning ( +- semitones)
---- EXP FM with VCA
---- LIN FM with MODINDEX ;)
---- OCTAVE control from -8 to +8
---- SWARM (green panel) activate MANY (many many) oscillators mode
------ SWARM ON-OFF
------ SWARMING Frequencies with CV (when using CV the POT becomes a VCA for the CV)
------ SWARMING Pulsewidth with CV (...)
------ SWARMING Banks with CV (...)
------ SWARMING Waves with CV (...)
---- PULSE WITH from 0 to 1 with CV control and VCA
---- WAVE SURFER CONTROL WITH from 0 to 64 with CV control and VCA
---- WAVE Visualizer, in yellow the current wave used by the VCO
---- WAVE Oscillocope, in cyan the current wave in output
---- DC BLOCK ON-OFF (sometimes the PW creates DC buildup)
---- MORPH ON-OFF (to have smooth(morphing changes between banks and waves)
---- BANK SURFER CONTROL WITH from 0 to 64 with CV control and VCA
---- BANK SURFER VISUALIZER present the curren MORPHED (if MORPH ON) BANK
---- in RED the current MORPHED WAVE (can be seen in the WAVE Visualizer in yellow)
---- the BANK SURFER VISUALIZER is an interactive control
------ you can browse between banks like a book, or between waves in the current morphed bank
------ you can drag in the "Visual Scale area" to increase decrease the visual scale
---- of course the OUTPUT STEREO, with integrated level
78

-- DISFUNCTIONALCONVOLVZILLA for brevity DISFUNCTIONACONVOLVZILL
---- added 3 attenuation levels: 0db, -6db, -24db
---- FEATURE REQUEST: default for a new module is -6db
---- default new module is ACTIVE now
---- FEATURE REQUEST: added DRY-WET cv (unipolar, from 0 to 10 volts)
---- added MONO mode: if only one input is connected, the process will use one convolver
    halving the CPU use
---- FEATURE REQUEST: added organization in subDIRS: you can add one level of directories
---- HUGE improvement in Impulse Wave Drawing (moved all offscreen) (1000x times faster)

-- 4HANDS
---- solved bug #77 ('e riavul') (updating a value with portamento also when is fresh inited)

-- JOOPER
---- solve requests #62
---- add command "TO FIRST" by TRIG and by TAP: will reset scene sequencer to step 1
---- add LOAD by TRIG (was only by TAP)
---- add SAVE by TRIG (was only by TAP)
---- add DELETE by TRIG (was only by TAP)
---- add DELETE ALL by TRIG (was only by TAP)
---- add UPDATE current SCENE with current SCREEN (TAP and TRIG)
---- add INSERT current SCREEN before current SCENE (TAP and TRIG)


v0.6.27 (2018-10-09)

-- RATCHET
---- a pulse ratcheting device
---- parameters
---- CLOCK IN (the time computer input)
---- TAP and PULSE IN, is the trig received to be RATCHETED
---- RANDOM ON - OG. IF OFF, every pulse will have a RATCHET,
    if ON some of the pulse will be not considered using the probabilty KNOB
---- PROBABILITY, from 0 to 1 (from never happen to happens evey time)
---- MIN and MAX range, are display clickable settable and CV controllable
---- if the RATCHET must be generated, will be with number of repetitions chosen in the range
    naturally if the MIN is 2 and MAX is 2, the result is ALWAYS 2 repetitions
---- PULSE OUT the RATCHETED PULSE

-- DISFUNCTIONALCONVOLVZILLA for brevity DISFUNCTIONACONVOLVZILL
---- removed setting to 4096 size blocks (always clicking...)
---- more smoother process adopting a triple buffering


v0.6.26 (2018-10-07)

-- ADDENDA doc for the OP aka µOPERATOR

The CLOCK in is not a REAL CLOCK in, it's a PULSE IN for the internal
TIME COMPUTER.
The TC computes time average of last 4 pulses and tries to set the frequency.
If you use with wiggly clocks, or with random pulses you'll get strange results.
Per design the CLOCK IN win OVER the inner FREQUENCY, so we can use an external
LFO or CLOCK generator and sync many OP to an external TIME BASE
and detach it, and the OP continues to use that as BASEFREQ.
To regain ownership of the frequency, just move the TUNE pot
(after you have detached anything is connected to the CLOCK IN).


-- DISFUNCTIONALCONVOLVZILLA for brevity DISFUNCTIONACONVOLVZILLA
---- it's just a convolver
---- you can drag an drop any file AIF or AIFF or WAV of any bit size, long, int, short, char, float
---- 22kHz to 96kHz
---- or you can open via menu
---- the impulse files will be added to the directory RTImpulse (at Rack level, so other can acess it)
---- or you can add directly to the directoy
---- the impulse in the directory will be listed in the contex menu
---- there is a control on the IN level and on the OUT level
---- on the output the level can be lowered by other -6 dB
---- if you hear any buzzing in the audio, try to hit the RESET button
---- I still have to fionish it adding envelopes and actions on the impulse

-- WORMHOLIZER
---- it's a temporal effect, a swarm of delays are involved,
    all set to different uncorrelated time distances
---- parameters are simple
----- BYPASS set the control for the heart of the sun
----- WORMOHLIZER (CV controllable) increase the number of wormholes
----- SPATIALIZER (CV controllable) increase the spread in the space of WHs
----- TUNNELIZER (CV controllable) decrease/increase the density of the temporal events
----- DRYWETIZER set the control for the liver of the earth

-- DL or µDELAY
---- dual signal DELAY with 200 msecs and 2000 msecs delays
---- parameters
---- IN signal 1
---- IN signal 2 (can be used to do feedback loops)
---- VCA IN signal 2 form 0 to 2
---- DELAY value (from 0 to 200 msecs fro D1 and from 0 to 2000 msecs for D2)
---- DELAY CV IN 1V is 20 msecs more for the D1 and 200 msecs more for the D2
---- FB VCA from 0 to 1.05 (infinite grow)
---- FB CV IN
---- MIX OUT and OUT (all left, original signal, all right effected delayed signal)
---- + show OF sreen to check the inner buffer...

-- SL or µSLEW
---- a dual SLEW with SHAPE control
---- paramenters (x 2)
---- SHAPE from linear to exponential
---- ATTACK (from 0 to 100 secs)
---- RELEASE (from 0 to 100 secs)
---- BYPASS TAP ad BYPASS TRIG
---- IN and OUT signal

-- metaAARDVARK
---- BUG: wrong behaviour of the smooth output when opening a patch

-- CONFUSINGSIMPLER
---- BUG: activated again the ANTICLICK on slices
---- modified auto level of the YUMMER
---- BUG: crash report 72. Slices are cut if samples changes (and size is shorter)

-- µSQ2
---- BUG: spelling error LENGTH ;)
---- When adding a stage, will move to the added stage
---- ADDING a CHEAT SHEET to use it with the KEYBOARD
---- TO use the keyboard your mouse must be placed on top of the µSQ2
------ "PAGE DOWN" go to the next stage (if last, goes to fist)
------ "PAGE UP" go to previous stage (if first, goes to last)
------ "ESCAPE" reload current stage removing current alterations
------ "OPTION/WINDOWKEY `P`" will reset current sequence, all stages will be deleted
------ "OPTION/WINDOWKEY `A`" will add current sequence to the patterns list
------ "N" or "*" set the data enteringMode to NOTEmode
------ "D" or "/" set the data enteringMode to DURATIONmode
------ "G" or "=" set the data enteringMode to GATEmode
------ "C" or "V" set the data enteringMode to CV2mode
------ "ENTER (keypad)" add a stage with current values at the end of the sequence
------ "RETURN" (or "OPTION/WINDOWKEY `ENTER (keypad)`") update current stage with current onscreen values
------ "I" insert a stage with current values before the current stage of the sequence
------ "DECIMAL POINT (keypad)" set current data entering to defaults:
-------- if in NOTEmode --> REST, if in GATEmode --> 50%, if in DURATIONmode --> 1/4, if in CV2mode --> 0.00
------ "R" set current entering NOTE to "REST"
------ "+" adds 1 to the current value of current enteringMode and overflows
------ "-" subtract 1 to the current value of current enteringMode and overflows
------ "OPTION/WINDOWKEY `-`" will delete current stage, and remove it from list
------ "OPTION/WINDOWKEY `+`" add a stage with current values at the end of the sequence (same as "ENTER (keypad)")
------ 0 1 2 3 4 5 6 7 8 9 are used to entering data
-------- values for modes are:
-------- NOTEmode from 0 to 255  (notes are midi note numbers)
-------- DURATIONmode from 0 to 21 (1/384 -> 4/1)
-------- GATEmode from 0 to 8 (0% -> 100%)
-------- CV2mode from 0 to 999 (0.00 to 9.99 volts)


E G A A

how to enter "I feel love"  4 notes E G A A, version 1

OPTION P  --> (clean the sequence)
D --> (durationMode)
6 --> (1/4)
G --> (gateMode)
4 --> (50%)
N --> (noteMode)
, --> (clean to ZERO)
5 --> (total 5 --> F-1)
2 --> (total 52 --> E3, good!)
ENTER --> (stage added)
+ --> (F3)
+ --> (F#3)
+ --> (G3, bingo)
ENTER --> (stage added)
+ --> (G#3)
+ --> (A3, bingo
ENTER --> (stage added)
ENTER --> (stage added BIS, same note)


how to enter "I feel love"  4 notes E G A A, version 2
(we don't care about durationa nd gates by default set to 1/4 and 50%)

OPTION P  --> (clean the sequence)
N --> (noteMode)
, --> (clean to ZERO)
5 --> (total 5 --> F-1)
2 --> (total 52 --> E3, good!)
ENTER --> (stage added)
, --> (clean to ZERO)
5 --> (total 5 --> F-1)
5 --> (total 55 --> G3, good!)
ENTER --> (stage added)
, --> (clean to ZERO)
5 --> (total 5 --> F-1)
7 --> (total 57 --> A3, good!)
ENTER --> (stage added)
ENTER --> (stage added BIS, same note)



-- µOP
---- BUG: wrapping freq after feedback (to avoid freq clip modulations)

-- µEN
---- BUG: LVL now is valid as offset of the envelope also when in idle/off mode
---- added contextual menu "ENVELOPE to ZERO when TRIGGED"
    when on, every time the ADSR/AR is trigged/gated, the value goes immediatly to ZERO
(more punchy when in FAST mode ;)

-- STEREOPHASER2
---- added DRY-WET parameter


v0.6.25 (2018-09-25)

-- SQ2 or µSEQUENCER2 pattern programmable sequencer
    there are 2 modes: you edit a sequence, and when ready you can add to the pattern list
    you can sequence in patterns, and all the pattern will be traversed
    when you finish to edit a sequence, you ADD it as pattern (becomes a memory of sequences)
---- parameters
---- START/STOP ON OFF TAP + TRIG IN
---- RESET TAP + RESET PULSE OUT
---- CLOCK FREQUENCY + CLOCK OUT
---- CLOCK IN (TIME computer) + SYNC (RESET) (to sync)
---- COUNT of STAGES in current SEQUENCE display
---- CURRENT STAGE in current SEQUENCE editable display
---- CURRENT STAGE MIDINOTE or REST
---- CURRENT STAGE CV2
---- CURRENT STAGE GATE (from 0% to 100%)
---- CURRENT STAGE DURATION
---- PATTERN SEQUENCER MODE ON OFF
---- COUNT of PATTERNS display
---- CURRENT PATTERN editable display
-- contextual menu
---- SHOW RUNNING STATUS
    if ON will update the screen with stage and pattern in execution
---- CONTINUOUS EDIT
    if ON and not RUNNING, evey edit will be automatically saved for the current stage
    very fast for editing
---- TRANSPOSE
    transposing adressable to current Sequence or current pattern
---- EDIT
    editing for FULL SEQUENCE or single PATTERNs
---- DIRECT STAGE COMMANDS
    will act on the current sequence
---- PATTERN COMMANDS
    will act on the PATTERNs memories




-- SQ1 or µSEQUENCER1 16 steps analog style sequencer
---- parameters
---- START/STOP ON OFF TAP + TRIG IN
---- RESET TAP + RESET PULSE OUT
---- CLOCK FREQUENCY + CLOCK OUT
---- CLOCK IN (TIME computer) + SYNC (RESET) (to sync)
---- GATE LENGTH and GATE LEN CV IN
---- NUMBER of STEPS and NUM OF STEPS CV IN
---- STAGES from 1 to 16, with yellow light for the current STAGE
    and RED light for the terminator
---- OFFSET VOLTAGE (to offset the output voltage) + OFFSET CV IN
---- STAGE SELECT TAP (advance to next) + CV SELECT STAGE
---- outputs:
---- PULSE OUT for every step, GATE for the current STEP
---- CV out CURRENT STAGE + LAST STEP PULSE OUT
-- contextual menu
---- OCTAVE OFFSET command
---- SEQUENCER MODE command (NORMAL, REVERSE, PENDULUM 1, PENDULUM 2, RANDOM)


-- EN or µENVELOPE AR or ADSR envelope
---- parameters
---- AR MODE ON OFF
---- LOOPED ON OFF (if in AR MODE ON)
---- TAP to GATE (or TRIG if in AR MODE ON)
---- IN PULSE to GATE (or IN PULSE to TRIG if in AR MODE ON)
---- ADSR (in in AR mode only ATTACK and RELEASE are used)
---- ATTACK + ATTACK CV IN
---- DECAY + DECAY CV IN
---- SUSTAIN + SUSTAIN CV IN
---- RELEASE + RELEASE CV IN
---- LVL -> LEVEL offset level of the ENV OUT
---- SCALE from -2 to + 2 used to invert the ADSR
---- ENVELOPE OUTPUT
---- ENV controlled VCA INPUT
---- ENV controlled VCA OUTPUT
---- END OF CYCLE PULSE (trigs at the end of RELEASE)
-- contextual menu
---- via contextual menu can be set in exponential mode


-- M2 or µMIXER  4 channels (CV aware)
---- via contextual menu can be set in exponential mode
---- parameters
-- x 4 times
---- INPUT CHAN
---- VCA CHAN
---- IN VCA CHAN
---- MUTE CHAN
-- global
---- CHAIN INPUT(to sum more mixers)
---- VOLUME OUT
---- OUTPUT
-- contextual menu
---- via contextual menu can be set in exponential mode

-- M1 or µMIXER 1 stereo, 3 channels
---- parameters
-- x 3 times
---- INPUT CHAN
---- VCA CHAN
---- IN VCA CHAN
---- PAN CHAN
---- MUTE CHAN
-- global
---- CHAIN IN LEFT and RIGHT (to sum more mixers)
---- VOLUME OUT
---- OUTPUT LEFT + OUTPUT RIGHT
-- contextual menu
---- via contextual menu can be set in exponential mode

-- OP or µOPERATOR
---- a basic Sine VCO with Linear FM, ideal to build up classic yamaha DX algorithms blocks (using mixers and ADSRs)
---- parameters
---- OCTAVE (from -8 to +8)
---- TUNING (from -1V to +1V)
---- SYNC input to SYNC the VCO Phase
---- TIME input: a steady clock can set a precise frequency
---- CVIO IN CV 1/v octave
---- CVIO OUT CV (the IN is copied to make OP chains)
---- EXPONENTIAL IN FM VCA CONTROL
---- EXP IN FM
---- LIN FM VCA CV IN
---- LIN FM VCA CV CONTROL
---- LIN FM CV IN 1
---- LIN FM CV IN 2
---- LIN FM CV IN 3
---- FEEDBACK (auto LINEAR FM, controlled by LIN FM VCA CV CONTROL)
---- RATIO internal frequency scaling :
    {0.1, 0.13333, 0.166666, 0.2, 0.25, 0.33333, 0.5, 0.6666, 1.0, 1.5, 2.0, 3.0, 4.0, 5.0, 6.0, 7.0, 8.0, 9.0, 10.0, 11., 12.}
---- OUTPUT

-- 4HANDS
---- add PORTA GLOBAL control (from 0 to 1.), default value to 1. (to be backward compatible)
---- add RESET to 1 TAP and IN TRIG control

-- CONFUSINGSIMPLER
---- Solve a crash when deleting samples at the end after a drag to select
---- Correct selection when deleting
---- Correct selection when pasting after or before
---- Paste before and after selection were inverted


v0.6.24 (2018-09-16)

-- CONFUSINGSIMPLER
---- removed the DUPLICATE command (via menu and via keyboard)
---- Add GLOBAL ON - OFF for the SOUND ON SOUND
---- Add ON - OFF for the PREVIEW of SOS when not in recording mode
---- Invert SOS MIX Meaning: FULLY CCW (all left) is internal signal, center is MIX 50%-50% internal signal and input signal
    FULLY CW (all right) is only external signal
---- Selection is maximized when a new sample is created via recording
---- GRID now is activated or via MENU (GRID Active command on SAMPLE DISPLAY menu) or using a PULSE. MUCH MORE CREATIVE
    for doing recursive samples
---- SCRAPBOOK is global, now you can cut and paste between CONFUSINGSIMPLERa
---- Add PASTE BEFORE selection and PASTE AFTER selection commands (and into an empty CONFUSINGSIMPLER)

-- COMPLEXSIMPLER
---- removed the DUPLICATE command (via menu and via keyboard)

-- QUADSIMPLER
---- removed the DUPLICATE command (via menu and via keyboard)

v0.6.23 (2018-09-15)

-- CONFUSINGSIMPLER
---- It's an interactive sampler with many little features, and a couple of sequencers
---- Can load AIFF, or WAV 16bit or 24bit PCM ot WAV IEEE FLOAT formats

    Starting from TOP

    There are 2 inputs, if are connected the SOS (Sound on Sound) act as a mixer with control voltage
    so you can mix the incoming sound with inner sampled sound.
    If the 2 INPUTs are not connected the CONFUSINGSIMPLER can record onanistically itself during execution!
    To close the recording you can press or trig the REC button again.
    The Recording can be terminated also using 3 commands from contextual menu:
        ABORT RECORDING (sample is not substited and memory is freed)
        STOP RECORDING AND SAVE IN A FILE (a SAVE AS dialog is presented)
            you can do a lot of performances "recording itself" and save it and WASTING your HD !
        STOP RECORDING and APPEND to SAMPLE (the memory is appended to the current sample (a la morphagene...)

    TIME DISPLAY can display
        CURRENT SAMPLE SIZE
        CURRENT SELECTION TIME SIZE
        CURRENT SELECTION SAMPLES COUNT
        CURRENT PLAYHEAD TIME
        if RECORDING --> CURRENT RECORDING TIME

    SPEED
        SPEED default is 1.0 can go from -2 to +2 and can be CV controlled

    CV and OCTAVE
        of course you can use CONFUSINGSIMPLER as VCO or LFO

    YUMMER it's a little temporal effect to increase grains spread: can be activated,
        increased as effect and the level can be adjusted with LVL pot.

    THE GREEN PANEL, the MODULATION panel
    FM IN + CV
    the LFO value is added to the SPEED giving the SCRATCHY feel to the sample
    the WAVE SELECTOR for the inner LFO for SIN, TRI, SAW, SQUARE and S&H
    the LFO is driven by the FREQ control
    the value of the LFO is controlled by the DEPTH
    the DEPTH can be controlled via CV
    the inner LFO can have the PHASE reset using SYNC
    the inner frequency can be overridded using the TIME pulse input: a time computer will compute the pulse speed
    and set the LFO frequency.
    the LFO can be driven (I tested it) till 8kHz (CRAZY EFFECTS!)
    the FLAG UNI set the inner LFO to UNIPOLAR and the FLAG INVERT set UNIPOLAR in NEGATIVE

    THE PURPLE PANEL, the sample play control panel
    GATED is a flag, and the sample will play only if the GATE is HIGH using START BTN or TRIG IN START
    CYCLE a flag that sets the sample in LOOP
    TAP START and TRIG IN START to control the start or GATING of the SAMPLE
    TAP STOP-CONT and TRIG, controls the STOP and CONTINUE of a play
    if the sample is not in CYCLE, will end at the end of the current selection
    EOC is the End Of Cycle pulse out, a PULSE is generated all the times the sample hits the end of the selection
    START and STOP are control point of the selection (that is also the play zone area)
    Can be CV controlled
    ZOOM is just a visual zoom of samples

    THE GREEN PANEL, the GRID panel
    When active the sample is mapped with a grid. the number of elements in the grid are the SLICES
    the CURR display gives you info about the current selected SLICE
    the current slice can be selected using CV (from 0 to 10v)
    if the flag RND is active next slice is picked random at the EOC (internally):
    if you have the SAMPLE in CYCLE will create an infinite sequence of slices

    THE RED PANEL, the SLICES SEQUENCER PANEL
    it's a set of memories storing selection (Slices)
    Many commands are replicate in the contextual menu appearing on the WAVE DISPLAY
    if you want to delete ALL the SLICES you need to press option/windows key down
    during the command.
    SLICES SEQ display shows the current count of SLICES
    CURR display shows the current selected SLICE
    LOAD PULSE IN load the current slice as current playing selection
    ADD PULSE IN will create a new SLICE in the SEQUENCER with current sample selection
    UPD PULSE IN updates the current slice with data of current sample selection
    DEL PULSE IN deletes the current selected slice
    PREV TAP and PREV TRIG will go to the previous SLICE and LOAD it
    NEXT TAP and NEXT TRIG will go to the next SLICE and LOAD it
    CV will select a current slice using a Voltage from 0 to 10v
    a pulse in RND will select a random current SLICE from the available set

    the SAMPLE DISPLAY
    there are many commands in the contextual menu
    important commands are
    RESET SELECTION to MAX to set current sample selection to full sample size
    TRIM sample, zoom-in in the current selection
    UN-TRIM Sample zooms-out to full sample display
    RENDER SELECTION to Sample, the current selection becomes the
    new sample of the SIMPLER

    there are many small EDIT commands on the samples
    CUT
    COPY
    PASTE
    DELETE
    ZERO
    INVERT
    NORMALIZE
    AMPLIFY

    no more items... :D

-- JOOPER
---- mode is reset only if OPTION/WINDOWS Key is donw

-- COMPLEXSIMPLER and QUADSIMPLER
---- can LOAD floating point WAV files
---- can LOAD multi channel wav files (just first 2 channels)

-- EQUAL DIVISION QUANTIZER
---- octaves to +8 max (to improve a better mapping for midi mapped notes)

-- SCALA QUANTIZER
---- octaves to +8 max (to improve a better mapping for midi mapped notes)


v0.6.22 (2018-09-06)

-- BIGNUMBER
---- an utility to present a single figure counter
---- you can combine many of them to have more sofisticated counters
---- using the contextual menu to set the overflow mode
---- commands
---- ACTIVE: IN PULSE, TAP, OUT PULSE
---- RESET: IN PULSE, TAP, OUT PULSE
---- OVERFLOW (OF): out PULSe whne the OVERFLOW limit is reached
---- PULSE IN, TAP, to increment the COUNTER
---- via contextual menu it is possible to set in count beat mode
    (to count from 1 and not from 0)
---- via contextual menu it is possible to set the overflow
    (so you can set it as clock, for example, if the pulses are seconds)

-- BIGBUTTON
---- utility with 2 BIG buttons to send TRIG and GATES
---- the BUTTONs are PULSER or GATER,
    they can be set using contextual menu
---- TRIG IN, PULSE OUT, GATE OUT and GATE PASSAGE of signal
---- from TOP
---- TRIG IN accept an externa PULSE as button PRESSED
---- PULSE OUT (when the button is pressed)
---- AUDIO CV IN combined with AUDIO CV OUT it's gate activated when the button
    is in GATE mode
---- GATE OUT: when the BTN is in GATE MODE and BTN is pressed outputs 10v


-- PHASOR HARMONIC VCO
---- CV IN for octave was accidentally disconnected!
---- OCTAVE now from -5 to +5
---- added a VCA to OCTAVE CV modulation


v0.6.21 (2018-09-03)

-- 4MIX 8MIX adn 16MIX
---- add the CV compatibility (with flag on the DC block is excluded and mixer could be used as CV mixers)


-- DEBUG!

-- 8MIX
---- correctly loading volumes and pans and mutes and solos

-- 16MIX
---- correctly loading volumes and pans and mutes and solos


v0.6.20 (2018-09-01)

-- DEBUG!

-- CLOCK MULTIPLIER
---- time computer sample rate update

-- LFO MULTIPHASE
---- time computer sample rate update

-- CLOCKABLEDELAY
---- time computer sample rate update

-- XATTODELAYER
---- time computer sample rate update

-- DX7 ENVELOPE
---- missing initialization of inner var

v0.6.19 (2018-08-30)

-- 4MIX + 8MIX + 16MIX
---- first nysthi mixer... needed! for my experiments...
---- 4 channels with VOLUME, PEAK meters
---- HM -> Hide meters to gain some processing speed
---- STEREO IN L and R
---- VOLUME display controller, with PEAK meter (red when clipping)
---- VOLUME CV
---- VOLUME CV VCA
---- PAN display controller
---- PAN CV
---- PAN CV VCA
---- SOLO BTN and SOLO IN TRIG
---- MUTE BTN and MUTE IN TRIG

---- OUT LEFT and RIGHT
---- VOLUME display controller, with PEAK meter (red when clipping)
---- VOLUME CV
---- VOLUME CV VCA
---- CHAIN IN LEFT RIGHT
---- MUTE BTN and MUTE IN TRIG

-- Funny UNNYSTHIPLEASURESGRAPHER
---- waterfall freq display

-- ALL METERS
---- changed curves to present from -30 dB on

-- DYNAMO
---- increased resolution for meters
---- removed useless and distracting RMS meter (too much movement)

-- LFOMULTIPHASE
---- some tweaking to improve performances, removing not needed calculations in the main loop
---- added VCA to control in CV for PWM
---- added VCA to control in CV for the FREE PHASE

v0.6.18 (2018-08-24)

-- 4HANDS
---- Utility multivoltage module. It's like a Surveillance, but with memory and automatized
---- it's 2 groups (A and B) of 10 voltages
---- the group A contains for every line an IN, a DRAGDISPLAY and an OUT
---- the group B contains for every line an IN, DRAGDISPLAY, a PORTA(mento) and an OUT
---- the INs are enabled by the "ENBLE INs" button
---- when INs are enable internal memory is written with the incoming CV (if any attached)
---- the idea is to record performance, or SAVE particular combinations of voltages
---- the RESET button, will reset only the loaded/current memory without affecting theSCENE memories
---- the commands and controls are:
------ IN to load a CV
------ DRAGDISPLAY to edit memory voltage, from -10v to +10v
------ PORTA(mento) to have portamento between 0 and 100 secs
------ OUT to output voltages
----
---- GLOBAL CONTROLS
------ ENABLE INs to enable overriding inner memory with incoming voltages
------ RESET to reset all current values to 0v and 0 portamento
----
---- SCENE MANAGER CONTROLS
------ DRAGDISPLAY to set and check current to be loaded scene
------ green DISPLAY showing number of saved scenes
------ LOAD to load in memory current selected scene (red display)
------ SEL SC to select and load a scene using a control voltage: the CV in accept from 0V (first scene)
    to 10v (last scene)
------ PREV TAP and TRIG, to move to prev scene and LOAD it in memory
------ NEXT TAP and TRIG, to move to next scene and LOAD it in memory
------ ADD TAP and TRIG, to add current screen situation as scene (last in list)
------ SAVE TAP and TRIG to save memory in the current presented scene, overriding the content
------ DELETE TAP to delete current presente scene (red display) (memory is unaffected)
------ DELETE ALL TAP --> BEWARE works only with "windows-Command" KEY down to delete all
    the scenes stored in the scene manager


-- CLOCKABLEDELAY
---- add an hard limiter (max voltages -20 to +20 after feedback)

-- SCALA QUANTIZER
---- bump to performances
---- when IN not connected, OUT presents ROOT voltage (+ octave and tuning)

-- EQUAL DIVISION QUANTIZER
---- bump to performances

-- everything is back to 64 bit processing


v0.6.17 (2018-08-20)

-- CLOCKABLEDELAY
---- in HOLD mode, respect the HOLD a la DLD way
---- the recorded data is preserved in memory
---- it is possbile to scan the memory dragging on the TIME filed with COMMAND/WINDOWS KEY down
    the text color becomes yellow and you can move the sampled window


v0.6.16 (2018-08-19)

-- CLOCKABLEDELAY
---- Freely inspired from MS Dual Looping Delay
---- it's a STEREO DELAY (or consider it as a dual delay line with same time base)
---- the time base is CV controllable, TAP-PINGABLE
---- the inner clock is exported in the pulse OUT to sync many other devices
---- there are 8 point of SEND RETURN, before FEEDBACK and before DRYWET, can be used as patch point to make complex
 and intricate dealy patterns (mixing 2 or 3 CLOCKABLEDELAY or just using LEFT and RIGHT)
---- HOLD and REVERSE
---- PARAMETERS and ACCESS
------ IN LEFT and IN RIGHT (signal In)
------ FEEDIN red display is the draggable amount of IN signal, from 0.0 to 2.0 (0% to 200%)
------ FEEDIN CV and CV VCA modulates the IN SIGNAL, the result is visible on the GREEN DIspaly
------ SEND and RETURN BEFORE FEEDBACK
    signal before entering the feedback loop is exposed to external devices and trasfromations
------ FEEDBACK red display is the draggable amount of the feedback
    (how much of the signal of the past is reassigned to the input)
    the value goes from 0.0 to 1.10 (0% to 110 %) (beware !!!)
------ FEEDBACK CV IN and CV IN VCA to modulate the FEEDBACK with external items
------ FEEDBACK green dispaly shows the amount of real feedback applied
------ TIME red display will set the base time for the delay, the multiplied by MULT will give the final time
    max total time is for 180 seconds stereo 48kHz (so is 90 seconds at 96kHz)
------ TIME is modulated via CV and CV VCA
------ TIME is multiplied by MULT (form 0.001 to 32.0). to have 1/8th (like in the DLD) you must multiply by 0.125 and multiples
    of course is much more flexible with very absurd times divisions
------ TAP TIME activate the time computer and after 3 taps compute the time base
------ TRIG TIME is the same but with external pulses
------ when a time is computed and multiplied the timebase is presented into the GREEN DISPLAY
------ the inner clock is set to the same frequency amd a pulse is OUTPUT from PULSE out
------ HOLD and HOLD TRIG IN will freeze current buffer a repeated forever...
------ REV and REV TRIG IN will reverse direction of the READ HEAD in the delays (both during execution and HOLD mode)
------ SEND and RETURN BEFORE DRY-WET
    signal before entering the DRY-WET mixer to have more signanl mangling
------ DRY-WET to set the amount of original signal and effected signal
------ OUT LEFT and RIGHT, signal out



-- metaAARDVARK
---- clamping portamento also if no modulations are in

v0.6.15 (2018-08-15)

-- JOOPER
---- its' 8 channel, UNITYMIXER, MULTIPLEXER, IN-OUT SWITCH, with local and global controls. With a scene managar
---- there was a request (Joop van der Linden) to have a complex and seletable on the fly multipath router for complex temporal structures

------ CONTROLS
------ there are 8 lines replicated of 4 INPUTS (ABCD) and 4 OUTPUTS (ABCD)

------ the JOOPER status could be

------- EXCLUSIVE: just one of the A B C D channels is selected on both INPUT and OUTPUT
------- in exclusive mode every one of the 8 lines is a 4 channels MULTISWITCH (IN and OUT)

------- MULTIPLEXER mode
------- any combination of the A B C D INPUTs can be selected. All the activated will be summed
------- any combination of the A B C D OUTPUTs can be selected. All the activated will receive the SUMMED INPUT

------- DUAL EXCLUSIVE A-B mode
------- it's like the EXCLUSIVE but there are A B and C D paired IN and OUT

------- all the channel can be activated with TAP TRIG local
------- Or all the channel can be activated with GLOBAL TAP TRIG

------- the RESET will move all to initial condition

------- SCENE MANAGER
--------- Let you save status in a memory and reuse during the execution of the sequence
--------- COMMANDS and DISPLAYs are are
---------
--------- GREEN display, total of available scenes
--------- RED display, draggable to select current scene
--------- LOAD will load curren scene into memory
--------- ADD will add a scene to the end of the scenes list
--------- DELETE will remove current RED displayed scene from memory
--------- DELETE ALL will clear the scenes list
--------- SELect CV: will select and LOAD a scene using a CV command: 
           cv is a grid of 10V divided by the number of availabel scenes
--------- PREV TAP TRIG, will go back one scene and LOAD it
--------- NEXT TAP TRIG, will advance one scene and LOAD it


-- metaAARDVARK
---- add guard for non finite numbers

v0.6.14 (2018-08-10)

-- metaAARDVARK
---- it's an attempt to obtain a super set of the RVG cell from the Warren Burt famous work "Aardvark IV"
---- http://www.warrenburt.com/my-history-with-music-tech2/
---- it's an LFO CLOCK S&H NOISE PULSE generator
---- contains a simulated R-2R resistor network (a vintage DAC) with deviations due to resistors tolerances (between 0% to 20%)
---- the deviations are recomputed every time the module is initialized or the DEV% param is changed
---- the simulated R-2R is from 1 bit (2 values) to 10 bits (1024 values)
---- values are subdivision of 10V
--- the OUTPUTS ARE:
---- STEPPED = (SAMPLED VALUE * INNER GAIN) + INNER OFFSET
---- SMOOTHED = PORTAMENTO(STEPPED)
---- PULSE = STEPPED > COMPARATOR ? PULSE OUT : NOTHING;
----
------ PARAMETERS
-------- SECTION 1: CLOCK OUT
---------- PULSE TRAIN OUT
---------- SQUARE OUT
---------- RAMP UP OUT
---------- RAMP DOWN OUT
-------- SECTION 2: CLOCK HZ DISPLAYS
---------- CLICK and DRAG display to set frequency of the pulse/sampler from 0.01Hz to 8kHz
---------- Display for modulated Hz
-------- SECTION 3: CLK IN
---------- CLK IN overrides the inner clock, the CLK In is copied ot the CLOCK OUT to create a CHAIN of CLOCKED metaAARDVARK
---------- CLK FM CV + CV VCA to modulta the inner CLOCK
-------- SECTION 4: VOLTAGE OFFSET
---------- CLICK and DRAG display to set VOLTAGE OFFSET from -15v to +15v
---------- Display for modulated OFFSET
---------- CV IN and VCA to modulate the OFFSET
-------- SECTION 5: GAIN
---------- CLICK and DRAG display to set GAIN from -2.0x to +2.0x
---------- Display for modulated GAIN
---------- CV IN and VCA to modulate the GAIN
-------- SECTION 6: PORTAMENTO (the portamento act only on the SMOOTHED OUT)
---------- CLICK and DRAG display to set PORTAMENTO from 0.0 to 1.0
---------- CV IN and VCA to modulate the PORTAMENTO
-------- SECTION 7: RESOLUTION
---------- CLICK and DRAG display to set resolution from 1 bit to 10bits (from 2 to 1024 values)
---------- CLICK and DRAG display to set the DEVIATION of resistors of the simulated DAC (from 0 % to 20% tolerance)
-------- SECTION 8: OUT
---------- STEPPED OUT the current value selected for the current resolution with OFFSET and GAIN
---------- SMOOTHED OUT the current STEPPED OUT value filtered by PORTAMENTO
---------- PULSE OUT uses a COMPARATOR (knob) settable from 0.01v to 9.99v;
----------- when the selected value is higher than KNOB a PULSE is emitted


-- NYVECTORMIXER (big REVAMP!)
---- added X and Y output to use it as automated CV controller
------ X and Y outputs can be UNIPOLAR ( UNI button ON) or BIPOLAR (UNI button OFF)
------ X and Y outputs can be in 1Vpp or 10Vpp range (10x button ON 10Vpp) (10x button OFF 1Vpp)


-- DYNAMO (stereo compressor - expander - hard limiter - ducking device)
---- ADD WALLED mode to ducking: if WALLED is ON, if the compression is reversed becoming an expansion, become ZERO
------ if not WALLEd signal compressed could have reversed phase expansion


v0.6.13 (2018-08-04)

-- NYVECTORMIXER (big REVAMP!)
---- inner one pole LOW PASS is now exposed and excludible
---- added normalized CV OUT for ports A B C and D (the sum is always 10.0f)
---- added the KF animation engine to make complex bidimensional envelopes
------ KEYFRAME ANIMATOR
------ let you record the screen situation in keyframe steps and given a time transitions
very complex enevelope could be created
------ if you have a current KF, the current position is always stored in the current KF
------ controls and VIEWS are:
-------- DELETE ALL KF: delete all the stored keyframes
-------- KF COUNT shows the current count of stored keyframes
-------- TOTAL TIME is the full time of the animation expressed in seconds (editable)
-------- CURRENT KF, presents the current keyframe (editable)
-------- CURR KF DEL when pressed ERASE the the CURRENT KF (and data related)
-------- CURR KF TIME is the time expressed in seconds to arrive to the CURRENT KF (editable)
---------- CURR KF TIME can be edited, and the edit is stored in the CURRENT KF
-------- NEXT KF TIME is the transition time assigned to the NEXT save keyframe (editable)
-------- SNAP KF ! add a NEW keyframe with time "NEXT KF TIME" to the animation
-------- AUTOREC KF record automatically kf with "NEXT KF TIME" time timing"
---------- AUTOREC KF works when ACTIVE and DRAGGING is happening
-------- RUN/HALT runs the animation (or HALT if running)
-------- PAUSE/CONT pauses the animation (and CONTINUE)
-------- RESET reset a running animation to the START condition
-------- LOOP, if active the animation runs forever

-- AUTO(X)FADER
---- timing corrected onSampleRate change
---- fade in fade out will use current level (if hit in the middle of a transition)

v0.6.12 (2018-07-30)

-- AUTO(X)FADER
---- a tool for automatic fades (and xfades)
------ PARAMETERS and controls
------ FADE STATUS, a led presenting the inner status of FADE
------ FADE IN, TRIG/TAP/OUT will TRIG the start of the FADE IN for FADE IN TIME
-------- when the end of FADE IN is hit, the END OF FADE IN will PULSE out
------ FADE OUT, TRIG/TAP/OUT will TRIG the start of the FADE OUT for FADE OUT TIME
-------- when the end of FADE OUT is hit, the END OF FADE OUT will PULSE out
------ FADE EXP  TRIG/TAP/OUT will set fade curves to exponential
------ XFADING  TRIG/TAP/OUT activates the CROSS FADE between LEFT and RIGHT
-------- (1 3 5 and 7 are LEFT, and 2 4 6 and 8 are RIGHT)
------ FADE IN TIME CV + VCA CV + display interactive will set the FADE IN TIME
------ FADE OUT TIME CV + VCA CV + display interactive will set the FADE OUT TIME
------ 8 INs and 8 OUTs
-------- all active in fade mode to do a fully MUTICHANNEL RECORDING
------ in XFADE mode
------ with LOW FADE status the IN 1 is presented on the OUT 1 and the IN 2 is presented on the OUT 2
------ during the FADE IN there is the automatic mix
------ with FADE in STATUS HIGH hte IN 1 is presented on the OUT 2 and the IN 2 on the OUT 1


-- STRUMMER
---- A multi trig sequential out simulating guitar strumming, UP and DOWN, with time from 0 to 10 secs
---- PARAMETERS
------ ALTERNATE (to alternate between DOWN and UP strumming)
------ DOWN sets the strum from 1 to 6
------ UP strums from 6 to 1
------ STRUM time, time differential between trigs, default 10 msecs, max 9.999 seconds
------ STRUM GLOBAL TRIG / TAP / TRIG OUT the main strum trig
------ 6 channel of strumming, hit directly to have strumming with less trigs
-------- for example if you wan to strum just 4 5 and 6, set to DOWN, and TAP on 4

-- PHASOR (Harmonic VCO) changes
---- BUG: don't try to update time for an empty set of KFs
---- BUG: don't try to change curr KF when empty set of KFs
---- BUG: don't try to update time on curr KF 0
---- BUG: change of the time  for KFsnow is regular (was advancing only by 0.01)

-- MASTER RECORDERs (all) + complex SIMPLER
---- reset timer on startup


v0.6.11 (2018-07-29)

-- DYNAMO (stereo compressor - expander - hard limiter - ducking device)
---- it's a second iteration on the compressor added to the Master recorder 2
---- all parameters can be monitored on the screen
---- there are 4 stereo meters running:
------ the first BLU is the original IN signal
------ the second GREEN is signal after PRE GAIN
------ the third PURPLE is the mangled signal
------ the fourth YELLOW is the signal after POST GAIN
------ all four meter represent RMS and PEAK, and they become RED if clipping
---- the center display shows the compressor curve, modified by THRESHOLD, RATIO and KNEE
---- Paramenters are
------ ATTACK (from 1 to 500 msecs)
------ RELEASE (from 1 to 500 msecs)
------ RATIO (from 0.1 to 1. for EXPANDING, from 1. to 20. for compression)
------ THRESHOLD (from -40dB to 0dB)
------ KNEE (from 0 to full size of the compressing side)
------ LOOKAHEAD for 0 to -500 msecs (used to compute compression on future data)
------ PRE-GAIN, boost the IN signal from (-40dB tp +20dB)
------ POST-GAIN, boost the OUT signal from (-40dB tp +20dB)
------ SHOW INFO hides the graphics and shows paramenter values
------ BYPASS TAP and TRIG IN to disable the effect
------ DUCKING MODE and TRIG IN to activate the compressor in DUCKING mode
------ LIMITER MODE and TRIG IN to activate the compressor in HARD LIMITER mode:
        all the signal over the THRESHOLD will have a THRESHOLD absolute value

-- STEREOCHORUS-TREMOLO
---- a simpler model for the chorus based on 12 delay lines (6 per channel)
---- same controls as the NYSTEREOCHORUS
---- added a tremolo effect
---- PARAMETERS
------ modulator waveshape
------ Modulator FREQUENCY (and CV in)
------ Modulation DEPTH (and CV in)
------ MOVEMENT set the influence of the secondary set of modulators (all sine) on the first modulators (+ CV in)
------ FEEDBACK, can be positive and negative (to recreate effect of White Chorus) (+ CV IN)
------ TREMOLO effect (it's a vca effect) , from 0 to 95%. (with CV in)
------ TREMOLO is stereo too
------ TREMOLO IN modulator LEFT and RIGHT (to associate a different external modulator to the TREMOLO)
------ MIX it's a DRY/WET pot (0 pos is all original signal, 12 'o clock is 50/50, full CW is all effect)
------ BOOST, is a gain stage to pump up after some phase cancellation
------ BYPASS let you set to OFF the effect on the fly, using the TRIG too
------ TEST guitar samples from "mareproduction" in https://freesound.org

-- FLIPPER (trigger and flip flop device)
---- it's a 2 part
---- 6 FLIP FLOPS;
---- for every FLIP FLOP:
------ TRIG IN
------ TAP with LIGHT status
------ GATE OUT (if light is ON, the GATE is at 10V level, otherwise is at 0v)
------ TRIG OUT: an immediate copy of the TRIG IN or TAP is sent as TRIG OUT
---- for every TRIG:
------ TRIG IN
------ TAP to TRIG
------ TRIG OUT: an immediate copy of the TRIG IN or TAP is sent as TRIG OUT

-- SLIM METER
---- a new SLIM meter, just the meter, with settings in contextual menu, just one UNIT


-- NYSTEREOCHORUS
---- optimizations


-- MASTER RECORDER 2
---- change the compressor from a dual mono model to a stereo compressor model
---- the compressor can work also with a single channel
---- change the compressor param ranges
------ attack from 1 to 20 msecs
------ release from 1 to 100 msecs
------ ratio from 0.5 (expansive) to 10.0
------ threshold from 0.01 to 1.0
---- stereo massager is active only if inL and inR are BOTH active


-- SCALA QUANTIZER
---- solved a crash on WIN10
---- support for -+4 octaves

-- ALL METERS
---- changed visualizaton curves


v0.6.10 (2018-07-25)

-- STEREOPHASER2
---- a low cost computation stereo phaser with 6 or 4 STAGEs of first or second ORDER

-- SCALA QUANTIZER
---- feature requests:
---- a new imported SCL file become immediatly the selected one
---- the menu is SORTED alphabetically NO CASE
---- menu items names are now composed with this formula "NAMEOFTHEFILE - COMMENTINTHEFILE"
    for example che "couperin.scl" file contains the comment "Couperin modified meantone"
    the resulting MENU ITEM will be "couperin.scl - Couperin modified meantone"


-- PHASOR (Harmonic VCO) changes
---- BUG: in release 6.9 I forgot to add back the trimmer for frequencies not in "Frequency Trimmers as FM inputs"
---- ADD four modes for the harmonics ratios (selectable via context menu):
    "standard tuning"
    "square of position"
    "cube of position"
    "square root of position"


-- NYSTEREOPHASER
---- optimizations: speed up internal calculations (around 45% better)



v0.6.9 (2018-07-23)

-- PHASOR (Harmonic VCO) changes
---- BUG: don't start animation with no frames
---- TOTAL TIME real time change when changing single KF Time: now you can DRAG edit the TOTAL time.
    Time will be compressed in all KFs
---- MIN TIME for single KF is now 0.01 secs
---- MIN TIME for next KF is now 0.01 secs
---- add LINEAR FM for single harmonics: activated with contextual menu "Frequency Trimmers as FM inputs"
---- add contextual menu command to "Load Current Frame To Screen"
---- add contextual menu command to "Save Screen To Current Frame"
---- add contextual menu command to add 1 10 100 KFs random based on MIN MAX established on the screen with
    harmonics 1 and 2 and with time between 0.01 and current "NEXT FK TIME" value:
    EXAMPLE do:
    a) DELETE ALL KFs
    b) context menu "Full Reset"
    c) use the MAGNITUDE of H1 to establish a START RANGE for  random
    d) use the MAGN of H2 to establish an END RANGE for  random (repeat with phase and frequencies if you want animate them)
    e) context menu "Add 10 Random KFs"

    at this point you have an animation of 10 random KFs based on the input data.
    If you repeat the action, remember to do a `context menu "Full Reset"` (because the range now are changed!)


-- MASTER RECORDER 2
---- removed the proto distort


v0.6.8 (2018-07-20)

-- PHASOR (Harmonic VCO)
---- My very naif take on additive synthesis, the tool could be used as teaching aid for fourier series
---- there are 16 oscillators organized as rotating vectors. with a visual representations of current Magnitude
        Frequency, Sign and Phase
---- there 3 panels:

----- the left TUNING/OUT panel
------- OUTPUT, GLOBAL or separated for ODD and EVEN harmonics. There is a gain control
------- base frequency (set to C2, but variable, just click and drag)
------- octave from -2 to +2 (CV controllable)
------- LINEAR FM (with CV)
------- EXPONENTIAL FM (with CV)
------- the standard CV control to drive the VCO

----- the center GRAPHIC panel
------- in the center there is a visual representation of the rotating vectors +
        the instanteous visualization of the audio wave created
------- many commands are in the contextual menu too (experiment with it!)
------- there are resets and classic waveshapes
------- from TOP
------- ROW 1: OUT of single oscillators
------- ROW 2: OUT of single low frequency oscillators (if in LOW POWER MODE will output ZERO)
------- ROW 3: frequency sign for the harmonic. the PHASOR can use negative frequencies too. click with right btn to invert
------- ROW 4: the MAGNITUDEs, can be dragged by hand, the RED LINE represent VALUE of 1.0. Can be dragged from -2 to +2
------- ROW 5 and 6: MAGNITUDE CV in and ATTENUATORS
------- ROW 7: PHASE for current harmonic, draggable, can be set from 0º to 360º
------- ROW 8: PHASE CV
------- ROW 9: FREQUENCY TRIM. Is a frequency deviation from correct "harmonicity"". From -20% to +20%
        clicking with right button is reset to ZERO position
------- ROW 10 and 11: FREQUENCY TRIM CV + ATTENUATOR.

----- the right ARTICULATION panele
------ here are element to give movements to the harmonics
------ TILT increases alterantively LOW or HIGH harmonics with CV and ATTENUVERTER
------ OFFSET move all harmonics up ot down (with CV and ATTENUVERTER)
------ KEYFRAME ANIMATOR
------ let you record the screen situation in keyframe steps and given a time transitions
        very complex enevelope could be created
------ controls and VIEWS are:
-------- DELETE ALL KF: delete all the stored keyframes
-------- KF COUNT shows the current count of stored keyframes
-------- TOTAL TIME is the full time of the animation expressed in seconds
-------- CURRENT KF, presents the current keyframe. Is editable
-------- CURR KF DEL when pressed ERASE the the CURRENT KF (and data related)
-------- CURR KF TIME is the time expressed in seconds to arrive to the CURRENT KF
         CURR KF TIME can be edited, and the edit is stored in the CURRENT KF
-------- NEXT KF TIME is the transition time assigned to the NEXT save keyframe
-------- SNAP KF ! add a NEW keyframe with time "NEXT KF TIME" to the animation
-------- RUN/HALT runs the animation (or HALT if running)
-------- PAUSE/CONT pauses the animation (and CONTINUE)
-------- RESET reset a running animation to the START condition
-------- LOOP, if active the animation runs forever


-- SOME optimizations in MasterRecorder2



v0.6.7 (2018-07-05)

-- DOPPLAB
---- it's a doppler simulator
---- click with right mousebutton to add point
---- click on points to move them
---- click on point with right button to remove it
------ PARAMETERS
-------- IN and OUT stereo mode
-------- ZOOM to scale the grid from 0.25x to 4x
---------- every single square in the grid represent 10 meters
-------- SOUND SOURCE SPEED is the base speed of the source moving on the path, is expressed in Km/h
-------- SPEED CV accept Voltages from 0 to 10v, the out is limited by the attenuator and summed to SOUND SOURCE SPEED
-------- START activates the sound source on the path resetting to the START position
-------- STOP-CONT can STOP and CONTINUE the source moving on the path
-------- RESET rest the source to the START position
-------- LOOP if ON the source will loop on the path
-------- PITCH SHIFT if OFF removes the pitch shift effect
-------- BINAURAL if OFF considers the 2 delay lines representing the ears as equivalent
-------- BINAURAL if ON intracranial delay is computed for evey position in space of the source
-------- VOLUME ATTEN if OFF removes the effect of the volume attenuation due to the distance source-listener
-------- SHOW INFO if ON shows informations about :
---------- complete path length
---------- istantaneous speed of the moving sound source
---------- traveled distance by the moving sound source
---------- distance of the source from the listener
---------- relative speed "moving sound source - listener"

-- MASTER RECORDER 2
---- add VCA + CV to control the STEREO MASSAGER
---- now Left slider is hidden when LFET-RIGHT LEVEL LOCK is ON
---- add a proto DISTORT
---- "Th"" (threshold) param goes from 0.0 to 2.0

-- CONST ADD MULT
---- add DIVISION out
---- "A / B" output is the division of A / B if B != 0. if A is missing, is 0 / B.

-- VECTOR MIXER
---- feature request: is stereo now (or can be used as 2 channels)


v0.6.6 (2018-06-26)
-- MASTER RECORDER 2
---- a more specialized version of the stereo recorder
---- added 2 full lenght METERS
---- added 2 volume SLIDERs for the 2 channels
---- volume SLIDERs go from 0.0 to 2.0
---- added MONITOR output to trace the audio being recorded
---- added TRIG OUT to sync more recorders
---- the switch for the AUTOSAVE is an ON-OFF button (if OFF a dialog for saving will be presented)
---- added a simple compressor
------ ON OFF compressor
------ Attack from 0 to 100 msecs
------ Release from 0 to 100 msecs
------ Ratio from 0.0001 to 10.0
------ Threshold from 0.0 to 1.0
---- added a simple STEREO MASSAGER
------ one knob, if default, no effect
---- added Left Right LEVEL LOCK ON OFF button: if ON the right slider will control BOTH volumes
---- added 2 ON OFF for PHASE INVERT of the channel

-- SCALA QUANTIZER
---- ADD extra 11 IN OUT quantizers
---- ADD bypass button
---- ADD CV control for OCTAVES

-- NYECHOecoeco
---- ADD time multiplier, now the minimum speed is 0.1 cm/sec
---- ADD CV control for the disc speed
---- ADD VCA for the CV control for the disc speed
---- ADD DUAL Echo for STEREO outputs

-- COMPLEX SIMPLER
---- CHANGE: the STOP will act as TOGGLE, so it's a STOP and CONTINUE trig/pulse/button


v0.6.5 (2018-06-18)
-- compatibility release for RACK 0.6.1


v0.6.4.1  2017-06-16
-- SCALA QUANTIZER
-- solved a crash for duplicate symbols in Scala Quantizer


v0.6.4  2017-04-14
-- DEEPNOTE
---- attempt to create a THX sound type generator
---- there 4 classes of frequencies
---- freq one is spread on 5 octeves
---- freq 2 on 6 octaves
---- freq 3 and4 on low mid and high
---- there are PAN animators and SPECTRUM animators (and AMPLI animators too)
---- this will consume on my MAC about 50% of the resources, so best use is to record it, alone...


-- EQUAL DIVISION QUANTIZER
---- ADD CV in for both N and X variables (of the "N th root of X")
---- REAL TIME change of the display to represent the OCTAVE and TUNING variations too
---- ADD Input and output 2, 3 and 4 to have microtonal chords based on the same scale
     (if you need more notes, just use another ED-QUANT)

-- SQUONK
---- feature request: change color for the case ONLY CV : from dark yellow to BLUE

-- CLOCK MULTIPLIER
-- XATTO TIME
-- CONST ADD MULT
---- corrected value skewing whne draggin and the screen is zoomed


v0.6.3  2017-04-08

-- EQUAL DIVISION QUANTIZER
---- inspired by discussions with Kent, Edward and Scott
        https://www.facebook.com/groups/vcvrack/permalink/171694843490668/
---- It is a grid create using the formula  "Nth root of X" where N is the first field and X the second field
---- You can use and REAL number, so you can have for example a scale  63.333ed1.6666  (63+1/3ed5/3)
---- both N and X fields are draggable editable
---- example N = 12 and X = 2 is the standard western 12th root of 2
---- or N = 25 and X = 5 gives you the Stockhausen's 25ed5 scale
---- the midi map mode, maps the midi notes (scaled 0.083333) to first 127 degree of the current scale
---- the pure quantize mode, quantize to the closest voltage of the grid
---- TUNING and OCTAVE are standard help for user for fine tuning


-- SCALA QUANTIZER
---- now support all types of SCL types (removed the boundary on perfect final RATIO (like 2/1 ro 3/1 ro 5/1 ))

-- CLOCK MULTIPLIER
---- ADDED autosync after a RESET (at first computed time)


v0.6.2  2017-03-30

-- SPECTRAL
---- a real time spectrograph wanna be,
---- is using very very little of CPU
---- explore different visualizations and windowing functions using the contextual menu

-- QUAD SIMPLER
---- bug solved: duplication and audio file persistance
---- added DRAG and DROP for audio files

-- COMPLEX SIMPLER
---- bug solved: duplication and audio file persistance
---- added DRAG and DROP for audio files

-- 4DCBLOCK
---- solved a crosstalk bug (some cleaning for the 4 dc filters!)

-- CLOCK MULTIPLIER
---- ADDED reset by trig or by TAP to align all the subclocks

-- SCALA QUANTIZER
---- added MIDI MAP mode

-- MODEL277
---- protect from init to time ZERO

v0.6.1  2017-03-29

-- QUAD SIMPLER SLICER QUANTIZER
---- 4 quantizer
---- 10v is divided from 1 to 99 slices, and IN VOLTAGE is quantized to the closest
---- perfect to use with simpler: load a LOOP and set to 16 or 8 slices
---- user SOU as Voltage source

-- QUAD SIMPLER
---- CRASH: in version 0.6.0 the load button is incompatible: removed
---- LOADING is via CONTEXT MENU
---- ADDED START-CV parameter (to set the start using CV 0V start, 10V end)
---- protect from opening EMTY files

-- COMPLEX SIMPLER
---- protect from opening EMPTY files

-- SCALA QUANTIZER
---- protect from opening wrong SCL files


v0.6.0.0  2017-03-08

-- 8 ATTACK DECAY
---- 8 AD EG with :
---- Attack control
---- Decay control
---- LINEAR - EXPONENTIAL control
---- SCALE control (with inversion)
---- TAP to single TRIG
---- IN PULSE to SINGLE TRIG
---- LOOPED MODE ON / OFF
---- End OF RISE (attack) PULSE OUT and LED
---- END of CYCLE (decay) PULSE OUT and LED
---- VCA IN
---- VCA OUT
---- Envelope signal OUT
---- Led signal out
---- UNITY MIX button (if ON, the EG value will be summed and presented to the total OUT)
----
---- GLOBAL CONTROLS :
---- ATTACK for all 8  + CV IN for all 8
---- DECAY for all 8  + CV IN for all 8
---- LIN-EXP for all 8
---- SCALE for all 8
---- VCA IN global
---- VCA OUT global
---- UNITY MIXER OUTPUT

-- CLOCK MULTIPLIER
---- CLK IN accept a clock (or a LFO )
---- RESET button will reset the TIME computer
---- the GREEN LED indicates that the TIME computer is in a stable state
---- CLK OUT 1, CLK OUT 2 and CLK OUT 3 are the same
---- the RED display is the time multiplier from 0.01 to 99.9999
---- is a DRAGGABLE display for precise value inputs
---- the OUTPUT put the multiplied CLOCK out


-- CONST ADD MULT
---- is a QUAD PRECISE constant, ADDER, MULTIPLIER.
---- "A IN" is OPERATOR 1
---- "B IN" is OPERATOR 2
---- "B OUT" is a CHAIn out of the OPERATOR 2
---- the DISPLAY is thB value and can be set precisely using MOUSE drag
---- the MOUSE dragging is positional, the more you are on the left, the more faster the value is updated
---- B value can be set precisely til 0.0001 steps
---- right clik will reset to 0
---- "A + B" output is the sum of A + B. if A is missing, is 0 + B
---- "A x B"output is the product of A x B. if A is missing, is 0 x B

-- XATTO TIME
---- defaul gain for IN2 to ZERO (feature request)

-- SCALA QUANTIZER
---- set octave and tuning to ZERO on reset (bug)
---- move all the possible UI operations out of the engine thread
---- bug importing non regular scl files (colundi is not octave based)
---- bug remove USELESS duplicate steps
---- bug solved crash change scala during execution

-- SOU UTILS
---- add overflow to both ASR
---- ASR 2 is clocked by ASR 1 in CLOCK if no clock in ASR2 clock in

-- DISSONANTVERB & PLATEVERB
---- corrected a nasty bug that was crashing RACK reopening a patch

-- NY1METER
---- smoother PEAK descending

-- NY2METER
---- smoother PEAK descending


v0.5.13.0  2017-01-22

-- XATTO TIME (4 delays)
---- 4 delays
---- every delay can accept audio or CV
---- delay from 0.01 msecs to 9999.99 msecs
---- click and drag to set PRECISE timing
---- no filter IN or OUT
---- there are 2 IN, the IN2 is controlled by an attenenverter (to create feedbacks)
---- every delay is clockable and tempo is computed with the tempo detector
---- the detected tempo is multiplied by a factor from 1 to 99

-- SCALA QUANTIZER
---- based on SCL files (scala files)
---- documentation here: http://www.huygens-fokker.org/scala/
---- QUANTIZERS are selected using contextual menu
---- new SCALA QUANTIZERS can be added using the contextual menu "ADD NEW SCL File..."
---- the scales are stored into the Rack/plugins/nysthi/res/microtuning/scala_scales/ directory
---- feel free to add and remove as needed
---- SCL are loaded at startutp
---- the GREEN DISPLAY shows:
------ ROW 1: the octave and the degree in the octave: for example "3-7" means degree 7 of octave 3
------ ROW 2: the octava and the original ratio or value in the original file
------ ROW 3: current value in Hz assuming C4 i     s Hz 261.63
------ ROW 4: curret quantized voltage associated to quantization
---- the OCTAVE DISPLAY DRAGGABLE let's you move the octave from -2 to +2 for the quantization
---- the TUNE DISPLAY DRAGGABLE let's you move from -.99 to +.99 the current voltage value


-- 4DCBLOCK
---- it is possible to set the HP frequency from PRESETs in the contextual menu (5, 10, 15, 20  30 Hz)

-- SQUONK
---- added RED mode: end of sequence marker

-- COMPLEX SIMPLER
---- added EOC (End of Cycle) pulse: triggered when the currentime hits the END
---- added visual timer representing current time in recording mode and length of the sample in play mode

-- QUAD SIMPLER
---- added 4 EOC (End of Cycle) pulse: triggered when the currentime hits the END

-- TIMEX
---- corrected name in the MENU, should be TIMEX (not timeoftheday)

v0.5.12.0  2017-01-21

-- DISSONANTVERB
---- it's a modification of the PLATEVERB inserting 2 pitchshifter in the feedback loop
---- the effect is quite dramatic (and soundtrackable)
----- DISSONACE1 controls the shifting of the first DISSONATOR (CV controllable)
----- DISSONACE1 MIX controls balance between original signal and shifted signal
----- DISSONACE2 controls the shifting of the second DISSONATOR (CV controllable)
----- DISSONACE2 MIX controls balance between original signal and shifted signal
------- DISSONACE1 and DISSONACE2 have different curves: smoother the 1, larger range the 2
----- all the other parameters are PLATEVERB equivalent

-- PLATEVERB
---- it's a new reverb based on the famous Dattorro paper. Was tweaked to adapt it to every samplerate and to add
---- Early reflections
---- tail is very smooth!
---- There is no control for the roomsize, you need to work on the decay
------ PARAMS
------ EARLY REFLECTIONS MIX: ER are 2 8 tap fractional delay lines with 16 differents times. the mix is a
balance between incoming signal and the reflections
------ PREDELAY from 0 tp 400 msecs
------ PREDELAY MIX, balance from previous stage and the delayed signal
------ BANDWIDTH is the frequency passed
------ DECAY the control of the tail (feedback)
------ DAMPING
------ WET-DRY balance between input and effect
------ BOOST from 0 to 2.0 to push up or down the signal if needed
------ FREEZE (triggable too) freeze the effect with the infinite decay

-- TIMEX
---- a CLOCK using the standard unix time functions and representing current HOUR (of your computer)
---- data represented and outputs:
------ current HOUR + RAMP representing current HOUR in a day in 0-10v scale + PULSE when DAY changes
------ current MINUTE + RAMP representing current MINUTE in a HOUR in 0-10v scale + PULSE when HOUR changes
------ current SECOND + RAMP representing current SECOND in a MINUTE in 0-10v scale + PULSE when MINUTE changes
------ current 1/10 of SECOND + RAMP representing current 1/10 in a SECOND in 0-10v scale + PULSE when SECOND changes
------ current 1/100 of SECOND + RAMP representing current 1/100 in 1/10 in 0-10v scale + PULSE when 1/10 of SECOND changes
---- ALARMS:
---- are 2 equivalent
------ to set the alarm, click and drag on the display
------ to ARM the ALARM, press the ON-OFF button
------ when current time HITS the ALARM set, a PULSE is generated and a GATE activated, and the ALARM is set to OFF
---- COUNTERS:
---- are 2 equivalent
------ to set the counter, click and drag on the TARGET display
------ to activate the counter, press the ON-OFF button
------ to run the counter, connect a PULSE to the PULSE IN, if ON the counter will start to COUNT
------ if the COUNTER is ON and COUNTER hits the TARGET a PULSE is GENERATE from PULSE OUT and the COUNT is set to 0

-- 4DCB
---- a 4 times DC BLOCK filter, current sample rate aware
---- needed to avoid unwanted Direct Current build up a the end of a module

-- complex DAHD
---- added envelope chain IN, to have complex chained envelopes

-- SINGLE METER
---- just a new meter: someone asked for a longer one. Same commands (via contextual menu) (feature request)

-- LFOMULTIPHASE
---- increased resolution from 0.00001 Hz to half of current sampling rate (beware, it is always an LFO
---- and aliasing is waiting to appear!)
---- added the ability to set the frequency via TEXT field, the computation is istantaneous
---- frequency can be expressed as BPM too, for example you could write "120 bpm" and you should get 2Hz
---- can be expressed as Quarter Per Minute , for example you could write "120 qpm" and you  get 2Hz
---- can be expressed as Eights Per Minute , for example you could write "120 epm" and you  get 4Hz
---- can be expressed as Sixteenths Per Minute , for example you could write "120 spm" and you  get 8Hz
---- added SYNC, to reset teh phase of the LFO (to do multiple LFO synchronization)

-- HOT TUNA
---- Improved visibility of the screen (frequency is fully visible) (feature request)
---- removed the annoying NaN appearing in the F2V part (sometimes...) (thanks Martin L)

-- MASTER RECORDER
---- added timer to check recording time (feature request)

-- MULTITRACK RECORDER
---- added timer to check recording time (feature request)



v0.5.11.0  2017-12-26

-- DUALFEEDBACKECHO
-- 2 echos almost the same, the only differences are minimum maximum time
---- ECHO 1 goes from 0.05 msecs to 2000 msecs
---- ECHO 2 goes from 0.01 msecs to 200 msecs
---- TIME is the time control
---- CV is summed to TIME (if present)
---- TRIGTIME if used, overrides TIME and CV. Is a time computer, calculates timing of the incoming pulses
      and synchronized the echo
---- You can drive also with a VCO in input (or an LFO, of course)
---- FEEDBACK is amount of the ECHO that is summed back to top of the CHAIN
---  OUT is the OUT...


-- NYECHOecoeco
---- more flexibilty to time: we are virtual we can do what we want :)
---- DISC time from SPEED POT is now from 1 cm/s to 100 cm/s
---- added inertial response
---- EVERY PLAY HEAD can move till next previous head influence area (+-49% of the current position)
---- added TAP and TRIG to tempo (you can trig till 4000 cm/s )
---- when in SYNC
---- added PANIC button (to clear the buffer immediatly :D :D )
---- added more control for inner infinite values
---- added MAGNETIZATION coefficient: represents the inability of the ERASE HEAD to do a complete ERASE
 if MAGNETIZATION is high you'll get faint repetition also when the ERASE HEAD is active


-- LFO MULTIPHASE
---- for some mysterious reasons the TAP to TEMPO feature was commented out...


v0.5.10.0  2017-12-21
-- NYECHOECOECO
---- a virtual BINSON Echorec homage, with 6 play HEADS
---- PARAMETERS:
----- SPEED to trim the speed of the disc (the speed is expressed in CM per second)
----- a SPEED of about 12 cm/s is exactly 1 round per second
----- EVERY PLAY HEAD can be activated by BUTTON (on the HEAD) or by TRIG
----- EVERY PLAY HEAD has a trimming function (to virtual move the headform -20% to +20% around the disc)
----- EVERY HEAD has a display for the current delay
----- EVERY HEAD has a volume (for the delay mixed)
----- EVERY HEAD has a TAP out TAP in (so you can process a delayed signal and insert it back in the chain)
----- THE SWELL is activated deactivating the ERASE HEAD
----- THE SWELL pot controls from ECHO to infinite feedback (beware)
----- DRY - WET is a mix from original input signal and the processed signal
----- INPUT and OUTPUT have both a gain control
----- INPUT has a simulated OCCHIO magico: if the 2 wings connect in the center, signal is clipping


-- COMPLEX DAHD
---- add a second VCA to process in stereo

v0.5.9.0  2017-12-18
-- SUPPORT for RACK 0.5.1

-- DX7ENVELOPE
---- emulation of the 4 rates 4 levels DX7 operator envelope
---- values are like in DX7 from 0 to 1
---- rates are from super SLOW to hyper FAST
---- levels are from 0 to MAX
---- added SCALE (from -1 to 1) and OFFSET (-10 to +10)
---- 2 inner VCA to control Audio Stereo signals
---- TRIG (Attack Release) mode or GATED (level 1, level 2 level3SUSTAIN, level 4)
---- TRIG CHAIN to control more DXEnvelopes with same trig or gate signal
---- TRIG GATE button
---- LED to signal the trig or gate status

-- QUAD PANNER
---- added chaining for cascading QUAD PANNERs (and remove cluttering from and to mixers)

v0.5.8.0  2017-12-12
-- QUAD PANNER
---- is an old style sound source placement using a quadraphonic system
---- implements some of the functionalities of a single channel of the Buchla 227e
---- position of the source can be established with MOUSE, or by X and Y Position
---- or by AZIMUTH and MAGNITUDE, or by SWIRL (a la 227e)
---- the SWIRL is internal LFO that rotates the sound source for teh 4 outputs, with RATE
---- and AMPLI (is the MAGNITUDE, again...)
---- X & Y positioning takes precendece on SWIRL that takes precendece on setting AZIMUTH (and MAGNITUDE) and on
---- the PANNING is LINEAR and becomes EQUAL POWER PANNING activating the FLAG
---- Activating the flag INFINITE DISTANCE CENTER, the center becomes an AUDIO BLACK HOLE
---- the audio disappear if the magnitude approximates to ZERO


-- HOTTUNA
----- FREQ TO VOLTAGE now tuned on FUNDAMENTALS VCOs (unison tracking perfect pitch)


v0.5.7.0  2017-12-12

-- VECTOR MIXER
---- is a mixer working in a 2d plane. the "joystick" position could be set by MOUSE, by X & Y position
---- and by AZIMUTH & MAGNITUDE. X & Y has precedence on AZI & MAGN that has precedence on MOUSE.
---- INPUT could be SIGNAL AUDIO or CV. The vector mixer is highly inspired to joystick and
---- vector functions of the Prophet VS.
---- Combined with JW XYPAd can emulate the 2D Vector Envelope too

-- SQUONK
---- BUG: missing repetition first step if chained SOLVED

-- HOTTUNA
---- FEATURE REQUEST: ADD FREQUENCY TO VOLTAGE with signal IN
---- FEATURE REQUEST: WHEN checking VOLTAGES now is not doing the animation (avoid waste of time for users)

-- COMPLEX SIMPLER
---- BUG at restart if in ONESHOT mode was cycling (CORRECTED)
---- FEATURE REQUEST: showing original file name in contextual menu

-- QUAD SIMPLER
---- FEATURE REQUEST: showing original file names in contextual menu

-- SOU UTILS
---- FEATURE REQUEST: the OFFSETTER will output a fixed or modulated voltage without an input too

-- NYSTEREOCHORUS
---- ADDED A DCBLOCK filter


v0.5.6.0  2017-12-11

-- SOU UTILS:
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


-- SOYMODELSOU MODs:
---- ADD PULSE in to the FRV1 section. for every pulse a new radom is generated.
------ A timing function is computed in realtime to have correct smoothing
---- ADD PROBABILTY to HAVE pulse, from 0 to 1
---- ADD PROBABILTY CV IN
---- ADD GATE OUT to FRV1. The gate function works like that: signal is gated till
------ the smoothing function is up a level decided by the probability setting

---- ADD PULSE in to the FRV2 section. for every pulse a new radom is generated.
------ A timing function is computed in realtime to have correct smoothing
---- ADD PROBABILTY to HAVE pulse, from 0 to 1
---- ADD PROBABILTY CV IN
---- ADD GATE OUT to FRV2. The gate function works like that: signal is gated till
------ the smoothing function is up a level decided by the probability setting

---- ADD a section with 3 FLIP-FLOPs for more GATING divertimento


-- SQUONK :
---- BUG for last chained step not triggering
---- BUG reset now set to the correct position
---- the CV now is scaled 1/12 V (with modf) to track steps like a keyboard using CV (0.08333 VOLT steps)

-- NYENVFOLLOWER :
---- SCALE from -5 to +5
---- OFFSET from -10 to +10


v0.5.4.1  2017-12-05
-- SOYMODELSOU
ADD: new extra selection for QRV, if DATA SET REPEATABLE is OFF, is guaranteed that all data selected will
be all different (no repeated quantized steps)
BUG: the SOU was not starting if his buddy "HOTTUNA" was not present... ;) Now, is starting alone
BUG: the QRV section had a WRONG count on N+1 when POT was on 1 (you didn't notice... but I'm picky)
BUG: the SRV SKEW function was overflowing if modulated

v0.5.4  2017-12-03
-- THE SQUONK
it's a PROGRAMMER, STAGE sequencer, Sampler TRIGGER, freely inspired to Serge TKB
is 12 steps with 11 lines of programming

line 1: TRIG IN: will select the stage triggered
line 2: STAGE: is the stage selector by button. when in sequencer mode the current step will light up
line 3: 5X: voltage multiplier for A B C D E channels
line 4: A: CV channel from 0 to 2 volts
line 5: B: CV channel from 0 to 2 volts
line 6: C: CV channel from 0 to 2 volts
line 7: D: CV channel from -1 to 1 volts
line 8: E: CV channel from -1 to 1 volts
line 9: MODE: TRIG mode; if bright yellow, CV and TRIG out, if dark yellow, only CV out, if black step is jumped
line 10: REP: if the sequencer is clocked will retrig the step from 1 to 8 times (subdivisions) (ratcheting)
line 11: TRIG OUT: single PULSE out when the stage is selected

SEL knob: will select the current stage
SEL CV input: selection of stage using CV (0 -> 10v)
CLK IN CLK OUT: to clock the sequencer (and output the same clock to other devices)
UP TRIG and BUTTON: if ON the sequence will go UP (normally is DOWN)
RND btn: if light up the next stage is randomized

OUTS A B C D E are the CV outs of the sequencer
ROT knob, from -5 to +5, is the number of steps the yellow channel will rotate jump and rotate  if in sequencer mode
LAST trig out: PULSE out when last step is reached
TRIG (global): current stage TRIG out (with repetitions if any)
CHAIN A B C D E  and CHAIN TRIG are useful when chaining many SQUONKs (to have just one connection for the CV and TRIGs)

START STOP RESET: sequencer status controls by BUTTON or by TRIG

RANDOMIZE ALL: must be pressed with COMMAND KEY (too dangerous!)

-- SOYMODELSOU
---- IS an imitation of the FLUCTUATING, QUANTIZED and STORED voltages sections of the Buchla 266 Source of Uncertainty
---- FLUCTUATING RANDOM VOLTAGES 1
control TIME via CV and KNOB: from 0.05 to 50 sampling per seconds
OUTS: SMOOTH, HARD (the sampled voltage),  PULSE ( when HARD > 0.5)

---- FLUCTUATING RANDOM VOLTAGES 2
control TIME via CV and KNOB from 0.05 to 50 sampling per seconds
has a different smoothing function that can be controlled via CV
OUTS: SMOOTH, HARD (the sampled voltage),  PULSE (when HARD > 0.5)

---- QUANTIZED RANDOM VOLTAGES
2 sections: 2^n and n+1, where N is form 1 to 6 (established via CV and KNOB)
the n+1 distribution is a Triangular distribution (like throwing 2 dice)

n+1 are in 1V jumps
2^n are in 1/12V jumps

---- STORED RANDOM VOLTAGES
Random with SKEWING function (CV controllable) to have more events in LOW MID or HIGH ranges

-- HOTUNA
---- add TUNE "A = " param (so you can tune to "432Hz" now")
---- addeed TUNE reference OSCILLATOR
---- add DO RE MI mode
---- INSTABILYT light (the background will become lighed RED if reading is invalid)
---- SMOOTHER come back to ZERO of the needle
---- IF FREQ not recognized, now goes to ZERO




v0.5.2.1 2017-11-27
-- more WORKAROUND (to correct vcv files)
---- change
"plugin": "NYSTHI",
"model": "HIVerb",
to:
"plugin": "NYSTHI",
"model": "HiVerb",

---- change
"plugin": "NYSTHI",
"model": "Model 277",
to:
"plugin": "NYSTHI",
"model": "Model277",


-- HOTUNA
---- the VU meter will give info about the note, the big black one text is the
---- frequency (expressed as MIDINOTE TAG) we are targeting;
---- starts to become GREEN when is at less than 4 % deviation
---- and RED when there is less than 0.5% of deviation

---- the TUNER works on SIGNALs (vco inputs, or any signal you want)
---- and with VOLTAGES (translated interanally in frequencies) + the offset given by the OCTAVE
---- POT (goes from -2 to +2 octaves)

---- the IN SIGNAL input has priority (if both are used)



v0.5.1 2017-11-26
- WORKAROUND for mismatched names in VCV files 0.4.0 to 0.5.0 (sorry for the problems ;)
-- substitute all the occurrences of "nysthi" with "NYSTHI"
-- change
"plugin": "NYSTHI",
"model": "TwistedVerb",
to:
"plugin": "NYSTHI",
"model": "TwistedMVerb",

"plugin": "NYSTHI",
"model": "Reverb",
to:
"plugin": "NYSTHI",
"model": "MVerb",

- DICA 33
---  filter module...
-- very unstable, but usable

- SUPERSIMPLER
-- bug: not saving the jog start and end point correctly. RESOLVED

- QUADSIMPLER
-- bug: FM IN was working only for SAMPLE1. RESOLVED
-- bug: name should be QUADSIMPLER. RESOLVED

- MVERB
-- bug: nasty crash on low memory. RESOLVED

v0.5.0 2017-11-19
- QUADSIMPLER
    - the son of SIMPLER, is a multi sample player with integrated stereo mixer
    - 4 equivalent sample player with
        LOAD sample button (load WAV or AIFF, PCM)
        GATE mode (when in GATE mode the sample will play when the signal is HIGH and STOP when TRIG is LOW)
        1-SHOT
        TRIG BTN (to start a sample manually, or GATE IT)
        TRIG IN (to start a sample with a trig in signal or used in GATE mode)
        STOP IN (a trign signal will stop the sample)
        START will move the start point of the sample
        FM CTRL from -2 to +2, by default is 1 and the input in FMIN/CV will be 1V/oct
        FMIN/CV (to modulate frequency)
        SPEED setting the base SPEED of the sample
        PAN to place the sample in the stereo field
        VOL volume of the smaple
        OUT the direct OUT of the sample player

    all the paramenters are repeated 4 times

    GLOBAL parameters is CHAIN IN of another mixer that will be summed to Channel L and R
    the idea is to have multiple QuadSimpler to have a BIG bank of samples


- MASTER-RECODER
    - correct bug: a nasty crash saving files without extensions

- MULTITRACK
    - correct bug: a nasty crash saving files without extensions

- SIMPLER
    - protect simpler from opening compressed WAV format (only PCM 16 and 24 bits are accepted)
    - correct bug: a nasty crash saving files without extensions
    - the LFO is morphable (the lights give you the idea)
    - add ANTI-CLICK param, filter to remove clicks in sample start and ends points
    - the ANTI CLICK goes from 0 to 100 ms
    - correct bug of removed FM input DONE
    - correct bug of removed CV START input DONE
    - add GATED mode to the TRIG: if GATED on, the sample will stop when TRIG/GATE is off
    - add the ability to open AIFF files (PCM)

- LFO MULTIPHASE
    - add morphing ability to the waveshapes
    - morphing is activate via "discrete - morph" switch
    - morphing is modulable via CV input and controllable via waveshape selector and modulation index

- LOGIC
    - IS BACK! .... :D
    - streamlined version, and color codes... (white sockets, inputs, black sockets, outputs)


v0.4.12 2017-11-14
- SIMPLER (the NYSTHIATOR fortunate son)
    - debug Sample rate change
    - debug a permission problem saving files
    - added OCTAVE parameter
    - CV for the START POINT

v0.4.11 2017-11-13
- complex DAHD Envelope (DelayAttackHoldDecay Envelope)
    -   added BUSY command (the DAHD will react to trigs only in STABLE state)
    -   added ZERO command (the DAHD will react to trig starting always with at ZERO and not
        from the current ENV point)

- SIMPLER (the NYSTHIATOR fortunate son)
    - It's a sampler with some great features
    - OPENS and SAVES WAV files (via context menu)
    - can record stereo samples usig TRIG (and TAP TRIG)
    - SPEED can control from -2x to +2x (default is 1x ;) )
    - SPEED FINE is fine control on speed
    - FM IN is controlled via MODINDEX
    - CV is 1V/oct input
    - the inner modulator, can do FM too,
    - can choose wave type
    - FREQUENCY and MODINDEX
    - the SAMPLE could be cycled or ONE SHOT
    - TRIG START (and TAP) will start the sample for the START point
    - TRIG STOP (and TAP) will stop the playing (cycling or not)
    - SAMPLE START controls the START point of playing
    - SAMPLE END controls the END point of playing
    - ZOOM is just a WAVE display zoomer


v0.4.10 2017-11-12
- AD Envelope (AttackDecay Envelope)
	A standard Envelope with some 281 features
		controls:
		ATTACK (timing attack from 0 to 10 secs)
		ATTACK CV (accept also negative values like, will be subtracted form the main value)
		DECAY (timing decay from 0 to 10 secs)
		DECAY CV 
		LIN-EXP curve modifier, from linar to eponential
		SCALE can scale Envelope for -2x to 2x (default to -1) (is used to invert the envelope)
		TRIG BTN to start the envelope manually
		TRIG IN accept trig to start envelope
		LOOP button to have a cyclable AD
		EOC (End of Cycle) out: triggers out when the Envelope reach the stable phase
		ENV LEVEL LED: metering the signal
		ENV OUT: the signal to be used
		
- complex DAHD Envelope (DelayAttackHoldDecay Envelope)
	an envelope with 2 stage with delays
		controls:
		DELAY (timing delay from 0 to 10 secs) is the time after the trig and before the Attach stage
		DELAY CV (CV for the DELAY)
		ATTACK (timing attack from 0 to 10 secs)
		ATTACK CV (accept also negative values like, will be subtracted form the main value)
		HOLD (timing from 0 to 10 secs) Holds 1 till the the Decay stage is reached
		HOLD CV (CV for the HOLD)
		DECAY (timing decay from 0 to 10 secs)
		DECAY CV (CV for the HOLD)
		LIN-EXP curve modifier, from linar to eponential
		SCALE can scale Envelope for -2x to 2x (default to -1) (is used to invert the envelope)
		SCALE CV (CV for SCALE)
		TRIG BTN to start the envelope manually
		TRIG IN accept trig to start envelope
		TRIG OUT aoutput a trigger, when a trig is received, or the button is pressed (to make chains)
		LOOP button to have a cyclable DAHD
		LOOP TRIG IN the LOOP mode can be activated using a trig
		HANG button to have the DAHD stopped in the HOLD max value status indefinetively
		HANG TRIG IN the HANG mode activated using a trig
		VCA IN OUT, a simple insert to get a signal already amplified using the DAHD
		ENV OUT LED the metering of current status
		ENV OUT the envelope signal

		END OF STAGE TRIGGERS
		EOD (End of Delay) out: triggers out when the Envelope reach the ATTACK phase
		EOR (End of Rise) out: triggers out when the Envelope reach the HOLD phase
		EOC (End of Hold) out: triggers out when the Envelope reach the DECAY phase
		EOC (End of Cycle) out: triggers out when the Envelope reach the STABLE phase
		

v0.4.9 2017-11-09
- DUALMETER
	to control clipping
	the timing for the rms and peakhold can be changed using the contextual menu

- NYSTEREOCHORUS
	smoothed some inner control
	add BYPASS and BYPASS with TRIG to

- NYSTEREOPHASER
	add BYPASS and BYPASS with TRIG to

- MASTER RECORDER
	add save in PCM 24bit mode
	via contextual menu 

- MULTITRACK
	add save in PCM 24bit mode
	via contextual menu 


v0.4.8 2017-11-07
- MULTITRACK (MULTI-TRACK RECORDER)
	a digital recorder working on 4 or 8 channels
	- 4 ot 8 channels input
	- controls:
		ch1 to ch8
		START BUTTON
		TRIG IN START INPUT
		TRIG OUT START (to chain and sync more MULTITRACKs)
		STOP BUTTON
		TRIG IN STOP INPUT
		TRIG OUT STOP
		SWITCH between "AUTOSAVE" and "CHOOSE FILE"
			if in AUTOSAVE mode, pressing START a WAV file is automatically 
			created in the RACK directory (same level as RACK)
			if in "CHOOSE FILE" mode a SAVE FILE DIALOG BOX will be presented
			letting you to choose the recording destination

			when in "CHOOSE FILE" mode the TRIG START INPUT is INACTIVE

		SWITCH between "4-TRACKS" and "8-TRACKS"


v0.4.7 2017-11-06

- MASTER RECORDER
	a new module for performance taping
	- is a 2 channel recorder, records at the current frequency of the system
	- contains 
		2 INPUTS
		1 START BUTTON
		1 TRIG START INPUT
		1 STOP BUTTON
		1 TRIG STOP BUTTON
		1 SWITCH between "AUTOSAVE" and "CHOOSE FILE"

			if in AUTOSAVE mode, pressing START a WAV file is automatically 
			created in the RACK directory (same level as RACK)
			
			if in "CHOOSE FILE" mode a SAVE FILE DIALOG BOX will be presented
			letting you to choose the recording destination

			when in "CHOOSE FILE" mode the TRIG START INPUT is INACTIVE
	


v0.4.0F 2017-11-01

- LFOMULTIPHASE
    bug: corrected tracking when FM IN is fully CW
    UI: bigger TAP button

- NYENVFOLLOWER
    tweaks: changed some internal time to get more flat envelopes


v0.4.0E 2017-10-30

- NYENVFOLLOWER
	bug: the OSZI now is correctly ON when started
 	added a SMOOTHING parameter (should smooth more the transients)

- LFOMULTIPHASE
	a simple LFO with:
		A) 4 waveshapes
		B) UNIPOLAR BIPOLAR mode (0 to 10v or -5v to 5v)
		C) TAP button to transform TAP to frequencyv
		D) TRIG to transform TRIG to frequency
		E) Main FREQUENCY for 0 to 10 Hz
		F) Frequency multiplier x1 and x10
		G) FREQUENCY FINE (to move into one octave)
		H) FM IN in pot to MAX is 1v/OCT
		I) PULSE WIDTH control
		J) PULSE WIDTH CV IN
		K) OUTPUTs with 0°, 45°, 90°, 135°, 180°, 225°, 270°, 315° phase displace
		L) FREE PHASE out with PHASE controllable from 0 to 360°
		M) FREE PHASE MOD is cv control for the FREE PHASE


v0.4.0D 2017-10-24

- some little restyling (all the outputs are black)

- NYSTEREOPHASER 
	added full stereo input

- SURVEILLANCE
	added switch to have 2 ranges 
		A) from -5v to +5v
		B) from 0v to +10v

- NYSTEREOCHORUS
	new module,a stereo chorus with some nice new params

- DUALSIGNALDELAYER (aks 2D)
	dual delay from 0 to 2000 msecs
	both delays are CV controllable

- NYENVFOLLOWER
	a classic Envelope Follower with :
	
		A) GAIN IN (multiply the incoming signal form 1 to 10)
		B) ATTACK time (from 0.5 to 250 msecs)
		C) RELEASE time (from 0.5 to 250 msecs)
		D) SCALE multiply the signal for -20v to 20v
		E) OFFSET add to the signal from (-20v to 20v)
		F) DELAY ENV delays the generated signal from 0 to 200msecs
		G) ENVELOPE OUT the generated signal
		H) DELAY SIGNAL delays the original signal from 0 to 200 msecs
		I) SIGNAL OUT the original signal in, shifted by DELAY SIGNAL
		K) OSZI (oscilloskope) ON/OFF button (to spare cpu time!)
		L) SCALE gain of the signal and time
		

v0.4.0C 2017-10-24

- NYSTEREOPHASER
	debuggin nasty nysthi noise (thanks Ivan!)
	added 4 different algorithms
	debbugged light show
	added 4 waveshapes for inner vco

- SURVEILLANCE
	new module: one control to send 10 different voltages
	the main pot goes from -5 to +5
	all the outs are controlled by attuenverters

v0.4.0D 2017-10-24

- some little restyling (all the outputs are black)

- NYSTEREOPHASER 
	added full stereo input

- SURVEILLANCE
	added switch to have 2 ranges 
		A) from -5v to +5v
		B) from 0v to +10v

- NYSTEREOCHORUS
	new module,a stereo chorus with some nice new params

- DUALSIGNALDELAYER (aks 2D)
	dual delay from 0 to 2000 msecs
	both delays are CV controllable

- NYENVFOLLOWER
	a classic Envelope Follower with :
	
		A) GAIN IN (multiply the incoming signal form 1 to 10)
		B) ATTACK time (from 0.5 to 250 msecs)
		C) RELEASE time (from 0.5 to 250 msecs)
		D) SCALE multiply the signal for -20v to 20v
		E) OFFSET add to the signal from (-20v to 20v)
		F) DELAY ENV delays the generated signal from 0 to 200msecs
		G) ENVELOPE OUT the generated signal
		H) DELAY SIGNAL delays the original signal from 0 to 200 msecs
		I) SIGNAL OUT the original signal in, shifted by DELAY SIGNAL
		K) OSZI (oscilloskope) ON/OFF button (to spare cpu time!)
		L) SCALE gain of the signal and time
		

v0.4.0C 2017-10-24

- NYSTEREOPHASER
	debuggin nasty nysthi noise (thanks Ivan!)
	added 4 different algorithms
	debbugged light show
	added 4 waveshapes for inner vco

- SURVEILLANCE
	new module: one control to send 10 different voltages
	the main pot goes from -5 to +5
	all the outs are controlled by attuenverters


v0.4.0B 2017-10-22

- LOGIC 
	removed module (obsolete)

- MVERB 
	now is 1 to 1 equivalent to the mVerb

- HI-VERB
	removed clear during room resize

- TWISTEDMVERB
	removed clear during room resize

- MODEL277
	removed filters from feedback paths
	removed smoothers on parameters changes
	timing is now the same as the Buchal 277 from 5 to 200 msecs
	added 10x time multiplier, bringing the time from 50 to 2000 msecs
	solved a bug on feeback paths 3 and 4

- NYSTEREOPHASER
	added new stero phaser, original design, based on 4th orders Allpasses
	

v0.4.0 2017-10-15 FIRST RELEASE

- MVERB
	a VCV RACK port of the mverb
	https://github.com/martineastwood/mverb

- HI-VERB
	a mutation of the MVERB using HIPASS filtering

- TWISTEDMVERB
	another mutation, of the MVERB with 8 delay lines and 4 allpass added 
	+ some parameter tweaking

- MODEL277
	a feedback delay tool, freely inspired from Buchla 277

- LOGIC
	a simple module for boolean logic, Was my gym to learn VCV modules
