# AMPds website migration

Migrated from smakonin/ampds.org commit 8354a1c9719dbc77aec5f19bc1f2ae97789b8e89 to https://makonin.com/ampds/.

## Scope

- Preserves the original content, citation records, fixed-width layout, logo, favicon, stylesheet, and four bundled WOFF fonts.
- Relative asset paths resolve inside /ampds/; font URLs remain relative to font/font.css.
- Adds an English language attribute and the new canonical URL; sitemap.xml contains the new URL without the old stale last-modified date.
- Replaces obsolete /doc/ publication links with their corresponding HTTPS DOIs; dataset DOI links use HTTPS. The original Dataverse direct-download URLs remain intact.
- NILM navigation points to /nilm/, the author link points to /, and the existing NILM page links back to /ampds/.
- Preserves Google Translate and StatCounter (including existing project ID); explicit widget and noscript URLs use HTTPS.
- Does not copy the old CNAME or robots.txt: these are domain-root configuration, not subdirectory settings. The existing makonin.com CNAME and homepage are unchanged. No redirect is installed or configured in the source repository.

## GitHub Pages and verification (2026-09-27)

The destination publishes from master at repository root using GitHub Pages' legacy build. This directory is plain static HTML/CSS/assets, with no front matter, plugins, server-side code, or build dependencies.

All 11 local HTML/CSS references resolve, including the four font URLs and root navigation. Browser preview at /ampds/ displays the original layout, logo, typography, and Google Translate selector; no warning/error console entries were observed. The homepage was compared byte-for-byte with HEAD. The original fixed-width mobile behavior is retained.

External checks: Nature and HUE article URLs and Google Translate/StatCounter endpoints returned HTTP 200. MDPI returned HTTP 403 to automated checks. Dataset DOIs resolve to Harvard Dataverse (HTTP 202); direct CSV/HDF5 download checks returned HTTP 403, including a ranged GET attempt. These external-service restrictions could not be resolved by this static-site migration. The dataset DOI link remains the alternative route to downloads. No dataset binaries were present in the source repository to migrate. Translation and analytics remain dependent on their third-party services; translation beyond selector rendering and analytics account reporting were not verified.
