---
description: 下列是媒體類型物件的相關函數。
ms.assetid: 7d4f3581-8cb9-4d31-b2f7-c8fbde24cf2a
title: 媒體類型 Helper 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e5edb9748bad8ee16903eb9ff1ada50c1c043b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514348"
---
# <a name="media-type-helper-functions"></a>媒體類型 Helper 函式

下列是媒體類型物件的相關函數。



| 函式                                                                     | 描述                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | 計算影片框架平均持續時間的畫面播放速率。 |
| [**MFCalculateImageSize**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | 抓取未壓縮影片格式的影像大小。            |
| [**MFCompareFullToPartialMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcomparefulltopartialmediatype)   | 將完整媒體類型與部分媒體類型進行比較。                   |
| [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype)                               | 建立空的媒體類型。                                          |
| [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | 將影片畫面播放速率轉換成框架持續時間。                    |
| [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | 捕獲影片格式的最小表面 stride。              |
| [**MFIsFormatYUV**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | 查詢 FOURCC 碼或 **D3DFORMAT** 值是否為 YUV 格式。 |
| [**MFValidateMediaTypeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfvalidatemediatypesize)                   | 驗證影片格式區塊的緩衝區大小。              |
| [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)                                   | 建立包裝另一個媒體類型的媒體類型。                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型轉換](media-type-conversions.md)
</dt> <dt>

[媒體類型](media-types.md)
</dt> </dl>

 

 



