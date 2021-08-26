---
description: 影片混合轉譯器篩選器7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: 影片混合轉譯器篩選器7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac39dfeab90fe97085c97b3a767f06d348a0f02
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466035"
---
# <a name="video-mixing-renderer-filter-7"></a>影片混合轉譯器篩選器7

本主題適用于 Windows XP 或更新版本。

在 Windows XP 和更新版本中，混合轉譯器 7 (VMR-7) 的影片是預設的影片轉譯器。 這稱為 VMR-7，因為它會在內部使用 DirectDraw 7。 在 DirectX 9 中，您可以在非 XP 系統上轉散發類似但個別的篩選器，也就是 VMR-9。 VMR-9 使用 Direct3D 9。

> [!Note]  
> VMR 可在 Windows XP 及更新版本上取得。 它無法透過 DirectX 可轉散發套件或舊版 Windows 取得。 在大部分的情況下，應用程式應該使用 [影片混合](video-mixing-renderer-filter-9.md)轉譯器9。

 

VMR 的功能包括：

-   真正的 Alpha 混合，最多16個輸入資料流程
-   轉譯之前的合成影像存取
-   可讓協力廠商執行自訂影片效果的外掛程式模型。
-   最多可支援15個監視器。

在 Windows XP 和更新版本的 graph 建立期間，除非應用程式明確建立並新增至圖形，否則篩選 Graph 管理員將不會使用較舊的影片轉譯器或重迭 Mixer 篩選。

如需詳細資訊，請參閱 [使用影片混合](using-the-video-mixing-renderer.md)轉譯器。




| | |篩選介面 |所有模式：<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li></ul>視窗模式：<br /><ul><li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li></ul>無視窗模式：<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li></ul>Renderless 模式：<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li></ul>Mixer 模式：<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li></ul>如需各種 VMR 7 模式的詳細資訊，請參閱 <a href="vmr-modes-of-operation.md">VMR 作業模式</a>。<br /> | |輸入 Pin 媒體類型 |主要類型： MEDIATYPE_VideoSubtype：相依于圖形硬體。 必須是未壓縮的影片。<br /> | |輸入 Pin 介面 | <ul><li><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (請參閱備註) </li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></li></ul> | |輸出釘選媒體類型 |不適用。 | |輸出 Pin 介面 |不適用。 | |篩選 CLSID |有兩個與此篩選準則相關聯的 Clsid：<ul><li>CLSID_VideoMixingRenderer：建立 VMR-7。 如果系統資源不足，無法建立 VMR-7，則對 <strong>CoCreateInstance</strong> 的呼叫會失敗。</li><li>CLSID_VideoRendererDefault：如果有可用的系統資源，則建立 VMR-7，否則會建立舊的 <a href="video-renderer-filter.md">影片</a> 轉譯器篩選器。</li></ul>如果您需要 VMR-7 的特定功能，請使用 CLSID_VideoMixingRenderer。 否則，請使用 CLSID_VideoRendererDefault，這幾乎不會失敗，因為它會切換回舊的影片轉譯器篩選器。<br /> | |屬性頁 CLSID |不適用。 | |可執行檔 |Quartz.dll | | <a href="merit.md">業績</a> |MERIT_PREFERRED + 1 | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>備註

只有當 VMR-7 篩選處於視窗模式時，輸入 pin 才會公開 **IOverlay** 介面。 Pin 所實 **IOverlay** 的唯一方法是 **GetWindowHandle**，這可讓應用程式取得篩選器影片視窗的控制碼。 所有其他 **IOverlay** 方法都會傳回 E \_ >notimpl。 在無視窗模式中，篩選不會建立影片視窗，因此 pin 不會公開介面。

應用程式可以提供公開下列介面的自訂配置器展示者物件：

-   [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   [**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (選用) 
-   [**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (選用) 
-   [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (選用) 

如需自訂配置器-展示者的詳細資訊，請參閱 [為 VMR 提供自訂 Allocator-Presenter-7](supplying-a-custom-allocator-presenter-for-vmr-7.md)。

應用程式也可以提供公開下列介面的自訂外掛程式組合器：

-   [**IVMRImageCompositor**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

若要使用自訂的組合器來設定 VMR，請呼叫 [**IVMRFilterConfig：： SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 




