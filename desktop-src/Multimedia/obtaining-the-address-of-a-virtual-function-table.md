---
title: 取得虛擬函式資料表的位址
description: 取得虛擬函式資料表的位址
ms.assetid: c9e9e2df-75e6-4684-a465-6905e76b10a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a0fbf941114cfff2b930ed329f7a35962b9ef07158fd5fda16a19a73c0f692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038428"
---
# <a name="obtaining-the-address-of-a-virtual-function-table"></a>取得虛擬函式資料表的位址

在以 C 程式設計語言撰寫的應用程式中，您可以使用 NewBall 函數來取出 **IAVIStreamVtbl** 結構的位址。 此函式會傳回結構的位址，其中包含指向 **IAVIStreamVtbl** 的指標。 **IAVIStreamVtbl** 指標後面的資訊會指定 AVIBall 在內部使用的資料。 您的串流處理常式可以在 **IAVIStreamVtbl** 指標之後附加自己的資訊。 這項資訊會在後續的資料流程處理常式呼叫中傳回。


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



 

 




