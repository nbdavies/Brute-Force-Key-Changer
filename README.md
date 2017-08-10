# Brute-Force-Key-Changer
JSFX plugin (for Reaper), intended for changing the key of a song in realtime. Also useful for producing strange noises

## Installation
1. Download the plugin and unzip: https://github.com/nbdavies/Brute-Force-Key-Changer/archive/master.zip
1. Copy brute-force-key-changer.jsfx into your Reaper plugin directory. http://reaperblog.net/2016/02/how-to-install-js-plugins/
2. Download and install the Cook DSP set of plugins: http://ajaxsoundstudio.com/cookdspdoc/index.html#download

## Controls
1. Filter Q: This controls the width of the bandwidth filters. At 100, all audio that isn't exactly on the notes of your starting scale will be discarded. At lower values, more of those frequencies will remain.
2. Starting key: What key the audio you're applying the filter to is in. This, along with target key, will determine which notes need to be moved.
3. Major/Minor (starting key): Control the tonality of your starting key. For those familiar with music theory, the plug-in uses harmonic minor.
4. Target key: This will indicate what key you want the resulting audio to be in.
5. Major/Minor (target key)
6. Transpose: This will pitch-shift the entire recording up or down, by a maximum of 6 semitones. The shifted signal will still be in your target key.

## Recipes
### Supercomb
1. Set the starting key to the key the audio is in.
2. Set the target key to the same key.
3. Set Filter Q to 100.
4. Leave Transpose at 0.

This will just filter out anything from the original signal that isn't exactly on one of the notes of the scale. For vocals this can give you a stepped vocoder effect. It can help tune your percussion to the key of the song.

### Relative shift
1. Set the starting key to the key the audio is in.
2. Set the target key to the relative minor (for example, going from C major to A minor).
3. Set Transpose to -3.
4. Adjust Filter Q to taste.

This should give you an idea of what the original melody would sound like in a minor key. Specifically in a minor key that would work well with the original key of the song.

### Horror
1. Set the starting key to a very different key than the audio is actually in (for example, if the song is in C major, try Eb minor).
2. Set the target key to that same key.
3. Set Filter Q to 100.
4. If there are vocals present, try low or high Transpose values.

This should produce some unsettling results that bear little resemblance to the music you started with.
