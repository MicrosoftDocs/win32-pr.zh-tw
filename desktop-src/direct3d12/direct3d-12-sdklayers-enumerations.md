---
title: Debug 圖層列舉
description: 下列列舉是在 d3d12sdklayers 中宣告。
ms.assetid: 6E76C857-128E-4F0E-9711-72C4CF6C835C
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746c0def35c8eb282264cb4ab0b40eb5c08f0f9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968444"
---
# <a name="debug-layer-enumerations"></a>Debug 圖層列舉

下列列舉是在 d3d12sdklayers 中宣告。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                                      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D12 \_ DEBUG \_ 命令 \_ 清單 \_ 參數 \_ 類型**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)<br/>                                 | 指出 [**ID3D12DebugCommandList1：： SetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-setdebugparameter) 和 [**ID3D12DebugCommandList1：： GetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-getdebugparameter)所使用的 debug 參數類型。<br/>                                                                                                                                                                                                      |
| [**D3D12 \_ DEBUG \_ 裝置 \_ 參數 \_ 類型**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)<br/>                                              | 指定由 [**ID3D12DebugDevice1：： SetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter)和 [**ID3D12DebugDevice1：： GetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-getdebugparameter)的 *.pdata* 參數所指向之記憶體的資料類型。<br/>                                                                                                                                                                                        |
| [**D3D12 \_ DEBUG \_ 功能**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature)<br/>                                                                            | 選擇性 D3D12 Debug 層功能的旗標。<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**D3D12 以 \_ GPU 為 \_ 基礎的 \_ 驗證 \_ 旗標**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_flags)<br/>                                                | 描述在執行時間執行的 GPU 型驗證層級。<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**D3D12 以 \_ GPU 為 \_ 基礎的 \_ 驗證 \_ 管線 \_ 狀態 \_ 建立 \_ 旗標**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)<br/> | 指定在 [**ID3D12Device：： CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) 和 [**ID3D12Device：： CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)期間，GPU-Based 驗證如何處理修補的管線狀態。<br/>                                                                                                                                                                             |
| [**D3D12 以 \_ GPU 為 \_ 基礎的 \_ 驗證 \_ 著色器 \_ 修補 \_ 模式**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)<br/>                      | 指定在裝置或命令清單層級 GPU-Based 驗證所使用的著色器修補類型。<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**D3D12 \_ 訊息 \_ 類別**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_category)<br/>                                                                      | 指定 debug 訊息的類別。 這將會在使用 [**ID3D12InfoQueue：： GetMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) 抓取訊息，以及使用 [**ID3D12InfoQueue：： AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage)來新增訊息時，識別訊息的類別。 建立資訊佇列篩選器時，這些值可以用來允許或拒絕任何類別的訊息，以通過儲存體和抓取篩選。 <br/> |
| [**D3D12 \_ 訊息 \_ 識別碼**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_id)<br/>                                                                                  | 指定用於設定資訊佇列篩選的偵錯工具訊息識別碼 (請參閱 [**D3D12 \_ 資訊 \_ 佇列 \_ 篩選**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)) ; 使用這些訊息來允許或拒絕訊息類別，以通過儲存體和抓取篩選。 這些識別碼是由 [**ID3D12InfoQueue：： GetMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) 或 [**ID3D12InfoQueue：： AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage)之類的方法所使用。 <br/>                        |
| [**D3D12 \_ 訊息 \_ 嚴重性**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity)<br/>                                                                      | 資訊佇列的 Debug 訊息嚴重性層級。<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| [**D3D12 \_ RLDO \_ 旗標**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_rldo_flags)<br/>                                                                                  | 指定要報告的即時裝置物件存留期之資訊數量的選項。 <br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 12 程式設計環境設定](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Debug 圖層參考](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Direct3D 12 參考](direct3d-12-reference.md)
</dt> </dl>

 

 





