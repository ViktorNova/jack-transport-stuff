# jack-transport-stuff
Random collection of stuff to query and control JACK transport &amp; song position
______________________________
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


