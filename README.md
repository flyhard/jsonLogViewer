# Wrapper for the json log viewer  

This is a wrapper for the json log viewer from https://github.com/gistia/json-log-viewer

## Usage

add this to your profile:
```bash
jvFunc() { filename=$(realpath $1); docker run -it --rm -v "$(dirname $filename):/logs" flyhard/json-log-viewer jv "/logs/$(basename $filename)"; }
alias jv=jvFunc
```

Now you can do ```jv /any/path/logs/log.json``` and it will load the jsonLogViewer.