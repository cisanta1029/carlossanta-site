# Project: carlossanta.com landing page

## Overview
A single-page personal landing page for Carlos Santa (Data Scientist / Analytics Lead, Verizon). Currently carlossanta.com just redirects to LinkedIn. Goal: replace that with a real, simple page.

## Scope (keep this tight, do not expand without asking)
One page only. Five sections, in this order:

1. Header — name + one-line title
2. Intro — short bio paragraph
3. Highlights — 4-5 lines of background
4. Featured project — LogosTransformer
5. Links — LinkedIn, GitHub, résumé download

No blog, no additional pages, no CMS. This is meant to ship fast.

## Tech decisions
- Plain HTML/CSS. No framework, no build step, no JS framework.
- Small amount of vanilla JS is fine if needed (e.g. for a subtle interaction), but keep it optional.
- Hosting: GitHub Pages, connected to the existing carlossanta.com domain.
- Design goal: clean and considered, not a default template look. Confident use of type and whitespace over heavy decoration.

## Draft copy (edit freely — this is a starting point, not final text)

### Header
Carlos Santa
Data Scientist & Analytics Lead — Marketing Measurement & Causal Inference

### Intro
I'm a data scientist and analytics lead with over 16 years of experience across business intelligence, marketing analytics, and applied data science. At Verizon, I build the measurement frameworks that connect marketing decisions to real outcomes, working as the translator between technical modeling teams and the stakeholders who act on what they find. I hold an M.S. in Analytics from Georgia Tech, completed while working full-time and raising three young kids.

### Highlights
- 16+ years in business intelligence, marketing analytics, and data science; currently Data Scientist / Analytics Lead at Verizon
- M.S. in Analytics (Data Science specialization), Georgia Tech
- B.S.B.A. in Finance and Accounting, Boston University
- Designs causal inference frameworks (nested RCTs, difference-in-differences) for marketing measurement at scale
- Founding member of a four-person analytics team built from the ground up

### Featured project: LogosTransformer
LogosTransformer is a decoder-only language model built from scratch in PyTorch, covering the full pipeline from tokenization through training and inference. Built to understand transformer architecture at the implementation level rather than just the API level.
[Link to GitHub repo]

### Links
- LinkedIn: [add URL]
- GitHub: [add URL]
- Résumé: Download PDF button — needs a general-purpose résumé, not the Anthropic-tailored version. Carlos: use a role-agnostic résumé for the public site.

## Future roadmap (not in current scope — for later reference)
Eventually Carlos may want to add an interactive demo of his LogosTransformer project to the site.

- Static hosting (GitHub Pages) cannot run live model inference, so this will need a separate service when the time comes.
- Preferred approach: Hugging Face Spaces (free CPU tier, built for hosting ML demos, typically via Gradio). The resulting demo can be embedded into this site via an iframe rather than hosted here directly.
- A Raspberry Pi 4 was considered as a self-hosted alternative. It's technically workable (would need Cloudflare Tunnel or similar to avoid exposing the home network and dealing with a dynamic IP), but reliability is tied to home power/internet, and the Pi's CPU-only ARM inference may be slow depending on the model's size. Better suited as a personal learning project than the primary hosting path for a public demo.
- Do not start on this until the static site is fully shipped and deployed.

## Status
- [ ] Scaffold HTML/CSS structure
- [ ] Drop in final copy (edit draft above)
- [ ] Add LogosTransformer GitHub link
- [ ] Add LinkedIn/GitHub links
- [ ] Add general-purpose résumé PDF to /assets and wire up download button
- [ ] Test responsive layout (mobile + desktop)
- [ ] Deploy to GitHub Pages
- [ ] Point carlossanta.com DNS at GitHub Pages
- [ ] Remove old LinkedIn redirect
