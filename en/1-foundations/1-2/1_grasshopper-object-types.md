### 1.2.1. GRASSHOPPER OBJECT TYPES

#####Grasshopper consists of two primary types of user objects: parameters and components. Parameters store data, whereas components perform actions that result in data. The most basic way to understand Grasshopper is to remember that we will use data to define the inputs of actions. In turn, the actions produce new data that we can use as inputs to later actions.

####1.2.1.1. PARAMETERS
Parameters act as input valves for the flow of the data that can pass through the graph of a definition.  This data may include numbers, colors, geometry and more. Parameters look like small rectangular boxes with a single input, a single output, and an icon. We also know that these are parameters because of the shape of their icon. All parameter objects exhibit icons with a hexagonal border.

Geometry parameters can reference geometry from Rhino, or inherit geometry from other components. Each parameter can contain a collection that includes zero or more values of the corresponding type.  With data wired to its input it merely passes on that data to the output.

![IMAGE](images/1-2-1/1-2-1_001-geometry-parameters.png)
>The point and curve collections are examples of geometry parameters.

Input parameters are dynamic interface objects that allow you to interact with your definition. 

![IMAGE](images/1-2-1/1-2-1_002-input-parameters.png)
>The number slider and the graph mapper are examples of input parameters.

####1.2.1.2. COMPONENTS
Components perform actions based on the inputs they receive. There are different components for different tasks.

![IMAGE](images/1-2-1/1-2-1_003-components.png)

>1. The multiplication component is an operator that calculates the product of two numbers.
2. The Divide component operates on geometry, dividing a curve into equal
segments.
3. The Circle CNR component constructs a circle geometry from input data. It accepts data specifying a center point, a normal vector, and a radius.
4. The Loft component constructs a surface by lofting curves.

####1.2.1.3. OBJECT COLORS
We can glean some information about the state of each object based on their color. Let’s take a look at Grasshopper’s default color coding system.

The color of a object which contains neither warnings nor errors is light
gray. This color indicates that everything is working properly with the parameter or component.

The color of a parameter which contains warnings is orange. An orange-colored parameter object is not able to send data. Failing to send data would result in a warning because the parameter is not yet contributing to the solution. 
The user can resolve this problem by wiring data to its input or configuring data for it to hold in its internal storage. A parameter can either store references to existing Rhino data or new data “picked” fresh for use in Grasshopper. All freshly added parameters appear orange until they have data to send.

![IMAGE](images/1-2-1/1-2-1_004-parameter-warning.png)
>By default, orange or red objects have a small balloon appear at their upper right hand corner. If you hover your mouse over this balloon, it will reveal information about why the object is giving you a warning. When the user resolves the problem, the object's color will return to gray and the balloon will disappear.

A component is a more involved object, since we have to understand and then coordinate what its inputs and outputs are. Like orange-colored parameters, an orange-colored component indicates a warning. Warnings aren’t necessarily bad. Often, they just mean that Grasshopper is alerting you to a potential problem in your definition.

![IMAGE](images/1-2-1/1-2-1_005-component-warning.png)

A component with a slightly darker gray color indicates a disabled state of its preview display. There are two ways to disable a component’s preview display. To disable component previews one-at-a-time, right-click on the component and toggle the preview button. To disable more than one component preview at a time, select the desired components. Right-click anywhere on the canvas then toggle the icon that looks like a blind-folded man.

A component with a dull gray color is in a disabled state. Disabled components stop sending data to downstream components. To disable component previews one-at-a-time, right-click on the component and toggle the disable button. To disable more than one component at a time, select the desired components. Right-click anywhere on the canvas to select the Disable item.

A light green colored object indicates it is part of the current selection. Its geometry in the Rhino scene receives the same color for extra visual feedback.

Red components communicate one or more error conditions. The errors can either originate in the component itself or one of its inputs or outputs.
Its geometry in Rhino will not be visible until you fix the problem.

![IMAGE](images/1-2-1/1-2-1_006-object-colors.png)
>1. A parameter with no warnings or errors
2. A parameter with warnings
3. A component with warnings
4. A component with no warnings or errors
5. A component with preview disabled
6. A component in its disabled state
7. A selected component
8. A component with an error
