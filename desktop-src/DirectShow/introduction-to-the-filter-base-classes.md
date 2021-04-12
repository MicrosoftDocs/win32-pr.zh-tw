---
description: 篩選基礎類別簡介
ms.assetid: db6324d7-1914-44a8-a202-dff752b61c1a
title: 篩選基礎類別簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44c104d8fe155a7c9f0edba72770a508c8ec43d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385509"
---
# <a name="introduction-to-the-filter-base-classes"></a>篩選基礎類別簡介

本文說明 Microsoft 的 DirectShow 基礎類別庫。 此程式庫適用于篩選開發人員，但應用程式寫入器可能會發現某些協助程式類別和偵測公用程式很有用。 但是，不需要基底類別庫來進行 DirectShow 程式設計。

下列各節摘要說明程式庫中最重要的基類。

**COM 物件類別**

下列類別支援 COM 物件的建立：



| 類別                              | 描述                            |
|------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject.md) | 基底物件類別。                     |
| [**CUnknown**](cunknown.md)       | 實行 **IUnknown** 介面。 |



 

大部分的 DirectShow 類別都是衍生自 **CBaseObject**。 這個類別會在執行時間保留 DLL 中所有使用中物件的計數，以提供偵錯工具的協助。 在偵錯工具組建中，如果物件計數大於零，則 DLL 會判斷提示是否已卸載。 這可讓您更輕鬆地追蹤參考計數問題所造成的流失問題。

所有支援 COM 介面的基類都衍生自 **CUnknown**，它會繼承 **CBaseObject**。 **CUnknown** 類別支援參考計數、 **QueryInterface** 和匯總。 如需詳細資訊，請參閱 [如何執行 IUnknown](how-to-implement-iunknown.md)。

**篩選和釘選類別**

下列類別支援建立 DirectShow 篩選器和釘選物件：



| 類別                                    | 描述                                                                                                                                                     |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBaseFilter**](cbasefilter.md)       | 篩選準則的基類。 實行 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面。                                                                            |
| [**CBasePin**](cbasepin.md)             | 圖釘的基類。 實行 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 和 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) 介面。                                             |
| [**CBaseInputPin**](cbaseinputpin.md)   | 使用本機記憶體傳輸的輸入針腳的基類。 實行 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面。 這個類別衍生自 **CBasePin**。 |
| [**CBaseOutputPin**](cbaseoutputpin.md) | 使用 **IMemInputPin** 連接之輸出圖釘的基類。 這個類別衍生自 **CBasePin**。                                                         |



 

下列類別適用于建立更特製化的篩選類型：



| 類別                                                  | 描述                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CSource**](csource.md)                             | 來源篩選準則的基類。 這個類別是專為建立推播來源所設計。 它不適合提取來源，例如檔案讀取器。 若要建立此類別的輸出針腳，請使用 [**CSourceStream**](csourcestream.md) 類別。                                                                   |
| [**CTransformFilter**](ctransformfilter.md)           | 轉換篩選準則的基類。 此類別會在資料上執行複製。 此類別的釘選為 [**CTransformInputPin**](ctransforminputpin.md) 和 [**CTransformOutputPin**](ctransformoutputpin.md)。                                                                                            |
| [**CTransInPlaceFilter**](ctransinplacefilter.md)     | 不復制資料之轉換篩選準則的基類。 此類別會直接在輸入資料上執行資料處理，再將其傳遞至下游。 此類別的釘選為 [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) 和 [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)。 |
| [**CVideoTransformFilter**](cvideotransformfilter.md) | 影片轉換篩選準則的基類。 這個類別衍生自 **CTransformFilter** ，並加入品質控制的支援。                                                                                                                                                                                |
| [**CBaseRenderer**](cbaserenderer.md)                 | 轉譯器篩選的基類。 此類別的輸入 pin 碼為 [**CRendererInputPin**](crendererinputpin.md)。                                                                                                                                                                                          |
| [**CBaseVideoRenderer**](cbasevideorenderer.md)       | 影片轉譯器的基類。 這個類別衍生自 **CBaseRenderer**。                                                                                                                                                                                                                                |



 

若要使用這些類別，您必須衍生自己的類別，並撰寫程式碼以支援您篩選準則的特定功能。 基類越特製化，您需要在衍生類別中撰寫的程式碼就越少。

**Helper 物件**

下列類別會執行篩選器和釘選所使用的協助程式物件。 您可以使用這些類別，而不需要從這些類別衍生新的類別：



| 類別                                              | 描述                                                                                                                                                        |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CPullPin**](cpullpin.md)                       | 剖析器篩選器上輸入 pin 的 Helper 物件。 支援使用提取來源的 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 連接。                                       |
| [**COutputQueue**](coutputqueue.md)               | 輸出圖釘的 Helper 物件，可在背景工作執行緒上將傳遞範例排入佇列。                                                                                  |
| [**CSourceSeeking**](csourceseeking.md)           | 用來在來源篩選器上執行搜尋的說明物件，只需一個輸出圖釘。  (此類別不是針對具有多個 pin 的篩選而設計，例如剖析器。 )  |
| [**CEnumPins**](cenumpins.md)                     | 列舉篩選上的釘選的列舉值物件。 實行 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面。                                                       |
| [**CEnumMediaTypes**](cenummediatypes.md)         | 列舉 pin 上慣用媒體類型的列舉值物件。 實行 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面。                             |
| [**CMemAllocator**](cmemallocator.md)             | 記憶體配置器物件。 實行 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面。                                                                          |
| [**CMediaSample**](cmediasample.md)               | 媒體範例物件。 實行 [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) 介面。                                                                              |
| [**CBaseReferenceClock**](cbasereferenceclock.md) | 參考時鐘的基類。 實行 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) 介面。                                                              |
| [**CMediaType**](cmediatype.md)                   | 用於操作 [**\_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的 Helper 物件。                                                                                |



 

 

 



