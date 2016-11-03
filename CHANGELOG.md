
1.3.2 / 2016-01-10
==================

  * int64: fix failing OS X tests now
  * int64: better error handling for Linux

1.3.1 / 2015-12-02
==================

  * writeUInt64: better error checking for `WriteUInt64()`
  * writeUInt64: allow hex or octal input string values

1.3.0 / 2015-12-02
==================

  * writeInt64: better error checking for `WriteInt64()`
  * writeInt64: allow hex or octal input string values
  * appveyor: test node v5
  * travis: test node v5

1.2.0 / 2015-10-08
==================

  * force Buffer length to 0 if NULL is read (#42, @saneki)

1.1.3 / 2015-09-23
==================

  * appveyor: remove v1
  * speed increase by avoiding `JSON.stringify()` constant call (#39, @dan-tull)

1.1.2 / 2015-09-19
==================

  * CString: allow a Buffer to be used as backing store in `set()` (https://github.com/node-ffi/node-ffi/issues/169)
  * travis, appveyor: test Node.js v4

1.1.1 / 2015-09-14
==================

  * remove unused WrapPointer overload (fix compile warning)
  * appveyor: better Windows testing

1.1.0 / 2015-08-26
==================

  * appveyor: 2.5 + 3 added
  * appveyor: attempt to fix v0.8 and v0.10
  * int64 conversion works with debug mode iojs runtime
  * persistent size fixed
  * better automated testing
  * package: update "weak" to v1
  * package: add "MIT" license field
  * NAN 2.0 support (#33, @unbornchikken)

1.0.2 / 2015-05-09
==================

  * package: update "nan" to v1.8.4 (#30, @mafintosh)
  * README: use SVG for appveyor badge

1.0.1 / 2015-03-22
==================

  * package: update "nan" to v1.7.0
  * appveyor: test node v0.12, don't test v0.11
  * travis: test node v0.12, don't test v0.11
  * README: add link to Known Types page

1.0.0 / 2015-01-20
==================

  * bumping to v1.0.0 for better semver semantics
  * travis: don't test node v0.8.x

0.3.5 / 2015-01-18
==================

  * src: add SET_SIZEOF and SET_ALIGNOF macros

0.3.4 / 2015-01-18
==================

  * package: update "nan" to v1.5.1
  * travis: don't test node v0.6.x
  * use `v8::Object::ForceSet` instead of `v8::Object:Set` (#20, @sarangsapre)

0.3.3 / 2014-12-29
==================

  * package: allow any "debug" v2
  * add support for `Buffer#reinterpret()` with `offset` (#18, @deepak1556)

0.3.2 / 2014-06-19
==================

  * src: fix comment typo
  * src: define our own `kMaxLength` constant

0.3.1 / 2014-06-09
==================

  * src: allow Buffers returned from `reinterpretUntilZeros()` up to `kMaxLength` bytes
  * test: move the reinterpretUntilZeros() tests to their own file
  * test: fix `Buffer#inspect()` test on Windows

0.3.0 / 2014-06-08
==================

  * ref: use `hexAddress()` for the Buffer inspect() override
  * ref: add `hexAddress()` function
  * src: use `NanEscapableScope` where appropriate
  * src: use `uintptr_t` to ensure a positive address
  * src: better _snprintf_s #define macro (#12, @fjhub)
  * package: update "debug" to v1.0.1

0.2.3 / 2014-06-04
==================

  * package: update "nan" to v1.2.0
  * src: remove commented code

0.2.2 / 2014-06-01
==================

  * package: update "nan" to v1.1.2
  * travis: remove IRC notifications from Travis

0.2.1 / 2014-05-27
==================

  * package: pin dev dependency versions
  * package: use explicit nan commit with LLVM fix
  * README: use https for Travis URL
  * travis: test node v0.6.x

0.2.0 / 2014-05-26
==================

  * binding: use `rvagg/nan` for node v0.8, v0.10, and v0.11 compat
  * package: update "nan" to v1.1.0
  * package: remove "engines" section
  * README: add appveyor test badge
  * README: use .svg for Travis badge
  * add appveyor.yml file
  * .travis: don't test node v0.9.x
  * package: beautify
  * add a `persistent` option to writeObject()
  * make passing `ref.NULL` to allocCString() work as expected
  * docs: document the "length" parameter of ref.readPointer()

0.1.3 / 2012-09-25
==================

  * fix compiler warnings on Windows

0.1.2 / 2012-09-02
==================

  * allow an offset as the third argument to the "reinterpret" functions

0.1.1 / 2012-08-03
==================

  * prevent multiple instances of ref from chaining inspects in "overwriteInspect"

0.1.0 / 2012-07-22
==================

  * initial release of the documentation (http://tootallnate.github.com/ref)
  * binding: make "endianness" and "NULL" be 'frozen'
  * lib: make derefType() throw an Error when given a "type" with indirection 1
  * augment the Buffer#inspect() function to print out the memory address as well

0.0.20 / 2012-06-27
===================

  * rename the `Utf8String` type to `CString` (#5)
  * make `Utf8String` an alias to `CString` and deprecated
  * more work on docs (not yet ready)

0.0.19 / 2012-06-25
==================

  * use node-bindings

0.0.18 / 2012-06-21
===================

  * add the non-native-endian read+write int64 functions
  * starting on some real (inline) documentation

0.0.17 / 2012-06-05
===================

  * allow the "bool" type to write arbitrary number values (0-255) to it
  * Utf8String: return JS `null` when reading a pointer pointing to NULL
  * make `reinterpret()` and `reinterpretUntilZeros()` throw an Error when given a NULL pointer
  * make `ref.get()` and `ref.set()` coerce their optional type when given
  * some more tests

0.0.16 / 2012-06-01
===================

  * use Object.create() and Object.getPrototypeOf() for `refType()` and `derefType()`
  * remove `cloneType()`
  * make reading from a NULL pointer always throw an Error:
    * readCString()
    * readPointer()
    * readObject()
    * readInt64()
    * readUInt64()

0.0.15 / 2012-05-31
===================

  * fix possible segmentation fault with `readObject()`
  * fix possible segmentation fault with `readPointer()`

0.0.14 / 2012-05-31
===================

  * fix possible segmentation fault with `readCString()`

0.0.13 / 2012-05-30
===================

  * make `refType()` coerce string types properly
  * make the `bool` type inherit from a proper fixed type (like `uint8`)

0.0.12 / 2012-05-30
===================

  * make the "char" and "uchar" types accept JS String values
  * make the synonym types (i.e. longlong is a synonym for int64) be distinct objects, rather than simple JS references
  * fix coersion of a string value of "Object"
  * added the `reinterpretUntilZeros()` function

0.0.11 / 2012-05-17
===================

  * always do string type coersion, like on `alloc()`
  * add a "bool" type, which works with JS `true`/`false` values

0.0.10 / 2012-05-15
===================

  * fix compiler error on Solaris
  * fix compiler errors on Windows

0.0.9 / 2012-05-13
==================

  * allow `ref.alloc()` to not have a value being set with it
  * add the `coerceType()` function (get a proper "type" instance from a string)
  * add the Utf8String type back over from node-ffi
  * conditionally extend SlowBuffer.prototype for node >= v0.7.9

0.0.8 / 2012-05-12
==================

  * make the `void` type "set()" function be a no-op instead of throwing
  * added some more test cases

0.0.7 / 2012-05-09
==================

  * added the `reinterpret()` function

0.0.6 / 2012-05-09
==================

  * add `alignof` mappings for the types
  * add an `Object` type
  * set the `alignment` property on the built-in types

0.0.5 / 2012-05-09
==================

  * quickly add get() and set() functions
  * use the `PRId64` and `PRIu64` snprintf types

0.0.4 / 2012-05-08
==================

  * README improvements; some API documentation
  * removed some leftover debugging statements

0.0.3 / 2012-05-08
==================

  * added `readCString()` function (to `Buffer.prototype` as well)
  * added `writeCString()` function (to `Buffer.prototype` as well)
  * added an `allocCString()` function
  * removed the `Utf8String` type; moved it to node-ffi
  * made `ref.NULL` be a 'void' type

0.0.2 / 2012-05-05
==================

  * Added missing includes for Linux, etc.

0.0.1 / 2012-05-04
==================

  * Initial release