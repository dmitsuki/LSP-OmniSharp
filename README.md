# LSP-OmniSharp

This is a helper package that automatically installs and updates
[OmniSharp](https://github.com/OmniSharp/omnisharp-roslyn) for you.

To use this package, you must have:
- The [LSP](https://packagecontrol.io/packages/LSP) package.
- The [.NET Core SDK](https://dotnet.microsoft.com/download).
- For macOS and Linux, [Mono](https://www.mono-project.com/) in order to be able to run the executable.

## Applicable Selectors

This language server operates on views with the `source.cs` base scope.

## Installation Location

The server is installed in the $DATA/Cache/LSP-OmniSharp directory, where $DATA is the base data path of Sublime Text.
For instance, $DATA is `~/.config/sublime-text` on a Linux system. If you want to force a re-installation of the server,
you can delete the entire $DATA/Cache/LSP-OmniSharp directory.

Like any helper package, installation starts when you open a view that is suitable for this language server. In this
case, that means that when you open a view with the `source.cs` base scope, installation commences.

## Configuration

Configure OmniSharp by accessing `Preferences > Package Settings > LSP > Servers > LSP-OmniSharp`.

## Quirks

OmniSharp takes a while to initialize itself because it starts compiling your project in the background. This is after
the "server" has initialized so it may look like it's doing nothing while it's compiling.

## Capabilities

OmniSharp can do a lot of cool things, like

- code completion
- signature help
- hover info
- some quality code actions
- formatting
- find references
- goto def
