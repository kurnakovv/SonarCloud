# SonarCloud for .NET
Repository that help you install the required version .NET sdk

## Setup .NET sdk version "x" for SonarCloud

``` yml
- name: Setup .NET x sdk version
  uses: actions/setup-dotnet@v1
  with:
    dotnet-version: x.x.x
```

## Real templates
- .NET 6
``` yml
- name: Setup .NET 6
  uses: actions/setup-dotnet@v1
  with:
    dotnet-version: 6.0.x
```

- .NET 5
``` yml
- name: Setup .NET 5
  uses: actions/setup-dotnet@v1
  with:
    dotnet-version: 5.0.x
```

- .NET Core 3
``` yml
- name: Setup .NET Core 3
  uses: actions/setup-dotnet@v1
  with:
    dotnet-version: 3.0.x
```

## Use it SonarCloud CI/CD
``` yml
name: SonarBuild
on:
  push:
    branches: [ main ]
  pull_request:
    types: [opened, synchronize, reopened]
jobs:
  build:
    name: Build
    runs-on: windows-latest
    steps:
      - name: Setup .NET x sdk version
        uses: actions/setup-dotnet@v1
        with:
          dotnet-version: x.x.x
    
    
# ...
```

## Real yml example
https://github.com/KurnakovMaksim/SonarCloud/blob/main/.github/workflows/build.yml

# Give a Star! ⭐
If I help you, can you give a star for me? :)
