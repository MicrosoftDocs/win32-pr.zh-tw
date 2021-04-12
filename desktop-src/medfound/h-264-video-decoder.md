---
description: 媒體基礎 h.264 視頻編碼程式是一種媒體基礎轉換，支援基準、主要和高設定檔的解碼，最多可達層級5.1。
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: H.264 Video 解碼
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75c4713b1a4e36d1ba085b2239c24ca0f6e4fae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468613"
---
# <a name="h264-video-decoder"></a>H.264 Video 解碼

媒體基礎 h.264 視頻編碼程式是一種 [媒體基礎轉換](media-foundation-transforms.md) ，支援基準、主要和高設定檔的解碼，最多可達層級5.1。

H.264 video 解碼會公開下列介面。

-   Windows 8) 支援的 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

若要建立此解碼器的實例，請執行下列其中一項：

-   呼叫 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 或 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數。
-   呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)。 此解碼器的 CLSID 是 **clsid \_ CMSH264DecoderMFT**，宣告于 wmcodecdsp 中。

## <a name="input-types"></a>輸入類型

輸入類型必須至少包含下列兩個屬性：



| 屬性                                                 | 描述                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) | **MFMediaType \_ 影片**                                                                        |
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)        | [MFVideoFormat \_H264](video-subtype-guids.md) 或 MFVideoFormat \_ h264 \_ ES |



 

如果輸入類型只包含這兩個屬性，則此解碼器將提供預設輸出類型，作為預留位置。 當解碼器收到足夠的輸入樣本來產生輸出框架時，它會從 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)傳回 **MF \_ E \_ 轉換 \_ 串流 \_ 變更**，以發出格式變更的信號。 如需處理格式變更的詳細資訊，請參閱 **ProcessOutput** 檔。

若要避免初始格式變更，請盡可能在輸入類型中提供最多資訊，包括：



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
<td><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></td>
<td>畫面播放速率。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></td>
<td>框架維度。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></td>
<td>交錯模式。
<blockquote>
[!Note]<br />
在 h.264 video 中，交錯結構可以動態變更，因此會 <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>這個屬性的建議值。 影片基本資料流程中的交錯資訊優先于媒體類型。 如需詳細資訊，請參閱 <a href="video-interlacing.md">影片交錯</a>。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>圖元外觀比例。</td>
</tr>
</tbody>
</table>



 

輸入類型必須在輸出類型之前設定。 在設定輸入類型之前，編碼器的 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 方法會傳回 **\_ \_ \_ \_ 未 \_ 設定的 MF E 轉換類型**。

## <a name="output-types"></a>輸出型別

此解碼器支援下列輸出子類型：

-   **MFVideoFormat \_ I420**
-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

如需這些子類型的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。

## <a name="transform-attributes"></a>轉換屬性

H.264 解碼會實行 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。 應用程式可以使用這個方法來取得或設定下列屬性。



| 屬性                                                                                       | 描述                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecVideoAcceleration \_ H264](../directshow/avdecvideoacceleration-h264-property.md)            | 啟用或停用硬體加速。                                                 |
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) | 啟用或停用縮圖產生模式。                                             |
| [MF \_ SA \_ D3D \_ 感知](mf-sa-d3d-aware-attribute.md)                                             | 指出此解碼器支援 (DXVA) 的 DirectX Video 加速。 視為唯讀。 |



 

在 Windows 8 中，h.264 解碼器也支援下列屬性。



| 屬性                                                                                                     | 描述                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | 啟用或停用低延遲解碼模式。                                                              |
| [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)                                         | 設定用於此解碼器的背景工作執行緒數目。                                                      |
| [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)                                     | 設定解碼器將接受做為輸入類型的最大圖片寬度。                               |
| [CODECAPI \_ AVDecVideoMaxCodedHeight](codecapi-avdecvideomaxcodedheight.md)                                   | 設定解碼器將接受做為輸入類型的最大圖片高度。                              |
| [MF \_ SA \_ 最小 \_ 輸出 \_ 範例 \_ 計數](mf-sa-minimum-output-sample-count.md)                               | 指定輸出樣本的最大數目。                                                             |
| [MFT \_ 解碼 \_ 會 \_ \_ \_ 以 \_ 原生 \_ 順序公開輸出類型](mft-decoder-expose-output-types-in-native-order.md) | 指定解碼器是否公開 IYUV/I420 輸出類型 (適用于其他格式之前的轉碼) 。 |



 

在 Windows 8 中，h.264 解碼支援 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面。 此介面提供 alternativate API 來設定下列編解碼器屬性。

-   [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)
-   [CODECAPI \_ AVDecVideoAcceleration \_ H264](../directshow/avdecvideoacceleration-h264-property.md)
-   [CODECAPI \_ AVDecVideoMaxCodedHeight](codecapi-avdecvideomaxcodedheight.md)
-   [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)
-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a>格式條件約束

此解碼器支援下列格式：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>設定檔/層級</td>
<td>基準、主要和高設定檔，最高到層級5.1。  (如需詳細資料，請參閱 ITU-T h.264 規格。 ) </td>
</tr>
<tr class="even">
<td>色度格式</td>
<td>4:2:0 色度或單色</td>
</tr>
<tr class="odd">
<td>最低解析度</td>
<td>48×48圖元</td>
</tr>
<tr class="even">
<td>最大解析度</td>
<td>4096×2304圖元<br/> DXVA 加速的保證解析度上限為1920×1088圖元;在較高的解析度中，解碼是使用 DXVA 來完成（如果基礎硬體支援的話），否則會使用軟體進行解碼。<br/>
<blockquote>
[!Note]<br />
在 Windows 7 中，軟體和 DXVA 解碼的最大支援解析度為1920×1088圖元。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>DXVA</td>
<td>此解碼器支援 DXVA 第2版，但不支援 DXVA 第1版。 只有主要相容的基準、主要和高設定檔 bitstreams 才支援 DXVA 解碼。  (主要相容的基準 bitstreams 定義為 <strong>profile_idc</strong>= 66， <strong>constrained_set1_flag</strong>= 1。 ) </td>
</tr>
</tbody>
</table>



 

輸入資料必須符合 ISO/IEC 14496-10 的附錄 B。 資料必須包含起始碼。 除非在位元組資料流程中找到有效的 sequence 參數集 (SPS) 和圖片參數集 (PPS) ，否則此解碼器會略過位元組。

此解碼器不支援電影細微性技術。

> [!Note]  
> 先前版本的檔不正確地指出 Windows Server 2008 R2 支援此解碼器。

 

如果已安裝 Windows Vista 的平臺更新補充，則可以在 Windows Vista 上使用 h.264 video 解碼器，但只能使用 [來源讀取器](source-reader.md)在 windows vista 上進行存取。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                  |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



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

 

 
