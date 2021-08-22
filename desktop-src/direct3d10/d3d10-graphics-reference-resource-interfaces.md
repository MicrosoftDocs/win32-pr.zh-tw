---
description: Direct3D 10 定義了數種基本資源類型的介面：緩衝區和紋理。
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: " (Direct3D 10 圖形) 的資源介面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94eb7a0f2ce0b6792ccb98b95605f00504fbf239ee0cecf0846814d84566de9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282818"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a> (Direct3D 10 圖形) 的資源介面

Direct3D 10 定義了數種基本資源類型的介面： [緩衝區](d3d10-graphics-programming-guide-resources-types.md) 和紋理。



| 介面                                           | 描述                                          |
|------------------------------------------------------|------------------------------------------------------|
| [**ID3D10Buffer 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | 存取緩衝區資料。                                |
| [**ID3D10Resource 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | 資源的基類。                           |
| [**ID3D10Texture1D 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | 存取1D 材質或1D 材質陣列中的資料。 |
| [**ID3D10Texture2D 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | 存取2D 材質或2D 材質陣列中的資料  |
| [**ID3D10Texture3D 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | 存取3D 紋理或3D 紋理陣列中的資料。 |



 

應用程式會使用 view 將資源系結至 [管線階段](d3d10-graphics-programming-guide-pipeline-stages.md)。 此 [視圖](d3d10-graphics-programming-guide-resources-access-views.md) 會定義在轉譯期間存取資源的方式。 API 包含這些 view 介面。



| 介面                                                               | 描述                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**ID3D10DepthStencilView 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | 存取 [深度](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) 樣板材質中的資料。 |
| [**ID3D10RenderTargetView 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | 存取轉譯 [目標](d3d10-graphics-programming-guide-resources-creating-textures.md)中的資料。        |
| [**ID3D10ShaderResourceView 介面**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | 存取在 Direct3D 10.0 中著色器資源的資料。                                                         |
| [**ID3D10ShaderResourceView1 介面**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | 存取在 Direct3D 10.1 中著色器資源的資料。                                                         |
| [**ID3D10View 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | 視圖的基類。                                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源參考](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
