ZSH Keybindings
===============

These are key bindings for *ZSH*. They were made for a Logitech K800 keyboard
on systems running Unbuntu server. It may work well with many other keyboards 
and systems but I don't have the resources to test other systems. I will make
changes as time goes on to make this work with as much as is possible. This 
certainly won't work perfect for everyone just as it is. I think there is
a way to make it work across more keyboard types but I decided not to do it
that way because it isn't as straight forward and I like to be able to easily
modify these (relatively speaking). If you'd like to see the suggested method,
then look at the [wiki page](http://zshwiki.org/home/zle/bindkeys).

This works from both the console and Putty for me on the keyboards I have so
I'm just sticking with the easy way. I wouldn't suggest putting everything
included on your servers. I use these on development machines only. It would
probably work fine but I don't like to put any bells and whistles like this 
on my public servers to ensure that they run smoothly at all times.

This is not a complete `~/.zshrc` file, it contains only the key bindings. It
is also intended to be edited for your own preferences. Just use what you want
and skip what you don't.


## Key Mappings ##
   The key modifications which this script makes are the following:


   - **Numpad** - These are mapped to the keys which they would be if the 
          <kbd>Num Lock</kbd> key was pressed.
   - **Cursor Keys** - The left and right each move a single character and the 
          up and down navigate the history. Use <kbd>Ctrl</kbd> + 
          <kbd>Left</kbd> and <kbd>Ctrl</kbd> + <kbd>Right</kbd> to jump whole
          words.
   - **Ins,Del,Home,End,PgUp,PgDn** - These work as they should. 
          <kbd>Page Up</kbd> and <kbd>Page Down</kbd> moves to the beggining
          and end of the history respectively.
   - **F1** - This clears the input buffer.
   - **F2** - This displays unread Gmail messages.
   - **F3 \ Shift+F3** - Locate \ Find
   - **F4 \ Shift+F4** - Spawns a new ZSH shell.
   - **F5 \ Shift+F5** - History search up \ History search down. Begin typing 
          and this will search the history for another command which started
          the same way.
   - **F6 \ Shift+F6** - Repeat last command with sudo this time \ su -
   - **F7 \ Shift+F7** - Displays various system information. \ Search Processes
   - **F8 \ Shift+F8** - Restart \ Shutdown the system. There is a 5 second
          countdown first which gives you time to cancel (<kbd>Ctrl</kbd>+
          <kbd>C</kbd>). Oh ya, it beeps once in order to make sure you notice
          it.
   - **F9 \ Shift+F9** - MySQL Restart\Stop
   - **F10 \ Shift+F10** - Apache 2 Restart\Stop
   - **F11** - Delete current word under the cursor.
   - **F12** - Clears the screen.
   - **Num Lock** - The runs `netstat -a`.

## Downloading ##

You only need the keymap for your keyboard. Currently, the only option available
here is the `.zshkeys-logitech-k800` file in this repository but I'll add more
if I make or get them. The `.zshcr_reference` file is not needed but may be
useful to you if you want to see the other settings I use.


## Configuration ##

You may either append this to your `~/.zshrc` file or you may `source` it from 
there. This should make the majority of the keys work for most people (even if
they are using different keyboards). Some of the keys need a little more work
to get working.

### The Email Key ###

The Email (<kbd>F2</kbd> key) script needs special attention to make work. To
configure this you will want to setup the email account in the `_check-gmail()`
function. Replace `EmailID` with the portion of your Gmail email address which
precedes the <kbd>@</kbd> symbol.

This also requires that you to enable the ATOM feed in Gmail. If you don't know 
what that is then go ahead and try this and let it fail. There will then be a 
message in your inbox. This message will have instructions on how to enable it. 

### The Restart \ Shutdown Keys ###

The Restart (<kbd>F5</kbd> key) and Shutdown (<kbd>Shift</kbd> + <kbd>F5</kbd>
key) scripts rely on *sudo*. If you do not use *sudo* then you'll want to modify
the scripts for them to work for you without it.

If you do use *sudo* then there is a small modification you'll want to make
to your *visudo* file. To do this type, `sudo visudo` at the command line.
Then add something similar to the following:

      username   ALL=(ALL) NOPASSWD: /sbin/reboot, /sbin/poweroff

Where `username` is replaced by you actual Linux user name. This will allow the
user specified to reboot the computer without a password. This must be placed
near the end of the file to work. Once you do this, you should be extra careful
about accidentally running reboot because it'll just work. It isn't a problem
for me because I usually use `shutdown -r now` myself.


## Limitations ##

:heavy_exclamation_mark: Currently the <kbd>Number Lock</kbd> key is not
supported. The keypad will always be numerical. I prefer this myself because
it always annoys me when I switch accidentally. That's also why I really
needed the other buttons to work though.

:heavy_exclamation_mark: The 3 multimedia keys and calculator button above
the keypad haven't been mapped once again because I use this in a VM. In a
VM this is the best way to leave them.

If you use this and make it better then send me a pull request, please. 
Anything that might be useful to someone else we can try to include. 
