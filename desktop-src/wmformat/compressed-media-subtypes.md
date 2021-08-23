---
title: 壓縮的媒體子類型
description: 壓縮的媒體子類型
ms.assetid: 0ed6b4e8-6450-4484-90d6-efa2f9101782
keywords:
- Windows媒體格式 SDK，媒體類型
- Advanced Systems Format (ASF) 、媒體類型
- ASF (Advanced 系統格式) 、媒體類型
- Windows媒體格式 SDK，壓縮的媒體子類型
- Advanced Systems Format (ASF) ，壓縮的媒體子類型
- ASF (Advanced Systems Format) ，壓縮的媒體子類型
- 媒體類型，壓縮的媒體子類型
- 壓縮的媒體子類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f231c9c8ff666c11d3fb3bf101dc3b43c1cd2ff90ca3a28ca1af0113fe8fccd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548088"
---
# <a name="compressed-media-subtypes"></a>壓縮的媒體子類型

下表列出壓縮的媒體子類型。 這些類型是用來識別檔案中的壓縮資料流程。 當您設定影片或音訊串流時，通常會使用這些類型。



| 壓縮的媒體子類型          | 描述                                                                                                                                                                                                                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ ACELPnet          | 以 Sipro Labs ACELP 編解碼器編碼的音訊。 這種音訊通常是語音資料。  (不再支援編碼。 )                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ MP43              | 由 Microsoft MPEG 4 編解碼器第3版編碼的影片。 Windows 媒體格式 SDK 不再支援此編解碼器。 如果電腦上已安裝此編解碼器，在電腦上安裝 Windows 媒體格式 SDK 或重新發佈套件將不會移除此編解碼器。 |
| WMMEDIASUBTYPE \_ mp4              | 使用 ISO MPEG 4 編解碼器第1版編碼的影片。                                                                                                                                                                                                                                         |
| WMMEDIASUBTYPE \_ MPEG2 \_ 影片      | 編碼為 MPEG 2 規格的影片。                                                                                                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ MSS1              | 以 Windows 媒體畫面編解碼器第1版編碼的影片。                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ MSS2              | 以 Windows Media 視訊9螢幕編解碼器編碼的影片。                                                                                                                                                                                                                                  |
| WMMEDIASUBTYPE \_ WMVP              | 以 Windows Media 視訊9影像編解碼器編碼的影片，可將點陣圖和變形資料轉換成影片串流。                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ WVP2              | 以 Windows Media 視訊9映射 v2 編解碼器編碼的影片。                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMAudio \_ 無損 | 使用 Windows Media 音訊9無失真編解碼器或 Windows Media 音訊9.1 編解碼器編碼的音訊。                                                                                                                                                                                           |
| WMMEDIASUBTYPE \_ WMAudioV2         | 以 Windows Media 音訊編解碼器第2版編碼的音訊。 此值與 WMMEDIASUBTYPE \_ WMAudioV7 和 WMMEDIASUBTYPE WMAudioV8 相同 \_ ，因為這些編解碼器版本的 bitstreams 是相容的。                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV7         | 以 Windows Media 音訊編解碼器版本7編碼的音訊。 此值與 WMMEDIASUBTYPE \_ WMAudioV2 和 WMMEDIASUBTYPE WMAudioV8 相同 \_ ，因為這些編解碼器版本的 bitstreams 是相容的。                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV8         | 以 Windows Media 音訊8編解碼器、Windows Media 音訊9編解碼器或 Windows Media 音訊9.1 編解碼器編碼的音訊。 此值與 WMMEDIASUBTYPE \_ WMAudioV2 和 WMMEDIASUBTYPE WMAudioV7 相同 \_ ，因為這些編解碼器版本的 bitstreams 是相容的。              |
| WMMEDIASUBTYPE \_ WMAudioV9         | 以 Windows Media 音訊 9 Professional 編解碼器或 Windows Media 音訊 9.1 Professional 編解碼器編碼的音訊。                                                                                                                                                                          |
| WMMEDIASUBTYPE \_ M4S2              | 以 ISO MPEG4 v1.1 編解碼器編碼的影片。                                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMSP1             | 以 Windows Media 音訊9語音編解碼器編碼的音訊。                                                                                                                                                                                                                                   |
| WMMEDIASUBTYPE \_ WMV1              | 使用 Windows Media 視訊編解碼器版本7編碼的影片。                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMV2              | 使用 Windows Media 視訊8編解碼器編碼的影片。                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMV3              | 使用 Windows Media 視訊9編解碼器編碼的影片。                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMVA              | 使用 Windows Media 視訊 9 Advanced Profile 編解碼器版本編碼的影片，該版本是以 Windows Media Format 9 系列 SDK 所發行。                                                                                                                                           |
| WMMEDIASUBTYPE \_ WVC1              | 使用以 Windows 媒體格式 11 SDK 發行的 Windows Media 視訊 9 Advanced Profile 編解碼器版本編碼的影片。 此子類型會識別符合 SMPTE VC-1 標準的位資料流程。                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**媒體類型識別碼**](media-type-identifiers.md)
</dt> <dt>

[**媒體類型**](media-types.md)
</dt> <dt>

[**未壓縮的媒體子類型**](uncompressed-media-subtypes.md)
</dt> </dl>

 

 




