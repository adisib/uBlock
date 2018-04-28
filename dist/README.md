## INSTALL

#### Location of uBO settings

On Linux, the settings are saved in a JSON file located at `~/.mozilla/firefox/[profile name]/browser-extension-data/uBlock0@raymondhill.net/storage.js`.

When you uninstall the extension, Firefox deletes that file, so all your settings are lost when you uninstall.

### Firefox legacy

Compatible with Firefox 24 to Firefox 56.

- Download `ublock0.firefox-legacy.xpi` ([latest release desirable](https://github.com/gorhill/uBlock/releases)).
- Drag and drop the previously downloaded `ublock0.firefox-legacy.xpi` into Firefox

With Firefox 43 and beyond, you may need to toggle the setting `xpinstall.signatures.required` to `false` in `about:config`.<sup>[see "Add-on signing in Firefox"](https://support.mozilla.org/en-US/kb/add-on-signing-in-firefox)</sup>

Your uBlock Origin settings are kept intact even after you uninstall the addon.

On Linux, the settings are saved in a SQlite file located at `~/.mozilla/firefox/[profile name]/extension-data/ublock0.sqlite`.

On Windows, the settings are saved in a SQlite file located at `%APPDATA%\Mozilla\Firefox\Profiles\[profile name]\extension-data\ublock0.sqlite`.

### Build instructions (for developers)

- Clone [uBlock](https://github.com/gorhill/uBlock) and [uAssets](https://github.com/uBlockOrigin/uAssets) repositories in the same parent directory
- Set path to uBlock: `cd uBlock`
- Optional: Select the version to build: `git checkout <tag>`
- Build the plugin:
    - Firefox legacy: `./tools/make-firefox-legacy.sh all`
- Load the result of the build into your browser:
    - Firefox: drag-and-drop `/uBlock/dist/build/uBlock0.firefox-legacy.xpi` into Firefox.
   
