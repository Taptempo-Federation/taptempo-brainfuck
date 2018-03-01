TapTempo: Haskell Version


Haskell implementation of [https://github.com/moleculext/taptempo](taptempo). It started as a joke on [LinuxFR](https://linuxfr.org) where everybody implements its own TapTempo using its favorite language.

# What is it?

Run it, press the `<Enter>` key, and see the beat per minute.

# Limitations

The current localisation includes English and French, however some items are not correctly localised:

- Most content generated by [optparse-applicative](https://hackage.haskell.org/package/optparse-applicative), such as "Usage", "Available options", "Default" in help menu
- Error messages from [refined](https://hackage.haskell.org/package/refined)

# Funny programmer things

- Using `optparse-applicative` and `refined`, the command line interface cannot accept an invalid input. The `Config` type, representing runtime configuration of the application, is full of refined types.
- I had never localised an application before, and found [Text.Shakespeare.I18N](https://hackage.haskell.org/package/shakespeare-2.0.15/docs/Text-Shakespeare-I18N.html). It's doing the job really well.
- The `--version` command line flags gives a version number using `git describe`, computed at compile time using template haskell. This is overkill and fun.
