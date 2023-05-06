# Electronics

<img src="/docs/images/Final_Electronix_Box.jpg" height="400"> <img src="/docs/images/interfacing-esp32-with-neopixel-and-sound-sensor-for-smart-led.webp" height="400">

There was limited creativity in the electronics. I followed a standard [WLED](https://kno.wled.ge/) deployment on an ESP32 board. The main difference in the diagram, above, was the inclusion of [SN74AHCT125N buffer gates](https://www.amazon.com/gp/product/B08R6BCSYC) to help protect the ESP32 from whatever may happen on the LED data lines. The other change, is the direct connection of the 5V supply to the LED line and not driving it off the ESP32 board.

Note, I did not attach a sound sensor module. I may create a [Nanoleaf](https://nanoleaf.me/en-US/) style project in the future. If so, I will probably add a sound sensor module to that implementation, but it didn't make sense for this project as I will not be playing audio to my neighbors.

The SN74AHCT125N package supports 4 buffers, so I wired up 4 data lines from the ESP32 for future lighting expansion. For example, some type of animated holiday display, or maybe even a sign display for in the workshop.  The [power supply](https://www.amazon.com/gp/product/B078RYWZMH/) is also oversized to support future lighting.

The project is packaged inside [water proof junction box](https://www.amazon.com/gp/product/B0B87VGV62). Given the environment and risks with lots of things happening in the outside world, I didn't want any issues reasonably contained. Most of the components in there should fail with only emitting some smoke.

The board shown is my second attempt. While testing one of the lanterns, I ended up letting smoke out of the ESP32 power circuit when something shorted. The original PCB didn't have any connecting traces so they wiring was a lot messier. The [new PCB](https://www.amazon.com/gp/product/B07YSCGBL7/) is a lot cleaner.

The circuit board, power supply and wiring are separated by a wiring panel to make the wiring a bit easier. The wiring panel is a [DIN rail](https://www.amazon.com/gp/product/B01JH2RZWC) with 8 [DIN terminal blocks](https://www.amazon.com/gp/product/B08R3FZ3QD).

On the other side of the wall from the project box is my patio entryway. I drilled a hole through the wall and just ran the wire, glueing it to the foundation pad to keep it less visible until it could go underground. Once I have more projects that use the LED controller, I'll come back and install some type of plug panel, so that various outdoor lighting projects can be plugged in. But, I think I need to know more about the future before it makes sense to pick a specific format.

As for the lantern wiring, the LED data lines are in series, from the first LED to the last. The power lines, however, are linked, lantern to lantern. Each 12 LED set is powered in series, but in parallel to the other lanterns. There was still a significant drop in voltage for the light levels to be notably different between the first and last lantern, which were right across the sidewalk from each other. I expected this and trenched out a path under the house side of the sidewalk path and connected the power and ground lines between the first and last lantern. This significantly smoothed out the brightness difference. I'm sure it gets dimmer as you go towards the drive way, but it isn't overly noticeably.

**Areas for improvement**
Other than the smoke failure, I didn't have any significant things I would do differently. I do want to learn how to draw and then make my own circuit boards (e.g. KiCad), but that was out of scope for this project.
