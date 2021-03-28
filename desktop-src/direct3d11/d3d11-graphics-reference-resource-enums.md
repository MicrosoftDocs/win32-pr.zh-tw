---
title: " (Direct3D 11 圖形) 的資源列舉"
description: 列舉是用來指定在轉譯期間如何建立和存取資源的相關資訊。
ms.assetid: b547819b-7006-40b5-84a4-adf198048051
keywords:
- 列舉，Direct3D 11 資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6124fcbc93cb0069152dd20d3b4b3bf0f4be60d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104971848"
---
# <a name="resource-enumerations-direct3d-11-graphics"></a> (Direct3D 11 圖形) 的資源列舉

列舉是用來指定在轉譯期間如何建立和存取資源的相關資訊。


## <a name="in-this-section"></a>本節內容



| 主題                                                                                                               | 描述                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D11 系結 \_ \_ 旗標**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)<br/>                                                             | 識別如何將資源系結至管線。<br/>                                                                                                                                 |
| [**D3D11 \_ BUFFEREX \_ SRV \_ 旗標**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag)<br/>                                            | 識別如何查看緩衝區資源。<br/>                                                                                                                                          |
| [**D3D11 \_ BUFFER \_ UAV \_ 旗標**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag)<br/>                                                | 識別緩衝區資源的未排序存取視圖選項。<br/>                                                                                                                    |
| [**D3D11 \_ 檢查多重取樣 \_ \_ 品質 \_ 層級 \_ 旗標**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag)<br/> | 識別如何檢查多層級的品質等級。<br/>                                                                                                                                |
| [**D3D11 \_ CPU \_ 存取 \_ 旗標**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)<br/>                                                | 指定資源允許的 CPU 存取類型。<br/>                                                                                                                          |
| [**D3D11 \_ DSV \_ 維度**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_dimension)<br/>                                                     | 指定如何存取深度範本視圖中使用的資源。<br/>                                                                                                                   |
| [**D3D11 \_ DSV \_ 旗標**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_flag)<br/>                                                               | 深度樣板的視圖選項。<br/>                                                                                                                                                        |
| [**D3D11 \_ 對應**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)<br/>                                                                          | 識別要存取以供 CPU 讀取和寫入的資源。 應用程式可以結合一或多個這些旗標。<br/>                                                      |
| [**D3D11 \_ 對應 \_ 旗標**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map_flag)<br/>                                                               | 指定當應用程式在 GPU 正在使用的資源上呼叫 [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) 方法時，CPU 應該如何回應。<br/> |
| [**D3D11 \_ 資源 \_ 維度**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)<br/>                                           | 識別正在使用的資源類型。<br/>                                                                                                                                        |
| [**D3D11 \_ 資源 \_ 其他 \_ 旗標**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)<br/>                                          | 識別資源的選項。<br/>                                                                                                                                                  |
| [**D3D11 \_ RTV \_ 維度**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_rtv_dimension)<br/>                                                     | 這些旗標會識別將視為呈現目標的資源類型。<br/>                                                                                                  |
| [**D3D11 \_ SRV \_ 維度**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85))<br/>                                                     | 這些旗標會識別將視為著色器資源的資源類型。<br/>                                                                                                |
| [**D3D11 \_ 標準 \_ 的 \_ 高採樣品質 \_ 層級**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_standard_multisample_quality_levels)<br/>       | 指定多重範例模式類型。<br/>                                                                                                                                             |
| [**D3D11 \_ 材質 \_ 版面配置**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout)<br/>                                                   | 指定材質版面配置選項。<br/>                                                                                                                                                  |
| [**D3D11 \_ 圖格 \_ 複製 \_ 旗標**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag)<br/>                                                 | 識別如何複製磚。<br/>                                                                                                                                                     |
| [**D3D11 \_ 圖格 \_ 對應 \_ 旗標**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_mapping_flag)<br/>                                           | 識別如何執行磚對應作業。<br/>                                                                                                                                |
| [**D3D11 \_ 圖 \_ 格範圍 \_ 旗標**](/windows/desktop/api/d3d11_2/ne-d3d11_2-d3d11_tile_range_flag)<br/>                                                | 指定要搭配 [**ID3D11DeviceCoNtext2：： UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)使用的圖格對應範圍。<br/>                                                      |
| [**D3D11 \_ UAV \_ 維度**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension)<br/>                                                     | 未排序的存取視圖選項。<br/>                                                                                                                                                     |
| [**D3D11 \_ 使用方式**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)<br/>                                                                      | 在轉譯期間識別預期的資源使用。 使用方式會直接反映 CPU 和/或圖形處理器 (GPU) 是否可存取資源。<br/>              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源參考](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

