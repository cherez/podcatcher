# Podcatcher
A simple command line podcatcher

## Prerequisites
Podcatcher only requires `requests` and `PyYAML` which can be installed with pip. Or use your package manager if that's how you roll.
```pip install pyyaml requests```

## Usage
Create a directory named `podcasts` in your home directory, and put a YAML file named `podcasts.yaml` in it.
It should look something like:
```yaml
-
  url: 'https://feeds.feedburner.com/dancarlin/history'
  path: 'Hardcore History'
-
  url: 'http://feed.thisamericanlife.org/talpodcast'
  path: 'This American Life'
```

Paths are either relative to the podcasts directory or absolute absolute.

Then run `catcher` and the paths should be filled with the files from the podcasts.
