# test-build-tag
This repository shows how to fix the test build tag issue in VSCode.

## Issue

`gopls returns the error "gopls: no packages returned: packages.Load error"`

## Solution

Create a vscode/settings.json file in the repository's root directory and add the following contents:

```json
{
    "go.buildFlags": [
        "-tags=functional"
    ],
    "go.testTags": "functional",
}
```
