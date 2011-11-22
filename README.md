# XMLWriter for NodeJS

It\'s native and full javascript implementation of the classic XMLWriter class.
The API is complete, flexible and tolerant.
XML is still valid.

# Installation

With [npm](http://npmjs.org) do:

    $ npm install xml-writer


# Examples

## Basic

	var XMLWriter = require('xml-writer');
	xw = new XMLWriter;
	xw.startDocument();
	xw.startElement('root');
	xw.text('Some content');
	xw.endDocument();

	console.log(xw.toString());

Output:


    <?xml version="1.0"?>
	<root>Some content</root>

	
# Tests

Use [nodeunit](https://github.com/caolan/nodeunit) to run the tests.

    $ npm install nodeunit
    $ nodeunit test

# API Documentation

## Generic

### text
Write text

### writeRaw 
Write a raw XML text

## Document
### startDocument(String version = '1.0', String encoding = NULL, Boolean standalone = false) 
Create document tag

### endDocument
End current document

## Element

### writeElement
Write full element tag

### writeElementNS
Write full namespaced element tag

### startElementNS
Create start namespaced element tag

### startElement
Create start element tag

### endElement
End current element

## Attributes

### writeAttribute
Write full attribute

### writeAttributeNS
Write full namespaced attribute

### startAttributeNS
Create start namespaced attribute

### startAttribute
Create start attribute

### endAttribute
End attribute

## Processing Instruction

### writePI
Writes a PI

### startPI
Create start PI tag

### endPI
End current PI

## CData

### writeCData
Write full CDATA tag

### startCData
Create start CDATA tag

### endCData
End current CDATA

## Comment
### writeComment 
Write full comment tag

### startComment 
Create start comment

### endComment 
Create end comment

# Also

* https://github.com/minchenkov/simple-xml-writer

# License

[MIT/X11](./LICENSE)
