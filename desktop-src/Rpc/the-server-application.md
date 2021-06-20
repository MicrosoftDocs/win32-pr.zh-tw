---
title: 伺服器應用程式
description: 查看遠端程序呼叫的伺服器應用程式部分， (RPC) 範例。 此範例來自 Platform SDK 中的「Hello World」應用程式。
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b8a2bb66fd415a9b8f778134edb4903f88a717
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406061"
---
# <a name="the-server-application"></a><span data-ttu-id="b7ca3-104">伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="b7ca3-104">The Server Application</span></span>

<span data-ttu-id="b7ca3-105">下列範例是從 \\ 平臺軟體發展工具組 (SDK) 的 RPC Hello 目錄中的「Hello World」應用程式。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-105">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="b7ca3-106">分散式應用程式的伺服器端會通知系統該服務是否可用。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-106">The server side of the distributed application informs the system that its services are available.</span></span> <span data-ttu-id="b7ca3-107">然後，它會等候用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-107">It then waits for client requests.</span></span> <span data-ttu-id="b7ca3-108">MIDL 編譯器必須與下列範例搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-108">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="b7ca3-109">根據您的應用程式大小和程式碼偏好設定，您可以選擇在一或多個不同的檔案中執行遠端程式。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-109">Depending on the size of your application and your coding preferences, you can choose to implement remote procedures in one or more separate files.</span></span> <span data-ttu-id="b7ca3-110">在本教學課程程式中，來源檔案 Hellos 包含主伺服器常式。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-110">In this tutorial program, the source file Hellos.c contains the main server routine.</span></span> <span data-ttu-id="b7ca3-111">File Hellop 包含遠端程式。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-111">The file Hellop.c contains the remote procedure.</span></span>

<span data-ttu-id="b7ca3-112">將遠端程式組織在不同檔案中的好處是，程式可以連結到獨立程式，以便在程式碼轉換成分散式應用程式之前先行進行程式碼的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-112">The benefit of organizing the remote procedures in separate files is that the procedures can be linked with a standalone program to debug the code before it is converted to a distributed application.</span></span> <span data-ttu-id="b7ca3-113">程式在獨立程式中運作之後，您可以使用伺服器應用程式來編譯和連結包含遠端程式的原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-113">After the procedures work in the standalone program, you can compile and link the source files containing the remote procedures with the server application.</span></span> <span data-ttu-id="b7ca3-114">如同用戶端應用程式的原始程式檔，伺服器應用程式來源檔案必須包含 Hello .h 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-114">As with the client-application source file, the server-application source file must include the Hello.h header file.</span></span>

<span data-ttu-id="b7ca3-115">伺服器會呼叫 RPC 執行時間函式 [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) 和 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) ，讓系結資訊可供用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-115">The server calls the RPC run-time functions [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) and [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to make binding information available to the client.</span></span> <span data-ttu-id="b7ca3-116">這個範例程式會將介面控制碼名稱傳遞給 **RpcServerRegisterIf**。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-116">This example program passes the interface handle name to **RpcServerRegisterIf**.</span></span> <span data-ttu-id="b7ca3-117">其他參數則設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-117">The other parameters are set to **NULL**.</span></span> <span data-ttu-id="b7ca3-118">然後，伺服器會呼叫 [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) 函式來指出它正在等候用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-118">The server then calls the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to indicate that it is waiting for client requests.</span></span>

<span data-ttu-id="b7ca3-119">伺服器應用程式也必須包含伺服器 stub 所呼叫的兩個記憶體管理函數： [**midl \_ user \_ allocate**](the-midl-user-allocate-function.md) 和 [**midl \_ user \_ free**](the-midl-user-free-function.md)。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-119">The server application must also include the two memory management functions that the server stub calls: [**midl\_user\_allocate**](the-midl-user-allocate-function.md) and [**midl\_user\_free**](the-midl-user-free-function.md).</span></span> <span data-ttu-id="b7ca3-120">當遠端程式將參數傳遞至伺服器時，這些函式會在伺服器上配置和釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-120">These functions allocate and free memory on the server when a remote procedure passes parameters to the server.</span></span> <span data-ttu-id="b7ca3-121">在此範例程式中 **，midl \_ 使用者 \_ 配置** 和 **midl \_ 使用者 \_ 可用** 是 [**直接和**](pointers-and-memory-allocation.md)**免費** 的 C 程式庫函式的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-121">In this example program, **midl\_user\_allocate** and **midl\_user\_free** are simply wrappers for the C-library functions [**malloc**](pointers-and-memory-allocation.md) and **free**.</span></span> <span data-ttu-id="b7ca3-122"> (請注意，在 MIDL 編譯器產生的向前宣告中，"MIDL" 為大寫。</span><span class="sxs-lookup"><span data-stu-id="b7ca3-122">(Note that, in the MIDL compiler- generated forward declarations, "MIDL" is uppercase.</span></span> <span data-ttu-id="b7ca3-123">標頭檔 Rpcndr \_ \_ 會將 midl 使用者 free 和 midl \_ 使用者 \_ 配置分別定義為 MIDL \_ 使用者 \_ free 和 midl \_ 使用者 \_ 配置。 ) </span><span class="sxs-lookup"><span data-stu-id="b7ca3-123">The header file Rpcndr.h defines midl\_user\_free and midl\_user\_allocate to be MIDL\_user\_free and MIDL\_user\_allocate, respectively.)</span></span>


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



 

 




