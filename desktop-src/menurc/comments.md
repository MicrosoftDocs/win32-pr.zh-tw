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
# <a name="comments-menus-and-other-resources"></a> (功能表和其他資源的批註) 

RC 支援單行批註和封鎖批註的 C 樣式語法。 單行批註是以兩個正斜線開始 (//) 並執行至該行的結尾。 以下是資源語句的範例，後面接著單行批註。

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

封鎖批註的開頭為開頭的分隔符號 (/ \*) 並執行至結尾分隔符號 (\* /) 。 註解不會巢狀化。 以下是 .rc 檔開頭的區塊批註範例。

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




