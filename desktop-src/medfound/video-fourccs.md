---
description: 影片 FOURCCs
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: 影片 FOURCCs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318916"
---
# <a name="video-fourccs"></a>影片 FOURCCs

許多影片格式都有指派的 FOURCC 碼。 FOURCC 程式碼是串連四個 ASCII 字元所建立的32位不帶正負號的整數。 例如，YUY2 video 的 FOURCC 程式碼為 ' YUY2 '。

定義各種 C/c + + 宏，以在原始程式碼中宣告 FOURCC 值。 **MAKEFOURCC** 宏是在 Mmsystem 中定義，而 **FCC** 宏則是在 Aviriff 和其他各種標頭檔中定義。 您也可以藉由反轉字元順序，直接將 FOURCC 程式碼宣告為字串常值。 因此，下列語句是相等的：

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

 (在最後一個範例中，必須反轉位元組順序，因為 Windows 會使用位元組由大到小的架構。 ' Y ' = 0x59，' U ' = 0x55，' 2 ' = 0x32，因此 ' 2YUY ' 為0x32595559。 ) 

某些 [DirectX Video 加速 2.0](directx-video-acceleration-2-0.md) api 會使用 **D3DFORMAT** 值來描述影片格式。 您也可以在此內容中使用 FOURCC 程式碼：

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a>FOURCC 常數

下表列出一些常見的 FOURCC 碼。



| FOURCC 值 | Description                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| H264       | H.264 video。                                                                                                          |
| 'I420'       | YUV 以平面4:2:0 格式儲存的影片。                                                                              |
| 'IYUV'       | YUV 以平面4:2:0 格式儲存的影片。                                                                              |
| 4S2 '       | MPEG 4 第2部分影片。                                                                                                  |
| MP4       | Microsoft MPEG 4 編解碼器第3版。 不再支援此編解碼器。                                                  |
| 'MP4V'       | MPEG 4 第2部分影片。                                                                                                  |
| 'MPG1'       | MPEG-2 影片。                                                                                                         |
| 'MSS1'       | 以 Windows Media 視訊7螢幕編解碼器編碼的內容。                                                          |
| 'MSS2'       | 以 Windows Media 視訊9螢幕編解碼器編碼的內容。                                                          |
| UYVY       | YUV 以壓縮的4:2:2 格式儲存的影片。 類似于 YUY2，但資料的順序不同。                         |
| 'WMV1'       | 以 Windows Media 視訊7編解碼器編碼的內容。                                                                 |
| 'WMV2'       | 以 Windows Media 視訊8編解碼器編碼的內容。                                                                 |
| 'WMV3'       | 以 Windows Media 視訊9編解碼器編碼的內容。                                                                 |
| 'WMVA'       | 以舊版、過時版本的 Windows Media 視訊 9 Advanced Profile 編解碼器編碼的內容。                 |
| 'WMVP'       | 以 Windows Media 視訊9.1 影像編解碼器編碼的內容。                                                         |
| 'WVC1'       | SMPTE 421M ( "VC-1" ) 。 使用 Windows Media 視訊 9 Advanced Profile 編碼的內容。                                     |
| 'WVP2'       | 以 Windows Media 視訊9.1 影像 v2 編解碼器編碼的內容。                                                      |
| YUY2       | YUV 以壓縮的4:2:2 格式儲存的影片。                                                                              |
| 'YV12'       | YUV 以平面4:2:0 或4:1:1 格式儲存的影片。 與 I420/IYUV 相同，不同之處在于您和 V 平面已切換。 |
| YVU9       | YUV 以平面16:1:1 格式儲存的影片。                                                                             |
| 'YVYU'       | YUV 以壓縮的4:2:2 格式儲存的影片。 類似于 YUY2，但資料的順序不同。                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片媒體類型](video-media-types.md)
</dt> <dt>

[影片子類型 Guid](video-subtype-guids.md)
</dt> </dl>

 

 



