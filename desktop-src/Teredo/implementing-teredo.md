---
title: 執行 Teredo
ms.assetid: f32e908e-a96d-48a2-8b79-e2e53c64cb68
description: 深入瞭解：執行 Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b24f4524d6c513dc0a5cd11e7f6420eb7e546fa3bce75c830759fc38faaef9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681648"
---
# <a name="implementing-teredo"></a>執行 Teredo

雖然不需要對 [teredo](about-teredo.md)進行程式設計變更，但建議開發人員進行較小的變更，以最有效率地使用 teredo 介面：

-   只有能夠使用 IPv6 流量才能利用 Teredo 的應用程式可能會發生這種情況。 不過，在開發應用程式協定時，應該將 IPv4 和 IPv6 流量的處理納入考慮。 應用程式必須系結至 [ \_ 通訊端選項] 中的 af INET6 或 af \_ UNSPEC。
-   如果應用程式能夠從網際網路接聽未經要求的流量，就必須在 Windows 防火牆內 (NAT) 的 [處理] 選項啟用網路位址轉譯。 這是藉由呼叫 [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) API，並將 "Edge 遍歷" 選項設定為 VARIANT \_ TRUE 來完成。 WindowsVista 可確保在應用程式需要 Teredo 位址時可供使用。 因此，當使用 Teredo 介面時，Teredo 位址會自動穩定。 如果應用程式想要確保 Teredo 位址穩定，呼叫 [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) API 會觸發 teredo 以轉換成穩定狀態。
-   應用程式也可以使用 [IPV6 \_ 保護 \_ 層級](/windows/desktop/WinSock/ipv6-protection-level) Winsock 通訊端選項來設定保護層級，以允許未經要求的輸入流量通過防火牆。 如需詳細資訊，請參閱透過 [Teredo 接收未經](receiving-unsolicited-traffic-over-teredo.md) 要求的流量。

網際網路通訊協定協助程式 (IP 協助程式) 特定 Teredo 函式的實作為範例，讓您瞭解如何驗證 Teredo 位址，並將其提供給應用程式。 如需詳細資訊，請參閱搭配 [IP Helper 使用 Teredo](using-teredo-with-ip-helper.md)。

 

 
