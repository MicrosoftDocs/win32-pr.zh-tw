---
description: 使用 DirectShow EVR 篩選器
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: 使用 DirectShow EVR 篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02568a5ea9cbaa0310409a5a0966a2bea1bbfffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993068"
---
# <a name="using-the-directshow-evr-filter"></a>使用 DirectShow EVR 篩選器

若要建立增強型影片轉譯器 (EVR) 篩選器，請呼叫 **CoCreateInstance**。 CLSID 是 CLSID \_ EnhancedVideoRenderer，定義于 uuid. h 中。 您不必呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 或 [**MFSHUTDOWN**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) 來使用 EVR 篩選器。

如需在 DirectShow 應用程式中使用 EVR 篩選的詳細資訊，請參閱 [directshow 中的音訊/影片播放](../directshow/audio-video-playback-in-directshow.md)。

EVR 篩選準則會以一個輸入的 pin （對應至參考資料流）開始。 若要加入子串流的 pin，請查詢 [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) 介面的篩選準則，然後呼叫 [**IEVRFilterConfig：： SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams)。 連接任何輸入圖釘之前，請先呼叫這個方法。 Pin 0 一律是參考資料流。 請在任何其他 pin 之前連接此 pin，因為參考資料流的格式可能會限制可用的子資料流程格式。

開始圖形之前，請先設定影片裁剪視窗和目的地矩形。 如需詳細資訊，請參閱 [使用影片顯示控制項](using-the-video-display-controls.md)。

不同于 (VMR) 的影片混合轉譯器，EVR 不會有運作模式 (視窗化、無視窗等等) 。 尤其是：

-   EVR 不支援視窗模式。 應用程式必須提供裁剪視窗。
-   EVR 沒有 renderless 模式。 若要取代預設的展示者，請呼叫 [**IMFVideoRenderer：： InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)。
-   EVR 沒有混合模式。 EVR 一律會建立混音器。 如果您有一個輸入資料流程，就不需要呼叫 [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) 來強制 EVR 使用混音器。

## <a name="filter-interfaces"></a>篩選介面

EVR 篩選器會公開下列介面。 其中一些介面記載于 DirectShow SDK 中。 使用 **QueryInterface** 來取得這些介面的指標：

-   [**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow) 
-   [**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow) 
-   [**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow) 
-   [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   [**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow) 
-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow) 
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   **IPersistStream**
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow) 
-   [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow) 
-   **ISpecifyPropertyPages**

## <a name="input-pin-interfaces"></a>輸入 Pin 介面

EVR 篩選器上的輸入圖釘會公開下列介面。 使用 **QueryInterface** 來取得這些介面的指標：

-   [**IEVRVideoStreamControl**](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   [**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow) 
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow) 
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow) 

此外，您可以使用 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面來取出下列介面：

-   [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 播放音訊/影片](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[增強的影片轉譯器](enhanced-video-renderer.md)
</dt> </dl>

 

 
