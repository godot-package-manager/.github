# The Godot package manager

[NPM](https://www.npmjs.com/) allows for arbitrary
packages to be uploaded, so why not upload Godot addons there to be automatically
managed?

## Using Packages Quickstart

1. Find some [Godot packages on NPM](https://www.npmjs.com/search?q=keywords:godot-engine)
2. Add them to the `godot.package` file [(See the `godot.package` section)](#godotpackage)
3. Install your [client](#clients) of choice
4. Run your client's update function

## `godot.package`

Describes packages to be installed. This _should_ be modified
by the user.

This file can be in different markup languages:

<details open>
<summary><b>JSON</b></summary>

```jsonc
{
  // comments are supported
  "packages": {
    "my_package": "1.0.0", // as are trailing commas
  }
}
```

</details>
<details>
<summary><b>YAML</b></summary>

```yaml
packages:
  package: 1.0.0
```

</details>
<details>
<summary><b>TOML</b></summary>

```toml
[packages]
package = "1.0.0"
```

</details

---

## Clients

- ### [client](https://github.com/godot-package-manager/client#installation): Rust client
- ### [godot-plugin](https://github.com/godot-package-manager/godot-plugin#installation): Godot plugin for downloading packages in the editor (does not support yaml and toml)
