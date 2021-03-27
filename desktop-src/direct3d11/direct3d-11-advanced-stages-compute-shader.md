---
title: 計算著色器總覽
description: 計算著色器是可程式化的著色器階段，可將 Microsoft Direct3D 11 擴充到圖形程式設計之外。 計算著色器技術也稱為 DirectCompute 技術。
ms.assetid: 02c1f98e-fdd6-49b0-b8b2-efbd472ab599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c890e63b468a993e0d08f678d2276d6ce2adad
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "103684221"
---
# <a name="compute-shader-overview"></a><span data-ttu-id="4128c-104">計算著色器總覽</span><span class="sxs-lookup"><span data-stu-id="4128c-104">Compute Shader Overview</span></span>

<span data-ttu-id="4128c-105">計算著色器是可程式化的著色器階段，可將 Microsoft Direct3D 11 擴充到圖形程式設計之外。</span><span class="sxs-lookup"><span data-stu-id="4128c-105">A compute shader is a programmable shader stage that expands Microsoft Direct3D 11 beyond graphics programming.</span></span> <span data-ttu-id="4128c-106">計算著色器技術也稱為 DirectCompute 技術。</span><span class="sxs-lookup"><span data-stu-id="4128c-106">The compute shader technology is also known as the DirectCompute technology.</span></span>

<span data-ttu-id="4128c-107">如同其他可程式化著色器 (頂點和幾何著色器（例如) ），計算著色器是使用 [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) 來設計和執行，但這只是相似性結束的位置。</span><span class="sxs-lookup"><span data-stu-id="4128c-107">Like other programmable shaders (vertex and geometry shaders for example), a compute shader is designed and implemented with [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) but that is just about where the similarity ends.</span></span> <span data-ttu-id="4128c-108">計算著色器提供高速一般用途運算，並且利用了圖形處理器 (GPU) 大量平行處理器的優勢。</span><span class="sxs-lookup"><span data-stu-id="4128c-108">A compute shader provides high-speed general purpose computing and takes advantage of the large numbers of parallel processors on the graphics processing unit (GPU).</span></span> <span data-ttu-id="4128c-109">計算著色器提供了記憶體共用以及執行緒同步功能，讓平行程式設計方法更有效率。</span><span class="sxs-lookup"><span data-stu-id="4128c-109">The compute shader provides memory sharing and thread synchronization features to allow more effective parallel programming methods.</span></span> <span data-ttu-id="4128c-110">您可以呼叫 [**>id3d11devicecoNtext：:D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch) 或 [**>id3d11devicecoNtext：:D ispatchindirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect) 方法，在計算著色器中執行命令。</span><span class="sxs-lookup"><span data-stu-id="4128c-110">You call the [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch) or [**ID3D11DeviceContext::DispatchIndirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect) method to execute commands in a compute shader.</span></span> <span data-ttu-id="4128c-111">計算著色器可在許多執行緒上平行執行。</span><span class="sxs-lookup"><span data-stu-id="4128c-111">A compute shader can run on many threads in parallel.</span></span>

## <a name="using-compute-shader-on-direct3d-10x-hardware"></a><span data-ttu-id="4128c-112">在 Direct3D 2.x 硬體上使用計算著色器</span><span class="sxs-lookup"><span data-stu-id="4128c-112">Using Compute Shader on Direct3D 10.x Hardware</span></span>

<span data-ttu-id="4128c-113">Microsoft Direct3D 10 上的計算著色器也稱為 DirectCompute 4.x。</span><span class="sxs-lookup"><span data-stu-id="4128c-113">A compute shader on Microsoft Direct3D 10 is also known as DirectCompute 4.x.</span></span>

<span data-ttu-id="4128c-114">如果您使用 Direct3D 11 API 和更新的驅動程式， [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 10 和 10.1 Direct3D 硬體可以選擇性地支援使用 cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 [設定檔](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models)的有限 DirectCompute 形式。</span><span class="sxs-lookup"><span data-stu-id="4128c-114">If you use the Direct3D 11 API and updated drivers, [feature level](overviews-direct3d-11-devices-downlevel-intro.md) 10 and 10.1 Direct3D hardware can optionally support a limited form of DirectCompute that uses the cs\_4\_0 and cs\_4\_1 [profiles](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models).</span></span> <span data-ttu-id="4128c-115">當您在此硬體上使用 DirectCompute 時，請記住下列限制：</span><span class="sxs-lookup"><span data-stu-id="4128c-115">When you use DirectCompute on this hardware, keep the following limitations in mind:</span></span>

-   <span data-ttu-id="4128c-116">最大執行緒數目限制為每個群組 D3D11 \_ CS \_ 4 \_ X \_ 執行緒群組的 \_ \_ 最大執行緒數目 \_ \_ \_ (768) 。</span><span class="sxs-lookup"><span data-stu-id="4128c-116">The maximum number of threads is limited to D3D11\_CS\_4\_X\_THREAD\_GROUP\_MAX\_THREADS\_PER\_GROUP (768) per group.</span></span>
-   <span data-ttu-id="4128c-117">**Numthreads** 的 X 和 Y 維度僅限於 D3D11 \_ cs \_ 4 \_ x \_ 執行緒 \_ 群組 \_ 最大 \_ x (768) 和 D3D11 \_ CS \_ 4 \_ x \_ 執行緒 \_ 群組 \_ 最大 \_ Y (768) 。</span><span class="sxs-lookup"><span data-stu-id="4128c-117">The X and Y dimension of **numthreads** is limited to D3D11\_CS\_4\_X\_THREAD\_GROUP\_MAX\_X (768) and D3D11\_CS\_4\_X\_THREAD\_GROUP\_MAX\_Y (768).</span></span>
-   <span data-ttu-id="4128c-118">**Numthreads** 的 Z 維度限制為1。</span><span class="sxs-lookup"><span data-stu-id="4128c-118">The Z dimension of **numthreads** is limited to 1.</span></span>
-   <span data-ttu-id="4128c-119">分派的 Z 維度限制 \_ \_ \_ \_ \_ \_ \_ \_ 在 \_ z \_ 維度 (1) 的 D3D11 CS 4 X 分派最大執行緒群組。</span><span class="sxs-lookup"><span data-stu-id="4128c-119">The Z dimension of dispatch is limited to D3D11\_CS\_4\_X\_DISPATCH\_MAX\_THREAD\_GROUPS\_IN\_Z\_DIMENSION (1).</span></span>
-   <span data-ttu-id="4128c-120">只有一個未排序的存取權可系結至著色器 (D3D11 \_ CS \_ 4 \_ X \_ UAV \_ REGISTER \_ COUNT 是 1) 。</span><span class="sxs-lookup"><span data-stu-id="4128c-120">Only one unordered-access view can be bound to the shader (D3D11\_CS\_4\_X\_UAV\_REGISTER\_COUNT is 1).</span></span>
-   <span data-ttu-id="4128c-121">只有 [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s 和 [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)可以作為未排序存取的視圖。</span><span class="sxs-lookup"><span data-stu-id="4128c-121">Only [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s and [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s are available as unordered-access views.</span></span>
-   <span data-ttu-id="4128c-122">執行緒只能在 groupshared 記憶體中存取自己的區域以進行寫入，不過它可以讀取任何位置。</span><span class="sxs-lookup"><span data-stu-id="4128c-122">A thread can only access its own region in groupshared memory for writing, though it can read from any location.</span></span>
-   <span data-ttu-id="4128c-123">[SV \_](/previous-versions/windows/desktop/legacy/ff471569(v=vs.85))存取 **groupshared** 記憶體以進行寫入時，必須使用 GroupIndex 或 [SV \_ DispatchThreadID](/windows/desktop/direct3dhlsl/sv-dispatchthreadid) 。</span><span class="sxs-lookup"><span data-stu-id="4128c-123">[SV\_GroupIndex](/previous-versions/windows/desktop/legacy/ff471569(v=vs.85)) or [SV\_DispatchThreadID](/windows/desktop/direct3dhlsl/sv-dispatchthreadid) must be used when accessing **groupshared** memory for writing.</span></span>
-   <span data-ttu-id="4128c-124">**Groupshared** 記憶體限制為每個群組的16KB。</span><span class="sxs-lookup"><span data-stu-id="4128c-124">**Groupshared** memory is limited to 16KB per group.</span></span>
-   <span data-ttu-id="4128c-125">單一線程受限於 **groupshared** 記憶體的256位元組區域以進行寫入。</span><span class="sxs-lookup"><span data-stu-id="4128c-125">A single thread is limited to a 256 byte region of **groupshared** memory for writing.</span></span>
-   <span data-ttu-id="4128c-126">沒有可部分完成的指示。</span><span class="sxs-lookup"><span data-stu-id="4128c-126">No atomic instructions are available.</span></span>
-   <span data-ttu-id="4128c-127">沒有雙精確度值可用。</span><span class="sxs-lookup"><span data-stu-id="4128c-127">No double-precision values are available.</span></span>

## <a name="using-compute-shader-on-direct3d-11x-hardware"></a><span data-ttu-id="4128c-128">在 Direct3D 11. x 硬體上使用計算著色器</span><span class="sxs-lookup"><span data-stu-id="4128c-128">Using Compute Shader on Direct3D 11.x Hardware</span></span>

<span data-ttu-id="4128c-129">Direct3D 11 上的計算著色器也稱為 DirectCompute 5.0。</span><span class="sxs-lookup"><span data-stu-id="4128c-129">A compute shader on Direct3D 11 is also known as DirectCompute 5.0.</span></span>

<span data-ttu-id="4128c-130">當您使用 DirectCompute 搭配 cs \_ 5 \_ 0 的 [設定檔](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models)時，請記住下列專案：</span><span class="sxs-lookup"><span data-stu-id="4128c-130">When you use DirectCompute with cs\_5\_0 [profiles](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models), keep the following items in mind:</span></span>

-   <span data-ttu-id="4128c-131">最大執行緒數目限制為每個群組 D3D11 \_ CS \_ 執行緒 \_ 群組 \_ 最大執行緒群組 \_ \_ \_ (1024) 每個群組。</span><span class="sxs-lookup"><span data-stu-id="4128c-131">The maximum number of threads is limited to D3D11\_CS\_THREAD\_GROUP\_MAX\_THREADS\_PER\_GROUP (1024) per group.</span></span>
-   <span data-ttu-id="4128c-132">**Numthreads** 的 x 和 Y 維度僅限於 D3D11 \_ cs \_ 執行緒 \_ 群組 \_ 最大 \_ x (1024) 和 D3D11 \_ CS \_ 執行緒 \_ 群組 \_ max \_ Y (1024) 。</span><span class="sxs-lookup"><span data-stu-id="4128c-132">The X and Y dimension of **numthreads** is limited to D3D11\_CS\_THREAD\_GROUP\_MAX\_X (1024) and D3D11\_CS\_THREAD\_GROUP\_MAX\_Y (1024).</span></span>
-   <span data-ttu-id="4128c-133">**Numthreads** 的 z 維度限制為 D3D11 \_ CS \_ 執行緒 \_ 群組 \_ 最大 \_ z (64) 。</span><span class="sxs-lookup"><span data-stu-id="4128c-133">The Z dimension of **numthreads** is limited to D3D11\_CS\_THREAD\_GROUP\_MAX\_Z (64).</span></span>
-   <span data-ttu-id="4128c-134">分派的最大維度限制為 \_ \_ \_ 每個維度 D3D11 CS 分派最大 \_ 執行緒 \_ 群組 \_ \_ (65535) 。</span><span class="sxs-lookup"><span data-stu-id="4128c-134">The maximum dimension of dispatch is limited to D3D11\_CS\_DISPATCH\_MAX\_THREAD\_GROUPS\_PER\_DIMENSION (65535).</span></span>
-   <span data-ttu-id="4128c-135">可系結至著色器的未排序存取視圖的最大數目為 D3D11 \_ PS \_ CS \_ UAV \_ REGISTER \_ COUNT (8) 。</span><span class="sxs-lookup"><span data-stu-id="4128c-135">The maximum number of unordered-access views that can be bound to a shader is D3D11\_PS\_CS\_UAV\_REGISTER\_COUNT (8).</span></span>
-   <span data-ttu-id="4128c-136">支援 [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s、 [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)和具類型的未排序存取視圖 ([RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d)、 [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)、 [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)等) 。</span><span class="sxs-lookup"><span data-stu-id="4128c-136">Supports [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s, [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s, and typed unordered-access views ([RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d), and so on).</span></span>
-   <span data-ttu-id="4128c-137">提供不可部分完成的指示。</span><span class="sxs-lookup"><span data-stu-id="4128c-137">Atomic instructions are available.</span></span>
-   <span data-ttu-id="4128c-138">可能會有雙精確度支援。</span><span class="sxs-lookup"><span data-stu-id="4128c-138">Double-precision support might be available.</span></span> <span data-ttu-id="4128c-139">如需如何判斷雙精確度是否可用的詳細資訊，請參閱 [**D3D11 \_ 功能 \_ 雙**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)精度浮點數。</span><span class="sxs-lookup"><span data-stu-id="4128c-139">For information about how to determine whether double-precision is available, see [**D3D11\_FEATURE\_DOUBLES**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4128c-140">本節內容</span><span class="sxs-lookup"><span data-stu-id="4128c-140">In this section</span></span>



| <span data-ttu-id="4128c-141">主題</span><span class="sxs-lookup"><span data-stu-id="4128c-141">Topic</span></span>                                                                              | <span data-ttu-id="4128c-142">描述</span><span class="sxs-lookup"><span data-stu-id="4128c-142">Description</span></span>                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4128c-143">新的資源類型</span><span class="sxs-lookup"><span data-stu-id="4128c-143">New Resource Types</span></span>](direct3d-11-advanced-stages-cs-resources.md)<br/>      | <span data-ttu-id="4128c-144">已在 Direct3D 11 中新增數個新的資源類型。</span><span class="sxs-lookup"><span data-stu-id="4128c-144">Several new resource types have been added in Direct3D 11.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="4128c-145">存取資源</span><span class="sxs-lookup"><span data-stu-id="4128c-145">Accessing Resources</span></span>](direct3d-11-advanced-stages-cs-access.md)<br/>        | <span data-ttu-id="4128c-146">有數種方式可存取 [資源](overviews-direct3d-11-resources-types.md)。</span><span class="sxs-lookup"><span data-stu-id="4128c-146">There are several ways to access [resources](overviews-direct3d-11-resources-types.md).</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="4128c-147">不可部分完成函式</span><span class="sxs-lookup"><span data-stu-id="4128c-147">Atomic Functions</span></span>](direct3d-11-advanced-stages-cs-atomic-functions.md)<br/> | <span data-ttu-id="4128c-148">若要存取新的資源類型或共用記憶體，請使用連鎖內建函式。</span><span class="sxs-lookup"><span data-stu-id="4128c-148">To access a new resource type or shared memory, use an interlocked intrinsic function.</span></span> <span data-ttu-id="4128c-149">連鎖函式保證會以不可部分完成的方式運作。</span><span class="sxs-lookup"><span data-stu-id="4128c-149">Interlocked functions are guaranteed to operate atomically.</span></span> <span data-ttu-id="4128c-150">也就是說，它們保證會以程式設計的順序發生。</span><span class="sxs-lookup"><span data-stu-id="4128c-150">That is, they are guaranteed to occur in the order programmed.</span></span> <span data-ttu-id="4128c-151">本節列出不可部分完成的函式。</span><span class="sxs-lookup"><span data-stu-id="4128c-151">This section lists the atomic functions.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="4128c-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="4128c-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4128c-153">圖形管線</span><span class="sxs-lookup"><span data-stu-id="4128c-153">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="4128c-154">如何：建立計算著色器</span><span class="sxs-lookup"><span data-stu-id="4128c-154">How To: Create a Compute Shader</span></span>](direct3d-11-advanced-stages-compute-create.md)
</dt> </dl>

 

