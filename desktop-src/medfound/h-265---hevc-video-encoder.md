---
description: 媒體基礎 .H 的視頻編碼器是媒體基礎轉換，支援將內容編碼為 HEVC 格式。
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: H. 265/HEVC 影片編碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015295792a72f3250c47389192586dbc00566858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943689"
---
# <a name="h265--hevc-video-encoder"></a>H. 265/HEVC 影片編碼器

媒體基礎 .H 的視頻編碼器是 [媒體基礎轉換](media-foundation-transforms.md) ，支援將內容編碼為 HEVC 格式。 編碼器支援下列設定檔：

-   主要設定檔

H. 視頻編碼器會公開下列介面：

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>輸入類型

輸入媒體類型必須有下列其中一個子類型：

-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

如需這些子類型的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。

輸出類型必須在輸入類型之前設定。 在設定輸出類型之前，編碼器的 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 方法會傳回 **\_ \_ \_ \_ 未 \_ 設定的 MF E 轉換類型**。

## <a name="output-types"></a>輸出型別

編碼器支援單一輸出子類型：

-   **MFVideoFormat \_ H265**

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
<td>影片子類型。 必須是 <strong>MFVideoFormat_HEVC</strong>。</td>
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
<td><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></td>
<td>H. 265 編碼設定檔。<br/> 支援的值為： <br/>
<ul>
<li><strong>eAVEncH265VProfile_Main_420_8</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></td>
<td>指定編碼影片的層級。 如需有關設定檔和層級條件約束的詳細資訊，請參閱 ITU-T H. 265 的附錄 A。<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>選擇性。 指定圖元外觀比例。 預設值為1:1。</td>
</tr>
</tbody>
</table>



 

設定輸出型別之後，影片編碼器會藉由新增 [**MF \_ MT \_ MPEG \_ SEQUENCE \_ 標頭**](mf-mt-mpeg-sequence-header-attribute.md) 屬性來更新型別。 此屬性包含 sequence 標頭。

## <a name="supported-imftransform-methods"></a>支援的 IMFTransform 方法

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)介面的下列方法支援適用于 .H/HEVC 編碼器：

-   [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [**GetInputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [**GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [**GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [**GetOutputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [**GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [**GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [**In processevent.<**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [**SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

所有其他 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 方法都會傳回錯誤 E \_ >notimpl。

## <a name="supported-icodecapi-methods"></a>支援的 ICodecAPI 方法

[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)介面的下列方法支援適用于 .H/HEVC 編碼器：

-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

所有其他 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 方法都會傳回錯誤 E \_ >notimpl。

## <a name="codec-properties"></a>編解碼器屬性

H. 編碼程式會實 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面來設定編碼參數。 它支援下列屬性。

如需 HCK 編碼器認證的編解碼器需求，請參閱下面的「 **經認證的硬體編碼器** 」一節。



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
<td><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></td>
<td>設定速率控制模式。 支援的模式如下：<br/>
<ul>
<li><strong>eAVEncCommonRateControlMode_CBR</strong></li>
<li><strong>eAVEncCommonRateControlMode_Quality</strong></li>
</ul>
如果指定了其他模式，則會使用 <strong>eAVEncCommonRateControlMode_CBR</strong> 速率控制。<br/> 這是 VT_UI4 的值。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></td>
<td>設定編碼位資料流程的平均位元速率，以每秒位數為單位。 <br/> 有效範圍為 [1 .。。2³²-1]。 <br/> 這是 VT_UI4 的值。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></td>
<td>以位元組為單位，設定常數速率的緩衝區大小（以位元組為單位） (CBR) 編碼。<br/> 有效範圍為 [1 .。。2³²-1]。 <br/> 這是 VT_UI4 的值。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></td>
<td>針對速率控制模式設定允許尖峰位元速率的最大位元速率。 <br/> 有效範圍為 [1 .。。2³²-1]。 <br/> 這是 VT_UI4 的值。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></td>
<td>將每個 GOP 標頭的圖片數目設定為下一個，包括前置錨點，但不包括下列各項。 <br/> 有效範圍是 [0 .。。2³²-1]。 如果為零，則編碼器會選取 GOP 大小。 預設值為零。 <br/> 這是 VT_UI4 的值。<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></td>
<td>啟用或停用低延遲模式。 <br/> 這是 VT_BOOL 的值。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></td>
<td>設定品質/速度的取捨。 此值會影響編碼器執行各種編碼作業（例如動作補償）的方式。 在較高的複雜性層級中，編碼器的執行速度會更慢，但以相同的位元速率產生更高的品質。 <br/> 有效範圍為 0-100。 就內部而言，此值會對應至編碼器所支援的一組較小品質/速度層級。<br/> 這是 VT_UI4 的值。<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></td>
<td>強制編碼器將下一個畫面格編碼為主要畫面格。<br/> 這是 VT_UI4 的值。<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></td>
<td>設定此屬性時，會導致編碼器使用指定的 QP 來編碼下一個框架和所有後續的框架，直到指定新的 QP 為止。 <br/> 有效範圍：0–51（含） <br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></td>
<td>這個屬性會設定編碼器在 CBR ratecontrol 期間可以使用的最小 QP 的限制。<br/> 這是 VT_UI4 的值。<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></td>
<td>這個屬性會設定在 CBR ratecontrol 期間，編碼器可使用的最大 QP 值的限制。<br/> 這是 VT_UI4 的值。<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></td>
<td>設定內容是否為全螢幕的影片，而不是可能有較小影片視窗或完全沒有影片的螢幕內容。<br/> 這是 VT_UI4 的值。<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></td>
<td>設定用來執行壓縮作業的執行緒數目。 編碼器會將框架分成磚，使執行緒數目等於磚數目。<br/>
<ul>
<li>邏輯處理器的數目。 執行緒的數目必須小於或等於邏輯處理器的數目。</li>
<li>框架的大小。 磚的大小必須大於或等於265x64 圖元。</li>
<li>同位。 執行緒的數目必須是偶數值。 如果指定的值為奇數，則會使用下一個較低的偶數值。</li>
</ul>
這是 VT_UI4 的值。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="certified-hardware-encoder"></a>經認證的硬體編碼器

如果有認證硬體編碼器，通常會使用它來取代媒體基礎相關案例的收件匣系統編碼器。 需要經過認證的編碼器，才能支援特定的 **ICodecAPI** 屬性集，並可選擇性地支援另一組屬性。 認證程式應保證所需的屬性受到適當支援，而且如果支援選擇性屬性，也會受到適當的支援。

以下是用來傳遞 HCK 編碼器認證之編碼器的必要和選擇性 **ICodecAPI** 屬性集。

-   [CODECAPI \_ AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI \_ AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI \_ AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI \_ AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI \_ AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh265enc.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> </dl>

 

 
