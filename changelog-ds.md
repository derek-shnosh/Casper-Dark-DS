## v2.9.6-002

- Margin and alignment formatting.
  - `.post-full-content p` margin.
  - `.post-full-content blockquote (p|ul):last-child` margin.
  - `.post-full-content p:only-child` bottom margin.
  - `.post-full-content h2` top margin.
  - `.post-full-content table (th|td)` middle aligned.
  - `summary` background lightens when opened
  - `summary` animation changed.
  - `#ToTop` button `background` declaration changed.
- Added Style: `steps-table`
  - Custom format for tables outlining process steps; [example][steps-table-eg].
    - `table thead` is collapsed.
    - `table tbody tr:nth-child` color change; i.e. alternating colors; e.g.
    - Usage;
      ```html
      <div class="steps-table" markdown="1">

          ```markdown
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
          ```
          
      </div>
      ```

[steps-table-eg]: https://shnosh.io/securecrt-echo-paste/#securecrtconfiguration

## v.2.9.6-001

- Dark theme.
- Bundled scripts: [clipboard.js][clipboardjs], [PrismJS][prismjs]
  - Custom (modified) PrismJS theme: [prism-theme-one-dark-ds][prismjs-onedark]
- Scroll-to-top button on post pages (`post.hbs`).
- Preferential style changes.