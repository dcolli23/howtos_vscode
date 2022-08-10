---
title: Display
nav_order: 2
---

# Display
{:.no_toc}

This page contains all of the information on setting up VS Code display how I prefer it.

* TOC
{:toc}

### File Explorer

The indentation size on the file explorer is really really small on some high resolution monitors, so increasing it can help with navigation a whole lot. To do this, change the indent setting to something higher (in pixels). 25 is typically pretty good.

```json
"workbench.tree.indent": 25
```

### Line Length Rulers

When developing, I find line length easy to forget about and before I know it I have a monstrous 150 character line. To add a small vertical line in VS Code as a visual reminder, do the following:
1. Open VS Code
2. Hit <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>p</kbd> to open the command palette
3. Type "Preferences: Open User Settings (JSON)"
4. Add this JSON specification on a new line: 
    ```
    "editor.rulers": [100]
    ```
    where the value (the thing after the colon) is a list which tells VS Code where to put a vertical line. 
    
    You can also set multiple vertical lines, though I'm not a huge fan of that. I'm personally a fan of the 100 character line limit since it's not very restrictive but still allows for full side-by-side viewing of two files on most modern 24 inch monitors.

### Miscellaneous

A sort of random collection of tips and tricks.

#### Single Page Display Scaling

##### Motivation

My motivation for this is that I have multiple monitors with different resolutions. VS Code's default setting is to keep the same zoom level consistent across all monitors which I dislike.

##### Solution

![A step-by-step detailing of how to change the single page display scaling. The steps are outlined below.](single_page_display_scaling.png)

1. Go to settings in the lower right hand corner.
2. Click the settings dialog from the popup menu (or hit <kbd>Ctrl</kbd> + <kbd>,</kbd>).
3. Search for "zoom".
4. Chech the checkbox called "Editor".

Unfortunately, this only works for mouse zooming, the keyboard zooming still affects all VS Code instances. However, I can live with this solution.