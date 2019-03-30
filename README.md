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

## Custom Callouts

5 custom callout styles (inspired by [BookStack callouts][bookstack-callouts]).

- Generic (white)
- Info (🛈 blue)
- Success (✓ green)
- Warning (⚠ orange)
- Danger (⯃ red)

### Usage

Wrap the text in a `<p>` tag, specifying the style; e.g. `<p class="callout info"></p>`

```html
<p class="callout">This is a plain callout.</p>

<p class="callout info">This is an informational callout.</p>

<p class="callout success">This is a success callout</p>

<p class="callout warning">This is a warning callout</p>

<p class="callout danger">This is a danger callout</p>

<p class="callout info whitespace">Add "whitespace" to the class to honor
New Lines without <br>. Blank lines will break <p>, use &nbsp;
&nbsp;
Note: Does not play well with markdown.</p>

<div class="callout">This is a plain callout wrapped in <div> to support Markdown; there must be a blank line before any markdown.

> Blockquote *within* a callout?!

Markdown formatted list;
- Item 1
- Item 2 has `inline code`

| Markdown | Table |
| :-:      | :-    |
| Center   | Left  |
</div>
```

### Result

![callout-styles][ss-callout-styles]

## Steps Tables

Custom format for tables outlining process steps; [example][steps-table-eg].

- `table thead` is collapsed.
- `table tbody tr:nth-child` color change; i.e. alternating colors; e.g.

### Usage

Wrap the table in a `<div>` tag, include `markdown=1` if the table is MD formatted; e.g. `<div class="steps-table" markdown="1"></div>`

```html
<div class="steps-table" markdown="1">

|   #   |       Steps        |
| :---: | :----------------: |
|   1   |   Do something.    |
|       |   ![image-1][1]    |
|   2   | Do something else. |
|       |   ![image-2][2]    |
|   3   | Do something else  |
|       |   ![image-3][3]    |
|   4   | Do something else  |
|       |   ![image-4][4]    |
|   5   | Do something else  |
|       |   ![image-5][5]    |


[1]: https://imgur.com/aaaaa
[2]: https://imgur.com/bbbbb
[3]: https://imgur.com/ccccc
[4]: https://imgur.com/ddddd
[5]: https://imgur.com/eeeee
    
</div>
```

### Result

![steps-table][ss-steps-table]

# Screenshots

## Home

![screenshot-desktop-home][ss-d-home]

## Post (Top)

![screenshot-desktop-post-2-top][ss-d-p2-top]

## Post (Bottom)

![screenshot-desktop-post-2-bottom][ss-d-p2-btm]

## Post Code

![screenshot-desktop-post-1-code][ss-d-p1-code]




[ghost]: http://github.com/tryghost/ghost/
[casper]: https://github.com/TryGhost/Casper
[ss-d-home]: assets/screenshot-desktop-home.png
[ss-d-p2-top]: assets/screenshot-desktop-post-2-top.png
[ss-d-p2-btm]: assets/screenshot-desktop-post-2-btm.png
[ss-d-p1-code]: assets/screenshot-desktop-post-1-code.png
[zip-dl]: https://github.com/derek-shnosh/casper-dark-ds/archive/master.zip
[prismjs-onedark]: https://github.com/derek-shnosh/prism-theme-one-dark-ds
[clipboardjs]: https://github.com/zenorocha/clipboard.js/
[prismjs]: https://github.com/PrismJS/prism
[bookstack-callouts]: https://www.bookstackapp.com/blog/beta-release-v0-11-0/
[steps-table-eg]: https://shnosh.io/securecrt-echo-paste/#securecrtconfiguration
[ss-steps-table]: assets/screenshot-steps-table.png
[ss-callout-styles]: assets/screenshot-callout-styles.png