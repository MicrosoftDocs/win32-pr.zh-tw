---
description: VBI 介面配置器
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: VBI 介面配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5849b23b8f21a7b49e477060386628ba4c19b2e5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909006"
---
# <a name="vbi-surface-allocator"></a>VBI 介面配置器

VBI 介面配置器會使用硬體視訊連接埠捕獲案例，控制類比電視圖中 VBI 緩衝區的配置。 使用 Bt829 解碼器這類裝置時，框架緩衝區可能包含多個 VBI capture 緩衝區，而這些緩衝區可透過以一般方式（通常是影片埠）的專屬硬體機制來存取。 VBI 介面配置器篩選器會從 capture 篩選器連線下游，而且沒有輸出 pin。 此篩選器會與重迭 [混音](overlay-mixer-filter.md) 器 (緊密配合，透過 DirectDraw) 在硬體視訊連接埠上執行協調作業，並利用相同的有限 SVGA 框架緩衝區記憶體。



| 標籤 | 值 |
|------------------------------------------|-------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| 輸入 Pin 媒體類型                    | 媒體媒體 \_ 、MEDIASUBTYPE \_ VPVBI                                               |
| 輸入 Pin 介面                     | [**IKsPropertySet**](ikspropertyset.md)                                            |
| 輸出 Pin 媒體類型                   | 媒體 \_ 值 Null、MEDIASUBTYPE \_ Null。  (沒有任何東西連接到輸出釘選。 )  |
| 輸出 Pin 介面                    | 不適用。                                                                     |
| 篩選 CLSID                             | CLSID \_ VBISurfaces                                                                  |
| 屬性頁 CLSID                      | 沒有屬性頁。                                                                   |
| 可執行檔                               | vbisurf.ax                                                                          |
| [優點](merit.md)                       | 一般的業績 \_                                                                       |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



