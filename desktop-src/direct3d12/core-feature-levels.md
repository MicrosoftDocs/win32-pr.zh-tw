---
title: Direct3D 12 Core 1.0 功能層級
description: 核心1.0 功能層級是完整的 Direct3D 12 功能集的子集。
ms.topic: article
ms.date: 11/05/2019
ms.openlocfilehash: 42d13b71c516e55ecce378cf9cb415c45e520ba9
ms.sourcegitcommit: bba068130240d16de8a3f3468b7cd72b2cd760f6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/03/2020
ms.locfileid: "106965419"
---
# <a name="the-direct3d-12-core-10-feature-level"></a><span data-ttu-id="c55ba-103">Direct3D 12 Core 1.0 功能層級</span><span class="sxs-lookup"><span data-stu-id="c55ba-103">The Direct3D 12 Core 1.0 Feature Level</span></span>

<span data-ttu-id="c55ba-104">核心1.0 功能層級是完整的 Direct3D 12 功能集的子集。</span><span class="sxs-lookup"><span data-stu-id="c55ba-104">The Core 1.0 Feature Level is a subset of the full Direct3D 12 feature set.</span></span> <span data-ttu-id="c55ba-105">核心1.0 功能等級可以由稱為 *僅限計算裝置* 的裝置類別公開。</span><span class="sxs-lookup"><span data-stu-id="c55ba-105">Core 1.0 Feature Level can be exposed by a category of devices known as *compute-only devices*.</span></span> <span data-ttu-id="c55ba-106">計算專用裝置的整體驅動程式模型是 Microsoft 計算驅動程式模型 (MCDM) 。</span><span class="sxs-lookup"><span data-stu-id="c55ba-106">The overall driver model for compute-only devices is the Microsoft Compute Driver Model (MCDM).</span></span> <span data-ttu-id="c55ba-107">MCDM 是 Windows 設備磁碟機模型的向下調整對等， (WDDM) ，其範圍較大。</span><span class="sxs-lookup"><span data-stu-id="c55ba-107">MCDM is a scaled-down peer of the Windows Device Driver Model (WDDM), which has a larger scope.</span></span>

<span data-ttu-id="c55ba-108">*僅* 支援核心功能等級內功能的裝置稱為 *核心裝置*。</span><span class="sxs-lookup"><span data-stu-id="c55ba-108">A device that supports *only* the features within a Core Feature Level is known as a *Core device*.</span></span>

> [!NOTE]
> <span data-ttu-id="c55ba-109">*僅限計算的裝置*、 *MCDM 裝置*、 *核心功能等級裝置* 和 *核心裝置* 都代表相同的東西。</span><span class="sxs-lookup"><span data-stu-id="c55ba-109">*Compute-only device*, *MCDM device*, *Core Feature Level device*, and *Core device* all mean the same thing.</span></span> <span data-ttu-id="c55ba-110">為了簡單起見，我們偏好使用 *核心裝置* 。</span><span class="sxs-lookup"><span data-stu-id="c55ba-110">We'll prefer *Core device* for simplicity.</span></span>

## <a name="creating-a-core-device"></a><span data-ttu-id="c55ba-111">建立核心裝置</span><span class="sxs-lookup"><span data-stu-id="c55ba-111">Creating a Core device</span></span>

<span data-ttu-id="c55ba-112">一般而言，若要建立 Direct3D 12 裝置，您必須呼叫 [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) 函式，並指定最小功能層級。</span><span class="sxs-lookup"><span data-stu-id="c55ba-112">In general, to create a Direct3D 12 device, you call the [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) function, and specify a minimum feature level.</span></span>

<span data-ttu-id="c55ba-113">如果您指定9到12的功能層級，則傳回的裝置會是功能豐富的裝置，例如傳統的 GPU (，可支援核心裝置) 功能的超集合。</span><span class="sxs-lookup"><span data-stu-id="c55ba-113">If you specify a feature level of 9 through 12, then the device that's returned is a feature-rich device, such as a traditional GPU (which supports a superset of the functionality of a Core device).</span></span> <span data-ttu-id="c55ba-114">這一系列的功能層級絕不會傳回核心裝置。</span><span class="sxs-lookup"><span data-stu-id="c55ba-114">A Core device is never returned for that range of feature levels.</span></span>

<span data-ttu-id="c55ba-115">另一方面，如果您指定核心功能等級 (例如 [**D3D_FEATURE_LEVEL：:D 3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)) ，則傳回的裝置可能會有豐富功能，或可能是核心裝置。</span><span class="sxs-lookup"><span data-stu-id="c55ba-115">On the other hand, if you specify a Core feature level (for example, [**D3D_FEATURE_LEVEL::D3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), then the device that's returned could be feature-rich, or it could be a Core device.</span></span>

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

<span data-ttu-id="c55ba-116">如果您指定 `_CORE` 功能等級，則執行時間/debug 層會驗證該功能層級是否允許您的應用程式所使用的功能 `_CORE` 。</span><span class="sxs-lookup"><span data-stu-id="c55ba-116">If you specify a `_CORE` feature level, then the runtime/debug layer validates that the features your application uses are allowed by that `_CORE` feature level.</span></span> <span data-ttu-id="c55ba-117">本主題稍後會定義這組功能。</span><span class="sxs-lookup"><span data-stu-id="c55ba-117">That set of features is defined later in this topic.</span></span>

## <a name="shader-model-for-core-devices"></a><span data-ttu-id="c55ba-118">核心裝置的著色器模型</span><span class="sxs-lookup"><span data-stu-id="c55ba-118">Shader model for Core devices</span></span>

<span data-ttu-id="c55ba-119">核心裝置支援著色器模型 5.0 +。</span><span class="sxs-lookup"><span data-stu-id="c55ba-119">A Core device supports Shader Model 5.0+.</span></span>

<span data-ttu-id="c55ba-120">執行時間會執行 5. x 非 DXIL 著色器模型至 6.0 DXIL 的轉換。</span><span class="sxs-lookup"><span data-stu-id="c55ba-120">The runtime performs conversion of 5.x non DXIL shader models to 6.0 DXIL.</span></span> <span data-ttu-id="c55ba-121">因此驅動程式只需要支援6.x。</span><span class="sxs-lookup"><span data-stu-id="c55ba-121">So the driver need only support 6.x.</span></span>

## <a name="resource-management-model-for-core-devices"></a><span data-ttu-id="c55ba-122">核心裝置的資源管理模型</span><span class="sxs-lookup"><span data-stu-id="c55ba-122">Resource management model for Core devices</span></span>

- <span data-ttu-id="c55ba-123">支援的資源維度：原始和結構化緩衝區只 (沒有具類型的緩衝區、texture1d/2D 等等 ) </span><span class="sxs-lookup"><span data-stu-id="c55ba-123">Supported resource dimensions: raw and structured buffers only (no typed buffers, texture1d/2D, etc.)</span></span>
- <span data-ttu-id="c55ba-124">不支援保留的 (磚) 資源</span><span class="sxs-lookup"><span data-stu-id="c55ba-124">No support for reserved (tiled) resources</span></span>
- <span data-ttu-id="c55ba-125">不支援自訂堆積</span><span class="sxs-lookup"><span data-stu-id="c55ba-125">No support for custom heaps</span></span>
- <span data-ttu-id="c55ba-126">不支援下列任何堆積旗標：</span><span class="sxs-lookup"><span data-stu-id="c55ba-126">No support for any of these heap flags:</span></span>
  - <span data-ttu-id="c55ba-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span><span class="sxs-lookup"><span data-stu-id="c55ba-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span></span>
  - <span data-ttu-id="c55ba-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span><span class="sxs-lookup"><span data-stu-id="c55ba-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span></span>
  - <span data-ttu-id="c55ba-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span><span class="sxs-lookup"><span data-stu-id="c55ba-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span></span>
  - <span data-ttu-id="c55ba-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (附注著色器 ATOMICS 是必要的，此旗標適用于另一項功能，也就是交叉配接器 ATOMICS) </span><span class="sxs-lookup"><span data-stu-id="c55ba-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (note shader atomics are required, this flag is for another feature, cross adapter atomics)</span></span>

## <a name="resource-binding-model-for-core-devices"></a><span data-ttu-id="c55ba-131">核心裝置的資源系結模型</span><span class="sxs-lookup"><span data-stu-id="c55ba-131">Resource binding model for Core devices</span></span>

- <span data-ttu-id="c55ba-132">僅支援資源系結層1</span><span class="sxs-lookup"><span data-stu-id="c55ba-132">Support for resource binding tier 1 only</span></span>
- <span data-ttu-id="c55ba-133">例外狀況：</span><span class="sxs-lookup"><span data-stu-id="c55ba-133">Exceptions:</span></span>
  - <span data-ttu-id="c55ba-134">不支援材質取樣器</span><span class="sxs-lookup"><span data-stu-id="c55ba-134">No support for texture samplers</span></span>
  - <span data-ttu-id="c55ba-135">支援 64 UAVs，例如功能等級 11.1 + (，而不只是 8) </span><span class="sxs-lookup"><span data-stu-id="c55ba-135">Support for 64 UAVs like Feature Level 11.1+ (as opposed to only 8)</span></span>
  - <span data-ttu-id="c55ba-136">在對資源的著色器存取中，執行不需要透過描述項來執行界限檢查，而超出範圍的存取會產生未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="c55ba-136">Implementations do not have to implement bounds checking on shader accesses to resources through descriptors, out of bounds accesses produce undefined behavior.</span></span>
    - <span data-ttu-id="c55ba-137">做為副產品，不支援根簽章中 D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS 描述項範圍旗標。</span><span class="sxs-lookup"><span data-stu-id="c55ba-137">As a byproduct, the descriptor range flag D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS in root signatures is not supported.</span></span>
- <span data-ttu-id="c55ba-138">UAV/CBV 描述項只能在 (預設堆積的資源上進行，所以沒有上傳/readback 堆積) 。</span><span class="sxs-lookup"><span data-stu-id="c55ba-138">UAV/CBV descriptors can only be made on resources from default heaps (so no upload/readback heaps).</span></span> <span data-ttu-id="c55ba-139">這會強制您的應用程式執行複本，以取得跨 CPU< >GPU 的資料。</span><span class="sxs-lookup"><span data-stu-id="c55ba-139">This forces your application to do copies to get data across CPU<->GPU.</span></span>
- <span data-ttu-id="c55ba-140">儘管是最低的系結功能層級，但仍有一些必要的功能，即使在這一層中也值得呼叫：</span><span class="sxs-lookup"><span data-stu-id="c55ba-140">Despite being the lowest binding capability tier, there are still some features required even in this tier worth calling out:</span></span>
  - <span data-ttu-id="c55ba-141">描述項堆積可以在記錄命令清單之後更新 (請參閱資源系結規格中的 D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE) </span><span class="sxs-lookup"><span data-stu-id="c55ba-141">Descriptor heaps can be updated after command lists are recorded (see D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE in the resource binding spec)</span></span>
  - <span data-ttu-id="c55ba-142">根目錄描述元基本上是 GPUVA 指標</span><span class="sxs-lookup"><span data-stu-id="c55ba-142">Root descriptors are basically GPUVA pointers</span></span>
    - <span data-ttu-id="c55ba-143">即使沒有 MMU/VA 支援，在根描述項中使用的緩衝區 VAs 也可以藉由執行位址修補來模擬。</span><span class="sxs-lookup"><span data-stu-id="c55ba-143">Even though there is no MMU / VA support, buffer VAs that are used in root descriptors can be emulated by implementations by doing address patching.</span></span>

### <a name="structured-buffer-restrictions"></a><span data-ttu-id="c55ba-144">結構化緩衝區限制</span><span class="sxs-lookup"><span data-stu-id="c55ba-144">Structured buffer restrictions</span></span>

<span data-ttu-id="c55ba-145">結構化緩衝區必須有4位元組對齊的基底位址，而跨距必須是2或4的倍數。</span><span class="sxs-lookup"><span data-stu-id="c55ba-145">Structured buffers must have a base address that is 4 byte aligned, and stride must be 2 or a multiple of 4.</span></span> <span data-ttu-id="c55ba-146">2 stride 的案例是針對具有16位資料的應用程式，特別是在 D3D_FEATURE_LEVEL_1_0_CORE 中不支援輸入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c55ba-146">The case for a stride of 2 is for apps with 16 bit data, particularly given there is no support for typed buffers in D3D_FEATURE_LEVEL_1_0_CORE.</span></span>

<span data-ttu-id="c55ba-147">描述項中指定的 stride 必須與 HLSL 中指定的 stride 相符。</span><span class="sxs-lookup"><span data-stu-id="c55ba-147">Stride specified in descriptors must match the stride specified in HLSL.</span></span>  

## <a name="command-queue-support-for-core-devices"></a><span data-ttu-id="c55ba-148">核心裝置的命令佇列支援</span><span class="sxs-lookup"><span data-stu-id="c55ba-148">Command queue support for Core devices</span></span>

<span data-ttu-id="c55ba-149">計算和複製佇列只 (沒有3D、影片等) 的佇列。</span><span class="sxs-lookup"><span data-stu-id="c55ba-149">Compute and copy queues only (no 3D, video, etc. queues).</span></span>

## <a name="shader-support-for-core-devices"></a><span data-ttu-id="c55ba-150">核心裝置的著色器支援</span><span class="sxs-lookup"><span data-stu-id="c55ba-150">Shader support for Core devices</span></span>

<span data-ttu-id="c55ba-151">僅計算著色器，沒有任何圖形著色器 (頂點、圖元著色器等，) 或任何相關的功能，例如呈現目標、交換鏈、輸入組合語言。</span><span class="sxs-lookup"><span data-stu-id="c55ba-151">Compute shaders only, no graphics shaders (Vertex, Pixel Shaders, etc.) nor any related functionality such as render targets, swap chains, input assembler.</span></span>

### <a name="arithmetic-precision"></a><span data-ttu-id="c55ba-152">算術精確度</span><span class="sxs-lookup"><span data-stu-id="c55ba-152">Arithmetic precision</span></span>

<span data-ttu-id="c55ba-153">核心裝置不需要支援16位浮點運算的 denorms。</span><span class="sxs-lookup"><span data-stu-id="c55ba-153">Core devices do not have to support denorms for 16 bit floating point operations.</span></span>

## <a name="supported-apis-for-core-devices"></a><span data-ttu-id="c55ba-154">核心裝置支援的 Api</span><span class="sxs-lookup"><span data-stu-id="c55ba-154">Supported APIs for Core devices</span></span>

<span data-ttu-id="c55ba-155">下列清單代表受支援的完整應用程式開發介面子集 *(不會\*\*在) 中列出核心* 1.0 功能等級所支援的 api。</span><span class="sxs-lookup"><span data-stu-id="c55ba-155">The list below represents the supported subset of the full application programming interface (APIs that are *not* supported in Core 1.0 Feature Level are *not* listed).</span></span>

### <a name="id3d12device-methods"></a><span data-ttu-id="c55ba-156">ID3D12Device 方法</span><span class="sxs-lookup"><span data-stu-id="c55ba-156">ID3D12Device methods</span></span>

* [<span data-ttu-id="c55ba-157">ID3D12Device::CheckFeatureSupport</span><span class="sxs-lookup"><span data-stu-id="c55ba-157">ID3D12Device::CheckFeatureSupport</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [<span data-ttu-id="c55ba-158">ID3D12Device::CopyDescriptors</span><span class="sxs-lookup"><span data-stu-id="c55ba-158">ID3D12Device::CopyDescriptors</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [<span data-ttu-id="c55ba-159">ID3D12Device::CopyDescriptorsSimple</span><span class="sxs-lookup"><span data-stu-id="c55ba-159">ID3D12Device::CopyDescriptorsSimple</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [<span data-ttu-id="c55ba-160">ID3D12Device::CreateCommandAllocator</span><span class="sxs-lookup"><span data-stu-id="c55ba-160">ID3D12Device::CreateCommandAllocator</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [<span data-ttu-id="c55ba-161">ID3D12Device::CreateCommandList</span><span class="sxs-lookup"><span data-stu-id="c55ba-161">ID3D12Device::CreateCommandList</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [<span data-ttu-id="c55ba-162">ID3D12Device::CreateCommandQueue</span><span class="sxs-lookup"><span data-stu-id="c55ba-162">ID3D12Device::CreateCommandQueue</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [<span data-ttu-id="c55ba-163">ID3D12Device::CreateCommandSignature</span><span class="sxs-lookup"><span data-stu-id="c55ba-163">ID3D12Device::CreateCommandSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [<span data-ttu-id="c55ba-164">ID3D12Device::CreateCommittedResource</span><span class="sxs-lookup"><span data-stu-id="c55ba-164">ID3D12Device::CreateCommittedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [<span data-ttu-id="c55ba-165">ID3D12Device::CreateComputePipelineState</span><span class="sxs-lookup"><span data-stu-id="c55ba-165">ID3D12Device::CreateComputePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [<span data-ttu-id="c55ba-166">ID3D12Device::CreateConstantBufferView</span><span class="sxs-lookup"><span data-stu-id="c55ba-166">ID3D12Device::CreateConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [<span data-ttu-id="c55ba-167">ID3D12Device::CreateDescriptorHeap</span><span class="sxs-lookup"><span data-stu-id="c55ba-167">ID3D12Device::CreateDescriptorHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [<span data-ttu-id="c55ba-168">ID3D12Device::CreateFence</span><span class="sxs-lookup"><span data-stu-id="c55ba-168">ID3D12Device::CreateFence</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [<span data-ttu-id="c55ba-169">ID3D12Device::CreateHeap</span><span class="sxs-lookup"><span data-stu-id="c55ba-169">ID3D12Device::CreateHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [<span data-ttu-id="c55ba-170">ID3D12Device::CreatePlacedResource</span><span class="sxs-lookup"><span data-stu-id="c55ba-170">ID3D12Device::CreatePlacedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [<span data-ttu-id="c55ba-171">ID3D12Device::CreateQueryHeap</span><span class="sxs-lookup"><span data-stu-id="c55ba-171">ID3D12Device::CreateQueryHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [<span data-ttu-id="c55ba-172">ID3D12Device::CreateRootSignature</span><span class="sxs-lookup"><span data-stu-id="c55ba-172">ID3D12Device::CreateRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [<span data-ttu-id="c55ba-173">ID3D12Device::CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="c55ba-173">ID3D12Device::CreateShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [<span data-ttu-id="c55ba-174">ID3D12Device::CreateSharedHandle</span><span class="sxs-lookup"><span data-stu-id="c55ba-174">ID3D12Device::CreateSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [<span data-ttu-id="c55ba-175">ID3D12Device::CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="c55ba-175">ID3D12Device::CreateUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [<span data-ttu-id="c55ba-176">ID3D12Device：：收回</span><span class="sxs-lookup"><span data-stu-id="c55ba-176">ID3D12Device::Evict</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [<span data-ttu-id="c55ba-177">ID3D12Device::GetAdapterLuid</span><span class="sxs-lookup"><span data-stu-id="c55ba-177">ID3D12Device::GetAdapterLuid</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [<span data-ttu-id="c55ba-178">ID3D12Device::GetCopyableFootprints</span><span class="sxs-lookup"><span data-stu-id="c55ba-178">ID3D12Device::GetCopyableFootprints</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [<span data-ttu-id="c55ba-179">ID3D12Device::GetCustomHeapProperties</span><span class="sxs-lookup"><span data-stu-id="c55ba-179">ID3D12Device::GetCustomHeapProperties</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [<span data-ttu-id="c55ba-180">ID3D12Device::GetDescriptorHandleIncrementSize</span><span class="sxs-lookup"><span data-stu-id="c55ba-180">ID3D12Device::GetDescriptorHandleIncrementSize</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [<span data-ttu-id="c55ba-181">ID3D12Device::GetDeviceRemovedReason</span><span class="sxs-lookup"><span data-stu-id="c55ba-181">ID3D12Device::GetDeviceRemovedReason</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [<span data-ttu-id="c55ba-182">ID3D12Device::GetNodeCount</span><span class="sxs-lookup"><span data-stu-id="c55ba-182">ID3D12Device::GetNodeCount</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [<span data-ttu-id="c55ba-183">ID3D12Device::GetResourceAllocationInfo</span><span class="sxs-lookup"><span data-stu-id="c55ba-183">ID3D12Device::GetResourceAllocationInfo</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [<span data-ttu-id="c55ba-184">ID3D12Device::MakeResident</span><span class="sxs-lookup"><span data-stu-id="c55ba-184">ID3D12Device::MakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [<span data-ttu-id="c55ba-185">ID3D12Device::OpenSharedHandle</span><span class="sxs-lookup"><span data-stu-id="c55ba-185">ID3D12Device::OpenSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [<span data-ttu-id="c55ba-186">ID3D12Device::OpenSharedHandleByName</span><span class="sxs-lookup"><span data-stu-id="c55ba-186">ID3D12Device::OpenSharedHandleByName</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [<span data-ttu-id="c55ba-187">ID3D12Device::SetStablePowerState</span><span class="sxs-lookup"><span data-stu-id="c55ba-187">ID3D12Device::SetStablePowerState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a><span data-ttu-id="c55ba-188">ID3D12Device1 方法</span><span class="sxs-lookup"><span data-stu-id="c55ba-188">ID3D12Device1 methods</span></span>

* [<span data-ttu-id="c55ba-189">ID3D12Device1::CreatePipelineLibrary</span><span class="sxs-lookup"><span data-stu-id="c55ba-189">ID3D12Device1::CreatePipelineLibrary</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [<span data-ttu-id="c55ba-190">ID3D12Device1::SetEventOnMultipleFenceCompletion</span><span class="sxs-lookup"><span data-stu-id="c55ba-190">ID3D12Device1::SetEventOnMultipleFenceCompletion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [<span data-ttu-id="c55ba-191">ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority</span><span class="sxs-lookup"><span data-stu-id="c55ba-191">ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a><span data-ttu-id="c55ba-192">ID3D12Device2 方法</span><span class="sxs-lookup"><span data-stu-id="c55ba-192">ID3D12Device2 methods</span></span>

* [<span data-ttu-id="c55ba-193">ID3D12Device2::CreatePipelineState</span><span class="sxs-lookup"><span data-stu-id="c55ba-193">ID3D12Device2::CreatePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a><span data-ttu-id="c55ba-194">ID3D12Device3 方法</span><span class="sxs-lookup"><span data-stu-id="c55ba-194">ID3D12Device3 methods</span></span>

* [<span data-ttu-id="c55ba-195">ID3D12Device3::OpenExistingHeapFromAddress</span><span class="sxs-lookup"><span data-stu-id="c55ba-195">ID3D12Device3::OpenExistingHeapFromAddress</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* <span data-ttu-id="c55ba-196">[ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span><span class="sxs-lookup"><span data-stu-id="c55ba-196">[ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span></span>
* [<span data-ttu-id="c55ba-197">ID3D12Device3::EnqueueMakeResident</span><span class="sxs-lookup"><span data-stu-id="c55ba-197">ID3D12Device3::EnqueueMakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a><span data-ttu-id="c55ba-198">ID3D12Device4 方法</span><span class="sxs-lookup"><span data-stu-id="c55ba-198">ID3D12Device4 methods</span></span>

* [<span data-ttu-id="c55ba-199">ID3D12Device4::GetResourceAllocationInfo1</span><span class="sxs-lookup"><span data-stu-id="c55ba-199">ID3D12Device4::GetResourceAllocationInfo1</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a><span data-ttu-id="c55ba-200">ID3D12Device5 方法</span><span class="sxs-lookup"><span data-stu-id="c55ba-200">ID3D12Device5 methods</span></span>

* [<span data-ttu-id="c55ba-201">ID3D12Device5::CreateMetaCommand</span><span class="sxs-lookup"><span data-stu-id="c55ba-201">ID3D12Device5::CreateMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [<span data-ttu-id="c55ba-202">ID3D12Device5::CreateStateObject</span><span class="sxs-lookup"><span data-stu-id="c55ba-202">ID3D12Device5::CreateStateObject</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [<span data-ttu-id="c55ba-203">ID3D12Device5::EnumerateMetaCommandParameters</span><span class="sxs-lookup"><span data-stu-id="c55ba-203">ID3D12Device5::EnumerateMetaCommandParameters</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [<span data-ttu-id="c55ba-204">ID3D12Device5::EnumerateMetaCommands</span><span class="sxs-lookup"><span data-stu-id="c55ba-204">ID3D12Device5::EnumerateMetaCommands</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [<span data-ttu-id="c55ba-205">ID3D12Device5::RemoveDevice</span><span class="sxs-lookup"><span data-stu-id="c55ba-205">ID3D12Device5::RemoveDevice</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a><span data-ttu-id="c55ba-206">ID3D12CommandQueue 方法</span><span class="sxs-lookup"><span data-stu-id="c55ba-206">ID3D12CommandQueue methods</span></span>

* [<span data-ttu-id="c55ba-207">ID3D12CommandQueue::BeginEvent</span><span class="sxs-lookup"><span data-stu-id="c55ba-207">ID3D12CommandQueue::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [<span data-ttu-id="c55ba-208">ID3D12CommandQueue::EndEvent</span><span class="sxs-lookup"><span data-stu-id="c55ba-208">ID3D12CommandQueue::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [<span data-ttu-id="c55ba-209">ID3D12CommandQueue::ExecuteCommandLists</span><span class="sxs-lookup"><span data-stu-id="c55ba-209">ID3D12CommandQueue::ExecuteCommandLists</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [<span data-ttu-id="c55ba-210">ID3D12CommandQueue::GetClockCalibration</span><span class="sxs-lookup"><span data-stu-id="c55ba-210">ID3D12CommandQueue::GetClockCalibration</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [<span data-ttu-id="c55ba-211">ID3D12CommandQueue::GetDesc</span><span class="sxs-lookup"><span data-stu-id="c55ba-211">ID3D12CommandQueue::GetDesc</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [<span data-ttu-id="c55ba-212">ID3D12CommandQueue::GetTimestampFrequency</span><span class="sxs-lookup"><span data-stu-id="c55ba-212">ID3D12CommandQueue::GetTimestampFrequency</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [<span data-ttu-id="c55ba-213">ID3D12CommandQueue::SetMarker</span><span class="sxs-lookup"><span data-stu-id="c55ba-213">ID3D12CommandQueue::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [<span data-ttu-id="c55ba-214">ID3D12CommandQueue：：信號</span><span class="sxs-lookup"><span data-stu-id="c55ba-214">ID3D12CommandQueue::Signal</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [<span data-ttu-id="c55ba-215">ID3D12CommandQueue：： Wait</span><span class="sxs-lookup"><span data-stu-id="c55ba-215">ID3D12CommandQueue::Wait</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a><span data-ttu-id="c55ba-216">ID3D12CommandList 方法</span><span class="sxs-lookup"><span data-stu-id="c55ba-216">ID3D12CommandList methods</span></span>

* [<span data-ttu-id="c55ba-217">ID3D12CommandList：： GetType</span><span class="sxs-lookup"><span data-stu-id="c55ba-217">ID3D12CommandList::GetType</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a><span data-ttu-id="c55ba-218">ID3D12GraphicsCommandList 方法</span><span class="sxs-lookup"><span data-stu-id="c55ba-218">ID3D12GraphicsCommandList methods</span></span>

* [<span data-ttu-id="c55ba-219">ID3D12GraphicsCommandList::BeginEvent</span><span class="sxs-lookup"><span data-stu-id="c55ba-219">ID3D12GraphicsCommandList::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [<span data-ttu-id="c55ba-220">ID3D12GraphicsCommandList::BeginQuery</span><span class="sxs-lookup"><span data-stu-id="c55ba-220">ID3D12GraphicsCommandList::BeginQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [<span data-ttu-id="c55ba-221">ID3D12GraphicsCommandList::ClearState</span><span class="sxs-lookup"><span data-stu-id="c55ba-221">ID3D12GraphicsCommandList::ClearState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [<span data-ttu-id="c55ba-222">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="c55ba-222">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [<span data-ttu-id="c55ba-223">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="c55ba-223">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [<span data-ttu-id="c55ba-224">ID3D12GraphicsCommandList：： Close</span><span class="sxs-lookup"><span data-stu-id="c55ba-224">ID3D12GraphicsCommandList::Close</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [<span data-ttu-id="c55ba-225">ID3D12GraphicsCommandList::CopyBufferRegion</span><span class="sxs-lookup"><span data-stu-id="c55ba-225">ID3D12GraphicsCommandList::CopyBufferRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [<span data-ttu-id="c55ba-226">ID3D12GraphicsCommandList::CopyResource</span><span class="sxs-lookup"><span data-stu-id="c55ba-226">ID3D12GraphicsCommandList::CopyResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [<span data-ttu-id="c55ba-227">ID3D12GraphicsCommandList::CopyTextureRegion</span><span class="sxs-lookup"><span data-stu-id="c55ba-227">ID3D12GraphicsCommandList::CopyTextureRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [<span data-ttu-id="c55ba-228">ID3D12GraphicsCommandList：:D ispatch</span><span class="sxs-lookup"><span data-stu-id="c55ba-228">ID3D12GraphicsCommandList::Dispatch</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [<span data-ttu-id="c55ba-229">ID3D12GraphicsCommandList::EndEvent</span><span class="sxs-lookup"><span data-stu-id="c55ba-229">ID3D12GraphicsCommandList::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [<span data-ttu-id="c55ba-230">ID3D12GraphicsCommandList::EndQuery</span><span class="sxs-lookup"><span data-stu-id="c55ba-230">ID3D12GraphicsCommandList::EndQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [<span data-ttu-id="c55ba-231">ID3D12GraphicsCommandList：： Reset</span><span class="sxs-lookup"><span data-stu-id="c55ba-231">ID3D12GraphicsCommandList::Reset</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [<span data-ttu-id="c55ba-232">ID3D12GraphicsCommandList::ResolveQueryData</span><span class="sxs-lookup"><span data-stu-id="c55ba-232">ID3D12GraphicsCommandList::ResolveQueryData</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [<span data-ttu-id="c55ba-233">ID3D12GraphicsCommandList::ResourceBarrier</span><span class="sxs-lookup"><span data-stu-id="c55ba-233">ID3D12GraphicsCommandList::ResourceBarrier</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [<span data-ttu-id="c55ba-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span><span class="sxs-lookup"><span data-stu-id="c55ba-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [<span data-ttu-id="c55ba-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span><span class="sxs-lookup"><span data-stu-id="c55ba-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [<span data-ttu-id="c55ba-236">ID3D12GraphicsCommandList::SetComputeRootConstantBufferView</span><span class="sxs-lookup"><span data-stu-id="c55ba-236">ID3D12GraphicsCommandList::SetComputeRootConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [<span data-ttu-id="c55ba-237">ID3D12GraphicsCommandList::SetComputeRootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="c55ba-237">ID3D12GraphicsCommandList::SetComputeRootDescriptorTable</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [<span data-ttu-id="c55ba-238">ID3D12GraphicsCommandList::SetComputeRootShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="c55ba-238">ID3D12GraphicsCommandList::SetComputeRootShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [<span data-ttu-id="c55ba-239">ID3D12GraphicsCommandList::SetComputeRootSignature</span><span class="sxs-lookup"><span data-stu-id="c55ba-239">ID3D12GraphicsCommandList::SetComputeRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [<span data-ttu-id="c55ba-240">ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="c55ba-240">ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [<span data-ttu-id="c55ba-241">ID3D12GraphicsCommandList::SetDescriptorHeaps</span><span class="sxs-lookup"><span data-stu-id="c55ba-241">ID3D12GraphicsCommandList::SetDescriptorHeaps</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [<span data-ttu-id="c55ba-242">ID3D12GraphicsCommandList::SetMarker</span><span class="sxs-lookup"><span data-stu-id="c55ba-242">ID3D12GraphicsCommandList::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [<span data-ttu-id="c55ba-243">ID3D12GraphicsCommandList::SetPipelineState</span><span class="sxs-lookup"><span data-stu-id="c55ba-243">ID3D12GraphicsCommandList::SetPipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [<span data-ttu-id="c55ba-244">ID3D12GraphicsCommandList::SetPredication</span><span class="sxs-lookup"><span data-stu-id="c55ba-244">ID3D12GraphicsCommandList::SetPredication</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a><span data-ttu-id="c55ba-245">ID3D12GraphicsCommandList1 方法</span><span class="sxs-lookup"><span data-stu-id="c55ba-245">ID3D12GraphicsCommandList1 methods</span></span>

* [<span data-ttu-id="c55ba-246">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT</span><span class="sxs-lookup"><span data-stu-id="c55ba-246">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [<span data-ttu-id="c55ba-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span><span class="sxs-lookup"><span data-stu-id="c55ba-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a><span data-ttu-id="c55ba-248">ID3D12GraphicsCommandList2 方法</span><span class="sxs-lookup"><span data-stu-id="c55ba-248">ID3D12GraphicsCommandList2 methods</span></span>

* [<span data-ttu-id="c55ba-249">ID3D12GraphicsCommandList2::WriteBufferImmediate</span><span class="sxs-lookup"><span data-stu-id="c55ba-249">ID3D12GraphicsCommandList2::WriteBufferImmediate</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a><span data-ttu-id="c55ba-250">ID3D12GraphicsCommandList4 方法</span><span class="sxs-lookup"><span data-stu-id="c55ba-250">ID3D12GraphicsCommandList4 methods</span></span>

* [<span data-ttu-id="c55ba-251">ID3D12GraphicsCommandList4::ExecuteMetaCommand</span><span class="sxs-lookup"><span data-stu-id="c55ba-251">ID3D12GraphicsCommandList4::ExecuteMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [<span data-ttu-id="c55ba-252">ID3D12GraphicsCommandList4::InitializeMetaCommand</span><span class="sxs-lookup"><span data-stu-id="c55ba-252">ID3D12GraphicsCommandList4::InitializeMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)
