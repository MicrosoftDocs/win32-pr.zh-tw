---
description: 用來建立和使用資源的結構。
ms.assetid: d8fe2ebe-349a-456e-9a5a-16f2d3419800
title: " (Direct3D 10 圖形) 的資源結構"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb45ff5d77d7bb0417b54b88a4014e2a96f522d2e026c778efcd05d23f624bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635018"
---
# <a name="resource-structures-direct3d-10-graphics"></a> (Direct3D 10 圖形) 的資源結構

用來建立和使用 [資源](d3d10-graphics-programming-guide-resources-types.md)的結構。



| 結構                                                                 | 描述                                                                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D10 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)                           | [緩衝區](d3d10-graphics-programming-guide-resources-types.md)資源的描述。                                                                     |
| [**D3D10 \_ 緩衝區 \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_rtv)                             | 描述要用於呈現目標視圖之 [緩衝區](d3d10-graphics-programming-guide-resources-types.md) 中的元素。                                |
| [**D3D10 \_ BUFFER \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_srv)                             | 描述 [緩衝區](d3d10-graphics-programming-guide-resources-types.md) 資源中要在著色器資源檢視中使用的元素。                         |
| [**D3D10 \_ 深度 \_ 樣板 \_ 視圖 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_view_desc) | 描述深度範本視圖。                                                                                                                               |
| [**D3D10 \_ 對應的 \_ TEXTURE2D**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture2d)                 | 提供 [2d 材質](d3d10-graphics-programming-guide-resources-types.md)中 subresource 資料的存取權。                                                  |
| [**D3D10 \_ 對應的 \_ TEXTURE3D**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture3d)                 | 提供 [3d 材質](d3d10-graphics-programming-guide-resources-types.md)中 subresource 資料的存取權。                                                  |
| [**D3D10 \_ 轉譯 \_ 目標 \_ 視圖 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_render_target_view_desc) | 描述呈現目標視圖。                                                                                                                               |
| [**D3D10 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)                 | 指定用於初始化資源的資料。                                                                                                                   |
| [**D3D10 \_ TEX1D \_ 陣列 \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_dsv)                  | 指定要用於深度樣板視圖的 [1d 材質陣列](d3d10-graphics-programming-guide-resources-types.md) 中的 mipmap 層級和紋理。       |
| [**D3D10 \_ TEX1D \_ 陣列 \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_rtv)                  | 從 [1d 紋理](d3d10-graphics-programming-guide-resources-types.md) 的陣列指定要在轉譯目標視圖中使用的 subresource (s) 。             |
| [**D3D10 \_ TEX1D \_ 陣列 \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_srv)                  | 指定要在著色器資源檢視中使用的 [1d 材質陣列](d3d10-graphics-programming-guide-resources-types.md) 中的 mipmap 層級和紋理。      |
| [**D3D10 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_dsv)                               | 指定要在深度樣板視圖中使用的一 [維材質](d3d10-graphics-programming-guide-resources-types.md) subresource (s) 。                        |
| [**D3D10 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_rtv)                               | 指定要在轉譯目標視圖中使用的一 [維材質](d3d10-graphics-programming-guide-resources-types.md) subresource (s) 。                        |
| [**D3D10 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_srv)                               | 指定從 [1d 材質](d3d10-graphics-programming-guide-resources-types.md)) 的 subresource (s，以用於著色器資源檢視。                      |
| [**D3D10 \_ TEX2D \_ 陣列 \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)                  | 指定要在深度範本視圖中使用之 [2d 材質陣列](d3d10-graphics-programming-guide-resources-types.md) 中的 mipmap 層級和紋理。 |
| [**D3D10 \_ TEX2D \_ 陣列 \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_rtv)                  | 指定要在呈現目標視圖中使用之 [2d 材質陣列](d3d10-graphics-programming-guide-resources-types.md) 中的 mipmap 層級和紋理。 |
| [**D3D10 \_ TEX2D \_ 陣列 \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_srv)                  | 指定從 [2d 材質](d3d10-graphics-programming-guide-resources-types.md) 陣列 subresource (s) ，以用於著色器資源檢視。           |
| [**D3D10 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_dsv)                               | 指定要在深度樣板視圖中使用之 [2d 材質](d3d10-graphics-programming-guide-resources-types.md) 的 subresource (s) 。                        |
| [**D3D10 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_rtv)                               | 從 [2d 材質](d3d10-graphics-programming-guide-resources-types.md) 指定要在轉譯目標視圖中使用的 subresource (s) 。                        |
| [**D3D10 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_srv)                               | 指定從 [2d 材質](d3d10-graphics-programming-guide-resources-types.md)) 的 subresource (s，以用於著色器資源檢視。                      |
| [**D3D10 \_ TEX2DMS \_ 陣列 \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_dsv)              | 從 [2d 材質](d3d10-graphics-programming-guide-resources-types.md) 陣列指定要在深度樣板視圖中使用的 subresource (s) 。             |
| [**D3D10 \_ TEX2DMS \_ 陣列 \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_rtv)              | 從 [2d 材質](d3d10-graphics-programming-guide-resources-types.md) 陣列指定要在轉譯目標視圖中使用的 subresource (s) 。             |
| [**D3D10 \_ TEX2DMS \_ 陣列 \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_srv)              | 指定從 [2d 材質](d3d10-graphics-programming-guide-resources-types.md) 陣列 subresource (s) ，以用於著色器資源檢視。           |
| [**D3D10 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_dsv)                           | 從多重取樣 [2d 材質](d3d10-graphics-programming-guide-resources-types.md) 指定要在深度樣板視圖中使用的 subresource () s。           |
| [**D3D10 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_rtv)                           | 從多重取樣 [2d 材質](d3d10-graphics-programming-guide-resources-types.md) 指定要在呈現目標視圖中使用的 subresource () s。           |
| [**D3D10 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_srv)                           | 指定從多重取樣 [2d 材質](d3d10-graphics-programming-guide-resources-types.md)) subresource (s，以用於著色器資源檢視。         |
| [**D3D10 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_rtv)                               | 指定要在轉譯目標視圖中使用之 [3d 材質](d3d10-graphics-programming-guide-resources-types.md) 中的 subresource (s) 。                        |
| [**D3D10 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_srv)                               | 指定從 [3d 材質](d3d10-graphics-programming-guide-resources-types.md)) 的 subresource (s，以用於著色器資源檢視。                      |
| [**D3D10 \_ TEXCUBE \_ 陣列 \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)            | 指定從 [cube 材質](d3d10-graphics-programming-guide-resources-types.md)) 的 subresource (s，以用於著色器資源檢視。                    |
| [**D3D10 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_texcube_srv)                           | 指定從 [cube 材質](d3d10-graphics-programming-guide-resources-types.md)) 的 subresource (s，以用於著色器資源檢視。                    |
| [**D3D10 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture1d_desc)                     | 描述 [1d 材質](d3d10-graphics-programming-guide-resources-types.md) 資源。                                                                      |
| [**D3D10 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture2d_desc)                     | 描述 [2d 材質](d3d10-graphics-programming-guide-resources-types.md) 資源。                                                                      |
| [**D3D10 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture3d_desc)                     | 描述 [3d 材質](d3d10-graphics-programming-guide-resources-types.md) 資源。                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源參考](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



