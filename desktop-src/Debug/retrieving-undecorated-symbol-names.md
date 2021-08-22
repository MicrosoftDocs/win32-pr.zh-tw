---
description: 下列程式碼示範如何使用 UnDecorateSymbolName 從符號名稱取出未修飾符號名稱。
ms.assetid: fcb0591a-dac3-45eb-b4c0-4a35c42450e5
title: 正在抓取未修飾的符號名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18a1cbdf51c64134489850343b466e49d9867fab483699a719997c3be9b5798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076342"
---
# <a name="retrieving-undecorated-symbol-names"></a>正在抓取未修飾的符號名稱

下列程式碼示範如何使用 [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)從符號名稱取出未修飾符號名稱。 裝飾名稱是儲存在中 `szName` 。 此範例假設您已使用 [初始化符號處理常式](initializing-the-symbol-handler.md)中的程式碼，初始化符號處理常式。


```C++
if (UnDecorateSymbolName(szName, szUndName, sizeof(szUndName), UNDNAME_COMPLETE))
{
    // UnDecorateSymbolName returned success
    printf ("Symbol : %s\n", szUndName);
}
else
{
    // UnDecorateSymbolName failed
    DWORD error = GetLastError();
    printf("UnDecorateSymbolName returned error %d\n", error);
}
```



 

 



