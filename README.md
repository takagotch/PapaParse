### PapaParse
---
https://github.com/mholt/PapaParse

https://www.papaparse.com/docs
```
npm install papaparse
```

```js
//csv to json
Papa.parse(csvString[, config])
Papa.parse(file, config)

Papa.parse(url, {
  download: true,
});
//json to csv
Papa.unparse(data[, config])
{
  quotes: false,
  quoteChar: '"',
  escapeChar: '"',
  delimiter: ",",
  header: true,
  newline: "\r\n"
}
var csv = Papa.unparse([
  ["1-1", "1-2", "1-3"],
  ["2-1", "2-2", "2-3"]
]);
var csv = Papa.unparse([
  {
    "Column 1": "foo",
    "Column 2": "bar"
  },
  {
    "Column 1": "abc",
    "Column 2": "def"
  }
]);
var csv = Papa.unparse({
  fields: ["Column 1", "Column 2"],
  data: [
   ["foo", "bar"],
   ["abc", "def"]
  ]
});

{
  delimiter: "", 
  newline: "",
  quoteChar: '"',
  escapeChar: '"',
  header: false,
  transformHeader: undefined,
  dynamicTyping: false,
  preview: 0,
  encoding: "",
  worker: false,
  comments: false,
  step: undefined,
  complete: undefined,
  error: undefined,
  download: false,
  skipEmptyLines: false,
  chunk: undefined,
  fastMode: undefined,
  beforeFirstChunk: undefined,
  withCredentials: undefined,
  transform: undefined
}

step: function(results, parser){
  console.log("Row data:", results.data);
  console.log("Row errors:", results.errors);
}

complete: function(results, file){
  console.log("Parsing complete:", results, file);
}

{
  data:
  errors:
  meta: 
}

[
  ["Column 1", "Column 2"],
  ["foo", "bar"],
  ["abc", "def"]
]
[
  {
     "Column 1": "foo",
     "Column 2": "bar"
  },
  {
    "Column 1": "abc",
    "Column 2": "def"
  }
]

{
  type: "",
  code: "",
  message: "",
  row: 0,
}

{
  delimiter:
  linebreak:
  aborted:
  fields:
  truncated:
}
```

```js
$('input[type=file]').parse({
  config: {},
  before: function(file, inputElem)
  {
  },
  error: function(err, file, inputElem, reason)
  {
  },
  omplete: function()
  {
  }
});

{
  action: "abort",
  reason: "Some reason",
  config: //
}
```
