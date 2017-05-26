# aframe-cli

A command-line tool for building A-Frame scenes.

> **⚠ NOTE:️ This is not meant to be used just yet. This is a WIP!**

> _TODO: Upstream changes to [`angle`](https://github.com/aframevr/angle)._


### Usage

```sh
npm install -g aframe-cli
aframe
```

### Commands

To get a list of all commands and options:

```sh
aframe --help
```

#### `aframe new <name> [template]`

To create a new A-Frame scene in the working directory:

```sh
aframe new
```

To create a new A-Frame scene in a different directory:

```sh
aframe new my-project-directory
```

To bootstrap a new A-Frame scene from a boilerplate template:

```sh
aframe new my-project-directory --template default
```

From a GitHub repository (such as [`aframevr/aframe-default-template`](https://github.com/aframevr/aframe-default-template)):

```sh
aframe new my-project-directory --template aframevr/aframe-default-template
```

#### `aframe install <aframe-component-name> [scene-filename.html]`

Install a component from the [A-Frame Registry](https://aframe.io/registry) to an HTML file. This will detect the A-Frame version from your HTML file and install the appropriate version of the component as a `<script>` tag.

```sh
aframe install aframe-mountain-component
aframe install aframe-physics-system myaframescene-1.html
```

#### `aframe component`

[component]: https://aframe.io/docs/master/introduction/writing-a-component.html

Create a template in the working directory for an A-Frame component for publishing to the ecosystem. This command will ask several questions about your component to get things set up. See [how to write a component][component].

```sh
aframe component
```

To develop the component:

```sh
aframe component add aframe-mountain-component
```

To list all installed components for your active project:

```sh
aframe component list
```

To publish the component to the ecosystem:

```sh
npm publish
npm run ghpages
```

Then submit to the [A-Frame Registry](https://github.com/aframevr/aframe-registry).


### License

This source code, including all contributions, is provided under an [MIT License](LICENSE.md).
