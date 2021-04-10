---
title: 關於 BITS
description: 使用背景智慧型傳送服務 (位) 在用戶端與伺服器之間非同步傳送檔案。
ms.assetid: 056007f4-6a71-4f8e-bf7d-17ed87088edf
keywords:
- 背景智慧型傳送服務，說明
- 傳送佇列位
- 傳送佇列位，節流
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b1ac0f587b496692ec1c2e62be06c0e64766a205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092771"
---
# <a name="about-bits"></a><span data-ttu-id="447fe-106">關於 BITS</span><span class="sxs-lookup"><span data-stu-id="447fe-106">About BITS</span></span>

<span data-ttu-id="447fe-107">使用背景智慧型傳送服務 (位) 從檔案下載檔案，或將檔案上傳至 HTTP 網頁伺服器或 SMB 檔案伺服器。</span><span class="sxs-lookup"><span data-stu-id="447fe-107">Use Background Intelligent Transfer Service (BITS) to download files from or upload files to HTTP web servers or SMB file servers.</span></span> 

<span data-ttu-id="447fe-108">只要起始傳送的使用者仍處於登入狀態，並維護網路連線，BITS 會在應用程式結束之後繼續傳輸檔案。</span><span class="sxs-lookup"><span data-stu-id="447fe-108">BITS continues to transfer files after an application exits as long as the user who initiated the transfer remains logged on and a network connection is maintained.</span></span> <span data-ttu-id="447fe-109">BITS 不會強制網路連接。</span><span class="sxs-lookup"><span data-stu-id="447fe-109">BITS will not force a network connection.</span></span> <span data-ttu-id="447fe-110">BITS 會在已中斷的網路連線重新建立之後，或在登出登入的使用者之後，繼續傳輸。</span><span class="sxs-lookup"><span data-stu-id="447fe-110">BITS resumes transfers after a network connection that had been lost is reestablished or after a user who had logged off logs back in.</span></span> <span data-ttu-id="447fe-111">如需詳細資訊，請參閱 [使用者和網路連接](users-and-network-connections.md)。</span><span class="sxs-lookup"><span data-stu-id="447fe-111">For more information, see [Users and Network Connections](users-and-network-connections.md).</span></span>

<span data-ttu-id="447fe-112">BITS 會留意目前的網路成本和擁塞，讓背景工作在使用使用者的前景體驗時可能會干擾到最少。</span><span class="sxs-lookup"><span data-stu-id="447fe-112">BITS is mindful of the current network cost and congestion so that a background job interferes as little as possible with the user's foreground experience.</span></span> <span data-ttu-id="447fe-113">BITS 會使用閒置的 [網路頻寬](network-bandwidth.md) 來傳輸檔案，並根據可用的閒置網路頻寬量來增加或減少傳輸檔案的速率。</span><span class="sxs-lookup"><span data-stu-id="447fe-113">BITS uses idle [network bandwidth](network-bandwidth.md) to transfer the files and will increase or decrease the rate at which files are transferred based on the amount of idle network bandwidth available.</span></span> <span data-ttu-id="447fe-114">如果網路應用程式開始佔用較多頻寬，BITS 便會降低其傳送速率，以保持使用者的互動體驗。</span><span class="sxs-lookup"><span data-stu-id="447fe-114">If a network application begins to consume more bandwidth, BITS decreases its transfer rate to preserve the user's interactive experience.</span></span> <span data-ttu-id="447fe-115">BITS 會使用應用程式指定的 [傳輸原則](how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md) 來防止檔案在有成本的網路連線上傳輸。</span><span class="sxs-lookup"><span data-stu-id="447fe-115">BITS uses app-specified [transfer policies](how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md) to prevent files from transferring on costed network connections.</span></span>

<span data-ttu-id="447fe-116">位也會留意電源使用量。</span><span class="sxs-lookup"><span data-stu-id="447fe-116">BITS is also mindful of power usage.</span></span> <span data-ttu-id="447fe-117">從 Windows 10 2019 年5月更新開始，BITS 會在電腦處於 [新式待命](/windows-hardware/design/device-experiences/modern-standby) 模式且電腦已插入電源時傳輸檔案。</span><span class="sxs-lookup"><span data-stu-id="447fe-117">Starting with the Windows 10 May 2019 Update, BITS will transfer files when the machine is in [Modern Standby](/windows-hardware/design/device-experiences/modern-standby) mode and the machine is plugged in.</span></span>

<span data-ttu-id="447fe-118">BITS 應用程式可使用不同的位 [優先權層級](/windows/desktop/api/Bits/ne-bits-bg_job_priority) ，讓 bits 以智慧方式挑選要執行的傳送作業。</span><span class="sxs-lookup"><span data-stu-id="447fe-118">The BITS application can use the different BITS [priority levels](/windows/desktop/api/Bits/ne-bits-bg_job_priority) to let BITS intelligently pick which transfer jobs to run.</span></span> <span data-ttu-id="447fe-119">優先順序較高的工作優先於優先順序較低的工作。</span><span class="sxs-lookup"><span data-stu-id="447fe-119">Higher priority jobs preempt lower priority jobs.</span></span> <span data-ttu-id="447fe-120">優先順序層級相同的工作則會共用傳送時間，如此可防止傳送佇列中的某個大型工作阻擋其他幾個小型工作。</span><span class="sxs-lookup"><span data-stu-id="447fe-120">Jobs at the same priority level share transfer time, which prevents a large job from blocking small jobs in the transfer queue.</span></span> <span data-ttu-id="447fe-121">直到所有優先順序較高的工作都完成或處於錯誤狀態後，優先順序較低的工作才能接收傳送時間。</span><span class="sxs-lookup"><span data-stu-id="447fe-121">Lower priority jobs do not receive transfer time until all higher priority jobs are complete or in an error state.</span></span>

<span data-ttu-id="447fe-122">BITS 會使用 Windows BranchCache 進行對等快取。</span><span class="sxs-lookup"><span data-stu-id="447fe-122">BITS uses Windows BranchCache for peer caching.</span></span> <span data-ttu-id="447fe-123">如需詳細資訊，請參閱 [BranchCache 總覽](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="447fe-123">For more information, see the [BranchCache Overview](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10)).</span></span>

<span data-ttu-id="447fe-124">通用 Windows 平臺 (UWP) 開發人員應該使用 [Windows.networking.backgroundtransfer.contentprefetcher](/uwp/api/Windows.Networking.BackgroundTransfer) API，而不是 BITS api。</span><span class="sxs-lookup"><span data-stu-id="447fe-124">Universal Windows Platform (UWP) developers should use the [Windows.Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) API and not the BITS API.</span></span>

<span data-ttu-id="447fe-125">有三種類型的 [**傳送作業**](/windows/desktop/api/Bits/ne-bits-bg_job_type)。</span><span class="sxs-lookup"><span data-stu-id="447fe-125">There are three types of [**transfer jobs**](/windows/desktop/api/Bits/ne-bits-bg_job_type).</span></span> <span data-ttu-id="447fe-126">下載作業會將檔案下載到用戶端、上傳作業會將檔案上傳到伺服器，而上傳-回復作業會將檔案上傳至伺服器，並從伺服器應用程式接收回複檔案。</span><span class="sxs-lookup"><span data-stu-id="447fe-126">A download job downloads files to the client, an upload job uploads a file to the server, and an upload-reply job uploads a file to the server and receives a reply file from the server application.</span></span>

<span data-ttu-id="447fe-127">下列主題提供更多有關 BITS 的詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="447fe-127">The following topics provide more detailed information about BITS:</span></span>

-   [<span data-ttu-id="447fe-128">驗證</span><span class="sxs-lookup"><span data-stu-id="447fe-128">Authentication</span></span>](authentication.md)
-   [<span data-ttu-id="447fe-129">BITS 工作的生命週期</span><span class="sxs-lookup"><span data-stu-id="447fe-129">Life Cycle of a BITS Job</span></span>](life-cycle-of-a-bits-job.md)
-   [<span data-ttu-id="447fe-130">使用者和網路連接</span><span class="sxs-lookup"><span data-stu-id="447fe-130">Users and Network Connections</span></span>](users-and-network-connections.md)
-   [<span data-ttu-id="447fe-131">網路頻寬</span><span class="sxs-lookup"><span data-stu-id="447fe-131">Network Bandwidth</span></span>](network-bandwidth.md)
-   [<span data-ttu-id="447fe-132">群組原則</span><span class="sxs-lookup"><span data-stu-id="447fe-132">Group Policies</span></span>](group-policies.md)
-   [<span data-ttu-id="447fe-133">服務帳戶和 BITS</span><span class="sxs-lookup"><span data-stu-id="447fe-133">Service Accounts and BITS</span></span>](service-accounts-and-bits.md)
-   [<span data-ttu-id="447fe-134">BITS 傳送工作的協助程式權杖</span><span class="sxs-lookup"><span data-stu-id="447fe-134">Helper Tokens for BITS Transfer Jobs</span></span>](helper-tokens-for-bits-transfer-jobs.md)
-   [<span data-ttu-id="447fe-135">檔案傳輸一致性</span><span class="sxs-lookup"><span data-stu-id="447fe-135">File Transfer Consistency</span></span>](file-transfer-consistency.md)
-   [<span data-ttu-id="447fe-136">BITS 下載的 HTTP 需求</span><span class="sxs-lookup"><span data-stu-id="447fe-136">HTTP Requirements for BITS Downloads</span></span>](http-requirements-for-bits-downloads.md)
-   [<span data-ttu-id="447fe-137">BITS 上傳的 IIS 需求</span><span class="sxs-lookup"><span data-stu-id="447fe-137">IIS Requirements for BITS Uploads</span></span>](iis-requirements-for-bits-uploads.md)
-   [<span data-ttu-id="447fe-138">虛擬目錄清理</span><span class="sxs-lookup"><span data-stu-id="447fe-138">Virtual Directory Cleanup</span></span>](virtual-directory-cleanup.md)
-   [<span data-ttu-id="447fe-139">BITS 和系統還原</span><span class="sxs-lookup"><span data-stu-id="447fe-139">BITS and System Restore</span></span>](bits-and-system-restore.md)
-   [<span data-ttu-id="447fe-140">BITS 啟動類型</span><span class="sxs-lookup"><span data-stu-id="447fe-140">BITS Startup Type</span></span>](bits-startup-type.md)
-   [<span data-ttu-id="447fe-141">網際網路連線共用</span><span class="sxs-lookup"><span data-stu-id="447fe-141">Internet Connection Sharing</span></span>](internet-connection-sharing.md)
-   [<span data-ttu-id="447fe-142">對等快取</span><span class="sxs-lookup"><span data-stu-id="447fe-142">Peer Caching</span></span>](peer-caching.md)
-   [<span data-ttu-id="447fe-143">BITS 安全性、權杖和系統管理員帳戶</span><span class="sxs-lookup"><span data-stu-id="447fe-143">BITS Security, Tokens, and Administrator Accounts</span></span>](user-account-control-and-bits.md)
-   [<span data-ttu-id="447fe-144">BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="447fe-144">BITS Compact Server</span></span>](bits-compact-server.md)

<span data-ttu-id="447fe-145">使用 BITS [介面](bits-interfaces.md) 撰寫用來建立和監視傳送作業的應用程式。</span><span class="sxs-lookup"><span data-stu-id="447fe-145">Use the BITS [interfaces](bits-interfaces.md) to write applications that create and monitor transfer jobs.</span></span> <span data-ttu-id="447fe-146">如需使用 BITS 介面的詳細資訊，請參閱 [使用 bits](using-bits.md)。</span><span class="sxs-lookup"><span data-stu-id="447fe-146">For details on using the BITS interfaces, see [Using BITS](using-bits.md).</span></span>