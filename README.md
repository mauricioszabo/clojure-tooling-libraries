# Clojure Tooling Libraries

## Tooling

* CIDER

* Clojure-LSP (https://github.com/snoe/clojure-lsp)

LSP server using statical analysis

* Orchard

http://metaredux.com/posts/2018/11/09/ciders-orchard-the-heart.html

* REPL-Tooling (https://github.com/mauricioszabo/repl-tooling)

A ClojureScript library that allows editors to connect to socket REPLs, "upgrade" then with UNREPL to work with Clojure or connect to Lumo/Shadow-CLJS.

The idea of the project is that other plug-ins (Clematis and Chlorine) to be just "clients" of this library. They would connect to a host/port, and this library will detect the capabilities of the REPL (is it a Clojure? ClojureScript? ClojureCLR? Lumo?) and return allowed commands. Also, when connecting, the client would register some callbacks that would allow most of evaluate, goto definition, and autocomplete code to run without any editor-specific command. Examples of these callbacks can be `editor-data` (gets current editor's contents, the cursor range, and file name), `open-file-at-position` (open a file at specific row/col, possibily a "virtual" file, readonly, with only some contents), `on-start-eval`, `on-eval`, `on-stdout`, and so on).

## Plug-ins

### Atom
* Chlorine (https://github.com/mauricioszabo/atom-chlorine)

Socket REPL client for Clojure, Shadow-CLJS and Lumo. Supports an integrated REPL, inline eval, autocomplete, goto definition, and refresh namespaces. Written in ClojureScript.

* Proto-REPL (https://github.com/jasongilman/proto-repl)

nREPL client for Clojure, supports an integrated REPL, inline eval, test runner, autocomplete, goto definition, and refresh namespaces. Written in CoffeeScript, with some ClojureScript parts.

### VIM
* Clematis (https://github.com/mauricioszabo/clematis)

Almost nothing works, just a client to REPL-Tooling to "test the waters". Written in ClojureScript.

* Fireplace (https://github.com/tpope/vim-fireplace)

### VS Code
* Calva (https://github.com/BetterThanTomorrow/calva)

nREPL client for Clojure. Supports an integrated REPL, linting, inline eval, test runner.
