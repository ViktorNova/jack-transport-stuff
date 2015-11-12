# jack-transport-stuff
Random collection of stuff to query and control JACK transport &amp; song position.

The core functionality bunch of scattered man pages for different apps that come with JACK, or the jack-tools package.

This document was made to simplify the use of this stuff by explaining it all in one place. 

There are also scripts to expose transport controls as commands like ````jack-transport-play````, ````jack-transport-locate````, etc., as JACK does not provide these 

This is useful for scripting your own show control via shell scripts, window manager buttons, smartphone (via sshmote or similar), etc, or even to control/query JACK transport from another language that doesn't have a native JACK transport control library.


______________________________
TODO: Write micro 1-line scripts to run these commands:

## Get song position with jack_showtime
Yep.

## jack_transport
JACK transport can be controlled from the commandline via the **jack_transport** command, which is included with JACK or in the *jack-tools* package in most linux distributions

The command ````jack_transport```` by itself runs an interactive prompt, which is not very useful for scripting. However, we can pipe commands into jack_transport for one-shot starting, stopping, setting the tempo, or relocating the song position with a single command

Here's the commands we might be interested in:
````
locate		  Locate to frame <position>.
master      Become timebase master [<conditionally>].
play        Start transport rolling.
stop        Stop transport.
tempo       Set beat tempo <beats_per_min>.
timeout     Set sync timeout in <seconds>.
````

####To start the transport rolling:
```` echo play |jack_transport````


