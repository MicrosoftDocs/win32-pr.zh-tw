---
title: 用戶端應用程式
description: " (RPC) 範例中，查看遠端程序呼叫的用戶端應用程式部分。 下列範例是從 Platform SDK 中的「Hello World」應用程式。"
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570e883d908a12a053052945675e8819c3dbdcc8bb6a30fba787f1f62c49e9e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924547"
---
# <a name="the-client-application"></a>用戶端應用程式

下列範例是從 \\ 平臺軟體發展工具組 (SDK) 的 RPC Hello 目錄中的「Hello World」應用程式。 Helloc 來源檔案包含指示詞，以包含 MIDL 產生的標頭檔（Hello. h）。 在 Hello. h 中，指示詞包含 Rpc 和 rpcndr，其中包含 RPC 執行時間常式的定義、 **HelloProc** 和 **關機**，以及用戶端和伺服器應用程式所使用的資料類型。 MIDL 編譯器必須與下列範例搭配使用。

由於用戶端會管理它與伺服器的連線，因此用戶端應用程式會呼叫執行時間函式來建立伺服器的控制碼，並在遠端程序呼叫完成之後釋放這個控制碼。 函式 [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) 會將系結控制碼的元件組合成該控制碼的字串表示，並配置字串系結的記憶體。 函數 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) 會針對用戶端應用程式，從該字串表示建立伺服器系結控制碼（ **hello \_ ClientIfHandle**）。

在呼叫 [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose)時，參數不會指定 UUID，因為本教學課程假設只有一個介面 "hello" 的實作為。 此外，呼叫不會指定網路位址，因為應用程式會使用預設值，也就是本機主機電腦。 通訊協定序列是代表基礎網路傳輸的字元字串。 端點是通訊協定順序的特定名稱。 此範例會針對其網路傳輸使用具名管道，因此通訊協定順序為 "ncacn \_ np"。 端點名稱為 " \\ pipe \\ hello"。

實際的遠端程序呼叫（ **HelloProc** 和 **關機**）會在 RPC 例外狀況處理常式內發生，這是一組宏，可讓您控制應用程式程式碼之外發生的例外狀況。 如果 RPC 執行時間模組報告例外狀況，控制權會傳遞至 [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) 區塊。 這是您插入程式碼以進行任何必要清除，然後正常結束的位置。 這個範例程式只會通知使用者發生例外狀況。 如果您不想要使用例外狀況，您可以使用 [ACF 屬性] 的 [ [comm \_ 狀態](/windows/desktop/Midl/comm-status) ] 和 [ [錯誤] \_ 狀態](/windows/desktop/Midl/fault-status) 來報告錯誤。

完成遠端程序呼叫之後，用戶端會先呼叫 [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) 來釋放為字串系結配置的記憶體。 請注意，建立系結控制碼之後，用戶端程式可以隨時釋放字串系結。 用戶端接著會呼叫 [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) 來釋放控制碼。


```C++
/* file: helloc.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h" 
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszUuid             = NULL;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszNetworkAddress   = NULL;
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned char * pszOptions          = NULL;
    unsigned char * pszStringBinding    = NULL;
    unsigned char * pszString           = "hello, world";
    unsigned long ulCode;
 
    status = RpcStringBindingCompose(pszUuid,
                                     pszProtocolSequence,
                                     pszNetworkAddress,
                                     pszEndpoint,
                                     pszOptions,
                                     &pszStringBinding);
    if (status) exit(status);

    status = RpcBindingFromStringBinding(pszStringBinding, &hello_ClientIfHandle);
 
    if (status) exit(status);
 
    RpcTryExcept  
    {
        HelloProc(pszString);
        Shutdown();
    }
    RpcExcept(1) 
    {
        ulCode = RpcExceptionCode();
        printf("Runtime reported exception 0x%lx = %ld\n", ulCode, ulCode);
    }
    RpcEndExcept
 
    status = RpcStringFree(&pszStringBinding); 
 
    if (status) exit(status);
 
    status = RpcBindingFree(&hello_IfHandle);
 
    if (status) exit(status);

    exit(0);
}

/******************************************************/
/*         MIDL allocate and free                     */
/******************************************************/
 
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t len)
{
    return(malloc(len));
}
 
void __RPC_USER midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 