## Downloads for Thunderbird Quantum (68+)

**[CustomCSSforTb releases & changelog](https://github.com/Aris-t2/CustomCSSforTb/releases)**  

## Want to support this project?

**[[ Paypal Me ]](https://www.paypal.me/tkpay)**  

## Instructions / Howto / Readme

- [Unlock custom CSS usage in Thunderbird 69 and newer](#unlock-custom-css-usage-in-thunderbird-69-and-newer)
- [Where to find Thundebird profile folder? The correct location for user styles.](#where-to-find-thunderbird-profile-folder-the-correct-location-for-user-styles)  
- [How to use custom user styles?](#how-to-use-custom-user-styles)  
- [How to find item ids and attributes?](#how-to-find-item-ids-and-attributes)  

## Unlock custom CSS usage in Thunderbird 69 and newer

`Settings/Options` > `Advanced` > `General` > `Config Editor...`    
`toolkit.legacyUserProfileCustomizations.stylesheets` > `true`  

## Where to find Thunderbird profile folder? The correct location for user styles.

**1.** Find your profile folder  
**Windows**  
`C:\Users\ USERNAME \AppData\Roaming\Mozilla\Thunderbird\Profiles\ PROFILE FOLDER NAME \`  
Hidden files must be visible to see `AppData` folder. Alternatively open `%APPDATA%\Mozilla\Thunderbird\Profiles\` from explorers location bar.  
**Linux**  
`/home/ username /.mozilla/thunderbird/ profile folder name /`  
Hidden files must be visible to see `.mozilla` folder.  
**Mac OS X**  
`~\Library\Mozilla\Thunderbird\Profiles\ PROFILE FOLDER NAME \` or  
`~\Library\Application Support\Mozilla\Thunderbird\Profiles\ PROFILE FOLDER NAME \`  
`\Users\ USERNAME \Library\Application\Support\Thunderbird\Profiles\`  

**2.** User styles belong into `\chrome\` folder. Create it, if there is none yet. It should look like this afterwards:  
`\ PROFILE FOLDER NAME \chrome\`  

**3.** Copy `userChrome.css`, `userContent.css` and `\config\`, `\css\`, `\images\` folders into `\chrome\` folder. It should look like this afterwards:  
`\chrome\config\`  
`\chrome\css\`  
`\chrome\image\`  
`\chrome\userChrome.css`  
`\chrome\userContent.css`  


## How to use custom user styles?

The _userChrome.css_ and _userContent.css_ files works like an options\configurations file. All main "features" can be enabled and disabled there.  
Edit _userChrome.css_ and _userContent.css_ with any text editor (**[Notepad++](https://notepad-plus-plus.org/download/)** recommended on Windows) and enable or disable any feature you like by modifying, removing or outcommenting available `@import` strings.  
Restart Thunderbird after every modification for changes to take effect.  

**Example**  
If "classic button appearance for navigation toolbar buttons" should be <u>enabled</u>, the corresponding line has to look like this:  
`@import "./css/buttons/ctb_on_main_toolbars.css"; /**/`  

If "classic button appearance for navigation toolbar buttons" should be <u>disabled</u>, the corresponding line has to look like this:  
`/* @import "./css/buttons/ctb_on_main_toolbars.css"; /**/`  

Note  
Code between `/*` and `*/` won't be used by Thunderbird unless there are other `/*` or `*/` inbetween.  

## How to find item ids and attributes?

Hit `Ctrl+Alt+Shift+I` or open 'Tools > WebDeveloper > Browser Toolbox'.  

Inspect ui or web content.  

Force popups to stay open for inspection: 
Click on 'Customize Tools and get help button' (= button with three dots) and select 'Disable popup auto-hide'.  
