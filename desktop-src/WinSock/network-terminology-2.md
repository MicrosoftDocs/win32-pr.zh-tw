---
description: 計量可用來測量網路和通訊協定效能的各個層面。
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: " (Windows 通訊端 2) 的網路術語"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690387"
---
# <a name="network-terminology-windows-sockets-2"></a><span data-ttu-id="c401f-103"> (Windows 通訊端 2) 的網路術語</span><span class="sxs-lookup"><span data-stu-id="c401f-103">Network Terminology (Windows Sockets 2)</span></span>

<span data-ttu-id="c401f-104">計量可用來測量網路和通訊協定效能的各個層面。</span><span class="sxs-lookup"><span data-stu-id="c401f-104">Metrics are used to measure aspects of network and protocol performance.</span></span> <span data-ttu-id="c401f-105">在各種案例中，這類計量的值會指出網路應用程式的效能層級。</span><span class="sxs-lookup"><span data-stu-id="c401f-105">The values for such metrics in various scenarios indicate the level of performance of a network application.</span></span> <span data-ttu-id="c401f-106">本章節定義了業界廣泛用來測量網路應用程式效能的詞彙和計量。</span><span class="sxs-lookup"><span data-stu-id="c401f-106">This section defines terms and metrics used industry-wide for measuring network application performance.</span></span> <span data-ttu-id="c401f-107">本指南的其餘部分會使用這些詞彙。</span><span class="sxs-lookup"><span data-stu-id="c401f-107">These terms are used throughout the rest of this guide.</span></span>

-   <span data-ttu-id="c401f-108">來回行程時間 (RTT) </span><span class="sxs-lookup"><span data-stu-id="c401f-108">Round Trip Time (RTT)</span></span>

    <span data-ttu-id="c401f-109">從來源電腦到目的地電腦的往返要求的時間（以毫秒為單位），然後重新執行。</span><span class="sxs-lookup"><span data-stu-id="c401f-109">Time, in milliseconds, for a request to make a trip from a source computer to a destination computer, and back again.</span></span> <span data-ttu-id="c401f-110">較低的值表示效能較佳。</span><span class="sxs-lookup"><span data-stu-id="c401f-110">Lower values indicate better performance.</span></span> <span data-ttu-id="c401f-111">轉寄和傳回路徑時間不一定相等。</span><span class="sxs-lookup"><span data-stu-id="c401f-111">Forward and return path times are not necessarily equal.</span></span>

    <span data-ttu-id="c401f-112">RTT 值會受到網路基礎結構、節點與網路條件之間的距離，以及封包大小的影響。</span><span class="sxs-lookup"><span data-stu-id="c401f-112">RTT values are affected by network infrastructure, distance between nodes, network conditions, and packet size.</span></span> <span data-ttu-id="c401f-113">當針對低速連結（例如撥號連線）測量時，封包大小、擁塞和承載 compressibility 會影響 RTT。</span><span class="sxs-lookup"><span data-stu-id="c401f-113">Packet size, congestion and payload compressibility impact RTT when measured on slow links, such as dial-up connections.</span></span> <span data-ttu-id="c401f-114">其他因素會影響 RTT，包括轉寄錯誤修正和資料壓縮，這會導入增加 RTT 的緩衝區和佇列，因此會降低效能。</span><span class="sxs-lookup"><span data-stu-id="c401f-114">Other factors affect RTT, including forward error correction and data compression, which introduce buffers and queues that increase RTT, and therefore decrease performance.</span></span>

-   <span data-ttu-id="c401f-115">Goodput</span><span class="sxs-lookup"><span data-stu-id="c401f-115">Goodput</span></span>

    <span data-ttu-id="c401f-116">接收者成功處理的實用應用程式資料量（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="c401f-116">Measure of useful application data successfully processed by the receiver, in bits-per-second.</span></span> <span data-ttu-id="c401f-117">Goodput 可測量有效或實用的輸送量，並只包含應用程式資料;封包、通訊協定和媒體標頭會被視為額外負荷，而且不是 goodput 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c401f-117">Goodput enables the measurement of effective or useful throughput and includes only application data; packet, protocol, and media headers are considered overhead, and are not part of goodput.</span></span>

-   <span data-ttu-id="c401f-118">通訊協定額外負荷</span><span class="sxs-lookup"><span data-stu-id="c401f-118">Protocol Overhead</span></span>

    <span data-ttu-id="c401f-119">Nonapplication 的位元組，包括通訊協定和媒體框架，除以傳輸的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="c401f-119">Nonapplication bytes, including protocol and media framing, divided by the total number of bytes transmitted.</span></span> <span data-ttu-id="c401f-120">此值以百分比表示。</span><span class="sxs-lookup"><span data-stu-id="c401f-120">The value is expressed as a percentage.</span></span> <span data-ttu-id="c401f-121">較高的值表示效能較差。</span><span class="sxs-lookup"><span data-stu-id="c401f-121">Higher values indicate poorer performance.</span></span>

    <span data-ttu-id="c401f-122">本指南中的雙向會計算出額外負荷，但可以個別計算每個方向的費用。</span><span class="sxs-lookup"><span data-stu-id="c401f-122">Overhead is calculated for both directions in this guide, but can be calculated for each direction separately.</span></span>

-   <span data-ttu-id="c401f-123">Bandwidth-Delay 產品</span><span class="sxs-lookup"><span data-stu-id="c401f-123">Bandwidth-Delay Product</span></span>

    <span data-ttu-id="c401f-124">網路的每秒每秒頻寬的乘積，而 RTT (以秒為單位) 。</span><span class="sxs-lookup"><span data-stu-id="c401f-124">Product of the bits-per-second bandwidth of the network, and the RTT (in seconds).</span></span> <span data-ttu-id="c401f-125">此值等於填滿可用的網路頻寬所花費的位數。</span><span class="sxs-lookup"><span data-stu-id="c401f-125">This value equates to the number of bits it takes to fill available network bandwidth.</span></span> <span data-ttu-id="c401f-126">當頻寬延遲產品的值偏高時，TCP/IP 堆疊必須處理大量未認可的資料，才能讓管線保持完整。</span><span class="sxs-lookup"><span data-stu-id="c401f-126">When the value for bandwidth-delay product is high, the TCP/IP stack must handle large amounts of unacknowledged data in order to keep the pipeline full.</span></span> <span data-ttu-id="c401f-127">頻寬延遲產品是串流應用程式的關鍵端對端計量。</span><span class="sxs-lookup"><span data-stu-id="c401f-127">Bandwidth-delay product is a key end-to-end metric for streaming applications.</span></span>

 

 



