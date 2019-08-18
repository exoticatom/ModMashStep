# ModMeshStep
This plugin is adding modified Mod_MeshStep and Mod_MeshOut steps for Craftbeerpi3.


Schematic and the code is meant for protection of the brew, if SSR fails shortened by adding an addition layer to disconnect the heater. If protective temp circuit is active relay will disconnect SSR from heater on the output side and stop/pause brewing process expecting manual intervention.

I.e. If you are mashing at 64C and temperature rises above configurable threshold temperture , brewing is interupted and alarim is raised.

Temp diff is the moment when protection will kick in and disconnect SSR output. For implemtation it is needed to have relay board (1 relay reserved) and high current circuit breaker. 

Threshold temperature = Temperature + temperature difference



