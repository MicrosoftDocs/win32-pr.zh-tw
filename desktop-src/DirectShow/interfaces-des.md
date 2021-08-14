---
description: DirectShow 編輯服務的介面
ms.assetid: e7fdb387-83b3-4fa2-9608-2f5dc95975bf
title: DirectShow 編輯服務的介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e913ec6bf17a11a4b772d288b9404113cd6bdc70bf441ed20dcbc69a086f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397589"
---
# <a name="interfaces-for-directshow-editing-services"></a>DirectShow 編輯服務的介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

本章節包含[DirectShow 編輯服務](directshow-editing-services.md) (DES) 介面的參考主題。



| 介面                                                  | 描述                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IAMErrorLog**](iamerrorlog.md)                         | 提供錯誤記錄的回呼方法。                                                                                  |
| [**IAMSetErrorLog**](iamseterrorlog.md)                   | 設定或抓取錯誤記錄檔。                                                                                                |
| [**IAMTimeline**](iamtimeline.md)                         | 提供操作時間軸的方法。                                                                                |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | 在組合上插入或抓取虛擬追蹤。                                                                          |
| [**IAMTimelineEffect**](iamtimelineeffect.md)             | 提供操作時間軸效果的方法。                                                                            |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | 提供將效果新增至時間軸物件的方法。                                                                      |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | 設定和抓取群組的屬性。                                                                                       |
| [**IAMTimelineObj**](iamtimelineobj.md)                   | 提供操作時間軸物件的方法。                                                                            |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | 分割時間軸物件。                                                                                                      |
| [**IAMTimelineSrc**](iamtimelinesrc.md)                   | 提供方法來操作和設定來源物件上的屬性。                                                    |
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | 提供操作追蹤物件的方法。                                                                               |
| [**IAMTimelineTrans**](iamtimelinetrans.md)               | 提供處理轉換物件的方法。                                                                          |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | 將轉換新增至物件。                                                                                                 |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | 提供使用虛擬追蹤的方法。                                                                              |
| [**IDxtAlphaSetter**](idxtalphasetter.md)                 | 設定 [Alpha Setter](alpha-setter-effect.md) 效果的屬性。                                                         |
| [**IDxtCompositor**](idxtcompositor.md)                   | 設定 [組合](compositor-transition.md) 器轉換的屬性。                                                     |
| [**IDxtJpeg**](idxtjpeg.md)                               | 設定 [SMPTE](smpte-wipe-transition.md) 抹除轉換的屬性。                                                     |
| [**IDxtKey**](idxtkey.md)                                 | 設定索引 [鍵](key-transition.md) 轉換的屬性。                                                                   |
| [**IFindCompressorCB**](ifindcompressorcb.md)             | 不支援。                                                                                                                 |
| [**IGrfCache**](igrfcache.md)                             | 不支援。                                                                                                                 |
| [**IMediaDet**](imediadet.md)                             | 抓取媒體檔案的相關資訊，例如資料流程的數目以及每個資料流程的類型、持續時間和畫面播放速率。 |
| [**IMediaLocator**](imedialocator.md)                     | 提供驗證檔案名的方法。                                                                                    |
| [**IPropertySetter**](ipropertysetter.md)                 | 設定效果或轉換的屬性。                                                                                    |
| [**IRenderEngine**](irenderengine.md)                     | 從時間軸建立篩選圖形來呈現 DES 專案。                                                          |
| [**IRenderEngine2**](irenderengine2.md)                   | 讓應用程式取代 DES 所使用的預設影片調整大小篩選。                                              |
| [**IResize**](iresize.md)                                 | 任何自訂影片調整器篩選都必須支援。                                                                          |
| [**ISampleGrabber**](isamplegrabber.md)                   | 當個別媒體範例在篩選圖形中移動時，會加以抓取。                                                      |
| [**ISampleGrabberCB**](isamplegrabbercb.md)               | [**ISampleGrabber**](isamplegrabber.md)介面的回呼介面。                                                 |
| [**ISmartRenderEngine**](ismartrenderengine.md)           | 提供支援智慧 recompression 的方法。                                                                             |
| [**IXml2Dex**](ixml2dex.md)                               | 在可延伸標記語言 (XML)  (XML) 中儲存和載入 DES 專案檔。                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow編輯服務 c + + 參考](directshow-editing-services-c---reference.md)
</dt> </dl>

 

 



