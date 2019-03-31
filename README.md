# Casper Dark (DS)

Based on the default theme ([Casper][casper]) for [Ghost][ghost].

> Forked from Casper v2.9.6 on 2019/03/19
> 
> [Changelog](changelog-ds.md)

# Installation

1. Download the files using the [GitHub .zip download][zip-dl] option.
2. Navigate to **Settings > Design** on your Ghost admin interface.
3. Click **Upload a theme** (near bottom).
4. Either drag the .zip file onto the dialogue, or click the center to browse to the .zip.
5. Click **Activate Now**.

# Features

## Styled `<details>` (Accordions)

Styling for HTML5 `<details>` elements, used as accordions.

### Usage

```html
<details><summary>Expand for <desc>Dynamic Variable Example</desc></summary>
 
`gi_ints` is a list of GigabitEthernet interfaces, which scales with the number of switches in the stack.

| Switch Count | `gi_ints` |
| :-: | :- |
|  1  | `gi1/0/1-36` |
|  2  | `gi1/0/1-36,gi2/0/1-36` |
|  3  | `gi1/0/1-36,gi2/0/1-36,gi3/0/1-36` |
|  4  | `gi1/0/1-36,gi2/0/1-36,gi3/0/1-36,gi4/0/1-36` |

</details>
```

### Result

**Closed (default)**

![screenshot-details-closed][ss-details-closed]

**Open**

![screenshot-details-open][ss-details-open]

## Custom Callouts

5 custom callout styles (inspired by [BookStack callouts][bookstack-callouts]).

- Generic (white)
- Info (🛈 blue)
- Success (✓ green)
- Warning (⚠ orange)
- Danger (⯃ red)

### Callouts with `<p>`

```html
<p class="callout">This is a plain callout.</p>

<p class="callout info">This is an informational callout.</p>

<p class="callout success">This is a success callout</p>

<p class="callout warning">This is a warning callout</p>

<p class="callout danger">This is a danger callout</p>
```

### Callout with `<div>`

*Can be used to include line-breaks and markdown in the callout; markdown requires a blank space after the `<div>` (ignore `\` in the code block).*

```html
<div class="callout info">

This is an informational callout with some `inline-code`

> Blockquote *within* a callout?!

\```bash
# And a code block.
sudo nanon /etc/hostname
\```

And a list
- Item 1
- Item 2
  - Sub-item
</div>
```

### Results

![screenshot-callouts][ss-callouts]

## Steps Tables

Custom format for tables outlining process steps; [example][steps-table-eg].

- `table thead` is collapsed.
- `table tbody tr:nth-child` color change; i.e. alternating colors; e.g.

### Usage

*Wrap the table in a `<div>` tag; markdown requires a blank space after the `<div>`.*

```html
<div class="steps-table">

| # | Count to three on your fingers...
|:-:| :-:
| 1 | Hold up **one** finger.
|   | ![1-finger][1]
| 2 | Hold up **two** fingers.
|   | ![2-fingers][2]
| 3 | Hold up **three** fingers.
|   | ![3-fingers][3]


[1]: /content/images/2019/03/step1.png
[2]: /content/images/2019/03/step2.png
[3]: /content/images/2019/03/step3.png
</div>
```

### Result

![steps-table][ss-steps-table]

# Screenshots

## Home

![screenshot-desktop-home][ss-d-home]

## Post

![screenshot-desktop-post-2-top][ss-d-post]



[ghost]: http://github.com/tryghost/ghost/
[casper]: https://github.com/TryGhost/Casper
[zip-dl]: https://github.com/derek-shnosh/casper-dark-ds/archive/master.zip
[prismjs-onedark]: https://github.com/derek-shnosh/prism-theme-one-dark-ds
[clipboardjs]: https://github.com/zenorocha/clipboard.js/
[prismjs]: https://github.com/PrismJS/prism
[bookstack-callouts]: https://www.bookstackapp.com/blog/beta-release-v0-11-0/
[steps-table-eg]: https://shnosh.io/securecrt-echo-paste/#securecrtconfiguration
[ss-steps-table]: assets/images/screenshot-steps-table.png
[ss-callouts]: assets/images/screenshot-callouts.png
[ss-details-closed]: assets/images/screenshot-details-closed.png
[ss-details-open]: assets/images/screenshot-details-open.png
[ss-d-home]: assets/images/screenshot-desktop-home.png
[ss-d-post]: assets/images/screenshot-desktop-post.png