---
title: 圖層列舉
description: 本節包含圖層列舉的相關資訊。
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- 列舉，Direct3D 11 層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af59a6ac6fae73cafdbee3f0d93d019d7a8ee0b472cd979e2ddcaeade387ef4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460889"
---
# <a name="layer-enumerations"></a>圖層列舉

本節包含圖層列舉的相關資訊。


## <a name="in-this-section"></a>本節內容



| 主題                                                                                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D11 \_ 訊息 \_ 類別**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | Debug 訊息的類別。 這將會在使用 [**ID3D11InfoQueue：： GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) 抓取訊息，以及使用 [**ID3D11InfoQueue：： AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage)來新增訊息時，識別訊息的類別。 建立 [**資訊佇列篩選器**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)時，這些值可以用來允許或拒絕任何類別的訊息，以通過儲存體和抓取篩選。<br/> |
| [**D3D11 \_ 訊息 \_ 識別碼**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | 設定資訊佇列篩選的偵錯工具 (參閱 [**D3D11 \_ 資訊 \_ 佇列 \_ 篩選**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)) ; 使用這些訊息來允許或拒絕訊息類別，以通過儲存體和抓取篩選。 這些識別碼是由 [**ID3D11InfoQueue：： GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) 或 [**ID3D11InfoQueue：： AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage)之類的方法所使用。 <br/>                                                             |
| [**D3D11 \_ 訊息 \_ 嚴重性**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | 資訊佇列的 Debug 訊息嚴重性層級。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**D3D11 \_ RLDO \_ 旗標**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | 有關裝置物件存留期的報告資訊量選項。<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**D3D11 \_ 著色器 \_ 追蹤 \_ 選項**](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | 指定如何執行著色器偵錯工具追蹤的選項。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**D3D11 \_ 著色器 \_ 追蹤 \_ 資源 \_ 類型**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | 指示要追蹤的資源類型。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖層參考](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





