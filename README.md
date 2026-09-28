# Python 101: 3-Hour Hands-On Workshop

A browser-based, instructor-led introduction to Python. The presentation is written in [Slidev](https://sli.dev/), and students run the lab code in the [Programiz Online Python Compiler](https://www.programiz.com/python-programming/online-compiler/). Students do not need to install Python or create an account for the labs.

## Agenda

| Time | Topic |
| --- | --- |
| 0:00–0:30 | Introductions, programming in the age of AI, and why Python |
| 0:30–1:00 | Data types, variables, and operators |
| 1:00–1:30 | Lab 1: personal budget calculator |
| 1:30–2:00 | Functions, parameters, and calling functions |
| 2:00–2:30 | Lab 2: tip calculator |
| 2:30–3:00 | Built-in functions, modules, `pip`, and next steps |

## Present locally

Install [Node.js 22.12 or newer](https://nodejs.org/), then run:

```bash
npm install
npm run dev
```

Open the local URL shown in the terminal. The source presentation is [`slides.md`](slides.md); edit that file to customize the lesson. Slidev's presenter view exposes instructor notes embedded in the slides.

To create a static web build, run `npm run build`. The output is in `dist/` and can be hosted on a static web server. To export a PDF, run `npm run export` (Slidev may request its browser dependency on first export).

You can also open [Slidev's browser editor](https://sli.dev/new) and paste the contents of `slides.md` to work without a local Node installation.

## Student labs

1. Open the [Programiz Online Python Compiler](https://www.programiz.com/python-programming/online-compiler/).
2. Replace its example code with the code from a lab slide.
3. Click **Run**, observe the output, and change the values to explore the result.
4. For exercises using `input()`, enter each requested value when prompted. If the browser compiler's input behavior changes, replace `input()` calls with sample literal values.

Lab 1 practices types, variables, numeric conversion, and operators through a personal budget calculator. Lab 2 defines and calls functions for a tip calculator, then adds user input and optional extensions. All required lab instructions are in `slides.md`.

The `pip` segment is a concept and instructor demonstration. Installing packages is not required in the student browser compiler.

## Instructor preparation

- Run the slides and the two labs once before class, including the examples that use `input()`.
- Have students open the compiler at the start of the workshop.
- Use the timing and facilitation notes in Slidev presenter view; leave time for students to type and debug.
- If the room is large, use a short pair introduction before taking examples from the group.

## Project files

- `slides.md` — complete presentation, lab instructions, and speaker notes
- `package.json` — Slidev commands and dependencies
