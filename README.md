# Mohamed Ayad — Portfolio

Personal portfolio site. Single self-contained `index.html` — no build step, no dependencies.

**Live:** https://memo410.github.io

## Stack

Plain HTML, CSS and vanilla JavaScript. IBM Plex Sans / Mono via Google Fonts, with a system fallback.

## Features

- Light and dark themes, following the system preference and remembering the choice.
  Toggling uses the View Transitions API for a circular wipe from the button, and a
  blocking head script resolves the stored theme before first paint so dark-mode
  visitors never see a light flash.
- Cover with a staggered entrance: mono labels wipe, headings mask-reveal, prose rises.
  The whole sequence settles in under a second.
- Live signals — an "open to work" status dot and a ticking Cairo clock (shown only if
  `Intl` actually resolves `Africa/Cairo`).
- Ambient background: a slow-drifting aurora wash over a technical hairline grid, with
  damped pointer parallax on fine pointers only.
- Scroll-driven reveals with per-container stagger, a reading-progress rule down the
  rail, and section rules that draw themselves in.
- Animated stat count-up with hairline meters, and a per-row cascade of the skill tags.
- Pointer-tracked spotlight on the card surfaces, and a sliding scroll-spy indicator
  that animates between nav items.
- Copy-to-clipboard on the email address, with a polite screen-reader announcement.
- Responsive from mobile through desktop.
- Respects `prefers-reduced-motion` throughout: every animation is neutralised, every
  rAF loop and listener is torn down, and each element's resting state is its natural
  one — so the page is correct, never blank, if the motion never runs.
- Degrades cleanly with JavaScript disabled or an early script error: nothing is hidden
  behind an animation that has to complete.

## Project links

Client applications are covered by non-disclosure agreements, so their source and builds
stay private. [Nada City](https://play.google.com/store/apps/details?id=com.nada.city) is
publicly listed on Google Play.

## Local preview

Open `index.html` in a browser. That's it.

## Contact

- Email — mohamedezatayad2005@gmail.com
- LinkedIn — https://www.linkedin.com/in/mohamedayad14
- GitHub — https://github.com/memo410
