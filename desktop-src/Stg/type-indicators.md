---
title: 類型指標
description: 實際屬性會遵循屬性識別碼/位移配對屬性集值的表格。 每個屬性都會儲存為 DWORD，後面接著資料類型值。
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8383a860f07e908b72a7b25091f3cc2e280e4407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023837"
---
# <a name="type-indicators"></a>類型指標

實際屬性會遵循屬性識別碼/位移配對屬性集值的表格。 每個屬性都會儲存為 **DWORD**，後面接著資料類型值。

類型指標和其相關聯的值會在 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構中描述。

所有類型/值組都必須從32位界限開始。 因此，值之後可能會有 null 位元組，以在32位界限上對齊後續的配對。

下列範例程式碼會根據指定的位元組計數，計算在32位界限上對齊所需的位元組數目。


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



在值的向量內，每次重複小於32位的簡單純量值，都必須符合其自然對齊，而不是32位的對齊方式。 在實務上，這僅適用于型 **別 \_ VT UI1**、 **vt \_ UI2**、 **vt \_ I2** 和 **vt \_ BOOL** (，其中有一個位元組或雙位元組的自然對齊) 。 所有其他類型都有四個位元組的自然對齊。 某些類型（例如 **VT \_ R8**）實際上有8個位元組的自然對齊，但是會儲存為具有四位元組對齊的方式。

型別指標 **vt \_** 的 \| **vt \_ 向量** 的屬性值包含：

-   **DWORD** 元素計數。
-   封裝的雙位元組整數，其之間沒有 null 填補的序列。

> [!IMPORTANT]
> 任何儲存為 vector property 元素一部分的32位元數目或屬性類型，也必須對齊32位。

 

類型識別碼 **VT \_ LPSTR** \| **vt \_ 向量** 的屬性值包含：

-   Dword **元素計數** (**dword** *cElems*) 。
-   字串序列 (**char** *rgch \[ \]*) ，每個字串前面都加上長度計數 **DWORD** ，而且後面可能接著 null 填補以舍入至32位界限。

 

 