# SideShift Mascot Co-Pilot Feature Concept
> A pitch-ready feature prototype built on top of [sideshift.app](https://sideshift.app/) to demonstrate high-impact improvements to the current UGC platform landing page, specifically around first-visit engagement, guided conversion, and brand personality.

> **Live demo:** [My prototype](https://sarthak-saharan.github.io/sideshift-rebuild/) (feature concept)

> Built by Sarthak Saharan · [LinkedIn](https://www.linkedin.com/in/sarthak-saharan/) · [Portfolio](https://sarthaksaharan.framer.ai/)

## What I Built

I rebuilt SideShift's landing page with pixel-perfect design system fidelity and layered a **Mascot Co-Pilot**, an interactive guided tour character, on top of it. The co-pilot walks new visitors through each section of the page, reducing cognitive load and driving them toward the trial CTA. I chose this feature because SideShift has a dense value proposition (creator sourcing + campaign management + payments + analytics) that risks overwhelming first-time visitors before they understand what makes the platform worth trying.

## The Problem I Spotted

SideShift's landing page communicates significant platform depth, but that is also its friction. A first-time visitor arriving from a paid ad or cold outreach sees 10+ sections of dense information with no guided path. There is no progressive engagement hook that says "let me show you around before you decide." Without that, visitors either scroll passively and leave or click the CTA before understanding the value, leading to low-quality trial signups. The page has strong social proof and metrics but they are not being surfaced in the right sequence.

## Before and After

| Dimension | Before (Original SideShift) | After (This Prototype) |
|---|---|---|
| **First-visit orientation** | Visitor must self-navigate 10+ sections with no guided path | Mascot co-pilot offers an opt-in tour that contextualises each section in sequence |
| **Feature discovery** | "How It Works" tabs require active exploration to find | Co-pilot proactively surfaces each tab and explains its relevance in plain language |
| **Engagement depth** | Linear scroll with no interactive hooks above the fold | Animated mascot + speech bubble creates a dynamic focal point that increases dwell time |
| **CTA readiness** | Trial CTA appears before visitor has processed the value stack | Co-pilot guides visitor through proof points (metrics, testimonials, comparison) before landing on CTA |
| **Brand personality** | Clean and professional but visually neutral | Mascot adds a memorable, humanised brand moment without breaking the design system |

## Target Metrics

If this feature shipped, I would track it against:

- **Time on page: +30 to 45%** — interactive co-pilot tours consistently increase dwell time by keeping users engaged rather than bouncing after the hero
- **Trial sign-up conversion: +10 to 18%** — guided onboarding flows that sequence value before the CTA reduce friction and improve intent quality at signup
- **Scroll depth: +25%** — visitors who engage with the co-pilot are pulled through sections they would otherwise skip, exposing them to testimonials and the comparison table
- **Bounce rate: 12 to 20% reduction** — the mascot creates an immediate engagement hook in the first 5 seconds, the window where most cold-traffic bounces happen

## How I Built It

- **Research:** Analysed SideShift's product positioning (UGC OS for brands), target audience (DTC/e-commerce growth teams), and full landing page structure including all 11 sections, copy hierarchy, and CTA strategy
- **Design extraction:** Pulled exact design tokens directly from the live site via DOM inspection, no guessing:
  - Font: `Geist` (Vercel) loaded from jsDelivr CDN
  - Primary button: `linear-gradient(rgb(81,81,81) 0%, rgb(32,32,32) 100%)` + noise texture from `sideshift.app/noise.avif`
  - H1: `69px`, `font-weight: 700`, `letter-spacing: -3.45px`, `line-height: 0.9`
  - Section gradients: `linear-gradient(180deg,#FFFFFF 0%,#E0F5FF 30%,#D0EDFF 50%,#E0F5FF 70%,#FFFFFF 100%)`
  - Header: transparent on load, light blue gradient (`#E0F5FF to #F0FAFF to #FFFFFF`) on scroll with `cubic-bezier(0.64,-0.01,0,1)` transition
- **Stack:** Vanilla HTML/CSS/JS, single file, zero dependencies, ships anywhere
- **Fidelity highlights:** Replicated the noise-texture dark gradient pill button, the scrolling brand logo marquee, the auto-scrolling testimonial carousel, and the sticky header scroll transition, all extracted from the live DOM, not approximated

## Run It Locally

```bash
git clone https://github.com/sarthak-saharan/sideshift-rebuild.git
cd sideshift-rebuild
python3 -m http.server 3000
# Open http://localhost:3000
```

## About Me

I am Sarthak Saharan, an AI-native Product Manager who builds working prototypes to validate ideas before writing a single line of a PRD. I diagnose UX and conversion gaps by going deep on the product, then ship proof-of-concept features that show exactly what the fix looks like, live, in the real design system, not in a Figma frame.

[LinkedIn](https://www.linkedin.com/in/sarthak-saharan/) · [Portfolio](https://sarthaksaharan.framer.ai/)

*Demo data only. Not affiliated with SideShift. Built as an unsolicited product concept.*
