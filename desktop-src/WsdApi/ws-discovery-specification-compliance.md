---
description: 深入瞭解： WS-Discovery 規格合規性
ms.assetid: b795a385-b48d-4a16-9d91-e48bca120572
title: WS-Discovery 規格合規性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcae062448b1913f0cc62dff3b6c86b98280a902
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386057"
---
# <a name="ws-discovery-specification-compliance"></a><span data-ttu-id="05ced-103">WS-Discovery 規格合規性</span><span class="sxs-lookup"><span data-stu-id="05ced-103">WS-Discovery Specification Compliance</span></span>

<span data-ttu-id="05ced-104">[WS-探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) 說明如何執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="05ced-104">[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) describes how to perform the following tasks:</span></span>

-   <span data-ttu-id="05ced-105">宣佈本機子網上的服務可用性</span><span class="sxs-lookup"><span data-stu-id="05ced-105">Announce the availability of services on the local subnet</span></span>
-   <span data-ttu-id="05ced-106">搜尋子網上的服務</span><span class="sxs-lookup"><span data-stu-id="05ced-106">Search for services on the subnet</span></span>
-   <span data-ttu-id="05ced-107">找出先前參考的服務</span><span class="sxs-lookup"><span data-stu-id="05ced-107">Locate a previously referenced service</span></span>

<span data-ttu-id="05ced-108">為了達成此目的，WS-Discovery 定義 2 1 方向的訊息、 [Hello](hello-message.md) 和 [再見](bye-message.md)，以及兩個雙向搜尋訊息、 [探查](probe-message.md) 和 [解決](resolve-message.md)。</span><span class="sxs-lookup"><span data-stu-id="05ced-108">To accomplish this, WS-Discovery defines two one-way messages, [Hello](hello-message.md) and [Bye](bye-message.md), and two bidirectional search messages, [Probe](probe-message.md) and [Resolve](resolve-message.md).</span></span>

<span data-ttu-id="05ced-109">WS-Discovery 也提供 IPv4 和 IPv6 連結本機探索的位址和保留埠。</span><span class="sxs-lookup"><span data-stu-id="05ced-109">WS-Discovery also provides addresses and a reserved port for IPv4 and IPv6 link local discovery.</span></span> <span data-ttu-id="05ced-110">此規格也可讓您在其他地方定義替代系結，例如在 [Web 服務的裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/) 中定義的 HTTP 系結探查 (DPWS) 。</span><span class="sxs-lookup"><span data-stu-id="05ced-110">The specification also allows for alternate bindings to be defined elsewhere, such as the Probe over HTTP binding defined in the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span>

<span data-ttu-id="05ced-111">WS-Discovery 規格會根據指定的執行建議或限制，使用條款來描述選用功能。</span><span class="sxs-lookup"><span data-stu-id="05ced-111">The WS-Discovery specification describes elective functionality by using the terms MAY or SHOULD in a given implementation recommendation or restriction.</span></span> <span data-ttu-id="05ced-112">省略的功能可能是在不是由 WSDAPI 所執行的 WS-Discovery 規格中所述的功能，也可能是 WSDAPI 在 WS-Discovery 規格中指定的方法中所執行的功能。</span><span class="sxs-lookup"><span data-stu-id="05ced-112">Omitted functionality may be functionality described as REQUIRED in the WS-Discovery specification that was not implemented by WSDAPI, or it may be functionality that WSDAPI implemented in a method other in the one specified in the WS-Discovery specification.</span></span>

<span data-ttu-id="05ced-113">本主題說明如何使用 WSDAPI 執行來處理 WS-Discovery 的限制、需求和選用功能。</span><span class="sxs-lookup"><span data-stu-id="05ced-113">This topic describes how WS-Discovery restrictions, requirements, and elective functionality are handled by the WSDAPI implementation.</span></span> <span data-ttu-id="05ced-114">本主題最適合與 WS-Discovery 規格一起閱讀。</span><span class="sxs-lookup"><span data-stu-id="05ced-114">This topic is best read in tandem with the WS-Discovery specification.</span></span>

## <a name="ws-discovery-and-soap-over-udp-support"></a><span data-ttu-id="05ced-115">WS-Discovery 和 SOAP over UDP 支援</span><span class="sxs-lookup"><span data-stu-id="05ced-115">WS-Discovery and SOAP-over-UDP Support</span></span>

<span data-ttu-id="05ced-116">在 SOAP over UDP 中，第3.2 節指定 UDP 訊息必須符合64K 資料包。</span><span class="sxs-lookup"><span data-stu-id="05ced-116">In SOAP-over-UDP, Section 3.2 specifies that the UDP message must fit in a 64K datagram.</span></span> <span data-ttu-id="05ced-117">WSDAPI 會接受64K 的 UDP 訊息，但是最大 \_ 信封 \_ 大小 (32k) 的 DPWS 條件約束將會限制訊息大小。</span><span class="sxs-lookup"><span data-stu-id="05ced-117">WSDAPI will accept 64K UDP messages, but the DPWS constraint of MAX\_ENVELOPE\_SIZE (32K) will constrain the message size.</span></span> <span data-ttu-id="05ced-118">根據 [WS 探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)的要求，WSDAPI 支援第4節所述的訊息模式。</span><span class="sxs-lookup"><span data-stu-id="05ced-118">As required by [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf), WSDAPI supports the message patterns described in Section 4.</span></span>

<span data-ttu-id="05ced-119">您可以將 WSDAPI 設定為支援區段7和8中的安全性模型。</span><span class="sxs-lookup"><span data-stu-id="05ced-119">WSDAPI may be configured to support the security model in Sections 7 and 8.</span></span> <span data-ttu-id="05ced-120">當設定時，WSDAPI 會將輸出 WS-Discovery 的訊息簽章，並驗證輸入訊息上的簽章。</span><span class="sxs-lookup"><span data-stu-id="05ced-120">When so configured, WSDAPI will sign outbound WS-Discovery messages and will validate signatures on inbound messages.</span></span>

<span data-ttu-id="05ced-121">WSDAPI 會實 DPWS 附錄 I 修改過的附錄 I 中所定義的重新傳輸演算法。</span><span class="sxs-lookup"><span data-stu-id="05ced-121">WSDAPI implements the retransmission algorithm defined in Appendix I as amended by DPWS Appendix I.</span></span>

<span data-ttu-id="05ced-122">在 WS-Discovery 中，WSDAPI 會使用2.4 節中指定的位址。</span><span class="sxs-lookup"><span data-stu-id="05ced-122">In WS-Discovery, WSDAPI uses the addresses specified in section 2.4.</span></span> <span data-ttu-id="05ced-123">WSDAPI \_ 會將應用程式最大 \_ 延遲從區段2.4 延伸，而不是 DPWS 附錄 I 中所定義的範圍。如需應用程式 \_ 最大延遲的詳細資訊 \_ ，請參閱 [其他 WS-Discovery 功能](additional-ws-discovery-functionality.md)。</span><span class="sxs-lookup"><span data-stu-id="05ced-123">WSDAPI extends APP\_MAX\_DELAY from section 2.4, but not to the extent as defined in DPWS Appendix I. For more information about APP\_MAX\_DELAY, see [Additional WS-Discovery Functionality](additional-ws-discovery-functionality.md).</span></span>

<span data-ttu-id="05ced-124">WS-Discovery 描述 `uuid:` 2.6 節中的 URI 格式建議，但 WSDAPI 會覆寫這項建議。</span><span class="sxs-lookup"><span data-stu-id="05ced-124">WS-Discovery describes the `uuid:` URI format recommendation in section 2.6, but WSDAPI overrides this recommendation.</span></span> <span data-ttu-id="05ced-125">相反地，WSDAPI 會使用 `urn:uuid:` DPWS 中所述的 URI 格式。</span><span class="sxs-lookup"><span data-stu-id="05ced-125">Instead, WSDAPI uses the `urn:uuid:` URI format described in DPWS.</span></span>

<span data-ttu-id="05ced-126">WS-Discovery 的第3節描述用戶端如何與探索 proxy 互動。</span><span class="sxs-lookup"><span data-stu-id="05ced-126">Section 3 of WS-Discovery describes how a client interacts with a discovery proxy.</span></span> <span data-ttu-id="05ced-127">WSDAPI 無法辨識此互動，並且會忽略來自探索 proxy 的宣告。</span><span class="sxs-lookup"><span data-stu-id="05ced-127">WSDAPI does not recognize this interaction and ignores announcements from discovery proxies.</span></span> <span data-ttu-id="05ced-128">在 Windows 7 中，WSDAPI 會對 WS-Discovery 通訊協定（WS-Discovery 遠端擴充功能）執行私用延伸，以允許探索用戶端藉由將要求傳送至集中式 proxy 來搜尋分散于許多不同網路的服務。如需詳細資訊，請參閱 [其他 WS-Discovery 功能](additional-ws-discovery-functionality.md)。</span><span class="sxs-lookup"><span data-stu-id="05ced-128">In Windows 7, WSDAPI implements a private extension to the WS-Discovery protocol, WS-Discovery Remote Extensions, to allow discovery clients to search for services spread across many different networks by sending requests to centralized proxies.For more information, see [Additional WS-Discovery Functionality](additional-ws-discovery-functionality.md).</span></span>

<span data-ttu-id="05ced-129">4.1 第3節的 WS-Discovery 要求在傳送 [Hello](hello-message.md) 訊息之前必須先經過一段計時器。</span><span class="sxs-lookup"><span data-stu-id="05ced-129">Section 4.1, paragraph 3 of WS-Discovery requires that a timer must elapse before a [Hello](hello-message.md) message is sent.</span></span> <span data-ttu-id="05ced-130">裝載 API 不會在傳送 Hello 訊息之前等候。</span><span class="sxs-lookup"><span data-stu-id="05ced-130">The hosting API does not wait before sending a Hello message.</span></span> <span data-ttu-id="05ced-131">如果案例需要延遲才能傳送 Hello 訊息，則應用程式開發人員必須執行等候。</span><span class="sxs-lookup"><span data-stu-id="05ced-131">If a scenario requires a delay before a Hello message is sent, then the application developer must implement a wait.</span></span>

<span data-ttu-id="05ced-132">WSDAPI 會執行 WS-Discovery 節4、5和6中所述的所有訊息。</span><span class="sxs-lookup"><span data-stu-id="05ced-132">WSDAPI implements all of the messages described in WS-Discovery Sections 4, 5, and 6.</span></span> <span data-ttu-id="05ced-133">WSDAPI 也會強制執行 \_ DPWS 附錄 I 所修改的第7節中所述的比對超時。 WSDAPI 只會防止從第9節的安全考慮進行「重新執行」。</span><span class="sxs-lookup"><span data-stu-id="05ced-133">WSDAPI also enforces the MATCH\_TIMEOUT described in Section 7 as amended by DPWS Appendix I. WSDAPI only protects against "Replay" from the secure considerations in Section 9.</span></span>

<span data-ttu-id="05ced-134">WSDAPI 會依照 WS-Discovery 附錄 I 中所述的方式來執行應用程式排序。</span><span class="sxs-lookup"><span data-stu-id="05ced-134">WSDAPI does implement application sequencing as described in WS-Discovery Appendix I.</span></span>

 

 



