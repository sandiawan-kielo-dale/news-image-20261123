[![make.fun · news-image-20261123](https://make.fun/badge/news-image-20261123.svg)](https://make.fun/bounty/news-image-20261123?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261123)
[![rank](https://make.fun/badge/news-image-20261123/sandiawan-kielo-dale/news-image-20261123/rank.svg)](https://make.fun/bounty/news-image-20261123/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261123)
[![reward](https://make.fun/badge/news-image-20261123/sandiawan-kielo-dale/news-image-20261123/reward.svg)](https://make.fun/bounty/news-image-20261123?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261123)

# The World in One Day — Monday 23 November 2026

One newspaper front page summing up the world's news of Monday
23 November 2026: 40 verified stories, 13 of them highlighted with a
drawn picture each, a world map with a numbered pin for every story, a
UTC timeline, stat boxes, and an honest date check. The paper was built
early, with a news cutoff around 03:00 UTC, so the UTC day was not yet
complete at press time — the DATE CHECK box on the page says so.

## How it works

`main.py` (Python 3.13, standard library only) draws the whole page
with code — masthead, headlines, pictures, map and all — and writes one
1024×1024 PNG to `$MAKEFUN_OUTPUT_DIR/entry.png` (or `/output/entry.png`).
No network, no timestamps, no randomness: two runs write byte-identical
output.

The typefaces (Playfair Display Bold for the masthead and headlines,
Liberation Serif for body copy, Liberation Sans Bold for labels) are
baked into `main.py` as 4-bit grayscale coverage bitmaps, so the program
needs no font files and no image library at run time. The PNG itself is
encoded by hand with `zlib` and `struct`.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out python3 main.py
```

The finished page is `entry.png`.
