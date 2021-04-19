---
description: 某些程式設計技術會遇到與 TCP/IP 執行連結的效能問題。
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: TCP/IP 特定問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9a7334471d3e419830eb054399ff1dcb721cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991873"
---
# <a name="tcpip-specific-issues"></a><span data-ttu-id="95bb6-103">TCP/IP 特定問題</span><span class="sxs-lookup"><span data-stu-id="95bb6-103">TCP/IP-specific Issues</span></span>

<span data-ttu-id="95bb6-104">某些程式設計技術會遇到與 TCP/IP 執行連結的效能問題。</span><span class="sxs-lookup"><span data-stu-id="95bb6-104">Certain programming techniques run into performance issues that are linked to the implementation of TCP/IP.</span></span> <span data-ttu-id="95bb6-105">這類效能問題不會建議 TCP/IP 沒有效率或效能瓶頸;相反地，當無法理解 TCP/IP 作業時，就會看到這些問題。</span><span class="sxs-lookup"><span data-stu-id="95bb6-105">Such performance issues do not suggest that TCP/IP is inefficient or a performance bottleneck; rather, these issues are seen when TCP/IP operations are not understood.</span></span>

<span data-ttu-id="95bb6-106">下列問題指出 TCP/IP 作業與網路應用程式開發選擇的組合會導致效能不佳的常見案例。</span><span class="sxs-lookup"><span data-stu-id="95bb6-106">The following issues identify common scenarios in which the combination of TCP/IP operation and network application development choices result in poor performance.</span></span>

-   <span data-ttu-id="95bb6-107">連接繁重的應用程式。</span><span class="sxs-lookup"><span data-stu-id="95bb6-107">Connect-heavy Applications.</span></span>

    <span data-ttu-id="95bb6-108">某些應用程式會為每個交易具現化新的 TCP 連接。</span><span class="sxs-lookup"><span data-stu-id="95bb6-108">Some applications instantiate a new TCP connection for each transaction.</span></span> <span data-ttu-id="95bb6-109">TCP 連線建立需要一些時間、額外的 RTTs，而且會受到緩慢的啟動。</span><span class="sxs-lookup"><span data-stu-id="95bb6-109">TCP connection establishment takes time, contributes extra RTTs, and is subject to slow-start.</span></span> <span data-ttu-id="95bb6-110">此外，關閉的連線會受時間等候，這會耗用系統資源。</span><span class="sxs-lookup"><span data-stu-id="95bb6-110">In addition, the closed connections are subject to TIME-WAIT, which consumes system resources.</span></span>

    <span data-ttu-id="95bb6-111">連接繁重的應用程式大多很常見，因為它們很容易建立;測試和錯誤處理非常簡單。</span><span class="sxs-lookup"><span data-stu-id="95bb6-111">Connect-heavy applications are common largely because they are easy to create; testing and error handling is very simple.</span></span> <span data-ttu-id="95bb6-112">在持續連線上偵測錯誤可能需要相當多的程式碼和精力，因此有時不會完成。</span><span class="sxs-lookup"><span data-stu-id="95bb6-112">Detecting faults on a persistent connection can take considerable code and effort, and therefore is sometimes not completed.</span></span>

    <span data-ttu-id="95bb6-113">重複使用 TCP 連線來解決這種情況。</span><span class="sxs-lookup"><span data-stu-id="95bb6-113">Remedy this situation by reusing the TCP connection.</span></span> <span data-ttu-id="95bb6-114">這可能會導致透過 TCP 連接進行序列化，除非交易是透過多個連接進行多工處理。</span><span class="sxs-lookup"><span data-stu-id="95bb6-114">This may cause serialization over the TCP connection unless the transactions are multiplexed over multiple connections.</span></span> <span data-ttu-id="95bb6-115">如果採取這種方式，連接數目應限制為兩個，而且需要應用層框架和先進的錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="95bb6-115">If this approach is taken, the number of connections should be limited to two, and application-layer framing and advanced error handling are required.</span></span>

-   <span data-ttu-id="95bb6-116">零長度的傳送緩衝區和封鎖傳送。</span><span class="sxs-lookup"><span data-stu-id="95bb6-116">Zero-length Send Buffers and Blocking Sends.</span></span>

    <span data-ttu-id="95bb6-117">藉由使用 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數設定傳送緩衝區來關閉緩衝處理 (如此 \_ SNDBUF) 為零，就類似于關閉磁碟快取。</span><span class="sxs-lookup"><span data-stu-id="95bb6-117">Turning off buffering by using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set the send buffer (SO\_SNDBUF) to zero is similar to turning off disk caching.</span></span> <span data-ttu-id="95bb6-118">將傳送緩衝區設定為零併發出封鎖傳送時，應用程式有50% 的機會達到200毫秒的延遲通知。</span><span class="sxs-lookup"><span data-stu-id="95bb6-118">When setting the send buffer to zero and issuing blocking sends, an application has a fifty percent chance of hitting a 200-millisecond delayed acknowledgment.</span></span>

    <span data-ttu-id="95bb6-119">除非您已考慮所有網路環境的影響，否則請勿關閉傳送緩衝處理。</span><span class="sxs-lookup"><span data-stu-id="95bb6-119">Do not turn off send buffering unless you have considered the impact in all network environments.</span></span> <span data-ttu-id="95bb6-120">其中一個例外狀況：使用重迭 i/o 的串流資料應該將傳送緩衝區設定為零。</span><span class="sxs-lookup"><span data-stu-id="95bb6-120">One exception: streaming data using overlapped I/O should set the send buffer to zero.</span></span>

-   <span data-ttu-id="95bb6-121">傳送-傳送-接收程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="95bb6-121">Send-Send-Receive programming model.</span></span>

    <span data-ttu-id="95bb6-122">將應用程式結構化以執行傳送傳送接收，會增加您遇到 Nagle 演算法的機率，而導致 RTT 的延遲 + 200 毫秒。</span><span class="sxs-lookup"><span data-stu-id="95bb6-122">Structuring an application to perform send-send-receives increases your chances of encountering the Nagle Algorithm, which causes a delay of RTT+200 ms.</span></span> <span data-ttu-id="95bb6-123">如果最後一次傳送小於 TCP 最大區段大小 (MSS、單一資料包中的最大資料) ，可能會遇到 Nagle 演算法。</span><span class="sxs-lookup"><span data-stu-id="95bb6-123">The Nagle Algorithm may be encountered if the last send is less than the TCP Maximum Segment Size (MSS, the maximum data in a single datagram).</span></span> <span data-ttu-id="95bb6-124">MSS 可以是較大的值 (64K 在 IPv4 中，甚至更大的 IPv6) ，因此不會計入通常小的 MSS。</span><span class="sxs-lookup"><span data-stu-id="95bb6-124">MSS can be a very large value (64K in IPv4, and even larger in IPv6), so do not count on a typically small MSS.</span></span> <span data-ttu-id="95bb6-125">更好的選擇是使用 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) 或 **memcpy** 函式，將這兩個傳送合併成單一傳送。</span><span class="sxs-lookup"><span data-stu-id="95bb6-125">A better option is to combine the two sends into a single send using the [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) or **memcpy** function.</span></span>

-   <span data-ttu-id="95bb6-126">大量的同時連線。</span><span class="sxs-lookup"><span data-stu-id="95bb6-126">Large Number of Simultaneous Connections.</span></span>

    <span data-ttu-id="95bb6-127">除了特殊用途的應用程式之外，並行連接不應超過二。</span><span class="sxs-lookup"><span data-stu-id="95bb6-127">Concurrent connections should not exceed two, except in special purpose applications.</span></span> <span data-ttu-id="95bb6-128">超過兩個並行連接會導致資源浪費。</span><span class="sxs-lookup"><span data-stu-id="95bb6-128">Exceeding two concurrent connections results in wasted resources.</span></span> <span data-ttu-id="95bb6-129">理想的規則是有最多四個短暫的連接，或每個目的地有兩個持續連線。</span><span class="sxs-lookup"><span data-stu-id="95bb6-129">A good rule is to have up to four short lived connections, or two persistent connections per destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95bb6-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="95bb6-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95bb6-131">應用程式行為</span><span class="sxs-lookup"><span data-stu-id="95bb6-131">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="95bb6-132">高效能的 Windows 通訊端應用程式</span><span class="sxs-lookup"><span data-stu-id="95bb6-132">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="95bb6-133">Nagle 演算法</span><span class="sxs-lookup"><span data-stu-id="95bb6-133">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



