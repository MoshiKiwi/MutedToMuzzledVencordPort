# Generated sheets

All 63 non-default combinations the customizer (`../index.html`) can produce, pre-rendered as **standalone, self-contained stylesheets** — each file is the full `MutedToMuzzled.css` with the relevant rule blocks removed or their icon URLs swapped, not an `@import` plus overrides. That means pasting one of these into QuickCSS is always a single line:

```css
@import url("https://moshikiwi.github.io/MutedToMuzzledVencordPort/custom/css/MutedToMuzzled-<bits>.css");
```

The 64th combination — every bit at `0` — is just the existing `MutedToMuzzled.css` itself (nothing removed or swapped), so it isn't duplicated here; point at that file directly instead.

Filename: `MutedToMuzzled-<b1>-<b2>-<b3>-<b4>-<b5>-<b6>.css`

| bit | meaning                 | 0 (matches default) | 1 (overridden) |
|-----|-------------------------|----------------------|-----------------|
| b1  | mic icon swap           | on                   | off (block removed) |
| b2  | mic icon style          | new                  | old (URLs swapped)  |
| b3  | deafen icon swap        | on                   | off (blocks removed) |
| b4  | deafen icon style       | new                  | old (URLs swapped)  |
| b5  | custom tooltip text     | on                   | off (blocks removed) |
| b6  | typing indicator text   | on                   | off (block removed) |

`0` always means "same as the default `MutedToMuzzled.css`" for that axis, `1` means "overridden away from it." A style bit (b2/b4) only has an effect when its matching swap bit is `0` (feature on); if the swap bit is `1` (off), the whole rule block is gone and the style bit is moot — both values produce identical content.

- `MutedToMuzzled-0-0-0-0-0-0.css` would be the default file itself — omitted.
- `MutedToMuzzled-1-1-1-1-1-1.css` — everything off (plain, unmodified Discord; just the file header comment remains).
- `MutedToMuzzled-0-1-0-1-0-0.css` — everything on, using the old icon art style.

Regenerated from the real `MutedToMuzzled.css` by deleting the exact rule blocks for a disabled feature, or swapping the `raw.githubusercontent.com/zoez22/muzzlemute/...` icon URLs for the old-style ones — so each file is a faithful, complete drop-in replacement, not a patch.
