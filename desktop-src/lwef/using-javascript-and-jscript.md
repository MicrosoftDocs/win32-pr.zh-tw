---
title: 使用 JavaScript 和 JScript
description: 使用 JavaScript 和 JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fbac6d69de69daecbf21c50aafdafce81ed9d95
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092706"
---
# <a name="using-javascript-and-jscript"></a>使用 JavaScript 和 JScript

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

如果您使用 JavaScript 或 Microsoft JScript 來存取 Microsoft 代理程式的程式設計介面，請依照此語言的慣例來指定方法或屬性：

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

若要存取代理程式的物件集合，請使用 JScript [**列舉**](https://www.bing.com/search?q=**Enumerator**) 值函數。 不過，在 Internet Explorer 4.0 之前所包含的 JScript 版本不支援此函式，且不支援集合。 若要存取 [**字元**](/windows/desktop/lwef/the-characters-object) 物件的方法和屬性，請使用 [**字元**](character-method.md) 方法。 同樣地，若要存取 [**命令**](/windows/desktop/lwef/the-command-object) 物件的屬性，請使用 [**命令**](command-method.md) 方法。

 

 