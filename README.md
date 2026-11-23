# Chasing the Beat: the download package

For the Making Sound Machines **Stolperbeats** (stock firmware 163). Goes with the manual *Chasing the Beat: Pushing Stolperbeats Forward* by The Beatnik Himself and Pulse.

## What's in here

| Folder | What it is |
|---|---|
| `Card Files - Slots 1-32/` | The 32 banks as `PatternBank000.txt` to `PatternBank031.txt`. They load into bank slots 1 to 32. |
| `Card Files - Slots 33-64/` | The same 32 banks as `PatternBank032.txt` to `PatternBank063.txt`, for bank slots 33 to 64. Byte for byte the same patterns. |
| `AI-Kit/` | A folder you give to an AI agent so it can build new banks the same way, for you. |
| `LICENSE`, `CREDITS.md` | Free to use, share and remix under CC BY 4.0: credit "Chasing the Beat by The Beatnik Himself and Pulse". The sources the banks cite are listed in `CREDITS.md`. |

Use **one** of the two card folders: the half of the card you don't mind replacing.

The manual, *Chasing the Beat*, is a PDF of its own. Download it from the same place as this package; it isn't inside the zip.

## Putting the banks on your module

1. **Back up your SD card first.** Copy everything on it to your computer.
2. Power the module off and take the card out.
3. Copy the 32 files from **one** card folder to the **top level** of the card (not into a folder). Let them replace the files with the same names. That replaces whatever banks were in those 32 slots.
4. **Change nothing else.** Don't touch `MachineConfig.txt`, `MachineState.txt`, `EnvelopeSettings.txt` or the MIDI maps: they hold your own settings.
5. Eject the card safely, put it back, power up.
6. **Press play, then stop, once.** The module saves its state when it stops.

If those bank slots were switched off on your card, switch them on with Bank Edit (hold a Bank button for 2 seconds).

Each bank's tempo and home setting (Timing, Shuffle row, Feel) are global on the module, so dial them in by hand. They're in the manual, and in `AI-Kit/banks/`.

## Using the AI kit

1. Open your AI agent (Claude, ChatGPT, Gemini, a local model: any agent that can read a folder of files).
2. Give it the `AI-Kit` folder.
3. Tell it: **"Read START-HERE.md first."**
4. Ask for a bank. For example:
   - "Build me a new bank: a UK garage two-step groove at 132 BPM, the way these banks are built."
   - "Make bank 21 more like bank 24."
   - "Less busy at slot 18."

It hands back a complete bank file, a note per track on what it did and why, the home setting to dial in, and which hits it invented. Agents that can run Python will check the file with `AI-Kit/tools/validate.py` before giving it to you. Copy the file to your card the same way as above: back up first, and remember it replaces the bank in that slot.
