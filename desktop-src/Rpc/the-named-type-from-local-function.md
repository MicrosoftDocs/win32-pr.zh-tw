---
title: Named_type_from_local 函式
description: 存根從區域函式呼叫命名的 \_ 型別 \_ \_ 。
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c294398913a3bf6fe8b88eed5c42ceec84abf6b23ed994c85ff0fae8f21f2e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127618"
---
# <a name="the-named_type_from_local-function"></a>區域函式中的命名 \_ 類型 \_ \_

存根從區域函式呼叫命名的 \_ 型別 \_ \_ 。 它會將應用程式使用的型別轉換成存根在網路上傳輸的型別。 函式定義如下：

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

第一個參數是應用程式資料的指標。 第二個參數是指向指標的指標。 函式會將它指向傳送的資料。 函數必須為傳輸的類型配置記憶體。

 

 




