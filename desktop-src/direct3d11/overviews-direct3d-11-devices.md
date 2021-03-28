---
title: '裝置 (Direct3D 11 圖形) '
description: 本節說明 Direct3D 11 裝置和裝置內容物件。
ms.assetid: 61d1ea92-e657-4931-8475-74a3123c72f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dda010b3801952e90514fac6307556f8f6fbaff
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104991062"
---
# <a name="devices-direct3d-11-graphics"></a>裝置 (Direct3D 11 圖形) 

Direct3D 裝置會配置和終結物件、呈現基本專案，以及與圖形驅動程式和硬體通訊。 在 Direct3D 11 中，裝置會分割成裝置物件來建立資源，以及執行轉譯的裝置內容物件。 本節說明 Direct3D 11 裝置和裝置內容物件。

從一個裝置建立的物件不能直接與其他裝置搭配使用。 使用共用資源，在多個裝置之間共用資料，其條件約束是共用物件只能由建立它的裝置使用。


## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                                                         | 描述                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Direct3D 11 中的裝置簡介](overviews-direct3d-11-devices-intro.md)<br/>                                                                 | Direct3D 11 物件模型會將資源建立和轉譯功能區分為裝置和一或多個內容。這項分隔是設計來協助多執行緒處理。<br/>                                                  |
| [軟體層](overviews-direct3d-11-devices-layers.md)<br/>                                                                                        | Direct3D 11 執行時間是使用圖層來建立，從核心的基本功能開始，並在外部層建立選擇性和開發人員協助工具。 本節說明每個圖層的功能。<br/> |
| [建立變形和參考裝置的限制](overviews-direct3d-11-devices-limitations.md)<br/>                                                   | 在 Direct3D 10.1 和 Direct3D 11.0 中建立變形和參考裝置有一些限制。 本主題討論這些限制。<br/>                                                                                              |
| [舊版硬體上的 Direct3D 11](overviews-direct3d-11-devices-downlevel.md)<br/>                                                                   | 本節討論如何設計 Direct3D 11，以支援新的和現有的硬體，從 DirectX 9 到 DirectX 11。<br/>                                                                                                             |
| [使用 Direct3D 11 功能資料來補充 Direct3D 功能等級](using-direct3d-optional-features-to-supplement-direct3d-feature-levels.md)<br/> | 瞭解如何檢查裝置支援的選用功能，包括最新的 Windows 版本中新增的功能。<br/>                                                                                                           |



 

## <a name="how-to-topics-about-devices"></a>裝置的 how to 主題



| 主題                                                                                                                                                                                                                                                                                                    | 描述                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="How_To__Create_a_Reference_Device"></span><span id="how_to__create_a_reference_device"></span><span id="HOW_TO__CREATE_A_REFERENCE_DEVICE"></span>[如何：建立參考裝置](overviews-direct3d-11-devices-create-ref.md)<br/>                                                 | 說明如何建立參照裝置。<br/>                            |
| <span id="How_To__Create_a_WARP_Device"></span><span id="how_to__create_a_warp_device"></span><span id="HOW_TO__CREATE_A_WARP_DEVICE"></span>[如何：建立變形裝置](overviews-direct3d-11-devices-create-warp.md)<br/>                                                                    | 說明如何建立變形裝置。<br/>                                 |
| <span id="How_To__Create_a_Swap_Chain"></span><span id="how_to__create_a_swap_chain"></span><span id="HOW_TO__CREATE_A_SWAP_CHAIN"></span>[如何：建立交換鏈](overviews-direct3d-11-devices-create-swap-chain.md)<br/>                                                                  | 說明如何建立交換鏈。<br/>                                  |
| <span id="How_To__Enumerate_Adapters"></span><span id="how_to__enumerate_adapters"></span><span id="HOW_TO__ENUMERATE_ADAPTERS"></span>[如何：列舉介面卡](overviews-direct3d-11-devices-enum.md)<br/>                                                                                   | 說明如何列舉實體顯示配接器。<br/>              |
| <span id="How_To__Get_Adapter_Display_Modes"></span><span id="how_to__get_adapter_display_modes"></span><span id="HOW_TO__GET_ADAPTER_DISPLAY_MODES"></span>[如何：取得介面卡顯示模式](overviews-direct3d-11-devices-get-adapter-info.md)<br/>                                           | 說明如何取得介面卡支援的顯示功能。<br/> |
| <span id="How_To__Create_a_Device_and_Immediate_Context"></span><span id="how_to__create_a_device_and_immediate_context"></span><span id="HOW_TO__CREATE_A_DEVICE_AND_IMMEDIATE_CONTEXT"></span>[如何：建立裝置和立即內容](overviews-direct3d-11-devices-initialize.md)<br/> | 說明如何初始化裝置。<br/>                                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11 的程式設計指南](dx-graphics-overviews.md)
</dt> </dl>

 

 





