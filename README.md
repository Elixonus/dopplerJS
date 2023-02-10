# doppler 🔊

![Doppler Effect Icon](./doppler/favicon.ico)

## About

Simulation of the doppler effect, particularized in the context of sound waves and explored through scenarios where a wave emitting source and wave detecting observer move with a user controllable velocity or acceleration.

## Source

Source is controllable in velocity and acceleration and is always in one of three states: stationary, constant velocity or constant acceleration.

Source emits waves with a constant frequency and amplitude.

## Waves

Waves propagate in time with their amplitude attenuatuating exponentially.

Only crests are illustrated in the rendering of waves.

Currently when multiple waves collide, interference is not accounted for.

## Observer

Observer, similarly, is controllable in velocity and acceleration and is always in one of three states: stationary, constant velocity or constant acceleration.

Observer detects a wave at a time and records its perceived frequency and amplitude.

## Algorithm

Data of each wave is stored in a rolling queue array where the array is overwritten progressively in a repeating fashion.

When each wave is emitted, the current time, as well as the position and velocity of the source is stored in an object to be used later.

To find which wave is currently being detected by the observer, the program goes through each wave to try to find the closest wave that has passed the observer, if any.

If an observer wave is found, the perceived frequency and amplitude is calculated using the vector position and velocity of the observer as well as the vector position and velocity of the source from the time of wave emission using the source wave data structure mentioned earlier.

## Functionality

`TIME` button group can be accessed with key `P` to pause the simulation, possibly to change the properties of the source and observer.

`BUFFER` button group can be accessed with keys `S` and `R` to save the current simulation time and restore the saved time later on.

`SOUND` button group can be accessed with key `M` to interpret the observed signal as a sound wave.

`OWAVE` button group can be accessed with key `O` to highlight the properties of the wave that is observed at the current time. This includes the position and velocity of the source.

`CONTROL` button group can be accessed with key `C` to toggle between modifying the properties of the source and observer.

`TYPE` button group can be accessed with key `T` to toggle between modifying the velocity and acceleration of the controlled object.

`DIRECTION` button group can be accessed with keys `ArrowLeft`, `ArrowRight`, `ArrowUp`, `ArrowDown` and `0` to set the direction of the vector (including origin) of the motion type of the controlled object.

`MAGNITUDE` button group can be accessed with keys `1`, `2` and `3` to set the magnitude of the vector (excluding origin) of the motion type of the controlled object.

## Limitations

Does not implement the effects of wave interference.

Observer can only detect one frequency and amplitude at a time.
