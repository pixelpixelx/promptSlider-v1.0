Prompt List Controller .tox (TouchDesigner)

This repository contains a custom TouchDesigner .tox component built as a modular prompt/keyword controller. It provides an editable table for managing prompt lists and a slider interface for stepping through them in real time.
The component was originally developed for use with StreamDiffusion and MIDI controllers, but it is intentionally lightweight and flexible, making it suitable for a wide range of real-time, generative, and interactive workflows.

FEATURES:
- Editable DAT table for prompt or keyword lists
- Slider-based index control for cycling through prompts
- Clean output via a Null operator for easy parameter referencing
- MIDI-friendly and automation-ready

SETUP & USAGE:
1. Slider
- Default range is set to 1–24
- If you add more rows to the prompt table, increase the slider range accordingly

2. promptTable DAT
- Do not remove or modify Row 0 (header row)
- Add as many rows as needed below Row 0
- Replace the "prompt" text in each row with your own prompts or keywords

3. Using the Output
- To reference the currently selected prompt in another operator’s parameter field, use: op('null1')[1, 0].val
This returns the active prompt value based on the slider position.

NOTES:
- The component is intentionally simple and unopinionated
- It can be extended to support additional indexing logic, CHOP control, or external data sources
