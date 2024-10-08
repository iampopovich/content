---
title: VRPose
slug: Web/API/VRPose
page-type: web-api-interface
status:
  - deprecated
  - non-standard
browser-compat: api.VRPose
---

{{APIRef("WebVR API")}}{{Deprecated_Header}}{{Non-standard_Header}}

The **`VRPose`** interface of the [WebVR API](/en-US/docs/Web/API/WebVR_API) represents the state of a VR sensor at a given timestamp (which includes orientation, position, velocity, and acceleration information).

> [!NOTE]
> This interface was part of the old [WebVR API](https://immersive-web.github.io/webvr/spec/1.1/). It has been superseded by the [WebXR Device API](https://immersive-web.github.io/webxr/).

This interface is accessible through the {{domxref("VRDisplay.getPose()")}} and {{domxref("VRDisplay.getFrameData()")}} methods. {{domxref("VRDisplay.getPose()")}} is deprecated.

## Instance properties

- {{domxref("VRPose.position")}} {{Deprecated_Inline}} {{ReadOnlyInline}} {{Non-standard_Inline}}
  - : Returns the position of the {{domxref("VRDisplay")}} at the current {{domxref("VRFrameData.timestamp")}} as a 3D vector
- {{domxref("VRPose.linearVelocity")}} {{Deprecated_Inline}} {{ReadOnlyInline}} {{Non-standard_Inline}}
  - : Returns the linear velocity of the {{domxref("VRDisplay")}} at the current {{domxref("VRFrameData.timestamp")}}, in meters per second.
- {{domxref("VRPose.linearAcceleration")}} {{Deprecated_Inline}} {{ReadOnlyInline}} {{Non-standard_Inline}}
  - : Returns the linear acceleration of the {{domxref("VRDisplay")}} at the current {{domxref("VRFrameData.timestamp")}}, in meters per second per second.
- {{domxref("VRPose.orientation")}} {{Deprecated_Inline}} {{ReadOnlyInline}} {{Non-standard_Inline}}
  - : Returns the orientation of the sensor at the current {{domxref("VRFrameData.timestamp")}}, as a quarternion value.
- {{domxref("VRPose.angularVelocity")}} {{Deprecated_Inline}} {{ReadOnlyInline}} {{Non-standard_Inline}}
  - : Returns the angular velocity of the {{domxref("VRDisplay")}} at the current {{domxref("VRFrameData.timestamp")}}, in radians per second.
- {{domxref("VRPose.angularAcceleration")}} {{Deprecated_Inline}} {{ReadOnlyInline}} {{Non-standard_Inline}}
  - : Returns the angular acceleration of the {{domxref("VRDisplay")}} at the current {{domxref("VRFrameData.timestamp")}}, in meters per second per second.

## Examples

See [`VRDisplay.getFrameData()`](/en-US/docs/Web/API/VRDisplay/getFrameData#examples) for example code.

## Specifications

This interface was part of the old [WebVR API](https://immersive-web.github.io/webvr/spec/1.1/) that has been superseded by the [WebXR Device API](https://immersive-web.github.io/webxr/). It is no longer on track to becoming a standard.

Until all browsers have implemented the new [WebXR APIs](/en-US/docs/Web/API/WebXR_Device_API/Fundamentals), it is recommended to rely on frameworks, like [A-Frame](https://aframe.io/), [Babylon.js](https://www.babylonjs.com/), or [Three.js](https://threejs.org/), or a [polyfill](https://github.com/immersive-web/webxr-polyfill), to develop WebXR applications that will work across all browsers. Read [Meta's Porting from WebVR to WebXR](https://developers.meta.com/horizon/documentation/web/port-vr-xr/) guide for more information.

## Browser compatibility

{{Compat}}

## See also

- [WebVR API](/en-US/docs/Web/API/WebVR_API)
