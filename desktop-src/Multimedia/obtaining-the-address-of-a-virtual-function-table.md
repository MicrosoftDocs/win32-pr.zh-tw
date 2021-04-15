---
title: 取得虛擬函式資料表的位址
description: 取得虛擬函式資料表的位址
ms.assetid: c9e9e2df-75e6-4684-a465-6905e76b10a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0d618e75d2c3a4fcc2550fca7cb90bd2a51d2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507208"
---
# <a name="obtaining-the-address-of-a-virtual-function-table"></a><span data-ttu-id="fa138-103">取得虛擬函式資料表的位址</span><span class="sxs-lookup"><span data-stu-id="fa138-103">Obtaining the Address of a Virtual Function Table</span></span>

<span data-ttu-id="fa138-104">在以 C 程式設計語言撰寫的應用程式中，您可以使用 NewBall 函數來取出 **IAVIStreamVtbl** 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="fa138-104">In an application written in the C programming language, you can retrieve the address of the **IAVIStreamVtbl** structure by using the NewBall function.</span></span> <span data-ttu-id="fa138-105">此函式會傳回結構的位址，其中包含指向 **IAVIStreamVtbl** 的指標。</span><span class="sxs-lookup"><span data-stu-id="fa138-105">This function returns the address of a structure containing a pointer to **IAVIStreamVtbl**.</span></span> <span data-ttu-id="fa138-106">**IAVIStreamVtbl** 指標後面的資訊會指定 AVIBall 在內部使用的資料。</span><span class="sxs-lookup"><span data-stu-id="fa138-106">Information following the **IAVIStreamVtbl** pointer specifies data used internally by AVIBall.</span></span> <span data-ttu-id="fa138-107">您的串流處理常式可以在 **IAVIStreamVtbl** 指標之後附加自己的資訊。</span><span class="sxs-lookup"><span data-stu-id="fa138-107">Your stream handler can append its own information after the **IAVIStreamVtbl** pointer.</span></span> <span data-ttu-id="fa138-108">這項資訊會在後續的資料流程處理常式呼叫中傳回。</span><span class="sxs-lookup"><span data-stu-id="fa138-108">This information is returned in subsequent calls to your stream handler.</span></span>


```C++
PAVISTREAM WINAPI NewBall(VOID) 
{ 
    PAVIBALL pball; 
    pball = (PAVIBALL) GlobalAllocPtr(GHND, sizeof(AVIBALL)); 
    if (!pball) 
        return 0; 
    pball->lpvtbl = &AVIBallHandler; 
    pball->lpvtbl->Create((PAVISTREAM) pball, 0, 0); 
    return (PAVISTREAM) pball; 
} 
```



 

 




