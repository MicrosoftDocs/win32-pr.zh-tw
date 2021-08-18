---
description: 裝置上的 web 服務 API (WSDAPI) 為 Windows Vista 上的 web 服務 (DPWS) 提供裝置設定檔的支援，這可讓 web 服務 () 型電腦和網路連線裝置之間的通訊 Windows 通訊。
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: WSDAPI 規格合規性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dcf649d8d2771d17f24e983a739c0119a0fe8af67f70b706ba35bcddec20d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991388"
---
# <a name="wsdapi-specification-compliance"></a>WSDAPI 規格合規性

裝置上的 web 服務 API (WSDAPI) 為 Windows Vista 上的 web 服務 (DPWS) 提供[裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/)的支援，這可讓 web 服務 () 型電腦和網路連線裝置之間的通訊 Windows 通訊。 DPWS 組合了基本的 WS 規格，例如 [ws-事件](https://schemas.xmlsoap.org/ws/2004/08/eventing/)、 [Ws-atomictransaction 探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)和 [ws-透過 ws-metadataexchange](https://schemas.xmlsoap.org/ws/2004/09/mex/)，並增強或限制其為資源受限的裝置提供一組基本的功能。 此基準規格包含必要的功能，例如透過中繼資料描述裝置屬性的能力，以及選用的功能，例如基於安全性理由拒絕特定訊息的能力。

Windows Vista 中的 WSDAPI 實作為第一版 DPWS 的明確支援，而且是 DPWS 的非受控執行，與其他 Web (服務的執行方式不同，例如[Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85))或[ws-management](https://schemas.xmlsoap.org/ws/2005/06/management/)) 。

下列主題是裝置製造商和其他裝置實施者的相關主題，這些裝置可建立與 Windows 型 wsdapi 用戶端和主機交互操作的裝置，而不需使用 WSDAPI。 這些主題會描述相對於基礎規格的 WSDAPI 執行。 其中涵蓋了執行必要功能、選擇性功能，以及未在規格中定義的其他功能。

-   [DPWS 規格合規性](dpws-specification-compliance.md)
-   [WS-探索規格合規性](ws-discovery-specification-compliance.md)
-   [透過 ws-metadataexchange 和 WS-Transfer 規格合規性](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [其他 WS-Discovery 功能](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WSD 裝置開發](wsd-device-development.md)
</dt> <dt>

[WSD 裝置執行建議](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
