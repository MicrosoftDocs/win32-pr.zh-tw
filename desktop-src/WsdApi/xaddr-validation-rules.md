---
description: ProbeMatches 和 ResolveMatches 訊息中包含的傳輸位址 (XAddrs) ，會在 WSDAPI 傳送 HTTP 訊息（例如中繼資料要求）之前，受到基本驗證的要求。
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: XAddr 驗證規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc91ce8a0e1bba267ea92fa79a6680b481297f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192047"
---
# <a name="xaddr-validation-rules"></a><span data-ttu-id="6be96-103">XAddr 驗證規則</span><span class="sxs-lookup"><span data-stu-id="6be96-103">XAddr Validation Rules</span></span>

<span data-ttu-id="6be96-104">[ProbeMatches](probematches-message.md)和[ResolveMatches](resolvematches-message.md)訊息中包含的傳輸位址 (XAddrs) ，會在 WSDAPI 傳送 HTTP 訊息（例如中繼資料要求）之前，受到基本驗證的要求。</span><span class="sxs-lookup"><span data-stu-id="6be96-104">Transport addresses (XAddrs) included in [ProbeMatches](probematches-message.md) and [ResolveMatches](resolvematches-message.md) messages are subject to basic validation before WSDAPI sends an HTTP message, such as a metadata request.</span></span>

<span data-ttu-id="6be96-105">這是為了確保 XAddrs 與用戶端位於相同的子網上。</span><span class="sxs-lookup"><span data-stu-id="6be96-105">This is in order to ensure that the XAddrs are on the same subnet as the client.</span></span>

<span data-ttu-id="6be96-106">下列 XML 會顯示範例 XAddrs 元素。</span><span class="sxs-lookup"><span data-stu-id="6be96-106">The following XML shows a sample XAddrs element.</span></span> <span data-ttu-id="6be96-107">Wsd 前置詞是指命名空間 `https://schemas.xmlsoap.org/ws/2005/04/discovery` 。</span><span class="sxs-lookup"><span data-stu-id="6be96-107">The wsd prefix refers to the namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery`.</span></span>

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

<span data-ttu-id="6be96-108">必須符合下列所有條件，HTTP 訊息才能透過網路傳送。</span><span class="sxs-lookup"><span data-stu-id="6be96-108">All of the following conditions must be met before the HTTP message will go out over the wire.</span></span>

-   <span data-ttu-id="6be96-109">XAddrs 必須是 HTTP 或 HTTPS 位址。</span><span class="sxs-lookup"><span data-stu-id="6be96-109">XAddrs must be HTTP or HTTPS addresses.</span></span> <span data-ttu-id="6be96-110">系統會忽略其他架構的 XAddrs。</span><span class="sxs-lookup"><span data-stu-id="6be96-110">XAddrs of other schemes are ignored.</span></span>
-   <span data-ttu-id="6be96-111">如果有任何 HTTPS XAddrs，則所有 XAddrs 都必須是 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="6be96-111">If any HTTPS XAddrs are present, all XAddrs must be HTTPS.</span></span> <span data-ttu-id="6be96-112">包含 HTTP 和 HTTPS 位址的 XAddr 區段都是完全忽略的。</span><span class="sxs-lookup"><span data-stu-id="6be96-112">XAddr sections which include both HTTP and HTTPS addresses are completely ignored.</span></span> <span data-ttu-id="6be96-113">此外，裝置的端點位址必須完全符合 HTTPS XAddrs。</span><span class="sxs-lookup"><span data-stu-id="6be96-113">Additionally, the device's endpoint address must match the HTTPS XAddrs exactly.</span></span>
-   <span data-ttu-id="6be96-114">XAddrs 必須是可透過 DNS 解析的 IP 位址或主機名稱。</span><span class="sxs-lookup"><span data-stu-id="6be96-114">XAddrs must be IP addresses or hostnames resolvable through DNS.</span></span> <span data-ttu-id="6be96-115">通常會使用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6be96-115">Usually, IP addresses are used.</span></span>
-   <span data-ttu-id="6be96-116">XAddrs (中至少有一個 IP 位址，或從 XAddrs) 中所包含之主機名稱解析的 IP 位址，必須與接收 [ProbeMatches](probematches-message.md) 或 [ResolveMatches](resolvematches-message.md) 訊息的介面卡位於相同的子網中。</span><span class="sxs-lookup"><span data-stu-id="6be96-116">At least one IP address included in the XAddrs (or IP address resolved from a hostname included in the XAddrs) must be on the same subnet as the adapter over which the [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message was received.</span></span>
-   <span data-ttu-id="6be96-117">第一個 XAddr 中指定的位址和埠必須是可存取的。</span><span class="sxs-lookup"><span data-stu-id="6be96-117">The address and port specified in the first XAddr must be accessible.</span></span> <span data-ttu-id="6be96-118">在建立 HTTP 連線時，WSDAPI 會嘗試連接到此位址。</span><span class="sxs-lookup"><span data-stu-id="6be96-118">WSDAPI attempts to connect to this address when establishing an HTTP connection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6be96-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="6be96-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6be96-120">ProbeMatches</span><span class="sxs-lookup"><span data-stu-id="6be96-120">ProbeMatches</span></span>](probematches-message.md)
</dt> <dt>

[<span data-ttu-id="6be96-121">ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="6be96-121">ResolveMatches</span></span>](resolvematches-message.md)
</dt> <dt>

[<span data-ttu-id="6be96-122">探索和中繼資料交換訊息模式</span><span class="sxs-lookup"><span data-stu-id="6be96-122">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



