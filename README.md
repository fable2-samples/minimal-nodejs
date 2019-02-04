# Minimal F# with Fable to Node.js Starter App

This is a Fable 2.1 starter app demostrating file I/O with Nodejs's fs.readFileSync.

Checkout other sample apps at [fable2-samples](https://github.com/fable2-samples)

## Requirements

- [dotnet SDK](https://www.microsoft.com/net/download/core) 2.1 or higher
- [Paket](https://fsprojects.github.io/Paket/installation.html) to manage F# dependencies
- [node.js](https://nodejs.org) with [npm](https://www.npmjs.com/)
- An F# editor like Visual Studio, Visual Studio Code with [Ionide](http://ionide.io/) or [JetBrains Rider](https://www.jetbrains.com/rider/).

## Building and running the app

### install JS dependencies

- `npm install` to

### install F# dependencies

- Windows: `.paket/paket.exe install` or `yarn run paket`
- Non-Windows: `mono .paket/paket.exe install` or `yarn run paket:mono`

Alternatively install paket as a global .NET tool

```bash
$ dotnet tool install --tool-path ".paket" Paket --add-source https://api.nuget.org/v3/index.json --framework netcoreapp2.1
```

With defaults, try simply: `$ dotnet tool install Paket`

In this case, make sure that the install location of `paket` is in your system `PATH`, see: [dotnet-tool-install](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-tool-install)

### Start and run

- `npm start` to compile and watch with fable-splitter.

Alternatively:

- `npm run build` - same but outputs javascript to `/out`.

## Add F# Modules

While fable-splitter is watching with one of above `npm` commands:

- Add `nuget ModuleName` to paket.dependencies and run paket install command above.
- Add `ModuleName` to src/paket.references

## Source Files

- `App.fsporj` - add source paths here. Note `paket.references` is referenced here.
- `App.fs` - starting point.
- `Util/File.fs` - sample lib file.
