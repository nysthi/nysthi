
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
	added new stero phaser, original design, based on 4th orders Allpasses (WOW :D)
	

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
