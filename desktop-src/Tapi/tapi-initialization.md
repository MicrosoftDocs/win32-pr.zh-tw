---
description: TAPI 元件的正常運作需要在電腦上設定通訊環境。
ms.assetid: 3df3d974-629e-4d78-b97d-b8121b185309
title: TAPI 初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f9062f8440cdec6597d21a2141a24b12f69bc9e940e189965d9e73880c54c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659898"
---
# <a name="tapi-initialization"></a>TAPI 初始化

TAPI 元件的正常運作需要在電腦上設定通訊環境，如下所示：

-   第一次將軟體或硬體新增至電腦時，會執行[安裝](installation.md)。 詳細的程式取決於作業系統和軟體本身。
-   [主要初始化](primary-initialization.md) 會建立物件和通訊路徑。
-   [版本協商](version-negotiation.md) 可確保 TAPI 元件可以交換資料。
-   [資源清查](resource-inventory.md) 會抓取可供 TAPI 應用程式使用之裝置的相關資訊。
-   [事件通知](event-notification.md) 會指定 TAPI 和服務提供者如何將非同步作業結果和狀態變更資訊傳遞給應用程式。

## <a name="summary-of-related-reference-pages"></a>相關參考頁面的摘要



| TAPI 2.x 函數                                        | 描述                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)     | 設定電話語音環境，傳回應用程式控制碼和裝置計數。                                                   |
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)         | 取得支援的裝置功能，例如 TAPI 版本或媒體類型。                                                          |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) | 取得位址功能，例如是否支援呼叫公園。                                                                |
| [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen)                     | 通知 TAPI 應用程式將會使用這一行，並以何種方式使用。                                                       |
| [**lineGetMessage**](/windows/win32/api/tapi/nf-tapi-linegetmessage)         | 傳回已排入佇列的下一個 TAPI 訊息，以傳遞至使用事件處理常式通知機制的應用程式 |



 



| TAPI 3.x 介面或方法                                                | 描述                                                                                                                                |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI：： Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)                               | 設定電話語音環境。                                                                                                             |
| [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)               | 列舉目前可用的位址。                                                                                                  |
| [**ITTAPI：： get \_ 位址**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses)                        | 建立目前可用的位址集合。 提供給 Automation 用戶端應用程式，例如以 Visual Basic 撰寫的應用程式。 |
| [**ITTAPIEventNotification：： Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)       | 判斷非同步事件通知的回應。 由 TAPI 叫用的應用程式所執行。                                |
| [**ITTAPI：:p 的 \_ >eventfilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)                    | 設定事件篩選器遮罩，以通知 TAPI 應用程式所需的事件。                                                     |
| [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) | 指示 TAPI 針對指定的位址和一組媒體類型傳遞應用程式傳入會話。                                   |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                                      | 允許應用程式探索位址的媒體支援功能。                                                           |



 

 

 
