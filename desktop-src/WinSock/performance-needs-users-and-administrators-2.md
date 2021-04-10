---
description: 具有 Windows 通訊端 (Winsock) 應用程式之使用者和系統管理員的效能需求。
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 效能需求：使用者和系統管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a8178cf1d7516e9c16493916f8cf911752b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026210"
---
# <a name="performance-needs-users-and-administrators"></a><span data-ttu-id="cdc86-103">效能需求：使用者和系統管理員</span><span class="sxs-lookup"><span data-stu-id="cdc86-103">Performance Needs: Users and Administrators</span></span>

<span data-ttu-id="cdc86-104">使用者會根據其體驗來判斷應用程式效能：</span><span class="sxs-lookup"><span data-stu-id="cdc86-104">Users judge application performance by their experience:</span></span>

-   <span data-ttu-id="cdc86-105">應用程式是否快速回應？</span><span class="sxs-lookup"><span data-stu-id="cdc86-105">Is the application quick to respond?</span></span>
-   <span data-ttu-id="cdc86-106">當背景作業執行時，會顯示沙漏圖示嗎？</span><span class="sxs-lookup"><span data-stu-id="cdc86-106">Is an hourglass icon displayed while background operations are carried out?</span></span>
-   <span data-ttu-id="cdc86-107">應用程式是否會快速啟動並關閉？</span><span class="sxs-lookup"><span data-stu-id="cdc86-107">Does the application launch and close quickly?</span></span>
-   <span data-ttu-id="cdc86-108">是否以可理解的方式處理錯誤？</span><span class="sxs-lookup"><span data-stu-id="cdc86-108">Are errors handled in an understandable way?</span></span>

<span data-ttu-id="cdc86-109">總而言之，使用者想要讓應用程式快速且可預測。</span><span class="sxs-lookup"><span data-stu-id="cdc86-109">To summarize, users want applications to be fast and predictable.</span></span>

<span data-ttu-id="cdc86-110">相反地，系統管理員通常會判斷應用程式使用網路資源的效率。</span><span class="sxs-lookup"><span data-stu-id="cdc86-110">In contrast, administrators often judge an application's performance on how efficiently it uses network resources.</span></span> <span data-ttu-id="cdc86-111">系統管理員可能會問：</span><span class="sxs-lookup"><span data-stu-id="cdc86-111">Administrators may ask:</span></span>

-   <span data-ttu-id="cdc86-112">應用程式是否具有低負擔和有效率的網路使用方式？</span><span class="sxs-lookup"><span data-stu-id="cdc86-112">Does the application have low overhead and efficient network usage?</span></span>
-   <span data-ttu-id="cdc86-113">使用的連接數目下限，所以我的伺服器可以盡可能地服務多個使用者？</span><span class="sxs-lookup"><span data-stu-id="cdc86-113">Are the minimum number of connections used, so my server can service as many users at once as possible?</span></span>
-   <span data-ttu-id="cdc86-114">我是否持續呼叫技術服務人員？</span><span class="sxs-lookup"><span data-stu-id="cdc86-114">Am I constantly calling helpdesk?</span></span>

<span data-ttu-id="cdc86-115">簡單來說，系統管理員想要讓應用程式調整規模。</span><span class="sxs-lookup"><span data-stu-id="cdc86-115">In short, administrators want applications to scale.</span></span>

## <a name="best-practices-for-performance-needs"></a><span data-ttu-id="cdc86-116">效能需求的最佳作法</span><span class="sxs-lookup"><span data-stu-id="cdc86-116">Best Practices for Performance Needs</span></span>

<span data-ttu-id="cdc86-117">開發 Windows 通訊端應用程式時，這些效能需求會轉譯成有用的規則。</span><span class="sxs-lookup"><span data-stu-id="cdc86-117">When developing a Windows Sockets application, these performance requirements translate into useful rules.</span></span>

-   <span data-ttu-id="cdc86-118">讓網路應用程式快速初始化。</span><span class="sxs-lookup"><span data-stu-id="cdc86-118">Have network applications initialize quickly.</span></span>

    <span data-ttu-id="cdc86-119">使用者介面應該不需要等待網路回應。</span><span class="sxs-lookup"><span data-stu-id="cdc86-119">The user interface should not have to wait for network responses.</span></span> <span data-ttu-id="cdc86-120">您可以在網路可用或沒有網路之前執行某些工作。</span><span class="sxs-lookup"><span data-stu-id="cdc86-120">Some tasks can be performed before the network is available, or without the network.</span></span> <span data-ttu-id="cdc86-121">如果網路沒有回應，使用者可能需要使用者介面來進行簡單的作業，例如關閉應用程式。</span><span class="sxs-lookup"><span data-stu-id="cdc86-121">If the network is not responding, the user may need the user interface for simple operations, such as closing the application.</span></span>

-   <span data-ttu-id="cdc86-122">請勿等待網路關機。</span><span class="sxs-lookup"><span data-stu-id="cdc86-122">Do not wait for the network for shutdown.</span></span>

    <span data-ttu-id="cdc86-123">正確撰寫的用戶端-伺服器應用程式會正常地處理 abortive 中斷連線。</span><span class="sxs-lookup"><span data-stu-id="cdc86-123">Properly written client-server applications handle abortive disconnects gracefully.</span></span> <span data-ttu-id="cdc86-124">請勿起始可能很長的作業（例如，將檔案或資料夾與伺服器同步處理，而無法在關機時中斷）。</span><span class="sxs-lookup"><span data-stu-id="cdc86-124">Do not initiate a potentially lengthy operation, such as synchronizing files or folders with a server, that cannot be interrupted on shutdown.</span></span> <span data-ttu-id="cdc86-125">網路的回應速度不一致，因此即使是小型作業也可以證明很耗時。</span><span class="sxs-lookup"><span data-stu-id="cdc86-125">Networks are not consistently responsive, so even small operations could prove time consuming.</span></span> <span data-ttu-id="cdc86-126">為使用者提供正面的意見反應，包括進度和預估完成時間的指示。</span><span class="sxs-lookup"><span data-stu-id="cdc86-126">Provide positive feedback for users, including indications of progress and estimated completion times.</span></span>

-   <span data-ttu-id="cdc86-127">確定有回應的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="cdc86-127">Ensure a responsive user interface.</span></span>

    <span data-ttu-id="cdc86-128">應用程式回應性有助於消除不必要的技術服務人員電話。</span><span class="sxs-lookup"><span data-stu-id="cdc86-128">Application responsiveness helps eliminate unnecessary helpdesk calls.</span></span> <span data-ttu-id="cdc86-129">互動式回應的良好指導方針是500毫秒。</span><span class="sxs-lookup"><span data-stu-id="cdc86-129">A good guideline for interactive response is 500 milliseconds.</span></span> <span data-ttu-id="cdc86-130">使用者觀察暫停的時間超過500毫秒，以作為效能的延隔時間。</span><span class="sxs-lookup"><span data-stu-id="cdc86-130">Users perceive pauses longer than 500 milliseconds as a lag in performance.</span></span> <span data-ttu-id="cdc86-131">應用程式應該有足夠的回應，可讓使用者安心地提供應用程式。</span><span class="sxs-lookup"><span data-stu-id="cdc86-131">Applications should be responsive enough to provide the user with confidence about the application.</span></span>

-   <span data-ttu-id="cdc86-132">請仔細進行網路錯誤。</span><span class="sxs-lookup"><span data-stu-id="cdc86-132">Scrutinize network errors.</span></span>

    <span data-ttu-id="cdc86-133">並非所有網路錯誤都很重要。</span><span class="sxs-lookup"><span data-stu-id="cdc86-133">Not all network errors are critical.</span></span> <span data-ttu-id="cdc86-134">例如，已接收或張貼其所有資料的應用程式可能會在關閉連接時忽略錯誤。</span><span class="sxs-lookup"><span data-stu-id="cdc86-134">For example, an application that has received or posted all of its data can likely ignore errors when closing the connection.</span></span> <span data-ttu-id="cdc86-135">請勿假設網路或使用者可供使用;您可以在不需要使用者介入的情況下處理錯誤，或在錯誤非關鍵性時予以忽略。</span><span class="sxs-lookup"><span data-stu-id="cdc86-135">Do not assume the network or the user is available; either handle errors without user intervention, or ignore them if errors are noncritical.</span></span>

-   <span data-ttu-id="cdc86-136">應用程式應該定義它自己合理的時間。</span><span class="sxs-lookup"><span data-stu-id="cdc86-136">An application should define its own reasonable time outs.</span></span>

    <span data-ttu-id="cdc86-137">例如，Windows 通訊端 connect () 要求可能會在某些情況下封鎖21秒。</span><span class="sxs-lookup"><span data-stu-id="cdc86-137">For example, a Windows Sockets connect() request may block under some conditions for as much as 21 seconds.</span></span> <span data-ttu-id="cdc86-138">應用程式可能需要將自己的時間引入適合其使用者的時間。</span><span class="sxs-lookup"><span data-stu-id="cdc86-138">Applications may need to introduce their own time outs as appropriate for their users.</span></span>

-   <span data-ttu-id="cdc86-139">將通訊協定額外負荷降到最低。</span><span class="sxs-lookup"><span data-stu-id="cdc86-139">Minimize protocol overhead.</span></span>

    <span data-ttu-id="cdc86-140">節省網路頻寬的部分是要將應用程式所產生的通訊協定額外負荷降到最低。</span><span class="sxs-lookup"><span data-stu-id="cdc86-140">Conserving network bandwidth is partially about minimizing the protocol overhead incurred by your application.</span></span> <span data-ttu-id="cdc86-141">它也會排除不必要的網路流量。</span><span class="sxs-lookup"><span data-stu-id="cdc86-141">It is also about eliminating unnecessary network traffic.</span></span> <span data-ttu-id="cdc86-142">具有較低標頭負荷的通訊協定可以用來傳輸應用程式資料。</span><span class="sxs-lookup"><span data-stu-id="cdc86-142">Protocols with a lower header overhead can be used to transfer application data.</span></span> <span data-ttu-id="cdc86-143">例如，傳送較少量非關鍵性或可重複的資料時，請使用 UDP 而不是 TCP，以降低與連線建立和維護相關的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="cdc86-143">For example, when sending smaller amounts of noncritical or repeatable data, use UDP as opposed to TCP to reduce the overhead associated with connection establishment and maintenance.</span></span> <span data-ttu-id="cdc86-144">如果相同的資料必須傳送給多個收件者，請考慮多播。</span><span class="sxs-lookup"><span data-stu-id="cdc86-144">If the same data must be sent to multiple recipients, consider multicast.</span></span> <span data-ttu-id="cdc86-145">請注意，UDP 應用程式不會受到流量控制，推播超過可用的頻寬可能會導致嚴重的網路失敗。</span><span class="sxs-lookup"><span data-stu-id="cdc86-145">Be aware that UDP applications are not flow-controlled—pushing beyond the available bandwidth can cause catastrophic network failure.</span></span> <span data-ttu-id="cdc86-146">Netstat 公用程式可以與其 **-e** 和 **-s** 選項搭配使用，以顯示各種通訊協定的統計資料。</span><span class="sxs-lookup"><span data-stu-id="cdc86-146">The Netstat utility can be used with its **-e** and **-s** options to display statistics for various protocols.</span></span>

-   <span data-ttu-id="cdc86-147">節省系統資源。</span><span class="sxs-lookup"><span data-stu-id="cdc86-147">Conserve system resources.</span></span>

    <span data-ttu-id="cdc86-148">如果未使用適當的擋板，則可以快速取用系統資源。</span><span class="sxs-lookup"><span data-stu-id="cdc86-148">System resources can be consumed quickly if proper restraint is not used.</span></span> <span data-ttu-id="cdc86-149">例如，通訊端和 TCP 連接都會耗用資源。</span><span class="sxs-lookup"><span data-stu-id="cdc86-149">For example, sockets and TCP connections consume resources.</span></span> <span data-ttu-id="cdc86-150">請勿針對每個用戶端使用數個 TCP 連線，其中一個會提供應用程式的用途。</span><span class="sxs-lookup"><span data-stu-id="cdc86-150">Do not use several TCP connections per client where one will serve the application's purpose.</span></span>

<span data-ttu-id="cdc86-151">針對交易式應用程式，良好的使用者經驗和低網路使用量都不會有衝突的目標。</span><span class="sxs-lookup"><span data-stu-id="cdc86-151">For transactional applications, good user experience and low network utilization are not conflicting goals.</span></span> <span data-ttu-id="cdc86-152">網路是瓶頸。</span><span class="sxs-lookup"><span data-stu-id="cdc86-152">The network is a bottleneck.</span></span> <span data-ttu-id="cdc86-153">需要大量網路的應用程式會花更多時間等候，而且妥善撰寫的網路應用程式是設計來將使用者介面和網路傳輸的不必要等候時間降到最低。</span><span class="sxs-lookup"><span data-stu-id="cdc86-153">Network-intensive applications spend more time waiting, and well written network applications are designed to minimize unnecessary wait time, both for the user interface and for network transmissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdc86-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="cdc86-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdc86-155">高效能的 Windows 通訊端應用程式</span><span class="sxs-lookup"><span data-stu-id="cdc86-155">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="cdc86-156">效能維度</span><span class="sxs-lookup"><span data-stu-id="cdc86-156">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



