---
description: 媒體會話事件
ms.assetid: 882a01f2-8f5c-4640-a8ac-f4f5860d7ed1
title: 媒體會話事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e128fc5e11f70fe47d02356ce44629b98bfdfe
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982146"
---
# <a name="media-session-events"></a>媒體會話事件

大部分媒體會話的作業都會以非同步方式執行，因此應用程式必須使用媒體會話的 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面來接聽事件。  ([**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) 介面會繼承 **IMFMediaEventGenerator**。 ) 確切的事件順序將取決於您的應用程式，但是媒體會話幾乎會在任何情況下引發下列事件。



| 事件                                                                  | 描述                                                                                                                                                                                                                    |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEEndOfPresentation](meendofpresentation.md)                         | 當媒體來源完成簡報時引發。 現在資料可能仍在管線中移動。                                                                                                     |
| [MEError](meerror.md)                                                 | 在串流期間發生錯誤時引發。                                                                                                                                                                                    |
| [MESessionClosed](mesessionclosed.md)                                 | 當 [**Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) 方法完成時引發。 此事件是媒體會話佇列的最後一個事件。 當您收到此事件之後，就可以安全地關閉您所建立的任何媒體來源。 |
| [MESessionEnded](mesessionended.md)                                   | 當最後一個簡報完成媒體會話時引發。                                                                                                                                                              |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) | 當新的簡報開始時，會通知應用程式呈現時間。                                                                                                                                        |
| [MESessionStarted](mesessionstarted.md)                               | [**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)方法完成時引發。 除非發生錯誤，否則資料會在此時間點透過管線移動。                                                                          |
| [MESessionTopologySet](mesessiontopologyset.md)                       | [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)方法完成時引發。 除非發生錯誤，否則應用程式不需要採取任何動作。                                                                 |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                 | 在拓撲的狀態變更時，于不同的時間引發。                                                                                                                                                                 |



 

[**IMFMediaSession：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)方法不會引發事件。 **Shutdown** 方法是同步的。 在這個方法傳回之後，就可以安全地釋放您的事件回呼指標。

除了來自媒體會話的事件之外，應用程式可能會從拓撲中的媒體接收器接收事件。 這些可以是媒體接收所定義的自訂事件，可能包含任意資料。 例如，接收可能會從來源資料衍生事件資料，而該資料可能來自不受信任的外部來源。 應用程式應該忽略無法辨識的任何事件，並在剖析事件資料時特別小心。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體會話](media-session.md)
</dt> </dl>

 

 



