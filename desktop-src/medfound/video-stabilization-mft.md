---
description: 影片穩定的 MFT 是在影片串流上執行影像穩定的 Microsoft 媒體基礎轉換 (MFT) 。
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: '影片防震 MFT (Camerauicontrol) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65eb64b05e41842b1f7b3ad2e49a6c064be08f0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999505"
---
# <a name="video-stabilization-mft"></a>影片防震 MFT

影片穩定的 MFT 是在影片串流上執行影像穩定的 Microsoft 媒體基礎轉換 (MFT) 。

## <a name="clsid"></a>CLSID

CLSID \_ CMSVideoDSPMFT

## <a name="interfaces"></a>介面

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMediaExtension**](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a>輸入格式

影片穩定 MFT 針對未壓縮影片所接受的輸入媒體類型和子類型組合如下：

-   **媒體 \_ 媒體**
-   **MEDIASUBTYPE \_ NV12**
-   **MEDIASUBTYPE \_ YUY2**

## <a name="output-formats"></a>輸出格式

影片穩定 MFT 接受的輸出媒體類型和子類型組合如下：

-   **媒體 \_ 媒體**
-   **MEDIASUBTYPE \_ NV12**

輸入媒體類型必須在輸出媒體類型之前設定。 在大多數情況下，有限的格式支援不會造成問題，因為管線會自動插入必要的色彩轉換。

影片穩定的 MFT 元件能夠在輸入變更時進行動態格式變更。 當輸入圖片大小變更或子類型變更時，它會觸發輸出資料流程的動態格式變更。

影片穩定的 MFT 在下列情況下將會進行色彩轉換：

-   當輸入格式為 **MEDIASUBTYPE \_ YUY2** 時。
-   使用 Microsoft DirectX 9.0 相容性模式時。

### <a name="attributes"></a>屬性

影片穩定 MFT 透過 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面支援下列屬性。

-   屬性 [MF \_ VIDEODSP \_ 模式](mf-videodsp-mode.md) 會將影片穩定的 MFT 置於穩定模式或通過模式。 應用程式應該針對 GUID **MF \_ VIDEODSP \_ 類型** 呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) ，並使用對應到下列其中一個有效值的整數： **MFVideoDSPMode \_ 穩定化**= 4， **MFVideoDSPMode \_ 傳遞**= 1。 您 \_ \_ 可以在播放期間隨時變更 MF VIDEODSP 模式。 這會導致動態模式變更。 輸出會切換至穩定或在16或2個框架之後傳遞 (，視延遲模式在屬性變更之後) 而定。
-   [ [MF \_ 低 \_ 延遲](mf-low-latency.md) ] 屬性可將影片穩定的 MFT 置於低延遲模式或高品質模式。 應用程式應該針對 GUID **MF \_ 低 \_ 延遲**，以對應到下列其中一個有效值的整數來呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) ：低延遲 = 1 高品質 = 0
-   管線使用屬性 [MF \_ SA \_ D3D11 \_ BINDFLAGS](mf-sa-d3d11-bindflags.md) 來指定 D3D11 系結旗標，以使用建立輸出範例。 D3D11 系結 [**\_ \_ 旗**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) 標列舉中值的任何組合都是有效的。
-   管線會使用屬性 **MF \_ SA 的 \_ 最小 \_ 輸出 \_ 範例 \_ 計數** ，來指定此元件在輸出時必須支援的樣本數目下限。
-   每個由穩定產生的範例都會設定屬性 [MFSampleExtension \_ VideoDSPMode](mfsampleextension-videodspmode.md) ，以指出套用至該範例的有效 [MF \_ VIDEODSP \_ 模式](mf-videodsp-mode.md) ， (範例是否穩定) 。 在某些情況下， (可能因為系統負載過高或使用者) 的要求，而無法穩定。 這個屬性的值與 MF \_ VIDEODSP 模式屬性的值相同 \_ (**MFVideoDSPMode \_ 穩定** 和 **MFVideoDSPMode \_ 傳遞**) 。 若要取得這個屬性的值，應用程式應該在 GUID **MFSampleExtension \_ VideoDSPMode** 上呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) 。

## <a name="remarks"></a>備註

您可以使用下列其中一種方式來建立影片穩定 DSP 的實例：

-   藉由呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)。 影片穩定的 DSP 會在 [ **MFT \_ 類別] \_ 影片 \_ 效果** 類別下註冊。
-   藉由呼叫 COM 函式， **CoCreateInstance** 將 clsid **clsid \_ CMSVideoDSPMFT** 傳遞給它。 若要使用這個方法，您必須包含 wmcodecdsp 和 wmcodecdspuuid 的連結。

此外，video 穩定的 DSP 支援使用 Windows 執行階段作為 Windows Media 擴充功能來進行具現化。 它是在 [**VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)上定義，其完整名稱是 "VideoEffects. VideoStabilization"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Camerauicontrol。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數位訊號處理器](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
