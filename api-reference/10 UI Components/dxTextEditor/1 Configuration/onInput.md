---
id: dxTextEditor.Options.onInput
type: function(e)
default: null
---
---
##### shortDescription
A function that is executed each time the UI component's input is changed while the UI component is focused.

##### param(e): Object
Information about the event.

##### field(e.component): {WidgetName}
The UI component's instance.

##### field(e.element): dxElement
#include common-ref-elementparam with { element: "UI component" }

##### field(e.event): event
#include common-ref-eventparam

##### field(e.model): Object
Model data. Available only if Knockout is used.

---