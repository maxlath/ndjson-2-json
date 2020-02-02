# ndjson-2-json

Minimal CLI converter from [newline-delimited JSON](https://en.wikipedia.org/wiki/JSON_streaming#Line-delimited_JSON) to a [JSON](https://en.wikipedia.org/wiki/JSON) array

Features:
* converts NDJSON to JSON
* uses streams to be able to handle very large files with minimal memory use
* zero validation: you have the responsability to send some proper newline-delimited JSON on `ndjson-2-json` [stdin](https://en.wikipedia.org/wiki/Standard_streams#Standard_input_(stdin))

## Install
```sh
npm i -g ndjson-2-json
```

## How to

```sh
# Convert all a file
cat some.ndjson | ndjson-2-json > some.json
# which can also be written
ndjson-2-json < some.ndjson > some.json

# Convert just the 20 first lines
head -n 20 some.ndjson | ndjson-2-json > 20_first_entries.json
```

## See also
* [ndjson-apply](https://github.com/maxlath/ndjson-apply)
* [ndjson-cli](https://github.com/mbostock/ndjson-cli)
