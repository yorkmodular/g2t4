## G2T4 - quad gate-to-trigger

Exactly what it says on the tin - sometimes you want a short pulse (aka. a trigger) but all you've got are gates. This module will help to rectify that - you can use it to convert up to 4 incoming gate signals into (much) shorter triggers, whether it be for sample and hold circuits or envelope generators.

The inputs are normalled together so it's quite possible to use a single gate to generate up to four triggers.

### Build notes
The range of trigger lengths is dependent on a couple of variables - first there's the value of channel's capacitor and then that of the resistance that it discharges through. Clearly, your incoming gate needs to be long enough to charge the trigger capactior, and with this in mind I generally use 33nF capacitors on the pre-built modules.

You can get a rough idea of what sort of trigger length you'll get by using the following formula using the __RC__ time constant as a guide - so for a capacitance of 33nF and a resistance of 1M you can reasonably expect a pulse length of around 30-40ms - in addition, each channel has a trimpot (1M on pre-builts) so you can fine-tune the trigger length. If 30ms is too long for you, replace the 33nF caps with 22nF or even 10nF - for best results, use polythene film caps

Extensive use is made of Schmitt triggers (hence the 3 40106s) - this means that the produced trigger should have relatively noise-free. The magnitude of the trigger is dependent on the power supply to the 40106 ICs - by default I use 5V; to change this, you'll need to change the voltage regulator (U4)