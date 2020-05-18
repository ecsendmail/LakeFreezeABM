# ABM-Lake-Freeze-Exothermic-Bottom
ABM in Javascript as .html file modelling freezing of lake with exotherrmic source at bottom


This is an agent-based simulation model to deal with the process of a lake at a constant 10C freezing (ice at 0C top layer), where water is densest at 4C, and there is a constant exothermic source at 6C at the bottom (rotting vegetation, tailing chemicals, etc)...

The differential equations are hard, and intuition fails to figure out the balance between the 4C water wanting to sink, but heated up by the 6C source, which then wants to rise, but meets the 4C layer and temperatures lower or higher than that (since both 3C and 5C are lighter than 4C)....

The model gives different positions depending on the heat exchange parameter (which has a starting value of 0.04)...

The partitions are fuzzy because of the mixing but also because there is a small stochastic terms added in to an exchange so we don't go back and forth in a stalemate.... ensuring non-identicality among the 600 layers.

To run it, you can't click on it...it is an html file....so it has to be seen as a web-site....the best thing is to locate it in its directory, right-click on it and OPEN WITH ...Chrome....

OR SELECT THE "LINK TO RUN MODELS" in this repository.

If you read the code it trades temperatures from a layer with the layer below, and this then determines the densities...the trade is pretty much linear with a tiny random factor for non identicality so we never get stalemates...

So higher trades means that the layer sinks faster -fewer stay here...till the layer from above affects this one...

Had to work to get linear variation of colors had to use HSV and convert to
#hex....with a color of change per 1C change 

The 6C bottom heat source came from a tailings pond problem...the top layer is ice so the first real exchange comes from a 10C difference with zero C.

I only looked at the bottom layer because upward movements happen anyway when one layer sinks  the other rises...so I hD to give each layer a unique identity...

Sorry, Github does not support pasting an image or I could share the interesting observation that in this ABM at least, the temperature changes do not go uniformly from top to bottom but in BANDS. It would be interesting to see if there is a mathematical relationship between the bands (sure one can be construed!)....😂

I KNOW IT WORKS ON CHROME AND I AM RUNNING IT ON EDGE

The temperature scale is on the left (RED at 10C, going to purple at 0C), with the 4C densest temperature as pale blue. What you would see as the simulation begins is a transition in bands from red to orange to green at the bottom, then the pale blue 4C zone, and eventually above that the layers from 4 to 0C going upwards to the top.

It would be interesting to set the exothermic layer to produce always a temperature of 2C....I will leave that to the reader to change just one constant in the Javascript program.

VALIDATION - GREAT QUESTION....LET ME KNOW IF YOU HAVE AN ANSWER OR EVEN A WAY TO RELATE THE THERMODYNAMIC EQUATIONS IN THE MATHEMATICAL MODEL TO THE HEAT EXCHANGE SIMPLISTIC APPROACH I HAVE ADOPTED...

UNTIL THEN, CREATE YOUR OWN ROTHKOS....BUT IF YOU CHANGE THE BOTTOM TEMP, YOU WILL FIND THAT QUALITATIVELY THE MODEL BEHAVES AS YOU THINK IT MIGHT....
