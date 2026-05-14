# Ask AI

## Main Objective

Do Not Make new context and Do not make the new script. Im here to mind dump my thoughts and perfect the whole logic so less errors occur. Be Fully Unbiased, Logical, Dont Sugarcoat. Make responses smaller and easier.

## Mind Dump

Im greatfull for your assistance, This context file is has been used to make this current script. There are some stuff i wanna say that, step 2 is downloading and installing the apps. so, why it didnt auto clened the files which was downloaded on the `~/Downloads` folder? it should clean its mess. So, after installation, it will delete all the `.deb` files from the `~/Downloads` folder.

`brave --new-window google.com youtube.com facebook.com github.com instagram.com` this is an example command.

### Step 3

this command will open links from the `Fresh-Ubuntu-Install.md` which are suggested on the _Restoration Phase_. new tabs on a window but completely detatched from the terminal. first link will be the `https://pass.proton.me` then other links. then i will log into the sites.
`https://developers.cloudflare.com/warp-client/get-started/linux/` and `https://pkg.cloudflareclient.com/` these are the two pages that is needed to install and setup the warp client on my ubuntu. how and why it needs to be done by a human? cant it be done by the script itself? i see that you have done the daemon setup thing done. hats off bro.

```json
{
  "workbench.productIconTheme": "material-product-icons",
  "workbench.iconTheme": "material-icon-theme",
  "workbench.statusBar.visible": false,
  "workbench.startupEditor": "none",
  "editor.minimap.enabled": false,
  "breadcrumbs.enabled": false,
  "window.zoomLevel": 3,
  "window.customMenuBarAltFocus": false,
  "window.enableMenuBarMnemonics": false,
  "editor.fontFamily": "'GeistMono NFP', 'Droid Sans Mono', monospace",
  "workbench.colorTheme": "Catppuccin Macchiato",
  "editor.padding.top": 16,
  "editor.padding.bottom": 16,
  "terminal.integrated.smoothScrolling": true,
  "editor.cursorSmoothCaretAnimation": "on",
  "workbench.list.smoothScrolling": true,
  "editor.smoothScrolling": true,
  "editor.formatOnSave": true,
  "editor.cursorStyle": "block",
  "editor.cursorBlinking": "phase",
  "workbench.navigationControl.enabled": false,
  "workbench.openInAgents.enabled": false,
  "workbench.browser.showInTitleBar": false,
  "window.menuBarVisibility": "toggle",
  "workbench.layoutControl.enabled": false,
  "window.commandCenter": false,
  "workbench.editor.enablePreview": false,
  "workbench.sideBar.location": "right",
  "workbench.activityBar.location": "hidden"
}
```

this is the minimal setup for the vscode.

```json
{
  "workbench.colorTheme": "GitHub Dark Colorblind (Beta)", // the location of the sidebar
  "workbench.activityBar.location": "hidden", // wether sidebar will be visible or not
  "workbench.editor.showTabs": "multiple", // very bottom Status Bar which is pretty much annoying TBH
  "workbench.tips.enabled": false, // the welcome screens keyboard tips
  "workbench.startupEditor": "none", // if there is at least one tab was opened before closing the VSCode then that one will appear else nothing will appear. else, nothing will be showed but just the VSCode icon. Usually the default option were to show a welcome screen.
  "editor.minimap.enabled": false, // the icons extention which is currently used
  "material-icon-theme.hidesExplorerArrows": true, // the arrows which indicate wether the folder is open or closed. these 2 are combined together.
  "workbench.tree.enableStickyScroll": false, // by default its true and this only shows on the sidebar explorer where it gets sticky. now it wont get any sticky. it will just go normally
  "workbench.tree.renderIndentGuides": "none", // its the long line which shows how big the folder is spread. by default its usually "always" and its pretty much annoying to look at when i dont need the indentation guide.
  "workbench.tree.indent": 16, // its the indentation of the files and folders and by default its very little. i guess the default value is 8.
  "explorer.compactFolders": false, // if there is only one folder or one file under a filder then it jsut shows it as if `folder/filename.extention`. which is annoying and i just removed that.
  "git.decorations.enabled": true, // this one is for when you do a single change and git just screams with some highlights and the big filled circle and the A, U, M and other indication which is just by defautl value and i just thought why not just remove it and see how it looks
  "window.zoomLevel": 3,
  "window.titleBarStyle": "custom", // "custom" is defult and it should be the default.
  "custom-ui-style.stylesheet": {
    ".notification-toast": "box-shadow: none !important",
    ".quick-input-widget.show-file-icons": "box-shadow: none !important",
    ".quick-input-widget": "top: 25vh !important",
    ".quick-input-list .scrollbar": "display: none",
    ".monaco-action-bar.quick-input-inline-action-bar": "display: none",
    ".editor-widget.find-widget": "box-shadow: none; border-radius: 4px",
    ".monaco-scrollable-element > .shadow.top": "display: none",
    ".sidebar > div.composite.title.has-actions": "padding: 0 8px !important",
    ".sidebar": "border: none !important",
    ".monaco-list-row.focused": "outline: none !important",
    ".mocaco-editor .scroll-decoration": "display: none",
    ".title-actions": "display: none !important",
    ".monaco-scrollable-element > div.split-view-container > div > div > div.title.show-file-icons > div.label-container > div": "justify-content: center",
    ".monaco-scrollable-element > div.split-view-container > div > div > div.title": "padding-left: 40px",
    ".monaco-scrollable-element > div.split-view-container > div:nth-child(1) > div > div.pane-body > div > div > div": "padding-left: 14px"
  },
  "custom-ui-style.font.sansSerif": "Dank Mono", // this setting is responsible to change the font family of the exploreres files, folder and some other things
  // text cursor/carets styling
  "editor.cursorStyle": "block", // "line" is default. "block" is good. "underline" is not good. "DONT TRY UNDERLINE".
  "editor.cursorBlinking": "smooth", // "smooth" is good. Dont try others.
  "editor.cursorSmoothCaretAnimation": "on", // "on" is good. dont try others.
  "workbench.colorCustomizations": {
    "editorCursor.background": "#ffffff" // this is for the cursor. when the cursor is already on a letter, then the texts color will be changes accordingly.
  },
  "editor.fontFamily": "'DM Mono', 'JetBrains Mono', monospace",
  "editor.fontSize": 16,
  "editor.fontLigatures": true, // =>, -->, === && all other symbols which morphs into other looking thing.
  "editor.codeLens": false, // dont know what this is. but dont touch until you are fully sure
  "editor.lightbulb.enabled": "off", // that stupid light bulb, sometimes it shows up while coding.
  "files.trimTrailingWhitespace": true, // this is a plug and play and never need to touch it after the setup completion
  "files.insertFinalNewline": true, // plug and play and never have to touch it again in life.
  "editor.renderLineHighlight": "none", // this is a time to time changable thing, this is the line highlight feature which just took the whole fucking line to be highlighted.
  "editor.scrollbar.horizontal": "hidden", // the x axis scrollbar of the editor
  "editor.scrollbar.vertical": "hidden", // the y axis scrollbar of the editor
  "editor.overviewRulerBorder": false, // false is better, dont change. y axis scrollbar has an annoying border which looks like a stupid shadow.
  "extensions.ignoreRecommendations": false, // When set to true, this setting stops VS Code from prompting you to install recommended extensions, though the `Show Recommended Extensions` command remains available if you wish to view them manually. It does not, however, hide the Recommended section in the Extensions view sidebar;
  "editor.formatOnSave": true, // plug and play and never to touch this sacred setting
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "workbench.iconTheme": "material-icon-theme",
  "[mdx]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "tailwind-fold.autoFold": false,
  "window.menuBarVisibility": "compact",
  "workbench.editor.empty.hint": "hidden",
  "[markdown]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "editor.tokenColorCustomizations": {
    "textMateRules": [
      {
        "name": "One Dark italic",
        "scope": [
          "comment",
          "entity.other.attribute-name",
          "keyword",
          "markup.underline.link",
          "storage.modifier",
          "storage.type",
          "string.url",
          "variable.language.super",
          "variable.language.this"
        ],
        "settings": {
          "fontStyle": "italic"
        }
      },
      {
        "name": "One Dark italic reset",
        "scope": [
          "keyword.operator",
          "keyword.other.type",
          "storage.modifier.import",
          "storage.modifier.package",
          "storage.type.built-in",
          "storage.type.function.arrow",
          "storage.type.generic",
          "storage.type.java",
          "storage.type.primitive"
        ],
        "settings": {
          "fontStyle": ""
        }
      }
    ]
  },
  "[javascriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "files.autoSave": "afterDelay",
  "shellformat.effectLanguages": [
    "shellscript",
    "dockerfile",
    "dotenv",
    "hosts",
    "jvmoptions",
    "ignore",
    "gitignore",
    "properties",
    "spring-boot-properties",
    "azcli",
    "bats"
  ],
  "workbench.sideBar.location": "right",
  "workbench.statusBar.visible": false,
  "terminal.integrated.stickyScroll.enabled": false
}
```

this is the current setup of my vscode setup. i dont like to install a new extention which will dictate the look over the native stuff.

i guess that there are some useful setups on my current setup. what do you say?

Next it will do stuff about the Whole ubuntu looks customization and the terminal customization thing. `Ubuntu-Look-Customization.md`, `Ubuntu-Terminal-Customization.md`. how much of this can be automated. i know it wont be fully 100% automated but most of them right?
