[update-readmes]   Mode: rewrite — migrating to template structure...
# uc-tool-mx

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/uc-tool-mx)

<!-- AI:start:what-it-does -->
_Description pending._
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
_Architecture documentation pending._
<!-- AI:end:architecture -->

## Install

<!-- Add installation instructions here. This section is yours — the AI will not modify it. -->

```bash
git clone https://github.com/Interested-Deving-1896/uc-tool-mx.git
cd uc-tool-mx
```

## Usage


```
Usage:  uc-tool [options]

  -u  --ucode=<list>       Vendors to build: amd, intel, or amd,intel
                           [default: amd,intel]
  -d  --directory=<dir>    Directory for .img files (generate/extract output)
                           or sections to repack (repack input)
  -D  --default            Set directory and initrd from current boot mode:
                             live:      initrd = /live/boot-dev/antiX/initrd.gz
                                        dir    = ./initrd.gz.D
                             installed: initrd = /boot/initrd.img-<kver>
                                        dir    = ./initrd.img-<kver>.D
                           explicit -d or -i always overrides -D
      --amd-dir=<dir>      AMD firmware source  [default: /lib/firmware/amd-ucode]
      --intel-dir=<dir>    Intel firmware source [default: /lib/firmware/intel-ucode]
  -F  --firmware=<path>    Firmware base: directory (auto-sets amd-ucode/ and
                           intel-ucode/ sub-dirs) or squashfs image (auto-mounted)
  -i  --initrd=<file>      Update this initrd in-place:
                             strip old ucode CPIOs, prepend new ones,
                             refresh <initrd>.md5 if present,
                             run e4defrag if on ext4
  -k  --keep               Keep generated .img files when using a temp dir
                           (only meaningful when -i is given without -d)
  -S  --strip              Strip ucode CPIOs from -i <initrd> without adding new
                           ones; other preamble sections are kept intact
  -H  --has-ucode          Check if -i <initrd> contains ucode CPIOs;
                           exits 0=found, 1=none  (no writes)
  -x  --extract[=<mode>]   Extract initrd sections to -d <dir> (must be empty or new):
                             (bare)    ucode CPIOs only
                             =all     all sections as raw files
                             =unpack  all sections + unpack each into <name>.D/
  -l  --list[=<mode>]      List initrd sections (no files written):
                             (bare)    ucode CPIOs only -- vendor, size, files
                             =all     all sections -- name, size, compression
                             =unpack  all sections + list files inside each
      --repack=<dir>        Repack sections from <dir> back into -i <initrd>;
                             uses <name>.D/ if it exists, else the raw file
  -h  --help               Show this usage
  -n  --no-color           Suppress ANSI color codes in output
  -q  --quiet              Suppress all progress output; only fatal errors shown
  -s  --silent             Only show error messages
  -V  --verbose            Show commands as they run
  -v  --version            Show version and exit
```

## Configuration

<!-- Document configuration options here. This section is yours — the AI will not modify it. -->

## CI

<!-- AI:start:ci -->
_CI documentation pending._
<!-- AI:end:ci -->

## Mirror chain

<!-- AI:start:mirror-chain -->
This repo is maintained in [`Interested-Deving-1896/uc-tool-mx`](https://github.com/Interested-Deving-1896/uc-tool-mx) and mirrored through:

```
Interested-Deving-1896/uc-tool-mx  ──►  OpenOS-Project-OSP/uc-tool-mx  ──►  OpenOS-Project-Ecosystem-OOC/uc-tool-mx
```

Changes flow downstream automatically via the hourly mirror chain in
[`fork-sync-all`](https://github.com/Interested-Deving-1896/fork-sync-all).
Direct commits to OSP or OOC are detected and opened as PRs back to `Interested-Deving-1896`.
<!-- AI:end:mirror-chain -->

## Contributors

<!-- AI:start:contributors -->
_Contributors pending._
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
[GPL-3.0](https://github.com/Interested-Deving-1896/uc-tool-mx/blob/main/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
