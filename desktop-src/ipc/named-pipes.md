---
description: 具名管道是管道伺服器與一或多個管道用戶端之間通訊的已命名單向或雙工管道。
ms.assetid: 7a4c11ac-14c0-4a93-b72e-02fb8852cc15
title: 具名管道
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0675244e09b7c202b4fa6b67f6268392b1b260f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944384"
---
# <a name="named-pipes"></a><span data-ttu-id="d1e44-103">具名管道</span><span class="sxs-lookup"><span data-stu-id="d1e44-103">Named Pipes</span></span>

<span data-ttu-id="d1e44-104">*具名管道* 是管道伺服器與一或多個管道用戶端之間通訊的已命名單向或雙工管道。</span><span class="sxs-lookup"><span data-stu-id="d1e44-104">A *named pipe* is a named, one-way or duplex pipe for communication between the pipe server and one or more pipe clients.</span></span> <span data-ttu-id="d1e44-105">具名管道的所有實例都共用相同的管道名稱，但每個實例都有自己的緩衝區和控制碼，並為用戶端/伺服器通訊提供個別的管道。</span><span class="sxs-lookup"><span data-stu-id="d1e44-105">All instances of a named pipe share the same pipe name, but each instance has its own buffers and handles, and provides a separate conduit for client/server communication.</span></span> <span data-ttu-id="d1e44-106">使用實例可讓多個管道用戶端同時使用相同的具名管道。</span><span class="sxs-lookup"><span data-stu-id="d1e44-106">The use of instances enables multiple pipe clients to use the same named pipe simultaneously.</span></span>

<span data-ttu-id="d1e44-107">任何程式都可以存取具名管道（受限於安全性檢查），使具名管道成為相關或不相關進程之間的簡單通訊形式。</span><span class="sxs-lookup"><span data-stu-id="d1e44-107">Any process can access named pipes, subject to security checks, making named pipes an easy form of communication between related or unrelated processes.</span></span>

<span data-ttu-id="d1e44-108">任何程式都可以同時作為伺服器和用戶端，以進行對等通訊。</span><span class="sxs-lookup"><span data-stu-id="d1e44-108">Any process can act as both a server and a client, making peer-to-peer communication possible.</span></span> <span data-ttu-id="d1e44-109">如這裡所用，「管道伺服器」一詞是指建立具名管道的進程，而「管道用戶端」一詞是指連接到具名管道實例的進程。</span><span class="sxs-lookup"><span data-stu-id="d1e44-109">As used here, the term pipe server refers to a process that creates a named pipe, and the term pipe client refers to a process that connects to an instance of a named pipe.</span></span> <span data-ttu-id="d1e44-110">用來具現化具名管道的伺服器端函式為 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)。</span><span class="sxs-lookup"><span data-stu-id="d1e44-110">The server-side function for instantiating a named pipe is [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).</span></span> <span data-ttu-id="d1e44-111">用於接受連接的伺服器端函數是 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)。</span><span class="sxs-lookup"><span data-stu-id="d1e44-111">The server-side function for accepting a connection is [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe).</span></span> <span data-ttu-id="d1e44-112">用戶端進程會使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 或 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) 函式連接到具名管道。</span><span class="sxs-lookup"><span data-stu-id="d1e44-112">A client process connects to a named pipe by using the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function.</span></span>

<span data-ttu-id="d1e44-113">具名管道可用來提供相同電腦上的處理常式或網路上不同電腦上的進程之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="d1e44-113">Named pipes can be used to provide communication between processes on the same computer or between processes on different computers across a network.</span></span> <span data-ttu-id="d1e44-114">如果伺服器服務正在執行，則所有具名管道都可從遠端存取。</span><span class="sxs-lookup"><span data-stu-id="d1e44-114">If the server service is running, all named pipes are accessible remotely.</span></span> <span data-ttu-id="d1e44-115">如果您想要在本機使用具名管道，請拒絕存取 NT 授權單位 \\ 網路或切換至本機 RPC。</span><span class="sxs-lookup"><span data-stu-id="d1e44-115">If you intend to use a named pipe locally only, deny access to NT AUTHORITY\\NETWORK or switch to local RPC.</span></span>

<span data-ttu-id="d1e44-116">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="d1e44-116">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="d1e44-117">管道名稱</span><span class="sxs-lookup"><span data-stu-id="d1e44-117">Pipe Names</span></span>](pipe-names.md)
-   [<span data-ttu-id="d1e44-118">具名管道開啟模式</span><span class="sxs-lookup"><span data-stu-id="d1e44-118">Named Pipe Open Modes</span></span>](named-pipe-open-modes.md)
-   [<span data-ttu-id="d1e44-119">具名管道類型、讀取和等候模式</span><span class="sxs-lookup"><span data-stu-id="d1e44-119">Named Pipe Type, Read, and Wait Modes</span></span>](named-pipe-type-read-and-wait-modes.md)
-   [<span data-ttu-id="d1e44-120">具名管道實例</span><span class="sxs-lookup"><span data-stu-id="d1e44-120">Named Pipe Instances</span></span>](named-pipe-instances.md)
-   [<span data-ttu-id="d1e44-121">具名管道作業</span><span class="sxs-lookup"><span data-stu-id="d1e44-121">Named Pipe Operations</span></span>](named-pipe-operations.md)
-   [<span data-ttu-id="d1e44-122">同步和重迭的輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="d1e44-122">Synchronous and Overlapped Input and Output</span></span>](synchronous-and-overlapped-input-and-output.md)
-   [<span data-ttu-id="d1e44-123">具名管道安全性和存取權限</span><span class="sxs-lookup"><span data-stu-id="d1e44-123">Named Pipe Security and Access Rights</span></span>](named-pipe-security-and-access-rights.md)
-   [<span data-ttu-id="d1e44-124">模擬具名管道用戶端</span><span class="sxs-lookup"><span data-stu-id="d1e44-124">Impersonating a Named Pipe Client</span></span>](impersonating-a-named-pipe-client.md)
-   [<span data-ttu-id="d1e44-125">使用管道</span><span class="sxs-lookup"><span data-stu-id="d1e44-125">Using Pipes</span></span>](using-pipes.md)

 

 
