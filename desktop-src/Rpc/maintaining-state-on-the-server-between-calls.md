---
title: 在呼叫之間維護伺服器上的狀態
description: 您通常需要在不同的 RPC 呼叫 \ 郵件之間維護伺服器上的狀態。使用內容控制碼是最好的方法。 在內部操作內容控制碼的一些單字，有助於瞭解內容控制碼的最大效果。
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- 遠端程序呼叫 RPC、最佳作法、維護呼叫之間的狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00090fb317cba8c33e7b60ac81762d7d21dd4dc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670991"
---
# <a name="maintaining-state-on-the-server-between-calls"></a><span data-ttu-id="a5fa4-105">在呼叫之間維護伺服器上的狀態</span><span class="sxs-lookup"><span data-stu-id="a5fa4-105">Maintaining State on the Server Between Calls</span></span>

<span data-ttu-id="a5fa4-106">您通常必須在不同的 RPC 呼叫之間維護伺服器上的狀態，而使用內容控制碼是最好的方式。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-106">It is often necessary to maintain state on the server between separate RPC calls—using context handles is the best way to do so.</span></span> <span data-ttu-id="a5fa4-107">在內部操作內容控制碼的一些單字，有助於瞭解內容控制碼的最大效果。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-107">A few words about how context handles operate internally helps in understanding when context handles work best.</span></span>

<span data-ttu-id="a5fa4-108">用戶端永遠不會收到保留在伺服器上的狀態。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-108">The client never receives the state kept on the server.</span></span> <span data-ttu-id="a5fa4-109">伺服器上的狀態通常是記憶體區塊的指標，而用戶端沒有相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-109">Most often the state on the server is a pointer to a memory block, and the client has no information about it.</span></span> <span data-ttu-id="a5fa4-110">所有用戶端接收都是一個大型的唯一數位，其中有與其相關聯的其他資訊，伺服器會傳送給用戶端，而這代表所有後續作業中的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-110">All the client receives is a large unique number, with other information associated with it, that the server sends to the client and which represents the context handle in all subsequent operations.</span></span> <span data-ttu-id="a5fa4-111">只要用戶端參考開啟的控制碼，它就會在開啟內容控制碼時，傳送從伺服器收到的大量數位。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-111">Whenever the client refers to an opened handle, it sends the large number it received from the server when that context handle was opened.</span></span>

<span data-ttu-id="a5fa4-112">伺服器會持續追蹤傳送至用戶端的所有大型數位。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-112">The server keeps track of all large numbers it sends to a client.</span></span> <span data-ttu-id="a5fa4-113">當伺服器收到代表內容控制碼的大量數位時，它會在集合中查閱該用戶端的有效、未完成內容控制碼的數目，並尋找對應至指定之大型數位的伺服器端內容。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-113">When the server receives a large number representing a context handle, it looks up the number in the collection of valid, outstanding context handles for that client, and finds the server-side context corresponding to a given large number.</span></span> <span data-ttu-id="a5fa4-114">這會傳遞至伺服器常式。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-114">This is passed to the server routine.</span></span> <span data-ttu-id="a5fa4-115">如果找不到大型數位，則 \_ \_ 會引發 RPC X SS \_ 內容不相符例外狀況，並將其 \_ 傳播至用戶端。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-115">If the large number is not found, an RPC\_X\_SS\_CONTEXT\_MISMATCH exception is raised and propagated to the client.</span></span>

<span data-ttu-id="a5fa4-116">此設計的 corollaries 如下所示：</span><span class="sxs-lookup"><span data-stu-id="a5fa4-116">The corollaries of this design are as follows:</span></span>

-   <span data-ttu-id="a5fa4-117">內容控制碼只在現有用戶端/伺服器會話的內容中有效。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-117">A context handle is valid only in the context of the existing client/server session.</span></span> <span data-ttu-id="a5fa4-118">它無法傳遞給另一個用戶端。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-118">It cannot be passed to another client.</span></span>
-   <span data-ttu-id="a5fa4-119">如果伺服器重新開機，或失去與用戶端的連線，則內容控制碼會變成無效。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-119">A context handle becomes invalid if the server is rebooted, or otherwise loses its connection to the client.</span></span>
-   <span data-ttu-id="a5fa4-120">用戶端無法解讀伺服器上內容控制碼所代表的內容。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-120">The client cannot interpret what the context handle represents on the server.</span></span> <span data-ttu-id="a5fa4-121">對用戶端而言，所有內容控制碼只是很大的數位。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-121">To a client, all context handles are simply large numbers.</span></span>

<span data-ttu-id="a5fa4-122">如果用戶端失敗，伺服器將會收到通知，並使用執行下機制來清除其內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="a5fa4-122">If the client fails, the server will get a notification and will clean up its context handles using the run-down mechanism.</span></span>

 

 




