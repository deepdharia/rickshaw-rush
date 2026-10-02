# 🛺 Rickshaw Rush — Grand Opening Edition

An endless arcade driver starring an auto rickshaw. Dodge traffic, grab coins,
pick up passengers for fares, and honk slower vehicles out of your way —
through a living Indian city that cycles from day to sunset to neon night.

Single HTML file (~71KB). Zero dependencies. Fully offline.

**Graphics (v2 redefined):** hand-detailed hero rickshaw (marigold garland,
driver silhouette, chrome bumper, spoked wheels that spin, glowing tail lamps),
desi trucks with peacock art, buses with route boards + passengers, neon shop
signboards, festive pennant banners, string lights, drifting clouds, birds,
receding trees, asphalt texture, and warm light-pools under vehicles at night.

## How to play

- **Steer:** drag left/right, or ← → / A D keys
- **Honk (📯):** shoos the vehicle ahead of you into another lane
- **Coins (₹):** +10 score each
- **Passengers 🧍:** drive close to the road edge to pick them up for a fare (+₹20–50)
- **Near miss:** threading past traffic earns +15 "CLOSE!"
- Crash and it's over — unless you revive and keep going.

## Features

- 🎉 **Grand opening on launch:** fireworks, confetti, ribbon banner, and the
  rickshaw drives in before "TAP TO START"
- 🎨 Hand-drawn canvas art: detailed rear-view rickshaw ("HORN OK PLEASE",
  license plate, mudguards, mirrors), cars, buses, trucks with desi truck art
  ("USE DIPPER AT NIGHT"), bikes with riders
- 🌆 Parallax city: skyline, lit windows, shop signboards (CHAI, MITHAI, SAREE…),
  streetlights, day→sunset→night cycle with stars, sun/moon, headlight glow
- 🔊 Synthesized WebAudio: engine hum pitched to speed, two-tone honk, coin
  dings, fare arpeggio, crash thud, firework pops — no audio files
- 📳 Screen shake, dust, exhaust smoke, speed lines, floating score popups
- 🏆 Best score in localStorage; pause; mute; one rewarded revive per run (ad hook)
- 📱 Mobile-first portrait, touch + keyboard, safe-area aware

## Monetization hooks (web = no-ops; wire in native wrapper)

```js
window.RR_ADS = {
  showRewarded: function(cb){ cb(true); },  // rewarded video → cb(true) if watched
  removeAdsOwned: function(){ return false; }
};
```

## Publish path (same as 123)

1. Create public repo `rickshaw-rush` on github.com
2. Push `index.html` (+ this README)
3. Import into Vercel → permanent link
4. Capacitor wrapper → Play Store ($25) + AdMob

## Tests

Logic suite (`node` + stubbed canvas/DOM): opening → countdown → play,
steering, spawns, coin/fare pickup, honk-shoo, crash → game over →
revive → retry. All passing.
