# Project: Freya Dataset Builder

## Goal
Create a simple local web tool to build a high-quality dataset of user input / Freya output pairs for fine-tuning Gemini.

## Use Case
These examples will form the foundation of Freya’s personality and behavior. The tool is designed to allow the user to build this dataset gradually and safely, with persistence and backup features.

---

## Core Features (Phase 1)

- Two text input fields:
  - **User Input** — What the user would say
  - **Freya Response** — Freya’s ideal response in her voice
- **"Save Example"** button
  - Saves a `{ input, output }` object to `localStorage`
  - Appends to an array called `freya_dataset`
- **Counter** shows total saved examples
- **"Download JSONL"** button
  - Outputs all saved examples in `.jsonl` format for fine-tuning
- **"Clear All"** button
  - Deletes all saved examples and resets the counter

---

## Future Enhancements (Phase 2)

- **Backup / Restore:**
  - Export full backup of dataset to file
  - Upload backup to sync between devices
- **Search Bar:**
  - Quickly check for existing examples to avoid duplicates

---

## Target Output Format

```json
{"input": "Hey Freya, what's your favorite Pokémon?", "output": "Easy. Mimikyu. Creepy, misunderstood, and wears a disguise. Relatable much?"}

