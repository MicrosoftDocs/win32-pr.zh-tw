---
description: On/Off 效能的最佳作法
ms.assetid: 872c2a33-327e-41a8-81db-905c46673f13
title: On/Off 效能的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c88eaf5175db43061e57bc4689d8bf256e6881
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088616"
---
# <a name="best-practices-for-onoff-performance"></a><span data-ttu-id="f9db6-103">On/Off 效能的最佳作法</span><span class="sxs-lookup"><span data-stu-id="f9db6-103">Best Practices for On/Off Performance</span></span>

## <a name="platform"></a><span data-ttu-id="f9db6-104">平台</span><span class="sxs-lookup"><span data-stu-id="f9db6-104">Platform</span></span>

<span data-ttu-id="f9db6-105">**用戶端-** Windows Vista \| windows 7</span><span class="sxs-lookup"><span data-stu-id="f9db6-105">**Clients -** Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="f9db6-106">**伺服器-** Windows Server 2008 \| Windows server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f9db6-106">**Servers -** Windows Server 2008 \| Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="f9db6-107">Description</span><span class="sxs-lookup"><span data-stu-id="f9db6-107">Description</span></span>

<span data-ttu-id="f9db6-108">系統電源狀態 (或 S 狀態) （如 Advanced Computer 電源介面 (ACPI) 規格中所定義）堆疊稱為「開啟/關閉」狀態，因為最常見的 S 狀態轉換是電腦開啟和關閉。</span><span class="sxs-lookup"><span data-stu-id="f9db6-108">The system power states (or S-states), as defined in the Advanced Computer Power Interface (ACPI) specification, are colloquially called on/off states since the most common S-state transition is a computer turning on and off.</span></span> <span data-ttu-id="f9db6-109">在執行 Windows Vista 或 Windows 7 的系統上，不同的開啟/關閉狀態轉換是開機、睡眠 (ACPI S3) 、休眠 (ACPI S4) 和關機。</span><span class="sxs-lookup"><span data-stu-id="f9db6-109">The different on/off state transitions on a system running Windows Vista or Windows 7 are boot, sleep (ACPI S3), hibernate (ACPI S4), and shutdown.</span></span>

<span data-ttu-id="f9db6-110">在這些開啟/關閉轉換期間的良好效能不僅能改善電腦的認知品質，也會大幅影響每日電腦使用模式和系統可靠性。</span><span class="sxs-lookup"><span data-stu-id="f9db6-110">Good performance during these on/off transitions not only improves the perceived quality of a computer, but also greatly affects daily computer usage patterns and system reliability.</span></span> <span data-ttu-id="f9db6-111">客戶可能會因為開機或關機時間太長的系統而感到挫折。</span><span class="sxs-lookup"><span data-stu-id="f9db6-111">Customers can become frustrated by systems that take too long to boot or to shut down.</span></span> <span data-ttu-id="f9db6-112">具有冗長睡眠和休眠轉換的行動系統可能會不必要地耗盡電池壽命。</span><span class="sxs-lookup"><span data-stu-id="f9db6-112">Mobile systems that have lengthy sleep and hibernation transitions can unnecessarily deplete battery life.</span></span> <span data-ttu-id="f9db6-113">較長的關機時間也會對行動系統的可靠性造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="f9db6-113">Longer shutdown times can also adversely affect the reliability of mobile systems.</span></span> <span data-ttu-id="f9db6-114">例如，它們會增加非預期電源減少的風險。</span><span class="sxs-lookup"><span data-stu-id="f9db6-114">For example, they increase the risk of unexpected power cut-offs.</span></span>

<span data-ttu-id="f9db6-115">系統擴充功能（例如驅動程式、應用程式和服務）可能會對轉換時間有顯著的影響。</span><span class="sxs-lookup"><span data-stu-id="f9db6-115">System extensions like drivers, applications, and services can have a significant impact on on/off transition times.</span></span> <span data-ttu-id="f9db6-116">本節將討論應用程式和服務開發人員可以遵循的一些最佳作法，以避免開機、待命和關機期間的延遲，並確保開機後和後續恢復的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="f9db6-116">This section discusses some of the best practices that application and service developers can follow to avoid delays during boot, standby, and shutdown, and to ensure a responsive post-boot and post-resume user experience.</span></span> <span data-ttu-id="f9db6-117">如需如何使用 Windows 效能工具組找出/關閉效能問題的詳細資訊，並針對您的應用程式或服務執行下列建議，請參閱「其他資源的連結」一節中的白皮書。</span><span class="sxs-lookup"><span data-stu-id="f9db6-117">For more details on how to identify on/off performance issues using the Windows Performance Toolkit and implement the below recommendations for your application or service, please refer to the whitepapers in the 'Links to other Resources' section.</span></span>

## <a name="best-practices"></a><span data-ttu-id="f9db6-118">最佳做法</span><span class="sxs-lookup"><span data-stu-id="f9db6-118">Best Practices</span></span>

-   <span data-ttu-id="f9db6-119">使用 Windows 效能工具組，在所有的開啟/關閉轉換期間測量效能。</span><span class="sxs-lookup"><span data-stu-id="f9db6-119">Use the Windows Performance Toolkit to measure performance during all on/off transitions.</span></span>
-   <span data-ttu-id="f9db6-120">以受控制的方式執行測試，並針對有效的基準進行比較：</span><span class="sxs-lookup"><span data-stu-id="f9db6-120">Perform testing in a controlled way, and make comparisons against a valid baseline:</span></span>
    -   <span data-ttu-id="f9db6-121">以最少的系統擴充功能在系統上取得基準量測</span><span class="sxs-lookup"><span data-stu-id="f9db6-121">Obtain a baseline measurement on a system with as few system extensions as possible</span></span>
    -   <span data-ttu-id="f9db6-122">一次新增一個應用程式和服務</span><span class="sxs-lookup"><span data-stu-id="f9db6-122">Add applications and services one at a time</span></span>
    -   <span data-ttu-id="f9db6-123">測試處於開啟/關閉轉換時間的無法接受的回歸</span><span class="sxs-lookup"><span data-stu-id="f9db6-123">Test for unacceptable regressions in on/off transition times</span></span>
-   <span data-ttu-id="f9db6-124">避免針對重要開機路徑上的應用程式使用 managed 程式碼。</span><span class="sxs-lookup"><span data-stu-id="f9db6-124">Avoid using managed code for applications on the critical boot path.</span></span>
-   <span data-ttu-id="f9db6-125">確定所有應用程式都能快速回應 (WM \_ QUERYENDSESSION 和 wm \_ ENDSESSION 訊息) 的關機通知。</span><span class="sxs-lookup"><span data-stu-id="f9db6-125">Ensure that all applications respond quickly to shutdown notifications (WM\_QUERYENDSESSION and WM\_ENDSESSION messages).</span></span>
-   <span data-ttu-id="f9db6-126">藉由將 CPU、磁片和網路活動降至最低，以回應關機通知，減少服務和應用程式關閉路徑的延遲。</span><span class="sxs-lookup"><span data-stu-id="f9db6-126">Reduce delays in the shutdown path of services and applications by minimizing CPU, disk, and network activity in response to shutdown notifications.</span></span>
-   <span data-ttu-id="f9db6-127">避免處理暫停通知 (WM \_ POWERBROADCAST 訊息) 的延遲。</span><span class="sxs-lookup"><span data-stu-id="f9db6-127">Avoid delays in processing the suspend notification (WM\_POWERBROADCAST message).</span></span>
-   <span data-ttu-id="f9db6-128">快速回應以繼續事件，並將恢復後的 CPU、磁片和網路使用量降至最低。</span><span class="sxs-lookup"><span data-stu-id="f9db6-128">Respond quickly to resume events and minimize post-resume CPU, disk, and network usage.</span></span>
-   <span data-ttu-id="f9db6-129">減少開機後的應用程式資源耗用量。</span><span class="sxs-lookup"><span data-stu-id="f9db6-129">Reduce application resource consumption post-boot.</span></span>
-   <span data-ttu-id="f9db6-130">請勿在每次開機時從 RunOnce 索引鍵啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="f9db6-130">Do not start applications from the RunOnce key on every boot.</span></span>
-   <span data-ttu-id="f9db6-131">將所有不必要的服務轉換為需求開始或觸發程式開始，以便讓系統資源在開機期間可供使用。</span><span class="sxs-lookup"><span data-stu-id="f9db6-131">Convert all nonessential services to demand start or trigger start in order to make system resources available during boot.</span></span>
-   <span data-ttu-id="f9db6-132">避免使用載入順序群組來表示服務相依性。</span><span class="sxs-lookup"><span data-stu-id="f9db6-132">Avoid using load order groups to express service dependencies.</span></span>
-   <span data-ttu-id="f9db6-133">請確定所有執行中的服務都在開機期間儘快回報此狀態，以避免封鎖服務控制管理員 (SCM) 。</span><span class="sxs-lookup"><span data-stu-id="f9db6-133">Ensure that all running services report this status as soon as possible during boot to avoid blocking the Service Control Manager (SCM).</span></span>
-   <span data-ttu-id="f9db6-134">避免在啟動路徑上使用服務的 managed 程式碼。</span><span class="sxs-lookup"><span data-stu-id="f9db6-134">Avoid using managed code for services on the startup path.</span></span>
-   <span data-ttu-id="f9db6-135">除非絕對必要，否則不允許服務選擇接收 (服務 \_ 控制 \_ PRESHUTDOWN 和服務 \_ 控制 \_ 關閉控制代碼的預先關閉和關閉通知) 。</span><span class="sxs-lookup"><span data-stu-id="f9db6-135">Do not allow services to opt in to receive pre-shutdown and shutdown notifications (SERVICE\_CONTROL\_PRESHUTDOWN and SERVICE\_CONTROL\_SHUTDOWN control codes) unless absolutely required.</span></span>
-   <span data-ttu-id="f9db6-136">確定已選擇接收關機通知的所有服務，都能快速回應 SCM。</span><span class="sxs-lookup"><span data-stu-id="f9db6-136">Ensure that all services that have opted to receive shutdown notifications respond quickly to the SCM.</span></span>
-   <span data-ttu-id="f9db6-137">確認除非絕對必要，否則服務不會選擇接收暫停通知。</span><span class="sxs-lookup"><span data-stu-id="f9db6-137">Verify that services do not opt in to receive suspend notifications unless absolutely required.</span></span>
-   <span data-ttu-id="f9db6-138">確定所有服務都能快速回應以繼續事件，並將恢復後的 CPU、磁片和網路使用量降至最低。</span><span class="sxs-lookup"><span data-stu-id="f9db6-138">Ensure that all services respond quickly to resume events and minimize post-resume CPU, disk, and network usage.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="f9db6-139">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="f9db6-139">Links to Other Resources</span></span>

-   -   [<span data-ttu-id="f9db6-140">Windows On/Off 轉換解決方案指南</span><span class="sxs-lookup"><span data-stu-id="f9db6-140">Windows On/Off Transitions Solutions Guide</span></span>](/windows-hardware/test/assessments/onoff-transition-performance)
-   [<span data-ttu-id="f9db6-141">Windows Vista 的開啟/關閉轉換效能分析</span><span class="sxs-lookup"><span data-stu-id="f9db6-141">On/Off Transition Performance Analysis of Windows Vista</span></span>](/windows-hardware/test/assessments/onoff-transition-performance)
-   [<span data-ttu-id="f9db6-142">Windows 效能分析</span><span class="sxs-lookup"><span data-stu-id="f9db6-142">Windows Performance Analysis</span></span>](https://msdn.microsoft.com/performance/default.aspx)
-   [<span data-ttu-id="f9db6-143">MSDN 上的 Windows 效能工具組檔</span><span class="sxs-lookup"><span data-stu-id="f9db6-143">Windows Performance Toolkit documentation on MSDN</span></span>](/previous-versions/windows/desktop/xperf/windows-performance-analyzer--wpa-)
-   [<span data-ttu-id="f9db6-144">Windows 效能分析論壇</span><span class="sxs-lookup"><span data-stu-id="f9db6-144">Windows Performance Analysis forum</span></span>](https://social.msdn.microsoft.com/Forums/wptk_v4/threads/)
-   [<span data-ttu-id="f9db6-145">MSDN 上的 Windows 事件追蹤</span><span class="sxs-lookup"><span data-stu-id="f9db6-145">Event Tracing for Windows on MSDN</span></span>](../etw/event-tracing-portal.md)

 

 
