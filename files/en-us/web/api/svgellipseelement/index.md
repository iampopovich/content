---
title: SVGEllipseElement
slug: Web/API/SVGEllipseElement
page-type: web-api-interface
browser-compat: api.SVGEllipseElement
---

{{APIRef("SVG")}}

The **`SVGEllipseElement`** interface provides access to the properties of {{SVGElement("ellipse")}} elements.

{{InheritanceDiagram}}

## Instance properties

_Inherits methods from its parent interface, {{domxref("SVGGeometryElement")}}._

- {{domxref("SVGEllipseElement.cx")}} {{ReadOnlyInline}}
  - : This property returns an {{domxref("SVGAnimatedLength")}} reflecting the {{SVGAttr("cx")}} attribute of the given {{SVGElement("ellipse")}} element.
- {{domxref("SVGEllipseElement.cy")}} {{ReadOnlyInline}}
  - : This property returns an {{domxref("SVGAnimatedLength")}} reflecting the {{SVGAttr("cy")}} attribute of the given {{SVGElement("ellipse")}} element.
- {{domxref("SVGEllipseElement.rx")}} {{ReadOnlyInline}}
  - : This property returns an {{domxref("SVGAnimatedLength")}} reflecting the {{SVGAttr("rx")}} attribute of the given {{SVGElement("ellipse")}} element.
- {{domxref("SVGEllipseElement.ry")}} {{ReadOnlyInline}}
  - : This property returns an {{domxref("SVGAnimatedLength")}} reflecting the {{SVGAttr("ry")}} attribute of the given {{SVGElement("ellipse")}} element.

## Instance methods

_Inherits methods from its parent interface, {{domxref("SVGGeometryElement")}}._

## Example

### SVG

```html
<svg width="200" height="200" xmlns="http://www.w3.org/2000/svg">
  <ellipse cx="100" cy="100" rx="100" ry="60" id="ellipse" />
</svg>
```

### JavaScript

```js
const ellipse = document.getElementById("ellipse");

function outputSize() {
  // Outputs "horizontal radius: 100 vertical radius: 60"
  console.log(
    `horizontal radius: ${ellipse.rx.baseVal.valueAsString}`,
    `vertical radius: ${ellipse.ry.baseVal.valueAsString}`,
  );
}

ellipse.addEventListener("click", outputSize);
```

### Result

{{EmbedLiveSample("Example", 220, 220)}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{SVGElement("ellipse")}} SVG Element
