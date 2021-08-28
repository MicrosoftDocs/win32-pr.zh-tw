---
description: 串流路由是媒體應用程式在裝置之間切換串流的能力，而不會中斷播放或捕捉會話。
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: 串流路由
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e76944954c969ce458175585076d23ce015ea573a86e3f89dbbcd296aff444
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018226"
---
# <a name="stream-routing"></a>串流路由

*串流路由* 是媒體應用程式在裝置之間切換串流的能力，而不會中斷播放或捕捉會話。

電腦可以有多個轉譯和捕獲裝置。 系統會 **在 [音效** ] 控制台上列出這些裝置。 從這份清單中，使用者可以將裝置設定為每個角色的預設裝置：播放、錄製或四個通訊角色 (主控台轉譯、主控台抓取、通訊轉譯或通訊捕捉) 。 裝置清單可以動態修改，因為有些裝置可以暫時使用，例如 USB 耳機。 當有多個裝置可用時，使用者可以將預設值變更為不同的裝置。 使用者也可以變更裝置的格式 (取樣率、每個樣本的位數，以及在裝置屬性的 [ **Advanced** ] 索引標籤上) 。

試想一個案例，讓使用者選取 **喇叭** 作為轉譯音訊串流的預設裝置。 使用者接著連接 USB 耳機、選取耳機作為新的預設裝置，並將裝置的取樣率從 44.1 kHz 變更為 48 kHz。 使用者想要以新的取樣率在耳機播放音訊串流，最短的串流會話中斷。

在此案例中，媒體應用程式必須處理的案例有兩種：

-   串流必須傳送至新的預設裝置，並在最短的播放中中斷。
-   新的裝置必須以新的格式繼續播放 (也就是，使用者可以) 的取樣率變更。

在 Windows Vista 中，為了支援此案例，媒體應用程式必須提供資料流程路由的執行。 應用程式負責終止現有的資料流程，並在新的裝置上重新開機串流。 如果使用者變更預設裝置或其混合格式變更，則會關閉所有相關聯的會話，而且應用程式必須處理復原。

在 Windows 7 中，應用程式可以順暢地將串流從現有的預設裝置傳送到新的預設音訊端點。 高階音訊 API 集（例如媒體基礎、DirectSound 和 WAVE Api）會執行串流路由功能。 使用這些 API 集合來播放或從預設裝置捕獲串流的媒體應用程式會使用預設的執行，而不需要修改應用程式。 但是，如果您的媒體應用程式直接使用 MMDeviceAPI 或 WASAPI，應用程式就必須提供資料流程路由執行。

> [!Note]  
> MMDeviceAPI 和 WASAPI 是核心音訊 API 元件，可供應用程式用來在裝置上轉譯或捕獲串流。 MMDeviceAPI 會探索新的音訊端點裝置，而 WASAPI 會管理媒體應用程式和音訊端點裝置之間的音訊資料流程程。

 

若要執行串流路由功能，應用程式必須在下列情況下接聽 MMDeviceAPI 和 WASAPI 所傳送的通知：

-   使用者會變更預設裝置。
-   移除現有的預設裝置，並新增預設裝置。
-   裝置格式已變更。

藉由處理這些通知，應用程式可以在傳送串流至新的預設裝置時執行必要的串流管理作業。 此外，應用程式可以在轉譯會話為作用中時，使用使用者所指定的新格式來轉譯或捕捉現有的資料流程。

本節包含下列主題：

-   [取得串流路由的裝置端點](getting-the-default-device-endpoint-for-stream-routing.md)
-   [串流路由的相關通知](relevant-device-notifications-for-stream-routing.md)
-   [串流路由的執行考慮](stream-routing-implementation-considerations.md)

Windows SDK 中包含的下列範例會示範應用程式如何處理串流路由通知。

-   [RenderSharedTimerDriven](rendersharedtimerdriven.md)
-   [RenderSharedEventDriven](rendersharedeventdriven.md)
-   [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md)
-   [RenderExclusiveEventDriven](renderexclusiveeventdriven.md)
-   [CaptureSharedTimerDriven](capturesharedtimerdriven.md)
-   [CaptureSharedEventDriven](capturesharedeventdriven.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[串流管理](stream-management.md)
</dt> <dt>

[關於 MMDevice API](mmdevice-api.md)
</dt> <dt>

[關於 WASAPI](wasapi.md)
</dt> </dl>

 

 



