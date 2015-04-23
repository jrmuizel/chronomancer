# Getting Started #

You need to be using Java 1.5 or later.

Install Eclipse 3.3 or later. Eclipse 3.2 might work, but I haven't tested it. You need to also install the CDT tools, so you might find that downloading "Eclipse IDE for C/C++ developers" is the way to go. See: http://www.eclipse.org/downloads/.

Install the GEF plugins: http://download.eclipse.org/tools/gef/downloads/.

Install the Chronomancer plugin. The easiest way is to download the [zip file](http://chronomancer.googlecode.com/files/chronomancer-0.1.zip) and unzip it in the same directory as the Eclipse binary so it drops directly into the plugins directory. If you want to hack on Chronomancer, pull from this Subversion repository instead and use the Eclipse PDE tools to build it.

Run Eclipse with Chronomancer installed.

In the Window menu, choose Show View, Other..., and select the views in the Chronomancer category. If there is no Chronomancer category, check Help/About to verify that the Chronomancer plugin is running.

Import your sources as an Eclipse project. You probably want to install the Eclipse CDT tools. Assuming you weren't already using CDT, you probably want to create a "Standard Make" project and turn off the CDT build and indexing features.

Run your program under Chronicle to get a trace to analyze: see [Chronicle instructions](http://code.google.com/p/chronicle-recorder/wiki/BuildNotes).

Create a script that runs "chronicle-query --db <your database name>". You can wrap it in ssh if you want to do remote debugging; all we require is that the script's standard input and standard output go to/from the right place.

In the Timeline view, click on the leftmost button in the toolbar to connect to the query engine. Enter your script name in the input dialog. Chronomancer and the query engine should start up, and the Timeline should fill with "start of trace" and "end of trace" events. This may take a while.

To get started debugging, choose "Search Function Calls" from the Timeline view's dropdown menu and enter a fully qualified function or method name.

Have fun!