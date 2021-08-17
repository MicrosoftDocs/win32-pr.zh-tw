---
description: 本主題的目的是要說明 WSDAPI 所執行的探索功能，但不會在 DPWS 或 WS-Discovery 規格中說明。
ms.assetid: ae7eff53-c932-4cba-9e71-c60f308f0e2d
title: 其他 WS-Discovery 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7ee4094950c51ed84724abb9eaea493f7dad7cf7803832fb6e8762fdd99811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106776"
---
# <a name="additional-ws-discovery-functionality"></a>其他 WS-Discovery 功能

在某些情況下，Web 服務 (DPWS) 和相關規格的 [裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/) 並不會明確定義執行功能。 例如， [WS 探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) 規格不會定義多主控環境中的用戶端和主機行為。 當執行 WSDAPI 時，某些探索功能已新增至規格中定義的功能之外。

WSDAPI 也會執行 WS-Discovery v1.1 CD1 的選取部分，以便透過 HTTP 與探索 proxy 進行通訊。

本主題的目的是要說明 WSDAPI 所執行的探索功能，但不會在 DPWS 或 WS-Discovery 規格中說明。

## <a name="ipv6-addresses-and-the-soapudp-uri-format"></a>IPv6 位址和 soap. udp URI 格式

SOAP over UDP 和 WS-Discovery 不會明確描述常值 IPv6 位址如何以 soap. udp URI 格式表示。 [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt)的「統一資源識別項 (URI) ：泛型語法」，指出 soap. udp URI 格式不支援常值 IPv6 位址。

為了簡單起見，WSDAPI 可辨識 soap udp 配置中以方括弧括住的 IPv6 位址。 例如， `soap.udp://[2001:abcd:0001:0002:0003:0004:0005:0032]:3702` WSDAPI 可辨識位址。 這類似于在 HTTP 中處理 IPv6 位址的方式。

## <a name="hello-and-xaddrs"></a>Hello 和 XAddrs

WSDAPI 的 DPWS 裝載物件將永遠不會在訊息本文中傳送具有[XAddrs](xaddr-validation-rules.md)的 WS-Discovery [Hello](hello-message.md)訊息。 如果用戶端需要取得 XAddrs，用戶端一律會在收到 Hello 訊息之後傳送 [解析](resolve-message.md) 訊息。

這種方法有兩個優點。 首先，在 WSDAPI 上建立的裝置絕不會公開可洩漏私人網路 IP 位址的 XAddrs。 其次，在 WSDAPI 上建立的裝置只會公開可供用戶端存取的 XAddrs，這表示 IPv6 位址永遠不會傳送至 IPv4 用戶端。

收到 [探查](probe-message.md) 或解析訊息時，只會在回應中傳送單一 XAddr。 傳送的 XAddr 會對應到收到要求的本機位址。 如果透過 IPv6 跨子網收到要求，WSDAPI 將會在回應中提供全域 IPv6 位址。

## <a name="preferred-addresses"></a>慣用位址

裝置可在 [Hello](hello-message.md)、 [ProbeMatch](probematches-message.md)或 [ResolveMatch](resolvematches-message.md) 訊息中提供多個 XAddrs。 服務也可以在具有不同傳輸位址的多個端點上使用。 在這些情況下，WSDAPI 會嘗試在其找到的第一個可用位址上與裝置通訊。 如果位址是來自可用的通訊協定（例如，在安裝 IPv4 的電腦上使用 IPv4，或在安裝 IPv6 的電腦上使用 IPv6），就可以使用位址。 此外，如果位址來自不在本機子網上的裝置或服務，只有在它是 IPv4、IPv6 網站本機或 IPv6 連結本機時，才能使用此位址。

## <a name="wsdl-in-metadata-exchange"></a>中繼資料交換中的 WSDL

在 WSDAPI 上建立的裝置和服務不會在中繼資料交換中提供其 WSDL，除非應用程式已擴充以提供此資訊。 依預設，WSDL 布建不是程式設計模型的一部分。

## <a name="app_max_delay"></a>應用程式 \_ 最大 \_ 延遲

DPWS 會定義應用程式 \_ 最大 \_ 延遲，這是在接收 [探查](probe-message.md) 和傳送 [ProbeMatch](probematches-message.md)之間延遲的隨機間隔（以5000毫秒為單位）。 Windows防火牆要求 UDP 的多播要求/單播回應模型只會在4秒的防火牆視窗中運作。 因此，WSDAPI 會以2500毫秒或更短的時間傳輸回應，而不是應用程式最大延遲所描述的 5000 ms 視窗 \_ \_ 。

## <a name="iana-port-reservations"></a>IANA 埠保留

WSDAPI 預設會針對 HTTP 流量使用 TCP 埠5357，HTTPS 流量則使用 TCP 埠5358。 這些埠會透過 HTTP.sys 中的 URL 保留專案保留給較低許可權的進程，而且也會使用 IANA 保留。

## <a name="udp-port-sharing"></a>UDP 埠共用

WSDAPI 使用埠共用。 傳送至埠3702的單播訊息可能無法由所有 WSDAPI 應用程式正確處理。 如果應用程式是以獨佔方式系結至埠3702，它可能會防止 WSDAPI 應用程式正確地使用該埠。

## <a name="ws-discovery-v11-cd1-proxy"></a>WS-Discovery v1.1 的 CD1 Proxy

WSDAPI 會搜尋並與探索 proxy 進行通訊，以執行 WS-Discovery v1.1 CD1 受管理模式的通訊協定。 WS-Discovery v1.1 CD1 是 WS-Discovery 的第一個修訂，以包含用於 proxy 與用戶端或裝置間通訊之 HTTP 通訊協定的明確描述。

為了限制多播要求中使用的並行版本數目，WSDAPI 會在2005/04 命名空間中傳送 WS-Discovery 探查要求，但會搜尋 WS-Discovery v1.1 CD1 DiscoveryProxy 類型。 如果 proxy 回應，則 WSDAPI 會將 HTTP 探查或解析要求傳送至指定的 proxy 端點，如 WS-Discovery v1.1 CD1 中所定義。

 

 



