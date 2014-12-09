Jsont — JSON data description and codecs for OCaml
-------------------------------------------------------------------------------
Release %%VERSION%%

Jsont describes JSON data structures in OCaml with combinators. The
resulting typed descriptions enable backend JSON codecs to encode and
decode these structures from/to OCaml values.

Jsont's descriptions can be used with different backends. The library
comes with a [Jsonm][1] backend and a JavaScript backend that depends
on [js_of_ocaml][2] and uses the browsers' builtin JSON codecs.

Jsont and its backends depend on [Jsonm][1] and [js_of_ocaml][2]. They
are distributed under the BSD3 license.

Home page: http://erratique.ch/software/jsont
Contact: Daniel Bünzli `<daniel.buenzl i@erratique.ch>`

[1]: http://erratique.ch/software/jsonm
[2]: http://ocsigen.org/js_of_ocaml/


## Installation

Jsont can be installed with `opam`:

    opam install jsonm jsont             # jsonm backend
    opam install js_of_ocaml jsont       # js_of_ocaml backend
    opam isntall jsonm js_of_ocaml jsont # all backends

If you don't use `opam` consult the [`opam`](opam) file for build
instructions.


## Documentation

The documentation and API reference is automatically generated by
`ocamldoc` from the interfaces. It can be consulted [online][5]
and there is a generated version in the `doc` directory of the
distribution.

[5]: http://erratique.ch/software/jsont/doc/Jsont


## Sample programs

If you installed Fut with `opam` sample programs are located in
the directory `opam config var jsont:doc`.

In the distribution sample programs are located in the `test`
directory of the distribution. They can be built with:

    ocamlbuild -use-ocamlfind test/tests.otarget

The resulting binaries are in `_build/test`.

- `test.native` tests the library, nothing should fail.
