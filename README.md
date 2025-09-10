InfoBasic is the quiet engine behind a lot of serious banking systems. There’s power here—multi-value arrays, terse I/O, industrial workflows—yet most materials feel like manuals, not mastery. This repo flips that script:

- **Tiny, purposeful programs** that teach one sharp idea at a time.
- **Obsidian notes** designed for deep reading, linking, and resurfacing—your second brain for mvBASIC.
- **Production-flavored context** (Temenos/T24, AA/arrangements, CIF, FX) so concepts stick.

---
## Who it’s for

- **New T24/Temenos engineers** who want a legible path into mvBASIC.
- **Backend devs** crossing over from Java/JS/Python who want the “mv” mental model quickly.
- **Banking technologists** who learn best by _editing code, not reading lore_.

---
## What you'll actually do

- Build and mutate **dynamic arrays** with `@FM/@VM/@SM` until nested data feels natural.
- Read/write records like it’s second nature (`READ`, angle-bracket extracts, `REPLACE`).
- Wire tiny utilities that mirror _real_ CBS tasks—formatting, validations, GL hints.    
- Translate between **business artifacts** (customer, deals, fees) and **program state**.

---
## Code Example

```basic
* src/ARRAY_DEMO.b
* One file. One idea: nested values without ceremony.

CUSTOMER = 'John Doe' : @FM : 'MTN Rwanda' : @VM : '0788000000' : @SM : '0788111111'

CRT "Name: "      : CUSTOMER<1>          ;* John Doe
CRT "Operator: "  : CUSTOMER<2,1>        ;* MTN Rwanda
CRT "Phone #1: "  : CUSTOMER<2,2,1>      ;* 0788000000
CRT "Phone #2: "  : CUSTOMER<2,2,2>      ;* 0788111111

* Evolve the structure in-place—no schema migration ceremony.
REPLACE CUSTOMER<2,1> WITH "Airtel Rwanda"
CRT "Updated Operator: " : CUSTOMER<2,1>
```

---
## Contribute

**Found a cleaner idiom? A sharper micro-lab?**  
Open a PR that improves **one** note or **one** program. Add a crisp header comment: what it teaches, any inputs/outputs, and one gotcha you hit.

---
## License

MIT. Use it, ship it, teach with it.