# ByteString: Fast, Packed Vectors of Bytes

[![Build Status](https://github.com/haskell/bytestring/workflows/ci/badge.svg)](https://github.com/haskell/bytestring/actions?query=workflow%3Aci) [![Hackage](http://img.shields.io/hackage/v/bytestring.svg)](https://hackage.haskell.org/package/bytestring) [![Hackage CI](https://matrix.hackage.haskell.org/api/v2/packages/bytestring/badge)](https://matrix.hackage.haskell.org/package/bytestring) [![Stackage LTS](http://stackage.org/package/bytestring/badge/lts)](http://stackage.org/lts/package/bytestring) [![Stackage Nightly](http://stackage.org/package/bytestring/badge/nightly)](http://stackage.org/nightly/package/bytestring)

This library provides the `Data.ByteString` module -- strict and lazy
byte arrays manipulable as vectors -- providing very time/space-efficient
vector and IO operations.

For very large data requirements, or constraints on heap size,
`Data.ByteString.Lazy` is provided, a lazy list of byte vector chunks.
Efficient processing of multi-gigabyte data can be achieved this way.

The library also provides `Data.ByteString.Builder` for efficient construction
of `ByteString` values from smaller pieces during binary serialization.

Requirements:

  * Cabal 1.10 or greater
  * GHC 7.0 or greater

### Naming

Although the name of the data type (and package) refers to "string",
the data type is actually more accurately a *vector* of bytes.

### Authors

`ByteString` was derived from the GHC `PackedString` library,
originally written by Bryan O'Sullivan, and then by Simon Marlow.
It was adapted and greatly extended for darcs by David Roundy and
others. Don Stewart and Duncan Coutts cleaned up and further extended
the implementation and added the `.Lazy` code. Simon Meier contributed
the `Builder` feature.
