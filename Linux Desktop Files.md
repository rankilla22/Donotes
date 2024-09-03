# creating quick and dirty .desktop files

## learning/research

I thought maybe some folks could use some help uncomplicating .desktop files so I'm gonna do a little tutorial. Here's what I think is the bare minimum for a .desktop file to work properly - the actual freedesktop standard only requries two entries in a .desktop file :)

Note: Please don't modify .desktop files in /usr/share/applications as a) that would require root and b) your changes will be overwritten the next time the app is updated. If you want to modify a .desktop file copy the file to ~/.local/share/applications and edit it there.

.desktop files in ~/.local/share/applications take precedence over .desktop files with the same name in /usr/share/applications and you can hack up the ones in your home directory all day long - worst that could happen is you'd do it wrong and have to start over but the original .desktop file is still on your system :)

Here we go -

# [Desktop Entry]

```
Type=Application

Name=alsamixergui
Exec=/usr/bin/alsamixergui
Icon=preferences-desktop

Comment=

Categories=AudioVideo;Audio;
Keywords=alsamixer;alsa;mixer;sound;volume;

NoDisplay=false
```

Okay, what we did here:

## `Type=`
 is required. Not all .desktop files are application launchers.

## `Name/Exec/Icon`
 are self-explanatory, I think. The `Name=` field is mandatory. If you want to use an icon that's not the default for your window manager you can specify the full path to the icon instead of just the name.

## `Comment=`
 Some menu systems use the comment field for text that displays on your menu, others use the Name= field. Check your menuing system to see which one yours uses so you can edit. I use jgmenu which uses the Name= field so I don't even include the comment field in my .desktop files.

## `Categories`:
 This is what determines which menu category displays the menu entry, like Accessories/Games/Graphics/Internet/Multimedia and so on.

## keywords
 are used by search tools and are not displayed by menu systems.

## NoDisplay
 is how we block an application from appearing on your menu. If I wanted alsamixergui to not display on menus I'd set NoDisplay=true

Note that all the region entries in a .desktop file are not required and can be removed. For example if you speak French you might want Comment[fr] but probably wouldn't want Comment[ru] unless you also speak Russian. The language-specific entries can be removed from a .desktop file - unless your PC is configured to speak that language, that is :)

If you really want to deep dive into the XDG desktop specification this should be helpful - https://specifications.freedesktop.org/desktop-entry-spec/latest/ar01s06.html 