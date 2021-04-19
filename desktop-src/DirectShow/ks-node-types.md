---
description: 下列全域唯一識別碼 (Guid) 定義核心模式篩選的節點類型。 若要尋找節點類型，請查詢 IKsTopologyInfo 介面的篩選準則。
ms.assetid: 0e133ce3-8815-47d1-a5c3-577a98963912
title: 'KS 節點類型 (Ksmedia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSNODETYPE_DEV_SPECIFIC
- KSNODETYPE_VIDEO_CAMERA_TERMINAL
- KSNODETYPE_VIDEO_INPUT_MTT
- KSNODETYPE_VIDEO_INPUT_TERMINAL
- KSNODETYPE_VIDEO_OUTPUT_MTT
- KSNODETYPE_VIDEO_OUTPUT_TERMINAL
- KSNODETYPE_VIDEO_PROCESSING
- KSNODETYPE_VIDEO_SELECTOR
- KSNODETYPE_VIDEO_STREAMING
api_type:
- HeaderDef
api_location:
- Ksmedia.h
ms.openlocfilehash: eadae4fdd70fd80115ea4e8902ba1bb2aa7bf53b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977649"
---
# <a name="ks-node-types"></a>KS 節點類型

下列全域唯一識別碼 (Guid) 定義核心模式篩選的節點類型。 若要尋找節點類型，請查詢 [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) 介面的篩選準則。



| GUID                                                                                                                                                                                                                     | Description                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KSNODETYPE_DEV_SPECIFIC"></span><span id="ksnodetype_dev_specific"></span><dl> <dt>**KSNODETYPE \_ 開發人員 \_ 專用**</dt> </dl>                             | 代表一或多個裝置特定的處理函式。 節點有一個輸入連接和一個輸出連接。<br/> 節點可能會透過 KsProxy 外掛程式公開自訂 COM 介面（如果裝置製造商有提供的話）。<br/>                                            |
| <span id="KSNODETYPE_VIDEO_CAMERA_TERMINAL"></span><span id="ksnodetype_video_camera_terminal"></span><dl> <dt>**KSNODETYPE \_ 攝影機 \_ \_ 終端機**</dt> </dl> | 代表從相機感應器移入裝置的資料，與 USB 匯流排無關。 節點有一個輸出連接。<br/> 此節點會公開用於控制攝影機的 [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) 和 [**ICameraControl**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-icameracontrol) 介面。<br/> |
| <span id="KSNODETYPE_VIDEO_INPUT_MTT"></span><span id="ksnodetype_video_input_mtt"></span><dl> <dt>**KSNODETYPE \_ 影片 \_ 輸入 \_ MTT**</dt> </dl>                   | 代表從連續媒體傳輸（例如 VTR 磁帶）移入裝置的資料，與 USB 匯流排無關。 節點有一個輸出連接。<br/> 此節點會公開 [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) 介面來控制傳輸機制。<br/>   |
| <span id="KSNODETYPE_VIDEO_INPUT_TERMINAL"></span><span id="ksnodetype_video_input_terminal"></span><dl> <dt>**KSNODETYPE \_ 影片 \_ 輸入 \_ 終端機**</dt> </dl>    | 代表移入裝置的資料，與 USB 匯流排無關。 例如，此節點可能代表類比音訊插孔或 S/PDIF 插口。 節點有一個輸出連接。<br/>                                                                                                             |
| <span id="KSNODETYPE_VIDEO_OUTPUT_MTT"></span><span id="ksnodetype_video_output_mtt"></span><dl> <dt>**KSNODETYPE \_ 影片 \_ 輸出 \_ MTT**</dt> </dl>                | 代表從裝置移至連續媒體傳輸（例如 VTR 磁帶）的資料，與 USB 匯流排無關。 節點有一個輸入連接。<br/> 此節點會公開 [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) 介面來控制傳輸機制。<br/>      |
| <span id="KSNODETYPE_VIDEO_OUTPUT_TERMINAL"></span><span id="ksnodetype_video_output_terminal"></span><dl> <dt>**KSNODETYPE \_ 影片 \_ 輸出 \_ 終端機**</dt> </dl> | 代表移動自裝置的資料，與 USB 匯流排無關。 例如，此節點可能代表類比音訊插孔或 S/PDIF 插口。 節點有一個輸入連接。<br/>                                                                                                              |
| <span id="KSNODETYPE_VIDEO_PROCESSING"></span><span id="ksnodetype_video_processing"></span><dl> <dt>**KSNODETYPE \_ 影片 \_ 處理**</dt> </dl>                 | 代表一或多個影片處理函數。 節點有一個輸入連接和一個輸出連接。<br/> 此節點會公開 [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) 和 [**IVideoProcAmp**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ivideoprocamp) 介面，以調整視訊訊號的品質。<br/> |
| <span id="KSNODETYPE_VIDEO_SELECTOR"></span><span id="ksnodetype_video_selector"></span><dl> <dt>**KSNODETYPE \_ 影片 \_ 選取器**</dt> </dl>                       | 表示從兩個或多個可能來源選取輸入路徑的機制。 節點有兩個或多個輸入連接和一個輸出連接。<br/> 節點會公開 [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) 介面，以便在輸入之間進行選取。<br/>                               |
| <span id="KSNODETYPE_VIDEO_STREAMING"></span><span id="ksnodetype_video_streaming"></span><dl> <dt>**KSNODETYPE \_ 影片 \_ 串流**</dt> </dl>                    | 代表在主機與裝置之間移動的資料。 針對 UVC 裝置，此節點代表 USB 端點。 輸入端點有一個輸入連接;輸出端點有一個輸出連接。<br/>                                                                                         |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Ksmedia。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[常數和 Guid](constants-and-guids.md)
</dt> </dl>

 

 




