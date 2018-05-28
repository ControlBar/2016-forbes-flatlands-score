# Scoring Log

With this repo and [flare-timing](https://github.com/BlockScope/flare-timing)
cloned as siblings the following commands show how to score all tasks at once
for the **2016 Forbes Flatlands** competition.

```
> ../../bin/extract-input --file=forbes2016.fsdb
Extracted 6 tasks from "2016 Forbes Flatlands"
Extracting tasks completed in 1.23 s

> ../../bin/task-length --file=forbes2016.comp-input.yaml
forbes2016.comp-input.yaml
Measuring task lengths completed in 3.33 m

> ../../bin/cross-zone --file=forbes2016.comp-input.yaml
Reading competition from 'forbes2016.comp-input.yaml'
Tracks crossing zones completed in 34.39 s
```
