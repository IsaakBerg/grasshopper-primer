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

>Note: This is the default color scheme.  You can edit it using the Document Preview Settings dialog. That dialog is accessible in Grasshopper through a button on the canvas toolbar. It also opens after invoking “Preview Settings...” on the “Display” menu.

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
Rhino geometry. This is helpful when creating more than one object with Grasshopper.



####1.1.3.5. UNITS & TOLERANCES
Grasshopper inherits units and tolerances from Rhino. To change the units,
type Document Properties in the Rhino command line to access the Document
Properties menu. Select Units to change the units and tolerances.

![IMAGE](images/1-1-3/1-1-3_006-units.png)
>Change the units and tolerances in the Rhino Document Properties menu.



####1.1.3.6. REMOTE CONTROL PANEL
Grasshopper is a plug-in for Rhino which supports a rapid, visual exploration of a design's parameter space. It offers a flexible graphic interface for making parameter adjustments. The effects of any adjustments are visible in a collection of temporary geometry results. The geometry results display nearly instantaneously during or after parameter changes. These abilities comprise a powerful tool for a designer.

Both Rhino and Grasshopper have rich interfaces which are easier to use when ample screen area is available. As a consequence, trying to suitably arrange both Rhino and Grasshopper windows can be a challenge.  The problem becomes acute when working on a small display. An elegant solution allows the user to add key Grasshopper controls to Rhino's interface.  This enables Rhino to use the entire screen, yet the user can  adjust the Grasshopper parameters when they want to.

Grasshopper's Remote Control Panel (RCP), like Rhino's own tool-bars, can hover
over Rhino or dock into it, allowing Rhino view-ports to use most of the screen.
Activating the toggle under the View menu of the Main Menu bar in Grasshopper makes the RCP visible. Initially, the RCP is blank — containing no Grasshopper parameter controls. Right-clicking on a Grasshopper control opens a context-based menu.  Invoking the “Publish To Remote Panel” menu item puts a linked copy of the control into the RCP.  Each linked copy controls the published control remotely from within Rhino. This maximizes the screen area available for seeing the updated preview results in Rhino.

Remote Control Panel item labels generate from the names of the remotely-controlled controls. As a best practice, provide controls with comprehensible, meaningful names before publishing them. Properly labeled elements will make both Grasshopper and Rhino interfaces easier to use.


![IMAGE](images/1-1-3/1-1-3_007-remote-control1.png)
> To make a parameter control (e.g. slider, toggle, button, etc.) show up in the Remote Control Panel, we publish it.

To help users understand your RCP, make sure it is well-organized. Click the
green pencil in the RCP's upper right corner to toggle the RCP into its editing
mode. Arrange its UI elements by groups and assign labels and colors to these groups. To delete unnecessary UI elements, drag them past the edge of the RCP. Afterwards, toggle the RCP back into working mode to resume normal functions.

>_The Remote Control Panel has two modes: Edit Mode (left), which allows you to
reorganize its look and feel, and Working Mode, where you can change
the values of the design parameters via the controls.

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
Creating and specifying a template file in your Grasshopper preferences is
convenient way to set up every new Grasshopper definition you create. The
template can include Grasshopper components as well as panels and sketch
objects for labeling.


![IMAGE](images/1-1-3/1-1-3_010-templates.png)
>Create a template file and save it

![IMAGE](images/1-1-3/1-1-3_011-templates2.png)
>1. In File/Preferences, load the file you just created under Template File.
Your template will serve as the starting point each time you create a new file.

