# Starship Drift

**Play it:** https://joranbeasley.github.io/starship-mobile/ (open on your phone)

A spaceship flying game for phones, steered by tilting the device. It is a single `index.html` with no build step or dependencies.

## How to play

Pick one of three modes on the title screen. Each mode keeps its own best score.

- **Tunnel run:** fly down an asteroid tunnel. Tilt sets where the ship sits inside it: tilt left and right to slide sideways, tip the top edge away from you to rise and back toward you to drop. Rings come straight at you.
- **Open space:** no walls, and you can turn all the way around. Tilt left and right to turn, tip the top edge away to climb and back to dive. Hold a tilt to keep turning and return to neutral to fly straight; the nose eases back to level on its own. One ring at a time appears ahead, and an arrow at the screen edge points to it with the distance when it is off screen.

- **Paper plane:** glide through an endless city at dusk. There is no engine: diving builds speed, pulling up (tip the top edge away) trades that speed for height, and if you get too slow the plane stalls and drops its nose. Tilt left and right to bank and turn; tight turns sink unless you pull up as well. Warm air rises from rooftop vents (the shimmering columns), so fly through one to gain height, and each hoop you thread gives a gust of speed. Hitting a building or the street crumples the plane; after three crumples the run ends. The HUD shows altitude, airspeed, and warns you when you stall or ride an updraft.

In all modes (firing is only in the space modes):

- When you press Launch, the way you are holding the phone becomes "neutral". The ⊕ button resets neutral to your current grip, and rotating the screen resets it too.
- **Hold a finger on the screen to fire** twin lasers. Large asteroids take two hits.
- Each ring threaded in a row raises your score multiplier, up to ×6. Missing a ring or taking a hit resets it.
- Collect amber crystals for points and green repair kits to restore hull.
- Red brackets mark asteroids that are on a collision course with you.
- Turn on *Reverse up/down* or *Reverse left/right* in settings if you prefer it the other way. If steering feels twitchy, try *Low* sensitivity. While flying, the dot in the bottom-left corner shows what the game reads from your tilt.

Without a tilt sensor, drag a finger to steer (in open space, let go to fly straight). On a computer, steer with the mouse or arrow keys/WASD, fire with click or Space, pause with P or Esc, and press C to recentre.

## Running it on a phone

Browsers only provide motion sensor data to pages served over **HTTPS**, so opening the file directly or from a plain-HTTP LAN address will not give you tilt controls. Some options:

- **GitHub Pages:** in the repository settings, go to Pages, choose "Deploy from a branch", and pick the branch and `/ (root)`. Open the resulting `https://…github.io/starship-mobile/` URL on your phone.
- **Local testing:** run `npx serve .` (or `python3 -m http.server`) and expose it over HTTPS with a tunnel such as `cloudflared tunnel --url http://localhost:3000`.

On iOS, Safari asks for motion access when you tap Launch. If you decline, the game falls back to drag steering. To get the prompt again, close the tab and reopen the page.

Tip: on iOS use *Share → Add to Home Screen*, and on Android use the browser's *Install app* option, to play full-screen.
