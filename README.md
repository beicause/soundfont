# soundfont

SoundFont assets used by [rustysynth-ext](https://github.com/beicause/rustysynth)
and other projects.

## Contents

| File | Size | Description |
| --- | --- | --- |
| `FluidR3Mono_GM.sf3` | 14.5 MB | FluidR3Mono_GM 2.315 in SoundFont3 format (Ogg Vorbis compressed samples). |
| `FluidR3Mono_GM.tar.zst` | 89.6 MB | The same font in uncompressed SoundFont2 format, shipped as a zstd-compressed tar archive. Extracting it yields `FluidR3Mono_GM.sf2`. |

The `.tar.zst` archive exists because GitHub cannot host the ~118 MB `.sf2`
file directly; zstd brings it down to a size the raw file host accepts.

## Usage

Raw file URL pattern:

```text
https://raw.githubusercontent.com/beicause/soundfont/main/<file>
```

Extract the SoundFont2 font:

```sh
zstd -d < FluidR3Mono_GM.tar.zst | tar -x
```

## License

FluidR3Mono_GM is released under the MIT license by its author,
Frank Wen / Christian Collins. See [LICENSE.txt](LICENSE.txt) for the full
text and [the Debian copyright file](https://metadata.ftp-master.debian.org/changelogs/main/f/fluidr3mono-gm-soundfont/fluidr3mono-gm-soundfont_2.315-7_copyright)
for the packaging details.
