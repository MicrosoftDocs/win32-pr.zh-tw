---
description: DirectShow基類參考
ms.assetid: 56f3685f-3df8-4358-b04e-3efc04b58008
title: DirectShow基類參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950a4eff89e235194be974256492bd23701f69e5f64181a2e805cf67c1fd62f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663045"
---
# <a name="directshow-base-class-reference"></a>DirectShow基類參考

本節包含所有 Microsoft [DirectShow 基類](directshow-base-classes.md)、其資料成員及其函數的參考專案。



| 類別                                                                  | 描述                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**CAggDirectDraw**](caggdirectdraw.md)                               | 已取代。                                                                                                                       |
| [**CAggDrawSurface**](caggdrawsurface.md)                             | 已取代。                                                                                                                       |
| [**CAMEvent**](camevent.md)                                           | 手動和自動重設事件的包裝函式類別。                                                                                  |
| [**CAMMsgEvent**](cammsgevent.md)                                     | 執行訊息處理之事件物件的包裝函式類別。                                                                  |
| [**CAMSchedule**](camschedule.md)                                     | 參考時鐘的排程器。                                                                                                   |
| [**CAMThread**](camthread.md)                                         | 管理工作者執行緒的低音類別。                                                                                           |
| [**CAutoLock**](cautolock.md)                                         | 保存區塊範圍的重要區段。                                                                                |
| [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md) | 取得和釋放 [**CDynamicOutputPin**](cdynamicoutputpin.md) 物件的存取權。                                           |
| [**CBaseAllocator**](cbaseallocator.md)                               | 配置器的低音類別。                                                                                                        |
| [**CBaseBasicVideo**](cbasebasicvideo.md)                             | 處理 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面的 IDispatch 元件。                                              |
| [**CBaseControlVideo**](cbasecontrolvideo.md)                         | 實作為一般影片視窗的 IBasicVideo 介面。                                                                  |
| [**CBaseControlWindow**](cbasecontrolwindow.md)                       | 實行 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面。                                                                    |
| [**CBaseDispatch**](cbasedispatch.md)                                 | 用來執行 IDispatch 介面的基類。                                                                              |
| [**CBaseFilter**](cbasefilter.md)                                     | 篩選準則的基類。                                                                                                           |
| [**CBaseInputPin**](cbaseinputpin.md)                                 | 輸入圖釘的基類。                                                                                                        |
| [**CBaseList**](cbaselist.md)                                         | 泛型清單的基類。                                                                                                     |
| [**CBaseMediaFilter**](cbasemediafilter.md)                           | 實行 [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) 介面。                                                                    |
| [**CBaseObject**](cbaseobject.md)                                     | 用來執行 DirectShow 物件的基類。                                                                                   |
| [**CBaseOutputPin**](cbaseoutputpin.md)                               | 輸出圖釘的基類。                                                                                                       |
| [**CBasePin**](cbasepin.md)                                           | 圖釘的基類。                                                                                                              |
| [**CBasePropertyPage**](cbasepropertypage.md)                         | 用來執行屬性頁的基類。                                                                                       |
| [**CBaseReferenceClock**](cbasereferenceclock.md)                     | 實行參考時鐘。                                                                                                     |
| [**CBaseRenderer**](cbaserenderer.md)                                 | 用來執行轉譯器篩選準則的基類。                                                                                     |
| [**CBaseStreamControl**](cbasestreamcontrol.md)                       | 實行 [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) 介面。                                                            |
| [**CBaseVideoRenderer**](cbasevideorenderer.md)                       | 影片轉譯器的基類。                                                                                                   |
| [**CBaseVideoWindow**](cbasevideowindow.md)                           | 處理 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面的 IDispatch 元件。                                            |
| [**CBaseWindow**](cbasewindow.md)                                     | 用於管理 windows 的基類。                                                                                                  |
| [**CBasicAudio**](cbasicaudio.md)                                     | 處理 [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) 介面的 IDispatch 介面元件。                                    |
| [**CCmdQueue**](ccmdqueue.md)                                         | 用來執行 [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) 介面的 Helper 類別。                                               |
| [**CCritSec**](ccritsec.md)                                           | 提供執行緒鎖定。                                                                                                           |
| [**CDeferredCommand**](cdeferredcommand.md)                           | 實行 [**IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) 介面。                                                            |
| [**CDispParams**](cdispparams.md)                                     | DISPPARAMS 結構的包裝函式類別。                                                                                       |
| [**CDrawImage**](cdrawimage.md)                                       | 用來繪製至視窗的 Helper 類別。                                                                                             |
| [**CDynamicOutputPin**](cdynamicoutputpin.md)                         | 支援 dyanamic 重新連接和格式變更的輸出 pin。                                                               |
| [**CEnumMediaTypes**](cenummediatypes.md)                             | 慣用媒體類型的列舉值。                                                                                             |
| [**CEnumPins**](cenumpins.md)                                         | 圖釘的列舉值。                                                                                                              |
| [**CFactoryTemplate**](cfactorytemplate.md)                           | 提供 class factory 資訊的類別。                                                                              |
| [**CGenericList**](cgenericlist.md)                                   | 可執行特定類型清單的類別範本。                                                                              |
| [**CImageAllocator**](cimageallocator.md)                             | DIB 區段的配置器。                                                                                                       |
| [**CImageDisplay**](cimagedisplay.md)                                 | 管理影像顯示格式的 Helper 類別。                                                                                  |
| [**CImagePalette**](cimagepalette.md)                                 | 用於管理調色板的 Helper 類別。                                                                                               |
| [**CImageSample**](cimagesample.md)                                   | 使用 DIB 區段的媒體範例。                                                                                              |
| [**CLoadDirectDraw**](cloaddirectdraw.md)                             | 已取代。                                                                                                                       |
| [**CMediaControl**](cmediacontrol.md)                                 | 處理 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 介面的 IDispatch 方法。                                            |
| [**CMediaEvent**](cmediaevent.md)                                     | 處理 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) 介面的 IDispatch 方法。                                                |
| [**CMediaPosition**](cmediaposition.md)                               | 處理 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 介面的 IDispatch 方法。                                          |
| [**CMediaSample**](cmediasample.md)                                   | 媒體範例。                                                                                                                     |
| [**CMediaType**](cmediatype.md)                                       | 用於管理媒體類型的類別。                                                                                                   |
| [**CMemAllocator**](cmemallocator.md)                                 | 記憶體配置器。                                                                                                                 |
| [**CMsg**](cmsg.md)                                                   | 用來管理對 [**CMsgThread**](cmsgthread.md) 物件提出之要求的 Helper 類別。                                             |
| [**CMsgThread**](cmsgthread.md)                                       | 將要求排入佇列執行緒以進行非同步完成的背景工作執行緒。                                             |
| [**COARefTime**](coareftime.md)                                       | 轉換秒和 100-毫微秒單位之間的參考時間。                                                                |
| [**COutputQueue**](coutputqueue.md)                                   | 物件，此物件會將媒體範例排到傳遞的佇列。                                                                                    |
| [**CPersistStream**](cpersiststream.md)                               | 用來執行 IPersistStream 介面的基類。                                                                         |
| [**CPosPassThru**](cpospassthru.md)                                   | 使用一個輸入圖釘來處理篩選的搜尋命令。                                                                             |
| [**CPullPin**](cpullpin.md)                                           | Helper 類別，可從支援 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面的輸出釘選資料。                 |
| [**CQueue**](cqueue.md)                                               | 實作為靜態大小的簡單佇列的類別範本。                                                                  |
| [**CRefTime**](creftime.md)                                           | 管理參考時間的 Helper 類別。                                                                                           |
| [**CRenderedInputPin**](crenderedinputpin.md)                         | 支援多個輸入之轉譯器篩選的輸入 pin。                                                                      |
| [**CRendererInputPin**](crendererinputpin.md)                         | [**CBaseRenderer**](cbaserenderer.md)類別的輸入 pin。                                                                   |
| [**CRendererPosPassThru**](crendererpospassthru.md)                   | 處理轉譯器篩選的搜尋命令。                                                                                       |
| [**CSeekingPassThru**](cseekingpassthru.md)                           | Helper 物件，可建立 [**CPosPassThru**](cpospassthru.md) 和 [**CRendererPosPassThru**](crendererpospassthru.md) 物件。 |
| [**CSource**](csource.md)                                             | 用於實作為來源篩選準則的基類。                                                                                       |
| [**CSourcePosition**](csourceposition.md)                             | 用來執行 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 介面的抽象類別。 已過時。                                 |
| [**CSourceSeeking**](csourceseeking.md)                               | 抽象類別，可在來源篩選準則中使用一個輸出圖釘來執行搜尋。                                                    |
| [**CSourceStream**](csourcestream.md)                                 | [**CSource**](csource.md)類別的輸出 pin。                                                                              |
| [**CSystemClock**](csystemclock.md)                                   | 系統時鐘。                                                                                                                     |
| [**CTransformFilter**](ctransformfilter.md)                           | 用來執行轉換篩選準則的基類。                                                                                    |
| [**CTransformInputPin**](ctransforminputpin.md)                       | CTransformFilter 類別所使用的輸入 pin。                                                                                     |
| [**CTransformOutputPin**](ctransformoutputpin.md)                     | CTransformFilter 類別所使用的輸出 pin。                                                                                    |
| [**CTransInPlaceFilter**](ctransinplacefilter.md)                     | 用於執行不復制資料之轉換篩選準則的類別。                                                                   |
| [**CTransInPlaceInputPin**](ctransinplaceinputpin.md)                 | CTransInPlaceFilter 類別的輸入 pin。                                                                                      |
| [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)               | CTransInPlaceFilter 類別的輸出 pin。                                                                                     |
| [**CUnknown**](cunknown.md)                                           | 實行 IUnknown 介面。                                                                                                |
| [**CVideoTransformFilter**](cvideotransformfilter.md)                 | 影片轉換篩選準則的基類。                                                                                           |
| [**FOURCCMap**](fourccmap.md)                                         | 在 Guid 與 FOURCCs 之間轉換的 Helper 類別。                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow基類](directshow-base-classes.md)
</dt> </dl>

 

 



