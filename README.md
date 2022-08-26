## exchanger

exchanger is a vst plugin that separates audio in real time into up to 20 sine partials, which can be changed into square waves or saw waves. it was inspired by eliderp's resynthesis max4live device, but it has a few additional features, like a built-in filter, pitch shifting in semitones instead of ratios, independent control of amplitude and frequency smoothing, low latency, and operation in any daw that supports vst3.

download the plugin from the "releases" page.

## warning

this plugin resets all parameters whenever it is loaded, even if the project it is loaded in is saved. this is a bug and i might look into fixing it if there's a lot of interest in the plugin. for now, you can bounce sounds to audio or automate any parameters you change to preserve their state. my recommendation is to bounce the wet signal so you can mix it in and maintain control of the dry signal.

## parameters

- "waveform" fades between different waveforms.
- "pitch" controls pitch of the wet signal in semitones. to adjust it in small increments, hold the shift key before clicking and dragging.
- "partials" controls the number of partials. partials are ordered by loudness, so the quietest partials are removed first.
- "max analysis" limits the maximum frequency that partials can track. this is useful if sudden jumps to high frequencies are ruining the sound. turning it down when there are many partials playing can lead to partials getting stuck inside the buffer and playing indefinitely.
- "amp time" limits how quickly partials can change in volume. it sounds similar to the attack and release knobs on a vocoder. it sounds better at low levels with transient sounds.
- "freq time" limits how quickly partials can change in frequency. at zero, partials can jump between frequencies instantly, which creates satisfying textures on certain sounds. higher levels create pitch glides.
- "filter" is a gentle low pass filter on the wet signal to keep square and saw sounds from sounding overly harsh.
- "stereo" controls stereo width. this is useful because the effect tends to exaggerate stereo width.
- "mix" allows the dry signal to be mixed in.

## installation

to install this plugin, extract it into your vst3 folder.
- on windows the folder is normally c:\program files\common files\vst3
- on mac the folder is normally library/audio/plug-ins/vst3

## credits

- [Pure Data](https://puredata.info/) by Miller Puckette and others
- [Camomile](https://github.com/pierreguillot/Camomile) by Pierre Guillot
- [resynthesis max4live device](https://www.youtube.com/watch?v=b0lA_FAUnlo) by eliderp
