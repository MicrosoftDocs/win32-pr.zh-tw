---
title: Type_free_inst 函式
description: Stub 會呼叫型別 \_ free \_ inst 函式來釋出與所呈現類型相關聯的記憶體。
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc71c8d3557c62eec39fe9a90855ef3ed057d29c21ec60a82ddc7fe04207f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923707"
---
# <a name="the-type_free_inst-function"></a>Type \_ free \_ inst 函式

Stub 會呼叫 **型別 \_ free \_ inst** 函式來釋出與所呈現類型相關聯的記憶體。 函式定義如下：

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

參數會指向所呈現的型別實例。 此物件不應該釋放。 如需有關何時呼叫函數的討論，請參閱 [傳輸 \_ 為屬性](the-transmit-as-attribute.md)。

在下列範例中，透過將清單移至結尾，然後備份和釋放清單的每個元素，來釋出雙重連結清單。


```C++
void __RPC_USER DOUBLE_LINK_TYPE_free_inst(
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    while (pList->pNext != NULL)  // go to end of the list
        pList = pList->pNext;

    pList = pList->pPrevious;
    while (pList != NULL) 
    {  
        // back through the list
        midl_user_free(pList->pNext);
        pList = pList->pPrevious;
    }
} 
```



 

 




