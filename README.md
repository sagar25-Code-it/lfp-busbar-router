# PS3D LFP Busbar Designer

PS3D LFP Busbar Designer is a browser-based battery pack layout and routing calculator for planning Lithium Iron Phosphate cell layouts, series/parallel connections, busbar routing, and electrical checks.

It helps you create a pack layout, connect cells visually, estimate total output, and check whether busbar routing is clean before moving to real mechanical or electrical design.

## How To Use

1. Open the tool in your browser.
2. Set the pack layout using row and column controls.
3. Add or remove cells as needed.
4. Enter the cell details:
   - Nominal voltage per cell
   - Capacity per cell in Ah
   - Cell max current
   - Design current
   - Busbar width
   - Busbar thickness
5. Click **Auto Series** to generate automatic busbar connections.
6. Use **Best Cost Layout** to let the tool choose a shorter routing layout for the active cell count.
7. Click any cell terminal to manually create a busbar connection.
8. Drag a busbar line to adjust its route manually.
9. Use each cell's **Flip** button to swap that cell's polarity.
10. Use the always-visible row and column buttons to flip a full row or column at one time.
11. Connect final output to the bottom main positive and negative terminals.
12. Check the output and electrical result panels before using the design.

## Special Features

- Responsive PS3D Master light-theme engineering interface.
- Branded header with direct owner portfolio, LinkedIn, Instagram, and email actions.
- Highlighted Sagar Patel owner profile and online CV callout.
- Auto-scrolling PS3D engineering tool suite in the marketing footer.
- Custom cell layout with adjustable rows and columns.
- Add, remove, restore, and rearrange active battery cells.
- Automatic series connection without changing cell position.
- Cell terminal flip while keeping the terminal physical position stable.
- Always-visible row and column terminal flip buttons for faster layout editing.
- Automatic busbar endpoint rearrangement after a cell, row, or column flip.
- Manual busbar creation by clicking terminals.
- Draggable busbar routing lines for final route adjustment.
- Target topology input such as `36S1P`.
- Stronger topology validation from main negative to main positive.
- Validation panel for topology, route clearance, output readiness, and paid pending items.
- Project JSON save/load.
- Route CSV export.
- Technician build sheet CSV export.
- Annotated layout SVG export.
- Print-ready engineering report export for PDF generation.
- Smart routing that tries to avoid terminal and busbar overlap.
- Outside-layout routing for bend connections and main terminal output routing.
- Straight/direct routing for nearby cell-to-cell connections when clear.
- Red and black color-coded main output connection lines.
- Bottom dummy main positive and negative terminals for final pack output.
- Layout optimizer for shorter, more cost-effective routing.
- Live pack output calculation:
  - Series count
  - Parallel count
  - Pack voltage
  - Pack capacity in Ah
  - Estimated energy in Wh
- Electrical check calculation:
  - Max pack current
  - Design C-rate
  - Estimated busbar length
  - Busbar resistance
  - Voltage drop
  - Busbar heat loss
  - Estimated copper mass
  - Routing status and overlap warning

## Pending Paid / Proprietary Items

These items are listed as pending because they require licensed standards data, manufacturer datasets, or certified simulation/correlation:

- Licensed creepage and clearance lookup tables from applicable standards.
- Certified thermal/electrical simulation solver correlation.
- Manufacturer-specific fuse, contactor, and busbar material databases.

## Important Safety Note

This tool is a layout helper only. Real battery pack design can involve high current, short-circuit risk, heat generation, insulation clearance, fusing, BMS selection, vibration, enclosure design, and safety certification. Always verify the final design with a qualified battery/electrical professional before manufacturing or assembly.

## Files For Deployment

- `public/index.html` - main web app
- `public/ps3d-brand-logo.webp` - optimized PS3D Master brand mark
- `public/robots.txt` - crawler access and sitemap location
- `public/sitemap.xml` - canonical production URL for search indexing
- `render.yaml` - Render static-site deployment configuration
- `.gitignore` - common ignored files

Upload the complete package so the HTML and logo asset remain together. No paid runtime dependency is required for this static deployment.

## Search Identity

- Official name: **PS3D LFP Busbar Designer**
- Category: **Battery Pack Layout & Routing Calculator**
- Canonical URL: `https://lfp-busbar-router.onrender.com/`
- Primary branded search: `PS3D LFP Busbar Designer`

After deployment, submit `https://lfp-busbar-router.onrender.com/sitemap.xml` in Google Search Console and request indexing for the canonical URL.
