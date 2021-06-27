## Pop-dark-dxps

My adjustments to the official Pop-dark theme that comes with Pop!\_os linux distro.

### Actions

What I did for having this _flavor_:

1. Extracted the `gtk-dark.css` file from `gtk.gresource` file.<br/>
   `sudo gresource extract gtk.gresource /org/pop-os/themes/Pop/3.20/gtk-dark.css > gtk-dark.css`
2. Copied `gtk.gresource` file locally (instead of using a symlink)<br/>
   `cp /usr/share/themes/Pop/gtk-3.0/gtk.gresource ./gtk-3.0/`
3. Have `gtk.css` file referring to the local (and customized) `gtk-dark.css`.
4. Of course, `index.theme` has a slightly updated name to be able to select it (using Gnome Tweaks).

### Updates

The adjustements include:

- Window close button is a simple one (I don't like that bright orange, that brightness looked like it is one of the most important elements).
- Some of the radii were updated from 2px to 5px (see for example `-gtk-outline-radius: 5px;` at line 18 within `* {` CSS rule).
