---
title: 伺服器內容執行例行常式
description: 如果通訊中斷時，伺服器會代表用戶端維護內容，則可能需要清除常式，以代表指定的用戶端清除伺服器所維護的狀態。
ms.assetid: b39654e4-6f03-43a0-8a5d-6f24bd0a529c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3bab4477555e5a304627d026c7471874af50daceb9fe3e4484928c290a55d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035488"
---
# <a name="server-context-run-down-routine"></a>伺服器內容執行例行常式

如果通訊中斷時，伺服器會代表用戶端維護內容，則可能需要清除常式，以代表指定的用戶端清除伺服器所維護的狀態。 此清除常式稱為 *內容執行常式*。 當連接中斷時，伺服器 stub 和執行時間程式庫會在用戶端開啟的每個內容控制碼上呼叫這個常式。

當您將 \[ **內容 \_ 控制碼** 屬性套用至型別定義時，需要執行內容執行程式，並以隱含方式宣告和命名 \] 。 如果 \[ **內容 \_ 控制碼** \] 屬性直接套用至參數，伺服器將不會呼叫內容執行常式。

內容的執行常式語法如下：

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

請注意，型別名稱會決定內容執行常式的名稱。

接下來的程式碼片段會顯示範例內容的執行常式。 這會使用內容控制碼、使用內容控制碼的[伺服器開發](server-development-using-context-handles.md)，以及[使用內容控制碼的用戶端開發](client-development-using-context-handles.md)，來呼叫在[介面開發](interface-development-using-context-handles.md)的範例中使用的 RemoteClose 程式。 此程式會關閉檔案控制代碼、釋出與檔案相關聯的記憶體，並將 **Null** 指派給內容控制碼。 指派 **Null** 是呼叫 RemoteClose 函式的結果，不需要在執行中的情況下執行。 無論內容控制碼是否設為 **Null**，RPC 執行時間都會清除其狀態。

``` syntax
//file: cxhndp.c (fragment of file containing remote procedures)
//The rundown routine is associated with the context handle type.  
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown(
    PCONTEXT_HANDLE_TYPE phContext)
{
    printf("Client died with an open file, closing it..\n");
    RemoteClose(&phContext);
    assert(phContext == 0);
}
```

 

 




