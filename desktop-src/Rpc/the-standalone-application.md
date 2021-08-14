---
title: 獨立應用程式
description: 此獨立應用程式是由單一函式的呼叫所組成，它會形成分散式應用程式的基礎。
ms.assetid: 640f5d01-84c8-4fe8-9dae-f4d55cc6f06b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 946d76d0259fd3db971da345a10108cb3dbe11c23184b4ea9a88254e4ecb5e0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923862"
---
# <a name="the-standalone-application"></a>獨立應用程式

此獨立應用程式是由單一函式的呼叫所組成，它會形成分散式應用程式的基礎。 函式 **HelloProc** 是在自己的原始程式檔中定義，因此可以使用獨立應用程式或分散式應用程式進行編譯和連結。


```C++
/* file hellop.c */
#include <stdio.h>
#include <windows.h>

void HelloProc(char * pszString)
{
    printf("%s\n", pszString);
}
 
/* file: hello.c, a stand-alone application */
#include "hellop.c"

void main(void)
{
    char * pszString = "Hello, World";
    HelloProc(pszString);
}
```



 

 




