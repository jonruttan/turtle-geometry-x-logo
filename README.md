# turtle-geometry-x-logo

The programs from *Turtle Geometry: The Computer as a Medium for Exploring
Mathematics* (Abelson and diSessa, MIT Press), written in the book's own
Turtle Procedure Notation and run unchanged on x/Logo —
[x-logo](https://github.com/jonruttan/x-logo), Logo hosted on
[x-lang](https://github.com/jonruttan/x-lang).

Companion code for the [Turtle Geometry blog
series](https://jonruttan.github.io/turtle-geometry/), which works through the
book figure by figure.

## Layout

One `.logo` file per figure or computation, one directory per chapter:

```
chapter-1/
├── figure1.1.logo
├── square.logo
└── …
```

Every commit that adds or changes a program carries the book's coordinates in
its subject (`Figure 1.2a, p.7#fig.0 — …`), in book-presentation order, so
`git log` reads like the book's own build-up.

## Running

CI runs these programs on [x-lang](https://github.com/jonruttan/x-lang)
**v0.4.0**, a release in which Logo shipped with the language: install the `x`
command from that [release's
tarball](https://github.com/jonruttan/x-lang/releases/tag/v0.4.0) (no toolchain
required) and nothing else is needed.

```sh
x -l logo -f chapter-1/square.logo   # batch; writes the bytecode to /tmp/turtle.bc
```

In current x-lang releases Logo is a separate lang,
[x-logo](https://github.com/jonruttan/x-logo), installed once:

```sh
x --install-lang https://github.com/jonruttan/x-logo/releases/latest/download/lang.pin.xon
```

The programs here are not yet run against it in CI.

For a live turtle, run the session, which serves the viewer and prints its
address:

```sh
x -l logo
```

```logo
LOAD "chapter-1/square.logo"
```

## License

[MIT No Attribution](LICENSE), same as x-lang.
