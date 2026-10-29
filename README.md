# Mohamed Ayad — Portfolio

Personal portfolio site. A single self-contained `index.html`: no build step, no framework.

**Live:** https://memo410.github.io

## Stack

Plain HTML, CSS and JavaScript (ES modules). [three.js](https://threejs.org) r0.143 and
[Lenis](https://lenis.darkroom.engineering) load from the unpkg CDN through an import map, and
Inter comes from Google Fonts.

## Features

- A fixed, full-viewport WebGL Earth behind the whole page. It has day/night shading with city
  lights, ocean glint and flow, a rim light, three drifting cloud shells, a blue atmosphere halo,
  a twinkling starfield, ambient motes and gold radar-ping markers on land, all composited through
  bloom and a corner-flame pass.
- Scroll choreography: the planet rises behind the hero, zooms out and swings left, then right,
  and settles behind the contact section, turning as you scroll.
- Glass sections over a deep-space palette with a mint accent, staggered fade-up reveals, and
  Lenis smooth scrolling.
- Live signals in the hero: an "open to work" status and the current time in Cairo (shown only
  if the browser's `Intl` resolves `Africa/Cairo`).
- Copy-to-clipboard on the email address, with a polite screen-reader announcement.
- Fixed navigation that turns to glass once you scroll and highlights the section on screen.
- Responsive from phone to desktop.
- Respects `prefers-reduced-motion`: reveals show immediately, and Lenis, the planet's entrance
  and the status pulse are switched off.
- The content never depends on the 3D scene. If WebGL, the CDN or the planet assets fail, the
  page still reads on a plain dark background.

## Project links

Client applications are covered by non-disclosure agreements, so their source and builds
stay private. [Nada City](https://play.google.com/store/apps/details?id=com.nada.city) is
publicly listed on Google Play.

## Local preview

Open `index.html` in a browser. It needs a network connection for the CDN scripts, the fonts and
the planet assets.

## Credits

The planet scene is ported from the "Ascend" WebGL template. Its planet, night-lights and cloud
assets load from the template's public asset bucket at `api.getlayers.ai`.

## Contact

- Email — mohamedezatayad2005@gmail.com
- LinkedIn — https://www.linkedin.com/in/mohamedayad14
- GitHub — https://github.com/memo410
