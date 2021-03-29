---
title: Direct3D 11 核心結構
description: 本節包含核心結構的相關資訊。
ms.assetid: 2a45182a-7114-4075-b8b8-147f52fe7aa9
keywords:
- 結構，Direct3D 11 核心
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7025de822265d86e5da9f1da3855d2542c76abf5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375988"
---
# <a name="direct3d-11-core-structures"></a><span data-ttu-id="d4316-104">Direct3D 11 核心結構</span><span class="sxs-lookup"><span data-stu-id="d4316-104">Direct3D 11 core structures</span></span>

<span data-ttu-id="d4316-105">本節包含核心結構的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d4316-105">This section contains information about the core structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d4316-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="d4316-106">In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4316-107">主題</span><span class="sxs-lookup"><span data-stu-id="d4316-107">Topic</span></span></th>
<th><span data-ttu-id="d4316-108">描述</span><span class="sxs-lookup"><span data-stu-id="d4316-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4316-109"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-109"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-110">描述您在呼叫 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device：： CreateBlendState</strong></a> 以建立 blend 狀態物件時所使用的 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="d4316-110">Describes the blend state that you use in a call to <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device::CreateBlendState</strong></a> to create a blend-state object.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-111"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-111"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="d4316-112">在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</span><span class="sxs-lookup"><span data-stu-id="d4316-112">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="d4316-113">描述您在呼叫 <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1：： CreateBlendState1</strong></a> 以建立 blend 狀態物件時所使用的 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="d4316-113">Describes the blend state that you use in a call to <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1::CreateBlendState1</strong></a> to create a blend-state object.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-114"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-114"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-115">定義3D 方塊。</span><span class="sxs-lookup"><span data-stu-id="d4316-115">Defines a 3D box.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-116"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-116"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-117">描述計數器。</span><span class="sxs-lookup"><span data-stu-id="d4316-117">Describes a counter.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-118"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-118"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-119">視訊卡效能計數器功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d4316-119">Information about the video card's performance counter capabilities.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-120"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-120"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-121">描述深度樣板的狀態。</span><span class="sxs-lookup"><span data-stu-id="d4316-121">Describes depth-stencil state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-122"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-122"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-123">可以根據樣板測試結果來執行的樣板作業。</span><span class="sxs-lookup"><span data-stu-id="d4316-123">Stencil operations that can be performed based on the results of stencil test.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-124"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-124"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-125">繪製已編制索引之實例間接的引數。</span><span class="sxs-lookup"><span data-stu-id="d4316-125">Arguments for draw indexed instanced indirect.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-126"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-126"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-127">繪製實例間接的引數。</span><span class="sxs-lookup"><span data-stu-id="d4316-127">Arguments for draw instanced indirect.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-128"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-128"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="d4316-129">在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</span><span class="sxs-lookup"><span data-stu-id="d4316-129">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="d4316-130">描述 Direct3D 11.1 介面卡架構的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d4316-130">Describes information about Direct3D 11.1 adapter architecture.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-131"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-131"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="d4316-132">在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</span><span class="sxs-lookup"><span data-stu-id="d4316-132">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="d4316-133">描述目前圖形驅動程式中的 Direct3D 9 功能選項。</span><span class="sxs-lookup"><span data-stu-id="d4316-133">Describes Direct3D 9 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-134"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-134"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-135">描述目前圖形驅動程式中的 Direct3D 9 功能選項。</span><span class="sxs-lookup"><span data-stu-id="d4316-135">Describes Direct3D 9 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-136"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-136"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="d4316-137">在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</span><span class="sxs-lookup"><span data-stu-id="d4316-137">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="d4316-138">描述目前圖形驅動程式中的 Direct3D 9 陰影支援。</span><span class="sxs-lookup"><span data-stu-id="d4316-138">Describes Direct3D 9 shadow support in the current graphics driver.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-139"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-139"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-140">描述是否支援簡單實例。</span><span class="sxs-lookup"><span data-stu-id="d4316-140">Describes whether simple instancing is supported.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-141"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-141"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-142">描述目前圖形驅動程式中的計算著色器和原始和結構化緩衝區支援。</span><span class="sxs-lookup"><span data-stu-id="d4316-142">Describes compute shader and raw and structured buffer support in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-143"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-143"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="d4316-144">在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</span><span class="sxs-lookup"><span data-stu-id="d4316-144">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="d4316-145">描述目前圖形驅動程式中的 Direct3D 11.1 功能選項。</span><span class="sxs-lookup"><span data-stu-id="d4316-145">Describes Direct3D 11.1 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-146"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-146"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-147">描述目前圖形驅動程式中的 Direct3D 11.2 功能選項。</span><span class="sxs-lookup"><span data-stu-id="d4316-147">Describes Direct3D 11.2 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-148"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-148"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-149">描述目前圖形驅動程式中的 Direct3D 11.3 功能選項。</span><span class="sxs-lookup"><span data-stu-id="d4316-149">Describes Direct3D 11.3 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-150"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-150"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-151">描述目前圖形驅動程式中的 Direct3D 11.3 功能選項。</span><span class="sxs-lookup"><span data-stu-id="d4316-151">Describes Direct3D 11.3 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-152"><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-152"><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-153">描述目前圖形驅動程式中的 Direct3D 11.4 功能選項。</span><span class="sxs-lookup"><span data-stu-id="d4316-153">Describes Direct3D 11.4 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-154"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-154"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-155">描述目前圖形驅動程式中共用資源的支援層級。</span><span class="sxs-lookup"><span data-stu-id="d4316-155">Describes the level of support for shared resources in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-156"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-156"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-157">描述目前圖形驅動程式中的雙重資料類型支援。</span><span class="sxs-lookup"><span data-stu-id="d4316-157">Describes double data type support in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-158"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-158"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-159">描述目前圖形驅動程式支援的資源，以指定的格式。</span><span class="sxs-lookup"><span data-stu-id="d4316-159">Describes which resources are supported by the current graphics driver for a given format.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-160"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-160"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-161">描述目前的圖形驅動程式支援指定格式的未排序資源選項。</span><span class="sxs-lookup"><span data-stu-id="d4316-161">Describes which unordered resource options are supported by the current graphics driver for a given format.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-162"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-162"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-163">描述功能資料 GPU 虛擬位址支援，包括每個資源和每個進程的最大位址位。</span><span class="sxs-lookup"><span data-stu-id="d4316-163">Describes feature data GPU virtual address support, including maximum address bits per resource and per process.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-164"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-164"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-165">描述是否支援 GPU 分析技術。</span><span class="sxs-lookup"><span data-stu-id="d4316-165">Describes whether a GPU profiling technique is supported.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-166"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-166"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-167">描述目前圖形驅動程式所支援的著色器快取層級。</span><span class="sxs-lookup"><span data-stu-id="d4316-167">Describes the level of shader caching supported in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-168"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-168"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="d4316-169">在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</span><span class="sxs-lookup"><span data-stu-id="d4316-169">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="d4316-170">描述目前圖形驅動程式中著色器的精確度支援選項。</span><span class="sxs-lookup"><span data-stu-id="d4316-170">Describes precision support options for shaders in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-171"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-171"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-172">描述目前圖形驅動程式所支援的多執行緒功能。</span><span class="sxs-lookup"><span data-stu-id="d4316-172">Describes the multi-threading features that are supported by the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-173"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-173"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-174">輸入組合語言階段之單一元素的描述。</span><span class="sxs-lookup"><span data-stu-id="d4316-174">A description of a single element for the input-assembler stage.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-175"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-175"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-176">有關圖形的查詢資訊- <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>>id3d11devicecoNtext：： Begin</strong></a> 和 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>>id3d11devicecoNtext：： End</strong></a>呼叫之間的管線活動。</span><span class="sxs-lookup"><span data-stu-id="d4316-176">Query information about graphics-pipeline activity in between calls to <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext::Begin</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext::End</strong></a>.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-177"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-177"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-178">在 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>>id3d11devicecoNtext：： Begin</strong></a> 和 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>>id3d11devicecoNtext：： End</strong></a>之間，查詢串流輸出到資料流程輸出緩衝區的資料量相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d4316-178">Query information about the amount of data streamed out to the stream-output buffers in between <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext::Begin</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext::End</strong></a>.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-179"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-179"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-180">查詢時間戳記查詢可靠性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d4316-180">Query information about the reliability of a timestamp query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-181"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-181"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-182">描述查詢。</span><span class="sxs-lookup"><span data-stu-id="d4316-182">Describes a query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-183"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-183"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-184">描述查詢。</span><span class="sxs-lookup"><span data-stu-id="d4316-184">Describes a query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-185"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-185"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-186">描述轉譯器的狀態。</span><span class="sxs-lookup"><span data-stu-id="d4316-186">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-187"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-187"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="d4316-188">在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</span><span class="sxs-lookup"><span data-stu-id="d4316-188">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="d4316-189">描述轉譯器的狀態。</span><span class="sxs-lookup"><span data-stu-id="d4316-189">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-190"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-190"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-191">描述轉譯器的狀態。</span><span class="sxs-lookup"><span data-stu-id="d4316-191">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-192"><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-192"><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-193">D3D11_RECT 的宣告方式如下：</span><span class="sxs-lookup"><span data-stu-id="d4316-193">D3D11_RECT is declared as follows:</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-194"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-194"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-195">描述呈現目標的 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="d4316-195">Describes the blend state for a render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-196"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-196"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="d4316-197">在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</span><span class="sxs-lookup"><span data-stu-id="d4316-197">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="d4316-198">描述呈現目標的 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="d4316-198">Describes the blend state for a render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-199"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-199"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-200">描述取樣器狀態。</span><span class="sxs-lookup"><span data-stu-id="d4316-200">Describes a sampler state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-201"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-201"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-202">輸出位置頂點緩衝區中頂點元素的描述。</span><span class="sxs-lookup"><span data-stu-id="d4316-202">Description of a vertex element in a vertex buffer in an output slot.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="d4316-203"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4316-203"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d4316-204">定義區的維度。</span><span class="sxs-lookup"><span data-stu-id="d4316-204">Defines the dimensions of a viewport.</span></span><br/></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4316-205">此外，D3D11 中有定義2D 矩形結構。</span><span class="sxs-lookup"><span data-stu-id="d4316-205">In addition, there's a 2D rectangle structure defined in D3D11.h.</span></span>

```cpp
typedef RECT D3D11_RECT;
```

<span data-ttu-id="d4316-206">如需檔，請參閱[WINDOWS GDI](../gdi/windows-gdi.md)中的[RECT](/previous-versions/dd162897%28v%3dvs.85%29) 。</span><span class="sxs-lookup"><span data-stu-id="d4316-206">For documentation, see [RECT](/previous-versions/dd162897%28v%3dvs.85%29) in [Windows GDI](../gdi/windows-gdi.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4316-207">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4316-207">Related topics</span></span>

[<span data-ttu-id="d4316-208">核心參考</span><span class="sxs-lookup"><span data-stu-id="d4316-208">Core Reference</span></span>](d3d11-graphics-reference-d3d11-core.md)