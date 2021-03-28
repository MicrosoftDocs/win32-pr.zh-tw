---
title: 立即和延後轉譯
description: Direct3D 11 支援兩種類型的轉譯立即和延後。 兩者都是使用 >id3d11devicecoNtext 介面來執行。
ms.assetid: 8991be9f-c882-4752-9048-704fe4ae1725
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef954a8e794755e1405c8e1e07505a5f39189b03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990634"
---
# <a name="immediate-and-deferred-rendering"></a><span data-ttu-id="d5f7d-104">立即和延後轉譯</span><span class="sxs-lookup"><span data-stu-id="d5f7d-104">Immediate and Deferred Rendering</span></span>

<span data-ttu-id="d5f7d-105">Direct3D 11 支援兩種轉譯類型：立即和延後。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-105">Direct3D 11 supports two types of rendering: immediate and deferred.</span></span> <span data-ttu-id="d5f7d-106">兩者都是使用 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 介面來執行。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-106">Both are implemented by using the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span>

## <a name="immediate-rendering"></a><span data-ttu-id="d5f7d-107">立即轉譯</span><span class="sxs-lookup"><span data-stu-id="d5f7d-107">Immediate Rendering</span></span>

<span data-ttu-id="d5f7d-108">立即轉譯是指從裝置呼叫轉譯 Api 或命令，這會將緩衝區中的命令排入佇列以在 GPU 上執行。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-108">Immediate rendering refers to calling rendering APIs or commands from a device, which queues the commands in a buffer for execution on the GPU.</span></span> <span data-ttu-id="d5f7d-109">使用立即內容來呈現、設定管線狀態，以及播放命令清單。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-109">Use an immediate context to render, set pipeline state, and play back a command list.</span></span>

<span data-ttu-id="d5f7d-110">使用 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)建立立即內容。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-110">Create an immediate context using [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>

## <a name="deferred-rendering"></a><span data-ttu-id="d5f7d-111">延後轉譯</span><span class="sxs-lookup"><span data-stu-id="d5f7d-111">Deferred Rendering</span></span>

<span data-ttu-id="d5f7d-112">延後轉譯會在命令緩衝區中記錄圖形命令，讓它們可以在其他時間播放。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-112">Deferred rendering records graphics commands in a command buffer so that they can be played back at some other time.</span></span> <span data-ttu-id="d5f7d-113">使用延後的內容，將命令 (轉譯和狀態設定) 記錄到命令清單中。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-113">Use a deferred context to record commands (rendering as well as state setting) to a command list.</span></span> <span data-ttu-id="d5f7d-114">延遲轉譯是 Direct3D 11 中的新概念;延後轉譯的設計目的是要在錄製命令以在其他執行緒上轉譯時，支援在某個執行緒上轉譯。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-114">Deferred rendering is a new concept in Direct3D 11; deferred rendering is designed to support rendering on one thread while recording commands for rendering on additional threads.</span></span> <span data-ttu-id="d5f7d-115">這種平行的多執行緒策略可讓您將複雜的場景分解成並行工作。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-115">This parallel, multithread strategy allows you to break up complex scenes into concurrent tasks.</span></span> <span data-ttu-id="d5f7d-116">如需呈現複雜場景的詳細資訊，請參閱 [多重傳遞](overviews-direct3d-11-render-multipass.md)轉譯。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-116">For more information about rendering complex scenes, see [Multiple-Pass Rendering](overviews-direct3d-11-render-multipass.md).</span></span>

<span data-ttu-id="d5f7d-117">使用 [**ID3D11Device：： CreateDeferredCoNtext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext)建立延遲的內容。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-117">Create a deferred context using [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

<span data-ttu-id="d5f7d-118">當 Direct3D 在命令緩衝區中將命令排入佇列時，會產生轉譯的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-118">Direct3D generates rendering overhead when it queues up commands in the command buffer.</span></span> <span data-ttu-id="d5f7d-119">相反地， [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md) 在播放期間會更有效率地執行。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-119">In contrast, a [command list](overviews-direct3d-11-render-multi-thread-command-list.md) executes much more efficiently during playback.</span></span> <span data-ttu-id="d5f7d-120">若要使用命令清單，請使用延後內容記錄轉譯命令，並使用立即內容播放這些命令。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-120">To use a command list, record rendering commands with a deferred context and play them back using an immediate context.</span></span>

<span data-ttu-id="d5f7d-121">您只能以單一執行緒的方式產生單一命令清單。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-121">You can generate only a single command list in a single-threaded fashion.</span></span> <span data-ttu-id="d5f7d-122">不過，您可以同時建立和使用多個延遲的內容，每個都在不同的執行緒中。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-122">However, you can create and use multiple deferred contexts simultaneously, each in a separate thread.</span></span> <span data-ttu-id="d5f7d-123">然後，您可以使用多個延遲的內容，同時建立多個命令清單。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-123">Then, you can use those multiple deferred contexts to simultaneously create multiple command lists.</span></span>

<span data-ttu-id="d5f7d-124">您無法在立即內容中同時播放兩個以上的命令清單。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-124">You cannot play back two or more command lists simultaneously on the immediate context.</span></span>

<span data-ttu-id="d5f7d-125">若要判斷裝置內容是否為立即或延遲的內容，請呼叫 [**>id3d11devicecoNtext：： GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gettype)。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-125">To determine if a device context is an immediate or a deferred context, call [**ID3D11DeviceContext::GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gettype).</span></span>

<span data-ttu-id="d5f7d-126">只有在動態資源的延遲內容中才支援 [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) 方法 ([**D3D11 \_ 使用 \_ 動態**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) ，命令清單中的第一個呼叫是 [**D3D11 \_ Map \_ WRITE \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-126">The [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) method is only supported in a deferred context for dynamic resources ([**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) where the first call within the command list is [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map).</span></span> <span data-ttu-id="d5f7d-127">**D3D11 \_如果適用于指定的資源類型，則在後續呼叫上支援對應 \_ 寫入 \_ 不 \_ 覆寫** 。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-127">**D3D11\_MAP\_WRITE\_NO\_OVERWRITE** is supported on subsequent calls if available for the given type of resource.</span></span>

<span data-ttu-id="d5f7d-128">延遲內容中的查詢僅限於資料產生和前提繪圖。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-128">Queries in a deferred context are limited to data generation and predicated drawing.</span></span> <span data-ttu-id="d5f7d-129">您無法在延遲的內容上呼叫 [**>id3d11devicecoNtext：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) ，以取得查詢的相關資料。您只能在立即 **內容上呼叫** 操作資訊，以取得查詢的相關資料。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-129">You cannot call [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) on a deferred context to get data about a query; you can only call **GetData** on the immediate context to get data about a query.</span></span> <span data-ttu-id="d5f7d-130">您可以呼叫 [**D3D11DeviceCoNtext：： SetPredication**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-setpredication) 來設定轉譯述詞 (一類型的) 查詢，以在 GPU 上使用查詢結果。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-130">You can set a rendering predicate (a type of query) by calling [**D3D11DeviceContext::SetPredication**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-setpredication) to use query results on the GPU.</span></span> <span data-ttu-id="d5f7d-131">您可以透過對 [**>id3d11devicecoNtext：： Begin**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-begin) 和 [**>id3d11devicecoNtext：： End**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-end)的呼叫來產生查詢資料。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-131">You can generate query data through calls to [**ID3D11DeviceContext::Begin**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-begin) and [**ID3D11DeviceContext::End**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-end).</span></span> <span data-ttu-id="d5f7d-132">不過，您必須在立即內容上呼叫 [**>id3d11devicecoNtext：： ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) 來提交延後的內容命令清單，查詢資料才能使用。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-132">However, the query data will not be available until you call [**ID3D11DeviceContext::ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) on the immediate context to submit the deferred context command list.</span></span> <span data-ttu-id="d5f7d-133">然後，GPU 會處理查詢資料。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-133">The query data is then processed by the GPU.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5f7d-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="d5f7d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5f7d-135">多執行緒</span><span class="sxs-lookup"><span data-stu-id="d5f7d-135">Multithreading</span></span>](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




