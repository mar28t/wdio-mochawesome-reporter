WDIO Mochawesome Reporter
=========================

Generates test results in the json formated needed to create [Mochawesome](https://github.com/adamgruber/mochawesome) reports.


## Installation

```shell
npm install --save wdio-mochawesome-reporter
```

A dependency will be added to your `package.json`

```json
{
  "dependencies": {
    "wdio-mochawesome-reporter": "^1.0.0"
  }
}
```

## Using

 Add to the list of reporters

```js
// sample wdio.conf.js
module.exports = {
  // ...
  reporters: ['dot', 'mochawesome'],
  reporterOptions: {
    outputDir: './'
  },

  // ...
};
```
## Mochawesome Report Generator
To convert the json generated by this package into a Mochawesome report you will need to use the [Mochawesome Report Generator](https://github.com/adamgruber/mochawesome-report-generator).

In summary...

* Add the package to your project
```shell
npm install --save mochawesome-report-generator
```

* Add a script to your package.json to generate the report
```json
  "scripts": {
    "generateMochawesome":"marge path/to/results.json --reportTitle 'My Project Results'"
  },
```
1) `path/to/results.json` = path and name of json file
2) `--reportTitle 'My Project Results' = unique report title