---
description: 深入瞭解： WS-Discovery 規格合規性
ms.assetid: b795a385-b48d-4a16-9d91-e48bca120572
title: WS-Discovery 規格合規性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07794140f05a065fb770ae2d5782f24180fb7e7ef66757278d5c5c93a3fd7e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991408"
---
# <a name="ws-discovery-specification-compliance"></a>WS-Discovery 規格合規性

[WS-探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) 說明如何執行下列工作：

-   宣佈本機子網上的服務可用性
-   搜尋子網上的服務
-   找出先前參考的服務

為了達成此目的，WS-Discovery 定義 2 1 方向的訊息、 [Hello](hello-message.md) 和 [再見](bye-message.md)，以及兩個雙向搜尋訊息、 [探查](probe-message.md) 和 [解決](resolve-message.md)。

WS-Discovery 也提供 IPv4 和 IPv6 連結本機探索的位址和保留埠。 此規格也可讓您在其他地方定義替代系結，例如在 [Web 服務的裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/) 中定義的 HTTP 系結探查 (DPWS) 。

WS-Discovery 規格會根據指定的執行建議或限制，使用條款來描述選用功能。 省略的功能可能是在不是由 WSDAPI 所執行的 WS-Discovery 規格中所述的功能，也可能是 WSDAPI 在 WS-Discovery 規格中指定的方法中所執行的功能。

本主題說明如何使用 WSDAPI 執行來處理 WS-Discovery 的限制、需求和選用功能。 本主題最適合與 WS-Discovery 規格一起閱讀。

## <a name="ws-discovery-and-soap-over-udp-support"></a>WS-Discovery 和 SOAP over UDP 支援

在 SOAP over UDP 中，第3.2 節指定 UDP 訊息必須符合64K 資料包。 WSDAPI 會接受64K 的 UDP 訊息，但是最大 \_ 信封 \_ 大小 (32k) 的 DPWS 條件約束將會限制訊息大小。 根據 [WS 探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)的要求，WSDAPI 支援第4節所述的訊息模式。

您可以將 WSDAPI 設定為支援區段7和8中的安全性模型。 當設定時，WSDAPI 會將輸出 WS-Discovery 的訊息簽章，並驗證輸入訊息上的簽章。

WSDAPI 會實 DPWS 附錄 I 修改過的附錄 I 中所定義的重新傳輸演算法。

在 WS-Discovery 中，WSDAPI 會使用2.4 節中指定的位址。 WSDAPI \_ 會將應用程式最大 \_ 延遲從區段2.4 延伸，而不是 DPWS 附錄 I 中所定義的範圍。如需應用程式 \_ 最大延遲的詳細資訊 \_ ，請參閱 [其他 WS-Discovery 功能](additional-ws-discovery-functionality.md)。

WS-Discovery 描述 `uuid:` 2.6 節中的 URI 格式建議，但 WSDAPI 會覆寫這項建議。 相反地，WSDAPI 會使用 `urn:uuid:` DPWS 中所述的 URI 格式。

WS-Discovery 的第3節描述用戶端如何與探索 proxy 互動。 WSDAPI 無法辨識此互動，並且會忽略來自探索 proxy 的宣告。 在 Windows 7 中，WSDAPI 會對 WS-Discovery 通訊協定（WS-Discovery 遠端擴充功能）執行私用擴充功能，以允許探索用戶端藉由將要求傳送至集中式 proxy 來搜尋分散于許多不同網路的服務。如需詳細資訊，請參閱[其他 WS-Discovery 功能](additional-ws-discovery-functionality.md)。

4.1 第3節的 WS-Discovery 要求在傳送 [Hello](hello-message.md) 訊息之前必須先經過一段計時器。 裝載 API 不會在傳送 Hello 訊息之前等候。 如果案例需要延遲才能傳送 Hello 訊息，則應用程式開發人員必須執行等候。

WSDAPI 會執行 WS-Discovery 節4、5和6中所述的所有訊息。 WSDAPI 也會強制執行 \_ DPWS 附錄 I 所修改的第7節中所述的比對超時。 WSDAPI 只會防止從第9節的安全考慮進行「重新執行」。

WSDAPI 會依照 WS-Discovery 附錄 I 中所述的方式來執行應用程式排序。

 

 



