---
title: 伺服器應用程式
description: 下列範例是從 \\ 平臺軟體發展工具組 (SDK) 的 RPC Hello 目錄中的「Hello World」應用程式。
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6f13e2c8fecdcff820c62f3076dd2a8edd1a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840080"
---
# <a name="the-server-application"></a>伺服器應用程式

下列範例是從 \\ 平臺軟體發展工具組 (SDK) 的 RPC Hello 目錄中的「Hello World」應用程式。 分散式應用程式的伺服器端會通知系統該服務是否可用。 然後，它會等候用戶端要求。 MIDL 編譯器必須與下列範例搭配使用。

根據您的應用程式大小和程式碼偏好設定，您可以選擇在一或多個不同的檔案中執行遠端程式。 在本教學課程程式中，來源檔案 Hellos 包含主伺服器常式。 File Hellop 包含遠端程式。

將遠端程式組織在不同檔案中的好處是，程式可以連結到獨立程式，以便在程式碼轉換成分散式應用程式之前先行進行程式碼的偵錯工具。 程式在獨立程式中運作之後，您可以使用伺服器應用程式來編譯和連結包含遠端程式的原始程式檔。 如同用戶端應用程式的原始程式檔，伺服器應用程式來源檔案必須包含 Hello .h 標頭檔。

伺服器會呼叫 RPC 執行時間函式 [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) 和 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) ，讓系結資訊可供用戶端使用。 這個範例程式會將介面控制碼名稱傳遞給 **RpcServerRegisterIf**。 其他參數則設定為 **Null**。 然後，伺服器會呼叫 [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) 函式來指出它正在等候用戶端要求。

伺服器應用程式也必須包含伺服器 stub 所呼叫的兩個記憶體管理函數： [**midl \_ user \_ allocate**](the-midl-user-allocate-function.md) 和 [**midl \_ user \_ free**](the-midl-user-free-function.md)。 當遠端程式將參數傳遞至伺服器時，這些函式會在伺服器上配置和釋放記憶體。 在此範例程式中 **，midl \_ 使用者 \_ 配置** 和 **midl \_ 使用者 \_ 可用** 是 [**直接和**](pointers-and-memory-allocation.md)**免費** 的 C 程式庫函式的包裝函式。  (請注意，在 MIDL 編譯器產生的向前宣告中，"MIDL" 為大寫。 標頭檔 Rpcndr \_ \_ 會將 midl 使用者 free 和 midl \_ 使用者 \_ 配置分別定義為 MIDL \_ 使用者 \_ free 和 midl \_ 使用者 \_ 配置。 ) 


```C++
/* file: hellos.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h"
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszSecurity         = NULL; 
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned int    cMinCalls = 1;
    unsigned int    fDontWait = FALSE;
 
    status = RpcServerUseProtseqEp(pszProtocolSequence,
                                   RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                                   pszEndpoint,
                                   pszSecurity); 
 
    if (status) exit(status);
 
    status = RpcServerRegisterIf(hello_ServerIfHandle,  
                                 NULL,   
                                 NULL); 
 
    if (status) exit(status);
 
    status = RpcServerListen(cMinCalls,
                             RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                             fDontWait);
 
    if (status) exit(status);
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



 

 




