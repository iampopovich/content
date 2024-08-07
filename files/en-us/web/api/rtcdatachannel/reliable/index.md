---
title: "RTCDataChannel: reliable property"
short-title: reliable
slug: Web/API/RTCDataChannel/reliable
page-type: web-api-instance-property
status:
  - deprecated
  - non-standard
browser-compat: api.RTCDataChannel.reliable
---

{{APIRef("WebRTC")}}{{Deprecated_Header}}{{Non-standard_Header}}

The read-only `RTCDataChannel` property
**`reliable`** indicates whether or not the data channel is
reliable.

> [!WARNING]
> This property is obsolete. Use {{domxref("RTCDataChannel.ordered")}} instead in any
> new code, and update existing code as soon as possible.

## Value

`true` if the {{domxref("RTCDataChannel")}}'s connection is reliable;
`false` if it isn't.

## Specifications

No longer part of any specification.

## Browser compatibility

{{Compat}}

## See also

- [WebRTC](/en-US/docs/Web/API/WebRTC_API)
- {{domxref("RTCDataChannel")}}
- {{domxref("RTCDataChannel.ordered")}}
