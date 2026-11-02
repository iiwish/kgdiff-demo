# kgdiff demo

This repository shows the [kgdiff](https://github.com/iiwish/kgdiff) GitHub Action on a pull
request. Open the pull request [**October release**](../../pull/1) to see what reviewers get:
a comment that lists every graph change (merges, moves, renames, obsoletions), the same summary
in the job summary, and the interactive HTML report as an artifact.

The whole setup is [one workflow](.github/workflows/graph-diff.yml):

```yaml
- uses: actions/checkout@v7
- uses: iiwish/kgdiff@v0
  with:
    files: |
      ontology/*.obo
      vocab/*.ttl
```

The graphs are two of kgdiff's [example datasets](https://github.com/iiwish/kgdiff/tree/main/examples/datasets):
a small OBO disease ontology and a schema.org-style Turtle vocabulary (CC0).

Try kgdiff without installing anything in the [playground](https://iiwish.github.io/kgdiff/playground.html).
