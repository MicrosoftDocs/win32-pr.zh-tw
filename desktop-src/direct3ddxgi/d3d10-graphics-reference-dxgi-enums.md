---
description: 本節包含有關 DXGI 所提供列舉的資訊。
ms.assetid: c4574c89-dee2-4841-9318-5383cf417111
title: DXGI 列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9347fdf39f2cde6bb50e3ae4c65f2601c570e084516bf817c4dc66169a83925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987138"
---
# <a name="dxgi-enumerations"></a>DXGI 列舉

本節包含有關 DXGI 所提供列舉的資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                         | 描述                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DXGI \_ 介面卡 \_ 旗標**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_adapter_flag)<br/>                                          | 識別 DXGI 介面卡的型別。<br/>                                                                                                                                   |
| [**DXGI \_ 介面卡 \_ 標誌**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)<br/>                                        | 識別 DXGI 介面卡的型別。<br/>                                                                                                                                   |
| [**DXGI \_ ALPHA \_ 模式**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)<br/>                                                       | 識別介面的 Alpha 值（透明行為）。<br/>                                                                                                       |
| [**DXGI \_ 色彩 \_ 空間 \_ 類型**](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)<br/>                                          | 指定色彩空間類型。<br/>                                                                                                                                           |
| [**DXGI \_ 計算 \_ 優先 \_ 細微性**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_compute_preemption_granularity)<br/>              | 識別圖形處理單位 (GPU) 可從執行其目前的計算工作的資料細微性。<br/>                                      |
| [**DXGI \_ DEBUG \_ RLO \_ 旗標**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_debug_rlo_flags)<br/>                                            | 與 [**ReportLiveObjects**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgidebug-reportliveobjects) 搭配使用的旗標，用來指定要報告物件存留期的資訊數量。 <br/>                         |
| [**DXGI \_ 功能**](/windows/desktop/api/DXGI1_5/ne-dxgi1_5-dxgi_feature)<br/>                                                              | 指定檢查功能支援時要使用的硬體功能範圍。<br/>                                                                                  |
| [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)<br/>                                                       | 資源資料格式，包括完整類型和不具類型的格式。 頁面底部的修飾詞清單會更完整地描述每種格式類型。 <br/>               |
| [**DXGI \_ 框架 \_ 簡報 \_ 模式**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_frame_presentation_mode)<br/>                            | 指出將畫面格呈現至交換鏈的選項。 <br/>                                                                                                            |
| [**DXGI \_ GPU \_ 喜好設定**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference)<br/>                                               | 要在其上執行應用程式的 GPU 喜好設定。<br/>                                                                                                                           |
| [**DXGI 圖形優先的資料 \_ \_ \_ 細微性**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_graphics_preemption_granularity)<br/>            | 識別可從執行目前圖形轉譯工作的 GPU 進行優先的資料細微性。<br/>                                                      |
| [**DXGI \_ 硬體 \_ 組合 \_ 支援 \_ 旗標**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)<br/>     | 描述支援的硬體組合層級。<br/>                                                                                                          |
| [**DXGI \_ HDR \_ 中繼資料 \_ 類型**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type)<br/>                                        | 指定標頭元資料類型。<br/>                                                                                                                                    |
| [**DXGI \_ 資訊 \_ 佇列 \_ 訊息 \_ 類別**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_category)<br/>                   | 指定 debug 訊息類別的值。<br/>                                                                                                                      |
| [**DXGI \_ 資訊 \_ 佇列 \_ 訊息 \_ 嚴重性**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_severity)<br/>                   | 值，指定資訊佇列的 debug 訊息嚴重性層級。<br/>                                                                                            |
| [**DXGI \_ 記憶體 \_ 區段 \_ 群組**](/windows/desktop/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)<br/>                                  | 指定要使用的記憶體區段群組。<br/>                                                                                                                             |
| [**DXGI \_ 模式 \_ 旋轉**](/previous-versions/windows/desktop/legacy/bb173065(v=vs.85))<br/>                                        | 旗標，指出如何旋轉回緩衝區以符合監視的實體旋轉。<br/>                                                                  |
| [**DXGI \_ 模式 \_ 調整**](/previous-versions/windows/desktop/legacy/bb173066(v=vs.85))<br/>                                          | 旗標，指出如何延展影像以符合指定的監視器解析度。<br/>                                                                                        |
| [**DXGI \_ 模式 \_ SCANLINE \_ 順序**](/previous-versions/windows/desktop/legacy/bb173067(v=vs.85))<br/>                           | 旗標，指出點陣用來在表面上建立影像的方法。<br/>                                                                                           |
| [**DXGI \_ MULTIPLANE 重迭 \_ \_ YCbCr \_ 旗標**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_multiplane_overlay_ycbcr_flags)<br/>             | 交換鏈色彩空間的選項。<br/>                                                                                                                                    |
| [**DXGI \_ 提供 \_ 資源 \_ 旗標**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags)<br/>                                  | 指定 [**OfferResources1**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) 方法的旗標。<br/>                                                                                |
| [**DXGI \_ 提供 \_ 資源 \_ 優先順序**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_offer_resource_priority)<br/>                           | 當您呼叫 [**IDXGIDevice2：： OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) 方法來提供資源時，識別資源內容的重要性。 <br/> |
| [**DXGI \_ OUTDUPL \_ 指標 \_ 圖形 \_ 類型**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_outdupl_pointer_shape_type)<br/>                     | 識別指標圖形的類型。<br/>                                                                                                                                  |
| [**DXGI 重迭 \_ \_ 色彩 \_ 空間 \_ 支援 \_ 旗標**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_overlay_color_space_support_flag)<br/>        | 指定對重迭色彩空間的支援。<br/>                                                                                                                             |
| [**DXGI 重迭 \_ \_ 支援 \_ 旗標**](/windows/desktop/api/DXGI1_3/ne-dxgi1_3-dxgi_overlay_support_flag)<br/>                                  | 指定要在呼叫 [**IDXGIOutput3：： CheckOverlaySupport**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgioutput3-checkoverlaysupport)時檢查的重迭支援。<br/>                                     |
| [**DXGI \_ 回收 \_ 資源 \_ 結果**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results)<br/>                          | 指定 [**ReclaimResources1**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) 方法的結果旗標。<br/>                                                                     |
| [**DXGI \_ 常駐**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_residency)<br/>                                                 | 旗標，指出資源的記憶體位置。<br/>                                                                                                                    |
| [**DXGI \_ 調整**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling)<br/>                                                              | 識別當後置緩衝區大小不符合目標輸出的大小時調整大小行為。<br/>                                                                     |
| [**DXGI \_ 交換 \_ 鏈 \_ 色彩 \_ 空間 \_ 支援 \_ 旗標**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_swap_chain_color_space_support_flag)<br/> | 指定交換鏈的色彩空間支援。<br/>                                                                                                                      |
| [**DXGI \_ 交換 \_ 鏈 \_ 旗標**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag)<br/>                                   | 交換鏈行為的選項。<br/>                                                                                                                                       |
| [**DXGI \_ 交換 \_ 效果**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)<br/>                                                     | 呼叫 IDXGISwapChain1 之後，在顯示介面中處理圖元的選項 [**：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)。 <br/>                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DXGI 參考](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

