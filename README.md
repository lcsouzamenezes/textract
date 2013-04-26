textract
========

A text extraction node module.

## Currently Extracts...

* PDF
* DOC
* DOCX
* `application/javascript`
* All `text/*` mime-types.

Does textract not extract from files of the type you need?  Add an issue or submit a pull request.  It's super easy to add an extractor for a new mime type.

## Install

```
npm install textract
```

## Requirements

* `PDF` extraction requires `pdftotext` be installed
* `DOC` extraction requires `catdoc` be installed
* `DOCX` extraction requires `unzip` be available

## Import

```javascript
var textract = require('textract');
```

## Usage

If you do not know the mime type of the file

```javascript
textract(filePath, function( error, text ) {

})
```

If you know the mime type of the file

```
textract(type, filePath, function( error, text ) {

})
```

Error will contain informative text about why the extraction failed. If textract does not currently extract files of the type provided, a `typeNotFound` flag will be tossed on the error object.

