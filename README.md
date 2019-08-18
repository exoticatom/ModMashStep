# ModMeshStep Plug-in
This plugin is made for CraftBeerPi3 to extend protective capabilities in regards to a problem which could occur with SSR when they fail (shortened).
This plugin adds new step called "Mod_MeshStep" to steps, with extended capabilites.
For implementation it is needed to have relay board (1 relay reserved) and high current circuit breaker.

Idea is to introduce "Protective Circuit" which will, when triggered:
- stop brewing process, after which manual intervention to continue the brewing is needed.
- show remaining time when process was stopped.
- by activating protective circuit disconnect output of the heater SSR in order to protect the mash from higher temperature.

In this version protection is relaying on the same sensor data as for the kettle which is being protected.

How to Config:
- Add an Actor which will act as protective circuit. Typically one output of relay board.
- Add the Mod_MeshStep to your brewing and configure Protective circuit + temperature difference.
- Connect high power breaker to your relay output and it's outputs in series to SSR relay.


Temperature threshold is the temperature when protection will kick in and disconnect SSR output.
Threshold temperature = Temperature (for mashing) + temperature difference


