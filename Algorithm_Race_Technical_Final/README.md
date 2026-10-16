# Algorithm Race — Advanced Edition

A browser-only interactive sorting visualization and performance comparison platform built with semantic HTML, CSS, and vanilla JavaScript. No framework, server, API key, database, or package installation is required.

## Project structure

```text
Algorithm_Race/
├── index.html
├── assets/
│   ├── css/style.css
│   └── js/script.js
├── docs/PROJECT_NOTES.md
├── .gitignore
└── README.md
```

## Run it

1. Extract the ZIP.
2. Open `index.html` in a modern browser, or open the folder in VS Code and use Live Server.
3. Internet is optional; Google Fonts enhance the typography, with local fallback fonts available.

## Features

- Six algorithms: Bubble, Insertion, Merge, Quick, Selection, and Heap Sort.
- Both racers use independent copies of the exact same input dataset.
- Five input patterns: random, nearly sorted, already sorted, reverse sorted, and few unique values.
- Adjustable array size (10–100) and five animation speeds.
- Play, Pause, Step, Reset, Restart, and New Dataset controls.
- Live comparisons, swaps, writes, event count, progress, elapsed animation time, and latest-event trace.
- Sorting validation at the end of each animated race.
- Benchmark Lab runs each selected algorithm synchronously on a fresh copy of the same input and reports browser-measured elapsed time plus operation counts.
- Algorithm guide with time/space complexity and strategy notes.
- Big-O growth explainer and interactive multiple-choice learning checkpoint.
- Responsive futuristic purple/cyan interface, keyboard shortcuts, help dialog, and reduced-motion support.

## Controls

- **Start race / Space:** Start or resume.
- **Pause / Space:** Pause.
- **Step / S:** Advance each unfinished racer by one generator event.
- **Restart:** Start over with the same original dataset.
- **Reset race:** Reset counters while preserving the current dataset.
- **New dataset / N:** Generate another dataset using the selected pattern.
- **Benchmark:** Run a non-animated local timing test on the same input.

## Measurement notes

- The race winner is based on the number of yielded algorithm events. It is not a claim about actual CPU runtime.
- The Benchmark Lab measures elapsed browser time, but single-run measurements—especially on arrays of 10–100 values—are noisy and affected by device load, browser optimization, and runtime environment. Repeat results before drawing conclusions.
- Comparisons, swaps, writes, and generator events are distinct measures. A swap is counted as one swap operation; writes count array assignments made by insertion/merge operations.
- Big-O describes growth as input size increases, not exact seconds.
- Quick Sort has average O(n log n) and worst-case O(n²) time. Merge Sort uses O(n) auxiliary memory. Heap Sort has O(n log n) worst-case time and O(1) auxiliary space.

## Hackathon demo flow (3 minutes)

1. Set Bubble Sort vs Merge Sort, choose 40 random values, and start the race.
2. Pause and step once to show comparison/movement highlights and the live execution trace.
3. Change to nearly sorted input and explain why input patterns affect algorithms differently.
4. Run Benchmark to show measured local time alongside operation counts—explain that timings vary.
5. Switch to Heap Sort and finish with the Big-O explainer or quiz.

## Validation

The six generator implementations were tested in Node.js with 20 randomized arrays at every length from 0 through 100 (12,120 algorithm runs total), and each output was checked against a numeric sorted reference. Browser rendering and full interaction still should be checked in the target presentation browser before the live demo.
