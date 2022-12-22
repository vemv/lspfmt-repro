## Bug repro

For https://github.com/clojure-lsp/clojure-lsp/issues/1421

You can repeatedly run these two commands:

```bash
clojure -m clojure-lsp.main format
clojure -m clojure-lsp.main clean-ns
```

...and each command will apply a slightly different formatting.

So given that disagreement, it's not possible to use both as a CI check simultaneously.
