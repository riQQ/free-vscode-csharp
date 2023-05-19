# free-omnisharp-vscode

The debugger included in the official C# extension is [proprietary](https://aka.ms/VSCode-DotNet-DbgLicense) and is licensed to only work with Microsoft versions of vscode.
This extension replaces it with [Samsung's MIT-licensed alternative](https://github.com/Samsung/netcoredbg/blob/master/LICENSE).

## Installation

This extension is published at [open-vsx.org](https://open-vsx.org/extension/muhammad-sammy/csharp).

### Build from source

Requirements:

- [nodejs](https://nodejs.org)
- npm (comes with nodejs)

```bash
git clone https://github.com/muhammadsammy/free-omnisharp-vscode.git

cd free-omnisharp-vscode

npm install

npx gulp 'vsix:release:package'

```

then run `Extensions: Install from VSIX` from the command pallete and select the `csharp-VERSION_NUMBER.vsix` file.

# From [OmniSharp/omnisharp-vscode](https://github.com/OmniSharp/omnisharp-vscode) README

## Announcements

### The C# extension no longer ships with an included Mono & MSBuild Tools

.NET Framework builds of OmniSharp no longer ship with Mono or the MSBuild tooling (See announcement [omnisharp-roslyn#2339](https://github.com/OmniSharp/omnisharp-roslyn/issues/2339)). To ensure that the C# extension remains usable out of the box for .NET SDK projects, we have changed the default value of `omnisharp.useModernNet` to `true`.

If you still need Unity or .NET Framework support, you can set `omnisharp.useModernNet` to `false` in your VS Code settings and restart OmniSharp. Please see the [Requirements](https://github.com/OmniSharp/omnisharp-vscode#requirements) section above to ensure necessary tooling is installed.

See issue [#5120](https://github.com/OmniSharp/omnisharp-vscode/issues/5120) for more details.

## What's new in 1.25.7
* Update Razor to 7.0.0-preview.23224.3 (PR: [#5660](https://github.com/OmniSharp/omnisharp-vscode/pull/5660))
  * Fix issue with Razor diagnostics (PR: [#8622](https://github.com/dotnet/razor/pull/8622))

## What's new in 1.25.6
* Update Razor to 7.0.0-preview.23213.4 (PR: [#5655](https://github.com/OmniSharp/omnisharp-vscode/pull/5655))
  * Fix serialization issue with project.razor.json files (PR: [#8489](https://github.com/dotnet/razor/pull/8489))

## What's new in 1.25.5
* Update Razor to 7.0.0-preview.23124.2 (PR: [#5604](https://github.com/OmniSharp/omnisharp-vscode/pull/5604))
  * Fix colorization when nullable operators are present ([#5570](https://github.com/OmniSharp/omnisharp-vscode/pull/5570))
  * Add C#/HTML folding range support ([razor#8309](https://github.com/dotnet/razor/pull/8309))
  * Formatting fixes ([razor#8318](https://github.com/dotnet/razor/pull/8318))
* Update OmniSharp to 1.39.6 (PR: [#5625](https://github.com/OmniSharp/omnisharp-vscode/pull/5625))
  * Use new VS threading version to match with Razor (PR:[#2518](https://github.com/OmniSharp/omnisharp-roslyn/pull/2518))
* Update OmniSharp to 1.39.5 (PR: [#5618](https://github.com/OmniSharp/omnisharp-vscode/pull/5618))
  * Update to Roslyn `4.6.0-3.23153.5` (PR:[#2511](https://github.com/OmniSharp/omnisharp-roslyn/pull/2511))
  * Report to the client if the project being loaded is sdk style (PR:[#2502](https://github.com/OmniSharp/omnisharp-roslyn/pull/2502))
* Automatically trust ASP.NET Core HTTPS development certificate (PR: [#5589](https://github.com/OmniSharp/omnisharp-vscode/pull/5589))
* Improve outline to be less verbose (PR: [#5536](https://github.com/OmniSharp/omnisharp-vscode/pull/5536))
* Update Razor TextMate grammar (PR: [#5570](https://github.com/OmniSharp/omnisharp-vscode/pull/5570))

## What's new in 1.25.4
* Update OmniSharp to 1.39.4 (PR: [#5544](https://github.com/OmniSharp/omnisharp-vscode/pull/5544))
  * Disable snippets in sync completion (PR: [#2497](https://github.com/OmniSharp/omnisharp-roslyn/pull/2497))

## What's new in 1.25.3
* Update Razor to 7.0.0-preview.23067.5 (PR: [#5543](https://github.com/OmniSharp/omnisharp-vscode/pull/5543))
  * Enables support for arm64
  * Adds document color and color presentation features
* Update Roslyn to 4.5.0-2.22527.10 (PR: [#2486](https://github.com/OmniSharp/omnisharp-roslyn/pull/2486))
* Update dotnet-script dependencies to 1.4.0 (PR: [#2477](https://github.com/OmniSharp/omnisharp-roslyn/pull/2477))
* Register the LanguageServerLogger only once (PR: [#2473](https://github.com/OmniSharp/omnisharp-roslyn/pull/2473))
* Fix extension not finding mono. ([#5454](https://github.com/OmniSharp/omnisharp-vscode/issues/5454), PR: [#5484](https://github.com/OmniSharp/omnisharp-vscode/pull/5484))
* Update debugger to 1.25.3. ([#5460](https://github.com/OmniSharp/omnisharp-vscode/issues/5460), PR: [#5489](https://github.com/OmniSharp/omnisharp-vscode/pull/5489))
* Fix missing fix all commands. ([#5474](https://github.com/OmniSharp/omnisharp-vscode/issues/5474), PR: [#5475](https://github.com/OmniSharp/omnisharp-vscode/pull/5475))
* Fix failure to parse sdk version and sdk path. ([#2412](https://github.com/OmniSharp/omnisharp-vscode/issues/2412), PR: [#5459](https://github.com/OmniSharp/omnisharp-vscode/pull/5459))
* Handle custom OmniSharp launch paths. ([#5449](https://github.com/OmniSharp/omnisharp-vscode/issues/5449), PR: [#5456](https://github.com/OmniSharp/omnisharp-vscode/pull/5456))

## What's new in 1.25.2
* Fix the MSBuild version check on Unix and Linux platforms. ([#5443](https://github.com/OmniSharp/omnisharp-vscode/issues/5443), PR: [#5444](https://github.com/OmniSharp/omnisharp-vscode/pull/5444))

## What's new in 1.25.1
* When `.editorconfig` support is enabled (on by default), it is given higher priority over the legacy `omnisharp.json` code formatting options. If you would like to have the `omnisharp.json` code formatting options respected, disable `.editorconfig` support by setting `"omnisharp.enableEditorConfigSupport": false`
* Fix csharp.unitTestDebuggingOptions description ([#5309](https://github.com/OmniSharp/omnisharp-vscode/issues/5309), PR: [#5315](https://github.com/OmniSharp/omnisharp-vscode/pull/5315))
* Removed quoted examples from omnisharp.sdkVersion and omnisharp.sdkPath ([omnisharp-roslyn#2412](https://github.com/OmniSharp/omnisharp-roslyn/issues/2412), PR: [#5301](https://github.com/OmniSharp/omnisharp-vscode/pull/5301))
* Added an example on how to launch swagger ui (PR: [#5283](https://github.com/OmniSharp/omnisharp-vscode/pull/5283))
* Package manager nullability fixes (PR: [#5255](https://github.com/OmniSharp/omnisharp-vscode/pull/5255))
* Return all launch targets when `maxProjectResults` is set to 0 ([#5227](https://github.com/OmniSharp/omnisharp-vscode/issues/5227), PR: [#5241](https://github.com/OmniSharp/omnisharp-vscode/pull/5241))
* Clear nullability warnings (PR: [#5236](https://github.com/OmniSharp/omnisharp-vscode/pull/5236))
*  Provide actionable error messages for .NET SDK issues ([#5223](https://github.com/OmniSharp/omnisharp-vscode/issues/5223), PR: [#5225](https://github.com/OmniSharp/omnisharp-vscode/pull/5225))
* Clear all strict mode violations in src & enforce strict mode (PR: [#5407](https://github.com/OmniSharp/omnisharp-vscode/pull/5407))
* Update debugger to 1.25.1  (PR: [#5415](https://github.com/OmniSharp/omnisharp-vscode/pull/5415))
* Add github action to merge master to feature branches (PR: [#5414](https://github.com/OmniSharp/omnisharp-vscode/pull/5414)
* coreclr-debug nullability (PR: [#5405](https://github.com/OmniSharp/omnisharp-vscode/pull/5405))
* Feature nullability (PR: [#5400](https://github.com/OmniSharp/omnisharp-vscode/pull/5400))
* Add prerequisite check for running OmniSharp. (PR: [#5397](https://github.com/OmniSharp/omnisharp-vscode/pull/5397))
* Add projectFilesIncludePattern & projectFilesExcludePattern options. (PR: [#5382)](https://github.com/OmniSharp/omnisharp-vscode/pull/5382))
* Replaced the deprecated ProjectDiagnosticStatus event with the newer BackgroundDiagnosticStatus. (PR: [#5372](https://github.com/OmniSharp/omnisharp-vscode/pull/5372))
* Implement the "dotNetCliPaths" option to support custom .NET SDK locations (PR: [#4738](https://github.com/OmniSharp/omnisharp-vscode/pull/4738))
* Make the sourceGeneratedDocumentProvider always lazy (PR: [#5340](https://github.com/OmniSharp/omnisharp-vscode/pull/5340))
* Reintroduce typing version bumps (PR: [#5350](https://github.com/OmniSharp/omnisharp-vscode/pull/5350))
* Observer nullability fixes (PR: [#5349](https://github.com/OmniSharp/omnisharp-vscode/pull/5349))
* Support generated files in referenceProvider (PR: [#5339](https://github.com/OmniSharp/omnisharp-vscode/pull/5339))
* Provide source generated file info for workspace symbols (PR: [#5338](https://github.com/OmniSharp/omnisharp-vscode/pull/5338))
* Provide CodeActionKind for code actions (PR: [#5337](https://github.com/OmniSharp/omnisharp-vscode/pull/5337))
* Fix alpine support (PR: [#5322](https://github.com/OmniSharp/omnisharp-vscode/pull/5322))
* Update OmniSharp to 1.39.2 (PR: [#5319](<TODO>))
  * Update Roslyn to 4.4.0 1.22369.1 (PR: [omnisharp-roslyn#2420](https://github.com/OmniSharp/omnisharp-roslyn/pull/2420))
  * Simplify some code (PR: [omnisharp-roslyn#2370](https://github.com/OmniSharp/omnisharp-roslyn/pull/2370))
  * Return meaningful error when pinned SDK version is not found. ([#5128](https://github.com/OmniSharp/omnisharp-vscode/issues/5128), PR: [omnisharp-roslyn#2403](https://github.com/OmniSharp/omnisharp-roslyn/pull/2403))
  * Added support for `<WarningsAsErrors>nullable</WarningsAsErrors>` ([omnisharp-roslyn#2292](https://github.com/OmniSharp/omnisharp-roslyn/issues/2292), PR: [omnisharp-roslyn#2406](https://github.com/OmniSharp/omnisharp-roslyn/pull/2406))
  * Removed nuget versioning reference from OmniSharp.Abstractions ([omnisharp-roslyn#2410](https://github.com/OmniSharp/omnisharp-roslyn/issues/2410), PR: [omnisharp-roslyn#2414](https://github.com/OmniSharp/omnisharp-roslyn/pull/2414))
  * Bump Newtonsoft.Json to 13.0.1 (PR: [omnisharp-roslyn#2415](https://github.com/OmniSharp/omnisharp-roslyn/pull/2415))
  * Add missing LSP Handlers (PR: [omnisharp-roslyn#2463](https://github.com/OmniSharp/omnisharp-roslyn/pull/2463))
  * Add the TypeDefinitionHandler to the LSP (PR: [omnisharp-roslyn#2461](https://github.com/OmniSharp/omnisharp-roslyn/pull/2461))
  * Update .NET SDK and Roslyn (PR: [omnisharp-roslyn#2458](https://github.com/OmniSharp/omnisharp-roslyn/pull/2458))
  * Don't remap line mappings in Razor files (PR: [omnisharp-roslyn#2460](https://github.com/OmniSharp/omnisharp-roslyn/pull/2460))
  * Adds missing /open endpoint to Cake (PR: [omnisharp-roslyn#2457](https://github.com/OmniSharp/omnisharp-roslyn/pull/2457))
  * Adds V2 Highlight support to Cake (PR: [omnisharp-roslyn#2456](https://github.com/OmniSharp/omnisharp-roslyn/pull/2456))
  * Include Cake bits in .NET 6 builds (PR: [omnisharp-roslyn#2455](https://github.com/OmniSharp/omnisharp-roslyn/pull/2455))
  * Host dependency cleanup (PR: [omnisharp-roslyn#2436](https://github.com/OmniSharp/omnisharp-roslyn/pull/2436))
  * Upgrade http driver to latest ASP.NET Core version when running in .NET 6 (PR: [omnisharp-roslyn#2446](https://github.com/OmniSharp/omnisharp-roslyn/pull/2446))
  * updated IL Spy to 7.2.1.6856 (PR: [omnisharp-roslyn#2447](https://github.com/OmniSharp/omnisharp-roslyn/pull/2447))
  * Add comment to app.config explaining System.Memory versioning (PR: [omnisharp-roslyn#2444](https://github.com/OmniSharp/omnisharp-roslyn/pull/2444))
  * Add explicit System.Memory dependency to Hosts (PR: [omnisharp-roslyn#2443](https://github.com/OmniSharp/omnisharp-roslyn/pull/2443))
  * Return generated file info for find references (PR: [omnisharp-roslyn#2434](https://github.com/OmniSharp/omnisharp-roslyn/pull/2434))
  * Support NUnit TheoryAttribute (PR: [omnisharp-roslyn#2435](https://github.com/OmniSharp/omnisharp-roslyn/pull/2435))
  * Provide SourceGeneratedFileInfo for workspace symbolls requests (PR: [omnisharp-roslyn#2431](https://github.com/OmniSharp/omnisharp-roslyn/pull/2431))
  * Take the first dotnet cli we find instead of the last one we find (match the comment) (PR: [omnisharp-roslyn#2427](https://github.com/OmniSharp/omnisharp-roslyn/pull/2427)]
  * Record whether a CodeAction is a fix or not (PR: [omnisharp-roslyn#2430](https://github.com/OmniSharp/omnisharp-roslyn/pull/2430))
  * Update VMs used in build CI. (PR: [omnisharp-roslyn#2425](https://github.com/OmniSharp/omnisharp-roslyn/pull/2425))
  * Only get first document's highlights (PR: [omnisharp-roslyn#2424](https://github.com/OmniSharp/omnisharp-roslyn/pull/2424))

### Emmet support in Razor files

To enable emmet support, add the following to your settings.json:

```json
"emmet.includeLanguages": {
    "aspnetcorerazor": "html"
}
```

### Semantic Highlighting

The C# semantic highlighting support is in preview. To enable, set `editor.semanticHighlighting.enabled` and `csharp.semanticHighlighting.enabled` to `true` in your settings. Semantic highlighting is only provided for code files that are part of the active project.

To really see the difference, try the new Visual Studio 2019 Light and Dark themes with semantic colors that closely match Visual Studio 2019.

### Development

First install:

- Node.js (8.11.1 or later)
- Npm (5.6.0 or later)

To **run and develop** do the following:

* Run `npm ci`
* Run `npm run compile`
* Open in Visual Studio Code (`code .`)
* _Optional:_ run `npm run watch`, make code changes
* Press <kbd>F5</kbd> to debug

To **test** do the following: `npm run test` or <kbd>F5</kbd> in VS Code with the "Launch Tests" debug configuration.
