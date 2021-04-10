---
description: 下列程式碼示範如何初始化符號處理常式。
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: 初始化符號處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a7ba79a71a389f185a5e18065af818223d4cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936101"
---
# <a name="initializing-the-symbol-handler"></a>初始化符號處理常式

下列程式碼示範如何初始化符號處理常式。 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)函式會延遲符號載入，直到要求符號資訊為止。 程式碼會針對 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)函式的 *BInvade* 參數傳遞 **TRUE** 值，以載入指定進程中每個模組的符號。  (此函式會針對進程已對應至其位址空間的每個模組，呼叫 [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) 函式。 ) 

如果指定的進程不是呼叫 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)的進程，則程式碼會傳遞處理序識別碼做為 **SymInitialize** 的第一個參數。

將 **Null** 指定為 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 的第二個參數，表示符號處理常式應該使用預設搜尋路徑來尋找符號檔。 如需有關符號處理常式如何尋找符號檔或應用程式如何指定符號搜尋路徑的詳細資訊，請參閱 [符號路徑](symbol-paths.md)。


```C++
DWORD  error;
HANDLE hProcess;

SymSetOptions(SYMOPT_UNDNAME | SYMOPT_DEFERRED_LOADS);

hProcess = GetCurrentProcess();

if (!SymInitialize(hProcess, NULL, TRUE))
{
    // SymInitialize failed
    error = GetLastError();
    printf("SymInitialize returned error : %d\n", error);
    return FALSE;
}
```



 

 



