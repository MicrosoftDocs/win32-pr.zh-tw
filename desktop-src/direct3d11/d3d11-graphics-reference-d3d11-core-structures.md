---
title: Direct3D 11 核心結構
description: 本節包含核心結構的相關資訊。
ms.assetid: 2a45182a-7114-4075-b8b8-147f52fe7aa9
keywords:
- 結構，Direct3D 11 核心
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abf2daccc08066d37c00ed2a4b15a19da35afb8e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473104"
---
# <a name="direct3d-11-core-structures"></a>Direct3D 11 核心結構

本節包含核心結構的相關資訊。

## <a name="in-this-section"></a>本節內容


| 主題 | 描述 | 
|-------|-------------|
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a><br /> | 描述您在呼叫 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device：： CreateBlendState</strong></a> 以建立 blend 狀態物件時所使用的 blend 狀態。 <br /> | 
| <a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a><br /> | <blockquote>[!Note]<br />在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</blockquote><br /> 描述您在呼叫 <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1：： CreateBlendState1</strong></a> 以建立 blend 狀態物件時所使用的 blend 狀態。 <br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a><br /> | 定義3D 方塊。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a><br /> | 描述計數器。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a><br /> | 視訊卡效能計數器功能的相關資訊。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a><br /> | 描述深度樣板的狀態。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a><br /> | 可以根據樣板測試結果來執行的樣板作業。<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a><br /> | 繪製已編制索引之實例間接的引數。 <br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a><br /> | 繪製實例間接的引數。 <br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a><br /> | <blockquote>[!Note]<br />在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</blockquote><br /> 描述 Direct3D 11.1 介面卡架構的相關資訊。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a><br /> | <blockquote>[!Note]<br />在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</blockquote><br /> 描述目前圖形驅動程式中的 Direct3D 9 功能選項。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a><br /> | 描述目前圖形驅動程式中的 Direct3D 9 功能選項。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a><br /> | <blockquote>[!Note]<br />在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</blockquote><br /> 描述目前圖形驅動程式中的 Direct3D 9 陰影支援。 <br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a><br /> | 描述是否支援簡單實例。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a><br /> | 描述目前圖形驅動程式中的計算著色器和原始和結構化緩衝區支援。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a><br /> | <blockquote>[!Note]<br />在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</blockquote><br /> 描述目前圖形驅動程式中的 Direct3D 11.1 功能選項。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a><br /> | 描述目前圖形驅動程式中的 Direct3D 11.2 功能選項。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a><br /> | 描述目前圖形驅動程式中的 Direct3D 11.3 功能選項。<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a><br /> | 描述目前圖形驅動程式中的 Direct3D 11.3 功能選項。<br /> | 
| <a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a><br /> | 描述目前圖形驅動程式中的 Direct3D 11.4 功能選項。<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a><br /> | 描述目前圖形驅動程式中共用資源的支援層級。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a><br /> | 描述目前圖形驅動程式中的雙重資料類型支援。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a><br /> | 描述目前圖形驅動程式支援的資源，以指定的格式。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a><br /> | 描述目前的圖形驅動程式支援指定格式的未排序資源選項。<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a><br /> | 描述功能資料 GPU 虛擬位址支援，包括每個資源和每個進程的最大位址位。 <br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a><br /> | 描述是否支援 GPU 分析技術。<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a><br /> | 描述目前圖形驅動程式所支援的著色器快取層級。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a><br /> | <blockquote>[!Note]<br />在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</blockquote><br /> 描述目前圖形驅動程式中著色器的精確度支援選項。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a><br /> | 描述目前圖形驅動程式所支援的多執行緒功能。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a><br /> | 輸入組合語言階段之單一元素的描述。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a><br /> | 有關圖形的查詢資訊- <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>>id3d11devicecoNtext：： Begin</strong></a> 和 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>>id3d11devicecoNtext：： End</strong></a>呼叫之間的管線活動。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a><br /> | 在 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>>id3d11devicecoNtext：： Begin</strong></a> 和 <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>>id3d11devicecoNtext：： End</strong></a>之間，查詢串流輸出到資料流程輸出緩衝區的資料量相關資訊。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a><br /> | 查詢時間戳記查詢可靠性的相關資訊。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a><br /> | 描述查詢。<br /> | 
| <a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a><br /> | 描述查詢。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a><br /> | 描述轉譯器的狀態。<br /> | 
| <a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a><br /> | <blockquote>[!Note]<br />在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</blockquote><br /> 描述轉譯器的狀態。<br /> | 
| <a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a><br /> | 描述轉譯器的狀態。<br /> | 
| <a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a><br /> | D3D11_RECT 的宣告方式如下：<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a><br /> | 描述呈現目標的 blend 狀態。<br /> | 
| <a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a><br /> | <blockquote>[!Note]<br />在 Windows 8 和更新版本的作業系統上提供的 Direct3D 11.1 執行時間支援此結構。</blockquote><br /> 描述呈現目標的 blend 狀態。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a><br /> | 描述取樣器狀態。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a><br /> | 輸出位置頂點緩衝區中頂點元素的描述。<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a><br /> | 定義區的維度。<br /> | 


此外，D3D11 中有定義2D 矩形結構。

```cpp
typedef RECT D3D11_RECT;
```

如需檔，請參閱[Windows GDI](../gdi/windows-gdi.md)中的[RECT](/previous-versions/dd162897%28v%3dvs.85%29) 。

## <a name="related-topics"></a>相關主題

[核心參考](d3d11-graphics-reference-d3d11-core.md)
