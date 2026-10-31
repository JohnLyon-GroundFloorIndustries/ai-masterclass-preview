# Deployment verification — Beginner v1.0

Verified October 31, 2026.

Live URL: https://johnlyon-groundfloorindustries.github.io/ai-masterclass-preview/beginner-v1/

Repository: https://github.com/JohnLyon-GroundFloorIndustries/ai-masterclass-preview

Release commit: fe6a364163ee8f7d44d2f5ed541eb92388ee9fd7

All nine public release artifacts returned HTTP 200 and matched the tested local files byte-for-byte. The original advanced course returned HTTP 200 and matched its original Git blob byte-for-byte. The commit diff changes only beginner-v1/. No Ground Floor Industries main-site repository was modified.

The live page was opened in a browser, the first lesson loaded and its simulation executed successfully. The live course was left open for review.

A fresh extraction of Developer_Source.zip rebuilt all ten initial release files byte-for-byte. This deployment record is a post-publication artifact, separate from the reproducible initial build and its checksum manifest.

See Quality_Assurance_Report.md for 36 passing Python tests, 75 JavaScript/static assertions, 51 lesson checks, 45 responsive cases and explicit verification limits.

## Published checksums

- Curriculum_and_Learning_Path.md: 3e35042ed7c6ca7c7d7cbd2b0801b833b5ebdf0af2de8f8b56c21692f736989a
- Developer_Source.zip: 56688b7a05983fc278d8077e86e1dccc6d44ac974e1199b29af2286bae3a0da0
- Ground_Floor_Academy_AI_Masterclass_Beginner_Edition.html: e46f40ce0cb9fdc25ad14388c69e9b4b78de8a8b583cbc4d4baa10a4c3e20a00
- Ground_Floor_Academy_Engineering_Labs.zip: b41c2ac4c1c417d5e025b3bb7117fcfa92dd4be776985d1d7422260fc837527c
- index.html: e46f40ce0cb9fdc25ad14388c69e9b4b78de8a8b583cbc4d4baa10a4c3e20a00
- Quality_Assurance_Report.md: da00f946ec686273e725d704273cede56325df1c3c0e19af8949885fbfab0059
- SHA256SUMS.json: 09bb728950c9d010e13386561c53d35a9c0aabb99b87c822410e881b9b85947f
- Source_Ledger.md: d1a7fe7331e66d25cbd231a24cba6670a41f0a8c511ca1c70282b3af684cfb31
- Student_Getting_Started_Guide.md: 765ef42b07e90d2cae25975ae0c2606f63e0d1bfb06bcb198505bdf855677c61
