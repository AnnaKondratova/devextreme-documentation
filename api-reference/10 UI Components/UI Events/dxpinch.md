---
id: UI Events.dxpinch
module: events/transform
type: eventType
---
---
##### shortDescription
Raised when the pinch gesture has been performed.

##### param(event): event
#include common-ref-eventparam The following fields are added to existing fields of this argument object.

##### field(event.cancel): boolean
Allows you to cancel the gesture processing.

##### field(event.deltaScale): number
The ratio between the current and previous scales.

##### field(event.scale): number
The ratio between the current and initial scales.

---
#####See Also#####
- [UI Events - Introduction](/api-reference/10%20UI%20Widgets/UI%20Events '/Documentation/ApiReference/UI_Components/UI_Events/')