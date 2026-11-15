# jMidi 1.0.0

**jMidi** is a Windows desktop MIDI processing studio for editing, transforming and routing MIDI performances.

This release adds a dedicated **MIDI In / Out** diagnostics screen:
- Selected MIDI input and output port names
- Live incoming and successfully transmitted message totals
- Last-message timestamps and MIDI message summaries
- Separate MIDI IN and MIDI OUT event logs
- Input/output queue depth and dropped-event counters

The 1.0.0 source package is available from the ChatGPT delivery accompanying this repository update. The project source includes Python modules, tests, documentation, Windows packaging files and a GitHub Actions CI workflow.

## Validation snapshot
- 67 automated tests passed locally
- 1 GUI smoke test skipped locally because PySide6 was unavailable
- Python compile checks passed
- Windows executable build and physical MIDI hardware acceptance still require the Windows CI/hardware environment

## Credits
Developed by Hartwinder Singh
