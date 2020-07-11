This repo contains a few tests for the validity of [CSS `@import`
rules](https://www.w3.org/TR/css-cascade-4/#at-import) in certain cases.

Some of these tests might give warnings or errors on validators. This is
intentional.

To run them, open `src/test.html` (for tests 1 to 9 and 11) and
`src/test10.html` on a browser.

From my few tests on various browsers, the results are consistent:

- Tests 1-4 and 10 ignore the `@charset` rules and treat the `@import` as valid.
- Tests 5 and 6 (the control tests) ignore the `@import` rule.
- Test 7 ignores the non-existent `@test` rule and so treats `@import` as valid.
- Test 8 ignores the `@charset` and `@test` rules, and so treats both `@import`s
  as valid.
- Test 9 doesn't ignore the `@page` rule, and so treats the first `@import` as
  valid but not the second.
- Test 11 ignores the `@page` rule because it has invalid syntax, and so treats
  `@import` as valid.

Please note that some of these tests depend on the bytes in the files staying as
is (in terms of character encodings and BOM's; newlines don't matter), so please
checkout the repo with `git` or download it as a zip file from Github, rather
than copying the contents into a text editor.

---

The contents of this repo are offered under the [CC0 Public Domain
Dedication](https://creativecommons.org/publicdomain/zero/1.0/).
