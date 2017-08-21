# DFDL parser/unparser for pextract and XML

This is a first try on a  [Data Format Description Language (DFDL)](http://dfdlschemas.github.io/) parser and unparser for [pextract](https://github.com/marfors/paradigmextract) paradigm files. The DFDL schema enables to read and modify extracted paradigm files using XML technology. This makes possible lossless archiving of original pextract files alongside a XML database. XML technology can be used to create interfaces and adapters between different data formats.

The XML schema is not definite yet. Any comments welcome.


## Creating XML from pextract files

The DFDL schema has been developed and tested using the open source tool [Daffodil](https://opensource.ncsa.illinois.edu/confluence/display/DFDL).

Parsing the example pextract file.
```shell
$ ../bin/daffodil parse --schema ./pextract.dfdl.xsd ./examples/vot_noun.p
```

## Creating pextract file from XML

Un-parsing the parsed example XML infoset back to a textual pextract file.

```shell
$ ../bin/daffodil unparse --schema ./pextract.dfdl.xsd ./examples/vot_noun.tdml
```
