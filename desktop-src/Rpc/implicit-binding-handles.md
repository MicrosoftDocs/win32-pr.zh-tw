---
title: 隱含系結控制碼
description: 隱含系結控制碼可讓您的應用程式選取特定的伺服器，以執行其遠端程序呼叫。
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d49618ec505cc776c346a504fb19b65db539dadb90d030e45efbabcf08371db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929073"
---
# <a name="implicit-binding-handles"></a>隱含系結控制碼

隱含系結控制碼可讓您的應用程式選取特定的伺服器，以執行其遠端程序呼叫。 如需詳細資訊，請參閱 [客戶](client-side-binding.md)端系結。 它們也可讓您的用戶端/伺服器程式使用已驗證的系結。 也就是說，用戶端可以在隱含系結控制碼中指定驗證資訊。 RPC 執行時間程式庫會使用驗證資訊，在用戶端與伺服器之間建立經過驗證的 RPC 會話。 如需詳細資訊，請參閱[安全性](security.md)。

> [!Note]  
> 隱含系結控制碼不是安全線程。 因此，多執行緒應用程式應該避免使用隱含的系結控制碼。

 

當您的應用程式使用隱含系結時，用戶端必須設定系結資訊，讓它可以建立系結。 用戶端建立隱含系結之後，不需要將任何系結控制碼傳遞至遠端程式。 RPC 程式庫會處理通訊會話的其他機制。

用戶端會將隱含控制碼的系結資訊儲存在全域變數中。 當 MIDL 編譯器從 MIDL 檔案中的介面規格產生用戶端 stub 和標頭檔時，它也會產生全域系結控制碼變數的程式碼。 您的用戶端程式會初始化控制碼，然後不會再次參考它，直到它終結系結為止。

您可以 \[ 在介面的 ACF 中指定 [**隱含 \_ 控制碼**](/windows/desktop/Midl/implicit-handle)屬性，藉以建立隱含的控制碼，如下所示 \] ：

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

在上述範例中使用的 **控制碼 \_ t 型別** 是用來定義系結控制碼的 MIDL 資料型別。

建立隱含控制碼之後，應用程式必須使用它做為 RPC 執行時間程式庫函式的參數。 請勿使用隱含控制碼做為遠端程序呼叫的參數。 下列程式碼範例將示範隱含系結控制碼的使用。

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

在上述範例中，RPC 執行時間程式庫函式 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) 和 [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) 都需要在其參數清單中傳遞隱含系結控制碼。 不過，遠端過程 MyRemoteProcedure 並不是 RPC 執行時間程式庫函式，因此不會發生。

 

 