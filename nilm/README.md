# NILM page

Static GitHub Pages page at https://makonin.com/nilm/. Uses the root `style.css`, portrait, and favicon; all additions are isolated to this directory. No JavaScript, build step, external fonts, analytics, or embedded video players.

## Content provenance (reviewed 2026-09-27)

- `SMakonin_DSM2017.pdf`: user-supplied, unmodified presentation, *The Expectations of Non-Intrusive Load Monitoring*, DSM Taiwan, November 21, 2017. Slides 4–6: definition and motivation; 7–10: anatomy and learning; 11–15: sampling and load states; 16–18: feedback, tools and datasets; 19–21: consumer rights, multi-fuel disaggregation and eco-visualization; 22–37: expectations; 38: further reading.
- The diagram is an accessible HTML simplification, not a reproduction of the slide’s block geometry. The optional feedback loops are explained in prose.
- The historical savings percentages and accuracy expectations are explicitly contextualized; no savings, accuracy, or quantum-advantage guarantee is made. The 2017 emuNILM release proposal is not represented as a verified current tool.
- Publication metadata: https://github.com/smakonin/Publications/blob/main/publications.bib . The library has no per-paper anchors or supported search URL; links therefore use `/Publications/`, its actual author-version PDF paths, and DOI destinations, without invented anchors. Stephen Makonin is bold in author lists.
- Software descriptions checked against public GitHub repository metadata and READMEs: SparseNILM, Gaussian-NILM, KP-NILM, WaterNILM, NILM_PerformanceEval, Q.NILM, uDisagg, AMPds, RAE.dataset, HUE.dataset, R1Hz.dataset. Related tools: eco-vis, DataWrangle_REDD, upstream nilmtk/nilmtk.
- Q.NILM was anonymously readable through the public GitHub API and raw README. Its README still has pre-publication visibility wording; this page links the research repository without implying publication acceptance or a verified packaged release.
- uDisagg’s README still says the thesis source has not been released; the page discloses that limitation.
- Dataset references: AMPds2 DOI 10.7910/DVN/FIE0S4, RAE DOI 10.7910/DVN/ZJW4LC, HUE DOI 10.7910/DVN/N3HGRN, R1Hz DOI 10.7910/DVN/RCB5VJ. HUE is building-level hourly data, not an appliance-ground-truth NILM benchmark. R1Hz’s recovery markers and mixed circuits require care.
- Videos verified against channel listing and YouTube oEmbed title/author metadata. Channel: https://www.youtube.com/@StephenMakonin (`UCuePk8HukBZwNKndziZyYdg`, display name “Prof. Stephen”). Video IDs: `qlpGfFg4bME` (What is NILM?), `pjzsigt3Cfo` (What is Ambient Energy Feedback?), `DF4ELRCvnIo` (A Consumer Bill of Rights for Energy Conservation). The latter two are labelled related context. Metadata verification does not establish playback availability in every region.

## Maintenance

Keep inherited theme changes in the root stylesheet; NILM-only overrides belong in `nilm.css`. Check at desktop and mobile widths, keyboard navigation, fragment targets, local assets, publication PDFs, DOI resolution and video ownership when updating. Preserve the homepage unchanged unless separately requested.

## Verification

- Local static-server preview checked at 1440, 768, and 390 px: no document overflow, console errors, or failing page assets; one H1 and a working keyboard-first skip link.
- All local files and fragment targets checked. All 11 author-version PDFs and all linked GitHub repositories returned HTTP 200. Three video watch pages and YouTube oEmbed ownership/title metadata checked.
- All four dataset records confirmed RELEASED via Harvard Dataverse’s API. Publication DOI titles checked against Crossref where publisher pages return anti-bot responses; the remaining directly readable DOI pages were checked by HTTP response.
- `ampds.org` currently has a hostname-mismatched HTTPS certificate. Its working HTTP site is used alongside secure DOI/Dataverse links. MDPI blocked automated page retrieval (403); its RAE DOI is independently registered with the expected title. Some IEEE pages respond with HTTP 202 instead of article HTML. These do not establish full publisher-page rendering or universal video playback.
