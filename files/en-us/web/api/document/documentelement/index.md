---
title: "Document: documentElement property"
short-title: documentElement
slug: Web/API/Document/documentElement
page-type: web-api-instance-property
browser-compat: api.Document.documentElement
---

{{ApiRef("DOM")}}

The **`documentElement`** read-only property of the {{domxref("Document")}} interface returns the
{{domxref("Element")}} that is the root element of the {{domxref("document")}} (for
example, the {{HTMLElement("html")}} element for HTML documents).

## Value

A {{domxref("Element")}} object.

## Examples

```js
const rootElement = document.documentElement;
const firstTier = rootElement.childNodes;
// firstTier is a NodeList of the direct children of the root element
// such as <head> and <body>

for (const child of firstTier) {
  // do something with each direct child of the root element
}
```

## Notes

For any non-empty HTML document, `documentElement` will always be an
{{HTMLElement("html")}} element. For any non-empty XML document,
`documentElement` will always be whatever element is the root element of the
document.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
