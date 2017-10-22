# `exists` command
Checks if file or directory with name given as first argument exist and returns proper exit code. It can be used to run some tasks in `package.json` conditionally. For example we can make a build before running tests if `build` directory does not exist, like in the example presented below.

## Installation
```
npm install exists-command --save-dev
```

## Example usage:
**package.json:**
```
{
  "scripts": {
    "pretest": "if !(exists build); then npm run build; fi",
  },
}
```
