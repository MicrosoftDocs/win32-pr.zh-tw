---
title: 執行 Teredo
ms.assetid: f32e908e-a96d-48a2-8b79-e2e53c64cb68
description: 深入瞭解：執行 Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffdf2859d3742bea02e240c6a26bd0e4ade85ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195070"
---
# <a name="implementing-teredo"></a>執行 Teredo

雖然不需要對 [teredo](about-teredo.md)進行程式設計變更，但建議開發人員進行較小的變更，以最有效率地使用 teredo 介面：

-   只有能夠使用 IPv6 流量才能利用 Teredo 的應用程式可能會發生這種情況。 不過，在開發應用程式協定時，應該將 IPv4 和 IPv6 流量的處理納入考慮。 應用程式必須系結至 [ \_ 通訊端選項] 中的 af INET6 或 af \_ UNSPEC。
-   能夠從網際網路接聽未經要求流量的應用程式，必須在 Windows 防火牆內啟用網路位址轉譯 (NAT) 遍歷選項。 這是藉由呼叫 [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) API，並將 "Edge 遍歷" 選項設定為 VARIANT \_ TRUE 來完成。 Windows Vista 可確保 Teredo 位址在應用程式需要時可供使用。 因此，當使用 Teredo 介面時，Teredo 位址會自動穩定。 如果應用程式想要確保 Teredo 位址穩定，呼叫 [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) API 會觸發 teredo 以轉換成穩定狀態。
-   應用程式也可以使用 [IPV6 \_ 保護 \_ 層級](/windows/desktop/WinSock/ipv6-protection-level) Winsock 通訊端選項來設定保護層級，以允許未經要求的輸入流量通過防火牆。 如需詳細資訊，請參閱透過 [Teredo 接收未經](receiving-unsolicited-traffic-over-teredo.md) 要求的流量。

網際網路通訊協定協助程式 (IP 協助程式) 特定 Teredo 函式的實作為範例，讓您瞭解如何驗證 Teredo 位址，並將其提供給應用程式。 如需詳細資訊，請參閱搭配 [IP Helper 使用 Teredo](using-teredo-with-ip-helper.md)。

 

 
