---
description: Web 服務的裝置設定檔 (DPWS) 主機和用戶端會透過 UDP 和 HTTP 使用一連串的 SOAP 訊息，透過網路進行通訊。
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: 探索和中繼資料交換訊息模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9a08852c5f25572daf9932afd2ce4b7e03858a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104195696"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a><span data-ttu-id="db523-103">探索和中繼資料交換訊息模式</span><span class="sxs-lookup"><span data-stu-id="db523-103">Discovery and Metadata Exchange Message Patterns</span></span>

<span data-ttu-id="db523-104">Web 服務的裝置設定檔 (DPWS) 主機和用戶端會透過 UDP 和 HTTP 使用一連串的 SOAP 訊息，透過網路進行通訊。</span><span class="sxs-lookup"><span data-stu-id="db523-104">Device Profile for Web Services (DPWS) hosts and clients communicate over the network using a series of SOAP messages over UDP and HTTP.</span></span>

<span data-ttu-id="db523-105">下圖顯示 DPWS 主機與用戶端之間預期的 UDP 和 HTTP 流量的總覽。</span><span class="sxs-lookup"><span data-stu-id="db523-105">The following diagram shows an overview of the expected UDP and HTTP traffic between a DPWS host and client.</span></span>

![此圖顯示 DPWS 主機與用戶端之間的 UDP 和 HTTP 流量。](images/ws-discovery-and-metadata-exchange-message-patterns.png)

<span data-ttu-id="db523-107">在沒有網路請求的情況下，會產生[Hello](hello-message.md)、[再見](bye-message.md)、[探查](probe-message.md)、[解析](resolve-message.md)和[取得](get--metadata-exchange--http-request-and-message.md)訊息;這些訊息是用來宣佈裝置狀態或發出搜尋要求。</span><span class="sxs-lookup"><span data-stu-id="db523-107">[Hello](hello-message.md), [Bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md), and [Get](get--metadata-exchange--http-request-and-message.md) messages are all generated without network solicitation; these messages are used to announce device state or to issue a search request.</span></span> <span data-ttu-id="db523-108">系統會產生[ProbeMatches](probematches-message.md)、 [ResolveMatches](resolvematches-message.md)和[GetResponse](getresponse--metadata-exchange--message.md)訊息，以回應探查、解決和取得訊息。</span><span class="sxs-lookup"><span data-stu-id="db523-108">[ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md), and [GetResponse](getresponse--metadata-exchange--message.md) messages are generated in response to Probe, Resolve and Get messages.</span></span>

<span data-ttu-id="db523-109">[Hello](hello-message.md)、 [再見](bye-message.md)、 [Resolve](resolve-message.md)和 [ResolveMatches](resolvematches-message.md) 訊息一律會透過 UDP 進行。</span><span class="sxs-lookup"><span data-stu-id="db523-109">[Hello](hello-message.md), [Bye](bye-message.md), [Resolve](resolve-message.md), and [ResolveMatches](resolvematches-message.md) messages will always occur over UDP.</span></span> <span data-ttu-id="db523-110">同樣地， [Get](get--metadata-exchange--http-request-and-message.md) 和 [GetResponse](getresponse--metadata-exchange--message.md) 中繼資料訊息一律會透過 HTTP 或 HTTPS 進行。</span><span class="sxs-lookup"><span data-stu-id="db523-110">Similarly, [Get](get--metadata-exchange--http-request-and-message.md) and [GetResponse](getresponse--metadata-exchange--message.md) metadata messages will always occur over HTTP or HTTPS.</span></span> <span data-ttu-id="db523-111">[探查](probe-message.md) 和 [ProbeMatches](probematches-message.md) 訊息通常會透過 UDP 傳輸，但會透過 HTTP 或 HTTPS 連接在導向的探索案例中進行。</span><span class="sxs-lookup"><span data-stu-id="db523-111">[Probe](probe-message.md) and [ProbeMatches](probematches-message.md) messages are normally transmitted over UDP, but take place over an HTTP or HTTPS connection in a directed discovery scenario.</span></span> <span data-ttu-id="db523-112">如需有關導向探索訊息模式的詳細資訊，請參閱 [使用導向探索來疑難排解應用程式](troubleshooting-applications-using-directed-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="db523-112">For more information about directed discovery message patterns, see [Troubleshooting Applications Using Directed Discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="db523-113">下列清單顯示網路上一般的訊息順序。</span><span class="sxs-lookup"><span data-stu-id="db523-113">The following list shows the typical sequence of messages on the wire.</span></span> <span data-ttu-id="db523-114">並非所有的訊息都是強制性的。</span><span class="sxs-lookup"><span data-stu-id="db523-114">Not all messages are mandatory.</span></span>

1.  [<span data-ttu-id="db523-115">您好</span><span class="sxs-lookup"><span data-stu-id="db523-115">Hello</span></span>](hello-message.md)
2.  [<span data-ttu-id="db523-116">探查</span><span class="sxs-lookup"><span data-stu-id="db523-116">Probe</span></span>](probe-message.md)
3.  [<span data-ttu-id="db523-117">ProbeMatches</span><span class="sxs-lookup"><span data-stu-id="db523-117">ProbeMatches</span></span>](probematches-message.md)
4.  [<span data-ttu-id="db523-118">解決</span><span class="sxs-lookup"><span data-stu-id="db523-118">Resolve</span></span>](resolve-message.md)
5.  [<span data-ttu-id="db523-119">ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="db523-119">ResolveMatches</span></span>](resolvematches-message.md)
6.  <span data-ttu-id="db523-120">[取得](get--metadata-exchange--http-request-and-message.md) (中繼資料交換要求) </span><span class="sxs-lookup"><span data-stu-id="db523-120">[Get](get--metadata-exchange--http-request-and-message.md) (metadata exchange request)</span></span>
7.  [<span data-ttu-id="db523-121">GetResponse</span><span class="sxs-lookup"><span data-stu-id="db523-121">GetResponse</span></span>](getresponse--metadata-exchange--message.md)
8.  [<span data-ttu-id="db523-122">再見</span><span class="sxs-lookup"><span data-stu-id="db523-122">Bye</span></span>](bye-message.md)

## <a name="related-topics"></a><span data-ttu-id="db523-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="db523-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db523-124">關於裝置上的 Web 服務</span><span class="sxs-lookup"><span data-stu-id="db523-124">About Web Services on Devices</span></span>](about-web-services-for-devices.md)
</dt> </dl>

 

 



