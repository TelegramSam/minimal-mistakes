---
published: true
title: 'Happy Birthday, Arduino Style'
---
![rachel-arduino-airstream.jpg]({{site.baseurl}}/media/rachel-arduino-airstream.jpg)

We homeschool our kids, which gives us flexibility in the curriculum department. This year, I decided that microcontroller programming would make a nice addition to school for my 11 and 9 year olds.

I found a serendipitously timed [Kickstarter][ks] for the [Plumduino][plumduino], an Arduino based board board with 8 NeoPixel LEDs, two proximity sensors, a button, and a wonderful expansion board with two sliders, a microphone, piezo buzzer, IR transmit and IR receive with an included remote.

I backed the project, and received it just in time for school this fall.
My 11 year old Rachel is been the first student to attack this wonderful piece of hardware, and I’ve been guiding her through learning all sorts of things about Arduino based microcontroller programming.  (My 9 year old is spending some additional time with Hour of Code based learning to prepare for it, and will be beginning later this year.)

Rachel just turned 11, and I wanted to prepare a small birthday surprise.

I found a code [snippit][cs] that plays the happy birthday melody out of the piezo buzzer, and combined it with some LED code and use of the IR receiver and the IRRemote library to recognize a press of the play button on the remote.

The code is organized like this:
- Play simple animation on the LEDs.
- When the IR receiver receives the play button, play the birthday song.
- During each note, play a random LED set to a random hue.
- After the song completes, return to the simple animation. 

And the code, via [CodeBender](http://www.codebender.cc):
<iframe style="height: 510px; width: 100%; margin: 10px 0 10px;" allowTransparency="true" src="https://codebender.cc/embed/sketch:379540" frameborder="0"></iframe>
I wrote this the evening before Rachel’s birthday, and left it out on the table. When she woke up, I told her how what to do to activate it, and she loved it! The first ‘happy birthday’ song she was sung was provided by an Arduino!

[ks]: https://www.kickstarter.com/projects/plumgeek/plumduino-diy-programmable-light-your-first-maker/description
[plumduino]: http://www.plumgeek.com/plumduino.html
[cs]: http://forum.arduino.cc/index.php?topic=178460.0
