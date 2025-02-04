# grommet-designer

A tool to design screens using grommet components.

Live at: [designer.grommet.io](https://designer.grommet.io)

## Reference

### Command shortcuts

* **command-e** or **windows-E**: toggles preview vs. edit modes
* **ArrowUp** and **ArrowDown**: traverses the selection across siblings
* **ArrowLeft** and **ArrowRight**: traverses the selection across parent/child
* **c**: toggles collapsing the currently selected component
* **p**: initiates searching of the currently selected component's properties
* **d**: duplicate the current component, and all of its children
* **a**: opens the add component dialog
* **command-click** or **windows-click**: when adding a component, it will be added as the parent of the currently selected component
* **command-delete** or **windows-backspace**: deletes the currently selected component and all of its children
* **z**: undo the most recent change
* **Z**: redo the most recently undone change

### Linking

Button and Menu items provide a means of linking them to affect the behavior
of other components. They can either navigate to another screen or toggle
whether a Layer is visible.

Layers can be toggled manually via the `hide` control on the right
when selecting a Layer.

### Saving

Your latest design edits are saved in your browser's local storage. So,
you can refresh your window without fear of losing anything. But, if you
clear your browser's local storage, you'll lose whatever you've done.

If you change the name of a design, it will create a new design with that name.
The control in the top left let's you browse your designs, create a new one,
or import a design file you've exported.

### Sharing

The Share control near the upper left provides three methods of sharing.

1. Publish your design. This will generate a unique URL you can send
to someone. When they open that URL, they will see your work. They will not be
able to modify the published version.
1. Download the design as a JSON file. You can save or send this
however you like. You can upload one of these files using the Designs
dialog, via the Import control.
1. Generate the appropriate code for your design such that you
or a developer could run it as an actual site.

### Design Components

The following components are not part of grommet. They are components
specific to this tool that come in rather handy for what this tool does.

#### Repeater

Give this component a `count` and it will repeat it's children count times.
This is super useful when mocking up lists and tiles.

#### Reference

Allows re-using another component in the design. For instance, if every
screen has the same banner at the top, create it in the first screen and
then reference it in subsequent screens. Hint: This is easier to use if you
give the component you want to re-use a `name`.

### Images

You can create SVG images in another tool and then embed them inline in the
design as either the `src` for an Image or the `background.image` for a Box.

### Theming

You can use either one of the official themes or a theme published via theme-designer.grommet.io. Just choose "published" as the theme and then
provide the theme sharing URL.

### Data

You can add data sources to a design to make the content more consistent
and real. A data source can be JSON text or a URL to a REST endpoint that returns JSON. Once you have a data source, you can reference values in it
in Heading, Paragraph, and Text `text` properties and Image `src`
by describing the path to the content
you want inside '{}'. For example: `{data-source-name[0].property-name}`.
You can also reference data in Repeater `dataPath`, so that Repeater will
iterate over an array.

## Local development

1. `git clone`

1. `yarn install`

1. `yarn start`
