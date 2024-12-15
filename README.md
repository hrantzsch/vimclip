# vimclip

vimclip is a tiny script to spawn your favorite `$EDITOR` and leave what you typed in your clipboard.
I like to think of it as a lightweight [vim-anywhere](https://github.com/cknadler/vim-anywhere).

## Installation and Usage

### Step 1: Dependencies

By default, vimclip relies on `xsel` (X11) / `wl-copy` (Wayland) on Linux and `pbcopy` on macOS to copy what you typed into the clipboard.
Make sure they are available, or make vimclip use a different command by setting `$VIMCLIP_CLIPBOARD_COMMAND`.

You should also set `$EDITOR` to your favorite editor (probably vim).

### Step 2: Integration

**Copy the script** to a folder in your `$PATH` and mark it executable.
Arch users can install `vimclip-git` from the AUR.

After that, you'll want to set a shortcut to automatically spawn a terminal and run `vimclip`.
This will depend on your desktop environment and terminal.
Some examples:

**Ubuntu with gnome-terminal**

Open `Settings > Devices > Keyboard`, scroll all the way to the bottom, and hit `+` to add a new shortcut.
Call it vimclip, set the command to `gnome-terminal -- vimclip`, and assign the shortcut you like.

**Other terminal emulators**

For **KDE's konsole** set the command to `konsole -e vimclip`.
For **kitty** simply set it to `kitty vimclip`.

**macOS iTerm**

Make an AppleScript to open an iTerm window with the command `zsh -c $HOME/bin/vimclip` (or wherever you placed vimclip).
Then make a keyboard shortcut to invoke the script.
See also https://github.com/hrantzsch/vimclip/issues/3.

**Others**

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
