---
title: Named_type_to_local 函式
description: 存根會將已命名的型別呼叫 \_ \_ 至區域函式 \_ ，以將資料從傳送的型別轉換為它們呈現給應用程式的型別。
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fc1d45545c920ef19eb4c230045e62322833d3ef38e765357c29b20a48589c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924058"
---
# <a name="the-named_type_to_local-function"></a>區域函式的命名 \_ 類型 \_ \_

存根會將 **已命名的型別呼叫 \_ \_ 至 \_ 區域** 函式，以將資料從傳送的型別轉換為它們呈現給應用程式的型別。 函式定義如下：

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

第一個參數會指向傳送的資料。 函式會設定第二個參數以指向呈現的資料。

**\_ \_ \_ 區域** 函式的命名類型必須管理所呈現類型的記憶體。 函式必須為從第二個參數所指定的位址開始的整個資料結構配置記憶體，但參數本身 (存根會為根節點配置記憶體，並將其傳遞至函式) 。 第二個參數的值不能在呼叫期間變更。 函數可以變更該位址的內容。

 

 




