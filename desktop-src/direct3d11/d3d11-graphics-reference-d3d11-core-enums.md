---
title: Direct3D 11 核心列舉
description: 本節包含核心列舉的相關資訊。
ms.assetid: 1641713a-5ac8-4597-900b-1bba54f9f522
keywords:
- 列舉，Direct3D 11 核心
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b012ae34367ef849bebf3fb25780310fcb924ba9
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383217"
---
# <a name="direct3d-11-core-enumerations"></a><span data-ttu-id="e2bf2-104">Direct3D 11 核心列舉</span><span class="sxs-lookup"><span data-stu-id="e2bf2-104">Direct3D 11 core enumerations</span></span>

<span data-ttu-id="e2bf2-105">本節包含核心列舉的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-105">This section contains information about the core enumerations.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e2bf2-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="e2bf2-106">In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e2bf2-107">主題</span><span class="sxs-lookup"><span data-stu-id="e2bf2-107">Topic</span></span></th>
<th><span data-ttu-id="e2bf2-108">描述</span><span class="sxs-lookup"><span data-stu-id="e2bf2-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e2bf2-109"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_async_getdata_flag"><strong>D3D11_ASYNC_GETDATA_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-109"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_async_getdata_flag"><strong>D3D11_ASYNC_GETDATA_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-110">控制 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-getdata"><strong>>id3d11devicecoNtext：：</strong></a>行為的選擇性旗標。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-110">Optional flags that control the behavior of <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-getdata"><strong>ID3D11DeviceContext::GetData</strong></a>.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-111"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend"><strong>D3D11_BLEND</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-111"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend"><strong>D3D11_BLEND</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-112">Blend 因數，lambert 圖元著色器和轉譯目標的值。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-112">Blend factors, which modulate values for the pixel shader and render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-113"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend_op"><strong>D3D11_BLEND_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-113"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend_op"><strong>D3D11_BLEND_OP</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-114">RGB 或 Alpha 混色運算。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-114">RGB or alpha blending operation.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-115"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_clear_flag"><strong>D3D11_CLEAR_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-115"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_clear_flag"><strong>D3D11_CLEAR_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-116">指定要清除之深度樣板的部分。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-116">Specifies the parts of the depth stencil to clear.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-117"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_color_write_enable"><strong>D3D11_COLOR_WRITE_ENABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-117"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_color_write_enable"><strong>D3D11_COLOR_WRITE_ENABLE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-118">找出轉譯目標的每個圖元元件在混合期間可寫入的元件。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-118">Identify which components of each pixel of a render target are writable during blending.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-119"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_comparison_func"><strong>D3D11_COMPARISON_FUNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-119"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_comparison_func"><strong>D3D11_COMPARISON_FUNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-120">比較選項。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-120">Comparison options.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-121"><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode"><strong>D3D11_CONSER加值稅IVE_RASTERIZATION_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-121"><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode"><strong>D3D11_CONSERVATIVE_RASTERIZATION_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-122">識別是否開啟或關閉保守的點陣化。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-122">Identifies whether conservative rasterization is on or off.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-123"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier"><strong>D3D11_CONSER加值稅IVE_RASTERIZATION_TIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-123"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier"><strong>D3D11_CONSERVATIVE_RASTERIZATION_TIER</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-124">指定硬體和驅動程式是否支援保守的點陣化和層級。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-124">Specifies if the hardware and driver support conservative rasterization and at what tier level.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-125"><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_context_type"><strong>D3D11_CONTEXT_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-125"><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_context_type"><strong>D3D11_CONTEXT_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-126">指定進行查詢的內容。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-126">Specifies the context in which a query occurs.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-127"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_copy_flags"><strong>D3D11_COPY_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-127"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_copy_flags"><strong>D3D11_COPY_FLAGS</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="e2bf2-128">在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此列舉。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-128">This enumeration is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="e2bf2-129">指定在該資源內的區域複製或更新作業期間，如何處理現有的資源內容。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-129">Specifies how to handle the existing contents of a resource during a copy or update operation of a region within that resource.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-130"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter"><strong>D3D11_COUNTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-130"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter"><strong>D3D11_COUNTER</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-131">效能計數器的選項。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-131">Options for performance counters.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-132"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter_type"><strong>D3D11_COUNTER_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-132"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter_type"><strong>D3D11_COUNTER_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-133">效能計數器的資料類型。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-133">Data type of a performance counter.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-134"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_create_device_flag"><strong>D3D11_CREATE_DEVICE_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-134"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_create_device_flag"><strong>D3D11_CREATE_DEVICE_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-135">描述用來建立裝置的參數。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-135">Describes parameters that are used to create a device.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-136"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_1_create_device_context_state_flag"><strong>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-136"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_1_create_device_context_state_flag"><strong>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-137">描述用來建立裝置內容狀態物件的旗標， (<a href="/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceCoNtextState</strong></a>) 與 <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate"><strong>ID3D11Device1：： CreateDeviceCoNtextState</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-137">Describes flags that are used to create a device context state object (<a href="/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a>) with the <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate"><strong>ID3D11Device1::CreateDeviceContextState</strong></a> method.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-138"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_cull_mode"><strong>D3D11_CULL_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-138"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_cull_mode"><strong>D3D11_CULL_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-139">表示不繪製面向特定方向的三角形。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-139">Indicates triangles facing a particular direction are not drawn.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-140"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_depth_write_mask"><strong>D3D11_DEPTH_WRITE_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-140"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_depth_write_mask"><strong>D3D11_DEPTH_WRITE_MASK</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-141">識別深度樣板緩衝區中用來寫入深度資料的部分。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-141">Identify the portion of a depth-stencil buffer for writing depth data.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-142"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_device_context_type"><strong>D3D11_DEVICE_CONTEXT_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-142"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_device_context_type"><strong>D3D11_DEVICE_CONTEXT_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-143">裝置內容選項。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-143">Device context options.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-144"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-144"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-145">Direct3D 11 功能選項。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-145">Direct3D 11 feature options.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-146"><a href="/windows/win32/api/d3d11_3/ne-d3d11_3-d3d11_fence_flag"><strong>D3D11_FENCE_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-146"><a href="/windows/win32/api/d3d11_3/ne-d3d11_3-d3d11_fence_flag"><strong>D3D11_FENCE_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-147">指定範圍選項。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-147">Specifies fence options.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-148"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_fill_mode"><strong>D3D11_FILL_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-148"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_fill_mode"><strong>D3D11_FILL_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-149">決定呈現三角形時要使用的填滿模式。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-149">Determines the fill mode to use when rendering triangles.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-150"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter"><strong>D3D11_FILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-150"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter"><strong>D3D11_FILTER</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-151">紋理取樣期間的篩選選項。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-151">Filtering options during texture sampling.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-152"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter_type"><strong>D3D11_FILTER_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-152"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter_type"><strong>D3D11_FILTER_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-153">放大或縮制取樣器篩選的類型。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-153">Types of magnification or minification sampler filters.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-154"><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_filter_reduction_type"><strong>D3D11_FILTER_REDUCTION_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-154"><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_filter_reduction_type"><strong>D3D11_FILTER_REDUCTION_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-155">指定減少取樣器篩選的類型。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-155">Specifies the type of sampler filter reduction.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-156"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-156"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-157">指定的格式和指定的裝置支援哪些資源 (請參閱 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkformatsupport"><strong>ID3D11Device：： CheckFormatSupport</strong></a> 和 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device：： CheckFeatureSupport</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-157">Which resources are supported for a given format and given device (see <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkformatsupport"><strong>ID3D11Device::CheckFormatSupport</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a>).</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-158"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-158"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-159">計算著色器資源的未排序資源支援選項 (參閱 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device：： CheckFeatureSupport</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-159">Unordered resource support options for a compute shader resource (see <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a>).</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-160"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_input_classification"><strong>D3D11_INPUT_CLASSIFICATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-160"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_input_classification"><strong>D3D11_INPUT_CLASSIFICATION</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-161">輸入位置中包含的資料類型。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-161">Type of data contained in an input slot.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-162"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_logic_op"><strong>D3D11_LOGIC_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-162"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_logic_op"><strong>D3D11_LOGIC_OP</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="e2bf2-163">在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此列舉。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-163">This enumeration is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="e2bf2-164">指定要為呈現目標設定的邏輯作業。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-164">Specifies logical operations to configure for a render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-165"><a href="/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive"><strong>D3D11_PRIMITIVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-165"><a href="/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive"><strong>D3D11_PRIMITIVE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-166">指出管線如何解讀幾何或輪廓著色器輸入基本專案。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-166">Indicates how the pipeline interprets geometry or hull shader input primitives.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-167"><a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)"><strong>D3D11_PRIMITIVE_TOPOLOGY</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-167"><a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)"><strong>D3D11_PRIMITIVE_TOPOLOGY</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-168">管線如何解讀系結至輸入組合語言階段的頂點資料。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-168">How the pipeline interprets vertex data that is bound to the input-assembler stage.</span></span> <span data-ttu-id="e2bf2-169">這些基本拓撲值會決定在螢幕上呈現頂點資料的方式。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-169">These primitive topology values determine how the vertex data is rendered on screen.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-170"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query"><strong>D3D11_QUERY</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-170"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query"><strong>D3D11_QUERY</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-171">查詢類型。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-171">Query types.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-172"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query_misc_flag"><strong>D3D11_QUERY_MISC_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-172"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query_misc_flag"><strong>D3D11_QUERY_MISC_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-173">描述其他查詢行為的旗標。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-173">Flags that describe miscellaneous query behavior.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-174"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_raise_flag"><strong>D3D11_RAISE_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-174"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_raise_flag"><strong>D3D11_RAISE_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-175">選項 (s) 將錯誤引發至非持續性例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-175">Option(s) for raising an error to a non-continuable exception.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-176"><a href="https://www.bing.com/search?q=<strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong>"><strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-176"><a href="https://www.bing.com/search?q=<strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong>"><strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-177">描述目前圖形驅動程式中著色器快取的支援層級。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-177">Describes the level of support for shader caching in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-178"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_shader_min_precision_support"><strong>D3D11_SHADER_MIN_PRECISION_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-178"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_shader_min_precision_support"><strong>D3D11_SHADER_MIN_PRECISION_SUPPORT</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="e2bf2-179">在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此列舉。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-179">This enumeration is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="e2bf2-180">在著色器階段指定最小有效位數層級的值。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-180">Values that specify minimum precision levels at shader stages.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-181"><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_shared_resource_tier"><strong>D3D11_SHARED_RESOURCE_TIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-181"><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_shared_resource_tier"><strong>D3D11_SHARED_RESOURCE_TIER</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-182">定義常數，指定共用資源支援的層級。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-182">Defines constants that specify a tier for shared resource support.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-183"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_stencil_op"><strong>D3D11_STENCIL_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-183"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_stencil_op"><strong>D3D11_STENCIL_OP</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-184">可以在深度樣板測試期間執行的樣板作業。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-184">The stencil operations that can be performed during depth-stencil testing.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-185"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode"><strong>D3D11_TEXTURE_ADDRESS_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-185"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode"><strong>D3D11_TEXTURE_ADDRESS_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-186">識別用來解析材質範圍外之材質座標的技巧。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-186">Identify a technique for resolving texture coordinates that are outside of the boundaries of a texture.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-187"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texturecube_face"><strong>D3D11_TEXTURECUBE_FACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-187"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texturecube_face"><strong>D3D11_TEXTURECUBE_FACE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-188">立方體材質的不同臉部。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-188">The different faces of a cube texture.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="e2bf2-189"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier"><strong>D3D11_TILED_RESOURCES_TIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2bf2-189"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier"><strong>D3D11_TILED_RESOURCES_TIER</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2bf2-190">指出支援並排資源的階層層級。</span><span class="sxs-lookup"><span data-stu-id="e2bf2-190">Indicates the tier level at which tiled resources are supported.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="e2bf2-191">相關主題</span><span class="sxs-lookup"><span data-stu-id="e2bf2-191">Related topics</span></span>

[<span data-ttu-id="e2bf2-192">核心參考</span><span class="sxs-lookup"><span data-stu-id="e2bf2-192">Core reference</span></span>](d3d11-graphics-reference-d3d11-core.md)