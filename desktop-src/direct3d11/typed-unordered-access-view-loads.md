---
title: 具類型的未排序存取視圖載入
description: 瞭解在 Direct3D 11 中 UAV) 具類型的載入 (未排序的存取視圖。 UAV 具型別的 Load 是可讓著色器從具有特定 DXGI_FORMAT 的 UAV 讀取的能力。
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6d2cbfa51c8473dc3da51c5844c63bef944b50
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396283"
---
# <a name="typed-unordered-access-view-loads"></a><span data-ttu-id="08a6b-104">具類型的未排序存取視圖載入</span><span class="sxs-lookup"><span data-stu-id="08a6b-104">Typed Unordered Access View Loads</span></span>

<span data-ttu-id="08a6b-105">未排序的存取視圖 (UAV) 具類型的負載，是可讓著色器從具有特定 DXGI 格式的 UAV 讀取的能力 \_ 。</span><span class="sxs-lookup"><span data-stu-id="08a6b-105">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span>

-   [<span data-ttu-id="08a6b-106">概觀</span><span class="sxs-lookup"><span data-stu-id="08a6b-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="08a6b-107">支援的格式和 API 呼叫</span><span class="sxs-lookup"><span data-stu-id="08a6b-107">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="08a6b-108">從 HLSL 使用具類型的 UAV 載入</span><span class="sxs-lookup"><span data-stu-id="08a6b-108">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="08a6b-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="08a6b-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="08a6b-110">概觀</span><span class="sxs-lookup"><span data-stu-id="08a6b-110">Overview</span></span>

<span data-ttu-id="08a6b-111">未排序的存取視圖 (UAV) 是未排序存取資源 (的視圖，可包含緩衝區、紋理和材質陣列，但不需要多取樣) 。</span><span class="sxs-lookup"><span data-stu-id="08a6b-111">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="08a6b-112">UAV 可讓您從多個執行緒暫時未排序的讀取/寫入存取。</span><span class="sxs-lookup"><span data-stu-id="08a6b-112">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="08a6b-113">這表示此資源類型可以由多個執行緒同時讀取/寫入，而不會產生記憶體衝突。</span><span class="sxs-lookup"><span data-stu-id="08a6b-113">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="08a6b-114">這項同時存取是透過使用不可部分 [完成的函](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions)式來處理。</span><span class="sxs-lookup"><span data-stu-id="08a6b-114">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="08a6b-115">D3D12 和 D3D 11.3 會展開可搭配具類型 UAV 載入的格式清單。</span><span class="sxs-lookup"><span data-stu-id="08a6b-115">D3D12 and D3D11.3 expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="08a6b-116">支援的格式和 API 呼叫</span><span class="sxs-lookup"><span data-stu-id="08a6b-116">Supported formats and API calls</span></span>

<span data-ttu-id="08a6b-117">先前支援下列三種格式的 UAV 載入，並為 D3D 11.0 硬體所需。</span><span class="sxs-lookup"><span data-stu-id="08a6b-117">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="08a6b-118">所有 D3D 11.3 和 D3D12 硬體都支援它們。</span><span class="sxs-lookup"><span data-stu-id="08a6b-118">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="08a6b-119">R32 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="08a6b-119">R32\_FLOAT</span></span>
-   <span data-ttu-id="08a6b-120">R32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="08a6b-120">R32\_UINT</span></span>
-   <span data-ttu-id="08a6b-121">R32 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="08a6b-121">R32\_SINT</span></span>

<span data-ttu-id="08a6b-122">以下是在 D3D12 或 D3D 11.3 硬體上支援的格式，因此，如果支援任何一種格式，則會支援所有的格式。</span><span class="sxs-lookup"><span data-stu-id="08a6b-122">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="08a6b-123">R32G32B32A32 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="08a6b-123">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="08a6b-124">R32G32B32A32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="08a6b-124">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="08a6b-125">R32G32B32A32 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="08a6b-125">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="08a6b-126">R16G16B16A16 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="08a6b-126">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="08a6b-127">R16G16B16A16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="08a6b-127">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="08a6b-128">R16G16B16A16 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="08a6b-128">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="08a6b-129">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-129">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="08a6b-130">R8G8B8A8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="08a6b-130">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="08a6b-131">R8G8B8A8 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="08a6b-131">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="08a6b-132">R16 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="08a6b-132">R16\_FLOAT</span></span>
-   <span data-ttu-id="08a6b-133">R16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="08a6b-133">R16\_UINT</span></span>
-   <span data-ttu-id="08a6b-134">R16 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="08a6b-134">R16\_SINT</span></span>
-   <span data-ttu-id="08a6b-135">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-135">R8\_UNORM</span></span>
-   <span data-ttu-id="08a6b-136">R8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="08a6b-136">R8\_UINT</span></span>
-   <span data-ttu-id="08a6b-137">R8 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="08a6b-137">R8\_SINT</span></span>

<span data-ttu-id="08a6b-138">D3D12 和 D3D 11.3 硬體上可選擇性且個別支援下列格式，因此必須在每一種格式上進行單一查詢，以測試支援。</span><span class="sxs-lookup"><span data-stu-id="08a6b-138">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="08a6b-139">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-139">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="08a6b-140">R16G16B16A16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-140">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="08a6b-141">R32G32 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="08a6b-141">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="08a6b-142">R32G32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="08a6b-142">R32G32\_UINT</span></span>
-   <span data-ttu-id="08a6b-143">R32G32 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="08a6b-143">R32G32\_SINT</span></span>
-   <span data-ttu-id="08a6b-144">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-144">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="08a6b-145">R10G10B10A2 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="08a6b-145">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="08a6b-146">R11G11B10 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="08a6b-146">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="08a6b-147">R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-147">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="08a6b-148">R16G16 \_ 浮點數</span><span class="sxs-lookup"><span data-stu-id="08a6b-148">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="08a6b-149">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-149">R16G16\_UNORM</span></span>
-   <span data-ttu-id="08a6b-150">R16G16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="08a6b-150">R16G16\_UINT</span></span>
-   <span data-ttu-id="08a6b-151">R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-151">R16G16\_SNORM</span></span>
-   <span data-ttu-id="08a6b-152">R16G16 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="08a6b-152">R16G16\_SINT</span></span>
-   <span data-ttu-id="08a6b-153">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-153">R8G8\_UNORM</span></span>
-   <span data-ttu-id="08a6b-154">R8G8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="08a6b-154">R8G8\_UINT</span></span>
-   <span data-ttu-id="08a6b-155">R8G8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-155">R8G8\_SNORM</span></span>
-   <span data-ttu-id="08a6b-156">8G8 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="08a6b-156">8G8\_SINT</span></span>
-   <span data-ttu-id="08a6b-157">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-157">R16\_UNORM</span></span>
-   <span data-ttu-id="08a6b-158">R16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-158">R16\_SNORM</span></span>
-   <span data-ttu-id="08a6b-159">R8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-159">R8\_SNORM</span></span>
-   <span data-ttu-id="08a6b-160">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-160">A8\_UNORM</span></span>
-   <span data-ttu-id="08a6b-161">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-161">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="08a6b-162">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-162">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="08a6b-163">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="08a6b-163">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="08a6b-164">若要判斷是否支援任何其他格式，請使用 [**D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2)結構來呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)做為第一個參數。</span><span class="sxs-lookup"><span data-stu-id="08a6b-164">To determine the support for any additional formats, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure as the first parameter.</span></span> <span data-ttu-id="08a6b-165">`TypedUAVLoadAdditionalFormats`如果支援上述的「支援為集合」清單，則會設定位。</span><span class="sxs-lookup"><span data-stu-id="08a6b-165">The `TypedUAVLoadAdditionalFormats` bit will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="08a6b-166">使用 [**D3D11 \_ 功能 \_ 資料 \_ 格式 \_ SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2)結構，對 **CheckFeatureSupport** 進行第二次呼叫， (檢查傳回的結構是否針對 \_ \_ \_ \_ \_ [**SUPPORT2 \_ 格式 \_ UAV**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)列舉) 的 D3D12 格式 D3D11 SUPPORT2 具類型的載入成員，以判斷上述選擇性支援格式清單中的支援，例如：</span><span class="sxs-lookup"><span data-stu-id="08a6b-166">Make a second call to **CheckFeatureSupport**, using a [**D3D11\_FEATURE\_DATA\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) enum) to determine support in the list of optionally supported formats above, for example:</span></span>

``` syntax
D3D11_FEATURE_DATA_D3D11_OPTIONS2 FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS2, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Can not assume other formats are supported, so we check:
        D3D11_FEATURE_DATA_FORMAT_SUPPORT2 FormatSupport;
        ZeroMemory(&FormatSupport, sizeof(FormatSupport));
        FormatSupport.InFormat = DXGI_FORMAT_R32G32_FLOAT;
        hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_FORMAT_SUPPORT2, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.OutFormatSupport2 & D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="08a6b-167">從 HLSL 使用具類型的 UAV 載入</span><span class="sxs-lookup"><span data-stu-id="08a6b-167">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="08a6b-168">針對具類型的 UAVs，HLSL 旗標為 D3D \_ 著色器， \_ 需要具 \_ 類型 \_ \_ 的 UAV 載入 \_ 其他 \_ 格式。</span><span class="sxs-lookup"><span data-stu-id="08a6b-168">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="08a6b-169">以下是處理具型別 UAV 負載的範例著色器程式碼：</span><span class="sxs-lookup"><span data-stu-id="08a6b-169">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="related-topics"></a><span data-ttu-id="08a6b-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="08a6b-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08a6b-171">Direct3D 11.3 功能</span><span class="sxs-lookup"><span data-stu-id="08a6b-171">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="08a6b-172">著色器模型5。1</span><span class="sxs-lookup"><span data-stu-id="08a6b-172">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 