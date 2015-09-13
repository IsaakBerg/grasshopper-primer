###1.1.3. TALKING TO RHINO

Unlike a Rhino document, a Grasshopper definition does not contain any actual
objects or geometry. Instead, a Grasshopper definition represents a set of
rules and instructions for how Rhino can automate tasks.

![IMAGE](images/1-1-3/1-1-3_001-talking-to-rhino.png)
>1. Grasshopper preview geometry.
2. Rhino view-ports.
3. Grasshopper Application window.




####1.1.3.1. VIEW-PORT FEEDBACK
All geometry generated using the Grasshopper components shows up in the Rhino view-port by default. This preview is just an Open GL approximation of the actual geometry. You will not be able to select the geometry in the Rhino view-port until you have “baked” it into the scene. You can turn the geometry preview on/off by right-clicking on a component and selecting the Preview toggle. The geometry in the view-port is color-coded to provide visual feedback. The image below outlines the default color scheme.

>Note: This is the default color scheme.  One can change color schemes using the Document Preview Settings tool on the canvas toolbar within Grasshopper.

![IMAGE](images/1-1-3/1-1-3_002-viewport-feedback.png)
>1. Green geometry in the view-port belongs to a component in the current selection.
2. Red geometry in the view-port belongs to a component not in the current selection.
3. Points drawn as crosses belong to preview geometry rather than Rhino geometry. In contrast, geometric-points in Rhino appear as rectangles.
4. Blue feedback delineates a selection underway in the Rhino view-port.

####1.1.3.2. LIVE WIRES
Grasshopper is a dynamic environment. Changes made to input parameters are live and their preview displays update in the Rhino view-port as soon as possible.

![IMAGE](images/1-1-3/1-1-3_003-live-wires.png)

####1.1.3.3. GUMBALL WIDGET
When storing geometry as internalized in a Grasshopper parameter, the gumball
allows you to interface with that geometry in the Rhino view-port. This updater
is live and updates will occur as you manipulate the gumball. If editing Rhino geometry without the gumball, Grasshopper will not update in this live mode.

![IMAGE](images/1-1-3/1-1-3_004-gumball.png)

####1.1.3.4. BAKING GEOMETRY
To work with (e.g. select, edit, transform, etc.) Grasshopper's preview from Rhino, you must “bake” it. Baking a Grasshopper preview object treats it as a mold from which a new Rhino object is cast. Baked geometry in the Rhino document ignores further changes in your Grasshopper definition.

![IMAGE](images/1-1-3/1-1-3_005-baking.png)
>1. Bake by right-clicking a component and selecting Bake.
2. A dialog will appear that allows you to select onto which Rhino layer the
geometry will bake.
3. Grouping your baked geometry is a convenient way to manage the instantiated
Rhino geometry, particularly if you are creating many objects with Grasshopper.


####1.1.3.5. UNITS & TOLERANCES
Grasshopper inherits units and tolerances from Rhino. To change the units,
type Document Properties in the Rhino command line to access the Document
Properties menu. Select Units to change the units and tolerances.

![IMAGE](images/1-1-3/1-1-3_006-units.png)
>Change the units and tolerances in the Rhino Document Properties menu.

####1.1.3.6. REMOTE CONTROL PANEL
Grasshopper is an incredibly powerful and flexible Rhino plugin which allows
rapid exploration of design iterations using a graphic interface. However since
both Rhino and Grasshopper have their own interfaces which each require lots of
screen pixels to meaningfully use, trying to suitably arrange both Rhino and
Grasshopper windows can be a challenge, particularly when the pixels available
are a scarce resource. An elegant solution allows Rhino's interface to keep the
focus and yet lets the user adjust key Grasshopper parameters whenever needed.

Grasshopper's Remote Control Panel (RCP), like Rhino's own toolbars, can hover
over Rhino or dock into it, allowing Rhino viewports to use most of the screen.
The RCP can be instantiated by activating the toggle under the View menu of the
Main Menu bar in Grasshopper. Initially, the RCP is blank — containing no user
interface element copies of Grasshopper inputs.  Right-clicking on a UI element
in Grasshopper and invoking its Publish To Remote Panel command copies a linked
version of it into the RCP providing a more visually compact way to control it
from within Rhino. Multiple Grasshopper UI elements can be published to the RCP
so they are conveniently accessible in a way that maximizes the screen area
available for seeing the updated preview results in Rhino after each UI change.

>Note: Each linked copy of published UI elements will be labelled in the RCP
with the original UI element's name. As a best practice, provide all UI input
elements with comprehensible and meaningful names. Properly labelled elements
will make both Grasshopper and RCP interfaces easier to use.


![IMAGE](images/1-1-3/1-1-3_007-remote-control1.png)
> In order to get a UI element (eg. slider, toggle, button, etc.) to show up in
the Remote Control Panel, we have to first publish it.

To help users understand your RCP, make sure it is well-organized. Click the
green pencil in the RCP's upper right corner to toggle the RCP into its editing
mode. Arrange its UI elements by groups and assign groups labels and colors. To
delete unnecessary UI elements, simply drag them past the edge of the RCP.
Afterwards, toggle the RCP back into working mode to resume normal functions.

>_The Remote Control Panel has two modes: Edit Mode (left) which allows you to
reorganize the look and feel of the RCP, and Working Mode where you can modify
the actual values of the UI elements._
![IMAGE](images/1-1-3/1-1-3_008-remote-control2.png)
>The Remote Control Panel in Edit Mode has an orange background.




####1.1.3.7. FILE MANAGEMENT
If your Grasshopper file references geometry from Rhino, you must open that
same file for the definition to work. Keep your files organized by storing the
Grasshopper and Rhino files in the same folder, and giving them related names.

![IMAGE](images/1-1-3/1-1-3_009-file-management.png)
>1. Project Folder.
2. Rhino file.
3. Grasshopper file.

####1.1.3.8. TEMPLATES
Creating and specifiying a template file in your Grasshopper preferences is
convenient way to set up every new Grasshopper definition you create. The
template can include Grasshopper components as well as panels and sketch
objects for labeling.


![IMAGE](images/1-1-3/1-1-3_010-templates.png)
>Create a template file and save it

![IMAGE](images/1-1-3/1-1-3_011-templates2.png)
>1. In File/Preferences, load the file you just created under Template File.
Your template will now be used each time you create a new file.

