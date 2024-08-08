<p align="center"><img width="800px" src="https://raw.githubusercontent.com/moxer-theme/moxer-icons-code/master/assets/cover.png"></p>

<p align="center">From the Material Theme authors...<br><strong>Moxer Icons</strong> provides the biggest file icons theme for Visual Studio Code</p>
<br><br>

---

- [Getting started](#getting-started)
	- [Installation](#installation)
		- [GitHub Repository Clone](#github-repository-clone)
- [Activate theme](#activate-theme)

## Getting started

You can install *the original* awesome theme through the [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/items?itemName=Equinusocio.moxer-icons).

...but if you want to use this version, then you'll need to build it yourself

### Installation (of my version)


#### Clone and Build it yourself

first, you should have the VS Code extension tool instaled (as well as the VS Code CLI and NPM, of course):

```sh
npm install -g vsce

```

Next, we can clone the Moxer Icon Theme repository as `colin.moxer-icons` (wherever you want):

```sh
git clone https://github.com/ColinMelendez/moxer-icons-code.git colin.moxer-icons
```

Then, enter the directory, install the dependencies, and build the theme:

```sh
cd colin.moxer-icons
npm install
npm run build
```

at this point, you could hypothetically take the project directory as-is and just place it into the `.vscode/extensions` directory, but that approach is awkward, so it is best to package the extension into a .visx and formally install it. 

To generate the .visx file, you can run:

```sh
vsce package
```

and then you can install it either by utilizing the `>Extensions: install from VISX...` command in the VS Code command palette and selecting your .visx file, or by running this command in your terminal:

```sh
code --install-extension <extension_name_here>.visx
```

alternatively, the previous two commands can be handily combined:

```sh
filename=$(vsce package | grep -oE '[^ ]+\.vsix'); code --install-extension "$filename"
```

That's it! The extension should now be available to select (and should already be selected by default).

you might consider cleaning up and removing the repository if you just wanted to install the extension:

```sh
cd ..
rm -rf colin.moxer-theme
```


## Activate theme

Launch *Quick Open*:

  - <img src="https://www.kernel.org/theme/images/logos/favicon.png" width=16 height=16/> <a href="https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf">Linux</a> `Ctrl + Shift + P`
  - <img src="https://developer.apple.com/favicon.ico" width=16 height=16/> <a href="https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf">macOS</a> `⌘ + Shift + P`
  - <img src="https://www.microsoft.com/favicon.ico" width=16 height=16/> <a href="https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf">Windows</a> `Ctrl + Shift + P`

Type `theme`, choose `Preferences: File Icon Theme`, and select **Moxer Icons** from the list.

---

<p align="center"> <img src="https://equinusocio.gallerycdn.vsassets.io/extensions/equinusocio/moxer-theme/1.2.0/1562674227593/Microsoft.VisualStudio.Services.Icons.Default" width=16 height=16/> Copyright &copy; 2019 - Now. Mattia Astorino</p>

<p align="center"><a href="http://www.apache.org/licenses/LICENSE-2.0"><img src="https://img.shields.io/badge/License-Apache_2.0-5E81AC.svg?style=flat-square"/></a></p>
