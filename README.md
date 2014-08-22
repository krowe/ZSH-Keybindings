kshrc-k800-keybindings
======================

These are fancy ZSH keybindings for a Logitech k800 keyboard.


This is not a complete .zshrc file, it contains only the keybindings. It is also intended to be edited for your own preferences. Just use what you want and skip what you don't.

This uses Ctrl+Arrow keys to jump through words. Because the brightness keys don't really apply here I've mapped them to search history from cursor.


## Configuration ##

You may either append this to your .zshrc file or you may call it from that file.

To configure this you will want to setup the email account in the _check-gmail() function. Replace username with the portion of your Gmail email address which preceeds the @ symbol. And 


## Limitations ##

- Currently the scroll lock key is not supported. The keypad will always be numerical. I prefer this myself buecause it always annoys me when I switch. That's also why I really needed the other buttons to work though.
- Keys F9-F12 do nothing. I'm in a VM and there is no need for multimedia keys so I haven't remapped them at all. It would be good to have these available for those who aren't though. Or to think of other good things to do with them.
- The 3 multimedia keys and calculator button above the keypad haven't been mapped once again because I use this in a VM. In a VM this is the best way to leave them. It would be good to have these available for those who aren't though.
- Remove the password from the _check-gmail() function.
- Fix the issue where multiple call to the custom function will not return to the prompt correctly. Just press enter for now when this happens.

