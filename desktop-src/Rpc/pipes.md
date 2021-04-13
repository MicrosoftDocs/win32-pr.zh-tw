---
title: " (RPC) 的管道"
description: 管道型別函式是一種非常有效率的機制，可傳遞大量資料，或一次無法在記憶體中使用的任何資料數量。
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- 遠端程序呼叫 RPC、描述、管道
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c670b51dfe634fb5b3318e0a0b8a796cfbf988
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464080"
---
# <a name="pipes-rpc"></a><span data-ttu-id="93805-104"> (RPC) 的管道</span><span class="sxs-lookup"><span data-stu-id="93805-104">Pipes (RPC)</span></span>

<span data-ttu-id="93805-105">管道型別函式是一種非常有效率的機制，可傳遞大量資料，或一次無法在記憶體中使用的任何資料數量。</span><span class="sxs-lookup"><span data-stu-id="93805-105">The pipe type constructor is a highly efficient mechanism for passing large amounts of data, or any quantity of data that is not all available in memory at one time.</span></span> <span data-ttu-id="93805-106">藉由使用管道，RPC 執行時間會處理實際的資料傳輸，消除與重複遠端程序呼叫相關聯的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="93805-106">By using a pipe, RPC run time handles the actual data transfer, eliminating the overhead associated with repeated remote procedure calls.</span></span>

<span data-ttu-id="93805-107">用戶端叫用具有管道參數的遠端程式之後，用戶端和伺服器會進入迴圈來傳送資料。</span><span class="sxs-lookup"><span data-stu-id="93805-107">After a client invokes a remote procedure that has a pipe parameter, the client and server enter loops to transfer data.</span></span> <span data-ttu-id="93805-108">資料可以在用戶端或伺服器上產生。</span><span class="sxs-lookup"><span data-stu-id="93805-108">The data can be produced on the client or the server.</span></span> <span data-ttu-id="93805-109">無論何種方式， (位元組的資料量（以位元組為) 單位）都不需要事先知道。</span><span class="sxs-lookup"><span data-stu-id="93805-109">Either way, the amount of data (in bytes) does not have to be known in advance.</span></span> <span data-ttu-id="93805-110">您可以用累加方式產生或取用資料。</span><span class="sxs-lookup"><span data-stu-id="93805-110">The data can be produced or consumed incrementally.</span></span> <span data-ttu-id="93805-111">在資料傳輸迴圈中，伺服器會呼叫載入或卸載資料緩衝區的存根常式。</span><span class="sxs-lookup"><span data-stu-id="93805-111">While in the data-transfer loop, the server calls stub routines that load or unload a buffer of data.</span></span> <span data-ttu-id="93805-112">用戶端會呼叫程式設計人員定義的程式，以配置緩衝區、將資料載入至緩衝區以及從中卸載資料。</span><span class="sxs-lookup"><span data-stu-id="93805-112">The client calls programmer-defined procedures to allocate buffers, load data into and unload data from the buffers.</span></span>

<span data-ttu-id="93805-113">本節提供使用管道進行遠端程序呼叫的總覽。</span><span class="sxs-lookup"><span data-stu-id="93805-113">This section provides an overview of using pipes for remote procedure calls.</span></span> <span data-ttu-id="93805-114">本主題提供下列主題的總覽：</span><span class="sxs-lookup"><span data-stu-id="93805-114">It presents the overview in the following topics:</span></span>

-   [<span data-ttu-id="93805-115">基本管道術語</span><span class="sxs-lookup"><span data-stu-id="93805-115">Essential Pipe Terminology</span></span>](essential-pipe-terminology.md)
-   [<span data-ttu-id="93805-116">管道狀態</span><span class="sxs-lookup"><span data-stu-id="93805-116">The Pipe State</span></span>](the-pipe-state.md)
-   [<span data-ttu-id="93805-117">在 IDL 檔案中定義管道</span><span class="sxs-lookup"><span data-stu-id="93805-117">Defining Pipes in IDL Files</span></span>](defining-pipes-in-idl-files.md)
-   [<span data-ttu-id="93805-118">用戶端管道執行</span><span class="sxs-lookup"><span data-stu-id="93805-118">Client-Side Pipe Implementation</span></span>](client-side-pipe-implementation.md)
-   [<span data-ttu-id="93805-119">伺服器端管道執行</span><span class="sxs-lookup"><span data-stu-id="93805-119">Server-Side Pipe Implementation</span></span>](server-side-pipe-implementation.md)
-   [<span data-ttu-id="93805-120">多個管道的規則</span><span class="sxs-lookup"><span data-stu-id="93805-120">Rules for Multiple Pipes</span></span>](rules-for-multiple-pipes.md)
-   [<span data-ttu-id="93805-121">結合管道和 Nonpipe 參數</span><span class="sxs-lookup"><span data-stu-id="93805-121">Combining Pipe and Nonpipe Parameters</span></span>](combining-pipe-and-nonpipe-parameters.md)

<span data-ttu-id="93805-122">如需管道語法和限制的詳細資訊，請參閱 MIDL 語言參考中的 [管道](/windows/desktop/Midl/pipe) 。</span><span class="sxs-lookup"><span data-stu-id="93805-122">For more information on pipe syntax and restrictions, see [pipe](/windows/desktop/Midl/pipe) in the MIDL Language Reference.</span></span> <span data-ttu-id="93805-123">平臺軟體發展工具組中的管道範例程式 (SDK) 範例 \\ rpc 目錄示範如何在用戶端與伺服器之間傳輸資料 **\[ ，以在中使用 in、out \]** 管道。</span><span class="sxs-lookup"><span data-stu-id="93805-123">The PIPES sample program in the Platform Software Development Kit (SDK) samples\\rpc directory demonstrates how to use **\[in,out\]** pipes to transfer data between a client and a server.</span></span>

 

 
