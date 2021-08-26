---
title: 事件
description: 如果託管服務具有 evented 狀態變數，則必須執行 IUPnPEventSource 介面。
ms.assetid: 7558496d-c909-4602-bfaa-d21108392fed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313f979072a447f41b9edadfeec7bf4407463be67c86e9c3b34f43f4dcc47874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008078"
---
# <a name="eventing"></a>事件

如果託管服務具有 evented 狀態變數，則必須執行 [**IUPnPEventSource**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource) 介面。 這個介面有兩種方法： [ [**建議**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) ] 和 [ [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise)]。 此介面提供一種機制，讓裝置主機訂閱託管服務所產生的事件通知。 一次只會註冊一個以上的事件接收器。

託管服務必須藉由保留 [**IUPnPEventSink**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink)介面（以參數形式傳遞）的參考，來執行 [**建議**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise)方法。 如果找到介面， **建議** 方法會保存該介面的參考，直到叫用 [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) 或移除託管服務物件為止。 **建議** 只呼叫一次。

若要移除訂用帳戶，裝置主機會叫用 [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) ，並在呼叫「 [**建議**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise)」時，于所使用的物件指標中傳遞。 如果指標與傳遞給 **建議** 的指標相同，則會移除訂用帳戶。

當狀態變數的值變更時，託管服務必須通知事件已發生。 這些服務會藉由叫用 [**IUPnPEventSink：： OnStateChanged**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsink-onstatechanged) 方法來執行此動作。

當裝置主機不再需要從託管服務接收通知時，它會叫用 [**IUPnPEventSource：： Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise)，並傳入從「 [**建議**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise)」接收的相同物件指標。 裝置主機不再位於網路時，會叫用此方法。

 

 




