---
description: 範例捕獲篩選器可讓您在範例通過篩選圖形時，取得範例。
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: " (Qedit 的範例捕獲篩選) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Sample
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f0b0ddffe2bc769b7c2371ef93091d8c1daf379c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909666"
---
# <a name="sample-grabber-filter"></a>範例捕獲篩選器

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

範例捕獲篩選器可讓您在範例通過篩選圖形時，取得範例。 它是具有一個輸入 pin 和一個輸出 pin 的轉換篩選。 它會以未變更的方式傳遞所有範例，因此您可以將它插入至篩選圖形，而不需要變更資料流程。 然後，您的應用程式可以藉由呼叫 [**ISampleGrabber**](isamplegrabber.md) 介面上的方法，從篩選器中取出個別樣本。

如果您想要在不轉譯資料的情況下取出範例，請將範例抓取器篩選器連接到 [**Null**](null-renderer-filter.md) 轉譯器篩選器。



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [ **ISampleGrabber**](isamplegrabber.md)                                                                       |
| 輸入 pin 媒體類型                    | 任何媒體類型。                                                                                                                                    |
| 輸入 pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| 輸出 pin 媒體類型                   | 任何媒體類型。 符合輸入媒體類型。                                                                                                          |
| 輸出 pin 介面                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| 篩選 CLSID                             | CLSID \_ SampleGrabber                                                                                                                               |
| 屬性頁 CLSID                      | 沒有屬性頁。                                                                                                                                  |
| 可執行檔                               | Qedit.dll                                                                                                                                          |
| [優點](merit.md)                       | \_ \_ 未 \_ 使用的業績                                                                                                                                |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>備註

若要使用此篩選，請將它新增至篩選圖形，並以所需的媒體類型呼叫 [**ISampleGrabber：： SetMediaType**](isamplegrabber-setmediatype.md) 。 這個方法會指定篩選的輸入和輸出連接的媒體類型。 然後將篩選連接到圖形中的其他篩選。

如果您使用值 **TRUE** 來呼叫 [**ISampleGrabber：： SetBufferSamples**](isamplegrabber-setbuffersamples.md) ，則篩選會緩衝處理其所接收的每個範例，然後再將它傳遞給下游。 呼叫 [**ISampleGrabber：： GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) 方法，以取出緩衝區的目前內容。 或者，您可以呼叫 [**ISampleGrabber：： SetCallback**](isamplegrabber-setcallback.md) ，讓篩選器在每次收到範例時叫用回呼函式。

篩選準則的影片格式有下列限制：

-   它不支援由上而下方向 (負面 **biHeight**) 的影片類型。
-   它不支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式結構 (格式類型等於 **format \_ VideoInfo2**) 。
-   它會拒絕表面 stride 不符合影片寬度的任何影片類型。

如此一來，範例抓取程式將無法連線到影片混合轉譯器 (VMR) 適用于某些影片類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Qedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 編輯服務物件](directshow-editing-services-objects.md)
</dt> <dt>

[使用範例捕獲](using-the-sample-grabber.md)
</dt> </dl>

 

 




