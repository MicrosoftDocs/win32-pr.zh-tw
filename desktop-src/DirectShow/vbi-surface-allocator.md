---
description: VBI 介面配置器
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: VBI 介面配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c586c3ef135722ac259813d918dc4054617b8ae6bfb987083f0a2ceaa986067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071982"
---
# <a name="vbi-surface-allocator"></a>VBI 介面配置器

VBI 介面配置器會使用硬體視訊連接埠捕獲案例，控制類比電視圖中 VBI 緩衝區的配置。 使用 Bt829 解碼器這類裝置時，框架緩衝區可能包含多個 VBI capture 緩衝區，而這些緩衝區可透過以一般方式（通常是影片埠）的專屬硬體機制來存取。 VBI 介面配置器篩選器會從 capture 篩選器連線下游，而且沒有輸出 pin。 此篩選器會與覆迭[Mixer](overlay-mixer-filter.md) (透過 DirectDraw) ，以在硬體視訊連接埠上執行協調作業，並利用相同的有限 SVGA 框架緩衝區記憶體。



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

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



