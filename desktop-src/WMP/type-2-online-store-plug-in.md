---
title: 類型 2 線上商店外掛程式
description: 類型 2 線上商店外掛程式
ms.assetid: 16e90a01-20be-49a6-96df-de81a7283f42
keywords:
- Windows Media Player 線上商店、外掛程式
- 線上商店、外掛程式
- 類型2線上商店、外掛程式
- Windows Media Player 線上商店、IWMPSubscriptionService 介面
- 線上商店、IWMPSubscriptionService 介面
- 類型2線上商店、IWMPSubscriptionService 介面
- 外掛程式，Windows Media Player 線上商店
- 外掛程式，線上商店
- 外掛程式，輸入2個線上商店
- 外掛程式，IWMPSubscriptionService 介面
- Windows Media Player 外掛程式，請輸入2個線上商店
- Windows Media Player 外掛程式，線上商店
- Windows Media Player 外掛程式，Windows Media Player 線上商店
- Windows Media Player 外掛程式、IWMPSubscriptionService 介面
- IWMPSubscriptionService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a254fe0aeed0d03f4437c408f4c00c181fdeb07cf75df8ff9d7a1139ea284150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117475"
---
# <a name="type-2-online-store-plug-in"></a>類型 2 線上商店外掛程式

Type 2 online store 外掛程式是一種 COM 元件，可實 [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) 介面並選擇性地執行 [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2) 介面。 Windows Media Player 9 會呼叫 **IWMPSubscriptionService** 介面的方法。 Windows Media Player 10 或更新版本會呼叫 **IWMPSubscriptionService** 和 **IWMPSubscriptionService2** 介面的方法。

Type 2 online store 外掛程式會封裝為同進程 COM 伺服器。 也就是說，外掛程式會在對應至 Windows Media Player 進程的 .dll 檔案中執行。

Windows Media Player 視需要啟用 type 2 online store 外掛程式。 例如，假設使用者嘗試播放受保護的歌曲，而且沒有任何目前的授權可以播放。 在此情況下，Windows Media Player 會檢查檔案標頭或 DRM 標頭中的 **ContentDistributor** 屬性。 如果存在與線上商店的金鑰名稱相符的值，Windows Media Player 會檢查登錄以查看該線上商店是否已提供類型2外掛程式。 如果外掛程式存在，Windows Media Player 載入外掛程式並呼叫其方法，以判斷使用者是否具有播放歌曲的許可權。

下列清單描述 Windows Media Player 呼叫 type 2 online store 外掛程式的一些案例。

-   **使用者嘗試播放線上商店內容。** 發生這種情況時，Windows Media Player 會呼叫外掛程式的[IWMPSubscriptionService：： allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay)方法，並將指標傳遞至使用者嘗試播放的數位媒體專案。 線上商店可以使用此功能來更新使用者的授權，以播放內容或不允許播放。 如果外掛程式在 *pfAllowPlay* 參數中傳回 **TRUE** ，Windows Media Player 會嘗試播放內容。 如果有效的授權不存在，播放仍會失敗;此流程不會規避 (DRM) 的數位版權管理。
-   **使用者要求將內容燒錄到 CD 或 DVD 的許可權。** 發生這種情況時，Windows Media Player 會呼叫外掛程式的[IWMPSubscriptionService：： allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn)方法。
-   **使用者嘗試同步處理線上商店內容與裝置，或 Windows Media Player 已準備好自動同步處理線上商店內容與裝置。** 發生這種情況時，Windows Media Player 會呼叫外掛程式的[IWMPSubscriptionService2：:p repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync)方法，以警示線上存放區，媒體專案即將與特定裝置同步處理（由其正式名稱識別）。 這是線上商店用來判斷是否允許使用者與裝置同步處理媒體專案的機會。 線上商店也有機會準備裝置進行同步處理，以及更新與裝置或媒體專案相關聯的記錄，例如同步處理計數。 外掛程式應將許可權、準備和記錄保留工作傳遞給個別的執行緒，並立即從 **prepareForSync** 傳回。 當個別的執行緒完成其工作時，必須呼叫[IWMPSubscriptionServiceCallback：： onComplete](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete)來通知 Windows Media Player。
-   **裝置會變成可供背景處理。** 當裝置連線時，Windows Media Player 藉由呼叫[IWMPSubscriptionService2：:d eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable)，向線上商店發出裝置可用和閒置的警示。
-   **使用者按一下按鈕，即可在 Windows Media Player 中啟用線上商店。** 發生這種情況時，Windows Media Player 會呼叫外掛程式的[IWMPSubscriptionService2：： serviceEvent](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-serviceevent)方法。 當使用者切換至另一個服務時，Windows Media Player 也會呼叫這個方法。
-   **Windows Media Player 進入較低的活動狀態。** 當這種情況發生時，播放程式會呼叫外掛程式的 [IWMPSubscriptionService：： startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing) 方法。 線上商店可以使用這個機會來啟動或喚醒任何執行背景工作的執行緒，例如更新過期的授權或編譯播放次數資料。
-   **Windows Media Player 進入高活動的狀態。** 發生這種情況時，Windows Media Player 會呼叫外掛程式的[IWMPSubscriptionService2：： stopBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-stopbackgroundprocessing)方法。 這會通知外掛程式必須暫停任何正在執行背景工作的執行緒。

當玩家會話結束時，Windows Media Player 會釋放線上商店元件。 在發行時，元件必須中斷進行中的任何背景處理，然後關閉。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMPSubscriptionService 介面**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**IWMPSubscriptionService2 介面**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> <dt>

[**IWMPSubscriptionServiceCallback 介面**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)
</dt> <dt>

[**類型2線上商店範例**](type-2-online-store-samples.md)
</dt> </dl>

 

 




