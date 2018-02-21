This is a fork of [mahkoh/scrot](https://github.com/mahkoh/scrot) which is a fork of the [scrot](http://en.wikipedia.org/wiki/Scrot) utilitiy.

I use the scrot command to create a screenshot for my i3lock. I used to blur the screenshot with ImageMagick afterwards but re-decoding, bluring and encoding it one more time took about 3 more second on my computer, which was pretty slow. That's why I added the blur option to the code.

- `-blur radius` can be used to blur the screenshot. Radius is an integer.

Below are the changes from [mahkoh](https://github.com/mahkoh):

Most of the code has been rewritten and restructured for the sake of clarity.

Two changes have been made:

- `-w` - The `-w` flag has been added. When scrot is started with this flag, it
  waits for the user to click on a window and will then take a screenshot of
  the window.
- `-s` - The `-s` flag has been modified. Clicking on a window will no longer
  take a screenshot of the window. Instead, when you press and release the left
  mouse button and then move the mouse, a rectangle will appear. Clicking and
  releasing again will take a screenshot of the marked rectangle. You can
  achieve the same by pressing the mouse button, moving the mouse, and releasing
  the mouse button. This change has been made so that the `-s` flag is easier to
  use with touchpads.
