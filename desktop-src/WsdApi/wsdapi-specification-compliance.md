---
description: 裝置上的 web 服務 API (WSDAPI) 支援 Windows Vista 上的 Web 服務 (DPWS) 的裝置設定檔，可在 Windows 電腦與網路連線裝置之間進行 Web 服務 () 通訊。
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: WSDAPI 規格合規性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192898"
---
# <a name="wsdapi-specification-compliance"></a>WSDAPI 規格合規性

裝置上的 web 服務 API (WSDAPI) 支援 Windows Vista 上的 Web 服務 (DPWS) 的 [裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/) ，可在 windows 電腦與網路連線裝置之間進行 web 服務 () 通訊。 DPWS 組合了基本的 WS 規格，例如 [ws-事件](https://schemas.xmlsoap.org/ws/2004/08/eventing/)、 [Ws-atomictransaction 探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)和 [ws-透過 ws-metadataexchange](https://schemas.xmlsoap.org/ws/2004/09/mex/)，並增強或限制其為資源受限的裝置提供一組基本的功能。 此基準規格包含必要的功能，例如透過中繼資料描述裝置屬性的能力，以及選用的功能，例如基於安全性理由拒絕特定訊息的能力。

Windows Vista 中的 WSDAPI 實作為第一版的 DPWS 明確支援，而且是 DPWS 的非受控執行，其與其他 Web 服務的執行方式不同， (例如 [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) 或 [ws-management](https://schemas.xmlsoap.org/ws/2005/06/management/)) 。

下列主題是裝置製造商和其他裝置實作者的相關主題，可建立與以 Windows 為基礎的 WSDAPI 用戶端和主機交互操作的裝置，而不需使用 WSDAPI。 這些主題會描述相對於基礎規格的 WSDAPI 執行。 其中涵蓋了執行必要功能、選擇性功能，以及未在規格中定義的其他功能。

-   [DPWS 規格合規性](dpws-specification-compliance.md)
-   [WS-探索規格合規性](ws-discovery-specification-compliance.md)
-   [透過 ws-metadataexchange 和 WS-Transfer 規格合規性](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [其他 WS-Discovery 功能](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WSD 裝置開發](wsd-device-development.md)
</dt> <dt>

[WSD 裝置實行建議](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
