---
title: 具類型的未排序存取視圖 (UAV) 載入
description: 未排序的存取視圖 (UAV) 具類型的負載，是可讓著色器從具有特定 DXGI 格式的 UAV 讀取的能力 \_ 。
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4adfd7511590a43b7f87507c5a1e0a2a87c925b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548386"
---
# <a name="typed-unordered-access-view-uav-loads"></a><span data-ttu-id="5f86a-103">具類型的未排序存取視圖 (UAV) 載入</span><span class="sxs-lookup"><span data-stu-id="5f86a-103">Typed unordered access view (UAV) loads</span></span>

<span data-ttu-id="5f86a-104">未排序的存取視圖 (UAV) 具類型的負載，是可讓著色器從具有特定 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)的 UAV 讀取的能力。</span><span class="sxs-lookup"><span data-stu-id="5f86a-104">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

-   [<span data-ttu-id="5f86a-105">概觀</span><span class="sxs-lookup"><span data-stu-id="5f86a-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="5f86a-106">支援的格式和 API 呼叫</span><span class="sxs-lookup"><span data-stu-id="5f86a-106">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="5f86a-107">從 HLSL 使用具類型的 UAV 載入</span><span class="sxs-lookup"><span data-stu-id="5f86a-107">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="5f86a-108">使用 UNORM 和 SNORM 具類型的 UAV 從 HLSL 載入</span><span class="sxs-lookup"><span data-stu-id="5f86a-108">Using UNORM and SNORM typed UAV loads from HLSL</span></span>](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="5f86a-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f86a-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="5f86a-110">概觀</span><span class="sxs-lookup"><span data-stu-id="5f86a-110">Overview</span></span>

<span data-ttu-id="5f86a-111">未排序的存取視圖 (UAV) 是未排序存取資源 (的視圖，可包含緩衝區、紋理和材質陣列，但不需要多取樣) 。</span><span class="sxs-lookup"><span data-stu-id="5f86a-111">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="5f86a-112">UAV 可讓您從多個執行緒暫時未排序的讀取/寫入存取。</span><span class="sxs-lookup"><span data-stu-id="5f86a-112">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="5f86a-113">這表示此資源類型可以由多個執行緒同時讀取/寫入，而不會產生記憶體衝突。</span><span class="sxs-lookup"><span data-stu-id="5f86a-113">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="5f86a-114">這項同時存取是透過使用不可部分 [完成的函](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions)式來處理。</span><span class="sxs-lookup"><span data-stu-id="5f86a-114">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="5f86a-115">D3D12 (和 D3D 11.3) 會在可與具類型 UAV 載入搭配使用的格式清單上展開。</span><span class="sxs-lookup"><span data-stu-id="5f86a-115">D3D12 (and D3D11.3) expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="5f86a-116">支援的格式和 API 呼叫</span><span class="sxs-lookup"><span data-stu-id="5f86a-116">Supported formats and API calls</span></span>

<span data-ttu-id="5f86a-117">先前支援下列三種格式的 UAV 載入，並為 D3D 11.0 硬體所需。</span><span class="sxs-lookup"><span data-stu-id="5f86a-117">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="5f86a-118">所有 D3D 11.3 和 D3D12 硬體都支援它們。</span><span class="sxs-lookup"><span data-stu-id="5f86a-118">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="5f86a-119">R32 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="5f86a-119">R32\_FLOAT</span></span>
-   <span data-ttu-id="5f86a-120">R32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5f86a-120">R32\_UINT</span></span>
-   <span data-ttu-id="5f86a-121">R32 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="5f86a-121">R32\_SINT</span></span>

<span data-ttu-id="5f86a-122">以下是在 D3D12 或 D3D 11.3 硬體上支援的格式，因此，如果支援任何一種格式，則會支援所有的格式。</span><span class="sxs-lookup"><span data-stu-id="5f86a-122">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="5f86a-123">R32G32B32A32 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="5f86a-123">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="5f86a-124">R32G32B32A32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5f86a-124">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="5f86a-125">R32G32B32A32 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="5f86a-125">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="5f86a-126">R16G16B16A16 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="5f86a-126">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="5f86a-127">R16G16B16A16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5f86a-127">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="5f86a-128">R16G16B16A16 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="5f86a-128">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="5f86a-129">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-129">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="5f86a-130">R8G8B8A8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5f86a-130">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="5f86a-131">R8G8B8A8 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="5f86a-131">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="5f86a-132">R16 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="5f86a-132">R16\_FLOAT</span></span>
-   <span data-ttu-id="5f86a-133">R16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5f86a-133">R16\_UINT</span></span>
-   <span data-ttu-id="5f86a-134">R16 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="5f86a-134">R16\_SINT</span></span>
-   <span data-ttu-id="5f86a-135">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-135">R8\_UNORM</span></span>
-   <span data-ttu-id="5f86a-136">R8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5f86a-136">R8\_UINT</span></span>
-   <span data-ttu-id="5f86a-137">R8 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="5f86a-137">R8\_SINT</span></span>

<span data-ttu-id="5f86a-138">D3D12 和 D3D 11.3 硬體上可選擇性且個別支援下列格式，因此必須在每一種格式上進行單一查詢，以測試支援。</span><span class="sxs-lookup"><span data-stu-id="5f86a-138">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="5f86a-139">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-139">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="5f86a-140">R16G16B16A16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-140">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="5f86a-141">R32G32 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="5f86a-141">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="5f86a-142">R32G32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5f86a-142">R32G32\_UINT</span></span>
-   <span data-ttu-id="5f86a-143">R32G32 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="5f86a-143">R32G32\_SINT</span></span>
-   <span data-ttu-id="5f86a-144">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-144">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="5f86a-145">R10G10B10A2 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5f86a-145">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="5f86a-146">R11G11B10 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="5f86a-146">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="5f86a-147">R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-147">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="5f86a-148">R16G16 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="5f86a-148">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="5f86a-149">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-149">R16G16\_UNORM</span></span>
-   <span data-ttu-id="5f86a-150">R16G16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5f86a-150">R16G16\_UINT</span></span>
-   <span data-ttu-id="5f86a-151">R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-151">R16G16\_SNORM</span></span>
-   <span data-ttu-id="5f86a-152">R16G16 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="5f86a-152">R16G16\_SINT</span></span>
-   <span data-ttu-id="5f86a-153">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-153">R8G8\_UNORM</span></span>
-   <span data-ttu-id="5f86a-154">R8G8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5f86a-154">R8G8\_UINT</span></span>
-   <span data-ttu-id="5f86a-155">R8G8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-155">R8G8\_SNORM</span></span>
-   <span data-ttu-id="5f86a-156">R8G8 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="5f86a-156">R8G8\_SINT</span></span>
-   <span data-ttu-id="5f86a-157">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-157">R16\_UNORM</span></span>
-   <span data-ttu-id="5f86a-158">R16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-158">R16\_SNORM</span></span>
-   <span data-ttu-id="5f86a-159">R8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-159">R8\_SNORM</span></span>
-   <span data-ttu-id="5f86a-160">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-160">A8\_UNORM</span></span>
-   <span data-ttu-id="5f86a-161">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-161">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="5f86a-162">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-162">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="5f86a-163">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5f86a-163">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="5f86a-164">若要判斷是否支援任何其他格式，請使用 [**D3D12 \_ 功能 \_ 資料 \_ D3D12 \_ 選項**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)結構來呼叫 [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) ，做為第一個參數 (參考) 的 [功能查詢](capability-querying.md)。</span><span class="sxs-lookup"><span data-stu-id="5f86a-164">To determine the support for any additional formats, call [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) with the [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure as the first parameter (refer to [Capability Querying](capability-querying.md)).</span></span> <span data-ttu-id="5f86a-165">如果支援上述的「支援為集合」清單，則會設定 *TypedUAVLoadAdditionalFormats* 欄位。</span><span class="sxs-lookup"><span data-stu-id="5f86a-165">The *TypedUAVLoadAdditionalFormats* field will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="5f86a-166">使用 [**D3D12 \_ 功能 \_ 資料 \_ 格式 \_ 支援**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support)結構，對 **CheckFeatureSupport** 進行第二次呼叫， (檢查傳回的結構是否符合 \_ \_ \_ \_ \_ [**UAV \_ 格式 \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2)列舉) 的 D3D12 格式 SUPPORT2 SUPPORT2 具類型的載入成員，以判斷上述選擇性支援格式清單中的支援，例如：</span><span class="sxs-lookup"><span data-stu-id="5f86a-166">Make a second call to **CheckFeatureSupport**, using a [**D3D12\_FEATURE\_DATA\_FORMAT\_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum) to determine support in the list of optionally supported formats listed above, for example:</span></span>

``` syntax
D3D12_FEATURE_DATA_D3D12_OPTIONS FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Cannot assume other formats are supported, so we check:
        D3D12_FEATURE_DATA_FORMAT_SUPPORT FormatSupport = {DXGI_FORMAT_R32G32_FLOAT, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT2_NONE};
        hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_SUPPORT, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.Support2 & D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="5f86a-167">從 HLSL 使用具類型的 UAV 載入</span><span class="sxs-lookup"><span data-stu-id="5f86a-167">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="5f86a-168">針對具類型的 UAVs，HLSL 旗標為 D3D \_ 著色器， \_ 需要具 \_ 類型 \_ \_ 的 UAV 載入 \_ 其他 \_ 格式。</span><span class="sxs-lookup"><span data-stu-id="5f86a-168">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="5f86a-169">以下是處理具型別 UAV 負載的範例著色器程式碼：</span><span class="sxs-lookup"><span data-stu-id="5f86a-169">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a><span data-ttu-id="5f86a-170">使用 UNORM 和 SNORM 具類型的 UAV 從 HLSL 載入</span><span class="sxs-lookup"><span data-stu-id="5f86a-170">Using UNORM and SNORM typed UAV loads from HLSL</span></span>

<span data-ttu-id="5f86a-171">使用具類型的 UAV 載入以從 UNORM 或 SNORM 資源讀取時，您必須將 HLSL 物件的元素類型正確宣告為 `unorm` 或 `snorm` 。</span><span class="sxs-lookup"><span data-stu-id="5f86a-171">When using typed UAV loads to read from a UNORM or SNORM resource, you must properly declare the element type of the HLSL object to be `unorm` or `snorm`.</span></span> <span data-ttu-id="5f86a-172">它會指定為未定義的行為，以將 HLSL 中宣告的元素類型與基礎資源資料類型不相符。</span><span class="sxs-lookup"><span data-stu-id="5f86a-172">It is specified as undefined behavior to mismatch the element type declared in HLSL with the underlying resource data type.</span></span> <span data-ttu-id="5f86a-173">例如，如果您在具有 R8 UNORM 資料的緩衝區資源上使用具類型的 UAV 載入 \_ ，則必須將元素類型宣告為 `unorm float` ：</span><span class="sxs-lookup"><span data-stu-id="5f86a-173">For example, if you are using typed UAV loads on a buffer resource with R8\_UNORM data, then you must declare the element type as `unorm float`:</span></span>

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a><span data-ttu-id="5f86a-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f86a-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f86a-175">轉譯</span><span class="sxs-lookup"><span data-stu-id="5f86a-175">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="5f86a-176">資源系結</span><span class="sxs-lookup"><span data-stu-id="5f86a-176">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="5f86a-177">HLSL 中的資源系結</span><span class="sxs-lookup"><span data-stu-id="5f86a-177">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="5f86a-178">著色器模型5。1</span><span class="sxs-lookup"><span data-stu-id="5f86a-178">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="5f86a-179">在 HLSL 中指定根簽章</span><span class="sxs-lookup"><span data-stu-id="5f86a-179">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 