# HEMS Testbed — Editorial alternative

This is a separate design variation. The original `hems-testbed` project and its downloads are preserved unchanged.

Design: TUM blue on white; a large typographic heading, fine section rules, an unboxed engineering schematic, and research content arranged in horizontal rows. German is the default. Both portrait and landscape diagrams are included.

# HEMS Testbed · CoSES · TUM

A bilingual English/German, single-page static website. Open `index.html` in a browser. The site uses plain HTML, CSS, JavaScript, local logos and a local photograph. No build, package installation, backend or external font service is required.

## Publish on GitHub Pages

Prepared for a new **public** repository named `hems-testbed` under `anuragmohapatra90`. Publication has not been performed: the connected GitHub tools can edit existing repositories but do not expose repository creation or Pages settings, and no suitable repository was accessible.

1. Create the public repository on GitHub. Initialize it with a README if you want the connected assistant to upload the site in a follow-up.
2. Upload `index.html`, `.nojekyll`, and the complete `images` folder into the repository root. If using this archive, extract it first; do not upload the ZIP as the website. You may also include this README and `SOURCE_NOTES.md`.
3. Open **Settings → Pages → Build and deployment**. Set **Source** to **Deploy from a branch**, choose **main** and **/(root)**, then **Save**.
4. Wait for the Pages build to complete. The Pages settings will display the verified live URL.

For the account and repository name above, the expected address after a successful deployment is `https://anuragmohapatra90.github.io/hems-testbed/`. This is an expected address, not a confirmed live website.

GitHub Pages is available for public repositories on GitHub Free. Instructions checked against the official documentation on 15 September 2026:

- [What is GitHub Pages?](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)
- [Configure a publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

After the repository is created, make it accessible to the connected GitHub app and share its URL with the assistant. The assistant can then upload the prepared files; Pages settings still require an available admin capability or the short manual step above.

## Replace the testbed photograph

Upload your new photograph as **`images/testbed.jpg`**, replacing the existing file. A landscape image around 4:3 works best. The current image comes from the supplied CoSES slide deck.

Search for **`TESTBED PHOTO`** in `index.html`. Update the English `alt` text, German `data-de-alt` text, and the caption in both languages. If the filename changes, also update the image's `src`. Commit the change to republish it.

This is a static website: photo updates happen through the repository. There is no visitor upload form. If the photograph is missing, the frame displays a bilingual placeholder.

## Edit content

- English text is written directly in the HTML. Its German translation is stored in the same element's `data-de` attribute.
- `data-de-aria`, `data-de-alt`, and `data-de-href` translate accessibility labels, photo descriptions and links.
- The language buttons update the page without a reload, including the schematic and its accessible description. German is the default; append `?lang=en` for an English-first link.
- CSS is inside `<style>`; language switching is inside `<script>`.
- The central schematic is inline SVG. Blue solid lines are electrical connections; teal dashed lines are always-visible HEMS access/communication.
- At 960 px and below, a dedicated portrait schematic replaces the desktop diagram. It reorganizes the same topology into a vertical AC-bus layout, keeps the PV/battery and charger/vehicle pairings explicit, and requires no horizontal scrolling. An expandable text description presents the same connections in prose.

## Logos

- `images/phylflex-logo.png` is a high-resolution transparent-background rendering of the supplied `PhyLFlex_Logo.pdf`, without redrawing the logo. It sits on the white hero area so its full form remains clear.
- `images/tum-logo.svg` reproduces the exact mark used in the current official TUM website header. Its blue artwork is intended for the white masthead.
- Keep both logos undistorted and retain their surrounding whitespace.

## Content and scope

The specification values come from brochure page 2. Current and planned capabilities are separated. The schematic is a functional overview, not an electrical installation drawing. A controllable DC source emulates PV generation and supplies the real PV inverter; no physical PV modules are connected. The real EV charger feeds the vehicle emulator through Type 2; the vehicle emulator is not drawn as an independent parallel household load. The battery's DC connection follows the supplied slide schematic.

See `SOURCE_NOTES.md` for source mapping and the validation limitation. The original PDFs and experimental validation report are not bundled into the public website.

## Checks performed

JavaScript syntax, local image references, in-page navigation targets, unique HTML IDs, translation coverage, and schematic label widths were checked. The photograph and both language versions of the schematic were visually inspected using static rendering. Full browser interaction/mobile rendering and live GitHub Pages deployment have not been verified.
