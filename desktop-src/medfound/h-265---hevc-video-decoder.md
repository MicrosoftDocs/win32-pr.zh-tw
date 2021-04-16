---
description: 媒體基礎 .H 的視頻編碼程式是一種媒體基礎轉換，支援在附錄 B 格式中解碼 H. 265/HEVC 內容，並可用於播放數量和 .m2ts 檔案。
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: H. 265/HEVC 影片解碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c20a83f82e106bd749deb8bf2350cc9e5a347a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512460"
---
# <a name="h265--hevc-video-decoder"></a>H. 265/HEVC 影片解碼器

媒體基礎 .H 的視頻編碼程式是一種 [媒體基礎轉換](media-foundation-transforms.md) ，支援在附錄 B 格式中解碼 H. 265/HEVC 內容，並可用於播放數量和 .m2ts 檔案。

H. 視頻解碼會公開下列介面。

-   Windows 8) 支援的 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

若要建立 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 或 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數的解碼器實例。

## <a name="input-types"></a>輸入類型

輸入類型必須至少包含下列兩個屬性：



| 屬性                                                 | 描述                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) | **MFMediaType \_ 影片**                                                                        |
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)        | [MFVideoFormat \_HEVC](video-subtype-guids.md) 或 MFVideoFormat \_ HEVC \_ ES |



 

第一個媒體子類型（MFVideoFormat \_ HEVC）指出媒體範例包含具有開始代碼的 h. 位流，且資料流程具有交錯的 SPS/PPS。 它會假設每個樣本都有一個畫面格。

媒體子類型 MFVideoFormat \_ HEVC \_ ES 指出媒體範例包含基本的 h. 位流，其中每個範例可能包含部分圖片、多張圖片、某些圖片，以及部分圖片。

輸入媒體類型無法在兩種類型之間動態變更。 此解碼器可以根據基礎資料流程語法來偵測進行中的輸出格式變更 (外觀比例、維度、交錯旗標、colorimetry 資訊) 和觸發程式對應的輸出媒體類型變更。

針對輸入媒體類型，解碼器預期來源必須設定正確的設定檔。 例如，如果內容即將10位，則輸入媒體類型應將設定檔指定為 Main10。

## <a name="output-types"></a>輸出型別

此解碼器支援下列輸出子類型：

-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ P010**

如需這些子類型的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。

## <a name="transform-attributes"></a>轉換屬性

H. 解碼會實 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。 應用程式可以使用這個方法來取得或設定下列屬性。



| 屬性                                                                                       | 描述                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                     | 啟用或停用低延遲解碼模式。                                                                                |
| [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)                           | 設定用於此解碼器的背景工作執行緒數目。                                                                        |
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) | 啟用或停用縮圖產生模式。                                                                                |
| [已 \_ 設定 MF NALU \_ 長度 \_](mf-nalu-length-set.md)                                                 | 指出 NALU 長度資訊會以 BLOB 的形式傳送，每個壓縮的 h. 範例。                              |
| [MF \_ NALU \_ 長度 \_ 資訊](mf-nalu-length-information.md)                                 | 指出範例中的 NALUs 長度。 這是在壓縮的輸入範例上設定為 .H 解碼的 MF BLOB。 |
| [MF \_ SA \_ 最小 \_ 輸出 \_ 範例 \_ 計數](mf-sa-minimum-output-sample-count.md)                 | 指定輸出樣本的最大數目。                                                                               |



 

H. 265 解碼支援 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面。 此介面提供 alternativate API 來設定下列編解碼器屬性。

-   [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)
-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a>格式條件約束

此解碼器支援下列格式：



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 設定檔/層級    | 主要、主要的圖片和 Main10 設定檔                                                                                                                                                                                                                        |
| 色度格式     | 4:2:0 色度                                                                                                                                                                                                                                                         |
| 最低解析度 | 48×48圖元                                                                                                                                                                                                                                                       |
| 最大解析度 | 4096×2304圖元<br/> DXVA 加速的保證解析度上限為1920×1088圖元;在較高的解析度中，解碼是使用 DXVA 來完成（如果基礎硬體支援的話），否則會使用軟體進行解碼。<br/> |
| DXVA               | 此解碼器支援 DX11 相互作用和 DX12 DXVA，但不支援 DXVA 第2版或 DXVA 第1版。                                                                                                                                                                                                         |



 

輸入資料必須符合 ITU-T H 的附錄 B。 265 \| ISO/IEC 23008-2。 資料必須包含起始碼。 除非在位元組資料流程中找到有效的 sequence 參數集 (SPS) 和圖片參數集 (PPS) ，否則此解碼器會略過位元組。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                |
| DLL<br/>                      | <dl> <dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> </dl>

 

 
