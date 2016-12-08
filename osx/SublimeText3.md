# Sublime Text 3 Setup on OSX

## Sync with Dropbox
cd ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/
rm -r User
ln -s ~/Dropbox/sync/SublimeText3/User



## Install Packages

Install package controller as per https://packagecontrol.io/installation

Install packages (special+shift+p)

```
All Autocomplete
Bracket​Highlighter
GitGutter (https://packagecontrol.io/packages/GitGutter)
Local History	
SideBarEnhancements
Monokai Extended (Theme)
Theme - Soda (Theme)
JsFormat
DocBlockr
SublimeLinter
```
	
Configure Preferences ( Preferences > Settings - User )
```json
{
	"bold_folder_labels": true,
	"caret_extra_bottom": 3,
	"caret_extra_top": 3,
	"caret_style": "smooth",
	"color_scheme": "Packages/Monokai Extended/Monokai Extended.tmTheme",
	"detect_indentation": false,
	"draw_minimap_border": true,
	"font_face": "Inconsolata",
	"font_size": 14,
	"highlight_line": true,
	"ignored_packages":
	[
		"Vintage",
		"Markdown"
	],
	"line_padding_bottom": 1,
	"line_padding_top": 1,
	"tab_size": 4,
	"theme": "Soda Dark 3.sublime-theme",
	"translate_tabs_to_spaces": false,
	"word_wrap": true
}
```

Configure JsFormat ( Preferences > Package Settings > JsFormat > Settings - User )
```json
{
	"end_with_newline": true,
	"space_after_anon_function": true,
	"indent_with_tabs": true,
	"keep_array_indentation": true
}
```

### Add Menu Command for Alignment

Preferences > Settings - User > Right Click on File Pane > Select 'Copy File Path'

Create a new file and paste the copied path

```
/Users/mwurzberger/Library/Application Support/Sublime Text 3/Packages/User/Preferences.sublime-settings
```

Replace "Preferences.sublime-settings" with "Main.sublime-menu"

Paste this configuration above the path
```json
[{
	"caption": "Selection",
	"mnemonic": "n",
	"id": "selection",
	"children": [
		{ "caption": "-" },
		{
			"command": "alignment",
			"caption": "Align Selection"
		}
	]
}]
```

Select the path and cut to the clipboard (cmd + x)

File > Save As > (shift + cmd + g) > (cmd + v) > Save

Restart Sublime Text 3

You should now see a new divider and the Align Selection command under the selection menu


## Setup SublimeLinter

Command line

    npm install -g jshint
    npm install -g eslint

Install packages (special+shift+p)

    SublimeLinter
    SublimeLinter-contrib-eslint