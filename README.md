This repo contains a few tests for the validity of [CSS `@import`
rules](https://www.w3.org/TR/css-cascade-4/#at-import) in certain cases.

Some of these tests might give warnings or errors on validators. This is
intentional.

To run them, open `src/test.html` (for tests 1 to 9 and 11) and
`src/test10.html` on a browser.

From my few tests on Firefox, Chrome and [Epiphany / GNOME
Web](https://wiki.gnome.org/Apps/Web/) (a [Webkit](https://webkit.org/)
representative, since I don't have access to Mac or iOS machines), the results
are consistent:

| Test | First `@import` rule is valid | Second `@import` rule is valid |
| ---- | ----------------------------- | ------------------------------ |
| 1    | ✔                             | N/A                            |
| 2    | ✔                             | N/A                            |
| 3    | ✔                             | N/A                            |
| 4    | ✔                             | N/A                            |
| 5    | ✘                             | N/A                            |
| 6    | ✘                             | N/A                            |
| 7    | ✔                             | N/A                            |
| 8    | ✔                             | ✔                              |
| 9    | ✔                             | ✘                              |
| 10   | ✔                             | N/A                            |
| 11   | ✔                             | N/A                            |
| 12   | ✔                             | N/A                            |
| 13   | ✘                             | N/A                            |
| 14   | ✘                             | N/A                            |

Please note that some of these tests depend on the bytes in the files staying as
is (in terms of character encodings and BOM's; newlines don't matter), so please
checkout the repo with `git` or download it as a zip file from Github, rather
than copying the contents into a text editor.

---

The contents of this repo are offered under the [CC0 Public Domain
Dedication](https://creativecommons.org/publicdomain/zero/1.0/).
