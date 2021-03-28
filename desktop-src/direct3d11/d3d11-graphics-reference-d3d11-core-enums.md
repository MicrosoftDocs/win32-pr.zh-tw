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
# <a name="direct3d-11-core-enumerations"></a>Direct3D 11 核心列舉

本節包含核心列舉的相關資訊。

## <a name="in-this-section"></a>本節內容

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_async_getdata_flag"><strong>D3D11_ASYNC_GETDATA_FLAG</strong></a><br/></td>
<td>控制 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-getdata"><strong>>id3d11devicecoNtext：：</strong></a>行為的選擇性旗標。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend"><strong>D3D11_BLEND</strong></a><br/></td>
<td>Blend 因數，lambert 圖元著色器和轉譯目標的值。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend_op"><strong>D3D11_BLEND_OP</strong></a><br/></td>
<td>RGB 或 Alpha 混色運算。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_clear_flag"><strong>D3D11_CLEAR_FLAG</strong></a><br/></td>
<td>指定要清除之深度樣板的部分。 <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_color_write_enable"><strong>D3D11_COLOR_WRITE_ENABLE</strong></a><br/></td>
<td>找出轉譯目標的每個圖元元件在混合期間可寫入的元件。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_comparison_func"><strong>D3D11_COMPARISON_FUNC</strong></a><br/></td>
<td>比較選項。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode"><strong>D3D11_CONSER加值稅IVE_RASTERIZATION_MODE</strong></a><br/></td>
<td>識別是否開啟或關閉保守的點陣化。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier"><strong>D3D11_CONSER加值稅IVE_RASTERIZATION_TIER</strong></a><br/></td>
<td>指定硬體和驅動程式是否支援保守的點陣化和層級。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_context_type"><strong>D3D11_CONTEXT_TYPE</strong></a><br/></td>
<td>指定進行查詢的內容。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_copy_flags"><strong>D3D11_COPY_FLAGS</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此列舉。
</blockquote>
<br/> 指定在該資源內的區域複製或更新作業期間，如何處理現有的資源內容。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter"><strong>D3D11_COUNTER</strong></a><br/></td>
<td>效能計數器的選項。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter_type"><strong>D3D11_COUNTER_TYPE</strong></a><br/></td>
<td>效能計數器的資料類型。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_create_device_flag"><strong>D3D11_CREATE_DEVICE_FLAG</strong></a><br/></td>
<td>描述用來建立裝置的參數。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_1_create_device_context_state_flag"><strong>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</strong></a><br/></td>
<td>描述用來建立裝置內容狀態物件的旗標， (<a href="/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceCoNtextState</strong></a>) 與 <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate"><strong>ID3D11Device1：： CreateDeviceCoNtextState</strong></a> 方法。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_cull_mode"><strong>D3D11_CULL_MODE</strong></a><br/></td>
<td>表示不繪製面向特定方向的三角形。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_depth_write_mask"><strong>D3D11_DEPTH_WRITE_MASK</strong></a><br/></td>
<td>識別深度樣板緩衝區中用來寫入深度資料的部分。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_device_context_type"><strong>D3D11_DEVICE_CONTEXT_TYPE</strong></a><br/></td>
<td>裝置內容選項。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE</strong></a><br/></td>
<td>Direct3D 11 功能選項。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11_3/ne-d3d11_3-d3d11_fence_flag"><strong>D3D11_FENCE_FLAG</strong></a><br/></td>
<td>指定範圍選項。 <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_fill_mode"><strong>D3D11_FILL_MODE</strong></a><br/></td>
<td>決定呈現三角形時要使用的填滿模式。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter"><strong>D3D11_FILTER</strong></a><br/></td>
<td>紋理取樣期間的篩選選項。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter_type"><strong>D3D11_FILTER_TYPE</strong></a><br/></td>
<td>放大或縮制取樣器篩選的類型。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_filter_reduction_type"><strong>D3D11_FILTER_REDUCTION_TYPE</strong></a><br/></td>
<td>指定減少取樣器篩選的類型。 <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a><br/></td>
<td>指定的格式和指定的裝置支援哪些資源 (請參閱 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkformatsupport"><strong>ID3D11Device：： CheckFormatSupport</strong></a> 和 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device：： CheckFeatureSupport</strong></a>) 。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a><br/></td>
<td>計算著色器資源的未排序資源支援選項 (參閱 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device：： CheckFeatureSupport</strong></a>) 。 <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_input_classification"><strong>D3D11_INPUT_CLASSIFICATION</strong></a><br/></td>
<td>輸入位置中包含的資料類型。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_logic_op"><strong>D3D11_LOGIC_OP</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此列舉。
</blockquote>
<br/> 指定要為呈現目標設定的邏輯作業。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive"><strong>D3D11_PRIMITIVE</strong></a><br/></td>
<td>指出管線如何解讀幾何或輪廓著色器輸入基本專案。 <br/></td>
</tr>
<tr>
<td><a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)"><strong>D3D11_PRIMITIVE_TOPOLOGY</strong></a><br/></td>
<td>管線如何解讀系結至輸入組合語言階段的頂點資料。 這些基本拓撲值會決定在螢幕上呈現頂點資料的方式。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query"><strong>D3D11_QUERY</strong></a><br/></td>
<td>查詢類型。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query_misc_flag"><strong>D3D11_QUERY_MISC_FLAG</strong></a><br/></td>
<td>描述其他查詢行為的旗標。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_raise_flag"><strong>D3D11_RAISE_FLAG</strong></a><br/></td>
<td>選項 (s) 將錯誤引發至非持續性例外狀況。<br/></td>
</tr>
<tr>
<td><a href="https://www.bing.com/search?q=<strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong>"><strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong></a><br/></td>
<td>描述目前圖形驅動程式中著色器快取的支援層級。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_shader_min_precision_support"><strong>D3D11_SHADER_MIN_PRECISION_SUPPORT</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此列舉。
</blockquote>
<br/> 在著色器階段指定最小有效位數層級的值。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_shared_resource_tier"><strong>D3D11_SHARED_RESOURCE_TIER</strong></a><br/></td>
<td>定義常數，指定共用資源支援的層級。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_stencil_op"><strong>D3D11_STENCIL_OP</strong></a><br/></td>
<td>可以在深度樣板測試期間執行的樣板作業。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode"><strong>D3D11_TEXTURE_ADDRESS_MODE</strong></a><br/></td>
<td>識別用來解析材質範圍外之材質座標的技巧。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texturecube_face"><strong>D3D11_TEXTURECUBE_FACE</strong></a><br/></td>
<td>立方體材質的不同臉部。<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier"><strong>D3D11_TILED_RESOURCES_TIER</strong></a><br/></td>
<td>指出支援並排資源的階層層級。<br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>相關主題

[核心參考](d3d11-graphics-reference-d3d11-core.md)