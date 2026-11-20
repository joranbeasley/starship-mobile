# Starship Drift

A spaceship flying game for phones, steered by tilting the device. It is a single `index.html` with no build step or dependencies.

## How to play

- **Tilt to steer.** When you press Launch, the way you are holding the phone becomes "neutral". Tilt left and right to bank, and tip the top edge away from you or toward you to climb or dive. Turn on *Flight-stick pitch* in settings to reverse the up/down direction.
- **Hold a finger on the screen to fire** twin lasers. Large asteroids take two hits.
- **Fly through the cyan rings.** Each ring in a row raises your score multiplier, up to ×6. Missing a ring or taking a hit resets it.
- Collect amber crystals for points and green repair kits to restore hull.
- Red brackets mark asteroids that are on a collision course with you.
- The ⊕ button resets neutral tilt to your current grip. Rotating the screen resets it too.

Without a tilt sensor, drag a finger to steer. On a computer, steer with the mouse or arrow keys/WASD, fire with click or Space, pause with P or Esc, and press C to recentre.

## Running it on a phone

Browsers only provide motion sensor data to pages served over **HTTPS**, so opening the file directly or from a plain-HTTP LAN address will not give you tilt controls. Some options:

- **GitHub Pages:** in the repository settings, go to Pages, choose "Deploy from a branch", and pick the branch and `/ (root)`. Open the resulting `https://…github.io/starship-mobile/` URL on your phone.
- **Local testing:** run `npx serve .` (or `python3 -m http.server`) and expose it over HTTPS with a tunnel such as `cloudflared tunnel --url http://localhost:3000`.

On iOS, Safari asks for motion access when you tap Launch. If you decline, the game falls back to drag steering. To get the prompt again, close the tab and reopen the page.

Tip: on iOS use *Share → Add to Home Screen*, and on Android use the browser's *Install app* option, to play full-screen.
