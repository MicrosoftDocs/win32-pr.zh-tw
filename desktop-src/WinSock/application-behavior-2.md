---
description: 要考慮的應用程式開發的另一個層面是本機或 intracomputer 作業之間的行為差異，以及在兩部網路電腦之間進行作業時的行為。
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: 應用程式行為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a9b871a2c0535d9ef4220824651657332a224a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511469"
---
# <a name="application-behavior"></a><span data-ttu-id="76921-103">應用程式行為</span><span class="sxs-lookup"><span data-stu-id="76921-103">Application Behavior</span></span>

<span data-ttu-id="76921-104">要考慮的應用程式開發的另一個層面是本機或 intracomputer 作業之間的行為差異，以及在兩部網路電腦之間進行作業時的行為。</span><span class="sxs-lookup"><span data-stu-id="76921-104">Another aspect of application development to consider is the difference in behavior between local, or intracomputer operations, and behavior when operations take place between two networked computers.</span></span> <span data-ttu-id="76921-105">有些應用程式行為在本機電腦上的可接受很好，但是在網路上執行時，會造成顯著的效能降低和資源耗用量。</span><span class="sxs-lookup"><span data-stu-id="76921-105">There are application behaviors that may work acceptably well on a local computer, but when run across a network, cause significant performance degradation and resource consumption.</span></span> <span data-ttu-id="76921-106">開發 Windows 通訊端應用程式時，應避免下列應用程式行為。</span><span class="sxs-lookup"><span data-stu-id="76921-106">The following application behaviors should be avoided when developing Windows Sockets applications.</span></span>

## <a name="behaviors-to-avoid"></a><span data-ttu-id="76921-107">要避免的行為</span><span class="sxs-lookup"><span data-stu-id="76921-107">Behaviors to Avoid</span></span>

-   <span data-ttu-id="76921-108">多對話應用程式。</span><span class="sxs-lookup"><span data-stu-id="76921-108">Chatty Applications.</span></span>

    <span data-ttu-id="76921-109">有些應用程式會執行許多小型交易。</span><span class="sxs-lookup"><span data-stu-id="76921-109">Some applications perform many small transactions.</span></span> <span data-ttu-id="76921-110">結合與每個這類交易相關聯的網路額外負荷時，會將效果相乘。</span><span class="sxs-lookup"><span data-stu-id="76921-110">When combined with the network overhead associated with each such transaction, the effect is multiplied.</span></span> <span data-ttu-id="76921-111">在網路中，小型交易可耗用的資源數量和大型交易的時間很多。</span><span class="sxs-lookup"><span data-stu-id="76921-111">In networking, small transactions can consume as many resources and as much time as large transactions.</span></span> <span data-ttu-id="76921-112">更好的方法是將許多小型交易合併成單一大型交易。</span><span class="sxs-lookup"><span data-stu-id="76921-112">A better approach is to combine many small transactions into a single large transaction.</span></span>

-   <span data-ttu-id="76921-113">序列化的交易。</span><span class="sxs-lookup"><span data-stu-id="76921-113">Serialized Transactions.</span></span>

    <span data-ttu-id="76921-114">非必要的交易序列化可能會導致效能不佳，而且會影響擴充性。</span><span class="sxs-lookup"><span data-stu-id="76921-114">Unnecessary serialization of transactions can result in poor performance, and affect scalability.</span></span> <span data-ttu-id="76921-115">例如，1000序列化交易至少需要 1000 \* RTT 才能完成。</span><span class="sxs-lookup"><span data-stu-id="76921-115">For example, 1000 serialized transactions take at least 1000 \* RTT to complete.</span></span> <span data-ttu-id="76921-116">更好的方法是以平行方式執行不相關的交易。</span><span class="sxs-lookup"><span data-stu-id="76921-116">A better approach is to run unrelated transactions in parallel.</span></span> <span data-ttu-id="76921-117">當序列化的應用程式與多對話應用程式結合時，回應可能會嚴重妨礙。</span><span class="sxs-lookup"><span data-stu-id="76921-117">When serialized applications are combined with chatty applications, responsiveness can be seriously hampered.</span></span>

    > [!Note]  
    > <span data-ttu-id="76921-118">將應用程式正確還原序列化可能很困難。</span><span class="sxs-lookup"><span data-stu-id="76921-118">Properly deserializing an application can be difficult.</span></span> <span data-ttu-id="76921-119">如果從序列化變更為平行證明太困難，請考慮將多個交易結合為較少的大型交易。</span><span class="sxs-lookup"><span data-stu-id="76921-119">If changing from serialized to parallel proves too difficult, consider combining multiple transactions into fewer large transactions.</span></span>

     

-   <span data-ttu-id="76921-120">Fat 交易。</span><span class="sxs-lookup"><span data-stu-id="76921-120">Fat Transactions.</span></span>

    <span data-ttu-id="76921-121">在網路上傳送不必要位元組的應用程式會被視為 fat 應用程式。</span><span class="sxs-lookup"><span data-stu-id="76921-121">Applications that send unnecessary bytes on the network are considered fat applications.</span></span> <span data-ttu-id="76921-122">在網路上傳送不必要位元組的應用程式會增加網路額外負荷，而且會妨礙效能。</span><span class="sxs-lookup"><span data-stu-id="76921-122">Applications that send unnecessary bytes on the network increase network overhead, and performance is hampered.</span></span> <span data-ttu-id="76921-123">這種情況通常來自無效率的資料結構或無效率的資料串流。</span><span class="sxs-lookup"><span data-stu-id="76921-123">This situation often comes from inefficient data structures or inefficient data streaming.</span></span> <span data-ttu-id="76921-124">若要解決此情況，請將資料結構優化，或考慮使用壓縮。</span><span class="sxs-lookup"><span data-stu-id="76921-124">To remedy this, optimize data structures, or consider using compression.</span></span>

<span data-ttu-id="76921-125">下列各節將討論要考慮的應用程式開發層面。</span><span class="sxs-lookup"><span data-stu-id="76921-125">The following sections address aspects of application development to consider.</span></span>

-   [<span data-ttu-id="76921-126">TCP/IP 特定問題</span><span class="sxs-lookup"><span data-stu-id="76921-126">TCP/IP-specific Issues</span></span>](tcp-ip-specific-issues-2.md)
-   [<span data-ttu-id="76921-127">辨識緩慢的應用程式</span><span class="sxs-lookup"><span data-stu-id="76921-127">Recognizing Slow Applications</span></span>](recognizing-slow-applications-2.md)
-   [<span data-ttu-id="76921-128">使用 Netstat 計算額外負荷</span><span class="sxs-lookup"><span data-stu-id="76921-128">Calculating Overhead with Netstat</span></span>](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a><span data-ttu-id="76921-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="76921-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76921-130">高效能的 Windows 通訊端應用程式</span><span class="sxs-lookup"><span data-stu-id="76921-130">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



