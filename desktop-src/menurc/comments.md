---
title: " (功能表和其他資源的批註) "
description: RC 支援單行批註和封鎖批註的 C 樣式語法。 單行批註是以兩個正斜線開始 (//) 並執行至該行的結尾。 以下是資源語句的範例，後面接著單行批註。
ms.assetid: 045268fb-2d6e-446c-8b95-90e42baeb282
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fda05690df9b7e7fff6974d75d8275a2842b68
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685439"
---
# <a name="comments-menus-and-other-resources"></a><span data-ttu-id="8a357-105"> (功能表和其他資源的批註) </span><span class="sxs-lookup"><span data-stu-id="8a357-105">Comments (Menus and Other Resources)</span></span>

<span data-ttu-id="8a357-106">RC 支援單行批註和封鎖批註的 C 樣式語法。</span><span class="sxs-lookup"><span data-stu-id="8a357-106">RC supports C-style syntax for both single-line comments and block comments.</span></span> <span data-ttu-id="8a357-107">單行批註是以兩個正斜線開始 (//) 並執行至該行的結尾。</span><span class="sxs-lookup"><span data-stu-id="8a357-107">Single-line comments begin with two forward slashes (//) and run to the end of the line.</span></span> <span data-ttu-id="8a357-108">以下是資源語句的範例，後面接著單行批註。</span><span class="sxs-lookup"><span data-stu-id="8a357-108">The following is an example of a resource statement followed by a single-line comment.</span></span>

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

<span data-ttu-id="8a357-109">封鎖批註的開頭為開頭的分隔符號 (/ \*) 並執行至結尾分隔符號 (\* /) 。</span><span class="sxs-lookup"><span data-stu-id="8a357-109">Block comments begin with an opening delimiter (/\*) and run to a closing delimiter (\*/).</span></span> <span data-ttu-id="8a357-110">註解不會巢狀化。</span><span class="sxs-lookup"><span data-stu-id="8a357-110">Comments do not nest.</span></span> <span data-ttu-id="8a357-111">以下是 .rc 檔開頭的區塊批註範例。</span><span class="sxs-lookup"><span data-stu-id="8a357-111">The following is an example of a block comment at the beginning of a .rc file.</span></span>

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




