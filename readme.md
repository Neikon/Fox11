# Fox11

A Firefox CSS themes with auto-color, Mica, auto-hide nav-bar support. Inspired in [firefox-one](https://github.com/Godiesc/firefox-one) , Edge/Chrome restyle 2023.

![1690216277849](image/readme/1690216277849.png)

![1690216288679](image/readme/1690216288679.png)

![1690216292119](image/readme/1690216292119.png)

## How to install

* [Download theme/Repo ](https://github.com/Neikon/Fox11/archive/refs/heads/main.zip)or download from [Github Releases](https://github.com/Neikon/Fox11/releases)
* Open a new tab in firefox and write in url bar `about:support` you should see a list with your firefox data, You only need **"Profile folder"**, you can now click in "Open folder" button o copy the address to your profile folder.
  the address should be similar to following example depend of your system:

  * Linux - `$HOME/.mozilla/firefox/XXXXXXX.default-XXXXXX/`
  * Windows 10 - `C:\Users\<USERNAME>\AppData\Roaming\Mozilla\Firefox\Profiles\XXX.default-XXX`
  * macOS - `Users/<USERNAME>/Library/Application Support/Firefox/Profiles/XXXXXXX.default-XXXXXXX`
* Go to that folder.
* if there is no folder called `chrome`. Create it.
* Extract the contents of the zip file you downloaded in the first step into the folder `chrome

  NOTE: You only need `userchrome.css` file and `components `folder

  * it should look something like this:

  ```
  chrome/
        |- userchrome.css
        |- components
  	      |- other files
  ```
* Now go to firefox open a new tab and write `about:config` in the url bar
* A dialog will warn you, but ignore it, just do it press the `I accept the risk!` button.
* Search this `toolkit.legacyUserProfileCustomizations.stylesheets` and set to  **true** .
* Restart Firefox
* That's all, after restarting you should be seeing your new topic

## How to enable Auto-color

**Uncomment** in `userchrome.css` the plugin you **use**

**comment** in `userchrome.css` the plugin you **don't** use

![1693329533229](image/readme/1693329533229.png)

### With VivaldiFox

> This is more configurable, you can set theme color text in when web is ligth or dark, but the last update is a little bit old and slower than [Adaptive Tab Bar Colour](https://addons.mozilla.org/es/firefox/addon/adaptive-tab-bar-colour/)

Download [VivaldiFox from Mozilla add-ons](https://addons.mozilla.org/es/firefox/addon/vivaldifox/)

**Uncomment** `@importurl('components/vivaldifox.css');` in `userchrome.css` 

**Comment** `@import url('components/adaptative_tab_bar_color.css');` in `userchrome.css` 

Configure Vivaldifox as the images you can find in this repository folder in [Minimal-VivaldiFox-Theme/VivaldiFox config screenshots/](https://github.com/Neikon/Minimal-VivaldiFox-Theme/tree/master/VivaldiFox%20config%20screenshots)

### With Adaptive Tab Bar Colour

> This is less configurable, you can **NOT** set theme color text in when web is ligth or dark ()It take firefox default color black/white). But it was updated in 10 de jul. de 2023 (at the moment to write this), can update theme color when you scroll down the website and is a little bit faster than [VivaldiFox](https://addons.mozilla.org/es/firefox/addon/vivaldifox/).

Download [Adaptive Tab Bar Colour](https://addons.mozilla.org/es/firefox/addon/adaptive-tab-bar-colour/)

**Comment** `@importurl('components/vivaldifox.css');` in `userchrome.css`

**Uncomment** `@import url('components/adaptative_tab_bar_color.css');` in `userchrome.css`

Configure like this:

![1691562149309](image/readme/1691562149309.png)

![1691562162205](image/readme/1691562162205.png)

## How to enable Mica (Deprecate in Firefox 117 )

![1691563418450](image/readme/1691563418450.png)

1. Download the portable or installation file from [github.com/MicaForEveryone](https://github.com/MicaForEveryone/MicaForEveryone/releases).
2. Install the extra files it asks you to install. And run the program.
3. At the bottom left corner press `Add Rule` -> `Add Process Rule`, type `firefox` -> `add`.
4. On the left panel select and open `firefox` section. Change Mica to `Acrilyc` for better blur effect.
5. Dont forget to uncomment `@importurl('components/mica_support.css');` from `userChrome.css`

## How to disable Mica

- Delete firefox rule from Micaforeveryone
- Comment `@importurl('components/mica_support.css');` from `userChrome.css`

> Test it in Win11
> Test it in Manjaro KDE(maybe need ForceBlur in kwin scripts)

> Thanks you to [Firefox-csshacks](https://mrotherguy.github.io/firefox-csshacks/?file=) for features code.
