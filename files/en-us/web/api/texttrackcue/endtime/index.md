---
title: "TextTrackCue: endTime property"
short-title: endTime
slug: Web/API/TextTrackCue/endTime
page-type: web-api-instance-property
browser-compat: api.TextTrackCue.endTime
---

{{APIRef("WebVTT")}}

The **`endTime`** property of the {{domxref("TextTrackCue")}} interface returns and sets the end time of the cue.

## Value

A number representing the end time, in seconds.

## Examples

In the following example a new {{domxref("VTTCue")}} (which inherits from `TextTrackCue`) is created starting at 0.1 second and ending at 0.9 seconds. The `endTime` property is then printed to the console.

```js
let video = document.querySelector("video");
let track = video.addTextTrack("captions", "Captions", "en");
track.mode = "showing";

let cue = new VTTCue(0.1, 0.9, "Hildy!");
console.log(cue.endTime); // 0.9
track.addCue(cue);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
