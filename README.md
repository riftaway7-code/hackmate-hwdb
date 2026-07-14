# hackmate-hwdb

a repo to improve [hackmate](https://github.com/riftaway7-code/hackmate) based on real users' hardware logs.

hackmate's compatibility checks (which macos versions work on which cpu gen, which kexts get picked, etc) are based on general known-good rules. this repo collects real, confirmed reports from actual machines so the tool can get more accurate over time, and so people can check if their exact device has already been tested before trying it themselves.

## how to submit a log

1. copy [`TEMPLATE.log`](TEMPLATE.log) and fill it out with your hardware and result
2. figure out which folder it goes in:
   - intel: `intel-genN/` where N is your cpu generation (hackmate shows you this)
   - amd: `amd-zenN/` matching your ryzen chip's zen architecture
3. name the file after your device, e.g. `thinkpad-t480-i5-8350u.log`
4. open a PR, or just paste your filled out log in a hackmate issue/reddit comment and it'll get added

doesn't matter if it worked perfectly or not, failed/partial results are just as useful as clean ones.
