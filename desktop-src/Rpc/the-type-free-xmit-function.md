---
title: Type_free_xmit 函式
description: Stub 會呼叫類型 \_ free xmit 函式 \_ 來釋出與傳輸資料相關聯的記憶體。
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c192e30ec4f18d70d6e694e6097cb77ee7a2338230868730dc37c1c3207010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016578"
---
# <a name="the-type_free_xmit-function"></a>Type \_ free \_ xmit 函式

Stub 會呼叫 **類型 \_ free \_ xmit** 函式來釋出與傳輸資料相關聯的記憶體。 在 [ \_ \_ xmit](the-type-from-xmit-function.md) 函式中的型別將傳輸的資料轉換成其所呈現的型別之後，就不再需要記憶體。 函式定義如下：

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

參數是記憶體的指標，其中包含已傳送的型別。

在此範例中，記憶體包含單一結構中的陣列。 函數雙重 \_ 連結 \_ 類型 \_ free xmit 會 \_ 使用使用者提供的 midl midl \_ 使用者 \_ free 來釋放記憶體：

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




