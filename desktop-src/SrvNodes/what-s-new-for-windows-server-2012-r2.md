---
description: 下列清單描述 Windows Server 2012 和 Windows Server 2012 R2 的新功能和更新功能區域。 如需新 Windows 8 和 Windows 8.1 技術的詳細資訊，請參閱 Windows 8 和 Windows 8.1 技術。
ms.assetid: bd8b4dd8-e0b7-4340-a6bd-1baa42d9a1dd
title: 新功能： Windows Server 2012 R2 & Windows Server 2012
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ba276ea8256299c5e667cbb5a1d2b0872bb282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850507"
---
# <a name="whats-new-windows-server-2012-r2--windows-server-2012"></a><span data-ttu-id="9bd15-104">新功能： Windows Server 2012 R2 & Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9bd15-104">What's New: Windows Server 2012 R2 & Windows Server 2012</span></span>

<span data-ttu-id="9bd15-105">下列清單描述 Windows Server 2012 和 Windows Server 2012 R2 的新功能和更新功能區域。</span><span class="sxs-lookup"><span data-stu-id="9bd15-105">The following list describes new and updated feature areas for Windows Server 2012 and Windows Server 2012 R2.</span></span> <span data-ttu-id="9bd15-106">如需新 Windows 8 和 Windows 8.1 技術的詳細資訊，請參閱 [Windows 8 和 Windows 8.1 技術](/previous-versions/windows/desktop/whatsnew/windows-8-technologies)。</span><span class="sxs-lookup"><span data-stu-id="9bd15-106">For more information on new Windows 8 and Windows 8.1 technologies, see [Windows 8 and Windows 8.1 Technologies](/previous-versions/windows/desktop/whatsnew/windows-8-technologies).</span></span>

## <a name="whats-new-for-windows-server-2012-r2"></a><span data-ttu-id="9bd15-107">Windows Server 2012 R2 的新功能</span><span class="sxs-lookup"><span data-stu-id="9bd15-107">What's New for Windows Server 2012 R2</span></span>

-   [<span data-ttu-id="9bd15-108">重複資料刪除</span><span class="sxs-lookup"><span data-stu-id="9bd15-108">Data Deduplication</span></span>](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    <span data-ttu-id="9bd15-109">重復資料刪除會在磁片區上的資料中尋找並移除重複的資料，同時確保資料保持正確且完整。</span><span class="sxs-lookup"><span data-stu-id="9bd15-109">Data deduplication finds and removes duplication within data on a volume while ensuring that the data remains correct and complete.</span></span> <span data-ttu-id="9bd15-110">如此即可節省磁碟區上的檔案資料儲存空間。</span><span class="sxs-lookup"><span data-stu-id="9bd15-110">This makes it possible to store more file data in less space on the volume.</span></span> <span data-ttu-id="9bd15-111">若為 Windows Server 2012 R2，則會啟用許多參數和錯誤碼，並新增 [**MSFT \_ DedupFileMetadata**](/previous-versions/windows/desktop/dedup/msft-dedupfilemetadata) 類別。</span><span class="sxs-lookup"><span data-stu-id="9bd15-111">For Windows Server 2012 R2, a number of parameters and error codes were activated, and the [**MSFT\_DedupFileMetadata**](/previous-versions/windows/desktop/dedup/msft-dedupfilemetadata) class was added.</span></span>

-   [<span data-ttu-id="9bd15-112">軟體清查記錄</span><span class="sxs-lookup"><span data-stu-id="9bd15-112">Software Inventory Logging</span></span>](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)

    <span data-ttu-id="9bd15-113">**新功能！**</span><span class="sxs-lookup"><span data-stu-id="9bd15-113">**New!**</span></span> <span data-ttu-id="9bd15-114">軟體清查記錄會收集安裝在 Windows 伺服器上之軟體的授權資料，並提供資料的遠端存取，讓資料中心可以輕鬆地匯總資料。</span><span class="sxs-lookup"><span data-stu-id="9bd15-114">Software Inventory Logging collects licensing data about software installed on a Windows Server, and provides remote access to the data so it can be aggregated easily by a datacenter.</span></span>

-   [<span data-ttu-id="9bd15-115">iSCSI 目標伺服器</span><span class="sxs-lookup"><span data-stu-id="9bd15-115">iSCSI Target Server</span></span>](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    <span data-ttu-id="9bd15-116">ISCSI 目標伺服器 API 提供 Windows Management Instrumentation (的 WMI) 提供者，以管理 Microsoft iSCSI 目標伺服器，例如建立虛擬磁片，以及將它們呈現給用戶端。</span><span class="sxs-lookup"><span data-stu-id="9bd15-116">The iSCSI Target Server API provides Windows Management Instrumentation (WMI) providers for managing the Microsoft iSCSI Target Server, such as creating virtual disks, and for presenting them to the client.</span></span> <span data-ttu-id="9bd15-117">針對 Windows Server 2012 R2 新增了許多新功能。</span><span class="sxs-lookup"><span data-stu-id="9bd15-117">A number of new features were added for Windows Server 2012 R2.</span></span>

-   [<span data-ttu-id="9bd15-118">Mobile 裝置管理註冊</span><span class="sxs-lookup"><span data-stu-id="9bd15-118">Mobile Device Management Registration</span></span>](../mdmreg/mobile-device-management-registration-portal.md)

    <span data-ttu-id="9bd15-119">**新功能！**</span><span class="sxs-lookup"><span data-stu-id="9bd15-119">**New!**</span></span> <span data-ttu-id="9bd15-120">產業趨勢的開發是讓員工將其個人行動運算裝置連接到公司網路和資源 (內部部署或透過雲端) 來執行工作場所工作。</span><span class="sxs-lookup"><span data-stu-id="9bd15-120">An industry trend has been developing in which employees connect their personal mobile computing devices to the corporate network and resources (either on premise or through the cloud) to perform workplace tasks.</span></span> <span data-ttu-id="9bd15-121">此趨勢需要支援輕鬆設定網路和資源，讓員工可以在公司註冊個人裝置，以進行工作相關的用途。</span><span class="sxs-lookup"><span data-stu-id="9bd15-121">This trend requires support for easy configuration of the network and resources, such that employees can register personal devices with the company for work-related purposes.</span></span> <span data-ttu-id="9bd15-122">支援輕鬆設定的應用程式和技術也必須讓 IT 專業人員管理與將未受管理的裝置連線到公司網路相關聯的風險。</span><span class="sxs-lookup"><span data-stu-id="9bd15-122">Applications and technology to support easy configuration must also enable IT professionals to manage the risk associated with having uncontrolled devices connected to the corporate network.</span></span> <span data-ttu-id="9bd15-123">行動裝置管理 (MDM) 註冊會將裝置註冊到管理服務中。</span><span class="sxs-lookup"><span data-stu-id="9bd15-123">The Mobile Device Management (MDM) registration enrolls a device into a management service.</span></span>

-   <span data-ttu-id="9bd15-124">[Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="9bd15-124">[Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)</span></span>

    <span data-ttu-id="9bd15-125">Windows PowerShell 是以工作為基礎的命令列 shell 和指令碼語言，專為系統管理所設計。</span><span class="sxs-lookup"><span data-stu-id="9bd15-125">Windows PowerShell is a task-based command-line shell and scripting language designed especially for system administration.</span></span> <span data-ttu-id="9bd15-126">Windows Server 2012 R2 中的新功能 Windows PowerShell v4 支援 Desired State Configuration，這是 Windows PowerShell 中的新管理平臺，可讓您部署和管理軟體服務的設定資料，以及管理這些服務執行所在的環境。</span><span class="sxs-lookup"><span data-stu-id="9bd15-126">New in Windows Server 2012 R2, Windows PowerShell v4 supports Desired State Configuration, which is a new management platform in Windows PowerShell that enables deploying and managing configuration data for software services and managing the environment in which these services run.</span></span>

## <a name="whats-new-for-windows-server-2012"></a><span data-ttu-id="9bd15-127">Windows Server 2012 的新功能</span><span class="sxs-lookup"><span data-stu-id="9bd15-127">What's New for Windows Server 2012</span></span>

-   [<span data-ttu-id="9bd15-128">Windows 叢集</span><span class="sxs-lookup"><span data-stu-id="9bd15-128">Windows Clustering</span></span>](/previous-versions/windows/desktop/mscs/windows-clustering)

    <span data-ttu-id="9bd15-129">Windows 叢集可讓您同時管理網路負載平衡叢集和容錯移轉叢集。</span><span class="sxs-lookup"><span data-stu-id="9bd15-129">Windows Clustering allows you to manage both network load-balanced clusters as well as failover clusters.</span></span> <span data-ttu-id="9bd15-130">此版本加入了許多新功能，包括新的群組管理功能、通用屬性，以及與 WMI 的整合。</span><span class="sxs-lookup"><span data-stu-id="9bd15-130">A number of new features were added in this release, including new Group management features, common properties, and integration with WMI.</span></span>

-   [<span data-ttu-id="9bd15-131">使用者存取記錄</span><span class="sxs-lookup"><span data-stu-id="9bd15-131">User Access Logging</span></span>](/previous-versions/windows/desktop/ual/user-access-logging)

    <span data-ttu-id="9bd15-132">**新功能！**</span><span class="sxs-lookup"><span data-stu-id="9bd15-132">**New!**</span></span> <span data-ttu-id="9bd15-133">使用者存取記錄 (UAL) 是 Windows Server 角色的通用架構，可報告其各自的耗用量計量。</span><span class="sxs-lookup"><span data-stu-id="9bd15-133">User Access Logging (UAL) is a common framework for Windows Server roles to report their respective consumption metrics.</span></span> <span data-ttu-id="9bd15-134">這個 UAL 架構是較大的授權管理解決方案的基礎和重要元件。</span><span class="sxs-lookup"><span data-stu-id="9bd15-134">This UAL framework is a foundational and critical component of the larger licensing management solution.</span></span>

-   [<span data-ttu-id="9bd15-135">Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="9bd15-135">Windows Remote Management</span></span>](../winrm/portal.md)

    <span data-ttu-id="9bd15-136">Windows 遠端管理 (WinRM) 是 Microsoft 在 WS-Management 通訊協定方面的實作，它是以簡易物件存取通訊協定 (SOAP) 為基礎、防火牆適用的通訊協定，允許不同廠商的硬體和作業系統互相操作。</span><span class="sxs-lookup"><span data-stu-id="9bd15-136">Windows Remote Management (WinRM) is the Microsoft implementation of WS-Management Protocol, a standard Simple Object Access Protocol (SOAP)-based, firewall-friendly protocol that allows hardware and operating systems, from different vendors, to interoperate.</span></span> <span data-ttu-id="9bd15-137">Windows Server 2012 包含許多連接 API，其著重于與執行中的實例和 shell 互動。</span><span class="sxs-lookup"><span data-stu-id="9bd15-137">Windows Server 2012 includes a number of Connection API's that focus on interacting with running instances and shells.</span></span>

-   [<span data-ttu-id="9bd15-138">Windows 管理基礎結構</span><span class="sxs-lookup"><span data-stu-id="9bd15-138">Windows Management Infrastructure</span></span>](/previous-versions/windows/desktop/wmi_v2/what-s-new-in-mi)

    <span data-ttu-id="9bd15-139">**新功能！**</span><span class="sxs-lookup"><span data-stu-id="9bd15-139">**New!**</span></span> <span data-ttu-id="9bd15-140">Windows 管理基礎結構 (MI) 功能代表 Windows Management Instrumentation (WMI) 技術的最新版本，這些技術是以來自 DMTF (分散式管理工作小組) 的 CIM 標準為基礎。</span><span class="sxs-lookup"><span data-stu-id="9bd15-140">The Windows Management Infrastructure (MI) features represent the latest version of the Windows Management Instrumentation (WMI) technologies, which are based on the CIM standard from DMTF (Distributed Management Task Force).</span></span> <span data-ttu-id="9bd15-141">MI 與舊版 WMI 完全相容，並提供一系列的功能和優點，讓設計和開發提供者和用戶端比以往更容易。</span><span class="sxs-lookup"><span data-stu-id="9bd15-141">MI is fully compatible with previous versions of WMI and provides a host of features and benefits that make designing and developing providers and clients easier than ever.</span></span>

-   [<span data-ttu-id="9bd15-142">重複資料刪除</span><span class="sxs-lookup"><span data-stu-id="9bd15-142">Data Deduplication</span></span>](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    <span data-ttu-id="9bd15-143">**新功能！**</span><span class="sxs-lookup"><span data-stu-id="9bd15-143">**New!**</span></span> <span data-ttu-id="9bd15-144">重復資料刪除會在磁片區上的資料中尋找並移除重複的資料，同時確保資料保持正確且完整。</span><span class="sxs-lookup"><span data-stu-id="9bd15-144">Data deduplication finds and removes duplication within data on a volume while ensuring that the data remains correct and complete.</span></span> <span data-ttu-id="9bd15-145">如此即可節省磁碟區上的檔案資料儲存空間。</span><span class="sxs-lookup"><span data-stu-id="9bd15-145">This makes it possible to store more file data in less space on the volume.</span></span>

-   [<span data-ttu-id="9bd15-146">iSCSI 目標伺服器</span><span class="sxs-lookup"><span data-stu-id="9bd15-146">iSCSI Target Server</span></span>](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    <span data-ttu-id="9bd15-147">**新功能！**</span><span class="sxs-lookup"><span data-stu-id="9bd15-147">**New!**</span></span> <span data-ttu-id="9bd15-148">ISCSI 目標伺服器 API 提供 Windows Management Instrumentation (的 WMI) 提供者，以管理 Microsoft iSCSI 目標伺服器，例如建立虛擬磁片，以及將它們呈現給用戶端。</span><span class="sxs-lookup"><span data-stu-id="9bd15-148">The iSCSI Target Server API provides Windows Management Instrumentation (WMI) providers for managing the Microsoft iSCSI Target Server, such as creating virtual disks, and for presenting them to the client.</span></span>

-   [<span data-ttu-id="9bd15-149">適用于 WMI 的 NFS 提供者</span><span class="sxs-lookup"><span data-stu-id="9bd15-149">NFS Provider for WMI</span></span>](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)

    <span data-ttu-id="9bd15-150">**新功能！**</span><span class="sxs-lookup"><span data-stu-id="9bd15-150">**New!**</span></span> <span data-ttu-id="9bd15-151">NFS WMI 提供者提供管理 NFS 伺服器和用戶端設定、檔案共用、群組和用戶端群組的方法。</span><span class="sxs-lookup"><span data-stu-id="9bd15-151">The NFS WMI provider provides a means of managing NFS server and client settings, file shares, netgroups, and client groups.</span></span>

-   [<span data-ttu-id="9bd15-152">離線檔案</span><span class="sxs-lookup"><span data-stu-id="9bd15-152">Offline Files</span></span>](../devnotes/offline-files.md)

    <span data-ttu-id="9bd15-153">離線檔案 API 可讓應用程式以程式設計方式控制和監視離線檔案的行為。</span><span class="sxs-lookup"><span data-stu-id="9bd15-153">The Offline Files API allows applications to control and monitor the behavior of Offline Files programmatically.</span></span> <span data-ttu-id="9bd15-154">Windows Server 2012 新增了 [**OfflineFilesQueryStatusEx**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex)、 [**OfflineFilesStart**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart) 和 [**RenameItem**](/previous-versions/windows/desktop/offlinefiles/win32-offlinefilescache-renameitem) 函數。</span><span class="sxs-lookup"><span data-stu-id="9bd15-154">Windows Server 2012 adds the [**OfflineFilesQueryStatusEx**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex), [**OfflineFilesStart**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart) and [**RenameItem**](/previous-versions/windows/desktop/offlinefiles/win32-offlinefilescache-renameitem) functions.</span></span>

-   [<span data-ttu-id="9bd15-155">SMB 管理</span><span class="sxs-lookup"><span data-stu-id="9bd15-155">SMB Management</span></span>](/previous-versions/windows/desktop/smb/smb-management-api-portal)

    <span data-ttu-id="9bd15-156">**新功能！**</span><span class="sxs-lookup"><span data-stu-id="9bd15-156">**New!**</span></span> <span data-ttu-id="9bd15-157">SMB 管理 API 提供 WMI 類別和方法來管理共用和共用存取。</span><span class="sxs-lookup"><span data-stu-id="9bd15-157">The SMB Management API provides WMI classes and methods to manage shares and share access.</span></span>

-   <span data-ttu-id="9bd15-158">[Server Core](/previous-versions/windows/desktop/legacy/hh846323(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9bd15-158">[Server Core](/previous-versions/windows/desktop/legacy/hh846323(v=vs.85))</span></span>

    <span data-ttu-id="9bd15-159">Windows Server 針對在 Windows Server 2008 作業系統或更新版本上執行的電腦，提供最基本的伺服器安裝選項。</span><span class="sxs-lookup"><span data-stu-id="9bd15-159">Windows Server provides minimal server installation options for computers running on the Windows Server 2008 operating system or later.</span></span> <span data-ttu-id="9bd15-160">Windows Server 2012 提供 Server Core 作為設定和安裝選項。</span><span class="sxs-lookup"><span data-stu-id="9bd15-160">Windows Server 2012 offers Server Core as both a configuration as well as an installation options.</span></span>

-   [<span data-ttu-id="9bd15-161">Windows Server Backup</span><span class="sxs-lookup"><span data-stu-id="9bd15-161">Windows Server Backup</span></span>](/previous-versions/windows/desktop/wsb/windows-server-backup-portal)

    <span data-ttu-id="9bd15-162">Windows Server Backup 功能會自動備份及還原應用程式資料。</span><span class="sxs-lookup"><span data-stu-id="9bd15-162">The Windows Server Backup feature automatically backs up and restores application data.</span></span> <span data-ttu-id="9bd15-163">Windows Server 2012 包含雲端備份提供者 API。</span><span class="sxs-lookup"><span data-stu-id="9bd15-163">Windows Server 2012 includes the Cloud Backup Provider API.</span></span>

-   [<span data-ttu-id="9bd15-164">Windows 桌面共用</span><span class="sxs-lookup"><span data-stu-id="9bd15-164">Windows Desktop Sharing</span></span>](/previous-versions/windows/desktop/rdp/rdp-portal)

    <span data-ttu-id="9bd15-165">Windows 桌面共用是一種多方的螢幕共用技術。</span><span class="sxs-lookup"><span data-stu-id="9bd15-165">Windows Desktop Sharing is a multiple-party screen-sharing technology.</span></span> <span data-ttu-id="9bd15-166">Windows Server 2012 使用 Windows 重複 API 來實行這項技術。</span><span class="sxs-lookup"><span data-stu-id="9bd15-166">Windows Server 2012 implements this technology using the Windows Duplication API.</span></span>

-   [<span data-ttu-id="9bd15-167">遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="9bd15-167">Remote Desktop Services</span></span>](../termserv/terminal-services-portal.md)

    <span data-ttu-id="9bd15-168">Windows 桌面共用可讓使用者從遠端存取作業系統的實例。</span><span class="sxs-lookup"><span data-stu-id="9bd15-168">Windows Desktop Sharing allows the user to remotely access an instance of the operating system.</span></span> <span data-ttu-id="9bd15-169">Windows Server 2012 包含許多新功能，包括子會話、RemoteFX 媒體重新導向，以及遠端桌面訊息代理程式用戶端。</span><span class="sxs-lookup"><span data-stu-id="9bd15-169">Windows Server 2012 includes a number of new features, including Child sessions, RemoteFX Media redirection, and the Remote Desktop Broker client.</span></span>

-   <span data-ttu-id="9bd15-170">[Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="9bd15-170">[Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)</span></span>

    <span data-ttu-id="9bd15-171">Windows PowerShell 是以工作為基礎的命令列 shell 和指令碼語言，專為系統管理所設計。</span><span class="sxs-lookup"><span data-stu-id="9bd15-171">Windows PowerShell is a task-based command-line shell and scripting language designed especially for system administration.</span></span> <span data-ttu-id="9bd15-172">Windows Server 2012 的新功能 Windows PowerShell v3 支援 Windows PowerShell 的工作流程，它利用 Windows Workflow Foundation 的優點，讓長時間執行的工作自動化。</span><span class="sxs-lookup"><span data-stu-id="9bd15-172">New in Windows Server 2012, Windows PowerShell v3 supports Windows PowerShell Workflow, which leverages the benefits of Windows Workflow Foundation to allow the automation of long-running tasks.</span></span>

-   [<span data-ttu-id="9bd15-173">管理 OData</span><span class="sxs-lookup"><span data-stu-id="9bd15-173">Management OData</span></span>](/powershell/scripting/developer/webservices/creating-a-management-odata-web-service?view=powershell-7&preserve-view=true)

    <span data-ttu-id="9bd15-174">**新功能！**</span><span class="sxs-lookup"><span data-stu-id="9bd15-174">**New!**</span></span> <span data-ttu-id="9bd15-175">也稱為 Windows PowerShell Web 服務、管理 OData、Windows PowerShell v3 的新功能，可讓您建立 ASP.NET Web 服務端點，以公開管理資料（透過 Windows PowerShell 命令 acessed）作為 OData Web 服務實體。</span><span class="sxs-lookup"><span data-stu-id="9bd15-175">Also known as Windows PowerShell Web Services, Management OData, new in Windows PowerShell v3, allows the creation of an ASP.NET web service end point that exposes management data, acessed through Windows PowerShell commands, as OData web service entities.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bd15-176">相關主題</span><span class="sxs-lookup"><span data-stu-id="9bd15-176">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9bd15-177">[TechNet 上的 Windows Server 2012 R2](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="9bd15-177">[Windows Server 2012 R2 on TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="9bd15-178">[TechNet Library 上的 windows Server 2012 R2 和 Windows Server 2012](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="9bd15-178">[Windows Server 2012 R2 and Windows Server 2012 on TechNet Library](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="9bd15-179">Microsoft.Com 上的 Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9bd15-179">Windows Server 2012 R2 on Microsoft.Com</span></span>](https://www.microsoft.com/evalcenter/evaluate-windows-server-2012-r2-essentials)
</dt> </dl>

 

 
