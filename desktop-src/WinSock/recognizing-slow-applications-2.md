---
description: 本指南將應用程式的效能降低為 Microsoft Windows 應用程式，且效能受損。
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: 辨識緩慢的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07be9484a3b08951b8b64989757459531ff72906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988379"
---
# <a name="recognizing-slow-applications"></a><span data-ttu-id="f50a9-103">辨識緩慢的應用程式</span><span class="sxs-lookup"><span data-stu-id="f50a9-103">Recognizing Slow Applications</span></span>

<span data-ttu-id="f50a9-104">本指南將應用程式的效能 *降低* 為 Microsoft Windows 應用程式，且效能受損。</span><span class="sxs-lookup"><span data-stu-id="f50a9-104">This guide identifies a *slow* application as a Microsoft Windows application with impaired performance.</span></span> <span data-ttu-id="f50a9-105">緩慢的應用程式會展示下列一或多個徵兆：</span><span class="sxs-lookup"><span data-stu-id="f50a9-105">A slow application exhibits one or more of the following symptoms:</span></span>

-   <span data-ttu-id="f50a9-106">CPU 和網路使用率偏低。</span><span class="sxs-lookup"><span data-stu-id="f50a9-106">CPU and network utilization are low.</span></span>

    <span data-ttu-id="f50a9-107">電腦似乎正在等待一些東西。</span><span class="sxs-lookup"><span data-stu-id="f50a9-107">The computer appears to be waiting on something.</span></span> <span data-ttu-id="f50a9-108">通常，應用程式會在網路上等候。</span><span class="sxs-lookup"><span data-stu-id="f50a9-108">Often, the application is waiting on the network.</span></span>

-   <span data-ttu-id="f50a9-109">透過 TCP \_ NODELAY 通訊端選項關閉 Nagle 演算法可提高效能。</span><span class="sxs-lookup"><span data-stu-id="f50a9-109">Turning off the Nagle Algorithm through the TCP\_NODELAY socket option increases performance.</span></span>

    <span data-ttu-id="f50a9-110">這表示其他問題，且不應視為解決方案。</span><span class="sxs-lookup"><span data-stu-id="f50a9-110">This indicates other problems, and should not be considered a solution.</span></span> <span data-ttu-id="f50a9-111">關閉 Nagle 演算法會增加通訊協定額外負荷。</span><span class="sxs-lookup"><span data-stu-id="f50a9-111">Turning off the Nagle algorithm increases the protocol overhead.</span></span> <span data-ttu-id="f50a9-112">請勿使用這個方法來修正中斷的應用程式，只是表示應用程式需要其他工作來修正效能問題。</span><span class="sxs-lookup"><span data-stu-id="f50a9-112">Do not use this method as a fix for the broken applications—only as an indication the application needs other work to fix performance issues.</span></span>

-   <span data-ttu-id="f50a9-113">應用程式展現高負荷。</span><span class="sxs-lookup"><span data-stu-id="f50a9-113">The application exhibits high overhead.</span></span>

    <span data-ttu-id="f50a9-114">若要計算您的應用程式額外負荷，請判斷您想要在每個方向傳輸多少資料。</span><span class="sxs-lookup"><span data-stu-id="f50a9-114">To calculate your applications overhead, determine how much data you intended to transfer in each direction.</span></span> <span data-ttu-id="f50a9-115">然後，針對每個連線使用 Netstat，並為每個封包和500位元組新增 Ethernet 的 () 60 個位元組。</span><span class="sxs-lookup"><span data-stu-id="f50a9-115">Then use Netstat and add (for Ethernet) 60 bytes for each packet and 500 bytes for each connection.</span></span> <span data-ttu-id="f50a9-116">透過乙太網路進行串流處理所預期的最大負擔大約是6%。</span><span class="sxs-lookup"><span data-stu-id="f50a9-116">The best overhead that can be expected for streaming over Ethernet is approximately 6%.</span></span> <span data-ttu-id="f50a9-117">針對數據機連線，最大的負擔大約是2%，因為 PPP 連結使用標頭壓縮。</span><span class="sxs-lookup"><span data-stu-id="f50a9-117">For a modem connection, the best overhead is approximately 2%, due to the fact that a PPP link uses header compression.</span></span> <span data-ttu-id="f50a9-118">如需詳細資訊，請參閱 [使用 Netstat 計算額外負荷](calculating-overhead-with-netstat-2.md) 。</span><span class="sxs-lookup"><span data-stu-id="f50a9-118">See [Calculating Overhead with Netstat](calculating-overhead-with-netstat-2.md) for more information.</span></span>

-   <span data-ttu-id="f50a9-119">當連接的 RTT 很大時，應用程式回應會變慢。</span><span class="sxs-lookup"><span data-stu-id="f50a9-119">Application response slows when the connection has a large RTT.</span></span>

    <span data-ttu-id="f50a9-120">假設應用程式未接近連結的頻寬，則大型 RTT 應該很少或沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="f50a9-120">Assuming the application is not approaching the link's bandwidth, a large RTT should have little or no effect.</span></span> <span data-ttu-id="f50a9-121">大型 RTT 的明顯減緩是序列化處理和許多小型交易的明確符號。</span><span class="sxs-lookup"><span data-stu-id="f50a9-121">A dramatic slowdown with a large RTT is a clear sign of serialized processing and many small transactions.</span></span>

<span data-ttu-id="f50a9-122">每個應用程式都應該在具有大型 RTT 的環境中進行測試。</span><span class="sxs-lookup"><span data-stu-id="f50a9-122">Every application should be tested in an environment with a large RTT.</span></span> <span data-ttu-id="f50a9-123">這麼做會顯示從不佳的開發選項中遭遇的大部分應用程式。</span><span class="sxs-lookup"><span data-stu-id="f50a9-123">Doing so reveals most applications that suffer from poor development choices.</span></span> <span data-ttu-id="f50a9-124">這項測試可以在數種環境下執行，包括無線區域網路網路、連結延遲模擬器或衛星網路。</span><span class="sxs-lookup"><span data-stu-id="f50a9-124">This testing can be performed in several environments, including a wireless LAN network, a link-delay simulator, or a satellite network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f50a9-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="f50a9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f50a9-126">應用程式行為</span><span class="sxs-lookup"><span data-stu-id="f50a9-126">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="f50a9-127">高效能的 Windows 通訊端應用程式</span><span class="sxs-lookup"><span data-stu-id="f50a9-127">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="f50a9-128">Nagle 演算法</span><span class="sxs-lookup"><span data-stu-id="f50a9-128">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



