![Logo](docs/img/logo.png "Logo")

VS Code Extension
---

> Context Menu to make Developing for Salesforce Commerce Cloud Easier:

- [X] Quickly Search SFCC Docs for Selected Text from ISML and JS Files
- [X] Open Content Assets in Business Manager from ISML Files
- [X] Open Slots in Business Manager from ISML Files


Setup
---

> You probably already have everything else you need, though we do add a new `sitecode` property to the `dw.json` as it is required for opening Slots & Content Assets in Business Manager.

1. Make sure you install [Prophet Debugger](https://marketplace.visualstudio.com/items?itemName=SqrTT.prophet)
2. Edit the `dw.json` file in your VS Code Workspace Root Folder
3. Add a new `sitecode` property ( _Administration >  Sites >  Manage Sites_ then copy the `ID` attribute for the one you use most )

Final JSON should look something like this:

```json
{
  "hostname": "dev01-web-sandbox.demandware.net",
  "username": "developer@redvanworkshop.com",
  "password": "supersecret",
  "code-version": "version1",
  "sitecode": "myclient-us"
}
```


Usage
---

#### Searching SFCC Docs

> This works in any `.isml` of `.js` file.  Select the text you want to lookup, right click it, and select **Search SFCC Docs**.

![demo](docs/img/search-docs.gif?v=1.1.0)

#### Open in Business Manager

> This works in any `.isml` file.  Select the entire `isslot` or `iscontentasset` HTML node ( tripple click to select an entire line ), right click it, and select **Open in BM**

![demo](docs/img/open-in-bm.gif?v=1.1.0)


Developer Overview
---

> Here is how you can work on this extension on your local machine:

1. Clone this repo to your local machine `git clone https://github.com/redvanworkshop/sfcc-vscode-extension.git`
2. Open `sfcc-vscode-extension` folder in VS Code
3. Open the `extension.js` file
4. Press the `F5` key to build & launch a new instance of VS Code
5. This extension will be installed the new instance for you to play with