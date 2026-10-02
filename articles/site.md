# Map gallery

Once you have exported a bunch of interactive map HTML files with
`map(ctdf) |> save_map(path = ...)`, you can call
[`site()`](https://xarvian.github.io/clusterTrack.Vis/reference/site.md)
to create a simple browsable index for that folder.

[`site()`](https://xarvian.github.io/clusterTrack.Vis/reference/site.md)
copies a Quarto `index.qmd` template into the same directory as your
saved map `.html` files. Render that `index.qmd` to produce an
`index.html` that links to the maps.

### Use site()

[`require`](https://rdrr.io/r/base/library.html)`(`[`clusterTrack`](https://xarvian.github.io/clusterTrack/)` ``)`` `[`require`](https://rdrr.io/r/base/library.html)`(`[`clusterTrack.Vis`](https://xarvian.github.io/clusterTrack.Vis/)`)`` `` ``out_path`` ``=`` ``"path/to/your/future_dir"`

Export many maps (use whatever loop/apply/parallel approach you prefer)

[`map`](https://xarvian.github.io/clusterTrack.Vis/reference/map.md)`(``x1``)`` ``|>`` `[`save_map`](https://xarvian.github.io/clusterTrack.Vis/reference/map.md)`(``path``=``out_path``)`` `[`map`](https://xarvian.github.io/clusterTrack.Vis/reference/map.md)`(``x2``)`` ``|>`` `[`save_map`](https://xarvian.github.io/clusterTrack.Vis/reference/map.md)`(``path``=``out_path``)`` ``...`` `[`map`](https://xarvian.github.io/clusterTrack.Vis/reference/map.md)`(``xn``)`` ``|>`` `[`save_map`](https://xarvian.github.io/clusterTrack.Vis/reference/map.md)`(``path``=``out_path``)`

Copy the Quarto index template into `out_path`

[`site`](https://xarvian.github.io/clusterTrack.Vis/reference/site.md)`(``out_path``)`

Then render `out_path/index.qmd` to get `out_path/index.html`
