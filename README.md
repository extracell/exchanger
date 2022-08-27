## overview

exchanger is a plugin that separates audio in real time into up to 20 sine partials, which can be changed into square waves or saw waves. it was inspired by eliderp's resynthesis max4live device, but it has a few additional features, like built-in pre and post filters, pitch shifting in semitones instead of ratios, independent control of amplitude and frequency smoothing, low latency, and operation in any daw that supports vst3.

download the plugin from the "releases" page.

## parameters

- "waveform" fades between different waveforms.
- "pitch" controls pitch of the wet signal in semitones. to adjust it in small increments, hold the shift key before clicking and dragging.
- "partials" controls the number of partials. partials are ordered by loudness, so the quietest partials are removed first.
- "min analysis" high passes the wet signal before it is separated into partials. this keeps low and sub frequencies from muddying up the entire frequency spectrum when they are turned into more harmonically rich waveforms.
- "max analysis" low passes the wet signal before it is separated into partials. this is useful if partials are randomly jumping to high frequencies in an undesirable way.
- "amp smooth" limits how quickly partials can change in volume. it sounds similar to the attack and release knobs on a vocoder.
- "freq smooth" limits how quickly partials can change in frequency. at zero, partials can jump between frequencies instantly, which creates satisfying textures on certain sounds. higher levels create pitch glides. 
- "filter" is a gentle low pass filter on the wet signal to keep square and saw sounds from sounding too harsh. 
- "stereo" controls stereo width. this is useful if the effect is exaggerating stereo width.
- "mix" allows the dry signal to be mixed in.

## installation

to install this plugin, extract it into your vst3 folder.
- on windows the folder is normally c:\program files\common files\vst3
- on mac the folder is normally library/audio/plug-ins/vst3
if you're on mac, you will have to do some additional work to get the plugin running. you can find instructions and a video [here](https://github.com/pierreguillot/Camomile/wiki/How-to-generate-plugins#manual-all-operating-system).

## changing source files

the architecture of this plugin allows users to edit source files on the fly and apply changes to the plugin simply by reloading it. the camomile wiki and pure data manual are good starting points if you're looking to make changes or even make your own pure data plugins. 

## credits

- [pure data](https://puredata.info/) by miller puckette and others
- [camomile](https://github.com/pierreguillot/Camomile) by pierre guillot
- [resynthesis max4live device](https://www.youtube.com/watch?v=b0lA_FAUnlo) by eliderp
