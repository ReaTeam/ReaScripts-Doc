## Usage:

```reaper [options] [filename.rpp] [filename.wav]```

## Options:

- **-audiocfg** : show audio configuration at startup
- **-cfgfile file.ini** : use full path for alternate resource directory, otherwise uses default path
- **-new** : start with new project
- **-template filename.rpp** : start with template project
- **-saveas newfilename.rpp** : save project (after creating/loading) as file
- **-renderproject filename.rpp** : render project and exit
- **-ignoreerrors** : do not show errors on load
- **-nosplash** : do not show slpash screen window
- **-splashlog /path/to/filename.log** : write splash screen message log to file
- **-newinst | -nonewinst** : override preference for new instance checking
- **-close[all][:save|:nosave]** : close project(s), optionally not prompting for save
- **-batchconvert filelist.txt** : batch converter mode, filelist.txt includes:
  - list of files to convert:
    `filename.wav`
      or
    `filename.wav(TAB CHARACTER)outputfile.wav`
  - \<CONFIG ...> block (optional) which can contain:
    - SRATE 44100 (omit to use source samplerate)
    - NCH 2 (omit to use source channel count)
    - RSMODE modeidx (resample mode, copy from project file)
    - DITHER 3 (1=dither, 2=noise shaping, 3=both)
    - USESRCSTART 1 (1=write source media BWF start offset to output)
    - USESRCMETADATA 1 (1=attempt to preserve original media file metadata if possible)
    - PAD_START 1.0 (leading silence in sec, can be negative)
    - PAD_END 1.0 (trailing silence in sec, can be negative)
    - OUTPATH 'path'
    - OUTPATTERN 'wildcardpattern'
    - FXCHAIN 'fxchainfilename' (use full path if specified, otherwise FxChains directory)
    - \<FXCHAIN
        (contents of .RfxChain file)
      \>
    - \<OUTFMT
      (base64 data, e.g. contents <RECORD_CFG block from project file)
      \>
    - \<METADATA
      (contents of RENDER_METADATA block from project file)
      \>

## Windows-only options:

- **-noactivate** : launch but do not activate
