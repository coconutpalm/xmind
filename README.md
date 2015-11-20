# Thanks/acknowledgement

First I'd like to thank the XMind company that makes this project possible.  If you like this, consider supporting them.  I intend to rebase this work on their stream on a regular basis.  They are welcome to do the same.

**[Download XMind for Windows/Mac/Ubuntu](http://www.xmind.net/download/)**

# Project status

XMind is a high-quality fully open source brainstorming/mind-mapping Eclipse RCP application, focused on both usability and extendability. It helps people in capturing ideas into visually self-organized charts and sharing them for collaboration and communication. Currently supporting mind maps, fishbone diagrams, tree diagrams, org-charts, logic charts, and even spreadsheets. It is often used for knowledge management, meeting minutes, task management, and GTD.

This version of XMind is fully buildable as an open-source project and produces Mac/Linux/Win32 RCP application binaries.  It is currently a standalone RCP application and this application, while lacking the commercial features of commercial XMind like Microsoft Word export is quite nice and very usable as it is.

There is also a project inside the repo for building a P2 update site that you can install into your Eclipse IDE.  If you choose this route, you should be aware that the result has some annoying, though generally not show-stopping glitches, noted below under "to-do" items.  Overall, if one is willing to overlook the current glitches, in its current state XMind is already a fantastic mind mapping addition to the Eclipse IDE.

# XMind Potential

XMind has huge potential if fully integrated into the Eclipse ecosystem.

* Integration with Mylyn for task/objective tracking.
* Visualization and editing of EMF object graphs.
* Export to Mylyn WikiText for producing Eclipse documentation.
* Export to OpenOffice Writer for turning brainstorms into business reports.
* Maybe even as a data structure visualizer for the debugger.
* Integration with data tools and BIRT for business analysis and reporting.

# Personal scope

My own objective is to make XMind Eclipse-friendly and to enable others to help XMind meet its potential.

In the near-term, this means refactoring some of XMind's internals to do things the "Eclipse way".  I imagine an RCP version of XMind that is more professional-focused than consumer-focused, unlike the RCP version that the XMind company is producing.  I want XMind to be usable in a generic RCP container as well as in the Eclipse IDE; I want XMind's RCP container to do things the Eclipse way so it plays nicely with otherr Eclipse plug-ins as well as other RCP tooling.

# Initial work

* There are now two Window menus; XMind RCP replaces Eclipse's Window menu with its own.
* There is a *File/New...* choice that does nothing when chosen.  However *File/Empty mindmap* works.
* XMind adds several other top-level menu bar choices that are only relevent when editing mind maps.
* XMind's cool bar appears *after* the perspective switcher but you can drag it to a more appropriate location.
* XMind does not use the Resources API when accessing files in the workspace, so the platform won't autmatically produce resource change deltas whenever an XMind file is saved unless you have automatic workspace refresh turned on in your preferences.
    * Also, this results in editors opened via *File/Open...* having a different identity than those double-clicked in the package explorer or resource explorer views.  If you *File/Open* a map, then double-click the same map in one of Eclipse's Resources-based views, you will get two editor windows editing the same file, but they will have different identities and not be linked to each other.  
    * Similarly, if you share a file via local network, then double-click it in the "shared files" view.  This simulates a *File/Open*, so if you then click the same file in, say, the Package View, you will open a different instance of the same file.


# Licensing

XMind is dual licensed under 2 open source licenses: the Eclipse Public License v1.0 (EPL), which is available at http://www.eclipse.org/legal/epl-v10.html , and the GNU Lesser General Public License v3 (LGPL), which is available at http://www.gnu.org/licenses/lgpl.html.

