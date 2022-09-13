# gendiff

[![Node CI](https://github.com/dpetruk/frontend-project-lvl2/workflows/Node.js%20CI/badge.svg)](https://github.com/dpetruk/frontend-project-lvl2/actions)
[![Maintainability](https://api.codeclimate.com/v1/badges/7066cc753129c0f62eac/maintainability)](https://codeclimate.com/github/dpetruk/frontend-project-lvl2/maintainability)
[![Test Coverage](https://api.codeclimate.com/v1/badges/7066cc753129c0f62eac/test_coverage)](https://codeclimate.com/github/dpetruk/frontend-project-lvl2/test_coverage)

This is the [second project](https://ru.hexlet.io/programs/frontend/projects/46) from Hexlet Frontend Program.

[Demonstration of gendiff on Replit](https://replit.com/@dpetruk/gendiff)

## Difference generator:

This utility compares two files and generates their difference. Structures can be deep.

Supports `.json`, `.yaml` or `.ini` as inputs. 

Can output in:
- `stylish` - readable united structure that marks changes with `+` and `-` signs (this is default option),
- `plain` - description of properties that were added, removed or updated,
- `json` - string with json formatting.

### Examples (asciinema):
<details>
  <summary>1. compare flat json files</summary>

  [Watch this recording at asciinema](https://asciinema.org/a/353328)
  ![](/docs/asciinema_compare_json_flat.gif)

</details>

<details>
  <summary>2. compare flat yaml files</summary>

  [Watch this recording at asciinema](https://asciinema.org/a/353530)
  ![](/docs/asciinema_compare_yaml_flat.gif)

</details>

<details>
  <summary>3. compare flat ini files</summary>

  [Watch this recording at asciinema](https://asciinema.org/a/353533)
  ![](/docs/asciinema_compare_ini_flat.gif)

</details>

<details>
  <summary>4. output to stylish</summary>

  [Watch this recording at asciinema](https://asciinema.org/a/355441)
  ![](/docs/asciinema_stylish_format.gif)

</details>

<details>
  <summary>5. output to plain</summary>

  [Watch this recording at asciinema](https://asciinema.org/a/356288)
  ![](/docs/asciinema_plain_format.gif)

</details>

<details>
  <summary>6. output to json</summary>

  [Watch this recording at asciinema](https://asciinema.org/a/356629)
  ![](/docs/asciinema_json_format.gif)

</details>

##

### Installing:

1) Clone this repository to your filesystem:

```sh
git clone https://github.com/dpetruk/frontend-project-lvl2.git
```

2) Go to directory `frontend-project-lvl2` and create links:
 ```sh
 npm link
 ```

### Running as CLI-app:

```sh
gendiff <filename1> <filename2>
```

#### Options:

`-f`, `--format` - specify output format (`stylish` - default, `plain` or `json`).

`-h`, `--help` - get help.

### Using as library:

```javascript
import genDiff from 'gendiff';
```
```javascript
// outputFormat can be 'stylish', 'plain' or 'json'. Default option is 'stylish'.
const diff = genDiff(filepath1, filepath2, outputFormat);

console.log(diff);
```
