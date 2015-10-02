jts-infer
=========


# Deprecation notice

This is no longer maintained.
Development has moved to:
- https://github.com/scienceai/preview-tabular-data which does the same thing but uses the [Metadata Vocabulary for Tabular Data](http://www.w3.org/TR/tabular-metadata/) to describe the metadata
- https://github.com/scienceai/jsonld-context-infer for the inference part.

---

Infer a
[JSON Table Schema](http://dataprotocols.org/json-table-schema/) from
a readable stream of a
[CSV](http://en.wikipedia.org/wiki/Comma-separated_values) source


[![NPM](https://nodei.co/npm/jts-infer.png)](https://nodei.co/npm/jts-infer/)


#API

##jtsInfer(readableStream, [options], callback)


    var jtsInfer = require('jts-infer)
      , fs = require('fs);

    jtsInfer(fs.createReadStream('path/to/data.csv'), function(err, schema, scores){
      //do something with schema [and scores]
    });


###Options

- ```separator```: separator to separate cells in a row (default to ',')
- ```newline```: separator to separate different rows (default to '\n')
- ```nSample```: if specified only the ```nSample``` first rows of the source will be used to infer the types otherwise all the rows will be used


#Tests

    npm test


#License

MIT
