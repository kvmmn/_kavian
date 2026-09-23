# Berlin photographs

`berlin-01.jpg` … `berlin-23.jpg` are the photographs `kaweinberlin-1` … `kaweinberlin-23`, in the same order.
Each is resized to at most 1600px on its long side, JPEG quality 82.

They appear on two slides, between the timeline and "In Berlin, two bronzes.":

1. **Then, Berlin.** All 23, whole and uncropped, in four justified rows. The slide opens out of the white
   Berlin bar on the timeline. On screen, a photograph grows when the pointer rests on it; in print the
   mosaic stays as it is and every photograph is legible. On a phone the mosaic becomes two columns.
   Row order: 06 01 08 05 16 · 13 20 12 03 17 14 · 10 22 04 19 02 11 · 07 21 15 23 18 09.
2. **Latent space.** Every Berlin picture in the deck sits at the tip of a vector among 170 grey ones:
   the 23 (they fly in from the mosaic), the two bronzes, and the first page of *Kāveh*. They form five
   clusters, each with a faint outline and a name. Hovering a picture turns its cluster's vectors red.
   Otherwise only the bronzes' vectors are red; moving on, the view closes in on them and sets them down
   where the next slide holds them.
   - skies: 01, 03, 07, 10, 18, 19, 20
   - night and light: 02, 04, 06, 08, 12
   - bronze and stone: 05, 11, 13, 14, 21, and the two bronzes
   - people: 09, 15, 16, 17, 22, 23
   - print and archive: *Kāveh*, 1916

To add photographs to the latent space only, put them in `assets/berlin/more/` (any names) and list each
one in the `MORE` array at the top of the latent-space script in `index.html`, with its cluster:
`{ src: 'assets/berlin/more/name.jpg', group: 'life' }`. The groups are `sky`, `night`, `stone`, `life`
and `print`. Resize them to at most 1600px on the long side first.

To swap a photograph, replace the file and keep its name. The row layout and each photo's zoom origin are
written into `index.html` for the current aspect ratios, so a replacement with a different shape needs the
rows recomputed. The clusters are set in the `groupOf` map in the latent-space script.

`berlin-23.jpg` exists only at 282×612, so it is soft when enlarged.
