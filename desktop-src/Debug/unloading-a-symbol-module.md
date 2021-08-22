---
description: 下列程式碼會使用 SymUnloadModule64 卸載 BaseOfDll 模組位址所參考的符號模組。
ms.assetid: f185ae64-1de9-4139-acd5-7c3a108e1eba
title: 卸載符號模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0da437fe0ce188e3559280d2bc347f3b976aba52adbf8e4a0306e4e469747435
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929278"
---
# <a name="unloading-a-symbol-module"></a>卸載符號模組

下列程式碼會使用 [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)卸載 BaseOfDll 模組位址所參考的符號模組。


```C++
if (SymUnloadModule64(hProcess, BaseOfDll))
{
    // SymUnloadModule64 returned success
}
else
{
    // SymUnloadModule64 failed
    DWORD error = GetLastError();
    printf("SymUnloadModule64 returned error : %d\n", error);
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[載入符號模組](loading-a-symbol-module.md)
</dt> </dl>

 

 



