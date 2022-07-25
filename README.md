# Embedded, low level, no_std Rust resources

View this as [published
slides](https://peter-kehl.github.io/embedded_low_level_rust). Or see the same
content as one [continuous
document](https://github.com/peter-kehl/embedded_low_level_rust/blob/main/README.md).

When viewing this as [published
slides](https://peter-kehl.github.io/embedded_low_level_rust), zoom in or out
(to fit it on your screen - because the slides can't be scrolled down,
unfortunately). Zoom in/out with Ctrl-/Ctrl+ (or Command-/Command+ on Mac), or
with Ctrl and mouse wheel up/down, until you see the following show up numbers
down to 0:
```
    10
    9
    8
    7
    6
    5
    4
    3
    2
    1
    0
```

Note: The content from here until the next horizontal line (`---` in README.md)
is a presenter's note. When viewing this in a browser, you can show it by
pressing "S". (You may need to allow browser to open a new window). See [speaker
view](https://revealjs.com/speaker-view).

Written in [Markdown](https://revealjs.com/markdown), rendered by
[Reveal.js](https://github.com/hakimel/reveal.js) (also
[https://revealjs.com](revealjs.com)). See also this [presentation's
source](https://github.com/peter-kehl/embedded_low_level_rust/blob/main/README.md?plain=1).

# Rendered with: Reveal.js
If you'd like to render this locally (for example, when editing `README.md`),
you need to run a web server. Then you can access this in a web browser as (a
part of) `index.html`. See [Reveal.js > Markdown > External
Markdown](https://revealjs.com/markdown/#external-markdown). You can also [test
snippets of markdown](https://marked.js.org/demo).

This uses my (identical/clean) [clone of Reveal.js](). That's because,
unfortunately, Reveal.js doesn't publish/document how to load its CSS & JS files
online (and they don't seem to be available for public on CDN's, either).
Instead, it wants us to [distribute its
copies](https://revealjs.com/installation). However, that would make the actual
presentation's repository much larger. It would also mean more work when
updating (a copy of) Reveal.js for several presentations. Having the
presentations refer to one clone of Remark.js makes it simpler.

Feel free to refer to my [clone of
Reveal.js](https://peter-kehl.github.io/reveal.js). I will update it whenever
Reveal.js has a new release. Or you can clone Reveal.js yourself.
(Unfortunately, https://hakimel.github.com/reveal.js/dist/reveal.js and related
files are not available.)

To make this GitHub repository show up [on GitHub
Pages](https://peter-kehl.github.io/embedded_low_level_rust), I configured its
GitHub repository's Settings > Pages > Source > Branch: `main` (and `/(root)`).

# Alternative: Remark.js
If you don't want to clone and track Reveal.js, and if you're happy with simpler
and lightweight alternative, try [Remark.js](https://remarkjs.com) (see also its
[wiki](https://github.com/gnab/remark/wiki)). It allows your presentations to
get Remark.js' JS files online (without copying and distributing them).

For an example on how to render it online with Gitlab CLI, see an example of
[slides](https://gitlab.com/indyrs/july2022) and their
[source](https://gitlab.com/indyrs/july2022/-/blob/main/index.html). (This
example is authored by Cameron Dersham, the leader of
[Indy.rs](https://indy.rs), in July 2022. In addition to kindly sharing his
knowledge, his presentation are a good source of important Rust news, both
general and embedded.) As with [Reveal.js](revealjs.com),
[Remark.js](https://remarkjs.com) also allows you to include a [separate
Markdown file](https://github.com/gnab/remark/wiki#external-markdown=). And it
has [slide notes](https://github.com/gnab/remark/wiki/Markdown#slide-notes=) and
[presenter mode](https://github.com/gnab/remark/wiki#getting-started=), too.

Both Reveal.js and Remark.js support code source highlighting. However, only
Reveal.js can highlight specified parts of (lines), and display (parts of)
external source files.
---

# In scope
An overview/introduction to embedded, low level, `no_std`, kernel and
cross-platform development in Rust. Per-architecture dependencies or build
configuration, too.

We also discuss conditional compilation and crate features. Those aspects of
Rust are less involved in small general purpose crate. However, they are useful
in (not low level-specific) development, too.

# Out of scope
Rust, as a systems programming language, is suitable for real time applications.
(Especially because it doesn't have garbage collection, so no unexpected delays,
but it's predictable.) That is true regardless of `no_std`. Indeed, it serves
well in RTOS (Real Time OS) applications, but this is not real
time/RTOS-specific.

`no_std` is tangentially related to `wasm` (Web Assembly). `no_std` crates are
usually
[wasm-friendly](https://rahul-thakoor.github.io/using-no-standard-library-crates-with-webassembly),
but the focus here is not on `wasm`, either.

This is not an introduction to low level/embedded development in general, its
techniques, architectures, tools. It mentions only their touchpoints with Rust.

## Ecosystem
The main focus here is not on the ecosystem. It's rather on Rust language
challenges, patterns and tips.

However, this does mention basic (low level-related) tools, some architectures
and common `no_std` crates. But we refer only to the main stream ones, and/or
ones with the least development pain (with easy debugging, and highest or
emerging Rust support).

# Prerequisites
You don't need any embedded/low level/specialized platform development
experience. Understanding of general (not embedded/low level) Rust helps. You do
need knowledge of a compiled language, build process, hardware components, but
only basics.

---


