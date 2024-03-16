# Helm Charts

This repo uses the subchart pattern for maintaing configuration of charts deployed into my pi cluster in a vcs

# Adding New Charts
To add a new chart, first create the parent chart:
```
helm create <chart name>
```
Add the target chart as a dependency and override custom configurations in the `values.yaml` using the subchart pattern (i.e. place all override under a key that corresponds to the subchart's name).

After adding a chart dependency make sure to run:
```
helm dependency update
```
from within the chart dir


