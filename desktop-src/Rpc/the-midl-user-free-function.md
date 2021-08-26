---
title: Midl_user_free 函式
description: Midl \_ 使用者 \_ free 函數必須由 RPC 開發人員提供。
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6ca52635da5bedb60fdc7f94165ad9c888c030d5fe3340c53dfc970a90ff49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080818"
---
# <a name="the-midl_user_free-function"></a>Midl \_ 使用者 \_ free 函數

**Midl \_ 使用者 \_ free** 函數必須由 RPC 開發人員提供。 它會配置 RPC 存根和程式庫常式的記憶體。 **Midl \_ 使用者 \_ free** 函數必須符合下列原型：

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

*PBuffer* 參數會指定要釋放之記憶體的指標。 用戶端應用程式和伺服器應用程式都必須執行 **midl \_ 使用者 \_ 自由** 函式，除非您在憑證相容性 ([**/osf**](/windows/desktop/Midl/-osf)) 模式中進行編譯。 **Midl \_ 使用者 \_ free** 函數必須能夠釋出 [**midl \_ 使用者配置所 \_ 配置**](the-midl-user-allocate-function.md)的所有儲存體。

處理已配置的物件時，應用程式和存根會呼叫 **midl \_ 使用者 \_ free** ：

-   伺服器應用程式應該呼叫 **midl \_ 使用者 \_ free** 以釋出應用程式所配置的記憶體，例如刪除動態配置的資料節點時。
-   伺服器 stub 會在封送處理所有 out **\_ \_** \[ \] 引數、 \[ in \] 、 \[ out \] 引數和函式傳回值之後，呼叫 midl 使用者 free 釋放伺服器上的記憶體。

例如，顯示 "Hello，world" 的 RPC Windows 範例程式會根據 C 函式免費執行 **midl \_ 使用者 \_** ：


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> 如果啟用了 RpcSs 封裝 (例如，因為使用 [ \[ [**啟用 \_ 配置**](/windows/desktop/Midl/enable-allocate)] \] 屬性) 的結果，您的伺服器程式應該使用 [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree)來釋放記憶體。 如需詳細資訊，請參閱「 [RpcSs 記憶體管理套件](rpcss-memory-management-package.md)」。

 

 

 