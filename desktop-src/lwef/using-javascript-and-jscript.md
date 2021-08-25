---
title: 使用 JavaScript 和 JScript
description: 使用 JavaScript 和 JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3b32fd3d8e2c8ce9e337f489c27dadaa32bb379d6bc90c6083d62af52bee24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960678"
---
# <a name="using-javascript-and-jscript"></a>使用 JavaScript 和 JScript

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

如果您使用 JavaScript 或 microsoft JScript 來存取 Microsoft 代理程式的程式設計介面，請依照此語言的慣例來指定方法或屬性：

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

JavaScript 目前沒有非 HTML 物件的事件語法。 不過，您可以使用 Internet Explorer 來使用 `<SCRIPT>` 標記的 **事件** 語法：

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

由於並非所有的瀏覽器目前都支援此事件語法，您可能只想在支援 Microsoft Internet Explorer 的頁面或不需要處理事件的程式碼中使用 JavaScript。

若要存取代理程式的物件集合，請使用 JScript [**列舉**](https://www.bing.com/search?q=**Enumerator**)值函數。 不過，Internet Explorer 4.0 之前所包含的 JScript 版本不支援此函式，且不支援集合。 若要存取 [**字元**](/windows/desktop/lwef/the-characters-object) 物件的方法和屬性，請使用 [**字元**](character-method.md) 方法。 同樣地，若要存取 [**命令**](/windows/desktop/lwef/the-command-object) 物件的屬性，請使用 [**命令**](command-method.md) 方法。

 

 