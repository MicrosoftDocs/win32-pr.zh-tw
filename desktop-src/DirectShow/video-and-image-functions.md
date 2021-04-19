---
description: 影片和影像函式
ms.assetid: 02401edc-362b-4f6c-b10b-c46b30b3ebe7
title: 影片和影像函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55e439a17dd570b6e939d1cb84d836f9100eaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979035"
---
# <a name="video-and-image-functions"></a>影片和影像函式

這些函式和宏會操作 DirectShow 影片格式結構。



| 函式                                                             | 描述                                                                                                                                                       |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**位 \_ 遮罩 \_ 相符**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bit_masks_match)                         | 比較兩個 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構的色遮罩。                                                                                       |
| [**位**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bitmasks)                                         | 從 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構抓取色彩遮罩                                                                                         |
| [**CheckVideoInfoType**](checkvideoinfotype.md)                     | 針對可能造成緩衝區溢位或整數溢位的錯誤，檢查包含 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 格式結構的媒體類型。   |
| [**CheckVideoInfo2Type**](checkvideoinfo2type.md)                   | 針對可能造成緩衝區溢位或整數溢位的錯誤，檢查包含 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式結構的媒體類型。 |
| [**顏色**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-colors)                                             | 從 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構抓取調色板專案                                                                                     |
| [**ContainsPalette**](containspalette.md)                           | 判斷指定的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構是否包含調色板。                                                           |
| [**ConvertVideoInfoToVideoInfo2**](convertvideoinfotovideoinfo2.md) | 將使用 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)的媒體類型轉換成使用 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)的媒體類型                          |
| [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize)                                           | 計算與裝置無關的點陣圖 (DIB) 所需的位元組數目。                                                                                     |
| [**GetBitCount**](getbitcount.md)                                   | 傳回指定的影片子類型所使用的每個圖元位數。                                                                                           |
| [**GetBitmapFormatSize**](getbitmapformatsize.md)                   | 計算 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構所需的大小，此結構可保存指定的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構。       |
| [**GetBitmapPalette**](getbitmappalette.md)                         | 傳回 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構中的第一個調色板專案。                                                                        |
| [**GetBitmapSize**](getbitmapsize.md)                               | 計算與裝置無關的點陣圖 (DIB) 所需的位元組數目。                                                                                     |
| [**GetBitmapSubtype**](getbitmapsubtype.md)                         | 傳回指定點陣圖的媒體子類型 **GUID** 。                                                                                                      |
| [**GetSubtypeName**](getsubtypename.md)                             | 抓取影片子類型的人類可讀取名稱。                                                                                                             |
| [**GetTrueColorType**](gettruecolortype.md)                         | 傳回16位未壓縮 RGB 點陣圖的媒體子類型 **GUID** 。                                                                                          |
| [**頭**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header)                                             | 傳回 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)內的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)位址。                                      |
| [**MPEG1 \_ 順序 \_ 資訊**](/previous-versions/windows/desktop/api/amvideo/nf-amvideo-mpeg1_sequence_info)                 | 傳回 [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) 結構內序列標頭的位址。                                                          |
| [**PALETTISED**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palettised)                                     | 檢查點陣圖的色彩深度是否為8位或更少。                                                                                                      |
| [**調色板 \_ 專案**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palette_entries)                          | 抓取指定點陣圖之調色板中的最大色彩數目。                                                                                      |
| [**重設 \_ 遮罩**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_masks)                                  | 以零填滿 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構中的色彩遮罩欄位。                                                                            |
| [**重設 \_ 標頭**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_header)                                | 以零填滿 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 。                                                                                                   |
| [**重設 \_ 調色板**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_palette)                              | 以零填滿 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構中的調色板專案。                                                                              |
| [**大小 \_ EGA \_ 調色板**](/previous-versions/windows/desktop/legacy/dd377602(v=vs.85))                       | 計算4位 RGB 點陣圖中的調色板專案所需的大小。                                                                                         |
| [**大小 \_ 遮罩**](/previous-versions/windows/desktop/legacy/dd377603(v=vs.85))                                    | 在 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構中計算色彩遮罩的大小。                                                                             |
| [**大小 \_ MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-size_mpeg1videoinfo)                  | 計算 [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) 結構的大小，包括 sequence 標頭。                                                      |
| [**大小 \_ 調色板**](/previous-versions/windows/desktop/legacy/dd377605(v=vs.85))                                | 計算 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構中的調色板專案大小。                                                                         |
| [**大小 \_ PREHEADER**](/previous-versions/windows/desktop/legacy/dd377606(v=vs.85))                            | 計算 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構內 **bmiHeader** 欄位的位元組位移。                                              |
| [**大小 \_ VIDEOHEADER**](/previous-versions/windows/desktop/legacy/dd377607(v=vs.85))                        | 計算 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構的大小。                                                                                  |
| [**彩色**](/previous-versions/windows/desktop/legacy/dd407230(v=vs.85))                                   | 從 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)結構傳回 [**TRUECOLORINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-truecolorinfo)結構。                                            |
| [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md)         | 檢查 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構是否有可能造成緩衝區溢位或整數溢位的錯誤。                                   |



 

## <a name="remarks"></a>備註

一節中所述的大部分宏和函式都是設計來操作 RGB 點陣圖的 **VIDEOINFOHEADER** 和 **VIDEOINFO** 結構。 請小心使用這些宏：它們大部分會假設指定的結構已正確初始化。 其中有許多也會假設 **BITMAPINFOHEADER** 結構是標準大小;也就是 `biSize == sizeof(BITMAPINFOHEADER)` 。

DirectShow 基類庫也提供下列全域常數，以定義 true 色彩點陣圖的標準色彩遮罩。



| 全域資料 | Description                                                   |
|-------------|---------------------------------------------------------------|
| **bits555** | 5-5-5 格式之16位 RGB 點陣圖的色彩遮罩陣列。 |
| **bits565** | 5-6-5 格式之16位 RGB 點陣圖的色彩遮罩陣列。 |
| **bits888** | 24位 RGB 點陣圖的色彩遮罩陣列。                 |



 

這兩個常數在三個 **DWORD** s 的陣列中，其中包含紅色、綠色和藍色遮罩（依該順序）。

 

 
