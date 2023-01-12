# Matplotlib Style Templates for JM

## Installation

These need to be copied into a folder in your user directory:

~/.matplotlib/stylelib

## Use
From there, they can be accessed in Python scripts thus:
```
from matplotlib.pyplot import style
style.use('coreEng')
```

Note that matplotlib styles are composable, which is to say that you can specify multiple styles and the features of 
the last in a list take precedent. The styles here are structured to take advantage of this, with the coreEng style
setting some sensible defaults (it's a slightly tweaked combination of seaborn-paper and tableau-colorblind10). The 
other styles provide alternate colour schemes, with the JM official colours and two other colour schemes sourced by
Manuele Romano. Thus 

```
style.use(['coreEng','JM'])
```

uses the settings from coreEng but with the JM corporate colours instead. Note that this also works with any of the
matplotlib inbuilt styles, listed [here](https://matplotlib.org/3.2.1/gallery/style_sheets/style_sheets_reference.html).
If you want to see how to wrangle your own style, I suggest trawling through the matplotlib source code, 
[here](https://github.com/matplotlib/matplotlib/tree/master/lib/matplotlib/mpl-data/stylelib).

The coreEng style produces charts which are the right size, shape and font for the internal report template, using
the Golden Ratio as an aspect ratio. It can be composed with the powerpoint style to generate plots which are
the right size and shape for use in presentations.

```
style.use(['coreEng','powerpoint'])
```