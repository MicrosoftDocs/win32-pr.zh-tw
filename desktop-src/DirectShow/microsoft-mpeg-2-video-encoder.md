---
description: Microsoft MPEG-2 影片編碼器篩選器會將 MPEG-2 和 MPEG-2 影片編碼。
ms.assetid: d52c1299-0641-405c-8960-edd738b56823
title: 'Microsoft MPEG-2 影片編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c96db605586c6abf0f51537689a9365df2842c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973140"
---
# <a name="microsoft-mpeg-2-video-encoder"></a>Microsoft MPEG 2 影片編碼器

Microsoft MPEG-2 影片編碼器篩選器會將 MPEG-2 和 MPEG-2 影片編碼。

若要編碼和多工音訊/影片串流，請使用 [**MICROSOFT Mpeg-2 編碼器**](microsoft-mpeg-2-encoder.md) 篩選器，它會封裝此篩選器和 [**Microsoft mpeg-2 音訊編碼器**](microsoft-mpeg-2-audio-encoder.md) 篩選器的功能。

> [!Note]  
> 以 IA-64 為基礎的平臺不支援此篩選器。

 



篩選資訊

篩選介面

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

輸入 Pin 媒體類型

**媒體媒體 \_影片**、 **MEDIASUBTYPE \_ I420**<br/> **媒體媒體 \_影片**、 **MEDIASUBTYPE \_ IYUV**<br/> **媒體媒體 \_影片**、 **MEDIASUBTYPE \_ RGB24**<br/> **媒體媒體 \_影片**、 **MEDIASUBTYPE \_ UYVY**<br/> **媒體媒體 \_影片**、 **MEDIASUBTYPE \_ YUY2**<br/> **媒體媒體 \_影片**、 **MEDIASUBTYPE \_ YV12**<br/>

輸入 Pin 介面

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

輸出 Pin 媒體類型

**媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ 影片**<br/> **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ 方案**<br/> **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**<br/> **媒體媒體 \_影片**， **MEDIASUBTYPE \_ MPEG2 \_ 影片**<br/>

輸出 Pin 介面

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

篩選 CLSID

**CLSID \_** 在 wmcodecdsp 中宣告的 CMPEG2EncoderVideoDS () 

可執行檔

msmpeg2enc.dll

[優點](merit.md)

**\_ \_ 未 \_ 使用的業績**

[篩選準則分類](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>備註

MPEG-2 影片編碼器可以產生下列種類的輸出：

-   影片基本資料流程
-   MPEG-2 程式串流中的影片
-   MPEG-2 傳輸串流中的影片

它支援下列 MPEG-2 設定檔和層級：



| 設定檔        | 等級                     | 備註                                            |
|----------------|----------------------------|----------------------------------------------------|
| 簡單設定檔 | 主要區段                       |                                                    |
| 主要設定檔   | 低、主要、高、高1440 |                                                    |
| 高調明確   | Main、High、High-1440      |  (只有 4:2:0) 的擴充性或4:2:2/4:4:4 支援 |
| 4:2:2 設定檔  | 主要、高                 |  (只有 4:2:0) 的擴充性或4:2:2 支援       |



 

### <a name="codec-properties"></a>編解碼器屬性

篩選準則透過 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)支援下列屬性。



| 屬性                                                                                      | 預設                                                          | 支援的值                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                             | MPEG-2 影片                                                     | **CODECAPI \_ GUID \_ AVEncMPEG1Video**<br/> **CODECAPI \_ GUID \_ AVEncMPEG2Video**<br/>                                                                                                                        |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)                         | 12222464位                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)                       | 12222464位                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                               | 12222464位                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)                   | [未指定]                                                      | **CODECAPI \_GUID \_ AVEncCommonFormatUnSpecified** (沒有格式條件約束) <br/> **CODECAPI \_GUID \_ AVEncCommonFormatDVD \_ V** (DVD-影片) <br/> **CODECAPI \_GUID \_ AVEncCommonFormatVCD** (視訊 CD) <br/> |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                               | 9800000 (9.8 Mb/秒)                                        |                                                                                                                                                                                                                      |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                             | 7000000 (7.0 Mb/秒)                                        |                                                                                                                                                                                                                      |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                               | 128                                                              |                                                                                                                                                                                                                      |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)                         | 1                                                                | 1                                                                                                                                                                                                                    |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                                     | 100                                                              | 1—100                                                                                                                                                                                                              |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)                       | 75                                                               | 0-100                                                                                                                                                                                                              |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)                     | Cbr                                                              | **eAVEncCommonRateControlMode \_ CBR**<br/> **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**<br/> **eAVEncCommonRateControlMode \_ 品質**<br/>                                                   |
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                               | [未指定]                                                      | \_未指定 eAVEncInputVideoSystem<br/> eAVEncInputVideoSystem \_ PAL<br/> eAVEncInputVideoSystem \_ NTSC<br/>                                                                                        |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)                 | 2                                                                | 0-2                                                                                                                                                                                                                |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                             | 框架模式                                                       |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)         | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)                 | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                           | **FALSE**                                                        |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                       | 1                                                                | 0-1                                                                                                                                                                                                                |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                           | 18個框架 (36 個欄位) 用於 NTSC;15個框架 (30 個欄位) 否則為。 | 1-30;請參閱備註                                                                                                                                                                                                  |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                         | 9                                                                | 8-10                                                                                                                                                                                                               |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                               | 高                                                             |                                                                                                                                                                                                                      |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                           | 主要區段                                                             |                                                                                                                                                                                                                      |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)   | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)               | Interlaced                                                       | **交錯式 eAVEncVideoSourceScan \_**<br/> **eAVEncVideoSourceScan \_ 漸進式**<br/>                                                                                                                   |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)           | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0) <br/> **eAVEncVideoChromaResolution \_ SameAsSource**<br/>                                                                                                     |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)         | 與來源相同                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)         | 與來源相同                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)               | 與來源相同                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md) | 與來源相同                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)     | 與來源相同                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)               | [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1          | 0或 [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                                                                                                                                                         |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                 | 0                                                                |                                                                                                                                                                                                                      |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)         | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0) <br/> **eAVEncVideoChromaResolution \_ SameAsSource**<br/>                                                                                                     |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                       |                                                                  | 必須與輸入畫面播放速率相同。                                                                                                                                                                            |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                         | 與輸入相同                                                    | **eAVEncVideoOutputScan \_ SameAsInput**                                                                                                                                                                               |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                     | 1:1                                                              |                                                                                                                                                                                                                      |



 

建議您以下列順序設定屬性：

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncCodecType**](avenccodectype-property.md)
3.  [**AVEncMPVProfile**](avencmpvprofile-property.md)
4.  [**AVEncMPVLevel**](avencmpvlevel-property.md)
5.  [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)

以任何順序設定其餘的屬性。  (不過，請參閱 [GOP 結構](#gop-structure)。 ) 

當篩選圖形正在執行時，可以設定屬性。 至少有一個 GOP 延遲，新的設定才會生效。

### <a name="encoder-operation"></a>編碼器操作

編碼 MPEG 1 影片時，如果符合所有條件約束，編碼器會自動設定 sequence 標頭中的1位 **限制 \_ 參數 \_ 旗** 標代碼。

如有需要，編碼器會將輸入影片維度四捨五入，讓輸出影片尺寸符合 MPEG 需求。 針對漸進式影片，輸出維度會舍入為寬度和高度的16倍數。 若為交錯式影片，width 會進位至16的倍數，且高度會進位至32的倍數。 此進位作業會視需要使用填補。

如果影片是交錯的，則編碼器會 (3:2) 偵測來執行自動電影。 輸入影片除了交錯框架之外，還可以包含欄位圖片組。

編碼器的內部格式為 4:2:0 IYUV (與 I420) 相同。 它可以從 YUY2、YV12、UYVY 和 RGB-24 影片格式執行色彩轉換。

若要將位流限制為 (DVD 或 VCD) 的目標格式，請設定 [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md) 屬性。 如果這個屬性具有 **GUID \_ AVEncCommonFormatUnSpecified** 以外的值，則編碼器會將 MPEG 語法限制為目標格式所允許的。

若為即時編碼，請將 [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) 屬性設定為零。 這會導致編碼器針對速度優化。

### <a name="encoding-modes"></a>編碼模式

編碼器支援數種編碼模式：

-   一次傳遞的常數位元速率 (CBR) 。
-   使用常數 quantizer 步驟大小，將以品質為基礎的變數位元速率 (VBR) 。 在此模式中，編碼器會嘗試符合目標品質等級，最高可達最大位元速率。
-   一次傳遞尖峰條件約束的 VBR。 在此模式中，編碼器會嘗試在特定的內部限制內達到目標平均位元速率。

若要設定編碼模式，請設定下列屬性：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>模式</th>
<th>屬性</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Cbr</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  = <strong>eAVEncCommonRateControlMode_CBR</strong><br/> <a href="avenccommonqualityvsspeed-property.md"><strong>AVEncCommonQualityVsSpeed</strong></a><br/> <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br/></td>
</tr>
<tr class="even">
<td>以品質為基礎的 VBR</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  = <strong>eAVEncCommonRateControlMode_Quality</strong><br/> <a href="avenccommonquality-property.md"><strong>AVEncCommonQuality</strong></a><br/> <a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br/>
<blockquote>
[!Note]<br />
在此模式中，不會使用 <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a> 和 <a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a> 屬性。 最低位元速率會假設為零。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>尖峰限制的 VBR</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  = <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong><br/> <a href="avenccommonmultipassmode-property.md"><strong>AVEncCommonMultipassMode</strong></a> = 1<br/> <a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a><br/> <a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br/> <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> 不支援雙通過 VBR。

 

### <a name="aspect-ratio"></a>外觀比例

顯示外觀比例和圖元外觀比例 (PAR) 與下列公式相關：

<dl> 顯示外觀比例 = PAR × (圖片寬度/圖片高度)   
</dl>

編碼器會使用此公式來計算 mpeg-2 \_ \_ BITSTREAMS 的 mpeg-2 bitstreams 或外觀比例資訊的 pel 外觀比例 \_ 值 \_ 。  (分別參閱 ISO/IEC 11172 和 ISO/IEC 138181-2。 ) 

編碼器會依序嘗試下列設定：

1.  如果應用程式在篩選圖形執行之前的任何時間都設定 [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md) 屬性，則會使用這個屬性做為 PAR。
2.  否則，如果 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)結構的 **dwPictAspectRatioX** 和 **dwPictAspectRatioY** 成員不是零，則會使用這些成員做為顯示外觀比例，而 PAR 則是從顯示外觀比例計算而得。
3.  如果這些值都不存在，則會假設為等於1.0，並據此計算顯示外觀比例。

在即時編碼模式中 ([**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) 等於零) ，顯示外觀比例必須是4:3 或16:9，預設值為4:3。 如果計算的顯示外觀比例不是4:3 或16:9，則編碼器會使用值4:3。

### <a name="gop-structure"></a>GOP 結構

若要指定 (GOP) 結構的圖片群組，請依序設定下列屬性：

1.  [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)
2.  [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)
3.  [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)

根據這些設定，編碼器會產生下列其中一個 GOP 結構：



| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md) | [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md) | GOP 結構 |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------|---------------|
| 0                                                                               | 0                                                                             | IIII...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 0                                                                             | IPPP...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 1                                                                             | IBPBP...      |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 2                                                                             | IBBPBBP...    |



 

預設的 GOP 結構為 IBBPBBP .。。具有15個框架的 GOP 大小。

如果應用程式透過 [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)) 屬性將目標格式限制為 DVD (，並將 [**AVEncInputVideoSystem**](avencinputvideosystem-property.md) 屬性設定為 NTSC 或 PAL，則編碼器支援下列 GOP 大小：



| 影片系統 | 有效的 GOP 大小 | 預設 GOP 大小 |
|--------------|-----------------|------------------|
| Ntsc         | 1-18            | 18 (36 欄位)    |
| PAL          | 1-15            | 15 (30 個欄位)    |



 

### <a name="codec-property-change-lists"></a>編解碼器屬性變更清單

設定一個編解碼器屬性的值時，可以變更另一個屬性的有效範圍。  (例如，限制目標格式會限制平均位元速率。 ) 每當應用程式設定屬性時，編碼器會檢查是否有任何其他屬性現在落在有效範圍之外。 如果是的話，編碼器會將該屬性重設為新的預設值。 若要在發生這種情況時接收通知，請執行下列動作：

1.  使用值 **CODECAPI \_ CHANGELISTS** 來呼叫 [**ICodecAPI：： RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) 。
2.  您可以使用 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 介面來監視篩選圖形中的事件。
3.  如果屬性的範圍或預設值變更，則編碼器會傳送包含已變更屬性清單的 [**EC \_ CODECAPI \_ 事件**](ec-codecapi-event.md) 事件。

### <a name="iencoderapi-support"></a>IEncoderAPI 支援

為了回溯相容性，此篩選會透過 **IEncoderAPI** 介面支援下列屬性：



| 屬性                       | 描述                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------|
| **ENCAPIPARAM \_ 位元速率**       | 相當於 [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)。         |
| **ENCAPIPARAM \_ 尖峰 \_ 位元速率** | 相當於 [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)。           |
| **ENCAPIPARAM \_ 位元速率 \_ 模式** | 相當於 [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)。 |



 

設定 **ENCAPIPARAM \_ 位元速率 \_ 模式** 屬性時，值會對應如下：



| **ENCAPIPARAM \_ 位元速率 \_ 模式** | [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) |
|--------------------------------|---------------------------------------------------------------------------|
| **T t e**            | **eAVEncCommonRateControlMode \_ CBR**                                      |
| **VariableBitRateAverage**     | 請參閱附註。                                                                 |
| **VariableBitRatePeak**        | **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       |



 

> [!Note]  
> 目前，MPEG-2 視頻編碼器不支援 **VariableBitRateAverage** 編碼模式。 如果您設定此值，編碼器會預設為 CBR 編碼 (**eAVEncCommonRateControlMode \_ CBR**) 。

 

取得 **ENCAPIPARAM \_ 位元速率 \_ 模式** 屬性時，值會對應如下：



| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) | **ENCAPIPARAM \_ 位元速率 \_ 模式** |
|---------------------------------------------------------------------------|--------------------------------|
| **eAVEncCommonRateControlMode \_ CBR**                                      | **T t e**            |
| **eAVEncCommonRateControlMode \_ 品質**                                  | **VariableBitRatePeak**        |
| **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       | **VariableBitRatePeak**        |



 

### <a name="limitations"></a>限制

編碼器目前不支援下列任何功能：

-   產生 packetized 基本資料流程 (PE) 封包。
-   畫面播放速率轉換。 輸入資料流程的畫面播放速率必須是對 MPEG-2 位流有效的畫面播放速率。
-   MPEG-2 的畫面播放速率延伸 (**畫面播放速率 \_ \_ 延伸 \_ n**、 **幀 \_ 速率 \_ 擴充功能 \_ d**) 。
-   進入/離開緩衝區 (VBV 剪輯) 位置。
-   將行21資料 (隱藏式輔助字幕資訊) 插入影片基礎資料流程中。
-   在 MPEG-2 的 GOP 標頭中設定 [25 位 **時間 \_ 代碼** ] 欄位。
-   Denoise 篩選準則。
-   數位版權管理 (DRM) 。

編碼器導入了至少一個 GOP 的編碼延遲。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista Home Premium、Windows Vista 旗艦版、Windows 7 Home Premium、Windows 7 Professional、Windows 7 企業版、僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl>                                                                                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[**MPEG-2 信號信號媒體類型**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
