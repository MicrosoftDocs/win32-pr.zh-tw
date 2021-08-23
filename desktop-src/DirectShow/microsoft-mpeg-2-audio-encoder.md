---
description: Microsoft MPEG-2 音訊編碼器篩選器會將 MPEG-2 音訊層編碼為 I 和 II，包括支援 MPEG-2 低取樣頻率 (LSF) 擴充功能。
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: 'Microsoft MPEG-2 音訊編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030821905862a9698ee24c3227f2846cd8c892e20c501d2776cdf2f9bb88f3e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584118"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a>Microsoft MPEG-2 音訊編碼器

Microsoft MPEG-2 音訊編碼器篩選器會將 MPEG-2 音訊層編碼為 I 和 II，包括支援 MPEG-2 低取樣頻率 (LSF) 擴充功能。

若要對音訊/影片串流進行編碼和多工處理，請使用 [**MICROSOFT Mpeg-2 編碼器**](microsoft-mpeg-2-encoder.md) 篩選器，它會封裝此篩選器和 [**Microsoft mpeg-2 影片編碼器**](microsoft-mpeg-2-video-encoder.md) 篩選器的功能。

> [!Note]  
> 以 IA-64 為基礎的平臺不支援此篩選器。

 



篩選資訊

篩選介面

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

輸入 Pin 媒體類型

**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ PCM**

輸入 Pin 介面

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

輸出 Pin 媒體類型

**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG2 \_ 音訊**<br/> **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ 音訊**<br/> **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ 方案**<br/> **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**<br/>

輸出 Pin 介面

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

篩選 CLSID

**CLSID \_** 在 wmcodecdsp 中宣告的 CMPEG2EncoderAudioDS () 

可執行檔

msmpeg2enc.dll

[優點](merit.md)

**\_ \_ 未 \_ 使用的業績**

[篩選準則分類](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>備註

MPEG-2 音訊編碼器可以產生下列種類的輸出：

-   音訊基本資料流程
-   MPEG-2 程式串流中的音訊
-   MPEG-2 傳輸串流中的音訊

它支援 (LSF) 擴充功能的 MPEG-2 層級 I 和 II 和 MPEG-2 低取樣頻率

輸入範例必須是每個樣本16位，音訊取樣率為48、44.1、32、22.05 或 16 KHz。 編碼器無法重新取樣音訊串流;編碼的音訊具有與輸入相同的取樣率。

輸入範例必須是 mono 或身歷聲。 編碼的音訊具有輸入的通道數目。

### <a name="limitations"></a>限制

編碼器不支援下列各項：

-   MPEG layer III 音訊 bitstreams。
-   MPEG-2 多通道擴充 bitstreams。
-   MPEG 4 AAC bitstreams。
-   MPEG-2 的非與舊版相容 (NBC) bitstreams。
-   產生 packetized 基本資料流程 (PE) 封包。
-   杜比數位編碼。

### <a name="codec-properties"></a>編解碼器屬性

篩選準則透過 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)支援下列屬性：

-   [**AVAudioChannelCount**](avaudiochannelcount-property.md)
-   [**AVAudioSampleRate**](avaudiosamplerate-property.md)
-   [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)
-   [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
-   [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
-   [**AVEncMPACodingMode**](avencmpacodingmode-property.md)
-   [**AVEncMPACopyright**](avencmpacopyright-property.md)
-   [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)
-   [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md)
-   [**AVEncMPALayer**](avencmpalayer-property.md)
-   [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)
-   [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)

> [!Note]  
> 舊版檔不正確地列出一些不支援的其他屬性。

 

為了回溯相容性，此篩選會透過 **IEncoderAPI** 介面支援下列屬性：



| 屬性                 | 描述                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| **ENCAPIPARAM \_ 位元速率** | 相當於 [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)。 |



 

建議您以下列順序設定屬性：

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncMPALayer**](avencmpalayer-property.md)
3.  [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
4.  [**AVEncMPACodingMode**](avencmpacodingmode-property.md)

以任何順序設定其餘的屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windowsvista Home 進階版、Windows vista 旗艦版、Windows 7 家用進階版、Windows 7 專業版、Windows 7 企業版 Windows 7 旗艦版 \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl>                                                                                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> <dt>

[**MPEG-2 信號信號媒體類型**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
