---
title: 透過 Teredo 接收請求的流量
description: 許多應用程式（例如 Microsoft Internet Explorer 和 Microsoft Outlook）只會起始與網際網路的連線。
ms.assetid: bff5d65e-050d-4b09-9982-8024612ffa6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035d067afeb9c62795efb5acd0bb28adc3afcb16
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104508175"
---
# <a name="receiving-solicited-traffic-over-teredo"></a>透過 Teredo 接收請求的流量

許多應用程式（例如 Microsoft Internet Explorer 和 Microsoft Outlook）只會起始與網際網路的連線。 針對這些應用程式， [Teredo](about-teredo.md) 可在沒有其他 ipv6 介面的情況下，透過 ipv6 提供順暢的連線。 此外，您可以透過舊版 Microsoft Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 平臺上的 Teredo 介面，來接收請求的流量。

下列檔說明這些應用程式如何達成連線能力，以及使用 Teredo 的情況。

## <a name="obtaining-a-destination-address"></a>取得目的地位址

應用程式會使用不同的方法（例如網域名稱系統 (DNS) 或對等名稱解析通訊協定 (PNRP) ）來嘗試取得目的地位址。 應用程式可以使用這些方法來取得多個 IPv4 和 IPv6 IP 位址。 用來取得 IP 位址的一般 Api 包括 Windows XP API [**GetHostByName**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) 和新的 WINDOWS Vista api [**GetAddrInfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)。 例如，使用 GetAddrInfo API 並將 *ai \_ 系列* 參數設定為 AF \_ INET6 做為 addrinfo/通訊協定提示，可讓使用者特別查詢 IPv6 位址的 DNS 伺服器。 具有類型 DNS 類型 AAAA 的 [**DnsQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) API \_ \_ 也可以用來查詢 DNS 伺服器的 aaaa 記錄。

## <a name="establishing-a-connection"></a>建立連線

使用 Teredo 建立的連接會被描述為「無縫」，因為它的處理方式就像任何其他 IPv6 連接一樣。 應用程式的程式設計不需要特別考慮，就能夠利用 Teredo 介面。 在 Teredo 介面之間建立連線時，不需要使用轉送路由器（通常是6to4 和其他原生介面）。 但是 Teredo 是設計為 IPv6 連線的最後手段轉換技術。

> [!Note]  
> 如果提供的主機名稱只解析成 IPv4 位址，就不會使用 Teredo。

 

當應用程式嘗試使用 IPv6 位址連接到目的地時，將會發生下列情況：

-   應用程式會藉由呼叫 [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) API 來取得 IPv6 地址清單。 Windows Vista 堆疊會根據 [RFC 3484](https://www.irt.org/rfc/rfc3484.htm)中指定的排序次序，傳回所有介面的清單。 如此一來，就會在 Teredo 介面之前列出 IPv6 和 6to4 IPv6 介面。 不過，當原生 IPv6 或6to4 連線無法使用時，Teredo 將會是唯一列出的 IPv6 可用介面。

    很重要的一點是，應用程式可以使用 Windows Vista 堆疊所提供的任何介面，但是傳回的介面清單順序通常會導致最後一次嘗試的 Teredo。

-   在 Windows Vista 嘗試透過 Teredo 介面進行連線之前，作業系統會確保 IPv6 位址已穩定。 這會針對傳出連線自動完成，並不是應用程式的重要考慮。 在此情況下，應用程式必須保證位址穩定性，才能呼叫 [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) API，以確保 Teredo 位址是穩定的。

-   Teredo 介面會嘗試連接至目的地的另一個 Teredo 介面。 如果沒有 Teredo 介面，則會透過主機特定轉送來建立與原生或6to4 目的地位址的連線。

初始化網際網路連線的應用程式也可能會收到未經要求的流量。 如需詳細資訊，請參閱透過 [Teredo 接收未經](receiving-unsolicited-traffic-over-teredo.md)要求的流量。

## <a name="using-the-wsaconnectbyname-api"></a>使用 WSAConnectByName API

藉由呼叫 WSAConnectByName API，應用程式可以連接到目的地名稱，而不是指定確切的 IP 位址。 Windows Vista 堆疊優先于 IPv4 的 IPv6，因此會先對 IPv6 位址進行任何連接嘗試。

呼叫 WSAConnectByName API 將會依下列順序來排序所取得的所有目的地 IP 位址：

-   原生 IPv6 位址
-   6to4 IP 位址
-   IPv4 位址
-   Teredo 位址

在內部排序目的地位址之後，系統會根據目的地位址的本機主機上可用的最佳路由來嘗試連接到目的地。 依排序的位址順序指出，如果目的地名稱解析為 IPv4 和 Teredo 位址，則會使用 IPv4 位址來建立連線。

WSAConnectByName API 會在內部運作，以找出位址之間的最佳對應。 這項嘗試是以本機主機和目的地位址上可用的路由為基礎。

由於網際網路上目前沒有 Teredo 轉送，因此原生 IPv6 位址的連線不太可能會成功通過 Teredo 介面。 如果呼叫 WSAConnectByName，Windows Vista 將不會在 Teredo 是唯一可用的 IPv6 支援介面時發出 AAAA 查詢。 這可確保原生 IPv6 位址不會以目的地的形式取得，而且會嘗試透過 IPv4 進行連線，這會有最高的成功機會。 為了在 Teredo 是唯一具備 IPv6 功能的介面時取得 IPv6 位址，應用程式必須明確地使用 DnsQuery API 來處理 AAAA 記錄。

 

 