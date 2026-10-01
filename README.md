# Time Complexity Analyzer

A web tool for the **Design & Analysis of Algorithms (DAA)** course. Paste pseudocode and it estimates the Big-O time complexity, explains which rule matched, and times real algorithms in your browser.

**Live demo:** https://professor471.github.io/time-complexity-analyzer/

## Features

- **Analyzer**: rule-based detection of complexity from pseudocode:
  - single loop → O(n)
  - nested loops → O(n²), O(n³)
  - halving/doubling loop variable (`i = i / 2`, `i *= 2`, `mid`) → O(log n)
  - recursion on halves + linear merge → O(n log n), solved with the Master Theorem
  - two or more recursive calls on n − 1 → O(2ⁿ)
- **Examples**: linear search, binary search, merge sort, quick sort, bubble sort, recursive Fibonacci, sum of subsets.
- **Performance test**: runs real JavaScript versions of linear search, binary search, bubble sort and merge sort on growing inputs, times them with `performance.now()`, and compares the measured slowdown with the theory.
- **Quick reference**: asymptotic notations (O, Ω, Θ, o), the Master Theorem's three cases, and a best/average/worst cheat sheet for common algorithms.

## Tech stack

- HTML5, CSS3 and vanilla JavaScript, all in a single `index.html`
- No frameworks, no backend, no build step
- Google Fonts (Inter, JetBrains Mono)

## Run it locally

Download `index.html` and open it in any modern browser.

> The analyzer uses pattern-matching rules, not a real parser, so treat its output as a teaching aid.
