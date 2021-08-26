---
title: HLSL 著色器模型5
description: HLSL 著色器模型5
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 537b2460b73f30397561dea37bcb3711b64a935c43d45662428585a47d6f6574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095348"
---
# <a name="hlsl-shader-model-5"></a>HLSL 著色器模型5

本章節包含 High-Level 著色器語言的總覽內容，特別是在 Microsoft Direct3D 11 引進的著色器模型5中的新功能。

## <a name="in-this-section"></a>本節內容



| 項目                                                                                                                                                                                                               | 描述                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[動態連結](overviews-direct3d-11-hlsl-dynamic-linking.md)<br/>                                 | 動態連結可讓執行時間在繪製 (時間進行決策，而不是在編譯時間) ，以瞭解要執行的程式碼路徑。 這樣可以減少著色器幾乎相同的輸入簽章所造成的著色器激增問題。<br/>                                                                                                                         |
| <span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[幾何著色器功能](overviews-direct3d-11-hlsl-gs-features.md)<br/> | 新的幾何著色器功能包括：實例，可在資料流程中的基本專案順序不重要時提高效能，以及多個點輸出資料流程，讓著色器可以在多個資料流程上輸出頂點。<br/>                                                                                                                |
| <span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[鑲嵌](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)<br/>                                        | Direct3D 11 執行時間支援三個新階段來執行鑲嵌式，這會將低細節的細分圖介面轉換成 GPU 上較高的基本專案。 鑲嵌並排顯示高位表面 (或將其分裂) 成為適合轉譯的結構。 三個鑲嵌階段為輪廓-著色器、鑲嵌和網域著色器階段。<br/> |



 

此外，參考章節還涵蓋了許多適用于著色器模型5的新 API 元素，包括： [屬性](d3d11-graphics-reference-sm5-attributes.md)、 [內建函式](d3d11-graphics-reference-sm5-intrinsics.md)、 [著色器模型5物件和方法](d3d11-graphics-reference-sm5-objects.md)，以及 [系統值](d3d11-graphics-reference-sm5-system-values.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

