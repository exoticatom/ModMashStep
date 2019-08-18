# ModMeshStep
This plugin is made for CraftBeerPi3 to extend capabilites in regards to common problem with SSR when they fail shortened.
It adds new step called "Mod_MeshStep" to steps.

Idea is to introduce "Protective Circuit" which will, when triggered:
- stop brewing process
- show remaining time
- disconnect output of SSR in order to protect the mash from higher temperature.

Configuration of  plugin is to adding protective circuit which can be one of the oputputs of the relay board.
Relay board (Protective Actor) is controlling high current (16+ A) breaker.
Breaker is in series to SSR output and in case of trouble will disconnect the heater.

If the portectection is active, manual intervention is needed.

Config:
- "Temperature threshold" is the  temperature when protection will kick in and disconnect SSR output.
For implementation it is needed to have relay board (1 relay reserved) and high current circuit breaker.

- Protective Circuit is an Actor which controls output of SSR.

info: Threshold temperature = Temperature + temperature difference



