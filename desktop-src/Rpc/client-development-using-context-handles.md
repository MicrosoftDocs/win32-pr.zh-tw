---
title: 使用內容控制碼的用戶端開發
description: 唯一使用用戶端程式的內容控制碼，就是在每次用戶端進行遠端程序呼叫時，將它傳遞至伺服器。
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c7d2dfca901085c743b25eb233ee2493b893e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507377"
---
# <a name="client-development-using-context-handles"></a><span data-ttu-id="bbe74-103">使用內容控制碼的用戶端開發</span><span class="sxs-lookup"><span data-stu-id="bbe74-103">Client Development Using Context Handles</span></span>

<span data-ttu-id="bbe74-104">唯一使用用戶端程式的內容控制碼，就是在每次用戶端進行遠端程序呼叫時，將它傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="bbe74-104">The only use a client program has for a context handle is to pass it to the server each time the client makes a remote procedure call.</span></span> <span data-ttu-id="bbe74-105">用戶端應用程式不需要存取控制碼的內容。</span><span class="sxs-lookup"><span data-stu-id="bbe74-105">The client application does not need to access the contents of the handle.</span></span> <span data-ttu-id="bbe74-106">它不應該嘗試以任何方式變更內容處理資料。</span><span class="sxs-lookup"><span data-stu-id="bbe74-106">It should not try to change the context handle data in any way.</span></span> <span data-ttu-id="bbe74-107">用戶端叫用的遠端程式會對伺服器內容執行所有必要的作業。</span><span class="sxs-lookup"><span data-stu-id="bbe74-107">The remote procedures that the client invokes perform all necessary operations on the server's context.</span></span>

<span data-ttu-id="bbe74-108">從伺服器要求內容控制碼之前，用戶端必須先建立與伺服器的系結。</span><span class="sxs-lookup"><span data-stu-id="bbe74-108">Prior to requesting a context handle from a server, clients must establish a binding with the server.</span></span> <span data-ttu-id="bbe74-109">用戶端可以使用自動、隱含或明確的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="bbe74-109">The client may use an automatic, implicit, or explicit binding handle.</span></span> <span data-ttu-id="bbe74-110">透過有效的系結控制碼，用戶端可以呼叫伺服器上的遠端程式，以傳回開啟的 (非 **Null**) 內容控制碼，或透過遠端程式的參數清單中的 **\[ out \]** 參數傳遞一個。</span><span class="sxs-lookup"><span data-stu-id="bbe74-110">With a valid binding handle, the client can call a remote procedure on the server that either returns an opened (non-**NULL**) context handle or passes one through an **\[out\]** parameter in the remote procedure's parameter list.</span></span>

<span data-ttu-id="bbe74-111">用戶端可能會以任何需要的方式使用開啟的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="bbe74-111">Clients may use opened context handles in any way they require.</span></span> <span data-ttu-id="bbe74-112">不過，它們應該會在不再需要時使控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="bbe74-112">They should, however, invalidate the handle when they no longer need it.</span></span> <span data-ttu-id="bbe74-113">有兩種方式可以執行此作業：</span><span class="sxs-lookup"><span data-stu-id="bbe74-113">There are two way to do this:</span></span>

-   <span data-ttu-id="bbe74-114">若要叫用伺服器程式所提供的遠端程式以釋出內容，並關閉內容控制碼 (將它設定為 **Null**) 。</span><span class="sxs-lookup"><span data-stu-id="bbe74-114">To invoke a remote procedure offered by the server program that frees the context and closes the context handle (sets it to **NULL**).</span></span>
-   <span data-ttu-id="bbe74-115">無法連線到伺服器時，請呼叫 [**RpcSsDestroyClientCoNtext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) 函式。</span><span class="sxs-lookup"><span data-stu-id="bbe74-115">When the server is unreachable, call the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="bbe74-116">第二種方法只會清除用戶端狀態，而且不會清除伺服器端狀態，因此只有在懷疑網路磁碟分割時，才應該使用它，而用戶端和伺服器則會執行獨立的清除作業。</span><span class="sxs-lookup"><span data-stu-id="bbe74-116">The second approach only cleans up the client side state, and does not clean up the server-side state, so it should be used only when network partition is suspected, and the client and the server will do an independent cleanup.</span></span> <span data-ttu-id="bbe74-117">伺服器會透過運行時常式執行獨立的清除，用戶端會使用 [**RpcSsDestroyClientCoNtext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) 函式來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="bbe74-117">The server performs independent cleanup through the run-down routine, the client does so using the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="bbe74-118">下列程式碼片段會顯示用戶端如何使用內容控制碼的範例。</span><span class="sxs-lookup"><span data-stu-id="bbe74-118">The following code fragment presents an example of how a client might use a context handle.</span></span> <span data-ttu-id="bbe74-119">若要查看此範例所使用介面的定義，請參閱 [使用內容控制碼進行介面開發](interface-development-using-context-handles.md)。</span><span class="sxs-lookup"><span data-stu-id="bbe74-119">To view the definition of the interface that this example uses, see [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span> <span data-ttu-id="bbe74-120">如需伺服器的執行，請參閱 [使用內容控制碼的伺服器開發](server-development-using-context-handles.md)。</span><span class="sxs-lookup"><span data-stu-id="bbe74-120">For the server implementation, see [Server Development Using Context Handles](server-development-using-context-handles.md).</span></span>

<span data-ttu-id="bbe74-121">在此範例中，用戶端會呼叫 RemoteOpen 來取得包含有效資料的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="bbe74-121">In this example, the client calls RemoteOpen to obtain a context handle that contains valid data.</span></span> <span data-ttu-id="bbe74-122">然後，用戶端就可以使用遠端程序呼叫中的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="bbe74-122">The client can then use the context handle in remote procedure calls.</span></span> <span data-ttu-id="bbe74-123">由於它不再需要系結控制碼，因此用戶端可以釋放用來建立內容控制碼的明確控制碼：</span><span class="sxs-lookup"><span data-stu-id="bbe74-123">Because it no longer needs the binding handle, the client can free the explicit handle it used to create the context handle:</span></span>


```C++
// cxhndlc.c  (fragment of client side application)
printf("Calling the remote procedure RemoteOpen\n");
if (RemoteOpen(&phContext, pszFileName) < 0) 
{
    printf("Unable to open %s\n", pszFileName);
    Shutdown();
    exit(2);
}
 
// Now the context handle also manages the binding.
// The variable hBindingHandle is a valid binding handle.
status = RpcBindingFree(&hBindingHandle);
printf("RpcBindingFree returned 0x%x\n", status);
if (status) 
    exit(status);
```



<span data-ttu-id="bbe74-124">此範例中的用戶端應用程式會使用名為 RemoteRead 的程式來讀取伺服器上的資料檔案，直到遇到檔案結尾為止。</span><span class="sxs-lookup"><span data-stu-id="bbe74-124">The client application in this example uses a procedure called RemoteRead to read a data file on the server until it encounters an end of file.</span></span> <span data-ttu-id="bbe74-125">然後藉由呼叫 RemoteClose 來關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="bbe74-125">It then closes the file by calling RemoteClose.</span></span> <span data-ttu-id="bbe74-126">內容控制碼會顯示為 RemoteRead 和 RemoteClose 函式中的參數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bbe74-126">The context handle appears as a parameter in the RemoteRead and RemoteClose functions as:</span></span>


```C++
printf("Calling the remote procedure RemoteRead\n");
do 
{
    cbRead = 1024; // Using a 1K buffer
    RemoteRead(phContext, pbBuf, &cbRead);
    // cbRead contains the number of bytes actually read.
    for (int i = 0; i < cbRead; i++)
        putchar(*(pbBuf+i));
} while(cbRead);
 
printf("Calling the remote procedure RemoteClose\n");
if (RemoteClose(&phContext) < 0 ) 
{
    printf("Close failed on %s\n", pszFileName);
    exit(2);
}
```



 

 




