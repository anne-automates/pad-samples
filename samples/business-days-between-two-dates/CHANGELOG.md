# Changelog - Business days between two dates

## 1.0.1 - 2026-10-07

- The gallery card shows an illustration (`assets/cover.png`). The flow did not change: no new run needed.

## 1.0.0 - 2026-10-07

- First public version: the business days between two dates, weekends and holidays left out. The local function `Get_Public_Holidays` (4 inputs, 3 outputs) reads the public holidays of a country from a public API: France in the sample, another country by changing its ISO code, a region by adding its code. The local function `Count_Business_Days` (4 inputs, 6 outputs) counts in one *Run PowerShell script* action. `Main` adds the days of the company from a CSV file; emptying one setting gives the file alone or the API alone.
- `Quick_Try` does the API call and the count in one block, without the functions. The optional `Tests` replays 59 cases through `Count_Business_Days`.
- Tested on Power Automate Desktop 2.72.183 on 2026-10-07: five subflows pasted without error; `Tests` 59 of 59 in 4 min 29 s (51 counts equal to NETWORKDAYS.INTL in Excel, 8 inputs refused with a message); `Main` gave 247 business days for France in 2026 (11 public holidays from the API, 6 company days from the file) in 21.1 s; the file alone gave 254, the API alone 252, Germany 254, France with Moselle 251; `Get_Public_Holidays` answered for FR, DE, BE, ES and IT, for the eleven years 2020 to 2030, and refused an unknown country, a year without data, a code in lower case and a date in another format; the quick try pasted into `Main` gave 252 business days in 13.7 s.
- The three header lines of the two functions (`# local subflow:`, `# inputs:`, `# outputs:`) are written in the form of the lab, and the title of region 3 of `Count_Business_Days` is shorter; comments and titles only, the actions are those of the tested run.
