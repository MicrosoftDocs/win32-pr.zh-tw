---
description: 此篩選器會解碼下列音訊格式：
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: 'Microsoft MPEG-1/DD/AAC 音訊解碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a685fa2be32dd963cdc7de08ec716117e6a7016e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106967008"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a>Microsoft MPEG-1/DD/AAC 音訊解碼器

此篩選器會解碼下列音訊格式：

-   MPEG-2 音訊層 I 和 II。
-   與舊版相容的 MPEG-2 音訊、圖層 I 和 II (ISO/IEC 13818-3) 、mono 和身歷聲。
-   Advanced Audio 編碼 (AAC) 低複雜度 (LC) 設定檔。
-   High-Efficiency AAC (AAC) 第1版和第2版。
-   傳遞數位劇院系統 (DTS) 的數位輸出。
-   LPCM、mono 和身歷聲（含或不含 PE 標頭）。
-   杜比數位。
-   杜比數位 Plus，包括從杜比數位的轉換到數位輸出的杜數位。

> [!Note]  
> Microsoft 應用程式使用的杜比數位授權方案，會限制 Microsoft 的杜比數位技術。

 

> [!Note]  
> 以 IA-64 為基礎的平臺不支援此篩選器。

 

將杜比數位加號、AAC 和 AAC 格式解碼需要 Windows 7。 Windows 7 Home Basic 或 Windows 7 Starter 版不支援對杜比數位或杜比數位加號進行解碼。

在登錄中，此篩選器的易記名稱是「Microsoft DTV DVD-音訊解碼」。



篩選資訊

篩選介面

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

輸入 Pin 媒體類型

在 Windows Vista 和更新版本中，篩選準則支援下列輸入類型：<br/>

-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ 杜比 \_ AC3** (請參閱附注1。 ) 
-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG1Audio**
-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG1Payload**
-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG2 \_ 音訊**
-   **媒體媒體 \_DVD \_ 加密 \_ 套件**， **MEDIASUBTYPE \_ 杜比 \_ AC3** (參閱附注1。 ) 
-   **媒體媒體 \_DVD \_ 加密 \_ 套件**， **MEDIASUBTYPE \_ DTS** (請參閱附注 2. ) 
-   **媒體媒體 \_DVD \_ 加密 \_ 套件**、 **MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊**
-   **媒體媒體 \_DVD \_ 加密 \_ 套件**， **MEDIASUBTYPE \_ MPEG2 \_ 音訊**
-   **媒體媒體 \_MPEG2 \_ pe**、 **MEDIASUBTYPE \_ 杜比 \_ AC3** (請參閱附注1。 ) 
-   **媒體媒體 \_MPEG2 \_ pe**、 **MEDIASUBTYPE \_ DTS** (請參閱附注 2. ) 
-   **媒體媒體 \_MPEG2 \_ pe**、 **MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊**
-   **媒體媒體 \_MPEG2 \_ pe**、 **MEDIASUBTYPE \_ MPEG2 \_ 音訊**
-   **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ 杜比 \_ AC3** (請參閱附注1。 ) 
-   **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG1Audio**
-   **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ 音訊**

從 Windows 7 開始，篩選準則也支援下列輸入類型：<br/>

-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ 杜比 \_ DDPLUS** (請參閱附注1。 ) 
-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ DTS2** (請參閱附注 2. ) 
-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊**
-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ DVM** (請參閱附注1。 ) 
-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG \_ loa**
-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG1AudioPayload**
-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ 原始 \_ AAC1**
-   **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ 杜比 \_ DDPLUS** (請參閱附注1。 ) 
-   **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG \_ loa**

輸入類型在串流處理期間可能會動態變更。<br/> 如需這些媒體類型的詳細資訊，請參閱 [**音訊子類型**](audio-subtypes.md)。<br/>

> [!Note]  
> 1. Microsoft 應用程式使用的杜比數位授權方案，會限制 Microsoft 的杜比數位技術。

<br/>

> [!Note]  
> 2. 針對數位劇院系統 (DTS) 輸入， (DTS over S/PDIF) 只支援 S/PDIF 輸出。 不支援音訊解碼。

<br/>

輸入 Pin 介面

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

輸出 Pin 媒體類型

在 Windows Vista 和更新版本中，篩選準則支援下列輸出類型：<br/>

-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ 杜比 \_ AC3 \_ SPDIF** (與 **KSDATAFORMAT \_ 子類型相同 \_ IEC61937 \_ 杜比 \_ 數位**) 
-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ PCM**

從 Windows 7 開始，篩選準則也支援下列輸出類型：<br/>

-   **媒體媒體 \_音訊**、 **KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ DTS**
-   **媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ IEEE \_ FLOAT**

輸出 Pin 介面

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

篩選 CLSID

**CLSID \_** 在 wmcodecdsp 中宣告的 CMPEG2AudDecoderDS () 

可執行檔

msmpeg2adec.dll

[優點](merit.md)

**業績 \_正常** -1

[篩選準則分類](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

> [!Note]  
> 舊版的檔規定此篩選器可以解碼「MPEG-2 音訊」。 篩選只會將後端相容的 MPEG-2 音訊解碼。

 

## <a name="remarks"></a>備註

Mono 資料流程一律會解碼為身歷聲。

針對通道設定為兩個以上的喇叭的串流，此解碼器會執行下列其中一項：

-   使用常見的5.1 喇叭設定，向上混合到六個通道。
-   Downmixes 至身歷聲。

若要在這兩個選項之間做選擇，請先使用 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) 介面設定 [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) 屬性，再連接釘選。 或者，當應用程式建立篩選圖形時，它可以在輸出釘選上設定所需的媒體類型。

### <a name="aac-decoding"></a>AAC 解碼

針對 AAC，此解碼器在壓縮的 AAC 輸入上有特定的格式條件約束。 這些格式條件約束與媒體基礎 [**AAC 解碼器**](../medfound/aac-decoder.md)相同，並記載于 "[**format 條件約束**](../medfound/aac-decoder.md)" 一節中。

DirectShow 解碼器也可接受與媒體基礎解碼器不同的輸入類型。 DirectShow 解碼器支援下列 AAC 輸入類型：

-   **MEDIASUBTYPE \_RAW \_ AAC1**：原始 AAC，通常會在 AVI 或 Matroska ( 中找到。.MKV) 檔。
-   **MEDIASUBTYPE \_MPEG \_ ADTS \_ AAC**：音訊資料傳輸串流中的 AAC (ADTS) 進行串流處理。
-   **MEDIASUBTYPE \_MPEG \_ loa**：具有同步處理層 (loa) 和多工層 (LATM) 的傳輸資料流程。

媒體基礎的解碼器支援下列 AAC 輸入類型：

-   MFAudioFormat \_ AAC (與 **MEDIASUBTYPE \_ MPEG \_ HEAAC**) 相同，可進行檔播放。
-   **MEDIASUBTYPE \_原始 \_ AAC1**。

### <a name="property-sets"></a>屬性集

此解碼器的輸入 pin 支援下列透過 [**IKsPropertySet**](ikspropertyset.md)的屬性集：

-   [**DVD 禁止複製屬性集**](dvd-copy-protection-property-set.md)
-   [**速率-變更屬性集**](rate-change-property-set.md)。

> [!Note]  
> 從 Windows 7 開始，解碼器會透過速率變更屬性集支援訣竅模式。 它支援範圍 \[ 0.501 –2.0 的播放率 \] ，其中1.0 是正常播放速率，而2.0 是一般速率的兩倍。

 

### <a name="codec-properties"></a>編解碼器屬性

此解碼器的輸入 pin 透過 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)支援下列屬性：



| 屬性                                                          | 需要                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md)     | Windows Vista                                            |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)       | Windows Vista                                            |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)           | Windows Vista                                            |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)             | 僅限 Windows Vista;在 Windows 7 或更新版本中不支援。 |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)         | Windows Vista                                            |
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md) | Windows Vista                                            |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)          | Windows 7                                                |



 

篩選準則透過 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)支援下列屬性：



| 屬性                                                                          | 需要      |
|-----------------------------------------------------------------------------------|---------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                       | Windows 7     |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)       | Windows Vista |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (參閱附注 3. )  | Windows Vista |
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md)     | Windows Vista |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)       | Windows Vista |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)                 | Windows Vista |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                    | Windows Vista |
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md)           | Windows 7     |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                             | Windows 7     |



 

> [!Note]  
> 3. [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md)屬性必須在已連接解碼器的輸出圖釘之前設定。 否則，變更不會有任何作用。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista Home Premium、Windows Vista 旗艦版、Windows 7 \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**音訊子類型**](audio-subtypes.md)
</dt> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[**DVD 媒體類型**](dvd-media-types.md)
</dt> </dl>

 

 
