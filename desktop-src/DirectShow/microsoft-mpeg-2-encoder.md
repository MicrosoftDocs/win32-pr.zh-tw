---
description: Microsoft MPEG-2 編碼器篩選器會編碼 MPEG-2 音訊和影片，並將分離信號串流以產生 MPEG-2 程式資料流程或傳輸串流。
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: 'Microsoft MPEG-2 編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ae7f1bd9cb8233d919689bbeb1eea496760ae1254bae88120776364528243d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051228"
---
# <a name="microsoft-mpeg-2-encoder"></a>Microsoft MPEG-2 編碼器

Microsoft MPEG-2 編碼器篩選器會編碼 MPEG-2 音訊和影片，並將分離信號串流以產生 MPEG-2 程式資料流程或傳輸串流。

> [!Note]  
> 以 IA-64 為基礎的平臺不支援此篩選器。

 



篩選資訊

篩選介面

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

輸入 Pin 媒體類型

請參閱備註

輸入 Pin 介面

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

輸出 Pin 媒體類型

請參閱備註

輸出 Pin 介面

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

篩選 CLSID

**CLSID \_** 在 wmcodecdsp 中宣告的 CMPEG2EncoderDS () 

可執行檔

msmpeg2enc.dll

[優點](merit.md)

**\_ \_ 未 \_ 使用的業績**

[篩選準則分類](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>備註

此篩選器結合兩個其他篩選準則的編碼功能：

-   [**Microsoft MPEG-2 音訊編碼器**](microsoft-mpeg-2-audio-encoder.md)
-   [**Microsoft MPEG 2 影片編碼器**](microsoft-mpeg-2-video-encoder.md)

除了所述，此篩選支援與這兩個編碼器相同的編碼功能。

一開始，篩選器會有一個輸入 pin，可以接受音訊或影片輸入。 連接該 pin 碼時，篩選器會建立第二個輸入 pin。 如果第一個輸入釘選到音訊，則第二個輸入 pin 只會接受影片，反之亦然。 每個輸入 pin 都支援與對應的編碼器篩選器相同的媒體類型。

如果只連接一個輸入 pin，則篩選準則支援的輸出類型與對應的音訊或影片編碼器相同。 如果這兩個 pin 都已連接，則篩選器支援下列類型的輸出：

-   音訊-MPEG-2 程式串流中的視覺效果
-   音訊-MPEG-2 傳輸串流中的視覺效果

這些會對應至下列輸出類型：

-   **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ 方案**
-   **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**

此篩選無法對先前編碼的資料流程進行多工處理。 輸入資料流程必須是未壓縮的音訊/影片，這會在多工處理之前進行篩選編碼。 多工資料流程受限於一個程式，包含最多一個音訊和一個影片串流。

### <a name="codec-properties"></a>編解碼器屬性

此篩選支援 [**Mpeg-2 音訊編碼器**](microsoft-mpeg-2-audio-encoder.md) 和 [**mpeg-2 視頻編碼器**](microsoft-mpeg-2-video-encoder.md) 篩選器的結合屬性，但有下列差異：

-   [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)屬性會設定影片串流的平均位元速率。
-   [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md)屬性會設定音訊串流的平均位元速率。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windowsvista Home 進階版、Windows vista 旗艦版、Windows 7 家用進階版、Windows 7 專業版、Windows 7 企業版 Windows 7 旗艦版 \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl>                                                                                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 
