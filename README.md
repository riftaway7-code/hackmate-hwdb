# hackmate-hwdb

a repo to improve [hackmate](https://github.com/riftaway7-code/hackmate) based on real users' hardware logs.

hackmate's compatibility checks (which macos versions work on which cpu gen, which kexts get picked, etc) are based on general known-good rules. this repo collects real, confirmed reports from actual machines so the tool can get more accurate over time, and so people can check if their exact device has already been tested before trying it themselves.

## structure

top level is split by which hackmate feature you used, since different modes have different failure points:

- `full-build-logs/` — Full Build (fresh usb, format + everything)
- `already-formatted-logs/` — Already Formatted mode
- `repair-efi-logs/` — Repair EFI mode
- `no-usb-logs/` — EFI folder output, no usb
- `dual-boot-logs/` — Dual Boot setup
- `efi-health-check-logs/` — standalone EFI Health Check

inside each of those, logs are further split by cpu generation (`intel-gen7`, `amd-zen3`, etc), matching hackmate's own compat tiers.

## how to submit a log

1. copy [`TEMPLATE.log`](TEMPLATE.log) and fill it out with your hardware and result
2. figure out which two folders it goes in:
   - which feature you used (e.g. `repair-efi-logs/`)
   - then your cpu gen inside that (e.g. `intel-gen8/`), intel: `intel-genN/`, amd: `amd-zenN/` matching your ryzen chip's zen architecture
3. name the file after your device, e.g. `thinkpad-t480-i5-8350u.log`
4. open a PR, or just paste your filled out log in a hackmate issue/reddit comment and it'll get added

doesn't matter if it worked perfectly or not, failed/partial results are just as useful as clean ones.
