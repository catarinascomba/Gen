# RedPitayaGenerator
RedPitaya Function Generator

This a modified version of the original RedPitaya function generator: http://wiki.redpitaya.com/index.php?title=Command_line_utilities

While the original generator doesn't support [PWM](https://en.wikipedia.org/wiki/Pulse-width_modulation), this version has an extra option. It's possible to use PWM output via 
`"./generate ch amp freq pwm dc" `
with a duty cycle between 0.1 and 99.9. 

## How to get it on the RedPitaya
Login via SSH into your RedPitaya and clone the files. You can use the precompiled "generate" or compile it on your own:

`git clone https://github.com/schlenzmeister/RedPitayaGenerator.git`
`make`

## Examples

Here in the examples, a frequency of 20kHz and Channel 2 was used. A duty cycle 50/50 is equal to a square wave:

`"./generate 2 2 20000 pwm 50"` 
` "./generate 2 2 20000 sqr"`

To get a duty cycle of 25/75 use:
`"./generate 2 2 20000 pwm 25"`

To get a duty cycle of 80/20 use:
`"./generate 2 2 20000 pwm 80"`


