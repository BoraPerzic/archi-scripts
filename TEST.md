# Manual test: assign_diagram.ajs

Tested on: Archi 5.7.0, jArchi 1.11.0 (Windows).
Use a **plain new model** (File > New > Empty Model) with two views, View A and View B, and one element on View A at the default size. That's how a new user starts.

| # | Do | Expect | OK |
|---|---|---|---|
| 1 | On View A, select the element and run the script; pick View B | A small handle appears bottom-right inside the element. Double-clicking it opens View B. | [ ] |
| 2 | Click empty canvas (nothing selected) and run | Message "Nothing selected"; nothing changes | [ ] |
| 3 | Select two elements and run | Message "Select exactly one element"; nothing changes | [ ] |
| 4 | Run again on the same element; pick View A | A second handle appears to the LEFT of the first, not on top of it | [ ] |
| 5 | Run, then cancel the dialog | Console says "Cancelled -- nothing placed"; nothing changes | [ ] |

Optional: Report > HTML… on the test model, open View A in the report, and click the handle. It should open View B.
