# POCATALICO source

Text-only source for the POCATALICO web build.

- `godot/` - the Godot 4.3 project with every picture removed. All pixel art
  is generated, never stored: `tools/make_pixel_assets.py` draws the tile
  atlas and `tools/make_sprites.py` draws the character sheets, props, crop
  stages, and item icons, both from the one palette in
  `godot/assets/palette.json`.
- `tools/` - those two generator scripts (Python 3, needs Pillow).

Build recipe (what the GitHub workflow runs, in order):

1. `python3 tools/make_pixel_assets.py` and `python3 tools/make_sprites.py`
2. Godot 4.3 headless: `--import`, then the three test scenes in
   `godot/tests/` (start_test, smoke_test, play_test)
3. `--export-release "Web"` to the published page

Style law for all art: simple 16-bit pixel art in the SNES Final Fantasy II
family, top-down tiles and small sprites, one bright limited palette.
