# Mohamed Ayad — Portfolio

Personal portfolio site: a single `index.html` with its CSS and JavaScript inline.

**Live:** https://memo410.github.io/protofolio/

## Stack

Plain HTML, CSS and JavaScript (ES modules). [three.js](https://threejs.org) r0.143 loads from
the unpkg CDN through an import map, and Inter comes from Google Fonts.

## Features

- A fixed, full-viewport WebGL Earth behind the whole page. It has day/night shading with city
  lights, ocean glint and flow, a rim light, three drifting cloud shells, a blue atmosphere halo,
  a twinkling starfield, ambient motes and gold radar-ping markers on land, all composited through
  bloom and a corner-flame pass.
- Scroll choreography: the planet rises behind the hero, zooms out and swings left, then right,
  and settles behind the contact section, turning as you scroll.
- Glass sections over a deep-space palette with a mint accent, and staggered fade-up reveals.
- Live signals in the hero: an "open to work" status and the current time in Cairo (shown only
  if the browser's `Intl` resolves `Africa/Cairo`).
- Copy-to-clipboard on the email address, with a polite screen-reader announcement.
- Fixed navigation that turns to glass once you scroll and highlights the section on screen.
- Responsive from phone to desktop.
- Respects `prefers-reduced-motion`: reveals show immediately, the planet holds still in its
  opening pose (no entrance, spin or scroll-driven swing), and the status pulse is switched off.
- The content never depends on the 3D scene. If WebGL, the CDN or the planet assets fail, the
  page still reads on a plain dark background.

## Performance

The planet is drawn on every frame, so the page is tuned to keep scrolling smooth on phones and
on laptops running the browser on integrated graphics:

- Scrolling is native, on the browser's compositor thread.
- Touch devices get a lite mode: solid glass panels instead of live background blur, the scene at
  1× pixel ratio, and a single render pass.
- On any device, a frame-time governor switches to lite mode, and then lowers the resolution, if
  the planet keeps missing about 40 fps.
- Rendering is capped near 60 fps on high-refresh screens.
- The planet's large textures are downscaled off the main thread and uploaded one per frame, and
  the shaders compile before the planet appears.

On laptops with two GPUs, the browser may run on the integrated one. Setting it to "High
performance" in Windows Settings → System → Display → Graphics makes the planet much smoother.

## Project links

Client applications are covered by non-disclosure agreements, so their source and builds
stay private. Nada City is publicly listed on
[Google Play](https://play.google.com/store/apps/details?id=com.nada.city) and the
[App Store](https://apps.apple.com/us/app/nada-city/id6785543617).

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
