---
title: " (Direct3D 11 圖形) 的資源結構"
description: 結構是用來建立及使用資源。
ms.assetid: a29e01ac-8aa1-4a40-ad4d-3b738e129436
keywords:
- 結構，Direct3D 11 資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5020792e1fb56a52e7a4354964c45bb5d65bbba4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103843008"
---
# <a name="resource-structures-direct3d-11-graphics"></a> (Direct3D 11 圖形) 的資源結構

結構是用來建立及使用資源。


## <a name="in-this-section"></a>本節內容



| 主題                                                                                         | 描述                                                                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)<br/>                                   | 描述緩衝區資源。<br/>                                                                           |
| [**D3D11 \_ 緩衝區 \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_rtv)<br/>                                     | 指定要在轉譯目標視圖中使用之緩衝區資源中的元素。<br/>                            |
| [**D3D11 \_ BUFFER \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_srv)<br/>                                     | 指定緩衝區資源中要在著色器資源檢視中使用的元素。<br/>                          |
| [**D3D11 \_ 緩衝區 \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav)<br/>                                     | 描述緩衝區中要用於未排序存取視圖的元素。<br/>                                  |
| [**D3D11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv)<br/>                                 | 描述要在著色器資源檢視中使用之原始緩衝區資源內的元素。<br/>                      |
| [**D3D11 \_ 深度 \_ 樣板 \_ 視圖 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)<br/>         | 指定可從深度範本視圖存取的材質子資源。<br/>                 |
| [**D3D11 \_ 對應的 \_ SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource)<br/>                     | 提供 subresource 資料的存取權。<br/>                                                                   |
| [**D3D11 \_ 封裝的 \_ MIP \_ DESC**](/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_packed_mip_desc)<br/>                          | 描述具有 mipmap 之已並排資源的磚結構。 <br/>                                        |
| [**D3D11 \_ 轉譯 \_ 目標 \_ 視圖 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc)<br/>         | 指定可使用轉譯目標視圖存取之資源的子資源。<br/>             |
| [**D3D11 \_ 轉譯 \_ 目標 \_ 視圖 \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_render_target_view_desc1)<br/>       | 描述可使用呈現目標視圖存取之資源的子資源。<br/>             |
| [**D3D11 \_ 著色器 \_ 資源 \_ 視圖 \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)<br/>     | 描述著色器資源檢視。<br/>                                                                      |
| [**D3D11 \_ 著色器 \_ 資源 \_ 視圖 \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_shader_resource_view_desc1)<br/>   | 描述著色器資源檢視。<br/>                                                                      |
| [**D3D11 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)<br/>                         | 指定用於初始化 subresource 的資料。<br/>                                                         |
| [**D3D11 \_ SUBRESOURCE \_ 平鋪**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_subresource_tiling)<br/>                     | 描述已平 subresource 的磁片區。<br/>                                                                  |
| [**D3D11 \_ TEX1D \_ 陣列 \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_dsv)<br/>                          | 從1D 紋理的陣列指定要在深度樣板視圖中使用的子資源。<br/>                |
| [**D3D11 \_ TEX1D \_ 陣列 \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_rtv)<br/>                          | 從1D 紋理的陣列指定要在轉譯目標視圖中使用的子資源。<br/>                |
| [**D3D11 \_ TEX1D \_ 陣列 \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_srv)<br/>                          | 從1D 紋理的陣列指定要在著色器資源檢視中使用的子資源。<br/>              |
| [**D3D11 \_ TEX1D \_ 陣列 \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_uav)<br/>                          | 描述未排序存取的1D 材質資源陣列。<br/>                                           |
| [**D3D11 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_dsv)<br/>                                       | 從可存取深度樣板視圖的1D 材質指定 subresource。<br/>                |
| [**D3D11 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_rtv)<br/>                                       | 指定要在呈現目標視圖中使用的一維材質 subresource。<br/>                            |
| [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)<br/>                                       | 指定要在著色器資源檢視中使用的一維材質 subresource。<br/>                          |
| [**D3D11 \_ TEX1D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_uav)<br/>                                       | 描述未排序存取的1D 材質資源。<br/>                                                      |
| [**D3D11 \_ TEX2D \_ 陣列 \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv)<br/>                          | 從可存取深度樣板視圖的陣列2D 材質指定子資源。<br/>      |
| [**D3D11 \_ TEX2D \_ 陣列 \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_rtv)<br/>                          | 從2D 材質陣列指定要在轉譯目標視圖中使用的子資源。<br/>                |
| [**D3D11 \_ TEX2D \_ 陣列 \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_rtv1)<br/>                        | 描述要在轉譯目標視圖中使用的2D 材質陣列子資源。<br/>                |
| [**D3D11 \_ TEX2D \_ 陣列 \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_srv)<br/>                          | 從2D 材質陣列指定要在著色器資源檢視中使用的子資源。<br/>              |
| [**D3D11 \_ TEX2D \_ 陣列 \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_srv1)<br/>                        | 描述從2D 材質陣列子資源至著色器資源檢視中使用的程式。<br/>              |
| [**D3D11 \_ TEX2D \_ 陣列 \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_uav)<br/>                          | 描述未排序存取2D 材質資源的陣列。<br/>                                           |
| [**D3D11 \_ TEX2D \_ 陣列 \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_uav1)<br/>                        | 描述未排序存取2D 材質資源的陣列。<br/>                                           |
| [**D3D11 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_dsv)<br/>                                       | 從2D 材質指定可供深度樣板視圖存取的 subresource。<br/>                |
| [**D3D11 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_rtv)<br/>                                       | 從2D 材質指定要在呈現目標視圖中使用的 subresource。<br/>                            |
| [**D3D11 \_ TEX2D \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_rtv1)<br/>                                     | 描述從2D 材質到轉譯目標視圖中使用的 subresource。<br/>                            |
| [**D3D11 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_srv)<br/>                                       | 從2D 材質指定要在著色器資源檢視中使用的 subresource。<br/>                          |
| [**D3D11 \_ TEX2D \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_srv1)<br/>                                     | 描述從2D 材質到著色器資源檢視中使用的 subresource。<br/>                          |
| [**D3D11 \_ TEX2D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_uav)<br/>                                       | 描述未排序的存取2D 材質資源。<br/>                                                      |
| [**D3D11 \_ TEX2D \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_uav1)<br/>                                     | 描述未排序的存取2D 材質資源。<br/>                                                      |
| [**D3D11 \_ TEX2DMS \_ 陣列 \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_dsv)<br/>                      | 從多重取樣2D 材質的陣列指定深度樣板視圖的子資源。<br/>         |
| [**D3D11 \_ TEX2DMS \_ 陣列 \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_rtv)<br/>                      | 從多重取樣2D 材質的陣列指定要在呈現目標視圖中使用的子資源。<br/> |
| [**D3D11 \_ TEX2DMS \_ 陣列 \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_srv)<br/>                      | 從多重取樣2D 材質的陣列指定要在著色器資源檢視中使用的子資源。<br/> |
| [**D3D11 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_dsv)<br/>                                   | 從多重取樣2D 材質指定可供深度樣板視圖存取的 subresource。<br/>   |
| [**D3D11 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_rtv)<br/>                                   | 從多重取樣2D 材質指定要在呈現目標視圖中使用的 subresource。<br/>               |
| [**D3D11 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_srv)<br/>                                   | 從多重取樣2D 材質指定要在著色器資源檢視中使用的子資源。<br/>            |
| [**D3D11 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_rtv)<br/>                                       | 指定要在呈現目標視圖中使用的3D 材質子資源。<br/>                           |
| [**D3D11 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_srv)<br/>                                       | 指定要在著色器資源檢視中使用的3D 紋理子資源。<br/>                         |
| [**D3D11 \_ TEX3D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_uav)<br/>                                       | 描述未排序存取的3D 材質資源。<br/>                                                      |
| [**D3D11 \_ TEXCUBE \_ 陣列 \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_array_srv)<br/>                      | 指定要在著色器資源檢視中使用的 cube 紋理陣列子資源。<br/>            |
| [**D3D11 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_srv)<br/>                                   | 指定要在著色器資源檢視中使用的 cube 材質 subresource。<br/>                        |
| [**D3D11 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture1d_desc)<br/>                             | 描述1D 材質。<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)<br/>                             | 描述2D 材質。<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1)<br/>                           | 描述2D 材質。<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture3d_desc)<br/>                             | 描述3D 紋理。<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1)<br/>                           | 描述3D 紋理。<br/>                                                                                |
| [**D3D11 \_ 圖格 \_ 區域 \_ 大小**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size)<br/>                        | 描述已並排區域的大小。<br/>                                                                  |
| [**D3D11 並排顯示的 \_ \_ 資源 \_ 座標**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate)<br/>      | 描述磚資源的座標。<br/>                                                         |
| [**D3D11 \_ 圖格 \_ 圖形**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape)<br/>                                     | 藉由指定圖格的維度來描述其形狀。<br/>                                            |
| [**D3D11 未 \_ 排序的 \_ 存取權 \_ 視圖 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc)<br/>   | 指定可使用未排序存取視圖來存取的資源子資源。<br/>         |
| [**D3D11 未 \_ 排序 \_ 存取 \_ 視圖 \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_unordered_access_view_desc1)<br/> | 描述可使用未排序存取視圖來存取的資源子資源。<br/>         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源參考](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





