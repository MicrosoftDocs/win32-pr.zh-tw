---
title: 參考指標
description: 參考指標是最簡單的指標，且需要用戶端存根的最少處理量。
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427605f330b1a73c541c95019f8ca4bdd6cc8ef4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023976"
---
# <a name="reference-pointers"></a>參考指標

參考指標是最簡單的指標，且需要用戶端存根的最少處理量。 當用戶端程式傳遞參考指標給遠端程式時，參考指標一律會包含有效記憶體區塊的位址。 當遠端程式完成時，它仍會指向相同的記憶體區塊。 這些指標主要用來實作為參考語義，並允許 \[ [](/windows/desktop/Midl/out-idl) \] C 中的 out 參數。

在下列範例中，在呼叫期間，指標的值不會變更，但是指標所指出之位址的資料內容可能會變更。

![在靜態參考指標位址變更資料](images/prog-a07.png)

參考指標具有下列特性：

-   它一律會指向有效的儲存體，而且永遠不會有 **Null** 值。
-   它永遠不會在呼叫期間變更，而且一律會在呼叫前後指向相同的儲存體。
-   從遠端程式傳回的資料會寫入至現有的儲存體。
-   參考指標所指向的儲存體無法由函式中的任何其他指標或任何其他名稱存取。

您可以使用 \[ [**ref**](/windows/desktop/Midl/ref) \] 屬性在介面定義中指定參考指標，如下列範例所示。

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, out, ref] char *pChar);
}
```

這個範例會將參數 *pChar* 定義為單一字元的指標，而不是字元陣列。 它是 \[ **out** \] 參數和參考指標，指向伺服器常式 RemoteFn 將填入資料的記憶體。

 

 