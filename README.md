# Ground Floor Academy — AI Agentic Infrastructure Masterclass

Two self-paced, offline-first courses on AI agents and the infrastructure behind them, from Ground Floor Academy, the education initiative of Ground Floor Industries.

| Course | Live site | In this repo |
| --- | --- | --- |
| **Beginner Edition v1.0.** 17 modules, 51 lessons, about 168 hours of study and practice. A complete beginner pathway from using a chatbot to controlled agent systems, with Python labs. | https://johnlyon-groundfloorindustries.github.io/ai-masterclass-preview/beginner-v1/ | `beginner-v1/` |
| **Advanced course.** 16 modules, 48 lessons, engineering labs and a capstone on enterprise agentic AI infrastructure. | https://johnlyon-groundfloorindustries.github.io/ai-masterclass-preview/ | `index.html` |

## How the courses work

- Each course is one self-contained HTML file with its lessons, simulations and a downloadable lab kit. Nothing loads from a CDN, a remote font service or a model API, so a saved copy works offline.
- Progress is stored in the browser, separately for each browser and each address. Use the export and import controls inside a course to move progress between a local copy and the hosted one.
- The simulations are educational. They are not live cloud services.

## Beginner Edition files (`beginner-v1/`)

| File | Purpose |
| --- | --- |
| `index.html` | The course, as served on the live site. |
| `Ground_Floor_Academy_AI_Masterclass_Beginner_Edition.html` | The same course under a descriptive file name, for download and offline use. |
| `Student_Getting_Started_Guide.md` | Installing Python and running the first lab on Windows, macOS and Linux. |
| `Curriculum_and_Learning_Path.md` | Modules 0–16 in six phases, with hours and a practical review rubric. |
| `Ground_Floor_Academy_Engineering_Labs.zip` | The runnable Python lab kit. It needs Python 3.10 or later and no extra packages. |
| `Developer_Source.zip` | Source used to rebuild the release files. |
| `Quality_Assurance_Report.md` | Tests run for the release and their limits. |
| `Deployment_Verification.md` | Record of the live deployment check on October 31, 2026. |
| `Source_Ledger.md` | Reference sources and the commits the release was built from. |
| `SHA256SUMS.json` | Checksums of the release files. |

The release files are checksummed. If any file in `beginner-v1/` changes, update `SHA256SUMS.json` and the checksum list in `Deployment_Verification.md` to match.

## Advanced course (`index.html`)

This is the original design preview. It uses a text wordmark and does not yet carry the official Ground Floor Industries logo or favicon. The Beginner Edition embeds the official logo.

## Viewing and updating

No installation or build step. Use the live sites, or download an HTML file and open it in a browser.

The site is published with GitHub Pages from the root of the `main` branch. A push to `main` updates it within a minute or two.
