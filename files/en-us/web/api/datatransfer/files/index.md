---
title: "DataTransfer: files property"
short-title: files
slug: Web/API/DataTransfer/files
page-type: web-api-instance-property
browser-compat: api.DataTransfer.files
---

{{APIRef("HTML Drag and Drop API")}}

The **`files`** read-only property of [`DataTransfer`](/en-US/docs/Web/API/DataTransfer) objects is a [list of the files](/en-US/docs/Web/API/FileList) in the drag operation. If the operation includes no files, the list is empty.

This feature can be used to drag files from a user's desktop to the browser.

> [!NOTE]
> The `files` property of [`DataTransfer`](/en-US/docs/Web/API/DataTransfer) objects can only be accessed from within the {{domxref("HTMLElement/drop_event", "drop")}} and {{domxref("Element/paste_event", "paste")}} events. For all other events, the `files` property will be empty — because its underlying data store will be in a [protected mode](https://html.spec.whatwg.org/multipage/dnd.html#the-drag-data-store).

## Value

A {{domxref("FileList","list")}} of the files in a drag operation, one list item for
each file in the operation. If the drag operation had no files, the list is empty.

## Examples

There are two live examples of this interface:

- Firefox only: <https://jsfiddle.net/9C2EF/>
- All browsers: [https://jsbin.com/hiqasek/](https://jsbin.com/hiqasek/edit?html,js,output)

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
