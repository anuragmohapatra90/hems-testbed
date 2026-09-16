# Source notes

## Brochure, page 2

Source: `Blue and White Modern Company Plumbing Solutions Brochure (1).pdf`, supplied in the conversation.

Used for:

- HEMS Wall positioning: real hardware/firmware, electrical power, sensors, reproducible daily and seasonal profiles.
- PV 12 kW; EV charging 11 kW; battery from 6.1 kWh; heat-pump load up to 12 kW; grid connection up to 40 kW.
- Testing algorithms/forecasts, interoperability, grid-friendly behaviour and dynamic tariffs.
- Current real PV-inverter/battery/EV-charger hardware, controllable-DC-source PV simulation, SG-Ready load emulation, 1-second measurement and analysis, and digital-twin extension.
- Planned real heat pump and thermal home prosumer, and iMSys functions with Fraunhofer IEE. These remain explicitly planned on the page.
- Contact addresses `anurag.mohapatra@tum.de` and `m.erhart@tum.de`.

The brochure mentions an open-source repository but gives no repository URL. The site describes this capability without inventing a download link.

## Rennes slide deck

Source: `Rennes_DataDrivenPHIL(1).pdf`, supplied in the conversation. PDF page numbers below are one-based; printed slide numbers differ.

- PDF pages 22–25: rationale for benchmarking, research/regulatory/real-world perspectives, reference profiles and objectives, PhyLFlex context.
- PDF pages 26–28: 1-second HEMS timescales; commercial inverters; Python simulation layer; Modbus TCP and MQTT; pandapower / Gridlock integration.
- PDF page 28 (printed slide 30): functional hardware architecture, DC battery/PV-inverter relationship, measured house bus and regenerative emulator concept.
- PDF page 29 (printed slide 31): the photograph used in `images/testbed.jpg`, extracted directly from the deck. Its original commissioning statements were not republished as current status claims.

The simplified landing diagram omits individual transformers, rectifiers, metering/protection hardware and regenerative paths. Its expandable explanation states this. The site uses the brochure's HEMS-specific ratings, not ratings for the wider CoSES laboratory in the slide appendix.

## User's topology requirements

- Real PV inverter supplied by a controllable DC source acting as the PV simulator; no physical PV modules are connected.
- Three additional inverters emulating household demand, an SG-Ready heat pump, and an electric car through a Type 2 plug.
- Grid-connected house with HEMS access to all devices in full prosumer mode.
- A replaceable testbed photo area.
- One static page in English and German, with GitHub Pages as the requested host.

The three emulated devices are explicitly differentiated from the real devices. The heat-pump card uses the same inverter symbol as the other two emulators and is labelled Emulator 02.

The page contains two views of the same functional topology: a landscape desktop schematic and a portrait mobile schematic shown at 960 px and below. The mobile view uses a vertical house AC bus and straight pairwise DC/Type-2 connections so it fits a narrow screen without sideways scrolling.

## Validation report

Source: `validation_interactive.html`, supplied in the conversation. Run `20260805T152151.971182Z_pv1-python-pv-day-5kw`.

The report describes **partial** validation of one 600-second PV-emulator experiment. It reports approximately 71% modeled maximum-power capture after inverter startup and a one-cycle-delayed response at 1 Hz, requiring a faster inner voltage-to-current servo or implementation inside the source. Safe completion does not establish complete validation of the testbed.

The public page therefore makes no claims of full validation, demonstrated benchmark accuracy, or certified regulatory compliance. The brochure's 1-second measurement capability is not presented as sufficient bandwidth for the PV emulator's inner control loop.

## Website instructions

Source: `how-to-make-a-website-for-this.txt`, supplied in the conversation.

Used the requested lightweight static architecture, top-level EN/DE switch, diagram-first landing, Test / Use / Extend structure, technical details and contact section. The user's explicit GitHub Pages choice takes precedence over the file's preference for Cloudflare Pages.

## Assets and dependency notes

All graphical schematic elements are inline SVG. No stock images, generated imagery, third-party scripts, remote fonts, trackers or cookies were added. Replace the supplied testbed photograph by uploading a new file at the documented path.

The PhyLFlex logo is rendered directly from the supplied `PhyLFlex_Logo.pdf`, with the white page background removed, and placed on the white hero area. The TUM mark uses the exact SVG path from the current official TUM homepage header: <https://www.tum.de/>. The public TUM Corporate Design hub is linked from the official homepage, but its detailed logo-download area requires TUM sign-in, so no unverified minimum-size or clear-space rule is claimed.

No public HEMS repository or deployment was created during this build. The connected account was verified as `anuragmohapatra90`, but the exposed GitHub tool surface did not provide repository creation or Pages configuration. Accessible unrelated private repositories were not modified.

## Alternative design

This independent copy retains the approved technical content and both diagram topologies. Presentation draws on Swiss typography and industrial-design ideas in the user-supplied reference: https://github.com/ConardLi/garden-skills/blob/main/skills/web-design-engineer/README.md#style-recipe-gallery. No remote code or skill was installed. Only general design principles were used. Section headings were made factual; technical claims were preserved.
