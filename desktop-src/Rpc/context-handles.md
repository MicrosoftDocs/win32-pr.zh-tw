---
title: 內容控制碼
description: 有時，分散式應用程式需要伺服器程式來維護用戶端呼叫之間的狀態資訊。
ms.assetid: 91732a75-0a3a-44bd-9db9-c11be6fd2d70
keywords:
- 遠端程序呼叫 RPC、描述、內容控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ff36ff8f1a36843293060e091b7eecee0d8666
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965796"
---
# <a name="context-handles"></a><span data-ttu-id="cd480-104">內容控制碼</span><span class="sxs-lookup"><span data-stu-id="cd480-104">Context Handles</span></span>

<span data-ttu-id="cd480-105">有時，分散式應用程式需要伺服器程式來維護用戶端呼叫之間的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="cd480-105">It is sometimes the case that distributed applications require the server program to maintain status information between client calls.</span></span> <span data-ttu-id="cd480-106">一次服務多個用戶端的伺服器程式必須保留每個用戶端的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="cd480-106">Server programs that service more than one client at a time must keep the state information for each client.</span></span> <span data-ttu-id="cd480-107">由於用戶端和伺服器在不同的電腦上使用不同的位址空間，而且它們不一定互相信任，通常資料共用的常見方法無法運作。</span><span class="sxs-lookup"><span data-stu-id="cd480-107">Because the client and the server use different address spaces on different computers, and they do not necessarily trust each other, common approaches to data sharing often do not work.</span></span> <span data-ttu-id="cd480-108">例如，用戶端和伺服器無法在其全域變數的遠端會話上維護狀態資訊，因為它們不會共用相同的全域位址空間。</span><span class="sxs-lookup"><span data-stu-id="cd480-108">For instance, the client and server are unable to maintain status information on their remote session in global variables because they do not share the same global address space.</span></span> <span data-ttu-id="cd480-109">因為它們是在不同的電腦上執行，所以很難將資訊保存在共用的檔案中。</span><span class="sxs-lookup"><span data-stu-id="cd480-109">It is difficult to keep the information in a shared file because they run on different computers.</span></span> <span data-ttu-id="cd480-110">簡單的方法可能是將所有狀態傳送給用戶端，並讓用戶端在下一次呼叫時傳回它，但是這個方法有個缺點：伺服器不一定會信任用戶端傳回正確的狀態，而且狀態可能會隱含地系結至伺服器上的其他狀態，例如，檔案控制代碼或開啟的通訊端。</span><span class="sxs-lookup"><span data-stu-id="cd480-110">A simplistic approach may be to ship all state to the client and have the client return it on the next call, but this approach has flaws: the server does not necessarily trust the client to return the right state, and the state may be implicitly tied to some other state on the server, such as file handles or opened sockets.</span></span>

<span data-ttu-id="cd480-111">Microsoft RPC 提供一個功能強大又安全的機制，稱為內容控制碼，可保持與伺服器上指定用戶端相關聯的狀態。</span><span class="sxs-lookup"><span data-stu-id="cd480-111">Microsoft RPC provides a powerful and secure mechanism called context handles for keeping state associated with a given client on a server.</span></span> <span data-ttu-id="cd480-112">狀態資訊稱為伺服器的內容。</span><span class="sxs-lookup"><span data-stu-id="cd480-112">The state information is called the server's context.</span></span> <span data-ttu-id="cd480-113">用戶端可以取得內容控制碼，以識別其個別 RPC 會話的伺服器內容。</span><span class="sxs-lookup"><span data-stu-id="cd480-113">Clients can obtain a context handle to identify the server's context for their individual RPC sessions.</span></span>

<span data-ttu-id="cd480-114">例如，分散式應用程式中的每個用戶端都可以讓伺服器程式建立並更新其 RPC 會話的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="cd480-114">As an example, each client in a distributed application can have the server program create and update a data file for their RPC session.</span></span> <span data-ttu-id="cd480-115">伺服器可以使用其檔案控制代碼，將每個用戶端的資料檔案當作內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd480-115">The server can use its file handle for each client's data file as the context handle.</span></span> <span data-ttu-id="cd480-116">每次用戶端對伺服器為其建立的資料檔案要求作業時，用戶端會將內容控制碼傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="cd480-116">Each time a client requests operations on the data file that the server creates for it, the client passes the context handle to the server.</span></span> <span data-ttu-id="cd480-117">用戶端不會實際取得檔案控制代碼;它會取得不透明的 token，讓伺服器的 RPC 執行時間可以與檔案控制代碼唯一相關聯。</span><span class="sxs-lookup"><span data-stu-id="cd480-117">The client does not actually get the file handle itself; it gets an opaque token that the server RPC run time can uniquely associate with the file handle.</span></span> <span data-ttu-id="cd480-118">因為內容控制碼其實是一個檔案控制代碼，所以內容控制碼只有在伺服器的位址空間中才有意義。</span><span class="sxs-lookup"><span data-stu-id="cd480-118">Since the context handle is really a file handle, the context handle only makes sense in the server's address space.</span></span> <span data-ttu-id="cd480-119">不過，用戶端程式可以使用內容控制碼來告訴伺服器要執行更新的檔案。</span><span class="sxs-lookup"><span data-stu-id="cd480-119">However, the client program can use the context handle to tell the server on which file to perform updates.</span></span>

<span data-ttu-id="cd480-120">其他資料也可以是內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd480-120">Other data can also be context handles.</span></span> <span data-ttu-id="cd480-121">例如，用戶端和伺服器可以使用資料庫記錄的記錄號碼做為檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="cd480-121">For instance, a client and server can use a record number of a database record as a file handle.</span></span> <span data-ttu-id="cd480-122">如果用戶端需要在特定記錄上執行一些更新，它可以取得記錄號碼作為內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd480-122">If the client needed to perform a number of updates on a particular record, it could obtain the record number as a context handle.</span></span> <span data-ttu-id="cd480-123">它會在每次叫用遠端程式來更新資料庫記錄時，將記錄號碼傳遞給伺服器。</span><span class="sxs-lookup"><span data-stu-id="cd480-123">It would pass the record number to the server each time it invoked a remote procedure to update the database record.</span></span>

<span data-ttu-id="cd480-124">內容控制碼通常會指向伺服器上的記憶體區塊，伺服器會在伺服器上保留各種管理資訊。</span><span class="sxs-lookup"><span data-stu-id="cd480-124">Most often a context handle points to a block of memory on the server where the server keeps various management information.</span></span>

<span data-ttu-id="cd480-125">本節提供定義和使用內容控制碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cd480-125">This section presents information on defining and using context handles.</span></span> <span data-ttu-id="cd480-126">以下主題會提供討論：</span><span class="sxs-lookup"><span data-stu-id="cd480-126">The discussion is presented in the following topics:</span></span>

-   [<span data-ttu-id="cd480-127">使用內容控制碼進行介面開發</span><span class="sxs-lookup"><span data-stu-id="cd480-127">Interface Development Using Context Handles</span></span>](interface-development-using-context-handles.md)
-   [<span data-ttu-id="cd480-128">使用內容控制碼進行伺服器開發</span><span class="sxs-lookup"><span data-stu-id="cd480-128">Server Development Using Context Handles</span></span>](server-development-using-context-handles.md)
-   [<span data-ttu-id="cd480-129">使用內容控制碼的用戶端開發</span><span class="sxs-lookup"><span data-stu-id="cd480-129">Client Development Using Context Handles</span></span>](client-development-using-context-handles.md)
-   [<span data-ttu-id="cd480-130">伺服器內容執行例行常式</span><span class="sxs-lookup"><span data-stu-id="cd480-130">Server Context Run-down Routine</span></span>](server-context-run-down-routine.md)
-   [<span data-ttu-id="cd480-131">用戶端內容重設</span><span class="sxs-lookup"><span data-stu-id="cd480-131">Client Context Reset</span></span>](client-context-reset.md)
-   [<span data-ttu-id="cd480-132">多執行緒用戶端和內容控制碼</span><span class="sxs-lookup"><span data-stu-id="cd480-132">Multithreaded Clients and Context Handles</span></span>](multithreaded-clients-and-context-handles.md)

 

 




