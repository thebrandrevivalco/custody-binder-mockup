# Custody Binder — 3D Mockup

A 3D render of the printed Co-Parenting Custody Tracker binder, made in Blender for the Etsy listing. Buyers print this product and put it in a real binder, so the listing needed a photo of exactly that — this is the next best thing to photographing my own copy every time.

## Files

- `custody-binder-mockup.blend` — the scene (binder, page block, pen, desk, lights, camera)
- `build_binder.py` — the script that builds the whole scene from scratch. Run it inside Blender (`blender -b --python build_binder.py`) and it saves the .blend and renders.
- `cover-texture.png` — the cover art, kept separate on purpose so I can swap the title/year without touching the scene
- `binder-mockup-render.png` — the current render (Cycles, 160 samples)

## Things I learned the hard way

- This Blender build has no OpenImageDenoiser, so denoising has to stay OFF or the render dies. 160 samples is the compromise.
- The binder looks thick because the real printed product IS thick (a year of logs). I thinned it once and it looked fake, so it stays.
- Cover text reads correctly from the listing camera angle. From the back angle it's upside down — only render from the saved camera.
