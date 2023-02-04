# testcafe-reporter-testrail-sh-cust
[![Build Status](https://travis-ci.org/khar4enko.maxim@gmail.com/testcafe-reporter-testrail-sh-cust.svg)](https://travis-ci.org/khar4enko.maxim@gmail.com/testcafe-reporter-testrail-sh-cust)

This is the **testrail-sh-cust** reporter plugin for [TestCafe](http://devexpress.github.io/testcafe).

<p align="center">
    <img src="https://raw.github.com/khar4enko.maxim@gmail.com/testcafe-reporter-testrail-sh-cust/master/media/preview.png" alt="preview" />
</p>

## Install

```
npm install testcafe-reporter-testrail-sh-cust
```

## Usage

```
TestCases should have the TestRail case ids present in the test meta in the format {testRailCaseId: 'C12345'}
```
test.meta({testRailCaseId: 'C239234'})

```
The reporter requires 3 environment variables to be present
```
```
TESTRAIL_HOST: https://some.testrail.com
TESTRAIL_USERNAME: username
TESTRAIL_APIKEY: password or api key
```
When you run tests from the command line, specify the reporter name by using the `--reporter` option:

```
testcafe chrome 'path/to/test/file.js' --reporter testrail-sh-cust
```


When you use API, pass the reporter name to the `reporter()` method:

```js
testCafe
    .createRunner()
    .src('path/to/test/file.js')
    .browsers('chrome')
    .reporter('testrail-sh-cust') // <-
    .run();
```

## Author
 (http://no)
