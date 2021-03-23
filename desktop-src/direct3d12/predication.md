---
title: 預測
description: Predication 是一項功能，可啟用 GPU 而非 CPU 來決定不繪製、複製或分派物件。
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/20/2020
ms.locfileid: "104548437"
---
# <a name="predication"></a><span data-ttu-id="944f9-103">預測</span><span class="sxs-lookup"><span data-stu-id="944f9-103">Predication</span></span>

<span data-ttu-id="944f9-104">Predication 是一項功能，可啟用 GPU 而非 CPU 來決定不繪製、複製或分派物件。</span><span class="sxs-lookup"><span data-stu-id="944f9-104">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy, or dispatch an object.</span></span>

-   [<span data-ttu-id="944f9-105">概觀</span><span class="sxs-lookup"><span data-stu-id="944f9-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="944f9-106">SetPredication</span><span class="sxs-lookup"><span data-stu-id="944f9-106">SetPredication</span></span>](#setpredication)
-   [<span data-ttu-id="944f9-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="944f9-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="944f9-108">概觀</span><span class="sxs-lookup"><span data-stu-id="944f9-108">Overview</span></span>

<span data-ttu-id="944f9-109">Predication 的一般用途是使用遮蔽;如果有繪製周框方塊，且 pixels occluded，在繪製物件本身時顯然沒有任何點。</span><span class="sxs-lookup"><span data-stu-id="944f9-109">The typical use of predication is with occlusion; if a bounding box is drawn and is occluded, there is obviously no point in drawing the object itself.</span></span> <span data-ttu-id="944f9-110">在這種情況下，物件的繪圖可以是 "前提"，以便從 GPU 的實際轉譯中移除它。</span><span class="sxs-lookup"><span data-stu-id="944f9-110">In this situation, the drawing of the object can be "predicated", enabling its removal from actual rendering by the GPU.</span></span>

<span data-ttu-id="944f9-111">一開始，這看起來可能會備援超過標準深度測試，再加上深度通過。</span><span class="sxs-lookup"><span data-stu-id="944f9-111">At first, this might seem redudant over and above the standard depth test plus an early depth pass.</span></span> <span data-ttu-id="944f9-112">但是 predication 可以移除 draw 命令狀態本身的額外負荷，加上點陣化。</span><span class="sxs-lookup"><span data-stu-id="944f9-112">But predication can remove the overhead of the draw command state itself, plus the rasterization.</span></span> <span data-ttu-id="944f9-113">雖然深度傳遞會移除不必要的圖元，但它仍然可以執行頂點、輪廓、網域和幾何著色器，並叫用固定函式的輸入組合語言、tesselator 和轉譯器。</span><span class="sxs-lookup"><span data-stu-id="944f9-113">While an early depth pass removes unnecessary pixels, it can still execute vertex, hull, domain, and geometry shaders, and invoke the fixed-function input assembler, tesselator, and rasterizer.</span></span> <span data-ttu-id="944f9-114">藉由繪製簡單的周框方塊或類似的周框， &mdash; 比實際模型更容易處理和點陣化， &mdash; 您可以避免不必要的點陣化和處理。</span><span class="sxs-lookup"><span data-stu-id="944f9-114">By drawing a simple bounding box or similar bounding volume&mdash;which is simpler to process and rasterize than the real model&mdash;you avoid unnecessary rasterization and processing.</span></span>

<span data-ttu-id="944f9-115">與 Direct3D 11 不同的是，predication 會從查詢分離出來，並在 Direct3D 12 中擴充，以根據應用程式開發人員可能 (決定的任何推理來啟用述詞物件，而不只是遮蔽) 。</span><span class="sxs-lookup"><span data-stu-id="944f9-115">Unlike Direct3D 11, predication is decoupled from queries, and is expanded in Direct3D 12 to enable an application to predicate objects based on any reasoning the app developer may decide on (not just occlusion).</span></span>

## <a name="setpredication"></a><span data-ttu-id="944f9-116">SetPredication</span><span class="sxs-lookup"><span data-stu-id="944f9-116">SetPredication</span></span>

<span data-ttu-id="944f9-117">Predication 可以根據緩衝區內64位的值來設定 (請參閱 [**D3D12 \_ Predication \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)) 。</span><span class="sxs-lookup"><span data-stu-id="944f9-117">Predication can be set based on the value of 64-bits within a buffer (refer to [**D3D12\_PREDICATION\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).</span></span>

<span data-ttu-id="944f9-118">當 GPU 執行 [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) 命令時，它會在緩衝區中貼上值。</span><span class="sxs-lookup"><span data-stu-id="944f9-118">When the GPU executes a [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) command it snaps the value in the buffer.</span></span> <span data-ttu-id="944f9-119">未來對緩衝區中資料所做的變更不會追溯影響 predication 狀態。</span><span class="sxs-lookup"><span data-stu-id="944f9-119">Future changes to the data in the buffer do not retroactively affect the predication state.</span></span>

<span data-ttu-id="944f9-120">如果輸入參數緩衝區為 Null，則會停用 predication。</span><span class="sxs-lookup"><span data-stu-id="944f9-120">If the input parameter Buffer is NULL, then predication is disabled.</span></span>

<span data-ttu-id="944f9-121">Direct3D 12 API 中不會有 Predication 提示;直接、計算和複製命令清單可以使用和 predication。</span><span class="sxs-lookup"><span data-stu-id="944f9-121">Predication hints are not present in the Direct3D 12 API; and predication is allowed on direct, compute, and copy command lists.</span></span> <span data-ttu-id="944f9-122">來源緩衝區可以是任何堆積類型 (預設、上傳、readback、自訂) 。</span><span class="sxs-lookup"><span data-stu-id="944f9-122">The source buffer can be in any heap type (default, upload, readback, custom).</span></span>

<span data-ttu-id="944f9-123">核心執行時間會驗證下列各項：</span><span class="sxs-lookup"><span data-stu-id="944f9-123">The core runtime will validate the following:</span></span>

-   <span data-ttu-id="944f9-124">*AlignedBufferOffset* 是8個位元組的倍數</span><span class="sxs-lookup"><span data-stu-id="944f9-124">*AlignedBufferOffset* is a multiple of 8 bytes</span></span>
-   <span data-ttu-id="944f9-125">資源是緩衝區</span><span class="sxs-lookup"><span data-stu-id="944f9-125">The resource is a buffer</span></span>
-   <span data-ttu-id="944f9-126">作業是列舉的有效成員</span><span class="sxs-lookup"><span data-stu-id="944f9-126">The operation is a valid member of the enumeration</span></span>
-   <span data-ttu-id="944f9-127">無法從組合內呼叫 [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)</span><span class="sxs-lookup"><span data-stu-id="944f9-127">[**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) cannot be called from within a bundle</span></span>
-   <span data-ttu-id="944f9-128">命令清單類型支援 predication</span><span class="sxs-lookup"><span data-stu-id="944f9-128">The command list type supports predication</span></span>
-   <span data-ttu-id="944f9-129">位移不超過緩衝區大小</span><span class="sxs-lookup"><span data-stu-id="944f9-129">The offset does not exceed the buffer size</span></span>

<span data-ttu-id="944f9-130">如果來源緩衝區不在與 [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)相同的 [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (，而且只是) 狀態的別名，debug 層將會發出錯誤。</span><span class="sxs-lookup"><span data-stu-id="944f9-130">The debug layer will issue an error if the source buffer is not in the [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (which is the same as [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states), and simply an alias) state.</span></span>

<span data-ttu-id="944f9-131">可以前提的一組作業如下：</span><span class="sxs-lookup"><span data-stu-id="944f9-131">The set of operations which can be predicated are:</span></span>

-   [<span data-ttu-id="944f9-132">**DrawInstanced**</span><span class="sxs-lookup"><span data-stu-id="944f9-132">**DrawInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [<span data-ttu-id="944f9-133">**DrawIndexedInstanced**</span><span class="sxs-lookup"><span data-stu-id="944f9-133">**DrawIndexedInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [<span data-ttu-id="944f9-134">**分派**</span><span class="sxs-lookup"><span data-stu-id="944f9-134">**Dispatch**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="944f9-135">**CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="944f9-135">**CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="944f9-136">**CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="944f9-136">**CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="944f9-137">**CopyResource**</span><span class="sxs-lookup"><span data-stu-id="944f9-137">**CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="944f9-138">**CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="944f9-138">**CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="944f9-139">**ResolveSubresource**</span><span class="sxs-lookup"><span data-stu-id="944f9-139">**ResolveSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [<span data-ttu-id="944f9-140">**ClearDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="944f9-140">**ClearDepthStencilView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [<span data-ttu-id="944f9-141">**ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="944f9-141">**ClearRenderTargetView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [<span data-ttu-id="944f9-142">**ClearUnorderedAccessViewUint**</span><span class="sxs-lookup"><span data-stu-id="944f9-142">**ClearUnorderedAccessViewUint**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="944f9-143">**ClearUnorderedAccessViewFloat**</span><span class="sxs-lookup"><span data-stu-id="944f9-143">**ClearUnorderedAccessViewFloat**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="944f9-144">**ExecuteIndirect**</span><span class="sxs-lookup"><span data-stu-id="944f9-144">**ExecuteIndirect**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

<span data-ttu-id="944f9-145">[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) 不是前提本身。</span><span class="sxs-lookup"><span data-stu-id="944f9-145">[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) is not predicated itself.</span></span> <span data-ttu-id="944f9-146">相反地，上述清單中包含在組合內的個別作業會前提。</span><span class="sxs-lookup"><span data-stu-id="944f9-146">Instead, individual operations from the list above which are contained in side of the bundle are predicated.</span></span>

<span data-ttu-id="944f9-147">ID3D12GraphicsCommandList 方法 [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)、 [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 和 [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) 不會前提。</span><span class="sxs-lookup"><span data-stu-id="944f9-147">The ID3D12GraphicsCommandList methods [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) and [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) are not predicated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="944f9-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="944f9-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="944f9-149">計數器和查詢</span><span class="sxs-lookup"><span data-stu-id="944f9-149">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="944f9-150">效能測量</span><span class="sxs-lookup"><span data-stu-id="944f9-150">Performance Measurement</span></span>](performance-measurement.md)
</dt> <dt>

[<span data-ttu-id="944f9-151">Predication 查詢逐步解說</span><span class="sxs-lookup"><span data-stu-id="944f9-151">Predication queries walk-through</span></span>](predication-queries.md)
</dt> </dl>

 

 




