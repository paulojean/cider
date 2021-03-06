# Additional Packages

There are many additional Emacs packages that can enhance your Clojure programming
experience. The majority of the minor modes listed here should be enabled for both
`cider-repl-mode` and `clojure-mode` for optimal effects.

## clj-refactor

[clr-refactor](https://github.com/clojure-emacs/clj-refactor.el) builds on top
of clojure-mode and CIDER and adds a ton of extra functionality (e.g. the
ability to thread/unthread expression, find and replace usages, introduce let
bindings, extract function and so on).

A full list of features is available
[here](https://github.com/clojure-emacs/clj-refactor.el/wiki).

We hope to incorporate some of its features into clojure-mode and CIDER themselves
down the road.

**Make sure that the version of `clj-refactor` you've installed is compatible with
your CIDER version.**

## emidje

[Emidje](https://github.com/nubank/emidje) is a test runner, report
viewer and formatting tool for
[Midje](https://github.com/marick/Midje) within Emacs.

Emidje extends CIDER to provide support for Midje tests in a similar
fashion as `cider-test.el` does for clojure.test tests. In fact, most of
Emidje functionalities were strongly inspired on `cider-test.el`
features.

## helm-cider

[helm-cider](https://github.com/clojure-emacs/helm-cider) provides Helm
interface for certain CIDER commands (e.g. `cider-apropos`).

## cider-hydra

[cider-hydra](https://github.com/clojure-emacs/cider-hydra) provides a nice way
to navigate groups of related CIDER commands.

You can think of it as a fancier [which-key](https://github.com/justbur/emacs-which-key).

## squiggly-clojure

[squiggly-clojure](https://github.com/clojure-emacs/squiggly-clojure) is a
Flycheck checker for Clojure, using tools like
[eastwood](https://github.com/jonase/eastwood),
[core.typed](http://typedclojure.org/) and
[kibit](https://github.com/jonase/kibit).

## sayid

[sayid](http://bpiel.github.io/sayid/) is a powerful alternative of CIDER's
built-in basic tracing functionality.

## Inf-clojure

This package provides basic interaction with a Clojure subprocess (REPL). It's
based on ideas from the popular inferior-lisp package.

[inf-clojure](https://github.com/clojure-emacs/inf-clojure) has two components -
a nice Clojure REPL with auto-completion and a minor mode
(`inf-clojure-minor-mode`), which extends clojure-mode with commands to evaluate
forms directly in the REPL.

It's basically a simple alternative of CIDER, which provides a subset of CIDER's
functionality.

## subword-mode

Enabling `CamelCase` support for editing commands(like
`forward-word`, `backward-word`, etc) in the REPL is quite useful since
we often have to deal with Java class and method names. The built-in
Emacs minor mode `subword-mode` provides such functionality:

```el
(add-hook 'cider-repl-mode-hook #'subword-mode)
```

## Paredit

The use of [paredit](http://mumble.net/~campbell/emacs/paredit.html)
when editing Clojure (or any other Lisp) code is highly
recommended.  You're probably using it already in your `clojure-mode`
buffers (if you're not you probably should). You might also want to
enable `paredit` in the REPL buffer as well:

```el
(add-hook 'cider-repl-mode-hook #'paredit-mode)
```

## Smartparens

[smartparens](https://github.com/Fuco1/smartparens) is an excellent alternative
  to paredit. Many Clojure hackers have adopted it recently and you might want
  to give it a try as well. To enable `smartparens` in the REPL buffer use the
  following code:

```el
(add-hook 'cider-repl-mode-hook #'smartparens-strict-mode)
```

## rainbow-delimiters

[RainbowDelimiters](https://github.com/Fanael/rainbow-delimiters) is a minor
mode which highlights parentheses, brackets, and braces according to their
depth. Each successive level is highlighted in a different color. This makes it
easy to spot matching delimiters, orient yourself in the code, and tell which
statements are at a given depth. Assuming you've already installed
RainbowDelimiters you can enable it in the REPL like this:

```el
(add-hook 'cider-repl-mode-hook #'rainbow-delimiters-mode)
```

## eval-sexp-fu

[eval-sexp-fu](https://github.com/hchbaw/eval-sexp-fu.el) provides some visual
feedback when evaluating expressions. [cider-eval-sexp-fu](https://github.com/clojure-emacs/cider-eval-sexp-fu) provides
CIDER integration for `eval-sexp-fu`.

```el
(require 'cider-eval-sexp-fu)
```
