---
title: 未壓縮的媒體子類型
description: 未壓縮的媒體子類型
ms.assetid: 5586e62a-d0f5-45cc-a690-4efa244b3f32
keywords:
- Windows媒體格式 SDK，媒體類型
- Advanced Systems Format (ASF) 、媒體類型
- ASF (Advanced 系統格式) 、媒體類型
- Windows媒體格式 SDK，未壓縮的媒體子類型
- Advanced Systems Format (ASF) 、未壓縮的媒體子類型
- ASF (Advanced 系統格式) 、未壓縮的媒體子類型
- 媒體類型、未壓縮的媒體子類型
- 未壓縮的媒體子類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdbd691a3b43a83656feffa1be114b5180d24cc5e29359b4168a4656d99fd03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807338"
---
# <a name="uncompressed-media-subtypes"></a>未壓縮的媒體子類型

下表列出未壓縮的媒體子類型。 這些是用來做為輸入和輸出格式的類型，以及未壓縮資料流程的格式。 並非下表中的所有類型都支援所有的方法。 在寫入器和讀取器/同步讀取器中，支援的輸入和輸出格式類型可以分別由編解碼器列舉。 如需有關未壓縮資料流程支援之類型的詳細資訊，請參閱 [使用未壓縮的音訊和影片串流](using-uncompressed-audio-and-video-streams.md)。

此處所列的各種 RGB 和調色盤 RGB 影片類型會使用 RGB 格式來定義色彩，其中每個色彩會以圖元的紅色、綠色和藍色元件的濃度值來表示。 每個濃度值的範圍可以從0到255，大約16780000個獨特的色彩。 RGB 可輕易轉譯成用於電腦監視器的色彩值，使用紅色、綠色和藍色 phosphors 來顯示色彩。 調色盤影片類型必須包含緊接在 [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) 結構後面的調色板資訊。 同樣地，16位的影片需要位欄位資訊，其應包含在 WMVIDEOINFOHEADER 結構之後。

下表中的數個媒體子類型所提供的色彩比 RGB 系統所能提供的色彩少，如 Description 資料行中所述。 在調色盤 RGB 類型中，調色板中的色彩代表 RGB 值，但是由指出色彩在調色板中位置的值所指定。



| 未壓縮的媒體子類型 | Description                                                                                                                                                                                                              |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ RGB1       | 調色盤 RGB 影片的1色位代表2個色彩。 通常用於單色影像。                                                                                                                         |
| WMMEDIASUBTYPE \_ RGB4       | 調色盤 RGB 影片有4個代表16色的色彩。                                                                                                                                                           |
| WMMEDIASUBTYPE \_ RGB8       | 具有8個色彩位代表256色彩的調色盤 RGB 影片。                                                                                                                                                          |
| WMMEDIASUBTYPE \_ RGB565     | 代表65536色彩的 RGB video 16 色位。 此格式使用5位（紅色）、6位（綠色）和5位（藍色）。                                                                                         |
| WMMEDIASUBTYPE \_ RGB555     | 代表32768色彩的 RGB video 16 色位。 這種格式會針對每個色彩使用5個位，並忽略第16位。                                                                                           |
| WMMEDIASUBTYPE \_ RGB24      | 具有24個色彩位的 RGB 影片，代表 RGB 色彩標記法配置可用的所有16777216色彩。 此格式會針對每個色彩濃度值使用8個位。                                                |
| WMMEDIASUBTYPE \_ RGB32      | 具有32色位的 RGB 影片，代表 RGB 色彩標記法配置可用的所有16777216色彩。 這種格式會針對每個色彩使用8個位，並保留其餘8位的透明資訊。 |
| WMMEDIASUBTYPE \_ I420       | YUV 以平面4:2:0 格式儲存的影片，會先出現 U 平面，後面接著 V 平面。                                                                                                                      |
| WMMEDIASUBTYPE \_ IYUV       | 與 I420 相同。                                                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ YV12       | YUV 以平面4:2:0 格式儲存的影片，先出現 V 平面，然後是 U 平面。 YV12 與 I420 相同，不同之處在于您和 V 平面已切換。                                               |
| WMMEDIASUBTYPE \_ YUY2       | YUV 以壓縮的4:2:2 格式儲存的影片。                                                                                                                                                                                 |
| WMMEDIASUBTYPE \_ UYVY       | YUV 以壓縮的4:2:2 格式儲存的影片。 類似于 YUY2，但資料的順序不同。                                                                                                                            |
| WMMEDIASUBTYPE \_ YVYU       | YUV 以壓縮的4:2:2 格式儲存的影片。 類似于 YUY2，但資料的順序不同。                                                                                                                            |
| WMMEDIASUBTYPE \_ P422       | YUV 使用平面4:2:2 格式儲存的影片。                                                                                                                                                                            |
| WMMEDIASUBTYPE \_ YVU9       | YUV 以平面16:1:1 格式儲存的影片。                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ PCM        | 使用脈衝程式碼調製儲存的未壓縮音訊資料。                                                                                                                                                              |
| WMMEDIASUBTYPE \_ DRM        | 以安全音訊路徑使用的未壓縮但加密音訊資料。                                                                                                                                                       |
| WMSCRIPTTYPE \_ TwoStrings   | 由包含命令類型之字串和包含命令資料之字串組成的指令碼命令。 這是 Windows 媒體格式 SDK 中唯一支援的腳本類型。                                     |
| WMMEDIASUBTYPE \_ WebStream  | 包含 HTML 檔案的檔案傳輸資料和 Web 串流處理的元件。                                                                                                                                               |
| WMMEDIASUBTYPE \_ VIDEOIMAGE | Windows Media 視訊9影像編解碼器的輸入類型。 範例是點陣圖影像和轉換資料的組合。                                                                                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**指派輸出格式**](assigning-output-formats.md)
</dt> <dt>

[**壓縮的媒體子類型**](compressed-media-subtypes.md)
</dt> <dt>

[**媒體類型識別碼**](media-type-identifiers.md)
</dt> <dt>

[**媒體類型**](media-types.md)
</dt> <dt>

[**列舉輸入格式**](to-enumerate-input-formats.md)
</dt> </dl>

 

 




