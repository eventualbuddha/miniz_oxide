<a name="0.7.1"></a>
### 0.7.1 (2023-02-02)
* **inflate:**
  * Fix for older versions of Rust (thanks jasonish) ([a65d0751](https://github.com/Frommi/miniz_oxide/commit/a65d0751f83c4e518cfecbf18e19de22692ae2b7))

<a name="0.7.0"></a>
### 0.7.0 (2023-02-01)

Yanked release

<a name="0.6.4"></a>
## 0.6.4 (2023-02-01)

Yanked release due to version requirement bump

* **inflate:**
  * move debug assert condition to if stmt  (thanks connorskees) ([b6d8824a](https://github.com/Frommi/miniz_oxide/commit/b6d8824a316522c292968f807c6455c1ec421bea))

<a name="0.6.3"></a>
## 0.6.3 (2023-02-01)

Yanked release due to version requirement bump

#### Bug Fixes

* **inflate:**
  *  Reject input with too many litlen codes as per spec/zlib ([f4ee585e](https://github.com/Frommi/miniz_oxide/commit/f4ee585eb382eeb7ea1db16458438c637de48349)), closes [#130](https://github.com/Frommi/miniz_oxide/issues/130)
* **deflate:**
  * Remove #\[inline(always)\] from CompressorOxide::default() (thanks jrmuizel) ([c7643aa2](https://github.com/Frommi/miniz_oxide/commit/c7643aa2ddd5c2ca45f6f506b281ee988ea8a296))
#### Features
* **inflate:**
  *  optimize inflate::core::transfer (thanks connorskees) ([dd2fa3e3](https://github.com/Frommi/miniz_oxide/commit/dd2fa3e33c7d8ce1bb8bbd7329a0dd571f4e2df6))
  *  optimize inflate::core::init_tree by precomputing reversed bits (thanks connorskees) ([bf660972](https://github.com/Frommi/miniz_oxide/commit/bf660972bcad23717e811e44b7ad8388ba5f29ec)), closes [#82](https://github.com/Frommi/miniz_oxide/issues/82)

#### Other
  * various typo/doc/ci fixes (thanks LollipopFt, striezel, jarede-dev)

## [0.6.2] - 2022-09-04

### Features

- Add std feature to allow error trait for DecompressError and other stuff later down the line
- impl Display for DecompressError

## [0.6.1] - 2022-08-25

### Bug Fixes

- Make building with --no-default-features actually work

<a name="0.6.0"></a>
## 0.6.0 (2022-08-21)

#### Bug Fixes

* **inflate:**  
  * Fix output size limit handling (thanks Shnatsel) ([c08ac1c6](https://github.com/Frommi/miniz_oxide/commit/c08ac1c60699025fea9c39250a41be54c6267813)), closes [#119](https://github.com/Frommi/miniz_oxide/issues/119))

#### Features

* **inflate:**
  * Return currently decompressed data on failure in decompress_to_vec.. functions ([81796330](https://github.com/Frommi/miniz_oxide/commit/8179633092b032b783333c73395490b6b9243823)), closes [#113](https://github.com/Frommi/miniz_oxide/issues/113))
  * Allow for running without allocator (inflate-only) ([96ad0b80](https://github.com/Frommi/miniz_oxide/commit/96ad0b80e107290be872bf8f010fa21d3ca790fe)), closes [#111](https://github.com/Frommi/miniz_oxide/issues/111))


<a name="0.5.4"></a>
### 0.5.4 (2022-05-30)

#### Bug Fixes

* **inflate:**  Backport fix for [#119](https://github.com/Frommi/miniz_oxide/issues/119)) for 0.5 releases ([7d38417c](https://github.com/Frommi/miniz_oxide/commit/7d38417c8ca18ec0cf38a01f66f7e0776b33a1b1))

<a name="0.5.3"></a>
### 0.5.3 (2022-05-30)

Clippy warnings and doc fixes (thanks @hellow554 and @MichaelMcDonnell)

#### Bug Fixes

* **core:**  Don't use simd-adler32 when building as part of std  ([5869904c](https://github.com/Frommi/miniz_oxide/commit/d3dee8760fd8b390ca079e8a80cb28f71948c379))

<a name="0.5.2"></a>
### 0.5.2 (2021-12-04)


#### Bug Fixes

* **inflate:**  Don't return HasMoreOutput if we are waiting for more input to read adler32 ([5869904c](https://github.com/Frommi/miniz_oxide/commit/5869904c7f789580ace18f7e9084acbcd54a95be))

#### Features

* **inflate:**   Add decompress_slice_iter_to_slice function. ([a359d678](https://github.com/Frommi/miniz_oxide/commit/a359d678c8d83565844ac5075e50c43d67d29879))


<a name="0.5.1"></a>
### 0.5.1 (2021-11-11)

Doc updates and minor refactor

<a name="0.5.0"></a>
## 0.5.0 (2021-11-04)


#### Bug Fixes

* **core:**
  * Don't use autofcg for alloc ([a9bf654f](https://github.com/Frommi/miniz_oxide/commit/a9bf654f6a6756eed0812e612d19137f5c486444), closes [#106](https://github.com/Frommi/miniz_oxide/issues/106))

#### Features

* **core:**
  * Add github actions CI and remove unused feature ([694803aa](https://github.com/Frommi/miniz_oxide/commit/694803aaf0bd4af7d00c08c10881bc121f1fb2c7), closes [#107](https://github.com/Frommi/miniz_oxide/issues/107))
  * Add optional use of simd-adler32 instead of adler behind simd feature flag ([19782aa](https://github.com/Frommi/miniz_oxide/commit/19782aa0833d201eed6bcbc847eefaa741bc2e32))

* **inflate:**
  * add option to ignore and not compute zlib checksum when decompressing ([2e9408ae](https://github.com/Frommi/miniz_oxide/commit/2e9408ae4cad10a00c604a008bd4f8c0704f0ac7), closes [#102](https://github.com/Frommi/miniz_oxide/issues/102))


<a name="0.4.4"></a>
### 0.4.4 (2021-02-25)

#### Features

* **core:**
  * Update adler to 1.0 ([b4c67ba0](https://github.com/Frommi/miniz_oxide/commit/b4c67ba06fc526a012d078efc925494d788b88d0))
  * Mark some internal functions as const ([52ce377a](https://github.com/Frommi/miniz_oxide/commit/28514ec09f0b1ce74bfb2d561de52a6652ce377a))

<a name="0.4.3"></a>
### 0.4.3 (2020-10-07)

#### Features

* **core:**
  * Increase the license options ([78d13b47](https://github.com/Frommi/miniz_oxide/commit/78d13b47))
  * Add forbid unsafe code to build ([80859093](https://github.com/Frommi/miniz_oxide/commit/80859093c1298ff5a97e149d9e3a882ce92fbde5))

#### Bug Fixes

* **core:**
  * in-libstd build attempting to use std ([5a5522de](https://github.com/Frommi/miniz_oxide//commit/5a5522de50129513cb059e73020c8f1aad047200))
  * Run CI on 1.34 ([c6f6cd42](https://github.com/Frommi/miniz_oxide/commit/c6f6cd42e8225ca2f32d6e8fd5a2ce6e99b9c7b1))

<a name="0.4.2"></a>
### 0.4.2 (2020-09-13)

#### Features

* **core:**
  * Add automatic alloc detection ([0c67dc5c](https://github.com/Frommi/miniz_oxide/commit/0c67dc5c))

#### Bug Fixes

* **inflate:**
  * Add missing pub to FullReset's data format ([743d6d37](https://github.com/Frommi/miniz_oxide/commit/743d6d37))

<a name="0.4.1"></a>
### 0.4.1 (2020-08-22)

#### Features

* **inflate:**
  * Add support for limiting output size when decompressing to vec  ([f8c25f3f](https://github.com/Frommi/miniz_oxide/commit/f8c25f3f))
  * Introduce reset policy to control InflateState::reset ([1f95a16f](https://github.com/Frommi/miniz_oxide/commit/1f95a16f)), closes [#89](https://github.com/Frommi/miniz_oxide/issues/89))

* **core:**
  * Add an optional feature for 1.34.2 backwards compatibility ([d18e847d](https://github.com/Frommi/miniz_oxide/commit/d18e847d))

<a name="0.4.0"></a>
## 0.4.0 (2020-06-28)


#### Features

* **core:**
  *  Switch from adler32 to adler crate ([ad0f8fef](https://github.com/Frommi/miniz_oxide/commit/ad0f8fef))
  *  Flag `miniz_oxide` as a `#![no_std]` library ([7f5aedd7](https://github.com/Frommi/miniz_oxide/commit/7f5aedd7))


<a name="0.3.7"></a>
## 0.3.7 (2020-04-30)


#### Bug Fixes

* **deflate:**
  *  overflow panic with very large input buffer ([f0b0e8fd](https://github.com/Frommi/miniz_oxide/commit/f0b0e8fd))
  *  compress_to_vec infinite loop ([f3299c8e](https://github.com/Frommi/miniz_oxide/commit/f3299c8e), closes [#75](https://github.com/Frommi/miniz_oxide/issues/75))
