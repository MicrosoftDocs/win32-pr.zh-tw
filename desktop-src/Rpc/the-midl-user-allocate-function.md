---
title: Midl_user_allocate 函式
description: Midl \_ 使用者 \_ 配置函數是必須由 RPC 應用程式開發人員提供的程式。
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b2e3196de79992f5856b7117b25f05ad782d26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092964"
---
# <a name="the-midl_user_allocate-function"></a>Midl \_ 使用者 \_ 配置函數

**Midl \_ 使用者 \_ 配置** 函數是必須由 RPC 應用程式開發人員提供的程式。 它會配置 RPC 存根和程式庫常式的記憶體。 **Midl \_ 使用者 \_ 配置** 函數必須符合下列原型：

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

*CBytes* 參數會指定要配置的位元組數目。 用戶端應用程式和伺服器應用程式都必須執行 **midl \_ 使用者 \_ 配置** 函式，除非您在憑證相容性 (/osf) 模式中進行編譯。 應用程式和產生的存根呼叫 midl 使用者直接或間接配置來管理 **\_ \_ 配置** 的物件。 例如：

-   用戶端和伺服器應用程式會呼叫 **midl \_ 使用者 \_ 配置** 來配置應用程式的記憶體，例如在樹狀結構或連結清單中建立新節點時。
-   當將資料封送處理至伺服器位址空間時，伺服器 stub 會呼叫 **midl \_ 使用者 \_ 配置** 。
-   從 out 指標所參考的伺服器封送資料時，用戶端 stub 會呼叫 **midl \_ 使用者 \_ 配置** \[ \] 。 請注意，對於 \[ in \] 、 \[ out \] 和 \[ unique \] 指標而言，只有在輸入上的唯一指標值為 null，且在呼叫期間變更為非 null 值時，用戶端 stub 才會呼叫 **midl \_ 使用者 \_ 配置** \[ \] 。 如果 \[ \] 輸入上的 unique 指標不是 null，則用戶端 stub 會將相關聯的資料寫入現有的記憶體。

如果 **midl \_ 使用者 \_ 配置** 無法配置記憶體，則應該傳回 null 指標。

**Midl \_ 使用者 \_ 配置** 函式應傳回8位元組對齊的指標。

例如，平臺軟體發展工具組所提供的範例程式 (SDK) 根據 C 函數 [**malloc**](pointers-and-memory-allocation.md)來實行 **midl \_ 使用者 \_ 配置**：


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> 如果已啟用 RpcSs 封裝 (例如，當使用 [ \[ [**啟用 \_ 配置**](/windows/desktop/Midl/enable-allocate)] 屬性) 的結果時 \] ，請使用 [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate)在伺服器端配置記憶體。 如需 \[ **啟用 \_ 配置** 的詳細資訊 \] ，請參閱 [MIDL 參考](/windows/desktop/Midl/midl-language-reference)。

 

 

 