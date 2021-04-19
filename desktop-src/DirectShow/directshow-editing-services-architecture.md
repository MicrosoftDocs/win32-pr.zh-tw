---
description: DirectShow 編輯服務架構
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: DirectShow 編輯服務架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6059eebe9228e61d3de9677972eedfcb51c62
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973735"
---
# <a name="directshow-editing-services-architecture"></a>DirectShow 編輯服務架構

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

下圖顯示 (DES) 的 [DirectShow 編輯服務](directshow-editing-services.md) 的架構。

![directshow 編輯服務架構](images/architecture.png)

-   時間軸：將影片生產形式表示為來源剪輯、轉換和效果的集合，並組織成一組嵌套的軌跡。 如需詳細資訊，請參閱 [時間軸模型](the-timeline-model.md)。
-   XML 剖析器：剖析時間軸並產生輸出檔，或讀取輸入檔並產生時間軸。 DES 支援以 XML 為基礎的持續性格式。
-   轉譯引擎：將時間軸轉譯成可轉譯為串流媒體的表單。 根據預設，轉譯引擎會產生 DirectShow 篩選圖形 (請參閱下一節) 。
-   媒體定位器：維持媒體元件位置的快取。 當嘗試開啟媒體元件失敗時，DES 會根據成功開啟的歷程記錄，使用快取來尋找元素。

時間軸是影片編輯專案的摘要描述。 它會指定專案中使用的來源剪輯、開始和停止時間、效果和轉換等等。 但是，時間軸不會轉譯影片和音訊串流。 相反地，轉譯引擎會將時間軸轉譯為預覽或檔案輸出的篩選圖形。 應用程式會操控時間軸，而不是直接操作篩選圖形，這會很麻煩且容易出錯。

下表列出一般影片編輯應用程式執行的主要工作，以及支援每項工作的介面。 稍後的章節會更詳細地說明這些工作和介面。



| Task                                     | 介面 (s)                                                                              |
|------------------------------------------|------------------------------------------------------------------------------------------|
| 建立或修改時間軸。          | [**IAMTimeline**](iamtimeline.md) 和其他 **IAMTimelineXXXX** 介面          |
| 儲存並載入專案檔。             | [**IXml2Dex**](ixml2dex.md)                                                             |
| 預覽專案或將其寫入檔案。 | [**IRenderEngine**](irenderengine.md)、 [ **ISmartRenderEngine**](ismartrenderengine.md) |



 

此外，應用程式可能會執行下列部分或所有的次要工作。



| Task                                                                                           | 介面 (s)                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| 取得媒體檔案的相關資訊。  (的資料流程數目;每個資料流程的格式和持續時間。 )  | [**IMediaDet**](imediadet.md)                                               |
| 設定轉換和效果的屬性。                                                     | [**IPropertySetter**](ipropertysetter.md)                                   |
| 在轉譯期間發生錯誤時收到通知。                                       | [**IAMSetErrorLog**](iamseterrorlog.md)、 [ **IAMErrorLog**](iamerrorlog.md) |
| 取出海報畫面。                                                                        | [**IMediaDet**](imediadet.md)、 [ **ISampleGrabber**](isamplegrabber.md)     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow 編輯服務開始使用](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



