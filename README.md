# POCATALICO

A farming and story game set in Lanham, West Virginia, in the years when the
timber gave out and the coal came up the creek: 1899 to 1907. You are a Vale,
working the family farm through four chapters: the Timber Days, the Land Man,
Coal Town, and the Reckoning. Eighteen valley people, each with their own
temper, errands, likes, dislikes, and secrets. Four ways the story can end.

By Joshua A. Lanham.

## Play

The game is published with GitHub Pages from this repository. It plays in a
web browser on a computer or a phone. Nothing to download, nothing to install.

Move with the arrow keys or WASD. Talk and use things with E or Space. Open
the menu with Esc, your journal with J, and change seed with Q.

## How this repository works

The playable game is built automatically by GitHub. The game's source
travels as `pocatalico-src.zip` (stored here in numbered parts): the Godot
4.3 project (scripts, scenes, and data as text) plus the two Python scripts
that draw every piece of pixel art from one palette, in the simple 16-bit
style of the SNES Final Fantasy II family. On every change, the workflow in
`.github/workflows/pocatalico.yml` unpacks the source, regenerates the art,
downloads Godot, runs the game's own test suites (88 checks, including a
start-of-game test that plays the real first minute), exports the web
version, and publishes it here. If any check fails, nothing is published
and the failure log is saved to `ci-log.txt`.

The valley people in play are composites, invented for the story. The real
names and records live only in the in-game Valley Museum, each with its
source.
