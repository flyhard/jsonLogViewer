# Wrapper for the json log viewer  

This is a wrapper for the json log viewer from https://github.com/gistia/json-log-viewer

## Usage

add this to your profile:
```bash
jvFunc() { docker run -it --rm -v "$(dirname $1):/logs" flyhard/json-log-viewer jv "/logs/$(basename $1)"; }
alias jv=jvFunc
```

Now you can do ```jv /any/path/logs/log.json``` and it will load the jsonLogViewer.