# vimclip

vimclip is a tiny script to spawn your favorite `$EDITOR` and leave what you typed in your clipboard.
I like to think of it as a poor man's [vim-anywhere](https://github.com/cknadler/vim-anywhere).

## Installation and Usage

### Step 1: Dependencies

vimclip requires `xsel` to be installed (`apt install xsel`, `pacman -S xsel`, ...), and `$EDITOR` to be set to your favorite editor (probably vim).

### Step 2: Integration

First **copy the script** to your `$HOME/bin` folder.
Remember to mark it executable and try it out by running `vimclip` in a terminal.

Next you'll want to set a shortcut to automatically spawn a terminal and run `vimclip`.
This will depend on your desktop environment and terminal of course:

**Ubuntu with gnome-terminal**

Open `Settings > Devices > Keyboard`, scroll all the way to the bottom, and hit `+` to add a new shortcut.
Call it vimclip, set the command to `gnome-terminal -- vimclip`, and assign the shortcut you like.

**Other terminal emulators**

For **KDE's konsole** set the command to `konsole -e vimclip`. For **kitty**  simply set it to `kitty vimclip`.

If you run another desktop environment with another terminal emulator I'm sure you'll be able to figure it out as well.
Don't hesitate to open an issue if not.

### Step 3: Profit

:money_with_wings: :money_with_wings: :money_with_wings:

## Help

### Damn I Lost the Clipboard Content

Don't worry, you won't have to type it all again.
vimclip stores your input in a temporary file at `/tmp/vimclip.XXXXXXXX` (where XXX... is replaced by a random string).
So if you accidentally copied something else into your clipboard before pasting your vimclip input, just go and grab the content from there.

### I Want to Use Another Editor

I called it vimclip, but if your `$EDITOR` is emacs, nano, or any other, it should work as well.
