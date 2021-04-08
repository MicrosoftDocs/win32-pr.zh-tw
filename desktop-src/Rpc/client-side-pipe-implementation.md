---
title: Client-Side 管道執行
description: 遠端程序呼叫中的用戶端管道執行 (RPC) 。
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5666656f1f7296c252395255c17902a91cb32a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840568"
---
# <a name="client-side-pipe-implementation"></a><span data-ttu-id="0c35a-103">Client-Side 管道執行</span><span class="sxs-lookup"><span data-stu-id="0c35a-103">Client-Side Pipe Implementation</span></span>

<span data-ttu-id="0c35a-104">用戶端應用程式必須執行下列程式，用戶端 stub 會在資料傳輸期間呼叫這些程式：</span><span class="sxs-lookup"><span data-stu-id="0c35a-104">The client application must implement the following procedures, which the client stub will call during data transfer:</span></span>

-   <span data-ttu-id="0c35a-105">輸入管道 (的提取程式) </span><span class="sxs-lookup"><span data-stu-id="0c35a-105">A pull procedure (for an input pipe)</span></span>
-   <span data-ttu-id="0c35a-106">輸出管道 (的推送程式) </span><span class="sxs-lookup"><span data-stu-id="0c35a-106">A push procedure (for an output pipe)</span></span>
-   <span data-ttu-id="0c35a-107">配置傳送資料緩衝區的配置程式</span><span class="sxs-lookup"><span data-stu-id="0c35a-107">An alloc procedure to allocate a buffer for the transfer data</span></span>

<span data-ttu-id="0c35a-108">所有這些程式都必須使用由 MIDL 產生的標頭檔所指定的引數。</span><span class="sxs-lookup"><span data-stu-id="0c35a-108">All of these procedures must use the arguments specified by the MIDL-generated header file.</span></span> <span data-ttu-id="0c35a-109">此外，用戶端應用程式必須有狀態變數，才能找出或放置資料的位置。</span><span class="sxs-lookup"><span data-stu-id="0c35a-109">In addition, the client application must have a state variable to identify where to locate or place data.</span></span>

<span data-ttu-id="0c35a-110">配置程式也可以像需要一樣簡單或複雜。</span><span class="sxs-lookup"><span data-stu-id="0c35a-110">The alloc procedure can also be as simple or as complex as needed.</span></span> <span data-ttu-id="0c35a-111">例如，它可以在每次存根呼叫函式時，傳回相同緩衝區的指標，或每次都可以配置不同數量的記憶體。</span><span class="sxs-lookup"><span data-stu-id="0c35a-111">For example, it can return a pointer to the same buffer every time the stub calls the function, or it can allocate a different amount of memory each time.</span></span> <span data-ttu-id="0c35a-112">如果您的資料已經採用適當的格式 (管道元素的陣列，例如) 您可以協調配置程式與提取程式，以配置已經包含資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0c35a-112">If your data is already in the proper form (an array of pipe elements, for example) you can coordinate the alloc procedure with the pull procedure to allocate a buffer that already contains the data.</span></span> <span data-ttu-id="0c35a-113">在這種情況下，您的提取程式可能是空的常式。</span><span class="sxs-lookup"><span data-stu-id="0c35a-113">In that case, your pull procedure could be an empty routine.</span></span>

<span data-ttu-id="0c35a-114">緩衝區配置必須以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="0c35a-114">The buffer allocation must be in bytes.</span></span> <span data-ttu-id="0c35a-115">相反地，推送和提取程式會操作以位元組大小為單位的元素，取決於定義它們的方式。</span><span class="sxs-lookup"><span data-stu-id="0c35a-115">The push and pull procedures, on the other hand, manipulate elements, whose size in bytes depends on how they were defined.</span></span>

<span data-ttu-id="0c35a-116">本節將討論下列各節中輸入和輸出管道的用戶端執行：</span><span class="sxs-lookup"><span data-stu-id="0c35a-116">This section discusses the client implementation of input and output pipes in the following sections:</span></span>

-   [<span data-ttu-id="0c35a-117">在用戶端上執行輸入管道</span><span class="sxs-lookup"><span data-stu-id="0c35a-117">Implementing Input Pipes on the Client</span></span>](implementing-input-pipes-on-the-client.md)
-   [<span data-ttu-id="0c35a-118">在用戶端上執行輸出管道</span><span class="sxs-lookup"><span data-stu-id="0c35a-118">Implementing Output Pipes on the Client</span></span>](implementing-output-pipes-on-the-client.md)

 

 




