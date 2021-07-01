---
description: 全螢幕轉譯器篩選
ms.assetid: 59332096-bdfe-4208-b99a-1f434652f287
title: 全螢幕轉譯器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d331ff6f31d1c985c7e255b23381a289931da60
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120473"
---
# <a name="full-screen-renderer-filter"></a>全螢幕轉譯器篩選

全螢幕轉譯器篩選器會在舊版硬體上提供全螢幕的影片呈現。 較新的視訊卡可以有效率地延展影片，而不需要全螢幕轉譯器。 因此，使用此篩選器現在已被取代。

請勿手動將此篩選新增至篩選圖形。 如果應用程式呼叫 [**IVideoWindow：:p 的 \_ FullScreenMode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode)，則篩選圖形管理員會自動針對全螢幕模式選取適當的影片轉譯器。 選取專案對應用程式而言是透明的。 使用目前的視訊卡時，篩選圖形管理員不太可能選取全螢幕轉譯器。



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IFullScreenVideoEx**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-ifullscreenvideoex)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)、 [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) |
| 輸入 Pin 媒體類型                    | 媒體媒體 \_ 、MEDIASUBTYPE \_ Null                                                                                                                                                                                                               |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| 輸出 Pin 媒體類型                   | 不適用                                                                                                                                                                                                                                     |
| 輸出 Pin 介面                    | 不適用                                                                                                                                                                                                                                     |
| 篩選 CLSID                             | CLSID \_ ModexRenderer                                                                                                                                                                                                                               |
| 屬性頁 CLSID                      | CLSID \_ ModexProperties                                                                                                                                                                                                                             |
| 可執行檔                               | quartz.dll                                                                                                                                                                                                                                         |
| [優點](merit.md)                       | 不 \_ 太可能                                                                                                                                                                                                                                    |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>備註

全螢幕轉譯器支援一組靜態的顯示模式。 不過，使用者系統上的視訊卡可能不支援每種模式。 若要判斷卡片是否支援特定模式，請呼叫 [**IFullScreenVideoEx：： IsModeAvailable**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-ismodeavailable) 方法。 您也可以藉由呼叫 [**IFullScreenVideoEx：： SetEnabled**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-setenabled)，以程式設計方式停用特定的顯示模式。 全螢幕轉譯器目前支援下表所示的顯示模式：



| 模式 | 寬度 | 高度 | 位元深度 |
|------|-------|--------|-----------|
| 0    | 320   | 200    | 16        |
| 1    | 320   | 200    | 8         |
| 2    | 320   | 240    | 16        |
| 3    | 320   | 240    | 8         |
| 4    | 640   | 400    | 16        |
| 5    | 640   | 400    | 8         |
| 6    | 640   | 480    | 16        |
| 7    | 640   | 480    | 8         |
| 8    | 800   | 600    | 16        |
| 9    | 800   | 600    | 8         |
| 10   | 1024  | 768    | 16        |
| 11   | 1024  | 768    | 8         |
| 12   | 1152  | 864    | 16        |
| 13   | 1152  | 864    | 8         |
| 14   | 1280  | 1024   | 16        |
| 15   | 1280  | 1024   | 8         |



 

 (所有模式都是 RGB。 ) 這份清單有可能變更。 您可以使用 [**IFullScreenVideoEx：： GetModeInfo**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getmodeinfo) 方法來取得模式的相關資訊。 全螢幕轉譯器一律會選擇可用的最低解析度模式，並受限於稱為「 *剪輯因數*」的屬性，它會決定允許全螢幕轉譯器裁剪的影片數量。 如需詳細資訊，請參閱 [**IFullScreenVideoEx：： GetClipFactor**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getclipfactor)。

當應用程式執行或暫停篩選圖形時，全螢幕轉譯器會切換至所選的顯示模式。 當圖形停止時，全螢幕轉譯器會還原原始的顯示模式。

全螢幕轉譯器只能以前景使用中視窗的形式運作。 如果使用者切換至另一個應用程式，則全螢幕轉譯器會藉由將影片視窗最小化或隱藏來隱藏影片。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



