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

> ../../bin/tag-zone --file=forbes2016.cross-zone.yaml
Reading zone crossings from 'forbes2016.cross-zone.yaml'
Tagging zones completed in 528.19 ms

> ../../bin/align-time --file=forbes2016.comp-input.yaml
Reading competition from 'forbes2016.comp-input.yaml'
Reading flying time range from 'forbes2016.cross-zone.yaml'
Reading zone tags from 'forbes2016.tag-zone.yaml'
Aligning times completed in 17.71 m

> ../../bin/discard-further --file=forbes2016.comp-input.yaml
Reading competition from 'forbes2016.comp-input.yaml'
Reading task length from 'forbes2016.task-length.yaml'
Reading zone tags from 'forbes2016.tag-zone.yaml'
Filtering times completed in 36.63 s

> ../../bin/mask-track --file=forbes2016.comp-input.yaml
Reading competition from 'forbes2016.comp-input.yaml'
Reading task length from 'forbes2016.task-length.yaml'
Reading flying time range from 'forbes2016.cross-zone.yaml'
Reading zone tags from 'forbes2016.tag-zone.yaml'
Masking tracks completed in 31.65 s

> ../../bin/land-out --file=forbes2016.comp-input.yaml
Reading land outs from 'forbes2016.mask-track.yaml'
Land outs counted for distance difficulty completed in 73.22 ms

> ../../bin/gap-point --file=forbes2016.comp-input.yaml
Reading pilots absent from task from 'forbes2016.comp-input.yaml'
Reading pilots that did not fly from 'forbes2016.cross-zone.yaml'
Reading start and end zone tagging from 'forbes2016.tag-zone.yaml'
Reading masked tracks from 'forbes2016.mask-track.yaml'
Reading distance difficulty from 'forbes2016.land-out.yaml'
Tallying points completed in 683.92 ms
```
