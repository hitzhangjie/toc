# toc

Program `toc` scans your markdown directory and automatically
generates `SUMMARY.md`, you can use it in this way:

```
toc [-d <dir>] > SUMMARY.md
```
It is useful when you organize markdowns in different folders,
similar cases are gitbook, hugo, etc. By `toc` we don't need
to manually write SUMMARY.md now.

`toc` will rewrite SUMMARY.md according to your filesystem
hierarchy, and liquid tag `weight` in same folder.

For example, if we have following files:

```bash
.
|-1
  - 1.1
  - 1.2
|-2
  - 2.1
  - 2.2

```

then `toc > SUMMARY.md` will generate following content:

file: SUMMARY.md

```markdown
# Summary
---
headless: true
bookhidden: true
---

* [1](1)
  * [1.1](1.1)
  * [1.2](1.2)
* [2](2)
  * [2.1](2.1)
  * [2.2](2.2)
```


Hope `toc` could ease your hand!
