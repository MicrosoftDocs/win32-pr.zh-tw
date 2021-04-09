---
title: 獨立應用程式
description: 此獨立應用程式是由單一函式的呼叫所組成，它會形成分散式應用程式的基礎。
ms.assetid: 640f5d01-84c8-4fe8-9dae-f4d55cc6f06b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf1b11df2372a1db5c74659d1800b62e53b7309
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021444"
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



 

 




