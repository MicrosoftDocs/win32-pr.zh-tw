---
description: Winsock 的安全通訊端延伸模組可讓通訊端應用程式透過網路控制其流量的安全性。
ms.assetid: 023a9f96-814f-40c3-a186-ae0a0c9baef2
title: Winsock 安全通訊端擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b62ee593b3abbb3bb0f8dbf27b79d6868f04fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026208"
---
# <a name="winsock-secure-socket-extensions"></a>Winsock 安全通訊端擴充功能

Winsock 的安全通訊端延伸模組可讓通訊端應用程式透過網路控制其流量的安全性。 這些延伸模組可讓應用程式針對其網路流量提供安全性原則和需求，以及查詢所套用的安全性設定。 例如，應用程式可以使用這些擴充功能來查詢對等安全性權杖，以用來執行應用層級的存取檢查。

安全通訊端擴充功能的目的是要將 IPsec 所提供的服務和其他安全性通訊協定與 Winsock 架構整合。 在 Windows Vista 之前的 windows Server 2003 和 Windows XP 上，系統管理員已透過本機和網域原則設定 IPsec。 在 Windows Vista 上，安全通訊端延伸模組會改為允許應用程式完全或部分設定和控制其在通訊端層級的網路流量安全性。

應用程式已可使用公用 Api （例如 IPsec 管理、Windows 篩選平台和安全性支援提供者介面 (SSPI) ）來保護網路流量。 不過，使用這些 Api 可能會讓應用程式更難開發，而且可能會使設定和部署變得更困難。 Winsock 安全通訊端擴充功能的設計目的是為了簡化需要安全網路流量的網路應用程式開發，讓 Winsock 處理大部分的複雜度。

這些安全通訊端擴充功能可在 Windows Vista 和更新版本上使用。

## <a name="secure-socket-functions"></a>安全通訊端函式

安全通訊端擴充功能如下所示：

-   [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> 安全通訊端函式目前只支援 IPsec 通訊協定，可在 Windows Vista 和更新版本上使用。

 

安全通訊端函數所使用的結構和列舉如下：

-   [**通訊端 \_ 對等 \_ 目標 \_ 名稱**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [**通訊端 \_ 安全性 \_ 通訊協定**](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [**通訊端 \_ 安全性 \_ 查詢 \_ 資訊**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [**通訊端 \_ 安全性 \_ 查詢 \_ 範本**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [**通訊端 \_ 安全性 \_ 設定**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [**通訊端 \_ 安全性 \_ 設定 \_ IPSEC**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

安全通訊端函式很容易用於一般的應用程式，而且對於需要高度控制安全性的應用程式來說，具有足夠的彈性。 這些函式可讓您將基礎安全性機制隱藏在應用程式之外。 應用程式可以指定一般安全性需求，並讓系統管理員控制用來支援需求的安全性通訊協定。 雖然可以擴充這些函式以新增其他安全性通訊協定，但目前只有 IPsec 會與安全通訊端功能整合。

[**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)函式可讓應用程式在建立連接之前啟用安全性並套用安全性設定。

[**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)函數可讓應用程式指定對應至對等實體的目標名稱。 在驗證對等時，所選取的安全性通訊協定會使用這類資訊。 這項功能解決了受信任攔截式攻擊的疑慮。

[**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)函式是用來刪除先前為通訊端指定的對等名稱。

建立連線之後， [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) 函式可讓應用程式查詢連接的安全性屬性，其中可包含對等存取或電腦存取權杖。

建立連線之後， [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) 函式可讓應用程式模擬對應至通訊端對等的安全性主體，以執行應用層級授權。

[**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)可讓應用程式終止通訊端對等互連的模擬。

## <a name="secure-socket-architecture"></a>安全通訊端架構

![winsock 安全通訊端擴充功能的基本架構](images/ss-arch.png)

-   應用程式會呼叫安全通訊端函數來設定或查詢通訊端的安全性設定。
-   安全通訊端函式是一組型別安全的擴充函式，會使用 Windows Vista 和更新版本上可用之 *dwIoControlCode* 參數的新定義值，將呼叫包裝至 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)函式。 這些 IOCTLs 由網路堆疊處理。
-   網路堆疊會將 [應用層強制執行 (ALE) ](../fwp/application-layer-enforcement--ale-.md) 以及端點控制碼的呼叫導向。 針對 [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)、 [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)和 [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) 函式，ALE 會在本機端點上設定應用程式的設定。 針對 [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) 函式，ALE 將會從適用的本機和遠端端點讀取要求的資訊。
-   根據通訊端事件、應用層強制執行 (ALE) 會使用 Windows 篩選平台來強制執行安全通訊端架構的原則。 如需詳細資訊，請參閱 [關於 Windows 篩選平台](../fwp/about-windows-filtering-platform.md) 和 [應用層強制執行 (ALE) ](../fwp/application-layer-enforcement--ale-.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 篩選平台](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[使用安全通訊端延伸模組的 Advanced Winsock 範例](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[應用層強制 (ALE) ](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[IPsec 設定](../fwp/ipsec-configuration.md)
</dt> <dt>

[IPsec 功能](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[安全 Winsock 程式設計](secure-winsock-programming.md)
</dt> <dt>

[安全性支援提供者介面 (SSPI)](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[使用安全通訊端擴充功能](using-secure-socket-extensions.md)
</dt> <dt>

[Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[Windows 篩選平台 API 函式](../fwp/fwp-functions.md)
</dt> </dl>

 

 
