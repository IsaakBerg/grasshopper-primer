## Grasshopper - an Overview

#####Grasshopper is a visual programming editor developed by David Rutten at Robert McNeel & Associates.  As a Rhino plug-in, Grasshopper is a robust and versatile tool used by creative professionals the world over. Its features are invaluable in diverse fields, including architecture, art, engineering and product-design. 

In tandem, Grasshopper and Rhino offer us:
- precise parameter-based control over models,
- exploration of generative design work-flows, and
- a development platform suited for higher-level programming logic.   

All this functionality fits into two intuitive, well-integrated graphical interfaces.

The origins of Grasshopper traces back to the functionality of the “Record History” button in Rhino 4. This built-in feature enabled implicit storage of modeling procedures in the background. If you lofted four curves then edited the control points of one of them, the surface geometry would update. Back in 2008, David posed the question: “What if you could have more explicit control over this history?”. The precursor to Grasshopper, Explicit History, was born. During six years of development, a new paradigm metastasized into the Grasshopper plug-in. 
These changes have exposed the history-tree to editing in detail. This in-turn has empowered users to raise logical sequencing to a higher level.

Grasshopper became a robust editor for parametric-programming in an interactive and visual way. Externally-developed add-on suites extend its capabilities further. It has fundamentally altered the work-flows of professionals across industries. It fosters an active global community of users that inspire, help, train and learn from one another.

This primer focuses on Foundations, offering the core knowledge you need
to dive into regular use of Grasshopper and on-ramps outlining how you
might go further within your own creative practice. Before diving into the
descriptions, diagrams, and examples supplied hereafter, let's discuss what visual
programming is, the basics of the Grasshopper interface and terminology, as well
as the “live” characteristics of the view-port feedback and user experience.

Visual Programming is a paradigm of computer programming within which
the user manipulates logic elements graphically instead of textually. Some of
the most well-known textual programming languages such as C#, Visual Basic,
Processing – and even Python and Rhino-script dictate that we write code bound by language-specific syntax. In contrast, visual
programming allows us to connect functional blocks into a sequence of actions
where the “syntax” requires that the inputs of the blocks receive the data
of the appropriate type, organized according to the desired result (\*). This characteristic of visual programming avoids the barrier to entry
commonly found in trying to learn a new language, even a spoken one, as well as
foregrounds the interface, which for designers locates Grasshopper within more
familiar territory.

\**See the sections on* Data Stream Matching *and* Designing with Data Trees *for more on how to structure data.*

![IMAGE](images/python-and-gh-sine.png)
>This image show the process for drawing a sine curve in python and in Grasshopper.

To access Grasshopper and its visual programming capabilities, we need to
download and install the program from the website, [Grasshopper3D.com](http://Grasshopper3D.com/).
Once installed, we can open the plug-in by typing *Grasshopper* into the Rhino
Command Line. The first time we do so in a new session of Rhino, we see the Grasshopper loading prompt followed by the Grasshopper editor window. We can now add functional blocks called “components” to the
“canvas”, connect them with “wires”, and save the entire “definition” in the .ghx
file format.

![IMAGE](images/gh-definition.png)
>A Grasshopper definition, made up of components connected with wires on the canvas

Once we've started to develop a Grasshopper definition and created “slider”
objects within our canvas to control geometry, we may naturally intuit the
connection we've made between this input object to what we see in Rhino's
view-ports. This connection is essentially live. While we adjust the grip on the slider, we see the immediate consequences within our definition.  In other words, as soon as an input value changes, the program recomputes a solution and displays the new result. To our benefit when getting started with using Grasshopper,
the geometry preview we see is a lightweight representation of the solution
and it automatically updates. It is important to take note of this connection
because when your definitions become more complex, adeptly managing the flow of
data, the status of the “solver”, and the preview in the Rhino view-port will prevent unwanted headaches.

![IMAGE](images/flow.png)
>Program flow from left to right

####THINGS TO REMEMBER
* Grasshopper is a graphical algorithm editor that integrates with
Rhino3D's modeling tools.
* Algorithms are step by step procedures designed to perform an operation.
* You use Grasshopper to design algorithms that then automate tasks in
Rhino3D.
* An easy way to get started if you are unclear how to perform a specific
operation in Grasshopper would be to try to manually and incrementally
create an algorithm using Rhino commands.

As you begin first exploring Grasshopper or further building your skills, you have
joined the global Grasshopper community, one that is full of active members
from a wide variety of fields, with diverse experience levels. The Grasshopper website offers a forum for posing questions, sharing findings, and gaining knowledge. This is a community that we have held dear as we've written this primer and watched Grasshopper develop over the years. Welcome!

####Links
____
[Rhino3D.com](http://www.Rhino3D.com)  
[Grasshopper3D.com](http://www.Grasshopper3D.com)

