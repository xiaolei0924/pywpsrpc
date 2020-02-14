# pywpsrpc

[![Build Status](https://travis-ci.org/timxx/pywpsrpc.svg?branch=master)](https://travis-ci.org/timxx/pywpsrpc)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Python bindings for WPS Office RPC (for Linux version only).

What is WPS Office RPC?

To make it simple, it means you can use the rpc (api) get working with WPS Office,
open, edit and save documents,
extend the WPS Office functionals etc.

The C++ SDK headers was taken from [wps_cpp](https://dev.tencent.com/u/zouyingfeng/p/wps/git/tree/master/cpp) with *no changes*:
```
Copyright @ 2012-2019, Kingsoft office,All rights reserved.
```

For full API references, go to [https://open.wps.cn/docs/office](https://open.wps.cn/docs/office).

**The project is under heavy development**.


## Requirements
  - Python 3.5+
  - Qt5 (the SDK required both for building & running)
  - WPS Office for Linux 11.1.0.9080+
  - sip 5.x or sip 4.x (for building)
  - python-sip (for running, sip 4.x only)
  - qmake (for building)
  - gcc (for building)

## How to build
  - For sip 5.x (recommended)

    run `sip-build` under the project root directory

  - For sip 4.x

    run `python configure.py` under the project root directory

  append --verbose for getting the progress of building

## Progress

- [x] WPS API bindings
- [x] WPP API bindings
- [x] ET API bindings
- [ ] Memory managerment
  - It seems that the bingings now cause memory leaks.
- [x] Packaging
  - run `sip-wheel` to make the whl package for sip5
- [ ] Python attribute bindings
  - Since now the SDK **DOES NOT** provide the IDispatch way's invoke, we have to find out a way to make it easy calling those get_XXX & put_XXX mehtods
- [ ] Examples
    - For now, only [test_rpcwpsapi.py](./tests/test_rpcwpsapi.py) is available for developing testing.
