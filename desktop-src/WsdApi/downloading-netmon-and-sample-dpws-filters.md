---
description: Microsoft 網路監視器 3 (Netmon) 是用來檢查網路流量的封包分析器。
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: 下載 Netmon 和範例 DPWS 篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47790b26164ec0ed2792d1d1e1f2ad4ba5d77d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996673"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a><span data-ttu-id="9a517-103">下載 Netmon 和範例 DPWS 篩選器</span><span class="sxs-lookup"><span data-stu-id="9a517-103">Downloading Netmon and Sample DPWS Filters</span></span>

<span data-ttu-id="9a517-104">Microsoft 網路監視器 3 (Netmon) 是用來檢查網路流量的封包分析器。</span><span class="sxs-lookup"><span data-stu-id="9a517-104">Microsoft Network Monitor 3 (Netmon) is a packet analyzer used to inspect network traffic.</span></span> <span data-ttu-id="9a517-105">必須先下載 Netmon，才能 [檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md) ，以及 [檢查是否可以遵循 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md) 。</span><span class="sxs-lookup"><span data-stu-id="9a517-105">Netmon must be downloaded before the troubleshooting steps given in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) can be followed.</span></span> <span data-ttu-id="9a517-106">下載 Netmon 之後，您可以使用 DPWS 篩選器來協助找出感興趣的流量。</span><span class="sxs-lookup"><span data-stu-id="9a517-106">After Netmon has been downloaded, DPWS filters can be used to help isolate traffic of interest.</span></span>

## <a name="downloading-netmon"></a><span data-ttu-id="9a517-107">下載 Netmon</span><span class="sxs-lookup"><span data-stu-id="9a517-107">Downloading Netmon</span></span>

<span data-ttu-id="9a517-108">若要下載 Netmon，請移至 [Microsoft 網路監視器](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) 並依照指示進行。</span><span class="sxs-lookup"><span data-stu-id="9a517-108">To download Netmon, go to [Microsoft Network Monitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) and follow the instructions.</span></span> <span data-ttu-id="9a517-109">如需有關 Netmon 的詳細資訊，請參閱 [說明及支援] 知識庫中的「網路監視器3.0 的相關資訊」 [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) 。</span><span class="sxs-lookup"><span data-stu-id="9a517-109">For more information about Netmon, see "Information about Network Monitor 3.0" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

## <a name="sample-dpws-filters"></a><span data-ttu-id="9a517-110">範例 DPWS 篩選</span><span class="sxs-lookup"><span data-stu-id="9a517-110">Sample DPWS Filters</span></span>

<span data-ttu-id="9a517-111">有時候，WS-Discovery 和中繼資料交換疑難排解必須在忙碌的網路上進行。</span><span class="sxs-lookup"><span data-stu-id="9a517-111">Sometimes, WS-Discovery and metadata exchange troubleshooting must take place on a busy network.</span></span> <span data-ttu-id="9a517-112">範例篩選可以用來協助將 Netmon 輸出限制為感興趣的流量。</span><span class="sxs-lookup"><span data-stu-id="9a517-112">The sample filters can be used to help limit the Netmon output to traffic of interest.</span></span> <span data-ttu-id="9a517-113">如需有關使用 Netmon 篩選器的詳細資訊，請參閱 [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) 。</span><span class="sxs-lookup"><span data-stu-id="9a517-113">For more information about using Netmon filters, see [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

<span data-ttu-id="9a517-114">下列範例顯示的篩選準則會將輸出限制為所有廣播 WS-Discovery 流量。</span><span class="sxs-lookup"><span data-stu-id="9a517-114">The following example shows a filter that limits output to all broadcast WS-Discovery traffic.</span></span>

> [!Note]  
> <span data-ttu-id="9a517-115">此篩選不會從堆疊中找出未回應源自埠3702之多播 WS-Discovery 訊息的流量。</span><span class="sxs-lookup"><span data-stu-id="9a517-115">This filter does not capture traffic from stacks that do not respond to multicast WS-Discovery messages that originate at port 3702.</span></span> <span data-ttu-id="9a517-116">如果使用這類堆疊，則必須先修改此範例篩選器再使用。</span><span class="sxs-lookup"><span data-stu-id="9a517-116">If such a stack is being used, then this sample filter must be modified before use.</span></span>

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

<span data-ttu-id="9a517-117">下列範例顯示的篩選準則會將輸出限制為預設埠上傳送至 WSDAPI 堆疊的 HTTP 訊息。</span><span class="sxs-lookup"><span data-stu-id="9a517-117">The following example shows a filter that limits output to HTTP messages sent to WSDAPI stacks on the default port.</span></span>

> [!Note]  
> <span data-ttu-id="9a517-118">服務可能會從5357以外的埠傳送相關的 HTTP 訊息。</span><span class="sxs-lookup"><span data-stu-id="9a517-118">Services may send relevant HTTP messages from ports other than 5357.</span></span> <span data-ttu-id="9a517-119">如果有興趣來自其他埠的流量，則必須先修改此範例篩選器再使用。</span><span class="sxs-lookup"><span data-stu-id="9a517-119">If traffic from other ports is of interest, then this sample filter must be modified before use.</span></span>

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

<span data-ttu-id="9a517-120">下列範例顯示的篩選準則會將輸出限制為 IPv4 多播流量。</span><span class="sxs-lookup"><span data-stu-id="9a517-120">The following example shows a filter that limits output to IPv4 multicast traffic.</span></span>

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

<span data-ttu-id="9a517-121">下列範例顯示的篩選準則會將輸出限制為 IPv6 多播流量。</span><span class="sxs-lookup"><span data-stu-id="9a517-121">The following example shows a filter that limits output to IPv6 multicast traffic.</span></span>

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

<span data-ttu-id="9a517-122">某些篩選準則可以合併以進一步限制結果。</span><span class="sxs-lookup"><span data-stu-id="9a517-122">Some filters can be combined to further limit results.</span></span> <span data-ttu-id="9a517-123">下列範例顯示的篩選準則會將輸出限制為 IPv4 多播 WS-Discovery 流量。</span><span class="sxs-lookup"><span data-stu-id="9a517-123">The following example shows a filter that limits output to IPv4 multicast WS-Discovery traffic.</span></span>

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

<span data-ttu-id="9a517-124">使用這些篩選器時，可能會從 Netmon 結果中排除相關的流量。</span><span class="sxs-lookup"><span data-stu-id="9a517-124">When these filters are used, relevant traffic may be excluded from the Netmon results.</span></span> <span data-ttu-id="9a517-125">當服務位於預設埠以外的埠（ (5357/5358) ，以及當 DPWS 堆疊未使用預設通訊埠回應訊息時，就會發生排除情形。</span><span class="sxs-lookup"><span data-stu-id="9a517-125">Exclusion can occur when services reside at ports other than the default ports (5357/5358) and when a DPWS stack does not respond to messages using the default port.</span></span> <span data-ttu-id="9a517-126">在這些情況下，必須在使用之前修改篩選。</span><span class="sxs-lookup"><span data-stu-id="9a517-126">In these cases, the filters must be modified before use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a517-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="9a517-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a517-128">WSDAPI 診斷程式</span><span class="sxs-lookup"><span data-stu-id="9a517-128">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="9a517-129">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="9a517-129">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



