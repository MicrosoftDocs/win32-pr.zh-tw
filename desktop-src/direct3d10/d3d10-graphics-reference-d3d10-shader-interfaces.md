---
description: 本節包含下列著色器介面的相關資訊：
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: " (Direct3D 10 圖形) 的著色器介面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96962407492f5fc6b6f7bbacd155c265ffd03e11eff31f2b012a2d1c644d3f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409148"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a> (Direct3D 10 圖形) 的著色器介面

本節包含下列著色器介面的相關資訊：

這些著色器介面都會管理已編譯的著色器。 介面是在編譯著色器時建立，然後傳遞至需要存取已編譯著色器的各種 Api;例如，將著色器系結至管線階段或取得著色器簽章時。



| Pipeline-Stage 介面                                      | 描述                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D10GeometryShader 介面**](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | 幾何著色器會在 [幾何著色器階段](d3d10-graphics-programming-guide-pipeline-stages.md)中執行每個基本處理。 |
| [**ID3D10PixelShader 介面**](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | 圖元著色器會在 [圖元著色器階段](d3d10-graphics-programming-guide-pipeline-stages.md)中執行每圖元處理。           |
| [**ID3D10VertexShader 介面**](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | 頂點著色器會在 [頂點著色器階段](d3d10-graphics-programming-guide-pipeline-stages.md)中執行每個頂點的處理。        |



 

著色器-反映介面可讓應用程式在設計/撰寫時間檢查著色器的內容。 著色器反映不適合用于在執行時間設定變數，因為它是著色器資料的鏡像，因此不支援設定資料的方法。



| Shader-Reflection 介面                                                                   | 描述                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**ID3D10ShaderReflection 介面**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | COM 介面，可在作者時從編譯的著色器讀取資訊。     |
| [**ID3D10ShaderReflectionConstantBuffer 介面**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | 取得著色器反射常數緩衝區介面的 helper 介面。      |
| [**ID3D10ShaderReflectionType 介面**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | 用來取得著色器反映類型介面的 helper 介面。                 |
| [**ID3D10ShaderReflectionVariable 介面**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | 取得著色器反射變數介面的 helper 介面。             |
| [**ID3D10ShaderResourceView 介面**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | 著色器反映介面，可從著色器資源檢視讀取資訊。 |



 

著色器反映 Api 會將一個 COM 著色器反映介面 ([**ID3D10ShaderReflection 介面**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) 和數個非 COM 協助程式介面 (其餘介面) 。 建立著色器反映物件時，會建立 **ID3D10ShaderReflection 介面**。 它會遵循標準 COM 規則;建立介面會增加參考計數，而且當不再需要介面時，必須釋放該介面。 其餘的著色器反映介面是不會繼承自 IUnknown 的 helper 介面。 這表示它們在建立時不會變更任何參考計數，而且當您完成時，不需要終結它們。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器參考](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
