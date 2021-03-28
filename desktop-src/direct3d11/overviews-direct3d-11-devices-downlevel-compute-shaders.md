---
title: 下層硬體上的計算著色器
description: 本主題將討論如何在 Direct3D 10 硬體上的 Direct3D 11 應用程式中使用計算著色器。
ms.assetid: b864269f-c1f7-4253-888d-04d1ed3e6587
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e77214e917d4d74b0e1eebcc3de245d136157976
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024302"
---
# <a name="compute-shaders-on-downlevel-hardware"></a><span data-ttu-id="24d80-103">下層硬體上的計算著色器</span><span class="sxs-lookup"><span data-stu-id="24d80-103">Compute Shaders on Downlevel Hardware</span></span>

<span data-ttu-id="24d80-104">Direct3D 11 提供使用 [計算著色](direct3d-11-advanced-stages-compute-shader.md) 器的功能，可在大部分的 Direct3D 2.x 硬體上運作，但有一些作業限制。</span><span class="sxs-lookup"><span data-stu-id="24d80-104">Direct3D 11 provides the ability to use [compute shaders](direct3d-11-advanced-stages-compute-shader.md) that operate on most Direct3D 10.x hardware, with some limitations to operation.</span></span> <span data-ttu-id="24d80-105">計算著色器技術也稱為 DirectCompute 技術。</span><span class="sxs-lookup"><span data-stu-id="24d80-105">The compute shader technology is also known as the DirectCompute technology.</span></span> <span data-ttu-id="24d80-106">本主題將討論如何在 Direct3D 10 硬體上的 Direct3D 11 應用程式中使用 [計算著色](direct3d-11-advanced-stages-compute-shader.md) 器。</span><span class="sxs-lookup"><span data-stu-id="24d80-106">This topic discusses how to make use of [compute shaders](direct3d-11-advanced-stages-compute-shader.md) in a Direct3D 11 app on Direct3D 10 hardware.</span></span>

<span data-ttu-id="24d80-107">舊版硬體上的計算著色器支援僅適用于與 Direct3D 2.x 相容的裝置。</span><span class="sxs-lookup"><span data-stu-id="24d80-107">Support for compute shaders on downlevel hardware is only for devices compatible with Direct3D 10.x.</span></span> <span data-ttu-id="24d80-108">無法在 Direct3D 2.x 硬體上使用計算著色器。</span><span class="sxs-lookup"><span data-stu-id="24d80-108">Compute shaders cannot be used on Direct3D 9.x hardware.</span></span>

<span data-ttu-id="24d80-109">若要檢查 Direct3D 10. x 硬體是否支援計算著色器，請呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)。</span><span class="sxs-lookup"><span data-stu-id="24d80-109">To check if Direct3D 10.x hardware supports compute shaders, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span></span> <span data-ttu-id="24d80-110">在 **CheckFeatureSupport** 呼叫中，將 D3D11 \_ feature \_ D3D10 \_ X \_ 硬體 \_ 選項值傳遞至 *FEATURE* 參數、將 [**D3D11 \_ FEATURE \_ data \_ D3D10 \_ x \_ 硬體 \_ 選項**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options) 結構的指標傳遞至 *pFeatureSupportData* 參數，並將 **D3D11 \_ FEATURE \_ data \_ D3D10 \_ x \_ 硬體 \_ 選項** 結構的大小傳遞給 *FeatureSupportDataSize* 參數。</span><span class="sxs-lookup"><span data-stu-id="24d80-110">In the **CheckFeatureSupport** call, pass the D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS value to the *Feature* parameter, pass a pointer to the [**D3D11\_FEATURE\_DATA\_D3D10\_X\_HARDWARE\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options) structure to the *pFeatureSupportData* parameter, and pass the size of the **D3D11\_FEATURE\_DATA\_D3D10\_X\_HARDWARE\_OPTIONS** structure to the *FeatureSupportDataSize* parameter.</span></span> <span data-ttu-id="24d80-111">如果 Direct3D 2.x 硬體支援計算著色器， **CheckFeatureSupport** 會在 ComputeShaders Plus RawAndStructuredBuffers 中透過 **D3D11 \_ FEATURE \_ DATA \_ D3D10 \_ x \_ 硬體 \_ 選項** 的 **\_ \_ \_ \_ 著色器 \_ 4 \_ x** 成員傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="24d80-111">**CheckFeatureSupport** returns **TRUE** in the **ComputeShaders\_Plus\_RawAndStructuredBuffers\_Via\_Shader\_4\_x** member of **D3D11\_FEATURE\_DATA\_D3D10\_X\_HARDWARE\_OPTIONS** if the Direct3D 10.x hardware supports compute shaders.</span></span>

<span data-ttu-id="24d80-112">[ [10Level9 參考](d3d11-graphics-reference-10level9.md) ] 區段會列出各種 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 和 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 方法在各種10Level9 功能層級的行為方式之間的差異。</span><span class="sxs-lookup"><span data-stu-id="24d80-112">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

-   [<span data-ttu-id="24d80-113">未排序的存取視圖 (UAVs) </span><span class="sxs-lookup"><span data-stu-id="24d80-113">Unordered Access Views (UAVs)</span></span>](#unordered-access-views-uavs)
-   [<span data-ttu-id="24d80-114">著色器資源檢視 (SRVs) </span><span class="sxs-lookup"><span data-stu-id="24d80-114">Shader Resource Views (SRVs)</span></span>](#shader-resource-views-srvs)
-   [<span data-ttu-id="24d80-115">執行緒群組</span><span class="sxs-lookup"><span data-stu-id="24d80-115">Thread Groups</span></span>](#thread-groups)
    -   [<span data-ttu-id="24d80-116">執行緒群組維度</span><span class="sxs-lookup"><span data-stu-id="24d80-116">Thread Group Dimensions</span></span>](#thread-group-dimensions)
    -   [<span data-ttu-id="24d80-117">二維執行緒索引</span><span class="sxs-lookup"><span data-stu-id="24d80-117">Two-Dimensional Thread Indices</span></span>](#two-dimensional-thread-indices)
    -   [<span data-ttu-id="24d80-118">執行緒群組共用記憶體 (TGSM) </span><span class="sxs-lookup"><span data-stu-id="24d80-118">Thread Group Shared Memory (TGSM)</span></span>](#thread-group-shared-memory-tgsm)
-   [<span data-ttu-id="24d80-119">使用 D3DCOMPILE \_ SKIP \_ 優化的 D3DCompile</span><span class="sxs-lookup"><span data-stu-id="24d80-119">D3DCompile with D3DCOMPILE\_SKIP\_OPTIMIZATION</span></span>](/windows)
-   [<span data-ttu-id="24d80-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="24d80-120">Related topics</span></span>](#related-topics)

## <a name="unordered-access-views-uavs"></a><span data-ttu-id="24d80-121">未排序的存取視圖 (UAVs) </span><span class="sxs-lookup"><span data-stu-id="24d80-121">Unordered Access Views (UAVs)</span></span>

<span data-ttu-id="24d80-122">舊版硬體支援原始的 ([RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)) 和結構化 ([RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)) 未排序的存取視圖，但有下列限制：</span><span class="sxs-lookup"><span data-stu-id="24d80-122">Raw ([RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)) and Structured ([RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)) Unordered Access Views are supported on downlevel hardware, with the following limitations:</span></span>

-   <span data-ttu-id="24d80-123">一次只能透過 [**>id3d11devicecoNtext：： CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)，將單一 UAV 系結至管線。</span><span class="sxs-lookup"><span data-stu-id="24d80-123">Only a single UAV may be bound to a pipeline at a time through [**ID3D11DeviceContext::CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews).</span></span>
-   <span data-ttu-id="24d80-124">原始 UAV 的基底位移必須對齊256位元組的界限 (而不是 Direct3D 11 硬體) 所需的16位元組對齊。</span><span class="sxs-lookup"><span data-stu-id="24d80-124">The base offset for a Raw UAV must be aligned on a 256-byte boundary (instead of 16-byte alignment required for Direct3D 11 hardware).</span></span>

<span data-ttu-id="24d80-125">下層硬體不支援具類型的 UAVs。</span><span class="sxs-lookup"><span data-stu-id="24d80-125">Typed UAVs are not supported on downlevel hardware.</span></span> <span data-ttu-id="24d80-126">這包括 [Texture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d)、 [Texture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)和 [Texture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d) UAVs。</span><span class="sxs-lookup"><span data-stu-id="24d80-126">This includes [Texture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [Texture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), and [Texture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d) UAVs.</span></span>

<span data-ttu-id="24d80-127">下層硬體上的圖元著色器不支援未排序的存取。</span><span class="sxs-lookup"><span data-stu-id="24d80-127">Pixel Shaders on downlevel hardware do not support unordered access.</span></span>

## <a name="shader-resource-views-srvs"></a><span data-ttu-id="24d80-128">著色器資源檢視 (SRVs) </span><span class="sxs-lookup"><span data-stu-id="24d80-128">Shader Resource Views (SRVs)</span></span>

<span data-ttu-id="24d80-129">在舊版硬體上，支援將原始和結構化緩衝區作為著色器資源查看，以進行唯讀存取，因為它們是在 Direct3D 11 硬體上。</span><span class="sxs-lookup"><span data-stu-id="24d80-129">Raw and Structured Buffers as Shader Resource Views are supported on downlevel hardware for read-only access, as they are on Direct3D 11 hardware.</span></span> <span data-ttu-id="24d80-130">這些資源類型支援頂點著色器、幾何著色器、圖元著色器以及計算著色器。</span><span class="sxs-lookup"><span data-stu-id="24d80-130">These resource types are supported for Vertex Shaders, Geometry Shaders, Pixel Shaders as well as Compute Shaders.</span></span>

## <a name="thread-groups"></a><span data-ttu-id="24d80-131">執行緒群組</span><span class="sxs-lookup"><span data-stu-id="24d80-131">Thread Groups</span></span>

<span data-ttu-id="24d80-132">計算著色器可以線上程群組內以平行方式在多個執行緒上執行。</span><span class="sxs-lookup"><span data-stu-id="24d80-132">A compute shader can execute on many threads in parallel, within a thread group.</span></span>

<span data-ttu-id="24d80-133">下層硬體支援執行緒群組，但有下列限制：</span><span class="sxs-lookup"><span data-stu-id="24d80-133">Thread groups are supported on downlevel hardware, with the following limitations:</span></span>

### <a name="thread-group-dimensions"></a><span data-ttu-id="24d80-134">執行緒群組維度</span><span class="sxs-lookup"><span data-stu-id="24d80-134">Thread Group Dimensions</span></span>

<span data-ttu-id="24d80-135">針對下層硬體定義的執行緒群組受限於768的 X 和 Y 維度。</span><span class="sxs-lookup"><span data-stu-id="24d80-135">Thread groups defined for downlevel hardware are limited to X and Y dimensions of 768.</span></span> <span data-ttu-id="24d80-136">這小於 Direct3D 11 硬體的最大值1024。</span><span class="sxs-lookup"><span data-stu-id="24d80-136">This is less than the maximum values of 1024 for Direct3D 11 hardware.</span></span> <span data-ttu-id="24d80-137">64的最大 Z 維度未變更。</span><span class="sxs-lookup"><span data-stu-id="24d80-137">The maximum Z dimension of 64 is unchanged.</span></span>

<span data-ttu-id="24d80-138">群組中的執行緒總數 (X × Y × Z) 限制為768。</span><span class="sxs-lookup"><span data-stu-id="24d80-138">The total number of threads in the group (X × Y × Z) is limited to 768.</span></span> <span data-ttu-id="24d80-139">這小於適用于 Direct3D 11 硬體的1024限制。</span><span class="sxs-lookup"><span data-stu-id="24d80-139">This is less than the limit of 1024 for Direct3D 11 hardware.</span></span>

<span data-ttu-id="24d80-140">如果超過這些數位，著色器編譯將會失敗。</span><span class="sxs-lookup"><span data-stu-id="24d80-140">If these numbers are exceeded, shader compilation will fail.</span></span>

### <a name="two-dimensional-thread-indices"></a><span data-ttu-id="24d80-141">Two-Dimensional 執行緒索引</span><span class="sxs-lookup"><span data-stu-id="24d80-141">Two-Dimensional Thread Indices</span></span>

<span data-ttu-id="24d80-142">執行緒群組內的特定執行緒會使用 (x、y、z) 指定的3D 向量進行編制索引。</span><span class="sxs-lookup"><span data-stu-id="24d80-142">A particular thread within a thread group is indexed using a 3D vector given by (x,y,z).</span></span>

<span data-ttu-id="24d80-143">針對在舊版硬體上運作的計算著色器，執行緒群組只支援兩個維度。</span><span class="sxs-lookup"><span data-stu-id="24d80-143">For compute shaders operating on downlevel hardware, thread groups only support two dimensions.</span></span> <span data-ttu-id="24d80-144">這表示3D 向量中的 Z 值必須一律為1。</span><span class="sxs-lookup"><span data-stu-id="24d80-144">This means that the Z value in the 3D vector must always be 1.</span></span>

<span data-ttu-id="24d80-145">這項限制特別適用于下列各項：</span><span class="sxs-lookup"><span data-stu-id="24d80-145">This limitation specifically applies to the following:</span></span>

-   <span data-ttu-id="24d80-146">[**>id3d11devicecoNtext：:D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch)— *ThreadGroupCountZ* 引數必須是1。</span><span class="sxs-lookup"><span data-stu-id="24d80-146">[**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch)— The *ThreadGroupCountZ* argument must be 1.</span></span>
-   <span data-ttu-id="24d80-147">[**>id3d11devicecoNtext：:D ispatchindirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect)-在舊版硬體上不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="24d80-147">[**ID3D11DeviceContext::DispatchIndirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect)— This function is not supported on downlevel hardware.</span></span>
-   <span data-ttu-id="24d80-148">[numthreads](/windows/desktop/direct3dhlsl/sm5-attributes-numthreads)-Z 值必須是1。</span><span class="sxs-lookup"><span data-stu-id="24d80-148">[numthreads](/windows/desktop/direct3dhlsl/sm5-attributes-numthreads)— The Z value must be 1.</span></span>

### <a name="thread-group-shared-memory-tgsm"></a><span data-ttu-id="24d80-149">執行緒群組共用記憶體 (TGSM) </span><span class="sxs-lookup"><span data-stu-id="24d80-149">Thread Group Shared Memory (TGSM)</span></span>

<span data-ttu-id="24d80-150">執行緒群組共用記憶體僅限於在下層硬體上16Kb。</span><span class="sxs-lookup"><span data-stu-id="24d80-150">Thread Group Shared Memory is limited to 16Kb on downlevel hardware.</span></span> <span data-ttu-id="24d80-151">這小於適用于 Direct3D 11 硬體的32Kb。</span><span class="sxs-lookup"><span data-stu-id="24d80-151">This is less than the 32Kb that is available to Direct3D 11 hardware.</span></span>

<span data-ttu-id="24d80-152">計算著色器執行緒只能寫入自己的 TGSM 區域。</span><span class="sxs-lookup"><span data-stu-id="24d80-152">A Compute Shader thread may only write to its own region of TGSM.</span></span> <span data-ttu-id="24d80-153">這個僅限寫入區域的大小上限為256個位元組或較小，且最大值會隨著針對群組宣告的執行緒數目增加而減少。</span><span class="sxs-lookup"><span data-stu-id="24d80-153">This write-only region has a maximum size of 256 bytes or less, with the maximum decreasing as the number of threads declared for the group increases.</span></span>

<span data-ttu-id="24d80-154">下錶針對群組中的執行緒數目，定義每個執行緒的 TGSM 區域大小上限：</span><span class="sxs-lookup"><span data-stu-id="24d80-154">The following table defines the per-thread maximum size of a TGSM region for the number of threads in the group:</span></span>



| <span data-ttu-id="24d80-155">群組中的執行緒數目</span><span class="sxs-lookup"><span data-stu-id="24d80-155">Number of Threads in Group</span></span> | <span data-ttu-id="24d80-156">每個執行緒的 TGSM 大小上限</span><span class="sxs-lookup"><span data-stu-id="24d80-156">Maximum TGSM Size Per Thread</span></span> |
|----------------------------|------------------------------|
| <span data-ttu-id="24d80-157">0-64</span><span class="sxs-lookup"><span data-stu-id="24d80-157">0-64</span></span>                       | <span data-ttu-id="24d80-158">256</span><span class="sxs-lookup"><span data-stu-id="24d80-158">256</span></span>                          |
| <span data-ttu-id="24d80-159">65-68</span><span class="sxs-lookup"><span data-stu-id="24d80-159">65-68</span></span>                      | <span data-ttu-id="24d80-160">240</span><span class="sxs-lookup"><span data-stu-id="24d80-160">240</span></span>                          |
| <span data-ttu-id="24d80-161">69-72</span><span class="sxs-lookup"><span data-stu-id="24d80-161">69-72</span></span>                      | <span data-ttu-id="24d80-162">224</span><span class="sxs-lookup"><span data-stu-id="24d80-162">224</span></span>                          |
| <span data-ttu-id="24d80-163">73-76</span><span class="sxs-lookup"><span data-stu-id="24d80-163">73-76</span></span>                      | <span data-ttu-id="24d80-164">208</span><span class="sxs-lookup"><span data-stu-id="24d80-164">208</span></span>                          |
| <span data-ttu-id="24d80-165">77-84</span><span class="sxs-lookup"><span data-stu-id="24d80-165">77-84</span></span>                      | <span data-ttu-id="24d80-166">192</span><span class="sxs-lookup"><span data-stu-id="24d80-166">192</span></span>                          |
| <span data-ttu-id="24d80-167">85-92</span><span class="sxs-lookup"><span data-stu-id="24d80-167">85-92</span></span>                      | <span data-ttu-id="24d80-168">176</span><span class="sxs-lookup"><span data-stu-id="24d80-168">176</span></span>                          |
| <span data-ttu-id="24d80-169">93-100</span><span class="sxs-lookup"><span data-stu-id="24d80-169">93-100</span></span>                     | <span data-ttu-id="24d80-170">160</span><span class="sxs-lookup"><span data-stu-id="24d80-170">160</span></span>                          |
| <span data-ttu-id="24d80-171">101-112</span><span class="sxs-lookup"><span data-stu-id="24d80-171">101-112</span></span>                    | <span data-ttu-id="24d80-172">144</span><span class="sxs-lookup"><span data-stu-id="24d80-172">144</span></span>                          |
| <span data-ttu-id="24d80-173">113-128</span><span class="sxs-lookup"><span data-stu-id="24d80-173">113-128</span></span>                    | <span data-ttu-id="24d80-174">128</span><span class="sxs-lookup"><span data-stu-id="24d80-174">128</span></span>                          |
| <span data-ttu-id="24d80-175">129-144</span><span class="sxs-lookup"><span data-stu-id="24d80-175">129-144</span></span>                    | <span data-ttu-id="24d80-176">112</span><span class="sxs-lookup"><span data-stu-id="24d80-176">112</span></span>                          |
| <span data-ttu-id="24d80-177">145-168</span><span class="sxs-lookup"><span data-stu-id="24d80-177">145-168</span></span>                    | <span data-ttu-id="24d80-178">96</span><span class="sxs-lookup"><span data-stu-id="24d80-178">96</span></span>                           |
| <span data-ttu-id="24d80-179">169-204</span><span class="sxs-lookup"><span data-stu-id="24d80-179">169-204</span></span>                    | <span data-ttu-id="24d80-180">80</span><span class="sxs-lookup"><span data-stu-id="24d80-180">80</span></span>                           |
| <span data-ttu-id="24d80-181">205-256</span><span class="sxs-lookup"><span data-stu-id="24d80-181">205-256</span></span>                    | <span data-ttu-id="24d80-182">64</span><span class="sxs-lookup"><span data-stu-id="24d80-182">64</span></span>                           |
| <span data-ttu-id="24d80-183">257-340</span><span class="sxs-lookup"><span data-stu-id="24d80-183">257-340</span></span>                    | <span data-ttu-id="24d80-184">48</span><span class="sxs-lookup"><span data-stu-id="24d80-184">48</span></span>                           |
| <span data-ttu-id="24d80-185">341-512</span><span class="sxs-lookup"><span data-stu-id="24d80-185">341-512</span></span>                    | <span data-ttu-id="24d80-186">32</span><span class="sxs-lookup"><span data-stu-id="24d80-186">32</span></span>                           |
| <span data-ttu-id="24d80-187">513-768</span><span class="sxs-lookup"><span data-stu-id="24d80-187">513-768</span></span>                    | <span data-ttu-id="24d80-188">16</span><span class="sxs-lookup"><span data-stu-id="24d80-188">16</span></span>                           |



 

<span data-ttu-id="24d80-189">計算著色器執行緒可能會從任何位置讀取 TGSM。</span><span class="sxs-lookup"><span data-stu-id="24d80-189">A Compute Shader thread may read the TGSM from any location.</span></span>

## <a name="d3dcompile-with-d3dcompile_skip_optimization"></a><span data-ttu-id="24d80-190">使用 D3DCOMPILE \_ SKIP \_ 優化的 D3DCompile</span><span class="sxs-lookup"><span data-stu-id="24d80-190">D3DCompile with D3DCOMPILE\_SKIP\_OPTIMIZATION</span></span>

<span data-ttu-id="24d80-191">當您傳遞 cs 4 0 做為著色器目標時， [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile)會傳回 **E \_ >notimpl** ， \_ \_ 以及 [**D3DCompile \_ SKIP \_ 優化**](/windows/desktop/direct3dhlsl/d3dcompile-constants)編譯選項。</span><span class="sxs-lookup"><span data-stu-id="24d80-191">[**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) returns **E\_NOTIMPL** when you pass cs\_4\_0 as the shader target along with the [**D3DCOMPILE\_SKIP\_OPTIMIZATION**](/windows/desktop/direct3dhlsl/d3dcompile-constants) compile option.</span></span> <span data-ttu-id="24d80-192">Cs \_ 5 \_ 0 著色器目標適用于 **D3DCOMPILE \_ SKIP \_ 優化**。</span><span class="sxs-lookup"><span data-stu-id="24d80-192">The cs\_5\_0 shader target works with **D3DCOMPILE\_SKIP\_OPTIMIZATION**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24d80-193">相關主題</span><span class="sxs-lookup"><span data-stu-id="24d80-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24d80-194">舊版硬體上的 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="24d80-194">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 