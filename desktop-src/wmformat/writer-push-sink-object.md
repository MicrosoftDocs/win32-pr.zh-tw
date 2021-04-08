---
title: 寫入器推送接收物件
description: 寫入器推送接收物件
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- Windows Media Format SDK，寫入器推播接收物件
- Advanced Systems Format (ASF) 、writer push sink 物件
- ASF (Advanced 系統格式) 、寫入器推送接收物件
- 物件、寫入器推送接收物件
- 寫入器推送接收物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19ea9855219dcb4572ef187ad93e03696b88492
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932923"
---
# <a name="writer-push-sink-object"></a>寫入器推送接收物件

寫入器發送接收物件會將數位媒體分配至發行端點。 例如，即時音樂會可以由單一伺服器進行編碼，然後傳遞或 *推送* 至數部其他伺服器，這些伺服器實際上會將內容串流至使用者。

寫入器發送接收物件是由函式 [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)所建立，它會設定 **IWMWriterPushSink** 介面的指標。 下表所列的物件所支援的其他介面，可以藉由呼叫 **QueryInterface** 方法來取得。



| 介面                                          | 描述                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | 讓應用程式從物件取得狀態訊息。                                                  |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | 管理推播散發會話。                                                                             |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | 配置記憶體、判斷接收是否即時運作，以及公開數個回呼函數。 |



 

下列回呼介面可以由應用程式執行，以追蹤寫入器推送接收物件的進度。



| 介面                                      | 描述                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | 必須將狀態資訊傳達給主應用程式時，才需要此資訊。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> <dt>

[**將 ASF 資料傳送至發行端點**](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[**使用寫入器接收器**](working-with-writer-sinks.md)
</dt> </dl>

 

 




