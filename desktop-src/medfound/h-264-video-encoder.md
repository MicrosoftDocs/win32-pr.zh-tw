---
description: Microsoft 媒體基礎 h.264 影片編碼器是支援下列 h.264 設定檔的媒體基礎轉換：
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: H.264 影片編碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5631239e9db0ddf078848bc3c4a04282e7e79990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982288"
---
# <a name="h264-video-encoder"></a>H.264 影片編碼器

Microsoft 媒體基礎 h.264 影片編碼器是支援下列 h.264 設定檔的 [媒體基礎轉換](media-foundation-transforms.md) ：

-   基準設定檔
-   主要設定檔
-   高設定檔 (需要 Windows 8) 

H.264 video 編碼器會公開下列介面：

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>輸入類型

輸入媒體類型必須有下列其中一個子類型：

-   **MFVideoFormat_I420**
-   **MFVideoFormat_IYUV**
-   **MFVideoFormat_NV12**
-   **MFVideoFormat_YUY2**
-   **MFVideoFormat_YV12**

如需這些子類型的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。

輸出類型必須在輸入類型之前設定。 在設定輸出類型之前，編碼器的 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 方法會傳回 **MF_E_TRANSFORM_TYPE_NOT_SET**。

## <a name="output-types"></a>輸出型別

編碼器支援單一輸出子類型：

-   **MFVideoFormat_H264**

在輸出媒體類型上設定下列屬性。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>主要類型。 必須是 <strong>MFMediaType_Video</strong>。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>影片子類型。 必須是 <strong>MFVideoFormat_H264</strong>。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></td>
<td>平均編碼的位速度，以位/秒為單位。 必須大於零。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></td>
<td>畫面播放速率。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></td>
<td>框架大小。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></td>
<td>交錯模式。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></td>
<td>H.264 編碼設定檔。<br/> 支援的值為：<br/>
<ul>
<li><strong>eAVEncH264VProfile_Base</strong> (預設) </li>
<li><strong>eAVEncH264VProfile_Main</strong></li>
<li><strong>eAVEncH264VProfile_High</strong> (需要 Windows 8) </li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></td>
<td>選擇性。 指定 h.264 編碼層級。<br/> 預設值為–1，表示編碼器將選取編碼層級。<br/> 建議不要設定媒體類型中的層級，並允許編碼器選取層級。 編碼器可以針對指定的影片串流衍生適當的層級，並考慮影片的格式限制和特性。 如需有關設定檔和層級條件約束的詳細資訊，請參閱 ITU-T H. h.264 的附錄 A。<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>選擇性。 指定圖元外觀比例。 預設值為1:1。</td>
</tr>
</tbody>
</table>



 

設定輸出類型之後，影片編碼器會藉由新增 [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) 屬性來更新類型。 此屬性包含 sequence 標頭。

## <a name="codec-properties"></a>編解碼器屬性

H.264 編碼器會實 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面來設定編碼參數。 它支援下列屬性。

如需 HCK 編碼器認證的編解碼器需求，請參閱下面的「 **經認證的硬體編碼器** 」一節。

以下是 Windows 7 中支援的屬性。



| 屬性                                                                              | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI_AVEncCommonRateControlMode**](../directshow/avenccommonratecontrolmode-property.md) | 設定速率控制模式。 請參閱＜備註＞。 預設模式是 (VBR) 的無限制變數位元速率。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**CODECAPI_AVEncCommonQuality**](../directshow/avenccommonquality-property.md)                 | 設定品質等級。 當速率控制模式是以品質為基礎的 VBR (**eAVEncCommonRateControlMode_Quality**) 時，就會套用此屬性。 有效範圍是1–100。 預設值為70。 <br/> 若要設定此參數，請在呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)之前設定屬性。 <br/> 若要在 Windows 7 中設定此參數，請在呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)之前設定屬性。 編碼器會在設定輸出類型之後忽略變更。 <br/> 在 Windows 8 中，您可以在編碼期間隨時設定這個屬性。 從下一個輸入畫面格開始套用變更。 <br/> 編碼器會在內部將此屬性轉換成 [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) 值。 <br/> |



 

下列屬性需要 Windows 8。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></td>
<td>設定適應性編碼模式。 在 Windows 8 中，h.264 編碼器支援下列模式：
<ul>
<li><strong>eAVEncAdaptiveMode_None</strong>。 無適應性編碼。 (預設值。)</li>
<li><strong>eAVEncAdaptiveMode_FrameRate</strong>。 自我調整變更畫面播放速率。</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></td>
<td>以位元組為單位，設定常數速率的緩衝區大小（以位元組為單位） (CBR) 編碼。<br/> 有效範圍為 [1 .。。2³²-1]。 <br/> 需要 Windows 8。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></td>
<td>針對 [受條件約束的 VBR 編碼]，指定 &quot; 有漏洞 bucket 的清空速率 &quot; （以每秒位數為單位）。 當速率控制模式 <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>時，就會套用此屬性。 <br/> 有效範圍為 [1 .。。2³²-1]。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></td>
<td>設定編碼位資料流程的平均位元速率，以每秒位數為單位。 如果 <strong>eAVEncCommonRateControlMode_Quality</strong>的速率控制模式，則會忽略這個屬性。 <br/> 有效範圍為 [1 .。。2³²-1]。 <br/> 在 CBR 和未受限制的 VBR 模式中，平均位元速率會決定檔案的最終大小。 在 CBR 模式中，平均位元速率也是壓縮的位從有漏洞值區中排出的速率 &quot; 。 &quot; (如需詳細資訊，請參閱 <a href="the-leaky-bucket-buffer-model.md">有漏洞 bucket 緩衝區模型</a>。 )  <br/> 在 Windows 7 中，平均位元速率是由媒體類型上的 <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> 屬性所指定。 <br/> 在 Windows 8 中，您可以使用 <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> 屬性或 <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> 屬性來設定平均位元速率。 如果兩者都已設定，CODECAPI_AVEncCommonMeanBitRate 覆寫。 在 Windows 8 中，您可以設定編碼期間的平均位元速率。 如果位元速率有所變更，則編碼器會使用適應性編碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></td>
<td>設定品質/速度的取捨。 有效範圍：
<ul>
<li>0-33：低複雜度</li>
<li>34–66：中等複雜度 (預設) </li>
<li>67–100：高複雜度</li>
</ul>
<br/> 此值會影響編碼器執行各種編碼作業（例如動作補償）的方式。 在較高的複雜性層級中，編碼器的執行速度會更慢，但以相同的位元速率產生更高的品質。<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></td>
<td>啟用或停用 CABAC (內容自我調整二進位算術編碼) 適用于 h.264 熵編碼。 預設值為 <strong>VARIANT_FALSE</strong>。 <br/> CABAC 不會用於基準設定檔。<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></td>
<td>將 NAL 的 <strong>seq_parameter_set_id</strong> 值設定在 h.264 位流的 SPS 單位中。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></td>
<td>設定輸出位流中連續 B 框架的最大數目。 有效值為：
<ul>
<li>0：請勿使用 B 框架 (預設) 。</li>
<li>1：使用一個 B 框架。</li>
<li>2：使用兩個 B 框架。</li>
</ul>
若要設定此參數，請在呼叫 <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform：： SetOutputType</strong></a>之前設定屬性。 <br/> 針對基準設定檔，B 框架的數目一律為零。 編碼器將覆寫非零值。<br/> 針對其他 h.264 設定檔，如果此屬性為非零，則會 IBBPBBP 編碼模式，其中連續 B 框架的最大數目等於 <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></td>
<td>將每個 GOP 標頭的圖片數目設定為下一個，包括前置錨點，但不包括下列各項。 <br/> 有效範圍是 [0 .。。2³²-1]。 如果為零，則編碼器會選取 GOP 大小。 預設值為零。 <br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></td>
<td>設定編碼器所使用的背景工作執行緒數目。<br/> 有效範圍為0到16。 如果為零，則編碼器會選取執行緒的數目。 <br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></td>
<td>表示影片內容的類型。<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></td>
<td>有效範圍：16–51。 預設值為24。 <br/> 當速率控制模式 <strong>eAVEncCommonRateControlMode_Quality</strong>時，就會套用此屬性。 <br/> 這個屬性會設定與 <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>相同的編碼設定。 但是， <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> 可讓應用程式直接指定 QP 的值。 如果同時設定這兩個屬性，則 AVEncVideoEncodeQP 覆寫。 <br/> 預設值24對應于 <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> 設定的預設值70。<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></td>
<td>強制編碼器將下一個畫面格編碼為主要畫面格。<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></td>
<td>有效範圍：0到51。 預設值為 0。 <br/> 這個屬性會套用至所有速率控制模式。 編碼器不應產生小於 <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> 屬性指定的值。<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></td>
<td>啟用或停用低延遲模式。 請參閱「 &quot; &quot; 備註」一節中的多執行緒。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

編碼器支援下列速率控制模式。



| 模式                                  | 常數                                            | 描述                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 固定位元速率 (CBR)                | **eAVEncCommonRateControlMode_CBR**                | 編碼器會使用 "有漏洞 bucket" 模型，嘗試達到常數的位元速率。 目標位速率是由 [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) 屬性提供。 <br/> 需要 Windows 8。 <br/> |
|  (VBR) 的限制變數位速率   | **eAVEncCommonRateControlMode_PeakConstrainedVBR** | 編碼器會使用具有尖峰位速率的「有漏洞 bucket」模型。 有漏洞 bucket 的清空率是由 [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) 屬性提供。 <br/> 需要 Windows 8。 <br/>     |
| 以品質為基礎的變數位元速率 (VBR)  | **eAVEncCommonRateControlMode_Quality**            | 編碼器會嘗試達成 [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) 屬性所提供的常數品質層級。                                                                                                           |
| 未受限制的 VBR                     | **eAVEncCommonRateControlMode_UnconstrainedVBR**   | 編碼器嘗試達到輸出媒體類型中 [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) 屬性指定的目標位元速率。 這是預設模式。                                                              |



 

CBR 和受限的 VBR 模式需要 Windows 8。

在 Windows 8 中，編碼器會在輸出範例中設定下列屬性：

-   [MFSampleExtension_DecodeTimestamp](mfsampleextension-decodetimestamp.md)
-   [MFSampleExtension_VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)
-   [MFSampleExtension_VideoEncodeQP](mfsampleextension-videoencodeqp.md)

> [!Note]  
> 先前版本的檔不正確地指出 Windows Server 2008 R2 支援編碼器。

 

### <a name="multithreading"></a>多執行緒

在 Windows 8 中，編碼器支援兩種編碼模式：

-   **配量編碼。** 在此模式中，配量會以平行方式編碼。 每個配量都會在不同的執行緒上進行編碼。 這個模式的延遲很低，因為單一圖片會以平行方式編碼。 不過，此方法不會隨著核心數目的增加而調整，因為配量的數目是由輸入圖片中的巨大區塊資料列數目所限制。
-   **多畫面編碼。** 在此模式中，編碼器會接受多個輸入畫面格，並以平行方式進行編碼。 這個模式在多核心環境中會調整得更好，但會引進更多延遲。

編碼器預設為配量編碼，以將延遲降至最低。 若要啟用多畫面編碼，請將 [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) 屬性設定為 **VARIANT_FALSE**。

若要設定編碼器所使用的背景工作執行緒數目，請設定 [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) 屬性。

在 Windows 7 中，編碼器一律會使用配量編碼。

### <a name="certified-hardware-encoder"></a>經認證的硬體編碼器

如果有認證硬體編碼器，通常會使用它來取代媒體基礎相關案例的收件匣系統編碼器。 需要經過認證的編碼器，才能支援特定的 **ICodecAPI** 屬性集，並可選擇性地支援另一組屬性。 認證程式應保證所需的屬性受到適當支援，而且如果支援選擇性屬性，也會受到適當的支援。

以下是用來傳遞 HCK 編碼器認證之編碼器的必要和選擇性 **ICodecAPI** 屬性集。

需要下列 Windows 8 和 Windows 8.1 **ICodecAPI** 屬性：

-   [CODECAPI_AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI_AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md)
-   [CODECAPI_AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI_AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI_AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

下列 Windows 8.1 **ICodecAPI** 屬性是選擇性的，但如果支援，則會在 HCK 中進行測試。

-   [CODECAPI_AVEncVideoMinQP](codecapi-avencvideominqp.md)
-   [CODECAPI_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md)
-   [CODECAPI_AVEncVideoMarkLTRFrame](codecapi-avencvideomarkltrframe.md)
-   [CODECAPI_AVEncVideoUseLTRFrame](codecapi-avencvideouseltrframe.md)
-   [CODECAPI_AVEncVideoEncodeFrameTypeQP](codecapi-avencvideoencodeframetypeqp.md)
-   [CODECAPI_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md)
-   [CODECAPI_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md)
-   [CODECAPI_AVEncVideoMaxNumRefFrame](codecapi-avencvideomaxnumrefframe.md)
-   [CODECAPI_AVEncVideoMeanAbsoluteDifference](codecapi-avencvideomeanabsolutedifference.md)
-   [CODECAPI_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md)
-   [CODECAPI_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md)
-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (動態) 
-   [CODECAPI_AVEncH264CABACEnable](codecapi-avench264cabacenable.md)

下列 Windows 8 和 Windows 8.1 **ICodecAPI** 屬性是選擇性的，但如果支援，則會在 HCK 中進行測試。

-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (靜態) 
-   [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md)

下列 **ICodecAPI** 屬性是選擇性的。 它們不會在 HCK 中進行測試。

-   [CODECAPI_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh264enc.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[媒體基礎中的 MPEG 4 支援](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[影片媒體類型](video-media-types.md)
</dt> </dl>

 

 
