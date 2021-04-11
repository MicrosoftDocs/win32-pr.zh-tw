---
title: Type_from_xmit 函式
description: 存根從 xmit 函式呼叫型別， \_ \_ 以將資料從其傳送的型別轉換為向應用程式呈現的型別。
ms.assetid: 679a2738-a166-4e73-bca7-950f979ed97a
keywords:
- type_from_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e594e8586522dd3697f5ae62c95851917741f73c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021891"
---
# <a name="the-type_from_xmit-function"></a>Xmit 函式中的型別 \_ \_

存根 **\_ 從 \_ xmit** 函式呼叫型別，以將資料從其傳送的型別轉換為向應用程式呈現的型別。 函式定義如下：

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

第一個參數是傳輸資料的指標。 函式會設定第二個參數以指向呈現的資料。

**\_ \_ Xmit** 函式中的型別必須管理顯示類型的記憶體。 函式必須為從第二個參數所指定的位址開始的整個資料結構配置記憶體，但參數本身 (存根會為根節點配置記憶體，並將其傳遞至函式) 。 第二個參數的值不能在呼叫期間變更。 函數可以變更該位址的內容。

在此範例中，xmit 的函式雙重 \_ 連結 \_ 類型會 \_ \_ 將調整大小的陣列轉換成雙重連結的清單。 函式會保留清單開頭的有效指標、釋放與清單其餘部分相關聯的記憶體，然後建立從相同指標開始的新清單。 函數會使用公用程式函式 **InsertNewNode**，將清單節點附加至清單結尾，並將 *pNext* 和 *pPrevious* 指標指派給適當的值。


```C++
void __RPC_USER DOUBLE_LINK_TYPE_from_xmit(
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    DOUBLE_LINK_TYPE *pCurrent;
    int i;
 
    if (pArray->sSize <= 0) 
    {  
        // error checking
        return;
    }
 
    if (pList == NULL) // if invalid, create the list head
        pList = InsertNewNode(pArray->asNumber[0], NULL);             
    else 
    {    
        DOUBLE_LINK_TYPE_free_inst(pList);  // free all other nodes
        pList->sNumber = pArray->asNumber[0];
        pList->pNext = NULL; 
    }
 
    pCurrent = pList; 
    for (i = 1; i < pArray->sSize; i++)  
        pCurrent = InsertNewNode(pArray->asNumber[i], pCurrent);
    
    return;
}
```



 

 




