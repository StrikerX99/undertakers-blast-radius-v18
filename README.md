# Undertakers Blast Radius V18

Extract the submission ZIP at the root of the team repository. Build for Linux/amd64.

```sh
docker build --platform linux/amd64 -t undertakers-v18 .
```

The selector reads the organizer’s test catalog and independent patches from `/data` and emits one JSON worker plan per patch. It uses the public SQLGlot pin `eb11aec4be8cb2122afe713a4816662c3f0fb2fa`. Its maps were produced from the team’s own measurements of that pin. The build prepares lookup indexes from the pristine code.

For the parser node-limit test, the selector runs the patched parser on the original assertions. It shortens two repeated SQL inputs and advances the node counter so the parser must cross the original 1,000,000 and 50,000 limits and produce the expected exceptions. This predicts the full-size result. Size-sensitive edits detected by the source checks, failed probes and interrupted probes retain the original test.

For qualifying changes to shared helper functions and generator callbacks, it retains tests that reached the affected code or used the changed dispatch entries. For some parser edits it can also clear the TPC-DS executor test using source lines recorded during the full native test, including its worker processes. The probe must account for all changed files. Ambiguous cases keep their existing schedule.

The scheduler evaluates the recorded runtime of the busiest worker plus the charge for each occupied worker, for up to eight workers. It skips optional verification when the potential reduction is too small. The separate comparison includes local batch inputs, answers, worker plans and reproducible performance measurements.
