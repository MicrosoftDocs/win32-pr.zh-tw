---
description: 影片混合轉譯器篩選器9
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: 影片混合轉譯器篩選器9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e20418aad6b9648835665fff98f894eeed1386
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986241"
---
# <a name="video-mixing-renderer-filter-9"></a>影片混合轉譯器篩選器9

在 DirectX 9 中，影片混合轉譯器 9 (VMR-9) 篩選器提供 DirectX 支援的所有平臺上的先進影片轉譯功能。 它與 DirectX 9 3D 功能完全整合。 例如，您可以輕鬆地將影片新增至遊戲和其他3D 環境，或使用 Direct3D 圖元著色器和其他效果來轉換影片影像。

此篩選器不支援視訊連接埠。

為了維持回溯相容性，VMR 不是任何系統上的預設轉譯器。 若要使用此篩選，請明確地將它新增至篩選圖形，然後在連接任何輸入圖釘之前加以設定。 VMR-9 使用自己的介面、結構和列舉集合，這些介面與 VMR-7 的對應資料類型不一定相同。

VMR-9 最多支援16個監視器。




| 標籤 | 值 |
|--------|-------|
| 篩選介面 | VMR-9 支援數個不同的轉譯模式。 它支援一組不同的介面，視轉譯模式而定：<br /><ul><li>所有模式： <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>、 <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li><li>Renderless 模式： <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></li><li>視窗模式： <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li><li>無視窗模式： <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li></ul>若要設定轉譯模式，請呼叫 <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9：： SetRenderingMode</strong></a>。 如需詳細資訊，請參閱 <a href="vmr-modes-of-operation.md">VMR 操作模式</a>。<br /> | 
| 輸入 Pin 媒體類型 | 輸入 pin 將會與基礎視頻硬體所支援的任何類型連接。 | 
| 輸入 Pin 介面 | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a> | 
| 輸出 Pin 媒體類型 | 不適用。 | 
| 輸出 Pin 介面 | 不適用。 | 
| 篩選 CLSID | CLSID_VideoMixingRenderer9 | 
| 屬性頁 CLSID | N/A | 
| 可執行檔 | Quartz.dll | 
| <a href="merit.md">優點</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">篩選準則分類</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>備註

應用程式可以提供公開下列介面的自訂配置器展示者物件：

-   [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   [**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (選用) 
-   [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (選用) 
-   [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (選用) 

如需自訂配置器-展示者的詳細資訊，請參閱 [提供 VMR 的自訂 Allocator-Presenter-9](supplying-a-custom-allocator-presenter-for-vmr-9.md)。

應用程式也可以提供公開下列介面的自訂外掛程式組合器：

-   [**IVMRImageCompositor9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

若要使用自訂的組合器來設定 VMR，請呼叫 [**IVMRFilterConfig9：： SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> <dt>

[使用影片混合轉譯器](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




