---
title: UWP Platform Specific Differences Generator
author: hermitdave
description: Given the min and max SDK versions, the generator loads the appropriate Windows.Foundation.UniversalApiContract.winmd and builds differences in terms of new types and new members (outdated docs).
keywords: windows 10, uwp, windows community toolkit, uwp community toolkit, uwp toolkit, platform specific, platform specific differences, platform specific differences generator
dev_langs:
  - csharp
---

# Platform Specific Differences Generator

> [!WARNING]
> This docs page is outdated and the Platform Specific Analyzers have been removed. Improvements are continually being made to the Visual Studio development experience, so please ensure you are on the latest version.

A Platform Specific Analyzer would require to know the differences between various versions of UWP SDK. The Differences Generator provides a means of generating a differences dataset that can then be embedded in the analyzer.

## Usage

```cmd
DifferencesGen /min:4.0.0.0 /max:6.0.0.0
```

## Sample Output

Differences-6.0.0.0.gz

Differences-5.0.0.0.gz

## Data format

All types are fully qualified

### Namespace.Type

`Windows.Management.Update.PreviewBuildsState`

`Windows.Management.Update.PreviewBuildsManager`

A new type does not have additional methods and properties listed.

For a type that has additions, the additions are listed alongside

### Namespace.Type:Method#ParamCount,Property

`Windows.Networking.NetworkOperators.MobileBroadbandModem:TryGetPcoAsync#0,IsInEmergencyCallMode`

## API Source Code

- [DifferencesGen](https://github.com/windows-toolkit/WindowsCommunityToolkit/tree/rel/7.1.0/Microsoft.Toolkit.Uwp.PlatformDifferencesGen/Program.cs)

## Related Topics

<!-- Optional -->

- [Platform Specific Analyzer](./PlatformSpecificAnalyzer.md)
