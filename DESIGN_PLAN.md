# Erika & Hilde — evidence-led website plan

Status: **implemented as a demo branch after approval in chat**. This document remains the source-of-truth for launch QA.

## 1. Evidence baseline

### Current facts used in the implementation

| Fact | Evidence | Implementation decision |
| --- | --- | --- |
| Business | Erika & Hilde, bar | Current Google/local business listing |
| Address | Weigandufer 9, 12045 Berlin-Neukölln | Published in hero and visit section |
| Phone | +49 177 8370797 | `tel:` CTA |
| Google rating | 4.6 / 5 from 192 reviews | Visible social proof, dated Sept. 2026 |
| Google price band | €1–10 | Used only as contextual proof; no menu prices invented |
| Current listing hours | daily 16:00–01:00 | Displayed as “currently listed online”; not treated as owner-confirmed |
| Official legacy-site hours | daily from 15:00 | Documented as a discrepancy requiring owner confirmation |
| Operator | Amos & Knoll GbR; represented by Ralf Amos and Christine Knoll | Impressum draft only |
| Outdoor seating | Current third-party listing | Mentioned only as current listing evidence, not as a guaranteed policy |
| Community use | Berlin Writers’ Workshop meetups at Erika & Hilde in 2024–2026 | Community proof, explicitly described as third-party gatherings |
| Historical concept | By May 2010: Franconian/Swabian pub character, Brotzeit, Wettelsheimer beer, homemade food/cake | Archive story only; never presented as today’s menu |
| Recent beer evidence | Wettelsheimer Hell (2025) and Wettelsheimer Wet Premium Pils (May 2026) check-ins | Supports beer heritage; does not guarantee permanent stock |

### Sources

- Current local business listing surfaced Sept. 2026: Google business data for Erika & Hilde, Weigandufer 9.
- Official legacy homepage: https://erikaundhilde.de/index.php/de/
- Official legacy imprint: https://www.erikaundhilde.de/index.php/de/impressum
- Current review/listing mirror: https://de.restaurantguru.com/Erika-and-Hilde-Berlin
- Beer activity: https://untappd.com/v/erika-und-hilde/922165
- 2010 archive: https://leckeressen.blogspot.com/2010/
- Berlin Writers’ Workshop events: https://berlinwritersworkshop.com/events
- Weigandufer licensed reference image: https://commons.wikimedia.org/wiki/File:Weigandufer_12-16_(Berlin-Neuk%C3%B6lln).jpg

### Facts intentionally not invented

No reservation policy, delivery/takeaway policy, full menu, current item prices, payment methods, accessibility policy, smoking policy, staff biographies, social accounts, or exact founding year are asserted as owner-confirmed facts.

**Launch blocker:** reconcile 15:00 vs 16:00 opening time with the operator before commercial launch, then update the visible site and structured data together.

## 2. Audience

Primary audience: neighbourhood residents and people already moving through northern Neukölln who want an uncomplicated place to stop, meet, talk, read, or have a drink.

Secondary audiences:

- people walking or cycling along Weigandufer / the Neuköllner Schifffahrtskanal;
- visitors comparing nearby Weserstraße bars but looking for something less cocktail-led;
- writers, newcomers and small social groups looking for a relaxed meeting place.

German is primary. An English mirror is included because recurring English-language community events are evidenced.

## 3. Conversion goals

1. **Get directions** — the primary conversion.
2. **Call** — a one-tap secondary conversion.
3. Establish confidence in under ten seconds: place, atmosphere, current listed hours, address, rating, and what kind of offer is publicly evidenced.

No booking/order CTA is shown because those capabilities are not verified.

## 4. Creative direction

Traits: **warm, classic, editorial, tactile, understated, local**.

Concept: **“A neighbourhood newspaper pinned up in a warm living room beside the canal.”**

The design deliberately avoids luxury cocktail-bar tropes, faux-Berlin graffiti, neon nightlife visuals, and over-produced restaurant photography. The site should digitize the place’s character rather than “upgrade” it into something else.

## 5. Color system

| Token | Value | Use |
| --- | --- | --- |
| Paper | `#F1E9DA` | Main background |
| Soft paper | `#FBF8F1` | Cards and light sections |
| Ink | `#221F1A` | Main text |
| Muted ink | `#665F55` | Supporting copy |
| Oxblood | `#6B3B34` | CTA and strong accents |
| Canal green | `#53685A` | Secondary accent |
| Lamp amber | `#C77C35` | Small warm highlight |
| Rule | `#CFC3B1` | Borders and editorial rules |

All important text/background pairs must meet WCAG 2.2 AA.

## 6. Typography

Implementation uses a system-first stack to avoid third-party font requests and unnecessary dependencies:

- Display: Iowan Old Style / Palatino / Georgia / serif.
- UI/body: Helvetica Neue / Arial / sans-serif.

If production receives owner-controlled webfont files, Source Serif 4 + IBM Plex Sans are good replacements, self-hosted as WOFF2.

## 7. Image strategy

### Production preference

1. Owner-controlled current photography.
2. Newly commissioned photography with commercial usage rights.
3. Clearly licensed neighbourhood imagery.

### Demo-only imagery currently used

The implementation uses real business imagery found online to make the prototype business-specific. Those images are visibly marked **“Demo image — replace before commercial launch”** because reuse rights are not established:

- LaptopFriendly interior photograph: https://laptopfriendly.co/berlin/erika-hilde
- Restaurant Guru Erika & Hilde collage: https://de.restaurantguru.com/Erika-and-Hilde-Berlin
- 2010 blog archive interior/food photographs: https://leckeressen.blogspot.com/2010/

These must be replaced with owner-controlled/commissioned assets before commercial deployment.

### Production-safe contextual image

A Weigandufer photograph by Bodo Kubrak is CC BY-SA 4.0 and may be used with attribution and license link:
https://commons.wikimedia.org/wiki/File:Weigandufer_12-16_(Berlin-Neuk%C3%B6lln).jpg

The caption must make clear that it depicts Weigandufer nearby, not Erika & Hilde itself.

### Photography brief

Capture: exterior with signage, canal relationship, outdoor tables, wide interior, lamps/newspapers/chairs, bar/service detail, current beer/drinks, any actual food available that day, and optional owner/team portrait with consent.

## 8. Information architecture

```text
/
├── Hero / immediate visit info
├── Why this place
├── What is publicly evidenced today
├── The room / atmosphere
├── Archive / story
├── Community use
├── Gallery
├── Social proof
└── Visit / directions / contact

/en/
/impressum.html
/datenschutz.html
```

No standalone menu/events page is created until there is an owner-maintained data source.

## 9. Section-by-section layout

### Header
Small wordmark, anchor navigation, DE/EN switch and a prominent directions CTA. Mobile uses a compact sticky action bar for directions and call.

### Hero
Real Erika & Hilde interior photo, business name, Weigandufer 9, concise value proposition, current-listed-hours wording, directions + call.

### Proof strip
4.6 Google rating / 192 reviews / Neukölln / canal-side address context.

### Value proposition
Three evidence-led pillars: canal location, unpretentious atmosphere, and a place people repeatedly use to meet.

### Current offer
Not a fabricated menu. It says exactly what public current sources support: beer, coffee, Spritz/drinks, Proviant Cola mentioned by guests, and occasional cheesecake mentioned in a recent review. It explicitly says the full current menu is not reliably published online.

### Real space
Photography-led editorial block around lamps, couches/chairs, newspapers and the lived-in interior character visible in available images and review descriptions.

### Archive/story
“Documented at Weigandufer by 2010.” Historical Franconian/Swabian identity, Wettelsheimer beer, Brotzeit and homemade cake appear only as archive material, with a clear note that this is not today’s menu.

### Community
Evidence from recurring Berlin Writers’ Workshop meetups. Copy makes clear these are third-party groups that chose the venue, not events operated by Erika & Hilde.

### Gallery
Rather than a generic carousel, real photography is distributed editorially through the place, archive and neighbourhood sections. This keeps images tied to the evidence they support and avoids duplicating low-resolution third-party assets.

### Social proof
Aggregate rating and summarized recurring themes (relaxed atmosphere, friendly service, canal location, fair prices). No scraped long-form customer quotes.

### Visit
Address, current listed hours, phone, directions. Prominent note that hours require owner reconciliation because the legacy website differs by one hour.

### Final CTA
“Bis später am Weigandufer.” + directions.

## 10. Three.js / animation plan

No Three.js. It does not add to the story and would add weight, battery use and accessibility complexity.

Motion is limited to CSS hover/focus transitions and a very small first-paint fade. `prefers-reduced-motion: reduce` removes nonessential transitions and smooth scrolling.

## 11. Responsive behavior

Mobile first. Under 640px, the order is: identity → place photo → address/hours → directions/call → offer → story/community → gallery → visit. Touch targets are at least 44×44px. Desktop uses editorial asymmetry rather than stretching content edge-to-edge.

## 12. Accessibility

Target WCAG 2.2 AA:

- semantic landmarks and one H1;
- skip link;
- logical headings;
- keyboard-accessible links/navigation;
- `:focus-visible` states;
- no hover-only content;
- meaningful alt text;
- decorative images have empty alt where appropriate;
- language declared per page;
- reduced-motion behavior;
- no autoplay media;
- content remains useful without JavaScript (the implementation uses no required JavaScript).

## 13. Performance

Static HTML + CSS, no framework, no Three.js, no analytics, no embed-heavy map.

Current demo-only remote imagery is the largest performance/privacy compromise. Before launch, replace it with local AVIF/WebP files with explicit dimensions and responsive `srcset`. Target LCP < 2.5s, CLS < 0.1, INP < 200ms.

## 14. SEO / local discovery

German title direction: **Erika & Hilde | Bar am Weigandufer in Berlin-Neukölln**.

Meta description focuses on location, current listed hours and directions. JSON-LD uses `BarOrPub`, address, telephone and geo only where evidence is strong. Opening-hours structured data is intentionally omitted until the 15:00/16:00 discrepancy is resolved.

Open Graph title/description/type/url are included. `og:image` is intentionally omitted until an owner-controlled social-share image exists.

## 15. Rights/licensing notes

- Real-business photos in this prototype are editorial/demo references and visibly marked for replacement.
- The Weigandufer contextual photo is CC BY-SA 4.0 by Bodo Kubrak; attribution and license link are retained.
- No full Google reviews are copied into the site.
- Owner/team biographies are not inferred from the legal imprint.
- The legal pages are implementation drafts, not a substitute for German legal review.

## 16. Implementation sequence

1. Research refresh and evidence register.
2. Write this plan.
3. Build German semantic HTML.
4. Build English mirror.
5. Add responsive editorial CSS and reduced-motion rules.
6. Add evidence notes, image-rights badges and source links.
7. Add minimal Impressum and privacy draft.
8. Validate HTML structure, internal links, accessibility basics and JS-free fallback.
9. Replace demo images and reconcile hours before commercial launch.
10. Deploy only after owner/legal/content sign-off.

## 17. Acceptance criteria

- [x] No invented price, service, reservation policy or full menu.
- [x] Current Google/local listing facts are dated and source-backed.
- [x] 15:00 vs 16:00 discrepancy is disclosed; not silently resolved.
- [x] Directions and call actions are obvious on mobile.
- [x] Real-business imagery is used where possible.
- [x] Every unlicensed/editorial business image is visibly marked demo-only.
- [x] Licensed Weigandufer image carries attribution.
- [x] Historical products are marked archive-only, not today’s menu.
- [x] Community events are described as third-party groups choosing the venue.
- [x] Semantic HTML and keyboard focus states are implemented.
- [x] Reduced-motion support is implemented.
- [x] No Three.js, framework or unnecessary dependency.
- [x] Static fallback is the primary experience; JavaScript is not required.
- [x] LocalBusiness/BarOrPub JSON-LD contains only strong facts.
- [x] Open Graph metadata is present without inventing an owned OG image.
- [ ] Replace demo/editorial images with owner-controlled files before commercial launch.
- [ ] Confirm exact opening hours with operator and update site + Google + structured data.
- [ ] Confirm current menu, payment/accessibility/smoking policies if the production site should publish them.
- [ ] Have Impressum/Datenschutz reviewed for the final hosting/data setup.
