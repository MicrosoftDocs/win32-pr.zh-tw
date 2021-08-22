---
title: Named_type_free_local 函式
description: Stub 會呼叫型別 \_ 自由區域函式，以釋出對 \_ \_ \_ 本機常式的命名類型呼叫所配置的記憶體 \_ 。
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 123e0eb12a187ee6a5b7665ec126ba98153638e9d766015a0c9e7b1c7aec7dee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924078"
---
# <a name="the-named_type_free_local-function"></a>指名 \_ 型別的 \_ Free \_ 區域函數

Stub 會呼叫 **型別 \_ 自由 \_ 區域** 函式，以釋出對本機常式的 [命名 \_ 類型 \_ \_](the-named-type-to-local-function.md) 呼叫所配置的記憶體。 它不會釋放由存根配置的記憶體。 函數原型的定義如下：

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

參數是由 **命名 \_ 類型配置 \_ 給 \_ 本機** 的記憶體指標。

 

 




