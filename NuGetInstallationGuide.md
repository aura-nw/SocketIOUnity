# Forking notes

This repo has been forked from itisnajim/SocketIOUnity with the purpose of removing embedded .dll packages and replacing it with nuget references, due to our library conflicts.

## How to install NuGet Package Manager

NuGetForUnity is a great Nuget Package Manager to start with. Install it by following the guide in this repo: <https://github.com/GlitchEnzo/NuGetForUnity>
After installation, you will find NuGet menu in your Unity Editor

## Add NuGet references to packages.config

NuGetForUnity will automatically create packages.config; if it doesn't, you can create your own in the Assets folder using the content below.

```xml
<?xml version="1.0" encoding="utf-8"?>
<packages>
    <!-- Append this packages block to existing packages.config file -->
    <package id="Microsoft.Bcl.AsyncInterfaces" version="7.0.0" />
    <package id="Newtonsoft.Json" version="12.0.3" />
    <package id="System.Reactive" version="6.0.0" />
    <package id="System.Runtime.CompilerServices.Unsafe" version="6.0" />
    <package id="System.Text.Encodings.Web" version="6.0" />
    <package id="System.Text.Json" version="6.0" />
</packages>
```

## Restore NuGet packages

Head to NuGet -> Restore Packages to restore referenced packages above.

