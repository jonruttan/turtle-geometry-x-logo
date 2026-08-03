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

From an x-lang checkout:

```sh
sh x.sh -l logo                     # REPL + live viewer on localhost:8080
```

```logo
LOAD "chapter-1/square.logo"
```

Or in batch, which writes the turtle's bytecode stream to `/tmp/turtle.bc`:

```sh
sh x.sh -l logo -f chapter-1/square.logo
```

## License

[MIT No Attribution](LICENSE), same as x-lang.
