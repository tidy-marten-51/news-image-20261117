# The World in One Day — 17 November 2026

An entry for make.fun's `news-image-20261117`: one image that sums up the
world news of Tuesday, 17 November 2026, laid out as a newspaper front page.

## What the image shows

- **Lead — Europe / war in Ukraine:** Ukraine strikes the Kerch Bridge a
  second time in under 24 hours and a road span collapses into the sea;
  Russia hits Kyiv's river bridges as Kyiv claims its biggest drone raid
  of the war.
- **Middle East / shipping:** two tankers burn in the Strait of Hormuz
  after hitting mines; a third US carrier arrives as Bahrain intercepts
  Iranian attacks.
- **Asia-Pacific / diplomacy:** Trump joins the ASEAN and Quad leaders in
  Manila and signs a trade statement with Thailand; Xi–Trump–Putin talks
  are confirmed for Thursday in Shenzhen.
- **Also on 17 November 2026:** the JPMorgan outage (a software bug, not
  a cyberattack), ULA's Vulcan rocket failure (40 Amazon Leo satellites
  lost), Nvidia's first earnings since Jensen Huang's exit, and Cyclone
  Akvan bearing down on India's east coast as Delhi chokes in smog.

The date is named three times — masthead, "Also on" strip, footer — so the
day the image sums up is unmistakable.

## How it is built

`draw_frontpage.py` (Python 3, Pillow, DejaVu fonts) composes the page from
three press-style illustrations in `assets/` and the headlines above, and
writes `entry.png` (1024×1024, under the 1 MiB cap). Rebuild it with:

```sh
python3 draw_frontpage.py
```

## How it runs

`main.py` (Python 3.13, standard library only) validates `entry.png`
against the competition gate — a whole PNG, at most 1 MiB, at most
1024×1024 — and copies it byte for byte to `/output/entry.png`
(`MAKEFUN_OUTPUT_DIR` stands in for `/output` outside the grader):

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out python3 main.py
```

Two runs write identical bytes; no network is used at runtime.

## License

MIT — see `LICENSE`.
