---
title: 新功能 (BITS)
description: 下表指出背景智慧型傳送服務 (位) 的每個版本的新功能。
ms.assetid: ef05f2e1-88be-4adb-aca7-a7b1451cfd04
keywords:
- 新功能位
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b171a1d8cede9e3fd49ac81ab47ffb09f72b6200
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024409"
---
# <a name="whats-new-bits"></a><span data-ttu-id="48ce0-104">新功能 (BITS)</span><span class="sxs-lookup"><span data-stu-id="48ce0-104">What's New (BITS)</span></span>

<span data-ttu-id="48ce0-105">因為它的第一個版本是 Windows XP 的一部分，所以背景智慧型傳送服務 (位) 持續改進，為開發人員和系統管理員新增更強大的控制項，以控制及管理下載。</span><span class="sxs-lookup"><span data-stu-id="48ce0-105">Since its first release as part of Windows XP, the Background Intelligent Transfer Service (BITS) has been constantly improved, adding more powerful controls for the developer and admin to control and manage downloads.</span></span> <span data-ttu-id="48ce0-106">已新增一組豐富的 PowerShell Cmdlet;它可以連接到更多類型的 HTTP 伺服器;比以往更小心的是使用者的網路頻寬和成本。</span><span class="sxs-lookup"><span data-stu-id="48ce0-106">A rich set of PowerShell cmdlets has been added; it can connect to more types of HTTP servers; it's more careful of the user's network bandwidth and costs than ever before.</span></span> 

<span data-ttu-id="48ce0-107">下表指出背景智慧型傳送服務 (位) 的每個版本的新功能。</span><span class="sxs-lookup"><span data-stu-id="48ce0-107">The following table identifies what is new for each release of Background Intelligent Transfer Service (BITS).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48ce0-108">版本</span><span class="sxs-lookup"><span data-stu-id="48ce0-108">Version</span></span></th>
<th><span data-ttu-id="48ce0-109">功能描述</span><span class="sxs-lookup"><span data-stu-id="48ce0-109">Description of features</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48ce0-110">版本10。3</span><span class="sxs-lookup"><span data-stu-id="48ce0-110">Version 10.3</span></span></td>
<td><span data-ttu-id="48ce0-111">新功能︰</span><span class="sxs-lookup"><span data-stu-id="48ce0-111">New features:</span></span><br/>
<ul>
<li><span data-ttu-id="48ce0-112">已新增 <a href="/windows/win32/api/bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3"><strong>BackgroundCopyJobHttpOptions3</strong></a> ，以將 HTTP 標頭標示為僅限寫入，以及設定伺服器憑證驗證回呼。</span><span class="sxs-lookup"><span data-stu-id="48ce0-112">Added <a href="/windows/win32/api/bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3"><strong>BackgroundCopyJobHttpOptions3</strong></a> to mark HTTP headers as write-only, and to set a server certificate validation callback.</span></span></li>
<li><span data-ttu-id="48ce0-113">BITS 會在其他系統服務建立時保留其服務識別。</span><span class="sxs-lookup"><span data-stu-id="48ce0-113">BITS will retain its service identity when created by another system service.</span></span></li>
<li><span data-ttu-id="48ce0-114">只要裝置已插入，BITS 將繼續在連線的待命上傳輸檔案。</span><span class="sxs-lookup"><span data-stu-id="48ce0-114">BITS will continue to transfer files on connected standby as long as the device is plugged in.</span></span></li>
</ul>
<span data-ttu-id="48ce0-115">BITS 10.3 版包含在 Windows 10 2019 年5月更新 (10.0;組建 18362) 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="48ce0-115">BITS version 10.3 is included in the Windows 10 May 2019 Update (10.0; Build 18362), and later.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="48ce0-116">版本10。2</span><span class="sxs-lookup"><span data-stu-id="48ce0-116">Version 10.2</span></span></td>
<td><span data-ttu-id="48ce0-117">新功能︰</span><span class="sxs-lookup"><span data-stu-id="48ce0-117">New features:</span></span><br/>
<ul>
<li><span data-ttu-id="48ce0-118">已新增 <a href="/windows/win32/api/bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2"><strong>BackgroundCopyJobHttpOptions2</strong></a> 來變更 HTTP 下載的 HTTP 方法。</span><span class="sxs-lookup"><span data-stu-id="48ce0-118">Added <a href="/windows/win32/api/bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2"><strong>BackgroundCopyJobHttpOptions2</strong></a> to change the HTTP method for HTTP downloads.</span></span></li>
<li><span data-ttu-id="48ce0-119">BITS 現在會使用預設 proxy 順序，與系統的其餘部分一致。</span><span class="sxs-lookup"><span data-stu-id="48ce0-119">BITS now uses the default proxy ordering to be more consistent with the rest of the system.</span></span></li>
<li><span data-ttu-id="48ce0-120">程式設計人員可以更輕鬆地為企業案例設定 BITS proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="48ce0-120">It's easier for programmers to set BITS proxy configuration for enterprise scenarios.</span></span></li>
<li><span data-ttu-id="48ce0-121">BITS 現在比較小心，並支援 [新式待命](/windows-hardware/design/device-experiences/modern-standby)。</span><span class="sxs-lookup"><span data-stu-id="48ce0-121">BITS is now more careful of power and supports [Modern Standby](/windows-hardware/design/device-experiences/modern-standby).</span></span></li>
<li><span data-ttu-id="48ce0-122">除了[群組原則](./group-policies)之外，BITS 現在還支援行動裝置管理員 (MDM) [原則](/windows/client-management/mdm/policy-configuration-service-provider)。</span><span class="sxs-lookup"><span data-stu-id="48ce0-122">BITS now support Mobile device manager (MDM) [policies](/windows/client-management/mdm/policy-configuration-service-provider) in addition to [group policies](./group-policies).</span></span></li>
</ul>
<span data-ttu-id="48ce0-123">BITS 10.2 版包含在 Windows 10 2018 年10月更新 (10.0;組建 17763) 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="48ce0-123">BITS version 10.2 is included in Windows 10 October 2018 Update(10.0; Build 17763), and later.</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48ce0-124">版本10。1</span><span class="sxs-lookup"><span data-stu-id="48ce0-124">Version 10.1</span></span></td>
<td><span data-ttu-id="48ce0-125">新功能︰</span><span class="sxs-lookup"><span data-stu-id="48ce0-125">New features:</span></span><br/>
<ul>
<li><span data-ttu-id="48ce0-126">已新增 <a href="/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6"><strong>BackgroundCopyFile6</strong></a> 和 <a href="/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3"><strong>IBackgroundCopyCallback3</strong></a> ，以啟用 HTTP 下載的隨機存取案例。</span><span class="sxs-lookup"><span data-stu-id="48ce0-126">Added <a href="/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6"><strong>BackgroundCopyFile6</strong></a> and <a href="/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3"><strong>IBackgroundCopyCallback3</strong></a> to enable  random-access scenarios for HTTP downloads.</span></span></li>
<li><span data-ttu-id="48ce0-127">新增 <strong>BITS_JOB_PROPERTY_ON_DEMAND_MODE</strong> 並 <strong>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS</strong> 至 <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a> 列舉，以分別調整下載和通知行為。</span><span class="sxs-lookup"><span data-stu-id="48ce0-127">Added <strong>BITS_JOB_PROPERTY_ON_DEMAND_MODE</strong> and <strong>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS</strong> to the <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a> enumeration to tweak download and notification behaviors, respectively.</span></span></li>
</ul>
<span data-ttu-id="48ce0-128">BITS 10.1 版包含在 Windows 10 Creator 的 Update 和更新版本中。</span><span class="sxs-lookup"><span data-stu-id="48ce0-128">BITS version 10.1 is included in Windows 10 Creator's Update and later.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="48ce0-129">版本 5.0</span><span class="sxs-lookup"><span data-stu-id="48ce0-129">Version 5.0</span></span></td>
<td><span data-ttu-id="48ce0-130">新功能︰</span><span class="sxs-lookup"><span data-stu-id="48ce0-130">New features:</span></span><br/>
<ul>
<li><span data-ttu-id="48ce0-131">加入 <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> 介面，這個介面會將用來取得和設定 BITS 工作屬性的泛型方法，新增至繼承自 <a href="/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4"><strong>IBackgroundCopyJob4</strong></a> 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="48ce0-131">Added the <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> interface which adds generic methods for getting and setting BITS job properties to the methods inherited from the <a href="/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4"><strong>IBackgroundCopyJob4</strong></a> interface.</span></span><br/> <span data-ttu-id="48ce0-132">如需使用新 <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> 介面的相關資訊，請參閱如何控制是否允許在 bits 下載作業中，透過 <a href="how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md">昂貴的連接來下載 bits 作業</a> ，以及 <a href="how-to-get-the-last-set-of-http-headers-received-for-each-file-in-a-bits-download-job.md">如何取得每個檔案所收到的最後一組 HTTP 標頭</a>。</span><span class="sxs-lookup"><span data-stu-id="48ce0-132">For information on using the new <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> interface, see <a href="how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md">How to control whether a BITS job is allowed to download over an expensive connection</a> and <a href="how-to-get-the-last-set-of-http-headers-received-for-each-file-in-a-bits-download-job.md">How to get the last set of HTTP headers received for each file in a BITS download job</a>.</span></span><br/></li>
<li><span data-ttu-id="48ce0-133">加入 <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_job_property_value"><strong>BITS_JOB_PROPERTY_VALUE</strong></a> 聯集和 <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a>，以及 <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_transfer_policy"><strong>BITS_JOB_TRANSFER_POLICY</strong></a> 列舉。</span><span class="sxs-lookup"><span data-stu-id="48ce0-133">Added the <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_job_property_value"><strong>BITS_JOB_PROPERTY_VALUE</strong></a> union and the <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a>, and <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_transfer_policy"><strong>BITS_JOB_TRANSFER_POLICY</strong></a> enumerations.</span></span> <span data-ttu-id="48ce0-134">如需使用範例，請參閱上述的 how to 主題。</span><span class="sxs-lookup"><span data-stu-id="48ce0-134">For usage examples, see the above How to topics.</span></span></li>
<li><span data-ttu-id="48ce0-135">加入 <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> 介面，這會新增方法，以在 BackgroundCopyFile 物件上取得和設定泛型屬性至繼承自 <a href="/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4"><strong>IBackgroundCopyFile4</strong></a> 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="48ce0-135">Added the <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> interface, which adds methods for getting and setting generic properties on BackgroundCopyFile objects to the methods inherited from the <a href="/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4"><strong>IBackgroundCopyFile4</strong></a> interface.</span></span> <span data-ttu-id="48ce0-136">新增泛型屬性可讓您在未來增強 BackgroundCopyFile 功能，而不需要建立新的介面。</span><span class="sxs-lookup"><span data-stu-id="48ce0-136">The addition of generic properties will make it possible to enhance BackgroundCopyFile capabilities in the future without requiring that a new interface be created.</span></span></li>
<li><span data-ttu-id="48ce0-137"><a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a>所公開的第一個泛型屬性是<strong>HttpResponseHeaders</strong>屬性。</span><span class="sxs-lookup"><span data-stu-id="48ce0-137">The first generic property exposed by <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> is the <strong>HttpResponseHeaders</strong> property.</span></span></li>
<li><span data-ttu-id="48ce0-138">加入 <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value"><strong>BITS_FILE_PROPERTY_VALUE</strong></a> 聯集和 <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_file_property_id"><strong>BITS_FILE_PROPERTY_ID</strong></a> 列舉。</span><span class="sxs-lookup"><span data-stu-id="48ce0-138">Added the <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value"><strong>BITS_FILE_PROPERTY_VALUE</strong></a> union and the <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_file_property_id"><strong>BITS_FILE_PROPERTY_ID</strong></a> enumeration.</span></span></li>
</ul>
<span data-ttu-id="48ce0-139">BITS 5.0 版包含在 Windows Server 2012 和 Windows 8 作業系統中，其中% windir% \System32\QMgr.dll 的版本是 7.7. xxxx &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="48ce0-139">BITS version 5.0 is included in the Windows Server 2012 and Windows 8 operating systems, where the version of %windir%\System32\QMgr.dll is &quot;7.7.xxxx.xxxx&quot;.</span></span><br/> <span data-ttu-id="48ce0-140">下列功能已新增至 Windows 10 中的位</span><span class="sxs-lookup"><span data-stu-id="48ce0-140">The following features were added to BITS in Windows 10</span></span><br/>
<ul>
<li><span data-ttu-id="48ce0-141">在 Windows 10 1607 版中，您可以使用 BITS COM Api 和 BITS PowerShell Cmdlet， (可在 PowerShell 遠端會話中使用) 。</span><span class="sxs-lookup"><span data-stu-id="48ce0-141">In Windows 10, version 1607, it is possible to use the BITS COM APIs and BITS PowerShell cmdlets (where available) in a PowerShell Remote Session.</span></span> <span data-ttu-id="48ce0-142">這在管理沒有本機登入功能的 Windows Server 2016 版本時特別有用。</span><span class="sxs-lookup"><span data-stu-id="48ce0-142">This is especially useful when administrating versions of Windows Server 2016 that have no local login capability.</span></span> <span data-ttu-id="48ce0-143">BITS 工作是透過在工作階段使用者帳戶內容中執行的 PowerShell 遠端工作階段啟動，並只會在至少有一個和該使用者帳戶關聯的作用中本機登入工作階段或 PowerShell 遠端工作階段時，才會呈現進度。</span><span class="sxs-lookup"><span data-stu-id="48ce0-143">BITS jobs started via PowerShell Remote Sessions run in the session's user account context, and will only make progress when there is at least on active local logon session or PowerShell Remote session associated with that user account.</span></span> <span data-ttu-id="48ce0-144">請考慮使用持續性的 PowerShell 遠端會話 (參閱 <a href="/powershell/module/microsoft.powershell.core/new-pssession">新的 PSSession</a>) 以進行長時間執行的傳送。</span><span class="sxs-lookup"><span data-stu-id="48ce0-144">Consider using persistent PowerShell Remote sessions (see <a href="/powershell/module/microsoft.powershell.core/new-pssession">New-PSSession</a>) for long-running transfers.</span></span></li>
<li><span data-ttu-id="48ce0-145">在 Windows 10 1607 版中，只要協助程式權杖沒有系統管理員功能，BITS 作業擁有者就可以在不是系統管理員的情況下設定 helper 權杖。</span><span class="sxs-lookup"><span data-stu-id="48ce0-145">In Windows 10, version 1607, it is now possible for a BITS job owner to set helper tokens without being an administrator, as long as the helper token does not have administrator capabilities.</span></span> <span data-ttu-id="48ce0-146">這將能透過讓背景下載或更新工具在具有較低權限的 NetworkService 帳戶 (而非具有系統管理員權限的帳戶) 下執行，來降低背景下載或更新工具的弱點數量。</span><span class="sxs-lookup"><span data-stu-id="48ce0-146">This reduces the vulnerability footprint of background download or update tools by enabling them to run under the lower-privileged NetworkService account rather than under an account with administrative privileges.</span></span></li>
</ul>
<span data-ttu-id="48ce0-147">BITS 5.0 版也包含在 Windows 10 中，其中% windir% \System32\QMgr.dll 的版本是 7.8. xxxx。 &quot; &quot;</span><span class="sxs-lookup"><span data-stu-id="48ce0-147">BITS version 5.0 is also included in Windows 10, where the version of %windir%\System32\QMgr.dll is &quot;7.8.xxxx.xxxx&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48ce0-148">4.0 版</span><span class="sxs-lookup"><span data-stu-id="48ce0-148">Version 4.0</span></span></td>
<td><span data-ttu-id="48ce0-149">新功能︰</span><span class="sxs-lookup"><span data-stu-id="48ce0-149">New features:</span></span><br/>
<ul>
<li><span data-ttu-id="48ce0-150">對等快取現在使用 Windows BranchCache。</span><span class="sxs-lookup"><span data-stu-id="48ce0-150">Peer caching now uses Windows BranchCache.</span></span> <span data-ttu-id="48ce0-151">這個新的對等快取模型會取代用於 BITS 3.0 版的模型。</span><span class="sxs-lookup"><span data-stu-id="48ce0-151">This new peer caching model replaces the model used for BITS version 3.0.</span></span> <span data-ttu-id="48ce0-152">如需詳細資訊，請參閱 <a href="peer-caching.md">對等</a>快取。</span><span class="sxs-lookup"><span data-stu-id="48ce0-152">For more information, see <a href="peer-caching.md">Peer Caching</a>.</span></span></li>
<li><span data-ttu-id="48ce0-153">新增更有彈性的資源存取模型，讓應用程式能夠將一組安全性權杖與 BITS 傳送工作產生關聯。</span><span class="sxs-lookup"><span data-stu-id="48ce0-153">Added a more flexible resource access model that allows applications to associate a pair of security tokens to a BITS transfer job.</span></span> <span data-ttu-id="48ce0-154">如需詳細資訊，請參閱 <a href="helper-tokens-for-bits-transfer-jobs.md">BITS 傳送工作的協助程式權杖</a>。</span><span class="sxs-lookup"><span data-stu-id="48ce0-154">For more information, see <a href="helper-tokens-for-bits-transfer-jobs.md">Helper tokens for BITS transfer jobs</a>.</span></span></li>
<li><span data-ttu-id="48ce0-155">新增 <a href="bits-compact-server.md">BITS Compact 伺服器</a>，這是一種獨立的 HTTP/HTTPS 檔案伺服器，可讓您在電腦之間以非同步方式傳輸有限數量的大型檔案。</span><span class="sxs-lookup"><span data-stu-id="48ce0-155">Added the <a href="bits-compact-server.md">BITS Compact Server</a>, which is a stand-alone HTTP/HTTPS file server that provides the ability to transfer a limited number of large files asynchronously between computers.</span></span></li>
<li><span data-ttu-id="48ce0-156">新增更細微的頻寬節流。</span><span class="sxs-lookup"><span data-stu-id="48ce0-156">Added more granular bandwidth throttling.</span></span> <span data-ttu-id="48ce0-157">如需詳細資訊，請參閱 <a href="group-policies.md">群組原則</a>。</span><span class="sxs-lookup"><span data-stu-id="48ce0-157">For more information, see <a href="group-policies.md">Group Policies</a>.</span></span></li>
</ul>
<span data-ttu-id="48ce0-158">BITS 4.0 版包含在 Windows Server 2008 R2 和 Windows 7 作業系統中。</span><span class="sxs-lookup"><span data-stu-id="48ce0-158">BITS version 4.0 is included in the Windows Server 2008 R2 and Windows 7 operating systems.</span></span><br/> <span data-ttu-id="48ce0-159">您也可以下載適用于 Windows Server 2008 Service Pack 2 (SP2) 、Windows Vista （含 Service Pack 1） (SP1) ，以及 Windows Vista （含 Service Pack 2 (SP2) ）的 BITS 4.0。</span><span class="sxs-lookup"><span data-stu-id="48ce0-159">You can also download BITS 4.0 for Windows Server 2008 with Service Pack 2 (SP2), Windows Vista with Service Pack 1 (SP1), and Windows Vista with Service Pack 2 (SP2).</span></span> <span data-ttu-id="48ce0-160">如需下載 BITS 4.0 的詳細資訊，請參閱 <a href="https://support.microsoft.com/kb/968929">KB968929</a>。</span><span class="sxs-lookup"><span data-stu-id="48ce0-160">For information about downloading BITS 4.0, see <a href="https://support.microsoft.com/kb/968929">KB968929</a>.</span></span><br/> <span data-ttu-id="48ce0-161">% Windir% \System32\QMgr.dll 的版本為 &quot; 7.5. xxxx &quot; 。</span><span class="sxs-lookup"><span data-stu-id="48ce0-161">The version of %windir%\System32\QMgr.dll is &quot;7.5.xxxx.xxxx&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48ce0-162">3.0 版</span><span class="sxs-lookup"><span data-stu-id="48ce0-162">Version 3.0</span></span></td>
<td><span data-ttu-id="48ce0-163">新功能︰</span><span class="sxs-lookup"><span data-stu-id="48ce0-163">New features:</span></span><br/>
<ul>
<li><span data-ttu-id="48ce0-164">新增 <a href="peer-caching.md">對等</a> 快取，可讓您從對等下載內容，也可以提供內容給網域網路中的對等。</span><span class="sxs-lookup"><span data-stu-id="48ce0-164">Added <a href="peer-caching.md">Peer Caching</a> which lets you download content from peers and also serve content to peers in a domain network.</span></span></li>
<li><span data-ttu-id="48ce0-165">已新增下載檔案時的 <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">通知</a> 。</span><span class="sxs-lookup"><span data-stu-id="48ce0-165">Added <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">notification</a> for when a file is downloaded.</span></span></li>
<li><span data-ttu-id="48ce0-166">在下載進行期間新增對 <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname">暫存檔案</a> 的存取權。</span><span class="sxs-lookup"><span data-stu-id="48ce0-166">Added access to the <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname">temporary file</a> while the download is in progress.</span></span></li>
<li><span data-ttu-id="48ce0-167">已新增控制 HTTP 重新 <a href="/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags">導向</a>的能力。</span><span class="sxs-lookup"><span data-stu-id="48ce0-167">Added the ability to control HTTP <a href="/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags">redirects</a>.</span></span></li>
<li><span data-ttu-id="48ce0-168">新增更多 <a href="group-policies.md">群組原則</a> 來控制對等快取和限制下載時間。</span><span class="sxs-lookup"><span data-stu-id="48ce0-168">Added more <a href="group-policies.md">group policies</a> to control peer caching and limit download times.</span></span></li>
<li><span data-ttu-id="48ce0-169">將診斷和疑難排解事件新增至系統事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="48ce0-169">Added diagnostic and troubleshooting events to the system event log.</span></span></li>
<li><span data-ttu-id="48ce0-170">已新增 (UAC) 的「 <a href="user-account-control-and-bits.md">使用者帳戶控制</a> 」支援。</span><span class="sxs-lookup"><span data-stu-id="48ce0-170">Added support for <a href="user-account-control-and-bits.md">User Account Control</a> (UAC).</span></span></li>
<li><span data-ttu-id="48ce0-171">在 Windows Vista 和更新版本上，預設的位啟動類型為延遲自動啟動。</span><span class="sxs-lookup"><span data-stu-id="48ce0-171">On Windows Vista and higher, the default BITS startup type is delayed auto-start.</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="48ce0-172">BITS 現在會使用群組原則來限制您可以建立的作業和檔案數目。</span><span class="sxs-lookup"><span data-stu-id="48ce0-172">BITS now uses group policies to limit the number of jobs and files you can create.</span></span> <span data-ttu-id="48ce0-173">這可能會影響目前建立大量作業或將大量檔案新增至作業的應用程式。</span><span class="sxs-lookup"><span data-stu-id="48ce0-173">This might affect applications that currently create a large number of jobs or add a large number of files to a job.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="48ce0-174">BITS 3.0 版包含在 Windows Server 2008 和 Windows Vista 作業系統中。</span><span class="sxs-lookup"><span data-stu-id="48ce0-174">BITS version 3.0 is included in the Windows Server 2008 and Windows Vista operating systems.</span></span> <br/> <span data-ttu-id="48ce0-175">% Windir% \System32\QMgr.dll 的版本為 &quot; 7.0. xxxx &quot; 。</span><span class="sxs-lookup"><span data-stu-id="48ce0-175">The version of %windir%\System32\QMgr.dll is &quot;7.0.xxxx.xxxx&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48ce0-176">版本2。5</span><span class="sxs-lookup"><span data-stu-id="48ce0-176">Version 2.5</span></span></td>
<td><span data-ttu-id="48ce0-177">新增對自訂 HTTP 標頭的支援、安全 HTTP 傳輸的憑證型用戶端驗證，以及 IPv6。</span><span class="sxs-lookup"><span data-stu-id="48ce0-177">Added support for custom HTTP headers, certificate-based client authentication for secure HTTP transports, and IPv6.</span></span> <span data-ttu-id="48ce0-178">此外，也新增了網際網路閘道裝置的使用 (IGD) 計數器，以更精確地計算可用的 <a href="network-bandwidth.md">頻寬</a>。</span><span class="sxs-lookup"><span data-stu-id="48ce0-178">Also added the use of Internet gateway device (IGD) counters to more accurately calculate available <a href="network-bandwidth.md">bandwidth</a>.</span></span><br/> <span data-ttu-id="48ce0-179">Windows Server 2008、Windows Vista 和 Windows XP Service Pack 3 (SP3) 作業系統都有提供 BITS 2.5 功能。</span><span class="sxs-lookup"><span data-stu-id="48ce0-179">The BITS 2.5 features are available in the Windows Server 2008, Windows Vista, and Windows XP with Service Pack 3 (SP3) operating systems.</span></span> <br/> <span data-ttu-id="48ce0-180">您也可以下載適用于 Windows Server 2003 （含 Service Pack 2）的 BITS 2.5 (SP2) 、Windows Server 2003 Service Pack 1 (SP1) 和 Windows XP Service Pack 2 (SP2) 。</span><span class="sxs-lookup"><span data-stu-id="48ce0-180">You can also download BITS 2.5 for Windows Server 2003 with Service Pack 2 (SP2), Windows Server 2003 with Service Pack 1 (SP1), and Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="48ce0-181">若要下載 BITS 2.5，請移至 <a href="https://www.microsoft.com/download/details.aspx?id=4933">Microsoft 下載中心</a> 並安裝 KB923845。</span><span class="sxs-lookup"><span data-stu-id="48ce0-181">To download BITS 2.5, go to the <a href="https://www.microsoft.com/download/details.aspx?id=4933">Microsoft Download Center</a> and install KB923845.</span></span><br/> <span data-ttu-id="48ce0-182">% Windir% \System32\QMgr.dll 的版本為 6.7. xxxx。 &quot; &quot;</span><span class="sxs-lookup"><span data-stu-id="48ce0-182">The version of %windir%\System32\QMgr.dll is &quot;6.7.xxxx.xxxx&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48ce0-183">版本2。0</span><span class="sxs-lookup"><span data-stu-id="48ce0-183">Version 2.0</span></span></td>
<td><span data-ttu-id="48ce0-184">已新增執行並行前景下載的支援、使用伺服器訊息區 (SMB) 遠端名稱的路徑、下載檔案範圍、變更遠端名稱的首碼或完整名稱，以及限制用戶端頻寬的使用。</span><span class="sxs-lookup"><span data-stu-id="48ce0-184">Added support for performing concurrent foreground downloads, using Server Message Block (SMB) paths for remote names, downloading ranges of a file, changing the prefix or complete name of a remote name, and limiting client bandwidth usage.</span></span> <span data-ttu-id="48ce0-185">JobInactivityTimeout 原則現在位於 [電腦設定]、[系統管理範本]、[網路] 背景智慧型傳送服務 (BITS) 下。</span><span class="sxs-lookup"><span data-stu-id="48ce0-185">The JobInactivityTimeout policy is now located under Computer Configuration, Administrative Templates, Network, Background Intelligent Transfer Service (BITS).</span></span><br/> <span data-ttu-id="48ce0-186">BITS 2.0 版包含在 Windows XP SP2 和 Windows Server 2003 SP1 中。</span><span class="sxs-lookup"><span data-stu-id="48ce0-186">BITS version 2.0 is included in Windows XP with SP2 and Windows Server 2003 with SP1.</span></span> <span data-ttu-id="48ce0-187">您也可以下載適用于 Windows Server 2003 和 Windows XP 的 BITS 2.0。</span><span class="sxs-lookup"><span data-stu-id="48ce0-187">You can also download BITS 2.0 for Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="48ce0-188">若要下載 BITS 2.0，請移至 <a href="https://www.microsoft.com/download/details.aspx?id=19031">Microsoft 下載中心</a> 並安裝 KB842773。</span><span class="sxs-lookup"><span data-stu-id="48ce0-188">To download BITS 2.0, go to the <a href="https://www.microsoft.com/download/details.aspx?id=19031">Microsoft Download Center</a> and install KB842773.</span></span><br/> <span data-ttu-id="48ce0-189">% Windir% \System32\QMgr.dll 的版本為 6.6. xxxx。 &quot; &quot;</span><span class="sxs-lookup"><span data-stu-id="48ce0-189">The version of %windir%\System32\QMgr.dll is &quot;6.6.xxxx.xxxx&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48ce0-190">1.5 版</span><span class="sxs-lookup"><span data-stu-id="48ce0-190">Version 1.5</span></span></td>
<td><span data-ttu-id="48ce0-191">已新增上傳和上傳-回復功能、事件的命令列執行，以及明確的認證和 proxy 認證。</span><span class="sxs-lookup"><span data-stu-id="48ce0-191">Added upload and upload-reply capability, command-line execution for events, and explicit credentials and proxy credentials.</span></span><br/> <span data-ttu-id="48ce0-192">從位1.5 開始，具有 <a href="/windows/win32/secauthz/restricted-tokens">受限權杖</a> 的使用者無法建立或修改作業。</span><span class="sxs-lookup"><span data-stu-id="48ce0-192">Starting with BITS 1.5, users with a <a href="/windows/win32/secauthz/restricted-tokens">restricted token</a> cannot create or modify jobs.</span></span><br/> <span data-ttu-id="48ce0-193">BITS 1.5 版包含在 Windows Server 2003 中。</span><span class="sxs-lookup"><span data-stu-id="48ce0-193">BITS version 1.5 is included in Windows Server 2003.</span></span> <span data-ttu-id="48ce0-194">您可以從 <a href="https://www.microsoft.com/download/details.aspx?id=22250">Microsoft 下載中心</a>取得適用于 Windows XP 的可轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="48ce0-194">A redistributable is available for Windows XP from the <a href="https://www.microsoft.com/download/details.aspx?id=22250">Microsoft Download Center</a>.</span></span><br/> <span data-ttu-id="48ce0-195">% Windir% \System32\QMgr.dll 的版本為 &quot; 6.5. &quot; xxxx。</span><span class="sxs-lookup"><span data-stu-id="48ce0-195">The version of %windir%\System32\QMgr.dll is &quot;6.5.xxxx.xxxx&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48ce0-196">版本1。2</span><span class="sxs-lookup"><span data-stu-id="48ce0-196">Version 1.2</span></span></td>
<td><span data-ttu-id="48ce0-197">與1.0 版相同的功能。</span><span class="sxs-lookup"><span data-stu-id="48ce0-197">Same functionality as version 1.0.</span></span> <span data-ttu-id="48ce0-198">包含內部升級和改進。</span><span class="sxs-lookup"><span data-stu-id="48ce0-198">Contains internal upgrades and improvements.</span></span><br/> <span data-ttu-id="48ce0-199">BITS 1.2 版包含在 Windows XP Service Pack 1 (SP1) 中。</span><span class="sxs-lookup"><span data-stu-id="48ce0-199">BITS version 1.2 is included in Windows XP with Service Pack 1 (SP1).</span></span><br/> <span data-ttu-id="48ce0-200">% Windir% \System32\QMgr.dll 的版本為 &quot; 6.2. &quot; xxxx。</span><span class="sxs-lookup"><span data-stu-id="48ce0-200">The version of %windir%\System32\QMgr.dll is &quot;6.2.xxxx.xxxx&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48ce0-201">版本 1.0</span><span class="sxs-lookup"><span data-stu-id="48ce0-201">Version 1.0</span></span></td>
<td><span data-ttu-id="48ce0-202">初始版本。</span><span class="sxs-lookup"><span data-stu-id="48ce0-202">Initial release.</span></span> <span data-ttu-id="48ce0-203">在背景或前景中提供優先順序、節流和非同步下載。</span><span class="sxs-lookup"><span data-stu-id="48ce0-203">Provides prioritized, throttled, and asynchronous downloads in the background or foreground.</span></span> <span data-ttu-id="48ce0-204">電腦重新開機和網路中斷連線之後，下載會自動繼續。</span><span class="sxs-lookup"><span data-stu-id="48ce0-204">The downloads automatically resume after computer restarts and network disconnects.</span></span><br/> <span data-ttu-id="48ce0-205">BITS 1.0 版包含在 Windows XP 中。</span><span class="sxs-lookup"><span data-stu-id="48ce0-205">BITS version 1.0 is included in Windows XP.</span></span><br/> <span data-ttu-id="48ce0-206">% Windir% \System32\QMgr.dll 的版本是 &quot; 6.0. xxxx &quot; 。</span><span class="sxs-lookup"><span data-stu-id="48ce0-206">The version of %windir%\System32\QMgr.dll is &quot;6.0.xxxx.xxxx&quot;.</span></span><br/></td>
</tr>
</tbody>
</table>

<span data-ttu-id="48ce0-207">若要根據 BITS 功能來照亮程式中的功能，請在 (上使用 QueryInterface，例如) 工作物件，以查看工作物件是否可讓您建立所需的版本。</span><span class="sxs-lookup"><span data-stu-id="48ce0-207">To light up features in your program based on BITS capabilities, use QueryInterface on (for example) your Job object to see if the Job object allows you to create the version you need.</span></span> <span data-ttu-id="48ce0-208">或者，請參閱 [判斷電腦上的位版本](./determining-the-version-of-bits-on-a-computer.md) ，以將 QMgr.dll 版本號碼轉換成 bits 版本。</span><span class="sxs-lookup"><span data-stu-id="48ce0-208">Alternatively, see [Determining the Version of BITS on a Computer](./determining-the-version-of-bits-on-a-computer.md) to convert the QMgr.dll version number into the BITS version.</span></span>

## <a name="version-103"></a><span data-ttu-id="48ce0-209">版本10。3</span><span class="sxs-lookup"><span data-stu-id="48ce0-209">Version 10.3</span></span>

<span data-ttu-id="48ce0-210">此版本已新增下列介面</span><span class="sxs-lookup"><span data-stu-id="48ce0-210">The following interfaces were added for this version</span></span>
-   <span data-ttu-id="48ce0-211">[**IBackgroundCopyJobHttpOptions3**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3) 
    [ **IBackgroundCopyServerCertificateValidationCallback**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback)</span><span class="sxs-lookup"><span data-stu-id="48ce0-211">[**IBackgroundCopyJobHttpOptions3**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3)
[**IBackgroundCopyServerCertificateValidationCallback**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback)</span></span>


## <a name="version-102"></a><span data-ttu-id="48ce0-212">版本10。2</span><span class="sxs-lookup"><span data-stu-id="48ce0-212">Version 10.2</span></span>

<span data-ttu-id="48ce0-213">此版本已新增下列介面</span><span class="sxs-lookup"><span data-stu-id="48ce0-213">The following interfaces were added for this version</span></span>
-   [<span data-ttu-id="48ce0-214">**IBackgroundCopyJobHttpOptions2**</span><span class="sxs-lookup"><span data-stu-id="48ce0-214">**IBackgroundCopyJobHttpOptions2**</span></span>](/windows/win32/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2)


## <a name="version-101"></a><span data-ttu-id="48ce0-215">版本10。1</span><span class="sxs-lookup"><span data-stu-id="48ce0-215">Version 10.1</span></span>

<span data-ttu-id="48ce0-216">此版本已新增下列介面</span><span class="sxs-lookup"><span data-stu-id="48ce0-216">The following interfaces were added for this version</span></span>
-   [<span data-ttu-id="48ce0-217">**BackgroundCopyFile6**</span><span class="sxs-lookup"><span data-stu-id="48ce0-217">**BackgroundCopyFile6**</span></span>](/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6)
-   [<span data-ttu-id="48ce0-218">**IBackgroundCopyCallback3**</span><span class="sxs-lookup"><span data-stu-id="48ce0-218">**IBackgroundCopyCallback3**</span></span>](/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3)

<span data-ttu-id="48ce0-219">已加入下列常數以搭配 [BITS_JOB_PROPERTY_ID 列舉](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id)使用。</span><span class="sxs-lookup"><span data-stu-id="48ce0-219">The following constants were added to use with the [BITS_JOB_PROPERTY_ID enumeration](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id).</span></span>

-   <span data-ttu-id="48ce0-220">**依 \_ \_ \_ \_ 需求 \_ 模式的 BITS 作業屬性**</span><span class="sxs-lookup"><span data-stu-id="48ce0-220">**BITS\_JOB\_PROPERTY\_ON\_DEMAND\_MODE**</span></span>
-   <span data-ttu-id="48ce0-221">**BITS \_ 作業 \_ 屬性 \_ 最小 \_ 通知 \_ 間隔 \_ 毫秒**</span><span class="sxs-lookup"><span data-stu-id="48ce0-221">**BITS\_JOB\_PROPERTY\_MINIMUM\_NOTIFICATION\_INTERVAL\_MS**</span></span>


## <a name="version-50"></a><span data-ttu-id="48ce0-222">版本 5.0</span><span class="sxs-lookup"><span data-stu-id="48ce0-222">Version 5.0</span></span>

<span data-ttu-id="48ce0-223">此版本已新增下列介面：</span><span class="sxs-lookup"><span data-stu-id="48ce0-223">The following interfaces were added for this version:</span></span>

-   [<span data-ttu-id="48ce0-224">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="48ce0-224">**IBackgroundCopyJob5**</span></span>](/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5)

## <a name="version-40"></a><span data-ttu-id="48ce0-225">4.0 版</span><span class="sxs-lookup"><span data-stu-id="48ce0-225">Version 4.0</span></span>

<span data-ttu-id="48ce0-226">此版本已新增下列介面：</span><span class="sxs-lookup"><span data-stu-id="48ce0-226">The following interfaces were added for this version:</span></span>

-   [<span data-ttu-id="48ce0-227">**IBitsToken**</span><span class="sxs-lookup"><span data-stu-id="48ce0-227">**IBitsToken**</span></span>](/windows/win32/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
-   [<span data-ttu-id="48ce0-228">**IBackgroundCopyFile4**</span><span class="sxs-lookup"><span data-stu-id="48ce0-228">**IBackgroundCopyFile4**</span></span>](/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4)

## <a name="version-30"></a><span data-ttu-id="48ce0-229">3.0 版</span><span class="sxs-lookup"><span data-stu-id="48ce0-229">Version 3.0</span></span>

<span data-ttu-id="48ce0-230">此版本已新增下列介面：</span><span class="sxs-lookup"><span data-stu-id="48ce0-230">The following interfaces were added for this version:</span></span>

-   [<span data-ttu-id="48ce0-231">**IBackgroundCopyCallback2**</span><span class="sxs-lookup"><span data-stu-id="48ce0-231">**IBackgroundCopyCallback2**</span></span>](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2)
-   [<span data-ttu-id="48ce0-232">**IBackgroundCopyFile3**</span><span class="sxs-lookup"><span data-stu-id="48ce0-232">**IBackgroundCopyFile3**</span></span>](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3)
-   [<span data-ttu-id="48ce0-233">**IBackgroundCopyJob4**</span><span class="sxs-lookup"><span data-stu-id="48ce0-233">**IBackgroundCopyJob4**</span></span>](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4)
-   [<span data-ttu-id="48ce0-234">**IBitsPeer**</span><span class="sxs-lookup"><span data-stu-id="48ce0-234">**IBitsPeer**</span></span>](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeer)
-   [<span data-ttu-id="48ce0-235">**IBitsPeerCacheAdministration**</span><span class="sxs-lookup"><span data-stu-id="48ce0-235">**IBitsPeerCacheAdministration**</span></span>](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration)
-   [<span data-ttu-id="48ce0-236">**IBitsPeerCacheRecord**</span><span class="sxs-lookup"><span data-stu-id="48ce0-236">**IBitsPeerCacheRecord**</span></span>](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacherecord)
-   [<span data-ttu-id="48ce0-237">**IEnumBitsPeerCacheRecords**</span><span class="sxs-lookup"><span data-stu-id="48ce0-237">**IEnumBitsPeerCacheRecords**</span></span>](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords)
-   [<span data-ttu-id="48ce0-238">**IEnumBitsPeers**</span><span class="sxs-lookup"><span data-stu-id="48ce0-238">**IEnumBitsPeers**</span></span>](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeers)

<span data-ttu-id="48ce0-239">新增下列常數以搭配 [**IBackgroundCopyJobHttpOptions：： SetSecurityFlags**](/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) 方法使用：</span><span class="sxs-lookup"><span data-stu-id="48ce0-239">The following constants were added to use with the [**IBackgroundCopyJobHttpOptions::SetSecurityFlags**](/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) method:</span></span>

-   <span data-ttu-id="48ce0-240">**BG \_ HTTP 重新 \_ 導向 \_ 原則 \_ 允許 \_ 無訊息**</span><span class="sxs-lookup"><span data-stu-id="48ce0-240">**BG\_HTTP\_REDIRECT\_POLICY\_ALLOW\_SILENT**</span></span>
-   <span data-ttu-id="48ce0-241">**BG \_ HTTP 重新 \_ 導向 \_ 原則 \_ 允許 \_ 報表**</span><span class="sxs-lookup"><span data-stu-id="48ce0-241">**BG\_HTTP\_REDIRECT\_POLICY\_ALLOW\_REPORT**</span></span>
-   <span data-ttu-id="48ce0-242">**不 \_ 允許 BG HTTP 重新 \_ 導向 \_ 原則 \_**</span><span class="sxs-lookup"><span data-stu-id="48ce0-242">**BG\_HTTP\_REDIRECT\_POLICY\_DISALLOW**</span></span>
-   <span data-ttu-id="48ce0-243">**BG \_ HTTP 重新 \_ 導向 \_ 原則 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="48ce0-243">**BG\_HTTP\_REDIRECT\_POLICY\_MASK**</span></span>
-   <span data-ttu-id="48ce0-244">**BG \_ HTTP 重新 \_ 導向 \_ 原則 \_ 允許 \_ HTTPS \_ 至 \_ HTTP**</span><span class="sxs-lookup"><span data-stu-id="48ce0-244">**BG\_HTTP\_REDIRECT\_POLICY\_ALLOW\_HTTPS\_TO\_HTTP**</span></span>

## <a name="version-25"></a><span data-ttu-id="48ce0-245">版本2。5</span><span class="sxs-lookup"><span data-stu-id="48ce0-245">Version 2.5</span></span>

<span data-ttu-id="48ce0-246">針對2.5 版新增了下列介面和列舉：</span><span class="sxs-lookup"><span data-stu-id="48ce0-246">The following interface and enumeration were added for version 2.5:</span></span>

-   [<span data-ttu-id="48ce0-247">**IBackgroundCopyJobHttpOptions**</span><span class="sxs-lookup"><span data-stu-id="48ce0-247">**IBackgroundCopyJobHttpOptions**</span></span>](/windows/win32/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions)
-   [<span data-ttu-id="48ce0-248">**BG \_ 證書 \_ 存儲 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="48ce0-248">**BG\_CERT\_STORE\_LOCATION**</span></span>](/windows/win32/api/Bits2_5/ne-bits2_5-bg_cert_store_location)

## <a name="version-20"></a><span data-ttu-id="48ce0-249">版本2。0</span><span class="sxs-lookup"><span data-stu-id="48ce0-249">Version 2.0</span></span>

<span data-ttu-id="48ce0-250">針對2.0 版新增了下列介面、結構和主題：</span><span class="sxs-lookup"><span data-stu-id="48ce0-250">The following interfaces, structure, and topics were added for version 2.0:</span></span>

-   [<span data-ttu-id="48ce0-251">**IBackgroundCopyJob3**</span><span class="sxs-lookup"><span data-stu-id="48ce0-251">**IBackgroundCopyJob3**</span></span>](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)
-   [<span data-ttu-id="48ce0-252">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="48ce0-252">**IBackgroundCopyFile2**</span></span>](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2)
-   [<span data-ttu-id="48ce0-253">**BG \_ 檔案 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="48ce0-253">**BG\_FILE\_RANGE**</span></span>](/windows/win32/api/Bits2_0/ns-bits2_0-bg_file_range)
-   [<span data-ttu-id="48ce0-254">群組原則</span><span class="sxs-lookup"><span data-stu-id="48ce0-254">Group Policies</span></span>](group-policies.md)

<span data-ttu-id="48ce0-255">如需並行前景下載的詳細資訊，請參閱「 [**BG \_ 工作 \_ 優先順序**](/windows/win32/api/Bits/ne-bits-bg_job_priority)」的備註一節。</span><span class="sxs-lookup"><span data-stu-id="48ce0-255">For information about concurrent foreground downloads, see the Remarks section for [**BG\_JOB\_PRIORITY**](/windows/win32/api/Bits/ne-bits-bg_job_priority).</span></span>

<span data-ttu-id="48ce0-256">如需使用 SMB 通訊協定的相關資訊，請參閱 [**BG 檔案 \_ \_ 資訊**](/windows/win32/api/Bits/ns-bits-bg_file_info)。</span><span class="sxs-lookup"><span data-stu-id="48ce0-256">For information about using the SMB protocol, see [**BG\_FILE\_INFO**](/windows/win32/api/Bits/ns-bits-bg_file_info).</span></span>

## <a name="version-15"></a><span data-ttu-id="48ce0-257">1.5 版</span><span class="sxs-lookup"><span data-stu-id="48ce0-257">Version 1.5</span></span>

<span data-ttu-id="48ce0-258">針對1.5 版新增了下列介面和主題：</span><span class="sxs-lookup"><span data-stu-id="48ce0-258">The following interfaces and topics were added for version 1.5:</span></span>

-   [<span data-ttu-id="48ce0-259">**IBackgroundCopyJob2**</span><span class="sxs-lookup"><span data-stu-id="48ce0-259">**IBackgroundCopyJob2**</span></span>](/windows/win32/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
-   [<span data-ttu-id="48ce0-260">從 Upload-Reply 作業中取出回復</span><span class="sxs-lookup"><span data-stu-id="48ce0-260">Retrieving the Reply from an Upload-Reply Job</span></span>](retrieving-the-reply-from-an-upload-reply-job.md)
-   [<span data-ttu-id="48ce0-261">註冊以執行程式</span><span class="sxs-lookup"><span data-stu-id="48ce0-261">Registering to Execute a Program</span></span>](registering-to-execute-a-program.md)
-   [<span data-ttu-id="48ce0-262">上傳作業的 BITS 伺服器設定</span><span class="sxs-lookup"><span data-stu-id="48ce0-262">BITS Server Settings for Upload Jobs</span></span>](bits-server-settings-for-upload-jobs.md)
-   [<span data-ttu-id="48ce0-263">設定伺服器以進行上傳</span><span class="sxs-lookup"><span data-stu-id="48ce0-263">Setting Up the Server for Uploads</span></span>](setting-up-the-server-for-uploads.md)
-   [<span data-ttu-id="48ce0-264">使用 BITS 通知要求/回應標頭</span><span class="sxs-lookup"><span data-stu-id="48ce0-264">Using BITS Notification Request/Response Headers</span></span>](using-bits-notification-request-response-headers.md)

 
## <a name="updating-bits-versions"></a><span data-ttu-id="48ce0-265">更新 BITS 版本</span><span class="sxs-lookup"><span data-stu-id="48ce0-265">Updating BITS versions</span></span>
 
<span data-ttu-id="48ce0-266">您可以下載 Windows Server 2008 （含 Service Pack 2）的 BITS 4.0 (SP2) 、Windows Vista （含 Service Pack 1） (SP1) ，以及 Windows Vista （含 Service Pack 2 (SP2) ）。</span><span class="sxs-lookup"><span data-stu-id="48ce0-266">You can download BITS 4.0 for Windows Server 2008 with Service Pack 2 (SP2), Windows Vista with Service Pack 1 (SP1), and Windows Vista with Service Pack 2 (SP2).</span></span> <span data-ttu-id="48ce0-267">如需下載 BITS 4.0 的詳細資訊，請參閱 [KB968929](https://support.microsoft.com/kb/968929)。</span><span class="sxs-lookup"><span data-stu-id="48ce0-267">For information about downloading BITS 4.0, see [KB968929](https://support.microsoft.com/kb/968929).</span></span>
