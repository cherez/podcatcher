# Podcatcher
A simple command line podcatcher

## Prerequisites
Podcatcher only requires `requests` and `PyYAML` which can be installed with pip. Or use your package manager if that's how you roll.
```pip install pyyaml requests```

It also likes to have `dateutil` installed to parse publication times.
```pip install dateutil```

## Usage
Create a directory named `podcasts` in your home directory, and put a YAML file named `podcasts.yaml` in it.
It should look something like:
```yaml
podcasts:
    -
        url: 'https://feeds.feedburner.com/dancarlin/history'
        path: 'Hardcore History'
    -
        url: 'http://feed.thisamericanlife.org/talpodcast'
        path: 'This American Life'
    -
        url: 'http://feeds.feedburner.com/SlateLexiconValley'
        path: 'Lexicon Valley'
        format: "{index:03} - {title}" #prepend the index so alphabetic sorting gets the right format
format: "{title}" #replace the ugly filenames with the title
threads: 2 #number of podcasts to fetch at a time
playlist: 'playlist.m3u' #create an m3u playlist in each podcast directory
```

Paths are either relative to the podcasts directory or absolute.

Then run `catcher` and the paths should be filled with the files from the podcasts.
