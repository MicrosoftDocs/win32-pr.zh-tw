---
description: 裝置上的 web 服務 API (WSDAPI) 是 Windows Vista 和 Windows Server 2008 的 web 服務 (DPWS) 的裝置設定檔的執行。
ms.assetid: 8eaeacb3-43db-4a57-8548-e5b81213269c
title: 關於裝置上的 Web 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7facef3bfed004a834e151db0c58c83a1576e515ed89fa0d690813bc4c18bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552507"
---
# <a name="about-web-services-on-devices"></a>關於裝置上的 Web 服務

裝置上的 web 服務 API (WSDAPI) 是 Windows Vista 和 Windows Server 2008 的 web 服務 (DPWS) 的[裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/)的執行。 DPWS 會限制 Web 服務規格，讓用戶端可以輕鬆地探索裝置。 探索到裝置之後，用戶端就可以取出該裝置上所裝載之服務的描述，並使用這些服務。

## <a name="devices-and-services"></a>裝置和服務

*裝置* 是連接到網路的元件，通常是硬體。 範例包括印表機、網路攝影機和影片系統。

裝置可能包含零或多個 *服務*。 例如，影片裝置可能包含支援開啟和關閉電源、播放控制、媒體彈出和影片串流的服務。 Play 控制項可能會支援播放、暫停、倒轉和向前快轉等動作。

## <a name="discovering-and-manipulating-a-device"></a>探索和操作裝置

WSDAPI 可讓用戶端透過網路探索及存取遠端裝置及其相關聯的服務，以擴充本機隨插即用模型。 它支援探索、單向和雙向控制訊息，以及事件。

![此圖顯示 WSDAPI 如何讓用戶端探索及存取遠端裝置。](images/overview01.png)

如果有任何) 使用唯一位址和一組標準化的 XML 訊息，DPWS 裝置就會宣佈其存在並公開服務 (。 DPWS 用戶端可以使用探索程式來尋找裝置、列舉其服務，並連接到這些服務以執行特定動作。

WSDAPI 用戶端會先查詢裝置以取得其服務的完整說明，包括服務類型 (例如印表機服務類型或掃描器服務類型) 。 然後，用戶端會藉由呼叫服務類型所定義的命令來控制裝置 (例如，藉由在印表機服務類型為) 的裝置上呼叫 **CreatePrintJob** 。 此外，用戶端也可以藉由訂閱命令執行期間發生的事件，監視每個服務中的狀態變更。

![顯示 WSDAPI 用戶端如何查詢和與裝置互動的圖表。](images/netdevice01.png)

如需裝置訊息模式的詳細資訊，請參閱[探索和中繼資料 Exchange 訊息模式](discovery-and-metadata-exchange-message-patterns.md)。

## <a name="logical-and-physical-addressing"></a>邏輯與實體定址

邏輯定址可用來唯一識別與實體位址無關的裝置。 WS-Discovery 提供了一種機制，可將邏輯位址解析成實體位址，讓用戶端對裝置的訊息得以進行。 例如，網路連接儲存體 (NAS) 與您一起攜帶。 如果您有膝上型電腦和 NAS，則不論您是在子網之間移動 (IP 位址) 的實體位址為何，您的膝上型電腦都應該能夠辨識它是相同的裝置。 完成此程式需要裝置具有與其取得的 IP 位址無關的身分識別;由於傳統的漫遊案例中無法使用 DNS 等傳統機制，因此 WS-Addressing 和 WS-Discovery 提供邏輯定址和解決方式作為臨機操作的替代方案。

製造裝置時，會提供一個全域唯一識別碼，以 UUID URI 表示。 裝置的這個識別碼永遠不會變更。 裝置開啟電源時，一律會透過 WS-Discovery [Hello](hello-message.md) 訊息來宣告其邏輯位址，並接受將其轉換為實體位址的要求， (通常是透過 WS-Discovery [解析](resolve-message.md) 或 [探查](probe-message.md) 訊息的 HTTP) 。 一旦取得有效的實體位址 (IP 位址) 取得之後，所有訊息都會在該位址上進行，而且只有在位址變更、裝置變更狀態和用戶端需要通知，或裝置離線時，才會使用 WS-Discovery。

## <a name="building-applications"></a>建置應用程式

WSDAPI 提供一般 DPWS SOAP 堆疊，供用戶端和服務應用程式使用。 [裝置上的 Web 服務程式碼](web-services-for-devices-code-generator.md)產生器 (WsdCodeGen.exe) 可用來將服務描述 (WSDL) 轉換成應用程式可直接呼叫的 proxy 和存根程式碼。 這個產生的程式碼會自動將函式呼叫和參數轉換成 SOAP 訊息和 XML 欄位，然後呼叫 WSDAPI 來發出對遠端裝置或用戶端的要求。

建立 WSDAPI 應用程式來建立和啟動 PnP 傳回的函式實例時，可以使用函數探索。 這些函式實例包含的資料，可以在只需要簡單探索時，透過 PnP Api 取得詳細資訊。 如需詳細資訊，請參閱函式 [探索](/previous-versions/windows/desktop/fundisc/fd-portal) 和 [PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[探索和中繼資料 Exchange 訊息模式](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[WSDAPI 規格合規性](wsdapi-specification-compliance.md)
</dt> <dt>

[WSDAPI 介面的總覽](overview-of-the-wsdapi-interfaces.md)
</dt> </dl>

 

 
