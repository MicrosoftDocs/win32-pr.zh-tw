---
description: MPEG-2 視頻解碼器是一種媒體基礎轉換，可將 MPEG-2 和 MPEG-2 影片解碼。
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: MPEG-2 視頻解碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca4384154faff777280fd0a03cf4fd289603e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512596"
---
# <a name="mpeg-2-video-decoder"></a>MPEG-2 視頻解碼器

MPEG-2 視頻解碼器是一種 [媒體基礎轉換](media-foundation-transforms.md) ，可將 MPEG-2 和 Mpeg-2 影片解碼。 此解碼器支援 MPEG-2 的簡單和主要設定檔影片 (262、ISO/IEC 13818-2) 和 MPEG-2 video (ISO/IEC 11172-2) 。

## <a name="input-types"></a>輸入類型

此解碼器支援下列輸入媒體類型。

| 屬性                                                 | 描述                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) | **MFMediaType \_ 影片**                                                  |
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ MPEG1**<br/> **MFVideoFormat \_ MPEG2**<br/> |



 

## <a name="output-types"></a>輸出型別

此解碼器支援下列輸出類型。

| 屬性                                                 | 描述                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) | **MFMediaType \_ 影片**                                                                                                                                                         |
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ I420**<br/> **MFVideoFormat \_ IYUV**<br/> **MFVideoFormat \_ NV12**<br/> **MFVideoFormat \_ YUY2**<br/> **MFVideoFormat \_ YV12**<br/> |



 

## <a name="remarks"></a>備註

MPEG-2 影片解碼會公開下列介面：

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

對解碼器的輸入必須是基本資料流程。 支援的最大解析度為1920×1088圖元。

此解碼器支援使用 Microsoft Direct3D 9 或 Microsoft Direct3D 11 (DXVA) 的 DirectX Video 加速。

### <a name="special-decoding-modes"></a>特殊解碼模式

-   **低延遲模式。** 這種模式適用于即時通訊等案例。 它可減少啟動延遲，讓解碼器更快產生第一個輸出範例。 不過，在此模式中，解碼器會緩衝較少的樣本，這可能會導致問題，因為此解碼器不會預先解碼為許多框架。 若要啟用低延遲模式，請設定 [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) 屬性。
-   **尋求。** 如需精確的搜尋，請呼叫 [**IMFTransform：： SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) 方法。 當呼叫這個方法時，此解碼器只會輸出落在呼叫端所指定時間戳記範圍內的框架。
-   **縮圖產生模式**。 此模式適用于快速產生縮圖影像。 在此模式中，解碼器一開始只會解碼 I 個框架。 如果在特定的畫面格數目內找不到 I 框架，則會以固定的間隔開始解碼 P 框架並輸出非 I 框架 (每 *N* 個圖片) 一次，直到達到 I 個框架為止。 若要啟用縮圖產生模式，請設定 [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) 屬性。
-   **訣竅。** 此解碼器可以更快地以速率解碼，而非即時。 在較高的播放速率中，解碼器會切換為僅解碼 I 個畫面格。 若要進行反向播放，只會解碼 I 個框架。

### <a name="codec-properties"></a>編解碼器屬性

此解碼器透過 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法支援下列屬性。



| 屬性                                                                                                      | 描述                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)               | 啟用或停用縮圖產生模式。                                                             |
| [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | 啟用或停用硬體加速解碼。                                                         |
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | 啟用或停用低延遲模式。                                                                      |
| [MFT \_ 解碼 \_ 會 \_ \_ \_ 以 \_ 原生 \_ 順序公開輸出類型](mft-decoder-expose-output-types-in-native-order.md) | 指定此解碼器是否會在其他格式之前公開適用于轉碼的輸出類型。 |



 

在這些屬性中，也可以透過 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面設定下列內容：

-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

### <a name="limitations"></a>限制

-   以 IA-64 為基礎的平臺不支援此解碼器。
-   此解碼器不支援 CSS 解密或播放加密的 Dvd。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                       |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> </dl>

 

 
