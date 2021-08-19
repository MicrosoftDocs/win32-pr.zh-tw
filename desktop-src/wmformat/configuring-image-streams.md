---
title: 設定影像串流
description: 設定影像串流
ms.assetid: 29325834-8766-47f4-8b33-b5fcbcc494c1
keywords:
- 串流，設定影像資料流程
- 編解碼器，設定影像串流
- 影像串流，設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ce58fe3da709772b08d0956f3f5540713f7960742338f73c9d9807ad1a1e40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848963"
---
# <a name="configuring-image-streams"></a>設定影像串流

影像資料流程包含靜止的影像（JPEG 格式）。 雖然影像串流像是影片串流，但它們會將未壓縮的影像作為輸入，因此需要的設定稍有不同。 若要設定影像資料流程，您必須設定影片設定結構成員的值，如下表所示。



| 設定                                                           | 描述                                                                                                                                                                      |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WM \_ 媒體 \_ 類型。 majortype**                                     | 設定為 WMMEDIATYPE \_ 影像。                                                                                                                                                       |
| **WM \_ 媒體 \_ 類型。子類型**                                       | 設定為 WMMEDIASUBTYPE \_ RGB24。                                                                                                                                                    |
| **WM \_ 媒體 \_ 類型。 bFixedSizeSamples**                             | 設定為 **FALSE**。                                                                                                                                                                |
| **WM \_ 媒體 \_ 類型。 bTemporalCompression**                          | 設定為 **FALSE**。                                                                                                                                                                |
| **WM \_ 媒體 \_ 類型。 lSampleSize**                                   | 設定為0。                                                                                                                                                                        |
| **WM \_ 媒體 \_ 類型。 formattype**                                    | 設定為 WMFORMAT \_ VideoInfo。                                                                                                                                                      |
| **WM \_ 媒體 \_ 類型。 pUnk**                                          | 設定為 **Null**。                                                                                                                                                                 |
| **WM \_ 媒體 \_ 類型。 cbFormat**                                      | 設定為 `sizeof(WMVIDEOINFOHEADER)`。                                                                                                                                              |
| **WM \_ 媒體 \_ 類型。 pbFormat**                                      | 設定為正確設定的 **WMVIDEOINFOHEADER** 結構位址。                                                                                                     |
| **WMVIDEOINFOHEADER. rcSource** 和 **WMVIDEOINFOHEADER. rcTarget** | 設定這兩個矩形，讓左上角成為座標 (0、0) 和右下角的座標 (x，y) 其中 x 是影像寬度，y 是影像高度。 |
| **WMVIDEOINFOHEADER.dwBitRate**                                   | 設定為數據流的位元速率。                                                                                                                                               |
| **WMVIDEOINFOHEADER.dwErrorRate**                                 | 設定為0。                                                                                                                                                                        |
| **WMVIDEOINFOHEADER.dwBitErrorRate**                              | 設定為0。                                                                                                                                                                        |
| **WMVIDEOINFOHEADER.AvgTimePerFrame**                             | 設定為0。                                                                                                                                                                        |
| **BITMAPINFOHEADER.biWidth**                                      | 設定為影像的寬度。                                                                                                                                                   |
| **BITMAPINFOHEADER.biHeight**                                     | 設定為影像的高度。                                                                                                                                                  |
| **BITMAPINFOHEADER.biPlanes**                                     | 設定為 1。                                                                                                                                                                        |
| **BITMAPINFOHEADER.biBitCount**                                   | 設定為24。                                                                                                                                                                       |
| **BITMAPINFOHEADER.biCompression**                                | 設定為 [BI \_ RGB]。                                                                                                                                                                  |
| **BITMAPINFOHEADER.biSizeImage**                                  | 設定為 ( (x \* y \* c) /8) ，其中 x 是影像的寬度，y 是影像的高度，而 c 是影像的色彩深度 (在此案例中一律為 24) 。                     |
| **BITMAPINFOHEADER.biXPelsPerMeter**                              | 設定為0。                                                                                                                                                                        |
| **BITMAPINFOHEADER.biYPelsPerMeter**                              | 設定為0。                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClrUsed**                                    | 設定為0。                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClrImportant**                               | 設定為0。                                                                                                                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**所有資料流程通用的設定**](configuration-common-to-all-streams.md)
</dt> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> <dt>

[**使用 Windows Media 視訊9螢幕編解碼器取得良好的結果**](getting-good-results-with-the-windows-media-video-9-screen-codec.md)
</dt> <dt>

[**影像串流**](image-streams.md)
</dt> </dl>

 

 




