---
title: 用戶端應用程式
description: 下列範例是從 \\ 平臺軟體發展工具組 (SDK) 的 RPC Hello 目錄中的「Hello World」應用程式。
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f97c7c35e00d3f36c645bfad2825dbada5e3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463605"
---
# <a name="the-client-application"></a><span data-ttu-id="4be62-103">用戶端應用程式</span><span class="sxs-lookup"><span data-stu-id="4be62-103">The Client Application</span></span>

<span data-ttu-id="4be62-104">下列範例是從 \\ 平臺軟體發展工具組 (SDK) 的 RPC Hello 目錄中的「Hello World」應用程式。</span><span class="sxs-lookup"><span data-stu-id="4be62-104">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="4be62-105">Helloc 來源檔案包含指示詞，以包含 MIDL 產生的標頭檔（Hello. h）。</span><span class="sxs-lookup"><span data-stu-id="4be62-105">The Helloc.c source file contains a directive to include the MIDL-generated header file, Hello.h.</span></span> <span data-ttu-id="4be62-106">在 Hello. h 中，指示詞包含 Rpc 和 rpcndr，其中包含 RPC 執行時間常式的定義、 **HelloProc** 和 **關機**，以及用戶端和伺服器應用程式所使用的資料類型。</span><span class="sxs-lookup"><span data-stu-id="4be62-106">Within Hello.h are directives to include Rpc.h and rpcndr.h, which contain the definitions for the RPC run-time routines, **HelloProc** and **Shutdown**, and data types that the client and server applications use.</span></span> <span data-ttu-id="4be62-107">MIDL 編譯器必須與下列範例搭配使用。</span><span class="sxs-lookup"><span data-stu-id="4be62-107">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="4be62-108">由於用戶端會管理它與伺服器的連線，因此用戶端應用程式會呼叫執行時間函式來建立伺服器的控制碼，並在遠端程序呼叫完成之後釋放這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="4be62-108">Because the client is managing its connection to the server, the client application calls run-time functions to establish a handle to the server and to release this handle after the remote procedure calls are complete.</span></span> <span data-ttu-id="4be62-109">函式 [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) 會將系結控制碼的元件組合成該控制碼的字串表示，並配置字串系結的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4be62-109">The function [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combines the components of the binding handle into a string representation of that handle and allocates memory for the string binding.</span></span> <span data-ttu-id="4be62-110">函數 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) 會針對用戶端應用程式，從該字串表示建立伺服器系結控制碼（ **hello \_ ClientIfHandle**）。</span><span class="sxs-lookup"><span data-stu-id="4be62-110">The function [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) creates a server binding handle, **hello\_ClientIfHandle**, for the client application from that string representation.</span></span>

<span data-ttu-id="4be62-111">在呼叫 [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose)時，參數不會指定 UUID，因為本教學課程假設只有一個介面 "hello" 的實作為。</span><span class="sxs-lookup"><span data-stu-id="4be62-111">In the call to [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), the parameters do not specify the UUID because this tutorial assumes there is just one implementation of the interface "hello."</span></span> <span data-ttu-id="4be62-112">此外，呼叫不會指定網路位址，因為應用程式會使用預設值，也就是本機主機電腦。</span><span class="sxs-lookup"><span data-stu-id="4be62-112">In addition, the call does not specify a network address because the application will use the default, which is the local host machine.</span></span> <span data-ttu-id="4be62-113">通訊協定序列是代表基礎網路傳輸的字元字串。</span><span class="sxs-lookup"><span data-stu-id="4be62-113">The protocol sequence is a character string that represents the underlying network transport.</span></span> <span data-ttu-id="4be62-114">端點是通訊協定順序的特定名稱。</span><span class="sxs-lookup"><span data-stu-id="4be62-114">The endpoint is a name which is specific to the protocol sequence.</span></span> <span data-ttu-id="4be62-115">此範例會針對其網路傳輸使用具名管道，因此通訊協定順序為 "ncacn \_ np"。</span><span class="sxs-lookup"><span data-stu-id="4be62-115">This example uses named pipes for its network transport, so the protocol sequence is "ncacn\_np".</span></span> <span data-ttu-id="4be62-116">端點名稱為 " \\ pipe \\ hello"。</span><span class="sxs-lookup"><span data-stu-id="4be62-116">The endpoint name is "\\pipe\\hello".</span></span>

<span data-ttu-id="4be62-117">實際的遠端程序呼叫（ **HelloProc** 和 **關機**）會在 RPC 例外狀況處理常式內發生，這是一組宏，可讓您控制應用程式程式碼之外發生的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4be62-117">The actual remote procedure calls, **HelloProc** and **Shutdown**, take place within the RPC exception handler—a set of macros that let you control exceptions that occur outside the application code.</span></span> <span data-ttu-id="4be62-118">如果 RPC 執行時間模組報告例外狀況，控制權會傳遞至 [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) 區塊。</span><span class="sxs-lookup"><span data-stu-id="4be62-118">If the RPC run-time module reports an exception, control passes to the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) block.</span></span> <span data-ttu-id="4be62-119">這是您插入程式碼以進行任何必要清除，然後正常結束的位置。</span><span class="sxs-lookup"><span data-stu-id="4be62-119">This is where you would insert code to do any needed cleanup and then exit gracefully.</span></span> <span data-ttu-id="4be62-120">這個範例程式只會通知使用者發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4be62-120">This example program simply informs the user that an exception occurred.</span></span> <span data-ttu-id="4be62-121">如果您不想要使用例外狀況，您可以使用 [ACF 屬性] 的 [ [comm \_ 狀態](/windows/desktop/Midl/comm-status) ] 和 [ [錯誤] \_ 狀態](/windows/desktop/Midl/fault-status) 來報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="4be62-121">If you do not want to use exceptions, you can use the ACF attributes [comm\_status](/windows/desktop/Midl/comm-status) and [fault\_status](/windows/desktop/Midl/fault-status) to report errors.</span></span>

<span data-ttu-id="4be62-122">完成遠端程序呼叫之後，用戶端會先呼叫 [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) 來釋放為字串系結配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4be62-122">After the remote procedure calls are completed, the client first calls [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) to free the memory that was allocated for the string binding.</span></span> <span data-ttu-id="4be62-123">請注意，建立系結控制碼之後，用戶端程式可以隨時釋放字串系結。</span><span class="sxs-lookup"><span data-stu-id="4be62-123">Note that once the binding handle has been created, a client program can free a string binding at any time.</span></span> <span data-ttu-id="4be62-124">用戶端接著會呼叫 [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) 來釋放控制碼。</span><span class="sxs-lookup"><span data-stu-id="4be62-124">The client next calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to release the handle.</span></span>


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



 

 