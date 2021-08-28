---
description: 影片埠管理員
ms.assetid: d70558a5-9820-432a-b4f3-ccf7bb2a34d5
title: 影片埠管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb7a31d21592bd94579ad608fb453e2a2ec0a264d674f807b404a43f2a0bc1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903510"
---
# <a name="video-port-manager"></a>影片埠管理員

影片埠管理員篩選器 (VPM) 可讓影片混合轉譯器篩選器 7 (VMR-7) 使用影片捕獲裝置或使用影片埠的硬體解碼器。 影片埠是圖形晶片的直接硬體連接。 它可讓影片直接傳送到圖形晶片，而不需要經過系統匯流排。

> [!Note]  
> 影片埠管理員與 VMR 9 不相容，因為 VMR-9 不支援影片埠。

 



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IAMVideoDecimationProperties**](/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IKsPropertySet**](ikspropertyset.md)、 [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop)、 [**IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager) |
| 輸入 Pin 媒體類型                    | 媒體媒體 \_ 、MEDIASUBTYPE \_ VPVIDEO 或 MEDIASUBTYPE \_ VPVBI、FORMAT \_ None                                                                                                                                         |
| 輸入 Pin 介面                     | [**IKsPin**](ikspin.md)、 [**IKsPropertySet**](ikspropertyset.md)、 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| 輸出 Pin 媒體類型                   | 媒體媒體 \_ ，格式 \_ VideoInfo2                                                                                                                                                                                 |
| 輸出 Pin 介面                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                     |
| 篩選 CLSID                             | CLSID \_ VideoPortManager                                                                                                                                                                                              |
| [優點](merit.md)                       | 一般的業績 \_                                                                                                                                                                                                        |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                        |



 

## <a name="remarks"></a>備註

影片埠管理員會結合重迭[Mixer 濾波器](overlay-mixer-filter.md)的影片埠功能和[VBI 介面](vbi-surface-allocator.md)配置器的功能。 VPM 會配置影片埠和表面，並從影片埠同步處理資料捕獲。 它允許獨立于轉譯的影片埠型捕捉。 如果需要預覽，VPM 會與 VMR-7 協調以顯示已捕獲的影片埠資料。 當系統上有影片埠時，capture 篩選器需要額外的緩衝區，才能從影片串流中解壓縮 VBI 資料。 這些緩衝區是由 VPM 所提供。 一旦 capture 篩選器解壓縮了 VBI 資料之後，它就會在個別的 pin 上傳遞給像是 CC 解碼器的篩選。 下圖顯示篩選圖形中的 VPM 和其連接。

![影片埠管理員篩選圖形區段](images/vpm.png)

當系統上偵測到影片埠時，DVD Graph Builder 會自動將 VPM 新增至篩選圖形。 新增至圖形後，VPM 會使用由影片混合轉譯器所提供的 DirectDraw 物件來配置兩個或三個表面。 這些表面會從上游捕捉篩選器接收數位化的框架。 當介面中有資料時，為了回應傳送的使用者模式事件通知，VPM 會自動 array.blit 至 VMR 提供的螢幕外介面。

VPM 針對其輸入緩衝區使用多個介面的事實，表示它需要比上一個 DirectShow 視訊連接埠執行更多的 VRAM。 從 VPM 到 VMR-7 的額外 array.blit 需要額外的視訊記憶體頻寬。 由於硬體自動翻轉未再使用，因此理論上可能會捨棄框架，但經驗辨識項建議您不會發生這種情況。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> <dt>

[**IVPManager 介面**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager)
</dt> </dl>

 

 



