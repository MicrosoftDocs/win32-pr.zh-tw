---
title: Type_to_xmit 函式
description: 存根會將型別呼叫 xmit 函式， \_ \_ 以將應用程式所呈現的型別轉換成傳輸型別。
ms.assetid: fb5b3760-d660-4e4e-b5c5-768e8e598e23
keywords:
- type_to_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970d4a0de9675ac7a5f1b1c1449521177ecb661a1a80fd9ef609a6dc630605a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016498"
---
# <a name="the-type_to_xmit-function"></a>要 xmit 的型別 \_ \_ 函數

存根會將 **型別 \_ 呼叫 \_ xmit** 函式，以將應用程式所呈現的型別轉換成傳輸型別。 函式定義如下：

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

第一個參數是應用程式資料的指標。 第二個參數是由函式所設定，以指向傳輸的資料。 函數必須為傳輸的類型配置記憶體。

在下列範例中，用戶端會呼叫具有 DOUBLE 連結類型之 **\[ in、out \]** 參數的遠端過程 \_ \_ 。 用戶端 stub 會呼叫 **\_ \_ xmit** 函式（在此為 xmit 的類型），以 \_ \_ \_ \_ 將雙重連結的清單資料轉換成大小的陣列。

函式會判斷清單中的專案數、配置夠大的陣列來容納這些元素，然後將清單專案複製到陣列中。 在函數傳回之前，會將第二個參數 *ppArray* 設定為指向新配置的資料結構。


```C++
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray)
{
    short cCount = 0;
    DOUBLE_LINK_TYPE * pHead = pList;  // save pointer to start 
    DOUBLE_XMIT_TYPE * pArray;
 
    /* count the number of elements to allocate memory */
    for (; pList != NULL; pList = pList->pNext)
        cCount++;
 
    /* allocate the memory for the array */
    pArray = (DOUBLE_XMIT_TYPE *) MIDL_user_allocate 
         (sizeof(DOUBLE_XMIT_TYPE) + (cCount * sizeof(short)));
    pArray->sSize = cCount;
 
    /* copy the linked list contents into the array */
    cCount = 0;
    for (i = 0, pList = pHead; pList != NULL; pList = pList->pNext)
        pArray->asNumber[cCount++] = pList->sNumber;
 
    /* return the address of the pointer to the array */
    *ppArray = pArray;
}
```



 

 




