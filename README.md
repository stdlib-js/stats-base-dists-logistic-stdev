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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Standard Deviation

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Logistic][logistic-distribution] distribution [standard deviation][standard-deviation].

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

The [standard deviation][standard-deviation] for a [logistic][logistic-distribution] random variable with location `μ` and scale `s > 0` is

<!-- <equation class="equation" label="eq:logistic_stdev" align="center" raw="\sigma = \tfrac{s\pi}{\sqrt{3}}" alt="Standard deviation for a logistic distribution."> -->

```math
\sigma = \tfrac{s\pi}{\sqrt{3}}
```

<!-- <div class="equation" align="center" data-raw-text="\sigma = \tfrac{s\pi}{\sqrt{3}}" data-equation="eq:logistic_stdev">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@51534079fef45e990850102147e8945fb023d1d0/lib/node_modules/@stdlib/stats/base/dists/logistic/stdev/docs/img/equation_logistic_stdev.svg" alt="Standard deviation for a logistic distribution.">
    <br>
</div> -->

<!-- </equation> -->

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import stdev from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-logistic-stdev@v0.1.1-esm/index.mjs';
```

#### stdev( mu, s )

Returns the [standard deviation][standard-deviation] for a [logistic][logistic-distribution] distribution with location parameter `mu` and scale parameter `s`.

```javascript
var y = stdev( 2.0, 1.0 );
// returns ~1.814

y = stdev( 0.0, 1.0 );
// returns ~1.814

y = stdev( -1.0, 4.0 );
// returns ~7.255
```

If provided `NaN` as any argument, the function returns `NaN`.

```javascript
var y = stdev( NaN, 1.0 );
// returns NaN

y = stdev( 0.0, NaN );
// returns NaN
```

If provided `s <= 0`, the function returns `NaN`.

```javascript
var y = stdev( 0.0, 0.0 );
// returns NaN

y = stdev( 0.0, -1.0 );
// returns NaN
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import randu from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@esm/index.mjs';
import stdev from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-logistic-stdev@v0.1.1-esm/index.mjs';

var mu;
var s;
var y;
var i;

for ( i = 0; i < 10; i++ ) {
    mu = ( randu()*10.0 ) - 5.0;
    s = randu() * 20.0;
    y = stdev( mu, s );
    console.log( 'µ: %d, s: %d, SD(X;µ,s): %d', mu.toFixed( 4 ), s.toFixed( 4 ), y.toFixed( 4 ) );
}

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-logistic-stdev.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-logistic-stdev

[test-image]: https://github.com/stdlib-js/stats-base-dists-logistic-stdev/actions/workflows/test.yml/badge.svg?branch=v0.1.1
[test-url]: https://github.com/stdlib-js/stats-base-dists-logistic-stdev/actions/workflows/test.yml?query=branch:v0.1.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-logistic-stdev/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-logistic-stdev?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-logistic-stdev.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-logistic-stdev/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-logistic-stdev/tree/deno
[umd-url]: https://github.com/stdlib-js/stats-base-dists-logistic-stdev/tree/umd
[esm-url]: https://github.com/stdlib-js/stats-base-dists-logistic-stdev/tree/esm
[branches-url]: https://github.com/stdlib-js/stats-base-dists-logistic-stdev/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-logistic-stdev/main/LICENSE

[logistic-distribution]: https://en.wikipedia.org/wiki/Logistic_distribution

[standard-deviation]: https://en.wikipedia.org/wiki/Standard_deviation

</section>

<!-- /.links -->
