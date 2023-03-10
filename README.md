# The Godot Package Manager

[![discord](https://img.shields.io/discord/853476898071117865?label=chat&logo=discord&style=for-the-badge&logoColor=white)](https://discord.gg/6mcdWWBkrr "Chat on Discord")

[NPM](https://www.npmjs.com/) allows for arbitrary packages to be uploaded, so why not upload Godot addons there to be automatically managed?

## Using Packages Quickstart

1. Find some [Godot packages on NPM](https://www.npmjs.com/search?q=keywords:godot-engine)
2. Add them to the `godot.package` file [(See the `godot.package` section)](#godotpackage)
3. Install your [client](#clients) of choice
4. Run your client's update function

## Publishing Packages Quickstart

1. Download the [npm cli tool](https://github.com/npm/cli) <!-- can use the rust cli for this? --> 
2. Copy your `README.md` and `LICENSE` files into the addon folder (if you don't have these, you should create them)
3. In your addon folder, run `npm init` (e.g. given `addons/my_plugin/`, run these commands in the `my_plugin` folder)
4. Answer the prompts given by `npm`
5. Run `npm publish --access public` to publish your package. [See the npm docs for more details](https://docs.npmjs.com/creating-and-publishing-scoped-public-packages)

## `godot.package`

Describes packages to be installed. This _should_ be modified
by the user.

This file can be in different markup languages:

<details open>
<summary><b>HJSON</b></summary>

<!-- this says jsonc because highlight.js doesnt have hjson. -->
```jsonc
packages: {
  my_package: 1.0.0
}
```

</details>
<details>
<summary><b>YAML</b></summary>

```yaml
packages:
  my_package: 1.0.0
```

</details>
<details>
<summary><b>TOML</b></summary>

```toml
[packages]
my_package = "1.0.0"
```

</details>

---

## Clients

- ### [cli](https://github.com/godot-package-manager/cli#installation): Rust CLI
- ### [godot-plugin](https://github.com/godot-package-manager/godot-plugin#installation): Godot plugin for downloading packages in the editor (does not support yaml and toml, only pure json)
