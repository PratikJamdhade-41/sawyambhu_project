# Project Notes — Algorithm Race Advanced Edition

## Purpose
An interactive browser-only learning tool that lets users compare sorting strategies visually and inspect their algorithmic work.

## Architecture
- `index.html`: semantic layout, controls, race panels, benchmark lab, and quiz.
- `assets/css/style.css`: futuristic dark-purple/cyan design, responsive layout, accessibility focus styles, and reduced-motion handling.
- `assets/js/script.js`: six generator-based sorting algorithms, dataset creation, race scheduler, counters, validation, benchmark lab, and quiz logic.

## Reliability decisions
- Racer arrays are cloned from the same `baseArray`; one algorithm cannot mutate the other's input.
- Race completion validates both arrays are sorted.
- Benchmark runs use independent fresh copies of the same dataset.
- The winner label explicitly uses generator event count, not elapsed CPU time.
- The benchmark explains that browser timings are noisy and should be repeated.
- No network APIs, back end, API keys, eval, or third-party runtime libraries are required.

## Automated algorithm test
The six generator implementations passed 20 randomized tests at each array length from 0 to 100 (12,120 runs total), compared against JavaScript's numeric sort result.

## Manual demo checklist
- [ ] Open `index.html` in the actual demo browser; inspect console errors.
- [ ] Test all six algorithms against one another with random and sorted presets.
- [ ] Test Play, Pause, resume, Step, Restart, Reset, New Dataset, and speed adjustment.
- [ ] Run Benchmark twice and verify both result panels update.
- [ ] Complete each quiz question.
- [ ] Check narrow mobile viewport and keyboard focus.
