---
description: 本節包含下列核心列舉的相關資訊：
ms.assetid: 3d1541bf-75d8-459d-a912-4068e9a0a9e4
title: Direct3D 10 核心列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe6e9b6c4e0ae472cca081b1bd3dfce06c7839e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317888"
---
# <a name="direct3d-10-core-enumerations"></a>Direct3D 10 核心列舉

本節包含下列核心列舉的相關資訊：



| 列舉型別                                                               | 描述                                                                                                                                         |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D10 \_ ASYNC \_ \_ 旗標**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_async_getdata_flag)           | 選擇性旗標，可控制透過呼叫 [**ID3D10Asynchronous：：**](/windows/desktop/api/D3D10/nf-d3d10-id3d10asynchronous-getdata)來取出資料時所發生的情況。       |
| [**D3D10 \_ BLEND**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend)                                       | Blend 選項。                                                                                                                                      |
| [**D3D10 \_ BLEND \_ OP**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend_op)                                | 在來源與目的地圖元之間混合作業。                                                                                          |
| [**D3D10 \_ CLEAR \_ 旗標**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_clear_flag)                            | 指定要清除之深度樣板的哪些部分。                                                                                                |
| [**D3D10 \_ 色彩 \_ 寫入 \_ 啟用**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_color_write_enable)           | 色彩書寫遮罩。                                                                                                                                |
| [**D3D10 \_ 比較 \_ FUNC**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_comparison_func)                  | 比較函數。                                                                                                                               |
| [**D3D10 \_ 計數器**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_counter)                                   | 效能計數器的類型。                                                                                                                      |
| [**D3D10 \_ 計數器 \_ 類型**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_counter_type)                        | 計數器的資料類型。                                                                                                                             |
| [**D3D10 \_ 建立 \_ 裝置 \_ 旗標**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)           | 裝置建立旗標。                                                                                                                              |
| [**D3D10 的 \_ 挑選 \_ 模式**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode)                              | 轉譯器的挑選模式。                                                                                                                              |
| [**D3D10 \_ 深度 \_ 寫入 \_ 遮罩**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_depth_write_mask)               | 判斷深度樣板的哪個部分是可寫入的。                                                                                          |
| [**D3D10 \_ 裝置 \_ 狀態 \_ 類型**](/windows/desktop/api/D3D10Effect/ne-d3d10effect-d3d10_device_state_types)           | 用於 [**ID3D10StateBlock 介面**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10stateblock) 函式呼叫。                                                                      |
| [**D3D10 \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)                          | 設備磁碟機的類型。                                                                                                                              |
| [**D3D10 功能 1-1 \_ \_**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)                    | 硬體加速的版本。                                                                                                               |
| [**D3D10 \_ 填滿 \_ 模式**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode)                              | 轉譯器填滿模式。                                                                                                                              |
| [**D3D10 \_ 篩選**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_filter)                                     | 取樣器篩選的類型。                                                                                                                           |
| [**D3D10 \_ 篩選器 \_ 類型**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_filter_type)                          | 紋理取樣篩選器的類型。                                                                                                                  |
| [**D3D10 \_ 格式 \_ 支援**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_format_support)                    | 指定的格式和指定的裝置支援哪些資源。 請參閱 [**ID3D10Device：： CheckFormatSupport**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-checkformatsupport)。 |
| [**D3D10 \_ 輸入 \_ 分類**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_input_classification)        | 輸入資料的類型。                                                                                                                                |
| [**D3D10 \_ 訊息 \_ 類別**](/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_category)                | Debug 訊息的類別。                                                                                                                       |
| [**D3D10 \_ 訊息 \_ 識別碼**](/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_id)                            | Debug 訊息的唯一識別碼。                                                                                                                        |
| [**D3D10 \_ 訊息 \_ 嚴重性**](/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity)                | Debug 訊息的嚴重性。                                                                                                                        |
| [**D3D10 \_ 基本 \_ 拓撲**](/previous-versions/windows/desktop/legacy/bb205334(v=vs.85))            | 基本拓撲的類型或基本資料的相片順序。                                                                              |
| [**D3D10 \_ 查詢**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_query)                                       | 查詢的類型。                                                                                                                                   |
| [**D3D10 \_ 查詢 \_ 其他 \_ 旗標**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_query_misc_flag)                 | 描述其他查詢行為的旗標。                                                                                                   |
| [**D3D10 \_ 引發 \_ 旗標**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_raise_flag)                            | 指出如何處理內部驅動程式錯誤的旗標。                                                                                           |
| [**D3D10 \_ 註冊 \_ 元件 \_ 類型**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_register_component_type) | 註冊元件類型，通常用於 D3D10 簽 [**章 \_ \_ 參數 \_ DESC**](/windows/desktop/api/D3D10Shader/ns-d3d10shader-d3d10_signature_parameter_desc)。                          |
| [**D3D10 \_ 資源 \_ 傳回 \_ 類型**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_resource_return_type)       | 資源的傳回型別。 請參閱 [**D3D10 \_ 著色器輸入系結 \_ \_ \_ DESC**](/windows/desktop/api/D3D10Shader/ns-d3d10shader-d3d10_shader_input_bind_desc)。                                        |
| [**D3D10 \_ 樣板 \_ OP**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_stencil_op)                            | 樣板作業。                                                                                                                                 |
| [**D3D10 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texture_address_mode)       | 材質座標超出材質界限時要執行的動作。                                                             |
| [**D3D10 \_ TEXTURECUBE \_ 臉**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texturecube_face)                | 立方體材質的不同臉部。                                                                                                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[核心參考](d3d10-graphics-reference-d3d10-core.md)
</dt> </dl>

 

 
