H5SectionsArrays.jl
===================
[![Build Status](https://travis-ci.org/seung-lab/H5SectionsArrays.jl.svg?branch=master)](https://travis-ci.org/seung-lab/H5SectionsArrays.jl)

cutout chunks from sections of hdf5 files as a Julia array
- only support cutout, no writting
- used as normal Julia array
- support negative coordinate

# Usage
```
using H5SectionsArrays
ba = H5SectionsArray("path/of/dataset/")
a = ba[101:300, -99:100, 1:3]
```

# section file format
The section format follows the convention of [ImageRegistration.jl](https://github.com/seung-lab/ImageRegistration.jl)

For details please take a look of the test script `runtests.jl`, which construct a fake dataset.
