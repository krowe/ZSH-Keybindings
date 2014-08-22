kshrc-k800-keybindings
======================

These are fancy *ZSH* key bindings for a Logitech K800 keyboard. It may work well on many other keyboards. It certainly won't work perfect for everyone. I think there is a way to fix that but I decided not to do it that way because it isn't as straight forward and I like to be able to easily modify these (relatively speaking).


This is not a complete `~/.zshrc` file, it contains only the key bindings. It is also intended to be edited for your own preferences. Just use what you want and skip what you don't.

This uses `Ctrl+Arrow` keys to jump through words. Because the brightness keys don't really apply here I've mapped them to search history from cursor.


## Configuration ##

You may either append this to your `~/.zshrc` file or you may `source` it from there.

To configure this you will want to setup the email account in the `_check-gmail()` function. Replace `username` with the portion of your Gmail email address which precedes the `@` symbol. 


## Limitations ##

:heavy_exclamation_mark: Currently the `scroll lock` key is not supported. The keypad will always be numerical. I prefer this myself because it always annoys me when I switch accidentally. That's also why I really needed the other buttons to work though.

:heavy_exclamation_mark: Keys F9-F12 do nothing. I'm in a [VM](http://en.wikipedia.org/wiki/Virtual_machine "VM") and there is no need for multimedia keys so I haven't remapped them at all. It would be good to have these available for those who aren't though. Or to think of other good things to do with them.

:heavy_exclamation_mark: The 3 multimedia keys and calculator button above the keypad haven't been mapped once again because I use this in a VM. In a VM this is the best way to leave them. It would be good to have these available for those who aren't though.

:interrobang: Remove the password from the `_check-gmail()` function.

:interrobang: Fix the issue where multiple call to the custom function will not return to the prompt correctly. Just press enter for now when this happens.


If you use this and make it better then send me a pull request, please. Anything that might be useful to someone else we can try to include. 
