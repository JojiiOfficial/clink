# Clink
Have you ever pasted a link in messenger and deleted all those fbclid, utm_source, and so on, GET params by hands? Clink does that for you.

It sits quietly in the background, and if you copy a link to the clipboard, Clink automatically removes those params for you.

## Config

In 0.4.0, we introduced the toml config. Clink will create a "clink.toml" file in a directory where the executable is located on a first-run. In this file, you will find the default config for Clink.

```
# You can find detail description of modes bellow
# one of: remove, your_mom, evil, rickroll
mode = 'remove' 
# Text for your_mom mode  
your_mom = 'your_mom' 
# If true in your_mom mode, Clink will automatically switch to the remove mode in Mother's Day. 
except_mothers_day: true,
# How often Clink will check clipboard in milliseconds
sleep_duration = 150
# Which GET params Clink should update
params = [
    'fbclid', # Facebook click identifier
    'gclid', # Google click identifier
    'gclsrc', # Google Ads
    'dclid', # DoubleClick click identifier (now Google)
    'zanpid', # zanox click identifier (now Awin)
    'utm_source', # Identifies which site sent the traffic 
    'utm_campaign', # Identifies a specific product promotion or strategic campaign
    'utm_medium', # Identifies what type of link was used
    'utm_term', # Identifies search terms
    'utm_content', Identifies what specifically was clicked to bring the user to the site
]
```

## Modes

* remove - removes params from links in clipboard
* your_mom - Sets values to "your_mom" (inspired by this [tweet](https://twitter.com/ftrain/status/1359138516681314311?s=21))
* evil -  swap two random chars in values (Diabolical Laughter)
* rickroll -  Rickroll them by replacing the actual value with a base64 encoded youtube link

## Build

### Linux

Make sure that you have libxcb-composite0-dev installed 
```
sudo apt-get install libxcb-composite0-dev
```

### MacOs

Works right away

### Windows

Should work but not tested, yet.

