---
description: 下列程式碼示範如何使用 UnDecorateSymbolName 從符號名稱取出未修飾符號名稱。
ms.assetid: fcb0591a-dac3-45eb-b4c0-4a35c42450e5
title: 正在抓取未修飾的符號名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b0f21c884a0a58f0546ef275f2f3096abe2c50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973400"
---
# <a name="retrieving-undecorated-symbol-names"></a><span data-ttu-id="7a91b-103">正在抓取未修飾的符號名稱</span><span class="sxs-lookup"><span data-stu-id="7a91b-103">Retrieving Undecorated Symbol Names</span></span>

<span data-ttu-id="7a91b-104">下列程式碼示範如何使用 [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)從符號名稱取出未修飾符號名稱。</span><span class="sxs-lookup"><span data-stu-id="7a91b-104">The following code demonstrates how to retrieve an undecorated symbol name from a symbol name using [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname).</span></span> <span data-ttu-id="7a91b-105">裝飾名稱是儲存在中 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="7a91b-105">The decorated name is stored in `szName`.</span></span> <span data-ttu-id="7a91b-106">此範例假設您已使用 [初始化符號處理常式](initializing-the-symbol-handler.md)中的程式碼，初始化符號處理常式。</span><span class="sxs-lookup"><span data-stu-id="7a91b-106">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


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



 

 



