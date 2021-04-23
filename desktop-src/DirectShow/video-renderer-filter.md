---
description: 影片轉譯器篩選
ms.assetid: 7719ed9d-e3b9-4c84-b587-4e120b5cabf8
title: 影片轉譯器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca3becb4fbdbb52a9968481aade07d14d963828
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908416"
---
# <a name="video-renderer-filter"></a>影片轉譯器篩選

影片轉譯器篩選器是一種強大的全用途影片轉譯器。

> [!Note]  
> 在 Windows XP 和更新版本上，預設的影片轉譯 [器是影片混合轉譯器篩選器 7](video-mixing-renderer-filter-7.md) (VMR-7) 。 VMR-7 和影片轉譯器都具有易記名稱「影片轉譯器」。 在舊版平臺上，影片轉譯器是預設轉譯器。 請參閱 [選擇正確的](choosing-the-right-renderer.md)轉譯器。

 

影片轉譯器會使用 DirectDraw 和重迭表面（如果視訊卡支援的話）。 篩選圖形管理員會公開 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面，此介面可讓應用程式設定和取出影片轉譯器上的屬性。 使用較新的視訊卡時，影片轉譯器支援全螢幕呈現。 否則，篩選圖形管理員會自動切換為全螢幕模式的 [全螢幕](full-screen-renderer-filter.md) 轉譯器篩選。 如需詳細資訊，請參閱 [**IVideoWindow：:p 的 \_ FullScreenMode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode) 。

-   \[!重要\]  
    > 一般來說，此篩選器的影片視窗會處理篩選圖形管理員所建立之工作者執行緒上的訊息。 但是，如果應用程式使用 **CoCreateInstance** 直接建立篩選器，則影片視窗會處理應用程式執行緒上的訊息。 在此情況下，應用程式執行緒必須有訊息迴圈，才能將訊息分派至影片視窗。 此外，在對影片轉譯器的最終 **發行** 呼叫（當篩選圖形管理員關閉時，就會發生這種情況），執行緒就不能結束。 否則，應用程式可能會鎖死。

     



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)、 [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2)、 [**IDirectDrawVideo**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo)、 [**IKsPropertySet**](ikspropertyset.md)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)、 [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop)、 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) |
| 輸入 Pin 媒體類型                    | 未壓縮的影片格式。                                                                                                                                                                                                                                                                                                                                                                              |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                           |
| 輸出 Pin 媒體類型                   | 不適用。                                                                                                                                                                                                                                                                                                                                                                                          |
| 輸出 Pin 介面                    | 不適用。                                                                                                                                                                                                                                                                                                                                                                                          |
| 篩選 CLSID                             | CLSID \_ VideoRenderer                                                                                                                                                                                                                                                                                                                                                                                     |
| 屬性頁 CLSID                      | 沒有屬性頁。                                                                                                                                                                                                                                                                                                                                                                                        |
| 可執行檔                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                                               |
| [優點](merit.md)                       | Windows XP 和更新版本：不 **\_ 太可能**                                                                                                                                                                                                                                                                                                                                                                |
| [篩選準則分類](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>備註

在 Quartz.dll 的偵錯工具版本中，如果記錄 \_ 追蹤調試層級設定為5或更高，則影片轉譯器會在影片視窗上顯示每個畫面格的時間戳記。 這些數位不會出現在 DLL 的零售版本中。 如需詳細資訊，請參閱 [Debug Output 函數](debug-output-functions.md)。

下列備註適用于篩選器開發人員：

如果影片圖形配接器支援 YUV 重迭表面，則影片轉譯器會接受 YUV 格式。 不過，當它第一次連線到上游篩選器時，影片轉譯器需要的 RGB 格式必須符合目前監視器設定的色彩深度。 例如，如果目前的顯示設定是24位色彩，上游篩選器必須能夠提供24位 RGB 影片。 當篩選圖形切換為「已在使用」狀態時，影片轉譯器會將動態格式變更協商至適當的 YUV 色彩空間。

藉由連接 RGB 型別，影片轉譯器可確保它在無法使用的情況下，可以使用 GDI。 如果有其他應用程式正在使用視訊記憶體，則會切換為 GDI; 如果影片矩形跨越多重監視器系統上的兩個監視器，或影片矩形完全被另一個視窗遮蔽，則會切換至 GDI。

> [!Note]  
> 影片混合轉譯器不會執行這種類型的動態格式變更，而且不需要 RGB 媒體類型，因為它永遠不會使用 GDI 來呈現。

 

為了協調格式變更，影片轉譯器會以新的媒體類型呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 。 如果上游篩選傳回 S \_ OK，則影片轉譯器會將新媒體附加至下一個範例。 上游篩選應針對每個範例呼叫 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) 。 如果 **GetMediaType** 傳回非 **Null** 值，則表示格式變更，而上游篩選器應藉由切換輸出類型來回應。  (不會在 **QueryAccept** 方法中切換類型。 ) 上游篩選器應該至少接受主要 RGB 型別，而且在理想情況下應該支援通用 YUV 類型。 在串流處理期間，影片轉譯器可能會在 YUV 和 RGB 類型之間來回切換。 影片轉譯器不接受上游篩選所起始的動態格式變更。

當影片轉譯器繪製至 DirectDraw 重迭介面時，它會為其輸入的 pin 配置單一緩衝區。 如果上游篩選嘗試使用多個緩衝區來強制連接，則影片轉譯器將無法使用覆迭表面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



