---
title: 完整指標
description: 與唯一指標不同，完整指標支援別名。
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18687b496ddd28dca9e70afca8deafb18774500a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933343"
---
# <a name="full-pointers"></a>完整指標

與 [唯一](unique-pointers.md) 指標不同，完整指標支援別名。 這表示多個指標可以參考相同的資料，如下圖所示：

![參考相同資料的兩個指標](images/prog-a02.png)

完整指標具有下列特性：

-   其值可以是 null。
-   在呼叫期間，它可以從 null 變更為非 null。 當值變更為非 null 時，用戶端 stub 會配置傳回時配置的新記憶體。 用戶端程式應該在它結束之前釋出此記憶體。
-   在呼叫期間，它可以從非 null 變更為 null。 當值變更為 null 時，應用程式會負責釋放記憶體。
-   值可以從一個非 null 值變更為另一個值。
-   在作業中，可能會透過另一個指標或名稱來存取完整指標指向的儲存體。
-   如果指標沒有 null 值，則會將傳回的資料寫入至現有的儲存體。

使用 \[ [**ptr**](/windows/desktop/Midl/ptr) \] 屬性指定完整的指標，如下列範例所示：

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface FullPtrInterface
{
  void RemoteFn([in,ptr,string]) char *ptrName1,
                [in,ptr,string]  char *ptrName2);
}
```

在此範例中， *ptrName1* 和 *ptrName2* 參數定義為字串的完整指標。 這兩個指標可能會指向包含單一字串的相同記憶體位址。

\[**ptr** \]提供別名支援時是必要的。 不過，因為它需要大部分的 RPC 中可用指標的處理，所以不建議用於大部分的應用程式。

 

 