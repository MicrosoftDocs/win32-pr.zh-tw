---
description: 本節包含下列核心結構的相關資訊：
ms.assetid: 84769515-3f3b-4464-9620-7b806bf905b3
title: Direct3D 10 核心結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de2260b108ea340a97f24acf61f6ae686e00342
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689212"
---
# <a name="direct3d-10-core-structures"></a>Direct3D 10 核心結構

本節包含下列核心結構的相關資訊：



| 結構                                                                               | Description                                                          |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)                                           | Direct3D 10.0 裝置的混合選項。                         |
| [**D3D10 \_ BLEND \_ DESC1**](/windows/desktop/api/D3D10_1/ns-d3d10_1-d3d10_blend_desc1)                                         | Direct3D 10.1 裝置的混合選項。                         |
| [**D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)                                                          | 矩形區域，通常是在材質中。                            |
| [**D3D10 \_ 計數器 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_counter_desc)                                       | 效能計數器描述。                                   |
| [**D3D10 \_ 計數器 \_ 資訊**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_counter_info)                                       | 視訊卡效能計數器功能的相關資訊。 |
| [**D3D10 \_ 深度 \_ 樣板 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)                          | 深度樣板描述。                                         |
| [**D3D10 \_ 深度 \_ STENCILOP \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)                      | 深度樣板操作。                                           |
| [**D3D10 \_ 資訊 \_ 佇列 \_ 篩選**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter)                            | Debug 訊息篩選器。                                              |
| [**D3D10 \_ 資訊 \_ 佇列 \_ 篩選 \_ DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc)                 | 偵錯工具訊息篩選描述。                                  |
| [**D3D10 \_ 輸入 \_ 元素 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                          | 輸入位置的頂點緩衝區元素描述。               |
| [**D3D10 \_ 查詢 \_ 資料 \_ 管線 \_ 統計資料**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_query_data_pipeline_statistics) | 管線查詢統計資料。                                           |
| [**D3D10 \_ 查詢 \_ 資料 \_ 的 \_ 統計資料**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_query_data_so_statistics)             | 資料流程輸出階段查詢統計資料。                                |
| [**D3D10 \_ 查詢 \_ 資料 \_ 時間戳記不 \_ 相交**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_query_data_timestamp_disjoint)   | 時間戳記查詢統計資料。                                          |
| [**D3D10 \_ 查詢 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_query_desc)                                           | 查詢描述。                                                 |
| [**D3D10 \_ 訊息**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_message)                                                  | 資訊佇列的偵錯工具訊息。                           |
| [**D3D10 轉譯器 \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                 | 轉譯器-階段描述。                                        |
| [**D3D10 \_ RECT**](d3d10-rect.md)                                                        | 2D 矩形。                                                      |
| [**D3D10 \_ 轉譯 \_ 目標 \_ BLEND \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1)           | Direct3D 10.1 轉譯目標的混合選項。                  |
| [**D3D10 \_ 取樣器 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)                                       | 取樣器描述。                                               |
| [**D3D10 \_ 著色器 \_ 資源 \_ 視圖 \_ DESC**](/windows/desktop/api/d3d10/ns-d3d10-d3d10_shader_resource_view_desc)           | 描述適用于 Direct3D 10.0 的著色器資源檢視。                  |
| [**D3D10 \_ 著色器 \_ 資源 \_ 視圖 \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_shader_resource_view_desc1)         | 描述適用于 Direct3D 10.1 的著色器資源檢視。                  |
| [**D3D10 \_ 簽名 \_ 參數 \_ DESC**](/windows/desktop/api/D3D10Shader/ns-d3d10shader-d3d10_signature_parameter_desc)              | 著色器參數描述。                                      |
| [**D3D10 \_ 狀態 \_ 區塊 \_ 遮罩**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask)                              | 狀態區塊遮罩。                                                  |
| [**D3D10 \_ 宣告 \_ \_ 專案**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_so_declaration_entry)                      | 輸出位置的頂點緩衝區元素描述。              |
| [**D3D10 \_ 區**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)                                                | 視口維度。                                                 |



 

此外，d3d10 中有定義2D 矩形結構。


```
typedef RECT D3D10_RECT;
```



如需檔，請參閱 [RECT](/previous-versions//ms536136(v=vs.85))。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[核心參考](d3d10-graphics-reference-d3d10-core.md)
</dt> </dl>

 

 
