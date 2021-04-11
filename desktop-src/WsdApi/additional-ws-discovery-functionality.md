---
description: 本主題的目的是要說明 WSDAPI 所執行的探索功能，但不會在 DPWS 或 WS-Discovery 規格中說明。
ms.assetid: ae7eff53-c932-4cba-9e71-c60f308f0e2d
title: 其他 WS-Discovery 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9856605273bec9c757e0b29c389991bf061309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194486"
---
# <a name="additional-ws-discovery-functionality"></a><span data-ttu-id="be29c-103">其他 WS-Discovery 功能</span><span class="sxs-lookup"><span data-stu-id="be29c-103">Additional WS-Discovery Functionality</span></span>

<span data-ttu-id="be29c-104">在某些情況下，Web 服務 (DPWS) 和相關規格的 [裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/) 並不會明確定義執行功能。</span><span class="sxs-lookup"><span data-stu-id="be29c-104">In some cases, the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) and related specifications do not explicitly define implementation functionality.</span></span> <span data-ttu-id="be29c-105">例如， [WS 探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) 規格不會定義多主控環境中的用戶端和主機行為。</span><span class="sxs-lookup"><span data-stu-id="be29c-105">For example, the [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) specification does not define client and host behavior in multi-homed environments.</span></span> <span data-ttu-id="be29c-106">當執行 WSDAPI 時，某些探索功能已新增至規格中定義的功能之外。</span><span class="sxs-lookup"><span data-stu-id="be29c-106">When WSDAPI was implemented, some discovery functionality was added beyond the functionality defined in the specification.</span></span>

<span data-ttu-id="be29c-107">WSDAPI 也會執行 WS-Discovery v1.1 CD1 的選取部分，以便透過 HTTP 與探索 proxy 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="be29c-107">WSDAPI also implements selected portions of WS-Discovery v1.1 CD1 for communicating with a discovery proxy over HTTP.</span></span>

<span data-ttu-id="be29c-108">本主題的目的是要說明 WSDAPI 所執行的探索功能，但不會在 DPWS 或 WS-Discovery 規格中說明。</span><span class="sxs-lookup"><span data-stu-id="be29c-108">The purpose of this topic is to describe the discovery functionality implemented by WSDAPI but not otherwise described in the DPWS or WS-Discovery specifications.</span></span>

## <a name="ipv6-addresses-and-the-soapudp-uri-format"></a><span data-ttu-id="be29c-109">IPv6 位址和 soap. udp URI 格式</span><span class="sxs-lookup"><span data-stu-id="be29c-109">IPv6 addresses and the soap.udp URI format</span></span>

<span data-ttu-id="be29c-110">SOAP over UDP 和 WS-Discovery 不會明確描述常值 IPv6 位址如何以 soap. udp URI 格式表示。</span><span class="sxs-lookup"><span data-stu-id="be29c-110">SOAP-over-UDP and WS-Discovery do not explicitly describe how a literal IPv6 address is represented in the soap.udp URI format.</span></span> <span data-ttu-id="be29c-111">[RFC 2396](https://www.ietf.org/rfc/rfc2396.txt)的「統一資源識別項 (URI) ：泛型語法」，指出 soap. udp URI 格式不支援常值 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="be29c-111">[RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), entitled "Uniform Resource Identifiers (URI): Generic Syntax", indicates that literal IPv6 addresses are not supported by the soap.udp URI format.</span></span>

<span data-ttu-id="be29c-112">為了簡單起見，WSDAPI 可辨識 soap udp 配置中以方括弧括住的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="be29c-112">For simplicity, WSDAPI recognizes IPv6 addresses enclosed in square brackets in the soap.udp scheme.</span></span> <span data-ttu-id="be29c-113">例如， `soap.udp://[2001:abcd:0001:0002:0003:0004:0005:0032]:3702` WSDAPI 可辨識位址。</span><span class="sxs-lookup"><span data-stu-id="be29c-113">For example, the address `soap.udp://[2001:abcd:0001:0002:0003:0004:0005:0032]:3702` is recognized by WSDAPI.</span></span> <span data-ttu-id="be29c-114">這類似于在 HTTP 中處理 IPv6 位址的方式。</span><span class="sxs-lookup"><span data-stu-id="be29c-114">This is similar to how IPv6 addresses are handled in HTTP.</span></span>

## <a name="hello-and-xaddrs"></a><span data-ttu-id="be29c-115">Hello 和 XAddrs</span><span class="sxs-lookup"><span data-stu-id="be29c-115">Hello and XAddrs</span></span>

<span data-ttu-id="be29c-116">WSDAPI 的 DPWS 裝載物件將永遠不會在訊息本文中傳送具有[XAddrs](xaddr-validation-rules.md)的 WS-Discovery [Hello](hello-message.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="be29c-116">WSDAPI's DPWS hosting object will never send a WS-Discovery [Hello](hello-message.md) message with [XAddrs](xaddr-validation-rules.md) in the message body.</span></span> <span data-ttu-id="be29c-117">如果用戶端需要取得 XAddrs，用戶端一律會在收到 Hello 訊息之後傳送 [解析](resolve-message.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="be29c-117">A client will always send a [Resolve](resolve-message.md) message after receiving a Hello message if the client needs to get the XAddrs.</span></span>

<span data-ttu-id="be29c-118">這種方法有兩個優點。</span><span class="sxs-lookup"><span data-stu-id="be29c-118">There are two benefits of this approach.</span></span> <span data-ttu-id="be29c-119">首先，在 WSDAPI 上建立的裝置絕不會公開可洩漏私人網路 IP 位址的 XAddrs。</span><span class="sxs-lookup"><span data-stu-id="be29c-119">First, a device built on WSDAPI will never expose XAddrs that disclose the IP addresses of private networks.</span></span> <span data-ttu-id="be29c-120">其次，在 WSDAPI 上建立的裝置只會公開可供用戶端存取的 XAddrs，這表示 IPv6 位址永遠不會傳送至 IPv4 用戶端。</span><span class="sxs-lookup"><span data-stu-id="be29c-120">Secondly, a device built on WSDAPI only exposes XAddrs that are accessible to the client, which means that IPv6 addresses are never sent to an IPv4 client.</span></span>

<span data-ttu-id="be29c-121">收到 [探查](probe-message.md) 或解析訊息時，只會在回應中傳送單一 XAddr。</span><span class="sxs-lookup"><span data-stu-id="be29c-121">When a [Probe](probe-message.md) or Resolve message is received, only a single XAddr is sent in response.</span></span> <span data-ttu-id="be29c-122">傳送的 XAddr 會對應到收到要求的本機位址。</span><span class="sxs-lookup"><span data-stu-id="be29c-122">The sent XAddr corresponds to the local address on which the request was received.</span></span> <span data-ttu-id="be29c-123">如果透過 IPv6 跨子網收到要求，WSDAPI 將會在回應中提供全域 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="be29c-123">If the request was received across subnets over IPv6, WSDAPI will provide a global IPv6 address in the response.</span></span>

## <a name="preferred-addresses"></a><span data-ttu-id="be29c-124">慣用位址</span><span class="sxs-lookup"><span data-stu-id="be29c-124">Preferred addresses</span></span>

<span data-ttu-id="be29c-125">裝置可在 [Hello](hello-message.md)、 [ProbeMatch](probematches-message.md)或 [ResolveMatch](resolvematches-message.md) 訊息中提供多個 XAddrs。</span><span class="sxs-lookup"><span data-stu-id="be29c-125">A device can provide multiple XAddrs in a [Hello](hello-message.md), [ProbeMatch](probematches-message.md), or [ResolveMatch](resolvematches-message.md) message.</span></span> <span data-ttu-id="be29c-126">服務也可以在具有不同傳輸位址的多個端點上使用。</span><span class="sxs-lookup"><span data-stu-id="be29c-126">A service can also be available at multiple endpoints with different transport addresses.</span></span> <span data-ttu-id="be29c-127">在這些情況下，WSDAPI 會嘗試在其找到的第一個可用位址上與裝置通訊。</span><span class="sxs-lookup"><span data-stu-id="be29c-127">In these cases, WSDAPI will try to communicate with the device on the first usable address it finds.</span></span> <span data-ttu-id="be29c-128">如果位址是來自可用的通訊協定（例如，在安裝 IPv4 的電腦上使用 IPv4，或在安裝 IPv6 的電腦上使用 IPv6），就可以使用位址。</span><span class="sxs-lookup"><span data-stu-id="be29c-128">An address is usable if it is from an available protocol, such as IPv4 on a machine where IPv4 is installed or IPv6 on a machine where IPv6 is installed.</span></span> <span data-ttu-id="be29c-129">此外，如果位址來自不在本機子網上的裝置或服務，只有在它是 IPv4、IPv6 網站本機或 IPv6 連結本機時，才能使用此位址。</span><span class="sxs-lookup"><span data-stu-id="be29c-129">Additionally, if the address came from a device or service that is not on the local subnet, it is usable only if it is IPv4, IPv6 site local, or IPv6 link local.</span></span>

## <a name="wsdl-in-metadata-exchange"></a><span data-ttu-id="be29c-130">中繼資料交換中的 WSDL</span><span class="sxs-lookup"><span data-stu-id="be29c-130">WSDL in metadata exchange</span></span>

<span data-ttu-id="be29c-131">在 WSDAPI 上建立的裝置和服務不會在中繼資料交換中提供其 WSDL，除非應用程式已擴充以提供此資訊。</span><span class="sxs-lookup"><span data-stu-id="be29c-131">Devices and services built on WSDAPI do not provide their WSDL in metadata exchange unless extended by the application to provide this information.</span></span> <span data-ttu-id="be29c-132">依預設，WSDL 布建不是程式設計模型的一部分。</span><span class="sxs-lookup"><span data-stu-id="be29c-132">By default, WSDL provision is not part of the programming model.</span></span>

## <a name="app_max_delay"></a><span data-ttu-id="be29c-133">應用程式 \_ 最大 \_ 延遲</span><span class="sxs-lookup"><span data-stu-id="be29c-133">APP\_MAX\_DELAY</span></span>

<span data-ttu-id="be29c-134">DPWS 會定義應用程式 \_ 最大 \_ 延遲，這是在接收 [探查](probe-message.md) 和傳送 [ProbeMatch](probematches-message.md)之間延遲的隨機間隔（以5000毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="be29c-134">DPWS defines APP\_MAX\_DELAY, the random interval to delay between receiving a [Probe](probe-message.md) and sending a [ProbeMatch](probematches-message.md), as 5,000 milliseconds.</span></span> <span data-ttu-id="be29c-135">Windows 防火牆要求 UDP 的多播要求/單播回應模型只能在4秒的防火牆視窗中運作。</span><span class="sxs-lookup"><span data-stu-id="be29c-135">Windows Firewall requires that the multicast request/unicast response model for UDP will only work within the 4 second firewall window.</span></span> <span data-ttu-id="be29c-136">因此，WSDAPI 會以2500毫秒或更短的時間傳輸回應，而不是應用程式最大延遲所描述的 5000 ms 視窗 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="be29c-136">As a result, WSDAPI will transmit responses in 2,500 ms or less, instead of the 5,000 ms window described by APP\_MAX\_DELAY.</span></span>

## <a name="iana-port-reservations"></a><span data-ttu-id="be29c-137">IANA 埠保留</span><span class="sxs-lookup"><span data-stu-id="be29c-137">IANA port reservations</span></span>

<span data-ttu-id="be29c-138">WSDAPI 預設會針對 HTTP 流量使用 TCP 埠5357，HTTPS 流量則使用 TCP 埠5358。</span><span class="sxs-lookup"><span data-stu-id="be29c-138">WSDAPI uses TCP port 5357 for HTTP traffic and TCP port 5358 for HTTPS traffic by default.</span></span> <span data-ttu-id="be29c-139">這些埠會透過 HTTP.sys 中的 URL 保留專案保留給較低許可權的進程，而且也會使用 IANA 保留。</span><span class="sxs-lookup"><span data-stu-id="be29c-139">These ports are reserved for lower privilege processes through a URL reservation in HTTP.sys, and are also reserved with IANA.</span></span>

## <a name="udp-port-sharing"></a><span data-ttu-id="be29c-140">UDP 埠共用</span><span class="sxs-lookup"><span data-stu-id="be29c-140">UDP port sharing</span></span>

<span data-ttu-id="be29c-141">WSDAPI 使用埠共用。</span><span class="sxs-lookup"><span data-stu-id="be29c-141">WSDAPI uses port sharing.</span></span> <span data-ttu-id="be29c-142">傳送至埠3702的單播訊息可能無法由所有 WSDAPI 應用程式正確處理。</span><span class="sxs-lookup"><span data-stu-id="be29c-142">Unicast messages sent to port 3702 may not be properly handled by all WSDAPI-based applications.</span></span> <span data-ttu-id="be29c-143">如果應用程式是以獨佔方式系結至埠3702，它可能會防止 WSDAPI 應用程式正確地使用該埠。</span><span class="sxs-lookup"><span data-stu-id="be29c-143">If an application binds exclusively to port 3702, it may prevent WSDAPI-based applications from using that port correctly.</span></span>

## <a name="ws-discovery-v11-cd1-proxy"></a><span data-ttu-id="be29c-144">WS-Discovery v1.1 的 CD1 Proxy</span><span class="sxs-lookup"><span data-stu-id="be29c-144">WS-Discovery v1.1 CD1 Proxy</span></span>

<span data-ttu-id="be29c-145">WSDAPI 會搜尋並與探索 proxy 進行通訊，以執行 WS-Discovery v1.1 CD1 受管理模式的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="be29c-145">WSDAPI will search for and communicate with a discovery proxy that implements the WS-Discovery v1.1 CD1 managed mode protocol.</span></span> <span data-ttu-id="be29c-146">WS-Discovery v1.1 CD1 是 WS-Discovery 的第一個修訂，以包含用於 proxy 與用戶端或裝置間通訊之 HTTP 通訊協定的明確描述。</span><span class="sxs-lookup"><span data-stu-id="be29c-146">WS-Discovery v1.1 CD1 is the first revision of WS-Discovery to include an explicit description of an HTTP protocol for communication between a proxy and a client or device.</span></span>

<span data-ttu-id="be29c-147">為了限制多播要求中使用的並行版本數目，WSDAPI 會在2005/04 命名空間中傳送 WS-Discovery 探查要求，但會搜尋 WS-Discovery v1.1 CD1 DiscoveryProxy 類型。</span><span class="sxs-lookup"><span data-stu-id="be29c-147">To limit the number of concurrent versions used in multicast requests, WSDAPI sends a WS-Discovery Probe request in the 2005/04 namespace, but searches for the WS-Discovery v1.1 CD1 DiscoveryProxy type.</span></span> <span data-ttu-id="be29c-148">如果 proxy 回應，則 WSDAPI 會將 HTTP 探查或解析要求傳送至指定的 proxy 端點，如 WS-Discovery v1.1 CD1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="be29c-148">If a proxy responds, WSDAPI will send an HTTP Probe or Resolve request to the specified proxy endpoint as defined in WS-Discovery v1.1 CD1.</span></span>

 

 



