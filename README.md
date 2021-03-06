# Hierarchy Icons

See at a glance what components are attached to game objects in your scene with
this editor extension for Unity. Icons beside each item in the Hierarchy pane
make it easy to see where your cameras are, which game objects are lights, and
which objects have an audio source attached. Think of it as Gizmos for the
editor.

![Screenshot](http://matthewminer.com/images/hierarchy-icons.png)


## Usage

Add the scripts to an *Editor* folder (or a subfolder of an *Editor* folder). To
turn off individual icons, navigate to the Hierarchy Icons pane in Unity's
preferences.


## Compatibility

Requires Unity 2018.3 or later.


## Adding or Updating Icons

The icons come from an icon font, with each letter mapped to a glyph. [IcoMoon](https://icomoon.io/app) provides an easy way to create one of these. Select icons for each component, click “Generate Font”, assign a character to each glyph, then download the font and replace *HierarchyIcons.ttf*.

The mapping from component type to characters is in *IconMapping.cs*. To add a new entry, add this line to the `componentIcons` dictionary:

    { typeof(MyScript), 'x' },


## Changelog

1.0.2
- Migrates from `PreferenceItem` to `SettingsProvider` to avoid deprecation
  warning

1.0.1
- Fixes error finding the font if any other assets are named "HierarchyIcons"
  (including the parent folder itself)

1.0.0
- Initial release


## Credit

The icons used are from the excellent WebHostingHub Glyphs collection
(http://www.webhostinghub.com/glyphs/). They are licensed under the SIL Open
Font License.
