# Kinema

App-specific language for Kinema (kinema.codesavory.dev), the first product from the Lasya studio: a browser tool for physically real motion design. It sits on top of the universal Codesavory language in `../../DESIGN.md`. Read that first. Kinema adds tokens and overrides none.

## What the product is

A spectral path tracer and directable physics in a browser tab. People drop in a logo, pick glass or chrome, drag a light by hand and render a short film. The landing page works like a product page (one line, one live demo, one call to action), not like the Lasya studio site.

## Direction

- **The live render is the hero.** A WebGPU canvas on `canvas-ground` renders as soon as the page opens. Where WebGPU is missing, a prerendered video takes its place and one line says which browsers work.
- **Rendered colour is content, not UI.** Spectral rainbows inside the canvas are the product's output. They never leak into buttons, text or surfaces.
- **The accent is spent once:** on the one serif flourish in the headline (`serif`, `accent-text`), like Lasya. Buttons are `brand`. Nothing else on the landing page is ember.
- **The render is a tool, not a video.** A deck of instrument controls sits under the canvas (angle, beam, dispersion, exposure, reset): mono uppercase labels, a hairline top, range inputs in `ink`, readouts in `ink-subtle`. Dragging the render aims the beam. Nothing in the deck is ember. (Owner, 22 Oct 2026: it should look like an actual tool and a web renderer running, not a static image or video.)
- **The icon is the prism:** a white triangle on `canvas-ground`, the beam entering, the ember seed where the spectrum leaves. Products keep the seed and change what it marks.
- **Instrument details from its own world:** the sample counter (spp) and frame number in Geist Mono or Doto on the canvas ground, small, never decorative.
- **Few words.** A wordmark, one headline, one line, one button. "Coming soon" is allowed only with one next step (rule 32).

## Theme

Follows the system (rule 2), with both themes designed. The canvas ground stays dark in both.

## Do not

- Do not copy the Lasya studio layout or the Kickoff app page (rule 36). Kinema is a tool page.
- Do not put text over the live render.
- Do not use spectral gradients on surfaces, buttons or text.
- Do not ship placeholder features, fake galleries or invented numbers.
