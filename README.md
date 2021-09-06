<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# Lucas Number

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> Maximum safe [Lucas number][lucas-number] when stored in [double-precision floating-point][ieee754] format.

<section class="installation">

## Installation

```bash
npm install @stdlib/constants-float64-max-safe-lucas
```

</section>

<section class="usage">

## Usage

```javascript
var FLOAT64_MAX_SAFE_LUCAS = require( '@stdlib/constants-float64-max-safe-lucas' );
```

#### FLOAT64_MAX_SAFE_LUCAS

The maximum [safe][safe-integers] [Lucas number][lucas-number] when stored in [double-precision floating-point][ieee754] format.

```javascript
var bool = ( FLOAT64_MAX_SAFE_LUCAS === 7639424778862807 );
// returns true
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var FLOAT64_MAX_SAFE_LUCAS = require( '@stdlib/constants-float64-max-safe-lucas' );

var v;
var i;

function lucas( n ) {
    var a;
    var b;
    var c;
    var i;

    a = 2;
    if ( n === 0 ) {
        return a;
    }
    b = 1;
    for ( i = 2; i <= n; i++ ) {
        c = a + b;
        a = b;
        b = c;
    }
    return b;
}

for ( i = 0; i < 100; i++ ) {
    v = lucas( i );
    if ( v > FLOAT64_MAX_SAFE_LUCAS ) {
        console.log( 'Unsafe: %d', v );
    } else {
        console.log( 'Safe:   %d', v );
    }
}
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   [`@stdlib/constants/float64/max-safe-fibonacci`][@stdlib/constants/float64/max-safe-fibonacci]: maximum safe Fibonacci number when stored in double-precision floating-point format.
-   [`@stdlib/constants/float64/max-safe-nth-lucas`][@stdlib/constants/float64/max-safe-nth-lucas]: maximum safe nth Lucas number when stored in double-precision floating-point format.

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/constants-float64-max-safe-lucas.svg
[npm-url]: https://npmjs.org/package/@stdlib/constants-float64-max-safe-lucas

[test-image]: https://github.com/stdlib-js/constants-float64-max-safe-lucas/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/constants-float64-max-safe-lucas/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/constants-float64-max-safe-lucas/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/constants-float64-max-safe-lucas?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/constants-float64-max-safe-lucas.svg
[dependencies-url]: https://david-dm.org/stdlib-js/constants-float64-max-safe-lucas/main

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/constants-float64-max-safe-lucas/main/LICENSE

[safe-integers]: http://www.2ality.com/2013/10/safe-integers.html

[lucas-number]: https://en.wikipedia.org/wiki/Lucas_number

[ieee754]: https://en.wikipedia.org/wiki/IEEE_754-1985

<!-- <related-links> -->

[@stdlib/constants/float64/max-safe-fibonacci]: https://github.com/stdlib-js/constants-float64-max-safe-fibonacci

[@stdlib/constants/float64/max-safe-nth-lucas]: https://github.com/stdlib-js/constants-float64-max-safe-nth-lucas

<!-- </related-links> -->

</section>

<!-- /.links -->
