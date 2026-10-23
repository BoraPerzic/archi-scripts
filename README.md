# archi-scripts

Small scripts for [Archi](https://www.archimatetool.com/) users, shared under the MIT licence.

## assign_diagram.ajs: link an element to another view

Select an element on a diagram, pick any view in your model from a drop-down list, and the script draws a small handle on the element that links to that view. In Archi, double-click the handle to open the view. In Archi's HTML report (Report > HTML…) the handle becomes a click-through link, so readers can move from a capability to its own diagram, and on from there.

### Requirements
- Archi (tested on 5.7.0)
- jArchi, Archi's scripting plugin (tested on 1.11.0)

jArchi is available to supporters of the Archi project. I'm one, and recommend it if you use Archi seriously.

### Install
Copy `jarchi/assign_diagram.ajs` into your jArchi scripts folder (set under Preferences > Scripting). It then appears in the Scripts Manager.

### Use
1. Open your model and a diagram.
2. Select exactly one element on that diagram.
3. Run `assign_diagram.ajs` from the Scripts Manager.
4. A dialog lists every view in the model. Type to narrow the list.
5. Pick a view and confirm.
6. A small handle appears at the bottom-right of the element, linking to that view.
7. Save the model yourself: the script never saves.

### Good to know
- One element per run. With nothing or several things selected, the script tells you and stops.
- An element can carry several handles; each new one steps to the left of the previous one. If the element is too small for another handle, nothing is placed and you're told why.
- To remove a handle, select it on the diagram and press Delete.
- Handle size and spacing are two constants at the top of the script (`ASSIGN_TILE`, `ASSIGN_INSET`).

## html-report/
Planned: small post-processing tweaks for Archi's HTML report.

## Licence
MIT. See [LICENSE](LICENSE).

---

Archi® is a registered trademark of Phillip Beauvoir. ArchiMate® is a registered trademark of The Open Group. This is a personal project, not affiliated with or endorsed by either.
