# Berlin photographs

`berlin-01.jpg` … `berlin-23.jpg` are the photographs `kaweinberlin-1` … `kaweinberlin-23`, in the same order.
Each is resized to at most 1600px on its long side, JPEG quality 82.

They appear on two slides, between the timeline and "In Berlin, two bronzes.":

1. **Then, Berlin.** All 23, whole and uncropped, in four justified rows. The slide opens out of the white
   Berlin bar on the timeline. On screen, a photograph grows when the pointer rests on it; in print the
   mosaic stays as it is and every photograph is legible. On a phone the mosaic becomes two columns.
   Row order: 06 01 08 05 16 · 13 20 12 03 17 14 · 10 22 04 19 02 11 · 07 21 15 23 18 09.
2. **Latent space.** Every Berlin picture in the deck sits at the tip of a vector among 170 grey ones:
   the 23 (they fly in from the mosaic), the two bronzes, the first page of *Kāveh*, and the 63 in `more/`,
   which appear only here. They form seven clusters, each with a faint outline and a name. Hovering a picture
   turns its cluster's vectors red. Otherwise only the bronzes' vectors are red; moving on, the view closes
   in on them and sets them down where the next slide holds them.
   Clusters: skies · night and light · monuments and bronze · buildings and glass · people · words and print ·
   art and walls.
   The mosaic photographs' clusters are in `groupOf`; the others are in the `MORE` list, both in the
   latent-space script in `index.html`.

To add photographs to the latent space only, resize them to at most 800px on the long side, save them in
`more/` as the next `more-NN.jpg`, and add a line to `MORE` with its cluster (`sky`, `night`, `stone`,
`arch`, `life`, `print` or `art`). The full-size originals are kept locally in `_originals/` under the same numbers (`more-NN.png`),
which is not published.

To swap a photograph, replace the file and keep its name. The row layout and each photo's zoom origin are
written into `index.html` for the current aspect ratios, so a replacement with a different shape needs the
rows recomputed. The clusters are set in the `groupOf` map in the latent-space script.

`berlin-23.jpg` exists only at 282×612, so it is soft when enlarged.
