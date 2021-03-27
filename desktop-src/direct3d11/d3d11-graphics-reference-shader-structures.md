---
title: " (Direct3D 11 圖形) 的著色器結構"
description: 結構是用來建立和使用著色器。
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- 結構，Direct3D 11 著色器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14739e3db38c075e19e58a90b12bbf7d06b48a4e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685430"
---
# <a name="shader-structures-direct3d-11-graphics"></a> (Direct3D 11 圖形) 的著色器結構

結構是用來建立和使用著色器。


## <a name="in-this-section"></a>本節內容



| 主題                                                                                       | 描述                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**D3D11 \_ 類別 \_ 實例 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | 描述 HLSL 類別實例。<br/>                           |
| [**D3D11 \_ 計算 \_ 著色器 \_ 追蹤 \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | 描述要追蹤的計算著色器實例。<br/>         |
| [**D3D11 \_ 網域 \_ 著色器 \_ 追蹤 \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | 描述要追蹤之網域著色器的實例。<br/>          |
| [**D3D11 \_ 函數 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | 描述函數。<br/>                                       |
| [**D3D11 \_ 幾何 \_ 著色器 \_ 追蹤 \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | 描述要追蹤之幾何著色器的實例。<br/>        |
| [**D3D11 \_ 輪廓 \_ 著色器 \_ 追蹤 \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | 描述要追蹤的輪廓著色器實例。<br/>            |
| [**D3D11 連結 \_ 庫 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | 描述程式庫。<br/>                                        |
| [**D3D11 \_ 參數 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | 描述函數參數。 <br/>                            |
| [**D3D11 \_ 圖元 \_ 著色器 \_ 追蹤 \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | 描述要追蹤之圖元著色器的實例。<br/>           |
| [**D3D11 \_ 著色器 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | 描述著色器常數緩衝區。<br/>                         |
| [**D3D11 \_ 著色器 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | 描述著色器。<br/>                                         |
| [**D3D11 \_ 著色器輸入系結 \_ \_ \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | 描述著色器資源系結至著色器輸入的方式。<br/> |
| [**D3D11 \_ 著色器 \_ 追蹤 \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | 描述著色器追蹤物件。<br/>                            |
| [**D3D11 \_ 著色器 \_ 類型 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | 描述著色器變數型別。<br/>                           |
| [**D3D11 \_ 著色器 \_ 變數 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | 描述著色器變數。<br/>                                |
| [**D3D11 \_ 簽名 \_ 參數 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | 描述著色器簽章。<br/>                               |
| [**D3D11 \_ 追蹤 \_ 註冊**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | 描述追蹤註冊。<br/>                                 |
| [**D3D11 \_ 追蹤 \_ 統計資料**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | 指定追蹤的相關統計資料。<br/>                         |
| [**D3D11 \_ 追蹤 \_ 步驟**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | 描述追蹤步驟，這是一個指令。<br/>            |
| [**D3D11 \_ 追蹤 \_ 值**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | 描述追蹤值。<br/>                                    |
| [**D3D11 \_ 頂點 \_ 著色器 \_ 追蹤 \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | 描述要追蹤之頂點著色器的實例。<br/>          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器參考](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





