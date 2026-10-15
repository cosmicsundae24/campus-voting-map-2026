# Campus Voting Sites, Texas, Nov 3 2026

One page showing, for 25 Texas college campuses, the nearest early-voting site and the Election Day site: a map per campus with labelled pins, the addresses, straight-line miles from campus, and a directions link. Built for student voter outreach.

Open `index.html` in a browser, or turn on GitHub Pages for this repo. It's a single file and needs an internet connection; the map library (Leaflet 1.9.4) loads from jsDelivr. On a website it uses OpenStreetMap tiles. OpenStreetMap's tile servers refuse pages opened straight from disk, so a local copy switches to Esri street tiles. That fallback is for quick personal viewing only; share the website link instead.

## Sources and dates
- Polling sites come from each county's posted Nov 3, 2026 early-voting and Election Day lists, checked Oct 13-14, 2026. **Counties can still move sites, so re-check the county's page before Oct 19 and again before Nov 3.**
- UTSA's room (Bexar Room, H-E-B Student Union, HSU 1.102) comes from UTSA's "Vote at UT San Antonio" page. Bexar County's list names the site as 1 UTSA Cir, and its early-voting hours match UTSA's page.
- Pins were placed by OpenStreetMap address lookup (Nominatim), with a few corrected by hand. Where the written address and the pin disagree, the written address wins.
- Miles are straight-line distances, not driving distances.

## Known gaps (also labelled on the page)
- The Waller County Community Center (Prairie View early voting) has no map pin; only the address is shown.
- Denton and Waller counties vote by precinct on Election Day. Texas Woman's University has no single Election Day site, and the UNT and Prairie View sites serve one precinct each (hollow ring on the map).
- For the Texas A&M International Election Day site, the building and room still need confirming with Webb County Elections.

## Editing
The data is the `const D = [...]` array near the bottom of `index.html`. Each entry has the campus, its county, the EV and Election Day labels and addresses, `[lat, lon]` pins, and the miles from campus.
