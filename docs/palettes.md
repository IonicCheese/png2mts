# Palette Files

Syntax:
```
# This is a comment
mod:name R G B [A]

# Example
wool:red 255 0 0
air      0   0 0 0
```

The encoder will load a palette file and grab every node/color pair in the file
and then try to match all the pixels in the image to the closest node based on the palette