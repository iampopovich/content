---
title: bookmarks.get()
slug: Mozilla/Add-ons/WebExtensions/API/bookmarks/get
page-type: webextension-api-function
browser-compat: webextensions.api.bookmarks.get
sidebar: addonsidebar
---

Given the ID of a {{WebExtAPIRef("bookmarks.BookmarkTreeNode")}} or an array of such IDs, the **`bookmarks.get()`** method retrieves the matching nodes.

This is an asynchronous function that returns a [`Promise`](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise).

## Syntax

```js-nolint
let getBookmarks = browser.bookmarks.get(
  idOrIdList                // string or string array
)
```

### Parameters

- `idOrIdList`
  - : A {{jsxref("string")}} or {{jsxref("array")}} of strings specifying the IDs of one or more {{WebExtAPIRef("bookmarks.BookmarkTreeNode", "BookmarkTreeNode")}} objects to retrieve.

### Return value

A [`Promise`](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) that will be fulfilled with an array of [`BookmarkTreeNode`](/en-US/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/BookmarkTreeNode), one for each matching node. Separators are not included in the results. If no nodes could be found, the promise will be rejected with an error message.

## Examples

This example tries to get the bookmark whose ID is `bookmarkAAAA`. If no bookmark with this ID exists, `onRejected` is called:

```js
function onFulfilled(bookmarks) {
  console.log(bookmarks);
}

function onRejected(error) {
  console.log(`An error: ${error}`);
}

let gettingBookmarks = browser.bookmarks.get("bookmarkAAAA");
gettingBookmarks.then(onFulfilled, onRejected);
```

{{WebExtExamples}}

## Browser compatibility

{{Compat}}

> [!NOTE]
> This API is based on Chromium's [`chrome.bookmarks`](https://developer.chrome.com/docs/extensions/reference/api/bookmarks#method-get) API. This documentation is derived from [`bookmarks.json`](https://chromium.googlesource.com/chromium/src/+/master/chrome/common/extensions/api/bookmarks.json) in the Chromium code.

<!--
// Copyright 2015 The Chromium Authors. All rights reserved.
//
// Redistribution and use in source and binary forms, with or without
// modification, are permitted provided that the following conditions are
// met:
//
//    * Redistributions of source code must retain the above copyright
// notice, this list of conditions and the following disclaimer.
//    * Redistributions in binary form must reproduce the above
// copyright notice, this list of conditions and the following disclaimer
// in the documentation and/or other materials provided with the
// distribution.
//    * Neither the name of Google Inc. nor the names of its
// contributors may be used to endorse or promote products derived from
// this software without specific prior written permission.
//
// THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
// "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
// LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
// A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
// OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
// SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
// LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
// DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
// THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
// (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
// OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
-->
