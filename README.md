# LSP-SourceKit

This is a helper package that automatically configures [Apple's SourceKit](https://github.com/apple/sourcekit-lsp) language server for you.

To use this package, you must have:

- The [LSP](https://packagecontrol.io/packages/LSP) package.
- swift toolchain [in case of macOS the one comes with Xcode].
- A [Swift-Next](https://github.com/Swift-Next/Swift-Next) syntax.

## Applicable Selectors

This language server operates on views with base scopes:

- `source.c` (C files)
- `source.c++` (C++ files)
- `source.objc` (Objective-C files)
- `source.objc++` (Objective-C++ files)
- `source.swift` (Swift files)

## Usage

> [!NOTE]
> The server is disabled globaly by default, you should either override its global setting to `"enabled": true,` or run in command palette `LSP: Enable language server in project` to enable it on per project basis.

SourceKit will expect either a `compile_commands.json` file at the root of your project, or a `Package.swift` file if project built around the [Swift Package Manager](https://swift.org/getting-started/#using-the-package-manager).
In case of `compile_commands.json`, this file is usually generated by CMake with the command-line option `-DCMAKE_EXPORT_COMPILE_COMMANDS=ON`.

## Installation Location

### macOS

Nothing is to install. The plugin will use the language server bundled with Xcode on macOS.

### Linux

You have to install a [swift toolchain](https://www.swift.org/install/) for your system and make it available in systems `$PATH`.

## Configuration

Configure SourceKit by running `Preferences: LSP-SourceKit` from the command palette.
