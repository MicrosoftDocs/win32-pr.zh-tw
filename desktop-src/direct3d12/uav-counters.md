---
title: UAV 計數器
description: 您可以使用未排序的存取-view (UAV) 計數器，將32位不可部分完成的計數器與未排序的存取權 (UAV) 產生關聯。
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: 94bc1492e3b984d96c76788430d2e63c0672ca76
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104548385"
---
# <a name="uav-counters"></a><span data-ttu-id="855e5-103">UAV 計數器</span><span class="sxs-lookup"><span data-stu-id="855e5-103">UAV Counters</span></span>
<span data-ttu-id="855e5-104">您可以使用未排序的存取-view (UAV) 計數器，將32位不可部分完成的計數器與未排序的存取權 (UAV) 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="855e5-104">You can use unordered-access-view (UAV) counters to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span>

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="855e5-105">從 Direct3D 11 UAV 至 Direct3D 12 的計數器差異</span><span class="sxs-lookup"><span data-stu-id="855e5-105">Differences in UAV counters from Direct3D 11 to Direct3D 12</span></span>
<span data-ttu-id="855e5-106">Direct3D 12 應用程式和 Direct3D 11 應用程式都使用相同的高階著色器語言 (HLSL) 著色器函數來存取 UAV 計數器。</span><span class="sxs-lookup"><span data-stu-id="855e5-106">Direct3D 12 apps and Direct3D 11 apps both use the same high-level shader language (HLSL) shader functions to access the UAV counters.</span></span>

-   <span data-ttu-id="855e5-107">**IncrementCounter**</span><span class="sxs-lookup"><span data-stu-id="855e5-107">**IncrementCounter**</span></span>
-   <span data-ttu-id="855e5-108">**DecrementCounter**</span><span class="sxs-lookup"><span data-stu-id="855e5-108">**DecrementCounter**</span></span>
-   <span data-ttu-id="855e5-109">**Append**</span><span class="sxs-lookup"><span data-stu-id="855e5-109">**Append**</span></span>
-   <span data-ttu-id="855e5-110">**取用**</span><span class="sxs-lookup"><span data-stu-id="855e5-110">**Consume**</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="855e5-111">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="855e5-111">Direct3D 12</span></span>
<span data-ttu-id="855e5-112">在 Direct3D 12 中，32位值是由應用程式佈建，因此，CPU 或 GPU 可以讀取和寫入32位值，就像任何其他 Direct3D 12 資源一樣。</span><span class="sxs-lookup"><span data-stu-id="855e5-112">In Direct3D 12, the 32-bit values are allocated by the application, so the 32-bit values can be read and written by either the CPU or the GPU, just like any other Direct3D 12 resource.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="855e5-113">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="855e5-113">Direct3D 11</span></span>
<span data-ttu-id="855e5-114">在著色器之外，使用 Direct3D 11 需要呼叫 API 方法才能存取計數器 (例如 [>id3d11devicecoNtext：： CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)) 。</span><span class="sxs-lookup"><span data-stu-id="855e5-114">Outside of the shaders, with Direct3D 11 you need to call API methods in order to access the counters (for example, [ID3D11DeviceContext::CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).</span></span>

## <a name="using-uav-counters"></a><span data-ttu-id="855e5-115">使用 UAV 計數器</span><span class="sxs-lookup"><span data-stu-id="855e5-115">Using UAV counters</span></span>
<span data-ttu-id="855e5-116">您的應用程式會負責為 UAV 計數器配置32位的儲存體。</span><span class="sxs-lookup"><span data-stu-id="855e5-116">Your app is responsible for allocating 32-bits of storage for UAV counters.</span></span> <span data-ttu-id="855e5-117">此儲存體可以配置在不同的資源中，因為其中包含可透過 UAV 存取的資料。</span><span class="sxs-lookup"><span data-stu-id="855e5-117">This storage can be allocated in a different resource as the one that contains data accessible via the UAV.</span></span>

<span data-ttu-id="855e5-118">請參閱 [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)、 [**D3D12 \_ Buffer \_ UAV \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) 和 [**D3D12 \_ BUFFER \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav)。</span><span class="sxs-lookup"><span data-stu-id="855e5-118">Refer to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12\_BUFFER\_UAV\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) and [**D3D12\_BUFFER\_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).</span></span>

<span data-ttu-id="855e5-119">如果在 [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)的呼叫中指定 *pCounterResource* ，則會有與 UAV 相關聯的計數器。</span><span class="sxs-lookup"><span data-stu-id="855e5-119">If *pCounterResource* is specified in the call to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), then there is a counter associated with the UAV.</span></span> <span data-ttu-id="855e5-120">在此案例中：</span><span class="sxs-lookup"><span data-stu-id="855e5-120">In this case:</span></span>

-   <span data-ttu-id="855e5-121">*StructureByteStride* 必須大於零</span><span class="sxs-lookup"><span data-stu-id="855e5-121">*StructureByteStride* must be greater than zero</span></span>
-   <span data-ttu-id="855e5-122">格式必須為未知的 DXGI \_ 格式 \_</span><span class="sxs-lookup"><span data-stu-id="855e5-122">Format must be DXGI\_FORMAT\_UNKNOWN</span></span>
-   <span data-ttu-id="855e5-123">不得設定原始旗標</span><span class="sxs-lookup"><span data-stu-id="855e5-123">The RAW flag must not be set</span></span>
-   <span data-ttu-id="855e5-124">這兩個資源都必須是緩衝區</span><span class="sxs-lookup"><span data-stu-id="855e5-124">Both of the resources must be buffers</span></span>
-   <span data-ttu-id="855e5-125">*CounterOffsetInBytes* 必須是4個位元組的倍數</span><span class="sxs-lookup"><span data-stu-id="855e5-125">*CounterOffsetInBytes* must be a multiple of 4 bytes</span></span>
-   <span data-ttu-id="855e5-126">*CounterOffsetInBytes* 必須在計數器資源的範圍內</span><span class="sxs-lookup"><span data-stu-id="855e5-126">*CounterOffsetInBytes* must be within the range of the counter resource</span></span>
-   <span data-ttu-id="855e5-127">*pDesc* 不可為 Null</span><span class="sxs-lookup"><span data-stu-id="855e5-127">*pDesc* cannot be NULL</span></span>
-   <span data-ttu-id="855e5-128">*pResource* 不可為 Null</span><span class="sxs-lookup"><span data-stu-id="855e5-128">*pResource* cannot be NULL</span></span>

<span data-ttu-id="855e5-129">並注意下列使用案例：</span><span class="sxs-lookup"><span data-stu-id="855e5-129">And note the following use cases:</span></span>

-   <span data-ttu-id="855e5-130">如果未指定 *pCounterResource* ，則 *CounterOffsetInBytes* 必須為0。</span><span class="sxs-lookup"><span data-stu-id="855e5-130">If *pCounterResource* is not specified, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="855e5-131">如果已設定原始旗標，則格式必須為 DXGI \_ 格式 \_ R32 無格式 \_ ，而且 UAV 資源必須是緩衝區。</span><span class="sxs-lookup"><span data-stu-id="855e5-131">If the RAW flag is set then the format must be DXGI\_FORMAT\_R32\_TYPELESS and the UAV resource must be a buffer.</span></span>
-   <span data-ttu-id="855e5-132">如果未設定 *pCounterResource* ，則 *CounterOffsetInBytes* 必須為0。</span><span class="sxs-lookup"><span data-stu-id="855e5-132">If *pCounterResource* is not set, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="855e5-133">如果未設定 RAW 旗標，且 *StructureByteStride* = 0，則格式必須是有效的 UAV 格式。</span><span class="sxs-lookup"><span data-stu-id="855e5-133">If the RAW flag is not set and *StructureByteStride* = 0, then the format must be a valid UAV format.</span></span>

<span data-ttu-id="855e5-134">Direct3D 12 會移除附加和計數器 UAVs (之間的差異，不過 HLSL 位元組碼) 中仍然存在差異。</span><span class="sxs-lookup"><span data-stu-id="855e5-134">Direct3D 12 removes the distinction between append and counter UAVs (although the distinction still exists in HLSL bytecode).</span></span>

<span data-ttu-id="855e5-135">核心執行時間會在 [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)內驗證這些限制。</span><span class="sxs-lookup"><span data-stu-id="855e5-135">The core runtime will validate these restrictions inside of [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span></span>

<span data-ttu-id="855e5-136">在繪製/分派期間，計數器資源必須處於狀態 [**D3D12 \_ 資源狀態的 \_ 未 \_ 排序 \_ 存取**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)。</span><span class="sxs-lookup"><span data-stu-id="855e5-136">During Draw/Dispatch, the counter resource must be in the state [**D3D12\_RESOURCE\_STATE\_UNORDERED\_ACCESS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).</span></span> <span data-ttu-id="855e5-137">此外，在單一繪製/分派呼叫中，應用程式會透過兩個不同的 UAV 計數器來存取相同的32位記憶體位置，這是不正確。</span><span class="sxs-lookup"><span data-stu-id="855e5-137">Also, within a single Draw/Dispatch call, it is invalid for an application to access the same 32-bit memory location via two separate UAV counters.</span></span> <span data-ttu-id="855e5-138">如果偵測到其中一個錯誤，debug 層將會發出錯誤。</span><span class="sxs-lookup"><span data-stu-id="855e5-138">The debug layer will issue errors if either of these is detected.</span></span>

<span data-ttu-id="855e5-139">沒有 "SetUnorderedAccessViewCounterValue" 或 "CopyStructureCount" 方法，因為應用程式可以直接將資料複製到計數器值或從中複製資料。</span><span class="sxs-lookup"><span data-stu-id="855e5-139">There are no "SetUnorderedAccessViewCounterValue" or "CopyStructureCount" methods because apps can simply copy data to and from the counter value directly.</span></span>

<span data-ttu-id="855e5-140">支援使用計數器的 UAVs 動態索引。</span><span class="sxs-lookup"><span data-stu-id="855e5-140">Dynamic indexing of UAVs with counters is supported.</span></span>

<span data-ttu-id="855e5-141">如果著色器嘗試存取沒有相關聯計數器之 UAV 的計數器，則調試層會發出警告，而且會發生 GPU 分頁錯誤，導致移除應用程式的裝置。</span><span class="sxs-lookup"><span data-stu-id="855e5-141">If a shader attempts to access the counter of a UAV that does not have an associated counter, then the debug layer will issue a warning, and a GPU page fault will occur causing the apps’s device to be removed.</span></span>

<span data-ttu-id="855e5-142">所有堆積類型都支援 UAV 計數器 (預設、上傳、readback) 。</span><span class="sxs-lookup"><span data-stu-id="855e5-142">UAV counters are supported in all heap types (default, upload, readback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="855e5-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="855e5-143">Related topics</span></span>

* [<span data-ttu-id="855e5-144">計數器和查詢</span><span class="sxs-lookup"><span data-stu-id="855e5-144">Counters and queries</span></span>](counters-and-queries.md)