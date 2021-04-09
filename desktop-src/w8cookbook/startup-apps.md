---
title: 啟動應用程式
description: 啟動應用程式
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- 啟動應用程式
- 背景工作
- 執行金鑰
- RunOnce
- 開機檔案夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a12f01dac073712512206a5c432561b4a0b75e
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "103684190"
---
# <a name="startup-apps"></a><span data-ttu-id="b6169-108">啟動應用程式</span><span class="sxs-lookup"><span data-stu-id="b6169-108">Startup apps</span></span>

## <a name="platform"></a><span data-ttu-id="b6169-109">平台</span><span class="sxs-lookup"><span data-stu-id="b6169-109">Platform</span></span>

<span data-ttu-id="b6169-110">**用戶端**   Windows 8</span><span class="sxs-lookup"><span data-stu-id="b6169-110">**Clients**   Windows 8</span></span>  


## <a name="description"></a><span data-ttu-id="b6169-111">Description</span><span class="sxs-lookup"><span data-stu-id="b6169-111">Description</span></span>

<span data-ttu-id="b6169-112">Windows 的其中一個重要的因素是，從傳統桌上型電腦和膝上型電腦到低電源的平板電腦，都能照亮各種外型規格。</span><span class="sxs-lookup"><span data-stu-id="b6169-112">One of the big bets with Windows is the ability to light up various form factors, from the traditional desktops and laptops to low-powered tablets.</span></span> <span data-ttu-id="b6169-113">為了確保我們的共同客戶擁有使用 Windows 所選擇之任何外型規格的絕佳體驗，需要處理的兩個關鍵成功計量是提高電池壽命和絕佳的電腦回應能力。</span><span class="sxs-lookup"><span data-stu-id="b6169-113">To ensure that our mutual customers have a great experience on any form factor they choose with Windows, two key success metrics that need to be addressed are increased battery life and excellent PC responsiveness.</span></span> <span data-ttu-id="b6169-114">為了達成這些目的，我們已在多個 Windows 區域中進行改良，包括處理生命週期、睡眠狀態和啟動應用程式 (應用程式，並在電腦開機) 之後自動啟動。</span><span class="sxs-lookup"><span data-stu-id="b6169-114">In order to achieve these, improvements have been made in multiple areas of Windows including process life cycle, sleep states and startup apps (apps with automated launch after machine boot).</span></span> <span data-ttu-id="b6169-115">本主題將重點放在 Windows 裝置上啟動應用程式的一些影響，並提供指引給開發人員 (ISV/IHV) 和 Oem 重新思考啟動應用程式的使用模式，以改善我們的共同客戶的電池壽命和回應能力。</span><span class="sxs-lookup"><span data-stu-id="b6169-115">This topic highlights some of the impacts that startup apps have on a Windows device, and provides guidance to developers (ISV/IHV) and OEMs to rethink the usage patterns of startup apps in order to improve battery life and responsiveness for our mutual customers.</span></span> <span data-ttu-id="b6169-116">它也會描述 Windows 中的變更，讓使用者能夠決定實際要執行的啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="b6169-116">It also describes the changes in Windows that put users in control of determining which of the startup apps actually get to execute.</span></span>

<span data-ttu-id="b6169-117">Windows Store 應用程式的設計目的是要遵守新的電池耗用量和回應性標準，而且 Windows 會藉由暫停和/或終止它們來管理其生命週期。</span><span class="sxs-lookup"><span data-stu-id="b6169-117">Windows Store apps are designed to adhere to new standards of battery consumption and responsiveness, and Windows manages their life cycle by suspending and/or terminating them.</span></span> <span data-ttu-id="b6169-118">不過，針對之前的 Windows 版本所設計的桌面應用程式不一定是設計來維持電池壽命或對使用者活動敏感，而且可能會影響系統回應性 (例如，當應用程式傳送一般1秒的心跳來檢查是否有更新時，或預先配置記憶體，以在稍後) 時需要它。</span><span class="sxs-lookup"><span data-stu-id="b6169-118">However, desktop apps designed for prior Windows versions have not necessarily been designed to preserve battery life or be sensitive to user activity, and can affect system responsiveness (for example, when an app sends a regular 1-second heartbeat to check for updates, or pre-allocates memory upfront in case it needs it later).</span></span> <span data-ttu-id="b6169-119">如此一來，如果使用者購買的 Windows tablet PC 有很長的電池壽命，而且有數周的待命時間，卻發現平板電腦的電池壽命無法達到這些目標。</span><span class="sxs-lookup"><span data-stu-id="b6169-119">This can create a poor experience for the user who buys a Windows tablet PC with a long battery life expectancy and weeks of standby, but discovers the tablet s battery life does not achieve these goals.</span></span> <span data-ttu-id="b6169-120">此外，由於啟動應用程式會在背景執行，因此在系統上執行的應用程式數目可能會比使用者察覺的還多，而且會影響系統的回應性。</span><span class="sxs-lookup"><span data-stu-id="b6169-120">Also, since startup apps run in the background, the number of apps running on the system can be significantly more than what the user is aware of and affect system responsiveness.</span></span> <span data-ttu-id="b6169-121">啟動應用程式會分類為包含利用這些機制來啟動的應用程式：</span><span class="sxs-lookup"><span data-stu-id="b6169-121">Startup apps are classified to include those leveraging these mechanisms to start:</span></span>

-   <span data-ttu-id="b6169-122">執行 (HKLM、HKCU、wow64 節點所包含的登錄機碼) </span><span class="sxs-lookup"><span data-stu-id="b6169-122">Run registry keys (HKLM, HKCU, wow64 nodes included)</span></span>
-   <span data-ttu-id="b6169-123">RunOnce 登錄機碼</span><span class="sxs-lookup"><span data-stu-id="b6169-123">RunOnce registry keys</span></span>
-   <span data-ttu-id="b6169-124">每個使用者和公用位置的 [開始] 功能表下的 [啟動] 資料夾</span><span class="sxs-lookup"><span data-stu-id="b6169-124">Startup folders under the start menu for per user and public locations</span></span>

<span data-ttu-id="b6169-125">Windows 已新增新功能，以確保終端使用者一律能夠控制其系統上執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b6169-125">New functionality has been added to Windows to ensure that end users are always in control of the apps that run on their systems.</span></span> <span data-ttu-id="b6169-126">工作管理員中的 [啟動] 索引標籤會顯示啟動應用程式的清單，以及可讓使用者停用啟動應用程式的控制項。</span><span class="sxs-lookup"><span data-stu-id="b6169-126">The Startup tab in Task Manager shows a list of startup apps, along with controls that allow users to disable startup apps.</span></span> <span data-ttu-id="b6169-127">為了協助使用者判斷要停用的內容，工作管理員會顯示每個啟動應用程式影響的量值。</span><span class="sxs-lookup"><span data-stu-id="b6169-127">To help users determine what to disable, Task Manager displays a measure of each startup app s impact.</span></span> <span data-ttu-id="b6169-128">系統會根據應用程式在啟動時的 CPU 和磁片使用量來評估影響。</span><span class="sxs-lookup"><span data-stu-id="b6169-128">Impact is assessed based on an app s CPU and disk usage at startup.</span></span> <span data-ttu-id="b6169-129">影響值取決於套用下列準則：</span><span class="sxs-lookup"><span data-stu-id="b6169-129">Impact values are determined by applying these criteria:</span></span>

-   <span data-ttu-id="b6169-130">**高影響力**   在啟動時使用超過1秒 CPU 時間或超過 3 MB 磁片 i/o 的應用程式</span><span class="sxs-lookup"><span data-stu-id="b6169-130">**High impact**   Apps that use more than 1 second of CPU time or more than 3 MB of disk I/O at startup</span></span>
-   <span data-ttu-id="b6169-131">**中度影響**   使用 300 ms-1000 ms CPU 時間或 300 KB-3 MB 磁片 i/o 的應用程式</span><span class="sxs-lookup"><span data-stu-id="b6169-131">**Medium impact**   Apps that use 300 ms - 1000 ms of CPU time or 300 KB - 3 MB of disk I/O</span></span>
-   <span data-ttu-id="b6169-132">**低影響**   使用小於 300 ms CPU 時間和小於 300 KB 磁片 i/o 的應用程式</span><span class="sxs-lookup"><span data-stu-id="b6169-132">**Low impact**   Apps that use less than 300 ms of CPU time and less than 300 KB of disk I/O</span></span>

<span data-ttu-id="b6169-133">Microsoft 提供的工具可協助應用程式開發人員評估、分析和採取步驟，以降低啟動的影響並改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="b6169-133">Microsoft provides tools to help app developers assess, analyze and take steps to reduce their startup impact and improve the user experience.</span></span> <span data-ttu-id="b6169-134">評定及部署套件提供執行開機效能評估的能力，以及測量在啟動時執行的應用程式所造成的影響。</span><span class="sxs-lookup"><span data-stu-id="b6169-134">The Assessment and Deployment Kit provides the ability to run a boot performance assessment and measure the impact of apps that run at startup.</span></span> <span data-ttu-id="b6169-135">評量結果包含適用的詳細分析和補救資訊，適用于 Windows 啟動時最受影響的元件。</span><span class="sxs-lookup"><span data-stu-id="b6169-135">The assessment results contain detailed analysis and remediation info where applicable, for the top-impacting components at Windows startup.</span></span> <span data-ttu-id="b6169-136">應用程式開發人員可以使用 Windows Performance Analyzer 來執行深入分析，以找出效能影響的根本原因，並改善 Windows 啟動效能。</span><span class="sxs-lookup"><span data-stu-id="b6169-136">Using the Windows Performance Analyzer, app developers can perform deep analysis to find the root cause of the performance impact and improve Windows startup performance.</span></span> <span data-ttu-id="b6169-137">從 [這裡](/previous-versions/windows/hh825494(v=win.10))安裝 Windows ADK。</span><span class="sxs-lookup"><span data-stu-id="b6169-137">Install the Windows ADK from [here](/previous-versions/windows/hh825494(v=win.10)).</span></span>

## <a name="guidance"></a><span data-ttu-id="b6169-138">指引</span><span class="sxs-lookup"><span data-stu-id="b6169-138">Guidance</span></span>

<span data-ttu-id="b6169-139">啟動應用程式涵蓋多個類別，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="b6169-139">Startup apps span multiple categories as described in the table below.</span></span> <span data-ttu-id="b6169-140">一組適用于開發人員的建議會對應至啟動應用程式的類別，以配合上述的 Windows 功能變更。</span><span class="sxs-lookup"><span data-stu-id="b6169-140">A set of recommendations for developers is mapped to the categories of startup apps to align with the Windows functional changes described above.</span></span>



<span data-ttu-id="b6169-141">啟動應用程式類別</span><span class="sxs-lookup"><span data-stu-id="b6169-141">Startup Apps Categories</span></span>

<span data-ttu-id="b6169-142">描述</span><span class="sxs-lookup"><span data-stu-id="b6169-142">Description</span></span>

<span data-ttu-id="b6169-143">建議</span><span class="sxs-lookup"><span data-stu-id="b6169-143">Recommendation</span></span>

<span data-ttu-id="b6169-144">**更新程式**</span><span class="sxs-lookup"><span data-stu-id="b6169-144">**Updaters**</span></span>

<span data-ttu-id="b6169-145">監視和更新線上更新的使用者</span><span class="sxs-lookup"><span data-stu-id="b6169-145">Monitor and update users for online updates</span></span>

<span data-ttu-id="b6169-146">**維護工作**</span><span class="sxs-lookup"><span data-stu-id="b6169-146">**Maintenance Task**</span></span>

> [!Note]  
> <span data-ttu-id="b6169-147">所有更新都應該是維護工作，不需要任何 UI 互動需求。</span><span class="sxs-lookup"><span data-stu-id="b6169-147">All updates should be maintenance tasks, without any UI interaction requirements.</span></span> <span data-ttu-id="b6169-148">應用程式應該直接以安靜的方式更新，並在失敗時回復</span><span class="sxs-lookup"><span data-stu-id="b6169-148">Apps should just update themselves quietly, and rollback on failure</span></span>

<br/>

<span data-ttu-id="b6169-149">$ {ROWSPAN2} $**硬體協助**$ {移除} $</span><span class="sxs-lookup"><span data-stu-id="b6169-149">${ROWSPAN2}$**Hardware Assistance**${REMOVE}$</span></span>  

<span data-ttu-id="b6169-150">替代存取點</span><span class="sxs-lookup"><span data-stu-id="b6169-150">Alternative Access Points</span></span>

<span data-ttu-id="b6169-151">提供可透過 Windows 中其他存取點存取的 Windows 功能和應用程式的存取權</span><span class="sxs-lookup"><span data-stu-id="b6169-151">Provide access to Windows features and apps that are accessible via other access points in Windows</span></span>

<span data-ttu-id="b6169-152">**移除**</span><span class="sxs-lookup"><span data-stu-id="b6169-152">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="b6169-153">重要的是要降低存在於 Windows 中的重複功能</span><span class="sxs-lookup"><span data-stu-id="b6169-153">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="b6169-154">通告</span><span class="sxs-lookup"><span data-stu-id="b6169-154">Notifiers</span></span>

<span data-ttu-id="b6169-155">為使用者提供有關其裝置的通知</span><span class="sxs-lookup"><span data-stu-id="b6169-155">Provide users with notifications regarding their devices</span></span>

<span data-ttu-id="b6169-156">**移除**</span><span class="sxs-lookup"><span data-stu-id="b6169-156">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="b6169-157">Windows 提供通知給使用者其裝置</span><span class="sxs-lookup"><span data-stu-id="b6169-157">Windows provides notifications to users about their devices</span></span>

<br/>

<span data-ttu-id="b6169-158">**預先啟動器**</span><span class="sxs-lookup"><span data-stu-id="b6169-158">**Pre-launchers**</span></span>

<span data-ttu-id="b6169-159">在使用者登入期間，應用程式所需的一些初步活動會卸載至啟動應用程式</span><span class="sxs-lookup"><span data-stu-id="b6169-159">Some of preliminary activities needed by apps is offloaded to a startup app during user login</span></span>

<span data-ttu-id="b6169-160">**移除**</span><span class="sxs-lookup"><span data-stu-id="b6169-160">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="b6169-161">Windows 8 已針對應用程式啟動的快速體驗進行優化。</span><span class="sxs-lookup"><span data-stu-id="b6169-161">Windows 8 is optimized for a fast experience for app launches.</span></span>

<br/>

<span data-ttu-id="b6169-162">$ {ROWSPAN4} $**Utility**$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6169-162">${ROWSPAN4}$**Utility**${REMOVE}$</span></span>  

<span data-ttu-id="b6169-163">電腦同步</span><span class="sxs-lookup"><span data-stu-id="b6169-163">PC Sync</span></span>

<span data-ttu-id="b6169-164">跨多個系統提供同步處理功能</span><span class="sxs-lookup"><span data-stu-id="b6169-164">Provide sync functionality across multiple systems</span></span>

<span data-ttu-id="b6169-165">Beta 版中的 **啟動** (可能的更新) </span><span class="sxs-lookup"><span data-stu-id="b6169-165">**Startup** (Potential updates in Beta)</span></span>

<span data-ttu-id="b6169-166">備份 & 復原</span><span class="sxs-lookup"><span data-stu-id="b6169-166">Backup & Recovery</span></span>

<span data-ttu-id="b6169-167">儲存及還原檔案、設定或整個系統狀態的進入點</span><span class="sxs-lookup"><span data-stu-id="b6169-167">Entry point to save and restore the state of files, settings, or entire systems</span></span>

<span data-ttu-id="b6169-168">**與使用者互動的 Windows Store 應用程式**</span><span class="sxs-lookup"><span data-stu-id="b6169-168">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="b6169-169">遙測</span><span class="sxs-lookup"><span data-stu-id="b6169-169">Telemetry</span></span>

<span data-ttu-id="b6169-170">收集和傳送使用者體驗和環境的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b6169-170">Collect and send info about the user experience and environment</span></span>

<span data-ttu-id="b6169-171">**維護工作**</span><span class="sxs-lookup"><span data-stu-id="b6169-171">**Maintenance Task**</span></span>

<span data-ttu-id="b6169-172">電腦監視</span><span class="sxs-lookup"><span data-stu-id="b6169-172">PC Monitoring</span></span>

<span data-ttu-id="b6169-173">提供重複的現有收件匣功能的未經要求系統狀態監視和通知</span><span class="sxs-lookup"><span data-stu-id="b6169-173">Provide unsolicited system state monitoring and notifications that duplicate existing inbox functionality</span></span>

<span data-ttu-id="b6169-174">**移除**</span><span class="sxs-lookup"><span data-stu-id="b6169-174">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="b6169-175">重要的是要降低存在於 Windows 中的重複功能</span><span class="sxs-lookup"><span data-stu-id="b6169-175">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="b6169-176">$ {ROWSPAN2} $**Security**$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6169-176">${ROWSPAN2}$**Security**${REMOVE}$</span></span>  

<span data-ttu-id="b6169-177">家長監護 & 篩選</span><span class="sxs-lookup"><span data-stu-id="b6169-177">Parental Control & Filters</span></span>

<span data-ttu-id="b6169-178">強制執行為網際網路存取和使用所建立的規則和限制</span><span class="sxs-lookup"><span data-stu-id="b6169-178">Enforce rules and restrictions established for Internet access and usage</span></span>

<span data-ttu-id="b6169-179">**啟動**</span><span class="sxs-lookup"><span data-stu-id="b6169-179">**Startup**</span></span>

<span data-ttu-id="b6169-180">設定和管理</span><span class="sxs-lookup"><span data-stu-id="b6169-180">Configuration & Management</span></span>

<span data-ttu-id="b6169-181">允許使用者控制系統安全性監視的診斷和修復選項，以通知使用者發現和安全性動作</span><span class="sxs-lookup"><span data-stu-id="b6169-181">Allow users to control diagnostic and remediation options for system security monitoring Notify users of findings and security actions</span></span>

<span data-ttu-id="b6169-182">**與使用者互動的 Windows Store 應用程式**</span><span class="sxs-lookup"><span data-stu-id="b6169-182">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="b6169-183">**通訊 & 網際網路** (IM & VoIP) </span><span class="sxs-lookup"><span data-stu-id="b6169-183">**Communication & Internet** (IM & VoIP)</span></span>

<span data-ttu-id="b6169-184">傳送和接收訊息和呼叫</span><span class="sxs-lookup"><span data-stu-id="b6169-184">Send and receive messages and calls</span></span>

<span data-ttu-id="b6169-185">**Windows Store 應用程式**</span><span class="sxs-lookup"><span data-stu-id="b6169-185">**Windows Store app**</span></span>

<span data-ttu-id="b6169-186">**音樂 & MP3**</span><span class="sxs-lookup"><span data-stu-id="b6169-186">**Music & MP3**</span></span>

<span data-ttu-id="b6169-187">播放、儲存和管理音樂</span><span class="sxs-lookup"><span data-stu-id="b6169-187">Play, store, and manage music</span></span>

<span data-ttu-id="b6169-188">**Windows Store 應用程式**</span><span class="sxs-lookup"><span data-stu-id="b6169-188">**Windows Store app**</span></span>

<span data-ttu-id="b6169-189">**相片 & 影片**</span><span class="sxs-lookup"><span data-stu-id="b6169-189">**Photo & Video**</span></span>

<span data-ttu-id="b6169-190">偵測、錄製、轉譯、儲存及管理相片和影片</span><span class="sxs-lookup"><span data-stu-id="b6169-190">Detect, record, render, store and manage photos and videos</span></span>

<span data-ttu-id="b6169-191">**Windows Store 應用程式**</span><span class="sxs-lookup"><span data-stu-id="b6169-191">**Windows Store app**</span></span>

<span data-ttu-id="b6169-192">**電腦遊戲**</span><span class="sxs-lookup"><span data-stu-id="b6169-192">**PC Gaming**</span></span>

<span data-ttu-id="b6169-193">跨不同網域啟動遊戲</span><span class="sxs-lookup"><span data-stu-id="b6169-193">Launch games across various domains</span></span>

<span data-ttu-id="b6169-194">**Windows Store 應用程式**</span><span class="sxs-lookup"><span data-stu-id="b6169-194">**Windows Store app**</span></span>

<span data-ttu-id="b6169-195">**銷售 & 公告**</span><span class="sxs-lookup"><span data-stu-id="b6169-195">**Upsell & Advertisement**</span></span>

<span data-ttu-id="b6169-196">特別注意可供購買的商品和服務</span><span class="sxs-lookup"><span data-stu-id="b6169-196">Draw attention to goods and services available for purchase</span></span>

<span data-ttu-id="b6169-197">**移除**</span><span class="sxs-lookup"><span data-stu-id="b6169-197">**Remove**</span></span>



 

> [!Note]  
> <span data-ttu-id="b6169-198">協助工具應用程式指導方針是與 Isv 的個別直接合作所涵蓋。</span><span class="sxs-lookup"><span data-stu-id="b6169-198">Accessibility apps guidelines are covered by separate direct engagements with ISVs.</span></span> <span data-ttu-id="b6169-199">如需詳細資訊，請參閱輕鬆存取的程式 [*設計*](../winauto/ease-of-access---assistive-technology-registration.md) 。</span><span class="sxs-lookup"><span data-stu-id="b6169-199">See [*Programming for Ease of Access*](../winauto/ease-of-access---assistive-technology-registration.md) for details.</span></span>

 

<span data-ttu-id="b6169-200">**Windows 市集應用程式**</span><span class="sxs-lookup"><span data-stu-id="b6169-200">**Windows Store apps**</span></span>

<span data-ttu-id="b6169-201">Windows Store 應用程式使用新的座標引進 Windows 空間，以增強使用者體驗：新的應用程式模型、新的使用者介面，以及 Windows 存放區。</span><span class="sxs-lookup"><span data-stu-id="b6169-201">Windows Store apps enhance the user experience by introducing a Windows space with new coordinates: a new app model, a new user interface, and a Windows Store.</span></span> <span data-ttu-id="b6169-202">您可以使用這些語言和展示架構選項來開發 Windows Store 應用程式：</span><span class="sxs-lookup"><span data-stu-id="b6169-202">These language and presentation framework options are available for developing Windows Store apps:</span></span>

-   <span data-ttu-id="b6169-203">HTML/JavaScript/CSS</span><span class="sxs-lookup"><span data-stu-id="b6169-203">HTML/JavaScript/CSS</span></span>
-   <span data-ttu-id="b6169-204">XAML/C#</span><span class="sxs-lookup"><span data-stu-id="b6169-204">XAML/C#</span></span>
-   <span data-ttu-id="b6169-205">XAML/C + +</span><span class="sxs-lookup"><span data-stu-id="b6169-205">XAML/C++</span></span>

<span data-ttu-id="b6169-206">您可以在 [Windows 開發人員中心](https://msdn.microsoft.com/windows/apps/)取得開發 Windows Store 應用程式的匯總資訊。</span><span class="sxs-lookup"><span data-stu-id="b6169-206">Aggregated info for developing Windows Store apps is available at the [Windows Dev Center](https://msdn.microsoft.com/windows/apps/).</span></span>

<span data-ttu-id="b6169-207">範例：</span><span class="sxs-lookup"><span data-stu-id="b6169-207">Examples:</span></span>

-   <span data-ttu-id="b6169-208">[開發 Windows Store 遊戲](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="b6169-208">[Developing Windows Store games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="b6169-209">[開發使用媒體的 Windows Store 應用程式](/previous-versions/windows/apps/hh465132(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="b6169-209">[Developing Windows Store app that use Media](/previous-versions/windows/apps/hh465132(v=win.10))</span></span>

<span data-ttu-id="b6169-210">**自動維護工作**</span><span class="sxs-lookup"><span data-stu-id="b6169-210">**Automatic maintenance tasks**</span></span>

<span data-ttu-id="b6169-211">定期背景活動應設計為自動維護工作。</span><span class="sxs-lookup"><span data-stu-id="b6169-211">Periodic background activity should be designed as Automatic Maintenance tasks.</span></span> <span data-ttu-id="b6169-212">這些會在系統閒置時間排程，以增加 Windows 電腦的回應能力和能源效率。</span><span class="sxs-lookup"><span data-stu-id="b6169-212">These are scheduled at system idle time to increase the responsiveness and energy efficiency of Windows PCs.</span></span> <span data-ttu-id="b6169-213">您可以使用桌面 SDK，在安裝期間由傳統型應用程式建立和設定維護工作。</span><span class="sxs-lookup"><span data-stu-id="b6169-213">Maintenance tasks can be created and configured by a desktop app at install time, using the desktop SDK.</span></span> <span data-ttu-id="b6169-214">如需詳細資訊，請參閱下面的自動維護主題。</span><span class="sxs-lookup"><span data-stu-id="b6169-214">See the Automatic Maintenance topic that follows for details.</span></span>

## <a name="resources"></a><span data-ttu-id="b6169-215">資源</span><span class="sxs-lookup"><span data-stu-id="b6169-215">Resources</span></span>

-   [<span data-ttu-id="b6169-216">協助工具指導方針</span><span class="sxs-lookup"><span data-stu-id="b6169-216">Accessibility Guidelines</span></span>](../winauto/ease-of-access---assistive-technology-registration.md)
-   [<span data-ttu-id="b6169-217">Windows 開發人員中心</span><span class="sxs-lookup"><span data-stu-id="b6169-217">Windows Dev Center</span></span>](https://msdn.microsoft.com/windows/apps/)
-   <span data-ttu-id="b6169-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="b6169-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span></span>

 

