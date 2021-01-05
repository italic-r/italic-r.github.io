---
layout: default
title: ConMan
---

# ConMan
### Download: [Source]({{ site.github.owner_url }}/ita_tools/tree/master/py/ita_ConMan) [Zip]({{ site.github.owner_url }}/ita_tools-dist/raw/master/ita_ConMan.zip)  
#### Create and manage constraints for rigging and animation.

![ConMan](/assets/img/tools/conman1.jpg)
![ConMan](/assets/img/tools/conman2.jpg)

### Install
Unzip and put the _ita_ConMan_ directory into your maya scripts directory.
The default locations are:

| System  | Location |
| :-----  | :-----   |
| Windows | C:\Users\\_**user**_\My Documents\maya\\_**version**_\prefs\scripts |
| Linux   | ~/maya/_**version**_/prefs/scripts                                  |
| Mac     | /Users/_**user**_/Library/Preferences/Autodesk/maya/_**version**_   |

### Loading and Unloading
```python
# Load
import ita_ConMan
ita_ConMan.show()
```

```python
# Unload
import ita_ConMan
ita_ConMan._CMan.close()
ita_ConMan.unregister_cb()
```

### Create Constraint
Create a constraint with custom options:
* Parent
* Point
* Orient
* Scale


### Switch targets
* "OFF" turns off all weights and blend attributes.
* "ON" turns on all weights and blend attributes.
* "SWITCH" activates the blend attribute, a single target and deactivates the rest.
* Maintain Visual Transforms: Update constraint offsets to maintain the object's world-space transforms.
* Key: Animate the switch between the current frame and immediately previous frame.

Constraint data is saved in the scene file under a fileInfo entry.
To see the raw data, issue this command in a script editor:  
`maya.cmds.fileInfo("CMan_data", q=True)`

### Remove Constraints and Data

Remove a constraint from the scene with the trash icon.

__WARNING: THIS IS NOT UNDO-ABLE!__  
Purge: Remove ALL data from the tool.


## License

(c) Jeffrey "italic" Hoover
italic.rendezvous AT gmail

Licensed under the open source
[Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0)
license. This script can be used for commercial
and non-commercial projects free of charge.

Attribution not necessary, but greatly appreciated.
Submit [bug reports]({{ site.github.owner_url }}/ita_tools/issues)
and [pull requests]({{ site.github.owner_url }}/ita_tools/pulls):

Enjoy!
