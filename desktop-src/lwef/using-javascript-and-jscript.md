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
# <a name="using-javascript-and-jscript"></a><span data-ttu-id="a156f-103">使用 JavaScript 和 JScript</span><span class="sxs-lookup"><span data-stu-id="a156f-103">Using JavaScript and JScript</span></span>

<span data-ttu-id="a156f-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a156f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a156f-105">如果您使用 JavaScript 或 Microsoft JScript 來存取 Microsoft 代理程式的程式設計介面，請依照此語言的慣例來指定方法或屬性：</span><span class="sxs-lookup"><span data-stu-id="a156f-105">If you use JavaScript or Microsoft JScript to access Microsoft Agent's programming interface, follow the conventions for this language for specifying methods or properties:</span></span>

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

<span data-ttu-id="a156f-106">JavaScript 目前沒有非 HTML 物件的事件語法。</span><span class="sxs-lookup"><span data-stu-id="a156f-106">JavaScript does not currently have event syntax for non-HTML objects.</span></span> <span data-ttu-id="a156f-107">不過，您可以使用 Internet Explorer 來使用 `<SCRIPT>` 標記的 **事件** 語法：</span><span class="sxs-lookup"><span data-stu-id="a156f-107">However, with Internet Explorer you can use the `<SCRIPT>` tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

<span data-ttu-id="a156f-108">由於並非所有的瀏覽器目前都支援此事件語法，您可能只想在支援 Microsoft Internet Explorer 的頁面或不需要處理事件的程式碼中使用 JavaScript。</span><span class="sxs-lookup"><span data-stu-id="a156f-108">Because not all browsers currently support this event syntax, you may want to use JavaScript only for pages that support Microsoft Internet Explorer or for code that does not require event handling.</span></span>

<span data-ttu-id="a156f-109">若要存取代理程式的物件集合，請使用 JScript [**列舉**](https://www.bing.com/search?q=**Enumerator**) 值函數。</span><span class="sxs-lookup"><span data-stu-id="a156f-109">To access Agent's object collections, use the JScript [**Enumerator**](https://www.bing.com/search?q=**Enumerator**) function.</span></span> <span data-ttu-id="a156f-110">不過，在 Internet Explorer 4.0 之前所包含的 JScript 版本不支援此函式，且不支援集合。</span><span class="sxs-lookup"><span data-stu-id="a156f-110">However, versions of JScript included prior to Internet Explorer 4.0 do not support this function and do not support collections.</span></span> <span data-ttu-id="a156f-111">若要存取 [**字元**](/windows/desktop/lwef/the-characters-object) 物件的方法和屬性，請使用 [**字元**](character-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a156f-111">To access methods and properties of the [**Character**](/windows/desktop/lwef/the-characters-object) object, use the [**Character**](character-method.md) method.</span></span> <span data-ttu-id="a156f-112">同樣地，若要存取 [**命令**](/windows/desktop/lwef/the-command-object) 物件的屬性，請使用 [**命令**](command-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a156f-112">Similarly, to access the properties of a [**Command**](/windows/desktop/lwef/the-command-object) object, use the [**Command**](command-method.md) method.</span></span>

 

 