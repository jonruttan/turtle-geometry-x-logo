# turtle-geometry-x-logo

The programs from *Turtle Geometry: The Computer as a Medium for Exploring
Mathematics* (Abelson and diSessa, MIT Press), written in the book's own
Turtle Procedure Notation and run unchanged on x/Logo — the Logo dialect of
[x-lang](https://github.com/jonruttan/x-lang).

Companion code for the [Turtle Geometry blog
series](https://jonruttan.github.io), which works through the book figure by
figure.

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

Requires [x-lang](https://github.com/jonruttan/x-lang) **v0.4.0 or later** — the
Logo dialect ships with the language, so a release is all you need. Install the
`x` command from a [release tarball](https://github.com/jonruttan/x-lang/releases)
(no toolchain required):

```sh
x -l logo -f chapter-1/square.logo   # batch; writes the bytecode to /tmp/turtle.bc
```

For a live turtle, run the REPL and viewer from an x-lang checkout:

```sh
sh x.sh -l logo                     # REPL + live viewer on localhost:8080
```

```logo
LOAD "chapter-1/square.logo"
```

## License

[MIT No Attribution](LICENSE), same as x-lang.
