# Transliterate

[![Build Status](https://travis-ci.com/zdroid/Transliterate.jl.svg?branch=master)](https://travis-ci.com/zdroid/Transliterate.jl)
[![Coverage](https://codecov.io/gh/zdroid/Transliterate.jl/branch/master/graph/badge.svg)](https://codecov.io/gh/zdroid/Transliterate.jl)

Converts non-ASCII characters into ASCII using [transliteration](https://en.wikipedia.org/wiki/Transliteration).

## Install

```julia
]add Transliterate
```

## Examples

```julia
using Transliterate

transliterate("Déjà Vu!") == "Deja Vu!"
transliterate("Привет") == "Privet"
transliterate("ث س و"; languages="ar") == "th s w"
transliterate("≠ ∉"; custom_replacements=Dict("≠" => "not equal", "∉" => "not in")) == "not equal not in"
```

## Todo

- Add all rules for every language, instead of the current approach
  - This will allow proper `languages="language"` syntax
- Support more languages

Contributions are welcome.
