---
title: styles
id: styles
applicable-version: 5.0
tags: 
view: lighttable
---

Create named styles from selected images' [history stacks](../../../darkroom/pixelpipe/history-stack.md) and apply styles to selected images. 

Styles can either be created within this panel or in the [history stack](../darkroom/history-stack.md) module in the darkroom.

A list of all available styles is displayed in the module. A search field above the list allows you to locate a style by name or description. This module also allows styles to be edited and deleted.

Double-click on a style name to apply that style to all selected images.  A style may also be applied to all selected images by pressing a shortcut key assigned to it (see [preferences > shortcuts](../../../preferences-settings/shortcuts.md)) while in the lighttable or darkroom view.

Hover over the style name with your mouse to view a preview of the first selected image with that style applied.

Remove all styles by clicking on the module's reset button.

Please note that styles also include the active state of each module. You can use this to create your own default settings, which you can then activate on-demand. Simply set your desired defaults for each module, disable the module, and save the style.

A large selection of "camera" styles is provided with darktable. These styles are designed to approximate the out-of-camera JPEG look for supported camera models and can be found within this module under the "darktable camera styles" style group. You can automatically apply these styles on import using the companion Lua script [official/camera style](https://docs.darktable.org/lua/stable/lua.scripts.manual/scripts/official/apply_camera_style/).

# module controls

create duplicate
: When applying a style to images, tick this box to create a duplicate of each image before applying the chosen style to that duplicate. Disable this option to apply the chosen style directly to the selected images. Beware that in this case any existing history stack is overwritten (depending on the mode -- see below) and cannot be recovered.

mode
: As with the [history stack](./history-stack.md) module, this combobox allows you to either "append" the style to the current history stack or to "overwrite" the history stack of the target image.

create
: Create new style(s) using the history stack of the selected image(s). For each selected image a style creation window is shown. You must supply a unique name for each new style and you can also add an optional description.

: You will be provided with the option to select which history stack items you want to include in the created style. For any module, you may also choose to "reset" that module's parameters -- this will cause the module to be included in the style but with all controls set to their initial (default) state (as if you had clicked the module reset button).

: The panel supports a hierarchical view, meaning that you can create categories using the pipe symbol “|” as a separator. For example “print|tone curve +0.5 EV” will create a "print" category with a style of "tone curve +0.5 EV" below it.

edit
: Select "edit" to bring up a dialog which allows you to include or exclude specific items from the stack of an existing style. Check the “duplicate” option if you want to create a new style, instead of overwriting the existing one, in which case you will need to provide a unique name for the new style.

remove
: Delete the selected style, without any further prompt.

import
: Import a previously saved style. Styles are stored as XML files with the extension `.dtstyle`. If a style with the same name already exists, you will be asked if you wish to overwrite.

export
: Save the selected style to disk as a `.dtstyle` file. This allows styles to be published and shared with other users.
