---
description: 從 Windows Vista 開始，Windows 隨附的主控台專案會獲得可用於 API 呼叫或命令列指令，以程式設計方式啟動該專案的標準名稱。
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: 主控台專案的正式名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55fc360b0d3db0f85a057977d1898c59d09d5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943269"
---
# <a name="canonical-names-of-control-panel-items"></a><span data-ttu-id="c2ce9-103">主控台專案的正式名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-103">Canonical Names of Control Panel Items</span></span>

<span data-ttu-id="c2ce9-104">從 Windows Vista 開始，Windows 隨附的主控台專案會獲得可用於 [API 呼叫或命令列指令](executing-control-panel-items.md) ，以程式設計方式啟動該專案的標準名稱。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-104">As of Windows Vista, Control Panel items included with Windows are given a canonical name that can be used in an [API call or a command-line instruction](executing-control-panel-items.md) to programmatically launch that item.</span></span> <span data-ttu-id="c2ce9-105">從 Windows 7 和 Windows Server 2008 R2，正式名稱可在群組原則中用來隱藏特定的主控台專案。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-105">As of Windows 7 and Windows Server 2008 R2, canonical names can be used in a group policy to hide specific Control Panel items.</span></span> <span data-ttu-id="c2ce9-106">本主題提供每個主控台專案的詳細資料：標準名稱、GUID、模組名稱，以及辨識正式名稱的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-106">This topic provides details for each Control Panel item: canonical name, GUID, module name, and the operating system versions that recognize the canonical name.</span></span>

> [!Note]  
> <span data-ttu-id="c2ce9-107">在 Windows Vista 之前，不支援主控台專案的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-107">Canonical names for Control Panel items are not supported prior to Windows Vista.</span></span>

 

-   [<span data-ttu-id="c2ce9-108">主控台標準名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-108">Control Panel Canonical Names</span></span>](#control-panel-canonical-names)
-   [<span data-ttu-id="c2ce9-109">已淘汰主控台正式名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-109">Deprecated Control Panel Canonical Names</span></span>](#deprecated-control-panel-canonical-names)
-   [<span data-ttu-id="c2ce9-110">在群組原則中使用正式名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-110">Using Canonical Names in Group Policy</span></span>](#using-canonical-names-in-local-group-policy)
-   [<span data-ttu-id="c2ce9-111">備註</span><span class="sxs-lookup"><span data-stu-id="c2ce9-111">Remarks</span></span>](#remarks)

## <a name="control-panel-canonical-names"></a><span data-ttu-id="c2ce9-112">主控台標準名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-112">Control Panel Canonical Names</span></span>

<span data-ttu-id="c2ce9-113">使用這些值時，請記住下列事項：</span><span class="sxs-lookup"><span data-stu-id="c2ce9-113">Points to remember when working with these values:</span></span>

-   <span data-ttu-id="c2ce9-114">根據定義，標準名稱不會根據系統語言而變更;即使系統的語言不是，它們一律會是英文。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-114">By definition, canonical names do not change based on the system language; they're always in English, even if the system's language is not.</span></span>
-   <span data-ttu-id="c2ce9-115">並非所有的主控台專案都存在於所有的 Windows 中。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-115">Not all Control Panel items are present in all varieties of Windows.</span></span>
-   <span data-ttu-id="c2ce9-116">只有在系統上偵測到正確的硬體時，才會顯示某些主控台專案。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-116">Some Control Panel items only appear if the right hardware is detected on the system.</span></span>
-   <span data-ttu-id="c2ce9-117">協力廠商也可以新增主控台專案。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-117">Third parties can also add Control Panel items.</span></span> <span data-ttu-id="c2ce9-118">此處所列的正式名稱只適用于 Windows 隨附的主控台專案。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-118">The canonical names listed here are only for Control Panel items that are included with Windows.</span></span>

<span data-ttu-id="c2ce9-119">以下是 Windows 8.1 中可用的主控台專案：</span><span class="sxs-lookup"><span data-stu-id="c2ce9-119">The following are the Control Panel items available in Windows 8.1:</span></span>

-   [<span data-ttu-id="c2ce9-120">控制中心</span><span class="sxs-lookup"><span data-stu-id="c2ce9-120">Action Center</span></span>](#action-center)
-   [<span data-ttu-id="c2ce9-121">系統管理工具</span><span class="sxs-lookup"><span data-stu-id="c2ce9-121">Administrative Tools</span></span>](#administrative-tools)
-   [<span data-ttu-id="c2ce9-122">播放</span><span class="sxs-lookup"><span data-stu-id="c2ce9-122">AutoPlay</span></span>](#autoplay)
-   [<span data-ttu-id="c2ce9-123">生物特徵辨識裝置</span><span class="sxs-lookup"><span data-stu-id="c2ce9-123">Biometric Devices</span></span>](#biometric-devices)
-   [<span data-ttu-id="c2ce9-124">BitLocker 磁碟機加密</span><span class="sxs-lookup"><span data-stu-id="c2ce9-124">BitLocker Drive Encryption</span></span>](#bitlocker-drive-encryption)
-   [<span data-ttu-id="c2ce9-125">色彩管理</span><span class="sxs-lookup"><span data-stu-id="c2ce9-125">Color Management</span></span>](#color-management)
-   [<span data-ttu-id="c2ce9-126">認證管理員</span><span class="sxs-lookup"><span data-stu-id="c2ce9-126">Credential Manager</span></span>](#credential-manager)
-   [<span data-ttu-id="c2ce9-127">日期和時間</span><span class="sxs-lookup"><span data-stu-id="c2ce9-127">Date and Time</span></span>](#date-and-time)
-   [<span data-ttu-id="c2ce9-128">預設程式</span><span class="sxs-lookup"><span data-stu-id="c2ce9-128">Default Programs</span></span>](#default-programs)
-   [<span data-ttu-id="c2ce9-129">裝置管理員</span><span class="sxs-lookup"><span data-stu-id="c2ce9-129">Device Manager</span></span>](#device-manager)
-   [<span data-ttu-id="c2ce9-130">裝置和印表機</span><span class="sxs-lookup"><span data-stu-id="c2ce9-130">Devices and Printers</span></span>](#devices-and-printers)
-   [<span data-ttu-id="c2ce9-131">顯示器</span><span class="sxs-lookup"><span data-stu-id="c2ce9-131">Display</span></span>](#display)
-   [<span data-ttu-id="c2ce9-132">輕鬆存取中心</span><span class="sxs-lookup"><span data-stu-id="c2ce9-132">Ease of Access Center</span></span>](#ease-of-access-center)
-   [<span data-ttu-id="c2ce9-133">家庭安全</span><span class="sxs-lookup"><span data-stu-id="c2ce9-133">Family Safety</span></span>](#family-safety)
-   [<span data-ttu-id="c2ce9-134">檔案歷程記錄</span><span class="sxs-lookup"><span data-stu-id="c2ce9-134">File History</span></span>](#file-history)
-   [<span data-ttu-id="c2ce9-135">資料夾選項</span><span class="sxs-lookup"><span data-stu-id="c2ce9-135">Folder Options</span></span>](#folder-options)
-   [<span data-ttu-id="c2ce9-136">字型</span><span class="sxs-lookup"><span data-stu-id="c2ce9-136">Fonts</span></span>](#fonts)
-   [<span data-ttu-id="c2ce9-137">HomeGroup</span><span class="sxs-lookup"><span data-stu-id="c2ce9-137">HomeGroup</span></span>](#homegroup)
-   [<span data-ttu-id="c2ce9-138">索引選項</span><span class="sxs-lookup"><span data-stu-id="c2ce9-138">Indexing Options</span></span>](#indexing-options)
-   [<span data-ttu-id="c2ce9-139">紅外線</span><span class="sxs-lookup"><span data-stu-id="c2ce9-139">Infrared</span></span>](#infrared)
-   [<span data-ttu-id="c2ce9-140">網際網路選項</span><span class="sxs-lookup"><span data-stu-id="c2ce9-140">Internet Options</span></span>](#internet-options)
-   [<span data-ttu-id="c2ce9-141">iSCSI 啟動器</span><span class="sxs-lookup"><span data-stu-id="c2ce9-141">iSCSI Initiator</span></span>](#iscsi-initiator)
-   [<span data-ttu-id="c2ce9-142">iSNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="c2ce9-142">iSNS Server</span></span>](#isns-server)
-   [<span data-ttu-id="c2ce9-143">鍵盤</span><span class="sxs-lookup"><span data-stu-id="c2ce9-143">Keyboard</span></span>](#keyboard)
-   [<span data-ttu-id="c2ce9-144">位置設定</span><span class="sxs-lookup"><span data-stu-id="c2ce9-144">Location Settings</span></span>](#location-settings)
-   [<span data-ttu-id="c2ce9-145">滑鼠</span><span class="sxs-lookup"><span data-stu-id="c2ce9-145">Mouse</span></span>](#mouse)
-   [<span data-ttu-id="c2ce9-146">MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2ce9-146">MPIOConfiguration</span></span>](#mpioconfiguration)
-   [<span data-ttu-id="c2ce9-147">網路和共用中心</span><span class="sxs-lookup"><span data-stu-id="c2ce9-147">Network and Sharing Center</span></span>](#network-and-sharing-center)
-   [<span data-ttu-id="c2ce9-148">通知區域圖示</span><span class="sxs-lookup"><span data-stu-id="c2ce9-148">Notification Area Icons</span></span>](#notification-area-icons)
-   [<span data-ttu-id="c2ce9-149">畫筆和觸控</span><span class="sxs-lookup"><span data-stu-id="c2ce9-149">Pen and Touch</span></span>](#pen-and-touch)
-   [<span data-ttu-id="c2ce9-150">個人化</span><span class="sxs-lookup"><span data-stu-id="c2ce9-150">Personalization</span></span>](#personalization)
-   [<span data-ttu-id="c2ce9-151">電話和數據機</span><span class="sxs-lookup"><span data-stu-id="c2ce9-151">Phone and Modem</span></span>](#phone-and-modem)
-   [<span data-ttu-id="c2ce9-152">電源選項</span><span class="sxs-lookup"><span data-stu-id="c2ce9-152">Power Options</span></span>](#power-options)
-   <span data-ttu-id="c2ce9-153">[[程式和功能]](#programs-and-features)</span><span class="sxs-lookup"><span data-stu-id="c2ce9-153">[Programs and Features](#programs-and-features)</span></span>
-   [<span data-ttu-id="c2ce9-154">復原</span><span class="sxs-lookup"><span data-stu-id="c2ce9-154">Recovery</span></span>](#recovery)
-   [<span data-ttu-id="c2ce9-155">區域</span><span class="sxs-lookup"><span data-stu-id="c2ce9-155">Region</span></span>](#region)
-   [<span data-ttu-id="c2ce9-156">RemoteApp 和桌面連線</span><span class="sxs-lookup"><span data-stu-id="c2ce9-156">RemoteApp and Desktop Connections</span></span>](#remoteapp-and-desktop-connections)
-   [<span data-ttu-id="c2ce9-157">音效</span><span class="sxs-lookup"><span data-stu-id="c2ce9-157">Sound</span></span>](#sound)
-   [<span data-ttu-id="c2ce9-158">語音辨識</span><span class="sxs-lookup"><span data-stu-id="c2ce9-158">Speech Recognition</span></span>](#speech-recognition)
-   [<span data-ttu-id="c2ce9-159">儲存空間</span><span class="sxs-lookup"><span data-stu-id="c2ce9-159">Storage Spaces</span></span>](#storage-spaces)
-   [<span data-ttu-id="c2ce9-160">同步中心</span><span class="sxs-lookup"><span data-stu-id="c2ce9-160">Sync Center</span></span>](#sync-center)
-   [<span data-ttu-id="c2ce9-161">系統</span><span class="sxs-lookup"><span data-stu-id="c2ce9-161">System</span></span>](#system)
-   [<span data-ttu-id="c2ce9-162">Tablet PC 設定</span><span class="sxs-lookup"><span data-stu-id="c2ce9-162">Tablet PC Settings</span></span>](#tablet-pc-settings)
-   [<span data-ttu-id="c2ce9-163">工作列和流覽</span><span class="sxs-lookup"><span data-stu-id="c2ce9-163">Taskbar and Navigation</span></span>](#taskbar-and-navigation)
-   [<span data-ttu-id="c2ce9-164">疑難排解</span><span class="sxs-lookup"><span data-stu-id="c2ce9-164">Troubleshooting</span></span>](#troubleshooting)
-   [<span data-ttu-id="c2ce9-165">TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="c2ce9-165">TSAppInstall</span></span>](#tsappinstall)
-   [<span data-ttu-id="c2ce9-166">使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="c2ce9-166">User Accounts</span></span>](#user-accounts)
-   [<span data-ttu-id="c2ce9-167">Windows Anytime Upgrade</span><span class="sxs-lookup"><span data-stu-id="c2ce9-167">Windows Anytime Upgrade</span></span>](#windows-anytime-upgrade)
-   [<span data-ttu-id="c2ce9-168">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="c2ce9-168">Windows Defender</span></span>](#windows-defender)
-   [<span data-ttu-id="c2ce9-169">Windows 防火牆</span><span class="sxs-lookup"><span data-stu-id="c2ce9-169">Windows Firewall</span></span>](#windows-firewall)
-   [<span data-ttu-id="c2ce9-170">Windows 行動中心</span><span class="sxs-lookup"><span data-stu-id="c2ce9-170">Windows Mobility Center</span></span>](#windows-mobility-center)
-   [<span data-ttu-id="c2ce9-171">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="c2ce9-171">Windows To Go</span></span>](#windows-to-go)
-   [<span data-ttu-id="c2ce9-172">Windows Update</span><span class="sxs-lookup"><span data-stu-id="c2ce9-172">Windows Update</span></span>](#windows-update)
-   [<span data-ttu-id="c2ce9-173">工作資料夾</span><span class="sxs-lookup"><span data-stu-id="c2ce9-173">Work Folders</span></span>](#work-folders)

### <a name="action-center"></a><span data-ttu-id="c2ce9-174">控制中心</span><span class="sxs-lookup"><span data-stu-id="c2ce9-174">Action Center</span></span>

-   <span data-ttu-id="c2ce9-175">正式 **名稱**： Microsoft. ActionCenter</span><span class="sxs-lookup"><span data-stu-id="c2ce9-175">**Canonical name**: Microsoft.ActionCenter</span></span>
-   <span data-ttu-id="c2ce9-176">**GUID**： {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-176">**GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span></span>
-   <span data-ttu-id="c2ce9-177">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-177">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-178">**模組名稱**： @% SystemRoot% \\ System32 \\ActionCenterCPL.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-178">**Module name**: @%SystemRoot%\\System32\\ActionCenterCPL.dll,-1</span></span>
-   <span data-ttu-id="c2ce9-179">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-179">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-180">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-180">Page Name</span></span>           | <span data-ttu-id="c2ce9-181">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-181">Opens</span></span>                      |
    |---------------------|----------------------------|
    | <span data-ttu-id="c2ce9-182">MaintenanceSettings</span><span class="sxs-lookup"><span data-stu-id="c2ce9-182">MaintenanceSettings</span></span> | <span data-ttu-id="c2ce9-183">自動維護</span><span class="sxs-lookup"><span data-stu-id="c2ce9-183">Automatic Maintenance</span></span>      |
    | <span data-ttu-id="c2ce9-184">pageProblems</span><span class="sxs-lookup"><span data-stu-id="c2ce9-184">pageProblems</span></span>        | <span data-ttu-id="c2ce9-185">問題報告</span><span class="sxs-lookup"><span data-stu-id="c2ce9-185">Problem Reports</span></span>            |
    | <span data-ttu-id="c2ce9-186">pageReliabilityView</span><span class="sxs-lookup"><span data-stu-id="c2ce9-186">pageReliabilityView</span></span> | <span data-ttu-id="c2ce9-187">可靠性監視器</span><span class="sxs-lookup"><span data-stu-id="c2ce9-187">Reliability Monitor</span></span>        |
    | <span data-ttu-id="c2ce9-188">pageResponseArchive</span><span class="sxs-lookup"><span data-stu-id="c2ce9-188">pageResponseArchive</span></span> | <span data-ttu-id="c2ce9-189">封存的訊息</span><span class="sxs-lookup"><span data-stu-id="c2ce9-189">Archived Messages</span></span>          |
    | <span data-ttu-id="c2ce9-190">pageSettings</span><span class="sxs-lookup"><span data-stu-id="c2ce9-190">pageSettings</span></span>        | <span data-ttu-id="c2ce9-191">問題報告設定</span><span class="sxs-lookup"><span data-stu-id="c2ce9-191">Problem Reporting Settings</span></span> |

    

     

### <a name="administrative-tools"></a><span data-ttu-id="c2ce9-192">[系統管理工具]</span><span class="sxs-lookup"><span data-stu-id="c2ce9-192">Administrative Tools</span></span>

-   <span data-ttu-id="c2ce9-193">正式 **名稱**： Microsoft. 依次</span><span class="sxs-lookup"><span data-stu-id="c2ce9-193">**Canonical name**: Microsoft.AdministrativeTools</span></span>
-   <span data-ttu-id="c2ce9-194">**GUID**： {D20EA4E1-3957-11d2-A40B-0C5020524153}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-194">**GUID**: {D20EA4E1-3957-11d2-A40B-0C5020524153}</span></span>
-   <span data-ttu-id="c2ce9-195">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-195">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-196">**模組名稱**： @% SystemRoot% \\ system32 \\shell32.dll，-22982</span><span class="sxs-lookup"><span data-stu-id="c2ce9-196">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22982</span></span>

### <a name="autoplay"></a><span data-ttu-id="c2ce9-197">自動播放</span><span class="sxs-lookup"><span data-stu-id="c2ce9-197">AutoPlay</span></span>

-   <span data-ttu-id="c2ce9-198">正式 **名稱**： Microsoft. 自動播放</span><span class="sxs-lookup"><span data-stu-id="c2ce9-198">**Canonical name**: Microsoft.AutoPlay</span></span>
-   <span data-ttu-id="c2ce9-199">**GUID**： {9C60DE1E-E5FC-40f4-A487-460851A8D915}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-199">**GUID**: {9C60DE1E-E5FC-40f4-A487-460851A8D915}</span></span>
-   <span data-ttu-id="c2ce9-200">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-200">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-201">**模組名稱**： @% SystemRoot% \\ System32 \\autoplay.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-201">**Module name**: @%SystemRoot%\\System32\\autoplay.dll,-1</span></span>

### <a name="biometric-devices"></a><span data-ttu-id="c2ce9-202">生物特徵辨識裝置</span><span class="sxs-lookup"><span data-stu-id="c2ce9-202">Biometric Devices</span></span>

-   <span data-ttu-id="c2ce9-203">正式 **名稱**： Microsoft. BiometricDevices</span><span class="sxs-lookup"><span data-stu-id="c2ce9-203">**Canonical name**: Microsoft.BiometricDevices</span></span>
-   <span data-ttu-id="c2ce9-204">**GUID**： {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-204">**GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span></span>
-   <span data-ttu-id="c2ce9-205">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-205">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-206">**模組名稱**： @% SystemRoot% \\ System32 \\biocpl.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-206">**Module name**: @%SystemRoot%\\System32\\biocpl.dll,-1</span></span>

### <a name="bitlocker-drive-encryption"></a><span data-ttu-id="c2ce9-207">BitLocker 磁碟機加密</span><span class="sxs-lookup"><span data-stu-id="c2ce9-207">BitLocker Drive Encryption</span></span>

-   <span data-ttu-id="c2ce9-208">正式 **名稱**： Microsoft. microsoft.bitlockerdriveencryption</span><span class="sxs-lookup"><span data-stu-id="c2ce9-208">**Canonical name**: Microsoft.BitLockerDriveEncryption</span></span>
-   <span data-ttu-id="c2ce9-209">**GUID**： {D9EF8727-CAC2-4e60-809E-86F80A666C91}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-209">**GUID**: {D9EF8727-CAC2-4e60-809E-86F80A666C91}</span></span>
-   <span data-ttu-id="c2ce9-210">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-210">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-211">**模組名稱**： @% SystemRoot% \\ System32 \\fvecpl.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-211">**Module name**: @%SystemRoot%\\System32\\fvecpl.dll,-1</span></span>

### <a name="color-management"></a><span data-ttu-id="c2ce9-212">色彩管理</span><span class="sxs-lookup"><span data-stu-id="c2ce9-212">Color Management</span></span>

-   <span data-ttu-id="c2ce9-213">正式 **名稱**： Microsoft. ColorManagement</span><span class="sxs-lookup"><span data-stu-id="c2ce9-213">**Canonical name**: Microsoft.ColorManagement</span></span>
-   <span data-ttu-id="c2ce9-214">**GUID**： {B2C761C6-29BC-4f19-9251-E6195265BAF1}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-214">**GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}</span></span>
-   <span data-ttu-id="c2ce9-215">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-215">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-216">**模組名稱**： @% systemroot% \\ system32 \\colorcpl.exe，-6</span><span class="sxs-lookup"><span data-stu-id="c2ce9-216">**Module name**: @%systemroot%\\system32\\colorcpl.exe,-6</span></span>

### <a name="credential-manager"></a><span data-ttu-id="c2ce9-217">認證管理員</span><span class="sxs-lookup"><span data-stu-id="c2ce9-217">Credential Manager</span></span>

-   <span data-ttu-id="c2ce9-218">正式 **名稱**： Microsoft. CredentialManager</span><span class="sxs-lookup"><span data-stu-id="c2ce9-218">**Canonical name**: Microsoft.CredentialManager</span></span>
-   <span data-ttu-id="c2ce9-219">**GUID**： {1206F5F1-0569-412C-8FEC-3204630DFB70}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-219">**GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}</span></span>
-   <span data-ttu-id="c2ce9-220">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-220">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-221">**模組名稱**： @% SystemRoot% \\ system32 \\Vault.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-221">**Module name**: @%SystemRoot%\\system32\\Vault.dll,-1</span></span>
-   <span data-ttu-id="c2ce9-222">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-222">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-223">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-223">Page Name</span></span>                   | <span data-ttu-id="c2ce9-224">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-224">Opens</span></span>               |
    |-----------------------------|---------------------|
    | <span data-ttu-id="c2ce9-225">?SelectedVault = CredmanVault</span><span class="sxs-lookup"><span data-stu-id="c2ce9-225">?SelectedVault=CredmanVault</span></span> | <span data-ttu-id="c2ce9-226">Windows 認證</span><span class="sxs-lookup"><span data-stu-id="c2ce9-226">Windows Credentials</span></span> |

    

     

### <a name="date-and-time"></a><span data-ttu-id="c2ce9-227">日期及時間</span><span class="sxs-lookup"><span data-stu-id="c2ce9-227">Date and Time</span></span>

-   <span data-ttu-id="c2ce9-228">正式 **名稱**： Microsoft. >formatting.dateandtime.custom</span><span class="sxs-lookup"><span data-stu-id="c2ce9-228">**Canonical name**: Microsoft.DateAndTime</span></span>
-   <span data-ttu-id="c2ce9-229">**GUID**： {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-229">**GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}</span></span>
-   <span data-ttu-id="c2ce9-230">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-230">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-231">**模組名稱**： @% SystemRoot% \\ System32 \\timedate.cpl，-51</span><span class="sxs-lookup"><span data-stu-id="c2ce9-231">**Module name**: @%SystemRoot%\\System32\\timedate.cpl,-51</span></span>
-   <span data-ttu-id="c2ce9-232">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-232">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-233">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-233">Page Name</span></span> | <span data-ttu-id="c2ce9-234">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-234">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="c2ce9-235">1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-235">1</span></span>         | <span data-ttu-id="c2ce9-236">其他時鐘</span><span class="sxs-lookup"><span data-stu-id="c2ce9-236">Additional Clocks</span></span> |

    

     

### <a name="default-programs"></a><span data-ttu-id="c2ce9-237">預設程式</span><span class="sxs-lookup"><span data-stu-id="c2ce9-237">Default Programs</span></span>

-   <span data-ttu-id="c2ce9-238">正式 **名稱**： Microsoft. DefaultPrograms</span><span class="sxs-lookup"><span data-stu-id="c2ce9-238">**Canonical name**: Microsoft.DefaultPrograms</span></span>
-   <span data-ttu-id="c2ce9-239">**GUID**： {17cd9488-1228-4b2f-88ce-4298e93e0966}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-239">**GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}</span></span>
-   <span data-ttu-id="c2ce9-240">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-240">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-241">**模組名稱**： @% SystemRoot% \\ System32 \\sud.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-241">**Module name**: @%SystemRoot%\\System32\\sud.dll,-1</span></span>
-   <span data-ttu-id="c2ce9-242">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-242">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-243">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-243">Page Name</span></span>          | <span data-ttu-id="c2ce9-244">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-244">Opens</span></span>                |
    |--------------------|----------------------|
    | <span data-ttu-id="c2ce9-245">pageDefaultProgram</span><span class="sxs-lookup"><span data-stu-id="c2ce9-245">pageDefaultProgram</span></span> | <span data-ttu-id="c2ce9-246">設定預設程式</span><span class="sxs-lookup"><span data-stu-id="c2ce9-246">Set Default Programs</span></span> |
    | <span data-ttu-id="c2ce9-247">pageFileAssoc</span><span class="sxs-lookup"><span data-stu-id="c2ce9-247">pageFileAssoc</span></span>      | <span data-ttu-id="c2ce9-248">設定關聯</span><span class="sxs-lookup"><span data-stu-id="c2ce9-248">Set Associations</span></span>     |

    

     

### <a name="device-manager"></a><span data-ttu-id="c2ce9-249">裝置管理員</span><span class="sxs-lookup"><span data-stu-id="c2ce9-249">Device Manager</span></span>

-   <span data-ttu-id="c2ce9-250">正式 **名稱**： Microsoft. DeviceManager</span><span class="sxs-lookup"><span data-stu-id="c2ce9-250">**Canonical name**: Microsoft.DeviceManager</span></span>
-   <span data-ttu-id="c2ce9-251">**GUID**： {74246bfc-4c96-11d0-abef-0020af6b0b7a}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-251">**GUID**: {74246bfc-4c96-11d0-abef-0020af6b0b7a}</span></span>
-   <span data-ttu-id="c2ce9-252">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-252">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-253">**模組名稱**： @% SystemRoot% \\ System32 \\devmgr.dll，-4</span><span class="sxs-lookup"><span data-stu-id="c2ce9-253">**Module name**: @%SystemRoot%\\System32\\devmgr.dll,-4</span></span>

### <a name="devices-and-printers"></a><span data-ttu-id="c2ce9-254">[裝置和印表機]</span><span class="sxs-lookup"><span data-stu-id="c2ce9-254">Devices and Printers</span></span>

-   <span data-ttu-id="c2ce9-255">正式 **名稱**： Microsoft. DevicesAndPrinters</span><span class="sxs-lookup"><span data-stu-id="c2ce9-255">**Canonical name**: Microsoft.DevicesAndPrinters</span></span>
-   <span data-ttu-id="c2ce9-256">**GUID**： {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-256">**GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span></span>
-   <span data-ttu-id="c2ce9-257">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-257">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-258">**模組名稱**： @% systemroot% \\ system32 \\DeviceCenter.dll，-1000</span><span class="sxs-lookup"><span data-stu-id="c2ce9-258">**Module name**: @%systemroot%\\system32\\DeviceCenter.dll,-1000</span></span>

### <a name="display"></a><span data-ttu-id="c2ce9-259">顯示</span><span class="sxs-lookup"><span data-stu-id="c2ce9-259">Display</span></span>

-   <span data-ttu-id="c2ce9-260">正式 **名稱**： Microsoft. Display</span><span class="sxs-lookup"><span data-stu-id="c2ce9-260">**Canonical name**: Microsoft.Display</span></span>
-   <span data-ttu-id="c2ce9-261">**GUID**： {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-261">**GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span></span>
-   <span data-ttu-id="c2ce9-262">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-262">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-263">**模組名稱**： @% SystemRoot% \\ System32 \\Display.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-263">**Module name**: @%SystemRoot%\\System32\\Display.dll,-1</span></span>
-   <span data-ttu-id="c2ce9-264">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-264">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-265">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-265">Page Name</span></span> | <span data-ttu-id="c2ce9-266">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-266">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="c2ce9-267">設定</span><span class="sxs-lookup"><span data-stu-id="c2ce9-267">Settings</span></span>  | <span data-ttu-id="c2ce9-268">螢幕解析度</span><span class="sxs-lookup"><span data-stu-id="c2ce9-268">Screen Resolution</span></span> |

    

     

### <a name="ease-of-access-center"></a><span data-ttu-id="c2ce9-269">輕鬆存取中心</span><span class="sxs-lookup"><span data-stu-id="c2ce9-269">Ease of Access Center</span></span>

-   <span data-ttu-id="c2ce9-270">正式 **名稱**： Microsoft. EaseOfAccessCenter</span><span class="sxs-lookup"><span data-stu-id="c2ce9-270">**Canonical name**: Microsoft.EaseOfAccessCenter</span></span>
-   <span data-ttu-id="c2ce9-271">**GUID**： {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-271">**GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span></span>
-   <span data-ttu-id="c2ce9-272">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-272">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-273">**模組名稱**： @% SystemRoot% \\ System32 \\accessibilitycpl.dll，-10</span><span class="sxs-lookup"><span data-stu-id="c2ce9-273">**Module name**: @%SystemRoot%\\System32\\accessibilitycpl.dll,-10</span></span>
-   <span data-ttu-id="c2ce9-274">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-274">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-275">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-275">Page Name</span></span>               | <span data-ttu-id="c2ce9-276">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-276">Opens</span></span>                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | <span data-ttu-id="c2ce9-277">pageEasierToClick</span><span class="sxs-lookup"><span data-stu-id="c2ce9-277">pageEasierToClick</span></span>       | <span data-ttu-id="c2ce9-278">讓滑鼠更容易使用</span><span class="sxs-lookup"><span data-stu-id="c2ce9-278">Make the mouse easier to use</span></span>                                        |
    | <span data-ttu-id="c2ce9-279">pageEasierToSee</span><span class="sxs-lookup"><span data-stu-id="c2ce9-279">pageEasierToSee</span></span>         | <span data-ttu-id="c2ce9-280">讓電腦看得更清楚</span><span class="sxs-lookup"><span data-stu-id="c2ce9-280">Make the computer easier to see</span></span>                                     |
    | <span data-ttu-id="c2ce9-281">pageEasierWithSounds</span><span class="sxs-lookup"><span data-stu-id="c2ce9-281">pageEasierWithSounds</span></span>    | <span data-ttu-id="c2ce9-282">使用文字或視覺效果替代音效</span><span class="sxs-lookup"><span data-stu-id="c2ce9-282">Use text or visual alternatives for sounds</span></span>                          |
    | <span data-ttu-id="c2ce9-283">pageFilterKeysSettings</span><span class="sxs-lookup"><span data-stu-id="c2ce9-283">pageFilterKeysSettings</span></span>  | <span data-ttu-id="c2ce9-284">設定篩選金鑰</span><span class="sxs-lookup"><span data-stu-id="c2ce9-284">Set up Filter Keys</span></span>                                                  |
    | <span data-ttu-id="c2ce9-285">pageKeyboardEasierToUse</span><span class="sxs-lookup"><span data-stu-id="c2ce9-285">pageKeyboardEasierToUse</span></span> | <span data-ttu-id="c2ce9-286">讓鍵盤更容易使用</span><span class="sxs-lookup"><span data-stu-id="c2ce9-286">Make the keyboard easier to use</span></span>                                     |
    | <span data-ttu-id="c2ce9-287">pageNoMouseOrKeyboard</span><span class="sxs-lookup"><span data-stu-id="c2ce9-287">pageNoMouseOrKeyboard</span></span>   | <span data-ttu-id="c2ce9-288">不透過滑鼠或鍵盤來使用電腦</span><span class="sxs-lookup"><span data-stu-id="c2ce9-288">Use the computer without a mouse or keyboard</span></span>                        |
    | <span data-ttu-id="c2ce9-289">pageNoVisual</span><span class="sxs-lookup"><span data-stu-id="c2ce9-289">pageNoVisual</span></span>            | <span data-ttu-id="c2ce9-290">不透過顯示器來使用電腦</span><span class="sxs-lookup"><span data-stu-id="c2ce9-290">Use the computer without a display</span></span>                                  |
    | <span data-ttu-id="c2ce9-291">pageQuestionsCognitive</span><span class="sxs-lookup"><span data-stu-id="c2ce9-291">pageQuestionsCognitive</span></span>  | <span data-ttu-id="c2ce9-292">取得建議，讓您的電腦更容易使用 (認知) </span><span class="sxs-lookup"><span data-stu-id="c2ce9-292">Get recommendations to make your computer easier to use (cognitive)</span></span> |
    | <span data-ttu-id="c2ce9-293">pageQuestionsEyesight</span><span class="sxs-lookup"><span data-stu-id="c2ce9-293">pageQuestionsEyesight</span></span>   | <span data-ttu-id="c2ce9-294">取得建議，讓您的電腦更容易使用 (視力) </span><span class="sxs-lookup"><span data-stu-id="c2ce9-294">Get recommendations to make your computer easier to use (eyesight)</span></span>  |

    

     

### <a name="family-safety"></a><span data-ttu-id="c2ce9-295">家庭安全</span><span class="sxs-lookup"><span data-stu-id="c2ce9-295">Family Safety</span></span>

-   <span data-ttu-id="c2ce9-296">正式 **名稱**： Microsoft. ParentalControls</span><span class="sxs-lookup"><span data-stu-id="c2ce9-296">**Canonical name**: Microsoft.ParentalControls</span></span>
-   <span data-ttu-id="c2ce9-297">**GUID**： {96AE8D84-A250-4520-95A5-A47A7E3C548B}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-297">**GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}</span></span>
-   <span data-ttu-id="c2ce9-298">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-298">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-299">**模組名稱**： @% SystemRoot% \\ System32 \\wpccpl.dll，-100</span><span class="sxs-lookup"><span data-stu-id="c2ce9-299">**Module name**: @%SystemRoot%\\System32\\wpccpl.dll,-100</span></span>
-   <span data-ttu-id="c2ce9-300">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-300">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-301">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-301">Page Name</span></span>   | <span data-ttu-id="c2ce9-302">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-302">Opens</span></span>                                  |
    |-------------|----------------------------------------|
    | <span data-ttu-id="c2ce9-303">pageUserHub</span><span class="sxs-lookup"><span data-stu-id="c2ce9-303">pageUserHub</span></span> | <span data-ttu-id="c2ce9-304">選擇使用者並設定家庭安全</span><span class="sxs-lookup"><span data-stu-id="c2ce9-304">Choose a user and set up Family Safety</span></span> |

    

     

### <a name="file-history"></a><span data-ttu-id="c2ce9-305">檔案歷程記錄</span><span class="sxs-lookup"><span data-stu-id="c2ce9-305">File History</span></span>

-   <span data-ttu-id="c2ce9-306">正式 **名稱**： Microsoft. FileHistory</span><span class="sxs-lookup"><span data-stu-id="c2ce9-306">**Canonical name**: Microsoft.FileHistory</span></span>
-   <span data-ttu-id="c2ce9-307">**GUID**： {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-307">**GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span></span>
-   <span data-ttu-id="c2ce9-308">**支援的 OS**： Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-308">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-309">**模組名稱**： @% SystemRoot% \\ System32 \\fhcpl.dll，-52</span><span class="sxs-lookup"><span data-stu-id="c2ce9-309">**Module name**: @%SystemRoot%\\System32\\fhcpl.dll,-52</span></span>
-   <span data-ttu-id="c2ce9-310">檔案歷程記錄包含較新版本的備份和還原專案，但較舊的專案的正式名稱不會重新對應到檔案歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-310">File History includes a newer version of the Backup and Restore item, but that older item's canonical name does not remap to File History.</span></span>

### <a name="folder-options"></a><span data-ttu-id="c2ce9-311">資料夾選項</span><span class="sxs-lookup"><span data-stu-id="c2ce9-311">Folder Options</span></span>

-   <span data-ttu-id="c2ce9-312">正式 **名稱**： Microsoft. FolderOptions</span><span class="sxs-lookup"><span data-stu-id="c2ce9-312">**Canonical name**: Microsoft.FolderOptions</span></span>
-   <span data-ttu-id="c2ce9-313">**GUID**： {6DFD7C5C-2451-11d3-A299-00C04F8EF6AF}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-313">**GUID**: {6DFD7C5C-2451-11d3-A299-00C04F8EF6AF}</span></span>
-   <span data-ttu-id="c2ce9-314">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-314">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-315">**模組名稱**： @% SystemRoot% \\ system32 \\shell32.dll，-22985</span><span class="sxs-lookup"><span data-stu-id="c2ce9-315">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22985</span></span>

### <a name="fonts"></a><span data-ttu-id="c2ce9-316">字型</span><span class="sxs-lookup"><span data-stu-id="c2ce9-316">Fonts</span></span>

-   <span data-ttu-id="c2ce9-317">正式 **名稱**： Microsoft 字型</span><span class="sxs-lookup"><span data-stu-id="c2ce9-317">**Canonical name**: Microsoft.Fonts</span></span>
-   <span data-ttu-id="c2ce9-318">**GUID**： {93412589-74D4-4E4E-AD0E-E0CB621440FD}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-318">**GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}</span></span>
-   <span data-ttu-id="c2ce9-319">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-319">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-320">**模組名稱**： @% SystemRoot% \\ System32 \\FontExt.dll，-8007</span><span class="sxs-lookup"><span data-stu-id="c2ce9-320">**Module name**: @%SystemRoot%\\System32\\FontExt.dll,-8007</span></span>

### <a name="homegroup"></a><span data-ttu-id="c2ce9-321">HomeGroup</span><span class="sxs-lookup"><span data-stu-id="c2ce9-321">HomeGroup</span></span>

-   <span data-ttu-id="c2ce9-322">正式 **名稱**： Microsoft. 家庭</span><span class="sxs-lookup"><span data-stu-id="c2ce9-322">**Canonical name**: Microsoft.HomeGroup</span></span>
-   <span data-ttu-id="c2ce9-323">**GUID**： {67CA7650-96E6-4FDD-BB43-A8E774F73A57}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-323">**GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}</span></span>
-   <span data-ttu-id="c2ce9-324">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-324">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-325">**模組名稱**： @% SystemRoot% \\ System32 \\hgcpl.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-325">**Module name**: @%SystemRoot%\\System32\\hgcpl.dll,-1</span></span>

### <a name="indexing-options"></a><span data-ttu-id="c2ce9-326">索引編製選項</span><span class="sxs-lookup"><span data-stu-id="c2ce9-326">Indexing Options</span></span>

-   <span data-ttu-id="c2ce9-327">正式 **名稱**： Microsoft. IndexingOptions</span><span class="sxs-lookup"><span data-stu-id="c2ce9-327">**Canonical name**: Microsoft.IndexingOptions</span></span>
-   <span data-ttu-id="c2ce9-328">**GUID**： {87D66A43-7B11-4A28-9811-C86EE395ACF7}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-328">**GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}</span></span>
-   <span data-ttu-id="c2ce9-329">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-329">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-330">**模組名稱**： @% SystemRoot% \\ System32 \\srchadmin.dll，-601</span><span class="sxs-lookup"><span data-stu-id="c2ce9-330">**Module name**: @%SystemRoot%\\System32\\srchadmin.dll,-601</span></span>

### <a name="infrared"></a><span data-ttu-id="c2ce9-331">紅外線</span><span class="sxs-lookup"><span data-stu-id="c2ce9-331">Infrared</span></span>

-   <span data-ttu-id="c2ce9-332">正式 **名稱**： Microsoft 紅外線</span><span class="sxs-lookup"><span data-stu-id="c2ce9-332">**Canonical name**: Microsoft.Infrared</span></span>
-   <span data-ttu-id="c2ce9-333">**GUID**： {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-333">**GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span>
-   <span data-ttu-id="c2ce9-334">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-334">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-335">**模組名稱**： @% SystemRoot% \\ System32 \\irprops.cpl，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-335">**Module name**: @%SystemRoot%\\System32\\irprops.cpl,-1</span></span>

### <a name="internet-options"></a><span data-ttu-id="c2ce9-336">網際網路選項</span><span class="sxs-lookup"><span data-stu-id="c2ce9-336">Internet Options</span></span>

-   <span data-ttu-id="c2ce9-337">正式 **名稱**： Microsoft. InternetOptions</span><span class="sxs-lookup"><span data-stu-id="c2ce9-337">**Canonical name**: Microsoft.InternetOptions</span></span>
-   <span data-ttu-id="c2ce9-338">**GUID**： {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-338">**GUID**: {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}</span></span>
-   <span data-ttu-id="c2ce9-339">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-339">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-340">**模組名稱**： @C: \\ Windows \\ System32 \\inetcpl.cpl、-4312</span><span class="sxs-lookup"><span data-stu-id="c2ce9-340">**Module name**: @C:\\Windows\\System32\\inetcpl.cpl,-4312</span></span>
-   <span data-ttu-id="c2ce9-341">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-341">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-342">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-342">Page Name</span></span> | <span data-ttu-id="c2ce9-343">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-343">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="c2ce9-344">1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-344">1</span></span>         | <span data-ttu-id="c2ce9-345">安全性</span><span class="sxs-lookup"><span data-stu-id="c2ce9-345">Security</span></span>    |
    | <span data-ttu-id="c2ce9-346">2</span><span class="sxs-lookup"><span data-stu-id="c2ce9-346">2</span></span>         | <span data-ttu-id="c2ce9-347">隱私權</span><span class="sxs-lookup"><span data-stu-id="c2ce9-347">Privacy</span></span>     |
    | <span data-ttu-id="c2ce9-348">3</span><span class="sxs-lookup"><span data-stu-id="c2ce9-348">3</span></span>         | <span data-ttu-id="c2ce9-349">Content</span><span class="sxs-lookup"><span data-stu-id="c2ce9-349">Content</span></span>     |
    | <span data-ttu-id="c2ce9-350">4</span><span class="sxs-lookup"><span data-stu-id="c2ce9-350">4</span></span>         | <span data-ttu-id="c2ce9-351">連接</span><span class="sxs-lookup"><span data-stu-id="c2ce9-351">Connections</span></span> |
    | <span data-ttu-id="c2ce9-352">5</span><span class="sxs-lookup"><span data-stu-id="c2ce9-352">5</span></span>         | <span data-ttu-id="c2ce9-353">程式</span><span class="sxs-lookup"><span data-stu-id="c2ce9-353">Programs</span></span>    |
    | <span data-ttu-id="c2ce9-354">6</span><span class="sxs-lookup"><span data-stu-id="c2ce9-354">6</span></span>         | <span data-ttu-id="c2ce9-355">進階</span><span class="sxs-lookup"><span data-stu-id="c2ce9-355">Advanced</span></span>    |

    

     

### <a name="iscsi-initiator"></a><span data-ttu-id="c2ce9-356">iSCSI 啟動器</span><span class="sxs-lookup"><span data-stu-id="c2ce9-356">iSCSI Initiator</span></span>

-   <span data-ttu-id="c2ce9-357">正式 **名稱**： Microsoft. iSCSIInitiator</span><span class="sxs-lookup"><span data-stu-id="c2ce9-357">**Canonical name**: Microsoft.iSCSIInitiator</span></span>
-   <span data-ttu-id="c2ce9-358">**GUID**： {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-358">**GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span></span>
-   <span data-ttu-id="c2ce9-359">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-359">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-360">**模組名稱**： @% SystemRoot% \\ System32 \\iscsicpl.dll，-5001</span><span class="sxs-lookup"><span data-stu-id="c2ce9-360">**Module name**: @%SystemRoot%\\System32\\iscsicpl.dll,-5001</span></span>

### <a name="isns-server"></a><span data-ttu-id="c2ce9-361">iSNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="c2ce9-361">iSNS Server</span></span>

-   <span data-ttu-id="c2ce9-362">正式 **名稱**： Microsoft. iSNSServer</span><span class="sxs-lookup"><span data-stu-id="c2ce9-362">**Canonical name**: Microsoft.iSNSServer</span></span>
-   <span data-ttu-id="c2ce9-363">**GUID**： {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-363">**GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}</span></span>
-   <span data-ttu-id="c2ce9-364">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-364">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-365">**模組名稱**： @% SystemRoot% \\ System32 \\isnssrv.dll，-5005</span><span class="sxs-lookup"><span data-stu-id="c2ce9-365">**Module name**: @%SystemRoot%\\System32\\isnssrv.dll,-5005</span></span>
-   <span data-ttu-id="c2ce9-366">此主控台專案只會在伺服器版本的 Windows 中看到。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-366">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="keyboard"></a><span data-ttu-id="c2ce9-367">鍵盤</span><span class="sxs-lookup"><span data-stu-id="c2ce9-367">Keyboard</span></span>

-   <span data-ttu-id="c2ce9-368">正式 **名稱**： Microsoft. 鍵盤</span><span class="sxs-lookup"><span data-stu-id="c2ce9-368">**Canonical name**: Microsoft.Keyboard</span></span>
-   <span data-ttu-id="c2ce9-369">**GUID**： {725BE8F7-668E-4C7B-8F90-46BDB0936430}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-369">**GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}</span></span>
-   <span data-ttu-id="c2ce9-370">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-370">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-371">**模組名稱**： @% SystemRoot% \\ System32 \\main.cpl，-102</span><span class="sxs-lookup"><span data-stu-id="c2ce9-371">**Module name**: @%SystemRoot%\\System32\\main.cpl,-102</span></span>

### <a name="location-settings"></a><span data-ttu-id="c2ce9-372">位置設定</span><span class="sxs-lookup"><span data-stu-id="c2ce9-372">Location Settings</span></span>

-   <span data-ttu-id="c2ce9-373">正式 **名稱**： Microsoft. LocationSettings</span><span class="sxs-lookup"><span data-stu-id="c2ce9-373">**Canonical name**: Microsoft.LocationSettings</span></span>
-   <span data-ttu-id="c2ce9-374">**GUID**： {E9950154-C418-419e-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-374">**GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}</span></span>
-   <span data-ttu-id="c2ce9-375">**支援的 OS**： Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-375">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-376">**模組名稱**： @% SystemRoot% \\ System32 \\SensorsCpl.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-376">**Module name**: @%SystemRoot%\\System32\\SensorsCpl.dll,-1</span></span>

### <a name="mouse"></a><span data-ttu-id="c2ce9-377">滑鼠</span><span class="sxs-lookup"><span data-stu-id="c2ce9-377">Mouse</span></span>

-   <span data-ttu-id="c2ce9-378">正式 **名稱**： Microsoft. 滑鼠</span><span class="sxs-lookup"><span data-stu-id="c2ce9-378">**Canonical name**: Microsoft.Mouse</span></span>
-   <span data-ttu-id="c2ce9-379">**GUID**： {6C8EEC18-8D75-41B2-A177-8831D59D2D50}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-379">**GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}</span></span>
-   <span data-ttu-id="c2ce9-380">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-380">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-381">**模組名稱**： @% SystemRoot% \\ System32 \\main.cpl，-100</span><span class="sxs-lookup"><span data-stu-id="c2ce9-381">**Module name**: @%SystemRoot%\\System32\\main.cpl,-100</span></span>
-   <span data-ttu-id="c2ce9-382">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-382">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-383">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-383">Page Name</span></span> | <span data-ttu-id="c2ce9-384">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-384">Opens</span></span>           |
    |-----------|-----------------|
    | <span data-ttu-id="c2ce9-385">1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-385">1</span></span>         | <span data-ttu-id="c2ce9-386">指標</span><span class="sxs-lookup"><span data-stu-id="c2ce9-386">Pointers</span></span>        |
    | <span data-ttu-id="c2ce9-387">2</span><span class="sxs-lookup"><span data-stu-id="c2ce9-387">2</span></span>         | <span data-ttu-id="c2ce9-388">指標選項</span><span class="sxs-lookup"><span data-stu-id="c2ce9-388">Pointer Options</span></span> |
    | <span data-ttu-id="c2ce9-389">3</span><span class="sxs-lookup"><span data-stu-id="c2ce9-389">3</span></span>         | <span data-ttu-id="c2ce9-390">Wheel</span><span class="sxs-lookup"><span data-stu-id="c2ce9-390">Wheel</span></span>           |
    | <span data-ttu-id="c2ce9-391">4</span><span class="sxs-lookup"><span data-stu-id="c2ce9-391">4</span></span>         | <span data-ttu-id="c2ce9-392">硬體</span><span class="sxs-lookup"><span data-stu-id="c2ce9-392">Hardware</span></span>        |

    

     

### <a name="mpioconfiguration"></a><span data-ttu-id="c2ce9-393">MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2ce9-393">MPIOConfiguration</span></span>

-   <span data-ttu-id="c2ce9-394">正式 **名稱**： Microsoft. MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2ce9-394">**Canonical name**: Microsoft.MPIOConfiguration</span></span>
-   <span data-ttu-id="c2ce9-395">**GUID**： {AB3BE6AA-7561-4838-AB77-ACF8427DF426}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-395">**GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}</span></span>
-   <span data-ttu-id="c2ce9-396">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-396">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-397">**模組名稱**： @% SystemRoot% \\ System32 \\mpiocpl.dll，-1000</span><span class="sxs-lookup"><span data-stu-id="c2ce9-397">**Module name**: @%SystemRoot%\\System32\\mpiocpl.dll,-1000</span></span>
-   <span data-ttu-id="c2ce9-398">此主控台專案只會在伺服器版本的 Windows 中看到。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-398">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="network-and-sharing-center"></a><span data-ttu-id="c2ce9-399">網路和共用中心</span><span class="sxs-lookup"><span data-stu-id="c2ce9-399">Network and Sharing Center</span></span>

-   <span data-ttu-id="c2ce9-400">正式 **名稱**： Microsoft. NetworkAndSharingCenter</span><span class="sxs-lookup"><span data-stu-id="c2ce9-400">**Canonical name**: Microsoft.NetworkAndSharingCenter</span></span>
-   <span data-ttu-id="c2ce9-401">**GUID**： {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-401">**GUID**: {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}</span></span>
-   <span data-ttu-id="c2ce9-402">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-402">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-403">**模組名稱**： @% SystemRoot% \\ System32 \\netcenter.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-403">**Module name**: @%SystemRoot%\\System32\\netcenter.dll,-1</span></span>
-   <span data-ttu-id="c2ce9-404">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-404">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-405">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-405">Page Name</span></span>  | <span data-ttu-id="c2ce9-406">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-406">Opens</span></span>                     |
    |------------|---------------------------|
    | <span data-ttu-id="c2ce9-407">進階</span><span class="sxs-lookup"><span data-stu-id="c2ce9-407">Advanced</span></span>   | <span data-ttu-id="c2ce9-408">Advanced 共用設定</span><span class="sxs-lookup"><span data-stu-id="c2ce9-408">Advanced sharing settings</span></span> |
    | <span data-ttu-id="c2ce9-409">ShareMedia</span><span class="sxs-lookup"><span data-stu-id="c2ce9-409">ShareMedia</span></span> | <span data-ttu-id="c2ce9-410">媒體串流選項</span><span class="sxs-lookup"><span data-stu-id="c2ce9-410">Media streaming options</span></span>   |

    

     

### <a name="notification-area-icons"></a><span data-ttu-id="c2ce9-411">通知區域圖示</span><span class="sxs-lookup"><span data-stu-id="c2ce9-411">Notification Area Icons</span></span>

-   <span data-ttu-id="c2ce9-412">正式 **名稱**： Microsoft. NotificationAreaIcons</span><span class="sxs-lookup"><span data-stu-id="c2ce9-412">**Canonical name**: Microsoft.NotificationAreaIcons</span></span>
-   <span data-ttu-id="c2ce9-413">**GUID**： {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-413">**GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}</span></span>
-   <span data-ttu-id="c2ce9-414">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-414">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-415">**模組名稱**： @% SystemRoot% \\ System32 \\taskbarcpl.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-415">**Module name**: @%SystemRoot%\\System32\\taskbarcpl.dll,-1</span></span>

### <a name="pen-and-touch"></a><span data-ttu-id="c2ce9-416">畫筆和觸控</span><span class="sxs-lookup"><span data-stu-id="c2ce9-416">Pen and Touch</span></span>

-   <span data-ttu-id="c2ce9-417">正式 **名稱**： Microsoft. PenAndTouch</span><span class="sxs-lookup"><span data-stu-id="c2ce9-417">**Canonical name**: Microsoft.PenAndTouch</span></span>
-   <span data-ttu-id="c2ce9-418">**GUID**： {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-418">**GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span>
-   <span data-ttu-id="c2ce9-419">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-419">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-420">**模組名稱**： @% SystemRoot% \\ System32 \\tabletpc.cpl，-10103</span><span class="sxs-lookup"><span data-stu-id="c2ce9-420">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10103</span></span>
-   <span data-ttu-id="c2ce9-421">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-421">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-422">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-422">Page Name</span></span> | <span data-ttu-id="c2ce9-423">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-423">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="c2ce9-424">1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-424">1</span></span>         | <span data-ttu-id="c2ce9-425">筆觸</span><span class="sxs-lookup"><span data-stu-id="c2ce9-425">Flicks</span></span>      |
    | <span data-ttu-id="c2ce9-426">2</span><span class="sxs-lookup"><span data-stu-id="c2ce9-426">2</span></span>         | <span data-ttu-id="c2ce9-427">Handwriting</span><span class="sxs-lookup"><span data-stu-id="c2ce9-427">Handwriting</span></span> |

    

     

### <a name="personalization"></a><span data-ttu-id="c2ce9-428">個人化</span><span class="sxs-lookup"><span data-stu-id="c2ce9-428">Personalization</span></span>

-   <span data-ttu-id="c2ce9-429">正式 **名稱**： Microsoft 個人化</span><span class="sxs-lookup"><span data-stu-id="c2ce9-429">**Canonical name**: Microsoft.Personalization</span></span>
-   <span data-ttu-id="c2ce9-430">**GUID**： {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-430">**GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span></span>
-   <span data-ttu-id="c2ce9-431">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-431">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-432">**模組名稱**： @% SystemRoot% \\ System32 \\themecpl.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-432">**Module name**: @%SystemRoot%\\System32\\themecpl.dll,-1</span></span>
-   <span data-ttu-id="c2ce9-433">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-433">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-434">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-434">Page Name</span></span>        | <span data-ttu-id="c2ce9-435">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-435">Opens</span></span>                |
    |------------------|----------------------|
    | <span data-ttu-id="c2ce9-436">pageColorization</span><span class="sxs-lookup"><span data-stu-id="c2ce9-436">pageColorization</span></span> | <span data-ttu-id="c2ce9-437">色彩和外觀</span><span class="sxs-lookup"><span data-stu-id="c2ce9-437">Color and Appearance</span></span> |
    | <span data-ttu-id="c2ce9-438">pageWallpaper</span><span class="sxs-lookup"><span data-stu-id="c2ce9-438">pageWallpaper</span></span>    | <span data-ttu-id="c2ce9-439">桌面背景</span><span class="sxs-lookup"><span data-stu-id="c2ce9-439">Desktop Background</span></span>   |

    

     

### <a name="phone-and-modem"></a><span data-ttu-id="c2ce9-440">電話和數據機</span><span class="sxs-lookup"><span data-stu-id="c2ce9-440">Phone and Modem</span></span>

-   <span data-ttu-id="c2ce9-441">正式 **名稱**： Microsoft. PhoneAndModem</span><span class="sxs-lookup"><span data-stu-id="c2ce9-441">**Canonical name**: Microsoft.PhoneAndModem</span></span>
-   <span data-ttu-id="c2ce9-442">**GUID**： {40419485-C444-4567-851A-2DD7BFA1684D}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-442">**GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}</span></span>
-   <span data-ttu-id="c2ce9-443">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-443">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-444">**模組名稱**： @% SystemRoot% \\ System32 \\telephon.cpl，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-444">**Module name**: @%SystemRoot%\\System32\\telephon.cpl,-1</span></span>
-   <span data-ttu-id="c2ce9-445">此值啟動的視窗在 Windows 8 之前的 Windows 版本中，標題為「位置資訊」。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-445">The window that this value launches is titled "Location Information" in versions of Windows prior to Windows 8.</span></span> <span data-ttu-id="c2ce9-446">當 Windows 8 時，專案的 UI 會大幅變更。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-446">The item's UI is considerably changed as of Windows 8.</span></span>

### <a name="power-options"></a><span data-ttu-id="c2ce9-447">電源選項</span><span class="sxs-lookup"><span data-stu-id="c2ce9-447">Power Options</span></span>

-   <span data-ttu-id="c2ce9-448">正式 **名稱**： Microsoft. PowerOptions</span><span class="sxs-lookup"><span data-stu-id="c2ce9-448">**Canonical name**: Microsoft.PowerOptions</span></span>
-   <span data-ttu-id="c2ce9-449">**GUID**： {025A5937-A6BE-4686-A844-36FE4BEC8B6D}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-449">**GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}</span></span>
-   <span data-ttu-id="c2ce9-450">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-450">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-451">**模組名稱**： @% SystemRoot% \\ System32 \\powercpl.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-451">**Module name**: @%SystemRoot%\\System32\\powercpl.dll,-1</span></span>
-   <span data-ttu-id="c2ce9-452">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-452">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-453">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-453">Page Name</span></span>          | <span data-ttu-id="c2ce9-454">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-454">Opens</span></span>              |
    |--------------------|--------------------|
    | <span data-ttu-id="c2ce9-455">pageGlobalSettings</span><span class="sxs-lookup"><span data-stu-id="c2ce9-455">pageGlobalSettings</span></span> | <span data-ttu-id="c2ce9-456">系統設定</span><span class="sxs-lookup"><span data-stu-id="c2ce9-456">System Settings</span></span>    |
    | <span data-ttu-id="c2ce9-457">pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="c2ce9-457">pagePlanSettings</span></span>   | <span data-ttu-id="c2ce9-458">編輯計畫設定</span><span class="sxs-lookup"><span data-stu-id="c2ce9-458">Edit Plan Settings</span></span> |

    

     

### <a name="programs-and-features"></a><span data-ttu-id="c2ce9-459">[程式和功能]</span><span class="sxs-lookup"><span data-stu-id="c2ce9-459">Programs and Features</span></span>

-   <span data-ttu-id="c2ce9-460">正式 **名稱**： Microsoft. ProgramsAndFeatures</span><span class="sxs-lookup"><span data-stu-id="c2ce9-460">**Canonical name**: Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="c2ce9-461">**GUID**： {7b81be6a-ce2b-4676-a29e-eb907a5126c5}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-461">**GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}</span></span>
-   <span data-ttu-id="c2ce9-462">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-462">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-463">**模組名稱**： @% systemroot% \\ system32 \\appwiz.cpl，-159</span><span class="sxs-lookup"><span data-stu-id="c2ce9-463">**Module name**: @%systemroot%\\system32\\appwiz.cpl,-159</span></span>
-   <span data-ttu-id="c2ce9-464">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-464">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-465">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-465">Page Name</span></span>                                | <span data-ttu-id="c2ce9-466">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-466">Opens</span></span>             |
    |------------------------------------------|-------------------|
    | <span data-ttu-id="c2ce9-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span></span> | <span data-ttu-id="c2ce9-468">已安裝的更新</span><span class="sxs-lookup"><span data-stu-id="c2ce9-468">Installed Updates</span></span> |

    

     

### <a name="recovery"></a><span data-ttu-id="c2ce9-469">復原</span><span class="sxs-lookup"><span data-stu-id="c2ce9-469">Recovery</span></span>

-   <span data-ttu-id="c2ce9-470">正式 **名稱**： Microsoft. Recovery</span><span class="sxs-lookup"><span data-stu-id="c2ce9-470">**Canonical name**: Microsoft.Recovery</span></span>
-   <span data-ttu-id="c2ce9-471">**GUID**： {9FE63AFD-59CF-4419-9775-ABCC3849F861}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-471">**GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}</span></span>
-   <span data-ttu-id="c2ce9-472">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-472">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-473">**模組名稱**： @% SystemRoot% \\ System32 \\recovery.dll，-101</span><span class="sxs-lookup"><span data-stu-id="c2ce9-473">**Module name**: @%SystemRoot%\\System32\\recovery.dll,-101</span></span>

### <a name="region"></a><span data-ttu-id="c2ce9-474">區域</span><span class="sxs-lookup"><span data-stu-id="c2ce9-474">Region</span></span>

-   <span data-ttu-id="c2ce9-475">正式 **名稱**： Microsoft. RegionAndLanguage</span><span class="sxs-lookup"><span data-stu-id="c2ce9-475">**Canonical name**: Microsoft.RegionAndLanguage</span></span>
-   <span data-ttu-id="c2ce9-476">**GUID**： {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-476">**GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span>
-   <span data-ttu-id="c2ce9-477">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-477">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-478">**模組名稱**： @% SystemRoot% \\ System32 \\intl.cpl，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-478">**Module name**: @%SystemRoot%\\System32\\intl.cpl,-1</span></span>
-   <span data-ttu-id="c2ce9-479">在 Windows 7 中找到的地區和語言專案是依 Windows 8 分割。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-479">The Region and Language item found in Windows 7 was split as of Windows 8.</span></span> <span data-ttu-id="c2ce9-480">RegionAndLanguage 現在會啟動區域專案。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-480">Microsoft.RegionAndLanguage now launches the Region item.</span></span> <span data-ttu-id="c2ce9-481">若要啟動語言專案，請使用 [Microsoft language](#location-settings)。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-481">To launch the Language item, use [Microsoft.Language](#location-settings).</span></span>
-   <span data-ttu-id="c2ce9-482">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-482">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-483">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-483">Page Name</span></span> | <span data-ttu-id="c2ce9-484">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-484">Opens</span></span>          |
    |-----------|----------------|
    | <span data-ttu-id="c2ce9-485">1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-485">1</span></span>         | <span data-ttu-id="c2ce9-486">Location</span><span class="sxs-lookup"><span data-stu-id="c2ce9-486">Location</span></span>       |
    | <span data-ttu-id="c2ce9-487">2</span><span class="sxs-lookup"><span data-stu-id="c2ce9-487">2</span></span>         | <span data-ttu-id="c2ce9-488">系統管理</span><span class="sxs-lookup"><span data-stu-id="c2ce9-488">Administrative</span></span> |

    

     

### <a name="remoteapp-and-desktop-connections"></a><span data-ttu-id="c2ce9-489">RemoteApp 和桌面連線</span><span class="sxs-lookup"><span data-stu-id="c2ce9-489">RemoteApp and Desktop Connections</span></span>

-   <span data-ttu-id="c2ce9-490">正式 **名稱**： Microsoft. RemoteAppAndDesktopConnections</span><span class="sxs-lookup"><span data-stu-id="c2ce9-490">**Canonical name**: Microsoft.RemoteAppAndDesktopConnections</span></span>
-   <span data-ttu-id="c2ce9-491">**GUID**： {241D7C96-F8BF-4F85-B01F-E2B043341A4B}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-491">**GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}</span></span>
-   <span data-ttu-id="c2ce9-492">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-492">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-493">**模組名稱**： @% SystemRoot% \\ System32 \\tsworkspace.dll，-15300</span><span class="sxs-lookup"><span data-stu-id="c2ce9-493">**Module name**: @%SystemRoot%\\System32\\tsworkspace.dll,-15300</span></span>

### <a name="sound"></a><span data-ttu-id="c2ce9-494">音效</span><span class="sxs-lookup"><span data-stu-id="c2ce9-494">Sound</span></span>

-   <span data-ttu-id="c2ce9-495">正式 **名稱**： Microsoft. 音效</span><span class="sxs-lookup"><span data-stu-id="c2ce9-495">**Canonical name**: Microsoft.Sound</span></span>
-   <span data-ttu-id="c2ce9-496">**GUID**： {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-496">**GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span>
-   <span data-ttu-id="c2ce9-497">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-497">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-498">**模組名稱**： @% SystemRoot% \\ System32 \\mmsys.cpl，-300</span><span class="sxs-lookup"><span data-stu-id="c2ce9-498">**Module name**: @%SystemRoot%\\System32\\mmsys.cpl,-300</span></span>

### <a name="speech-recognition"></a><span data-ttu-id="c2ce9-499">語音辨識</span><span class="sxs-lookup"><span data-stu-id="c2ce9-499">Speech Recognition</span></span>

-   <span data-ttu-id="c2ce9-500">正式 **名稱**： Microsoft. SpeechRecognition</span><span class="sxs-lookup"><span data-stu-id="c2ce9-500">**Canonical name**: Microsoft.SpeechRecognition</span></span>
-   <span data-ttu-id="c2ce9-501">**GUID**： {58E3C745-D971-4081-9034-86E34B30836A}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-501">**GUID**: {58E3C745-D971-4081-9034-86E34B30836A}</span></span>
-   <span data-ttu-id="c2ce9-502">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-502">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-503">**模組名稱**： @% SystemRoot% \\ System32 \\ 語音 \\ SpeechUX \\speechuxcpl.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-503">**Module name**: @%SystemRoot%\\System32\\Speech\\SpeechUX\\speechuxcpl.dll,-1</span></span>

### <a name="storage-spaces"></a><span data-ttu-id="c2ce9-504">儲存空間</span><span class="sxs-lookup"><span data-stu-id="c2ce9-504">Storage Spaces</span></span>

-   <span data-ttu-id="c2ce9-505">正式 **名稱**： Microsoft. StorageSpaces</span><span class="sxs-lookup"><span data-stu-id="c2ce9-505">**Canonical name**: Microsoft.StorageSpaces</span></span>
-   <span data-ttu-id="c2ce9-506">**GUID**： {F942C606-0914-47AB-BE56-1321B8035096}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-506">**GUID**: {F942C606-0914-47AB-BE56-1321B8035096}</span></span>
-   <span data-ttu-id="c2ce9-507">**支援的 OS**： Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-507">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-508">**模組名稱**： @C: \\ Windows \\ System32 \\SpaceControl.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-508">**Module name**: @C:\\Windows\\System32\\SpaceControl.dll,-1</span></span>

### <a name="sync-center"></a><span data-ttu-id="c2ce9-509">同步中心</span><span class="sxs-lookup"><span data-stu-id="c2ce9-509">Sync Center</span></span>

-   <span data-ttu-id="c2ce9-510">正式 **名稱**： Microsoft. SyncCenter</span><span class="sxs-lookup"><span data-stu-id="c2ce9-510">**Canonical name**: Microsoft.SyncCenter</span></span>
-   <span data-ttu-id="c2ce9-511">**GUID**： {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-511">**GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}</span></span>
-   <span data-ttu-id="c2ce9-512">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-512">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-513">**模組名稱**： @% SystemRoot% \\ System32 \\SyncCenter.dll，-3000</span><span class="sxs-lookup"><span data-stu-id="c2ce9-513">**Module name**: @%SystemRoot%\\System32\\SyncCenter.dll,-3000</span></span>

### <a name="system"></a><span data-ttu-id="c2ce9-514">系統</span><span class="sxs-lookup"><span data-stu-id="c2ce9-514">System</span></span>

-   <span data-ttu-id="c2ce9-515">正式 **名稱**： Microsoft.System</span><span class="sxs-lookup"><span data-stu-id="c2ce9-515">**Canonical name**: Microsoft.System</span></span>
-   <span data-ttu-id="c2ce9-516">**GUID**： {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-516">**GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span></span>
-   <span data-ttu-id="c2ce9-517">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-517">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-518">**模組名稱**： @% SystemRoot% \\ System32 \\systemcpl.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-518">**Module name**: @%SystemRoot%\\System32\\systemcpl.dll,-1</span></span>

### <a name="tablet-pc-settings"></a><span data-ttu-id="c2ce9-519">Tablet PC 設定</span><span class="sxs-lookup"><span data-stu-id="c2ce9-519">Tablet PC Settings</span></span>

-   <span data-ttu-id="c2ce9-520">正式 **名稱**： Microsoft. TabletPCSettings</span><span class="sxs-lookup"><span data-stu-id="c2ce9-520">**Canonical name**: Microsoft.TabletPCSettings</span></span>
-   <span data-ttu-id="c2ce9-521">**GUID**： {80F3F1D5-FECA-45F3-BC32-752C152E456E}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-521">**GUID**: {80F3F1D5-FECA-45F3-BC32-752C152E456E}</span></span>
-   <span data-ttu-id="c2ce9-522">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-522">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-523">**模組名稱**： @% SystemRoot% \\ System32 \\tabletpc.cpl，-10100</span><span class="sxs-lookup"><span data-stu-id="c2ce9-523">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10100</span></span>

### <a name="taskbar-and-navigation"></a><span data-ttu-id="c2ce9-524">工作列和流覽</span><span class="sxs-lookup"><span data-stu-id="c2ce9-524">Taskbar and Navigation</span></span>

-   <span data-ttu-id="c2ce9-525">正式 **名稱**： Microsoft. 工作列</span><span class="sxs-lookup"><span data-stu-id="c2ce9-525">**Canonical name**: Microsoft.Taskbar</span></span>
-   <span data-ttu-id="c2ce9-526">**GUID**： {0DF44EAA-FF21-4412-828E-260A8728E7F1}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-526">**GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span>
-   <span data-ttu-id="c2ce9-527">**支援的 OS**： Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-527">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-528">**模組名稱**： @% SystemRoot% \\ system32 \\shell32.dll，-32517</span><span class="sxs-lookup"><span data-stu-id="c2ce9-528">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-32517</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="c2ce9-529">疑難排解</span><span class="sxs-lookup"><span data-stu-id="c2ce9-529">Troubleshooting</span></span>

-   <span data-ttu-id="c2ce9-530">正式 **名稱**： Microsoft. 疑難排解</span><span class="sxs-lookup"><span data-stu-id="c2ce9-530">**Canonical name**: Microsoft.Troubleshooting</span></span>
-   <span data-ttu-id="c2ce9-531">**GUID**： {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-531">**GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span></span>
-   <span data-ttu-id="c2ce9-532">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-532">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-533">**模組名稱**： @% SystemRoot% \\ System32 \\DiagCpl.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-533">**Module name**: @%SystemRoot%\\System32\\DiagCpl.dll,-1</span></span>
-   <span data-ttu-id="c2ce9-534">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-534">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-535">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-535">Page Name</span></span>   | <span data-ttu-id="c2ce9-536">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-536">Opens</span></span>   |
    |-------------|---------|
    | <span data-ttu-id="c2ce9-537">HistoryPage</span><span class="sxs-lookup"><span data-stu-id="c2ce9-537">HistoryPage</span></span> | <span data-ttu-id="c2ce9-538">記錄</span><span class="sxs-lookup"><span data-stu-id="c2ce9-538">History</span></span> |

    

     

### <a name="tsappinstall"></a><span data-ttu-id="c2ce9-539">TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="c2ce9-539">TSAppInstall</span></span>

-   <span data-ttu-id="c2ce9-540">正式 **名稱**： Microsoft. TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="c2ce9-540">**Canonical name**: Microsoft.TSAppInstall</span></span>
-   <span data-ttu-id="c2ce9-541">**GUID**： {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-541">**GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}</span></span>
-   <span data-ttu-id="c2ce9-542">**支援的作業系統**： Windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-542">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-543">**模組名稱**： @% systemroot% \\ system32 \\tsappinstall.exe，-2001</span><span class="sxs-lookup"><span data-stu-id="c2ce9-543">**Module name**: @%systemroot%\\system32\\tsappinstall.exe,-2001</span></span>

### <a name="user-accounts"></a><span data-ttu-id="c2ce9-544">使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="c2ce9-544">User Accounts</span></span>

-   <span data-ttu-id="c2ce9-545">正式 **名稱**： Microsoft. UserAccounts</span><span class="sxs-lookup"><span data-stu-id="c2ce9-545">**Canonical name**: Microsoft.UserAccounts</span></span>
-   <span data-ttu-id="c2ce9-546">**GUID**： {60632754-c523-4b62-b45c-4172da012619}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-546">**GUID**: {60632754-c523-4b62-b45c-4172da012619}</span></span>
-   <span data-ttu-id="c2ce9-547">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-547">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-548">**模組名稱**： @% SystemRoot% \\ System32 \\usercpl.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-548">**Module name**: @%SystemRoot%\\System32\\usercpl.dll,-1</span></span>

### <a name="windows-anytime-upgrade"></a><span data-ttu-id="c2ce9-549">Windows Anytime Upgrade</span><span class="sxs-lookup"><span data-stu-id="c2ce9-549">Windows Anytime Upgrade</span></span>

-   <span data-ttu-id="c2ce9-550">正式 **名稱**： Microsoft. WindowsAnytimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="c2ce9-550">**Canonical name**: Microsoft.WindowsAnytimeUpgrade</span></span>
-   <span data-ttu-id="c2ce9-551">**GUID**： {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-551">**GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}</span></span>
-   <span data-ttu-id="c2ce9-552">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-552">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-553">**模組名稱**： @ $ (resourceString。 \_SYS \_ MOD \_ 路徑) ，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-553">**Module name**: @$(resourceString.\_SYS\_MOD\_PATH),-1</span></span>

### <a name="windows-defender"></a><span data-ttu-id="c2ce9-554">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="c2ce9-554">Windows Defender</span></span>

-   <span data-ttu-id="c2ce9-555">正式 **名稱**： Microsoft. windowsdefender.msi</span><span class="sxs-lookup"><span data-stu-id="c2ce9-555">**Canonical name**: Microsoft.WindowsDefender</span></span>
-   <span data-ttu-id="c2ce9-556">**GUID**： {D8559EB9-20C0-410E-BEDA-7ED416AECC2A}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-556">**GUID**: {D8559EB9-20C0-410E-BEDA-7ED416AECC2A}</span></span>
-   <span data-ttu-id="c2ce9-557">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-557">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-558">**模組名稱**： @% ProgramFiles% \\ Windows Defender \\MsMpRes.dll，-104</span><span class="sxs-lookup"><span data-stu-id="c2ce9-558">**Module name**: @%ProgramFiles%\\Windows Defender\\MsMpRes.dll,-104</span></span>

### <a name="windows-firewall"></a><span data-ttu-id="c2ce9-559">Windows 防火牆</span><span class="sxs-lookup"><span data-stu-id="c2ce9-559">Windows Firewall</span></span>

-   <span data-ttu-id="c2ce9-560">正式 **名稱**： Microsoft. windows 防火牆</span><span class="sxs-lookup"><span data-stu-id="c2ce9-560">**Canonical name**: Microsoft.WindowsFirewall</span></span>
-   <span data-ttu-id="c2ce9-561">**GUID**： {4026492F-2F69-46B8-B9BF-5654FC07E423}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-561">**GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}</span></span>
-   <span data-ttu-id="c2ce9-562">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-562">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-563">**模組名稱**： @C: \\ Windows \\ system32 \\FirewallControlPanel.dll、-12122</span><span class="sxs-lookup"><span data-stu-id="c2ce9-563">**Module name**: @C:\\Windows\\system32\\FirewallControlPanel.dll,-12122</span></span>
-   <span data-ttu-id="c2ce9-564">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-564">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-565">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-565">Page Name</span></span>         | <span data-ttu-id="c2ce9-566">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-566">Opens</span></span>        |
    |-------------------|--------------|
    | <span data-ttu-id="c2ce9-567">pageConfigureApps</span><span class="sxs-lookup"><span data-stu-id="c2ce9-567">pageConfigureApps</span></span> | <span data-ttu-id="c2ce9-568">允許的應用程式</span><span class="sxs-lookup"><span data-stu-id="c2ce9-568">Allowed apps</span></span> |

    

     

### <a name="windows-mobility-center"></a><span data-ttu-id="c2ce9-569">Windows 行動中心</span><span class="sxs-lookup"><span data-stu-id="c2ce9-569">Windows Mobility Center</span></span>

-   <span data-ttu-id="c2ce9-570">正式 **名稱**： Microsoft. MobilityCenter</span><span class="sxs-lookup"><span data-stu-id="c2ce9-570">**Canonical name**: Microsoft.MobilityCenter</span></span>
-   <span data-ttu-id="c2ce9-571">**GUID**： {5ea4f148-308c-46d7-98a9-49041b1dd468}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-571">**GUID**: {5ea4f148-308c-46d7-98a9-49041b1dd468}</span></span>
-   <span data-ttu-id="c2ce9-572">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-572">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-573">**模組名稱**： @% SystemRoot% \\ system32 \\mblctr.exe，-1002</span><span class="sxs-lookup"><span data-stu-id="c2ce9-573">**Module name**: @%SystemRoot%\\system32\\mblctr.exe,-1002</span></span>

### <a name="windows-to-go"></a><span data-ttu-id="c2ce9-574">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="c2ce9-574">Windows To Go</span></span>

-   <span data-ttu-id="c2ce9-575">正式 **名稱**： Microsoft. PortableWorkspaceCreator</span><span class="sxs-lookup"><span data-stu-id="c2ce9-575">**Canonical name**: Microsoft.PortableWorkspaceCreator</span></span>
-   <span data-ttu-id="c2ce9-576">**GUID**： {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-576">**GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}</span></span>
-   <span data-ttu-id="c2ce9-577">**支援的 OS**： Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-577">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-578">**模組名稱**： @% SystemRoot% \\ System32 \\pwcreator.exe，-151</span><span class="sxs-lookup"><span data-stu-id="c2ce9-578">**Module name**: @%SystemRoot%\\System32\\pwcreator.exe,-151</span></span>

### <a name="windows-update"></a><span data-ttu-id="c2ce9-579">Windows Update</span><span class="sxs-lookup"><span data-stu-id="c2ce9-579">Windows Update</span></span>

-   <span data-ttu-id="c2ce9-580">正式 **名稱**： Microsoft. windowsupdate.log</span><span class="sxs-lookup"><span data-stu-id="c2ce9-580">**Canonical name**: Microsoft.WindowsUpdate</span></span>
-   <span data-ttu-id="c2ce9-581">**GUID**： {36eef7db-88ad-4e81-ad49-0e313f0c35f8}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-581">**GUID**: {36eef7db-88ad-4e81-ad49-0e313f0c35f8}</span></span>
-   <span data-ttu-id="c2ce9-582">**支援的作業系統**： windows Vista、windows 7、Windows 8、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-582">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-583">**模組名稱**： @% SystemRoot% \\ system32 \\wucltux.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-583">**Module name**: @%SystemRoot%\\system32\\wucltux.dll,-1</span></span>
-   <span data-ttu-id="c2ce9-584">**頁面**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-584">**Pages**</span></span>

    | <span data-ttu-id="c2ce9-585">頁面名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-585">Page Name</span></span>         | <span data-ttu-id="c2ce9-586">開啟</span><span class="sxs-lookup"><span data-stu-id="c2ce9-586">Opens</span></span>               |
    |-------------------|---------------------|
    | <span data-ttu-id="c2ce9-587">pageSettings</span><span class="sxs-lookup"><span data-stu-id="c2ce9-587">pageSettings</span></span>      | <span data-ttu-id="c2ce9-588">變更設定</span><span class="sxs-lookup"><span data-stu-id="c2ce9-588">Change settings</span></span>     |
    | <span data-ttu-id="c2ce9-589">pageUpdateHistory</span><span class="sxs-lookup"><span data-stu-id="c2ce9-589">pageUpdateHistory</span></span> | <span data-ttu-id="c2ce9-590">查看更新歷程記錄</span><span class="sxs-lookup"><span data-stu-id="c2ce9-590">View update history</span></span> |

    

     

### <a name="work-folders"></a><span data-ttu-id="c2ce9-591">工作資料夾</span><span class="sxs-lookup"><span data-stu-id="c2ce9-591">Work Folders</span></span>

-   <span data-ttu-id="c2ce9-592">正式 **名稱**： Microsoft. workfolders.domainname</span><span class="sxs-lookup"><span data-stu-id="c2ce9-592">**Canonical name**: Microsoft.WorkFolders</span></span>
-   <span data-ttu-id="c2ce9-593">**GUID**： {ECDB0924-4208-451E-8EE0-373C0956DE16}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-593">**GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}</span></span>
-   <span data-ttu-id="c2ce9-594">**支援的 OS**： Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-594">**Supported OS**: Windows 8.1</span></span>
-   <span data-ttu-id="c2ce9-595">**模組名稱**： @C: \\ Windows \\ System32 \\WorkfoldersControl.dll，-1</span><span class="sxs-lookup"><span data-stu-id="c2ce9-595">**Module name**: @C:\\Windows\\System32\\WorkfoldersControl.dll,-1</span></span>

## <a name="deprecated-control-panel-canonical-names"></a><span data-ttu-id="c2ce9-596">已淘汰主控台正式名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-596">Deprecated Control Panel Canonical Names</span></span>

<span data-ttu-id="c2ce9-597">以下是 Windows 8.1 或更新版本不再使用的標準名稱。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-597">The following are canonical names that are no longer in use as of Windows 8.1 or later.</span></span> <span data-ttu-id="c2ce9-598">部分已完全移除。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-598">Some have been removed altogether.</span></span> <span data-ttu-id="c2ce9-599">在這些情況下，其他專案已重新對應：</span><span class="sxs-lookup"><span data-stu-id="c2ce9-599">Others have been remapped in these situations:</span></span>

-   <span data-ttu-id="c2ce9-600">主控台專案已重新命名。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-600">A Control Panel item is renamed.</span></span> <span data-ttu-id="c2ce9-601">重新命名的專案會獲得新的正式名稱，但會保留相同的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-601">The renamed item is given a new canonical name but keeps the same GUID.</span></span> <span data-ttu-id="c2ce9-602">在此情況下，舊的正式名稱會啟動重新命名的主控台專案。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-602">In this case, the old canonical name launches the renamed Control Panel item.</span></span> <span data-ttu-id="c2ce9-603">請注意，啟動的專案可能不會使用與該專案較舊版本相同的 UI。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-603">Be aware that the item that's launched might not use the same UI as that item's older version.</span></span>
-   <span data-ttu-id="c2ce9-604">一或多個主控台專案的功能會移動或合併到新的專案中。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-604">The functionality of one or more Control Panel items is moved or consolidated into a new item.</span></span> <span data-ttu-id="c2ce9-605">在此情況下，舊的正式名稱會對應至最適當的新主控台專案。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-605">In this case, the old canonical name maps to the most appropriate new Control Panel item.</span></span>

> [!Note]  
> <span data-ttu-id="c2ce9-606">重新對應存在以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-606">Remappings exist for backward compatibility.</span></span> <span data-ttu-id="c2ce9-607">您不應該在新的程式碼中使用已被取代的值。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-607">You should not use deprecated values in new code.</span></span>

 



| <span data-ttu-id="c2ce9-608">已淘汰的正式名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-608">Deprecated canonical name</span></span>                                   | <span data-ttu-id="c2ce9-609">主控台專案</span><span class="sxs-lookup"><span data-stu-id="c2ce9-609">Control Panel Item</span></span>                | <span data-ttu-id="c2ce9-610">GUID</span><span class="sxs-lookup"><span data-stu-id="c2ce9-610">GUID</span></span>                                   | <span data-ttu-id="c2ce9-611">備註</span><span class="sxs-lookup"><span data-stu-id="c2ce9-611">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ce9-612">AddHardware</span><span class="sxs-lookup"><span data-stu-id="c2ce9-612">Microsoft.AddHardware</span></span>                                       | <span data-ttu-id="c2ce9-613">新增硬體</span><span class="sxs-lookup"><span data-stu-id="c2ce9-613">Add Hardware</span></span>                      | <span data-ttu-id="c2ce9-614">{7A979262-40CE-46ff-AEEE-7884AC3B6136}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-614">{7A979262-40CE-46ff-AEEE-7884AC3B6136}</span></span> | <span data-ttu-id="c2ce9-615">與 Windows 7 的 [DevicesAndPrinters](#devices-and-printers) 對應。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-615">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="c2ce9-616">AudioDevicesAndSoundThemes</span><span class="sxs-lookup"><span data-stu-id="c2ce9-616">Microsoft.AudioDevicesAndSoundThemes</span></span>                        | <span data-ttu-id="c2ce9-617">音效</span><span class="sxs-lookup"><span data-stu-id="c2ce9-617">Sound</span></span>                             | <span data-ttu-id="c2ce9-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span> | <span data-ttu-id="c2ce9-619">對應至 Windows 7 的 [Microsoft 音效](#sound) 。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-619">Maps to [Microsoft.Sound](#sound) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c2ce9-620">BackupAndRestoreCenter/Microsoft. BackupAndRestore</span><span class="sxs-lookup"><span data-stu-id="c2ce9-620">Microsoft.BackupAndRestoreCenter/Microsoft.BackupAndRestore</span></span> | <span data-ttu-id="c2ce9-621">備份及還原中心</span><span class="sxs-lookup"><span data-stu-id="c2ce9-621">Backup and Restore Center</span></span>         | <span data-ttu-id="c2ce9-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span></span> | <span data-ttu-id="c2ce9-623">BackupAndRestoreCenter 對應至 Windows 7 的 BackupAndRestore。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-623">Microsoft.BackupAndRestoreCenter maps to Microsoft.BackupAndRestore in Windows 7.</span></span> <span data-ttu-id="c2ce9-624">從 Windows 8 移除兩者;請改用 [FileHistory](#file-history) 。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-624">Both are removed as of Windows 8; use [Microsoft.FileHistory](#file-history) instead.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="c2ce9-625">Microsoft CardSpace</span><span class="sxs-lookup"><span data-stu-id="c2ce9-625">Microsoft.CardSpace</span></span>                                         | <span data-ttu-id="c2ce9-626">Windows CardSpace</span><span class="sxs-lookup"><span data-stu-id="c2ce9-626">Windows CardSpace</span></span>                 | <span data-ttu-id="c2ce9-627">{78CB147A-98EA-4AA6-B0DF-C8681F69341C}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-627">{78CB147A-98EA-4AA6-B0DF-C8681F69341C}</span></span> | <span data-ttu-id="c2ce9-628">從 Windows 8 移除。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-628">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c2ce9-629">DesktopGadgets</span><span class="sxs-lookup"><span data-stu-id="c2ce9-629">Microsoft.DesktopGadgets</span></span>                                    | <span data-ttu-id="c2ce9-630">桌面小工具</span><span class="sxs-lookup"><span data-stu-id="c2ce9-630">Desktop Gadgets</span></span>                   | <span data-ttu-id="c2ce9-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="c2ce9-632">從 Windows 8 移除。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-632">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c2ce9-633">GetProgramsOnline</span><span class="sxs-lookup"><span data-stu-id="c2ce9-633">Microsoft.GetProgramsOnline</span></span>                                 | <span data-ttu-id="c2ce9-634">Windows 交易市集</span><span class="sxs-lookup"><span data-stu-id="c2ce9-634">Windows Marketplace</span></span>               | <span data-ttu-id="c2ce9-635">{3e7efb4c-faf1-453d-89eb-56026875ef90}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-635">{3e7efb4c-faf1-453d-89eb-56026875ef90}</span></span> | <span data-ttu-id="c2ce9-636">從 Windows 7 移除。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-636">Removed as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c2ce9-637">InfraredOptions</span><span class="sxs-lookup"><span data-stu-id="c2ce9-637">Microsoft.InfraredOptions</span></span>                                   | <span data-ttu-id="c2ce9-638">紅外線</span><span class="sxs-lookup"><span data-stu-id="c2ce9-638">Infrared</span></span>                          | <span data-ttu-id="c2ce9-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span> | <span data-ttu-id="c2ce9-640">對應至 Windows 7 的 [Microsoft 紅外線](#infrared) 。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-640">Maps to [Microsoft.Infrared](#infrared) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c2ce9-641">Microsoft. Language</span><span class="sxs-lookup"><span data-stu-id="c2ce9-641">Microsoft.Language</span></span>                                          | <span data-ttu-id="c2ce9-642">語言</span><span class="sxs-lookup"><span data-stu-id="c2ce9-642">Language</span></span>                          | <span data-ttu-id="c2ce9-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span></span> | <span data-ttu-id="c2ce9-644">從 Windows 10 1803 版移除</span><span class="sxs-lookup"><span data-stu-id="c2ce9-644">Removed as of Windows 10, version 1803</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="c2ce9-645">LocationAndOtherSensors</span><span class="sxs-lookup"><span data-stu-id="c2ce9-645">Microsoft.LocationAndOtherSensors</span></span>                           | <span data-ttu-id="c2ce9-646">定位和其他感應器</span><span class="sxs-lookup"><span data-stu-id="c2ce9-646">Location and Other Sensors</span></span>        | <span data-ttu-id="c2ce9-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span></span> | <span data-ttu-id="c2ce9-648">從 Windows 8 對應至 [LocationSettings](#infrared) 。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-648">Maps to [Microsoft.LocationSettings](#infrared) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c2ce9-649">PenAndInputDevices</span><span class="sxs-lookup"><span data-stu-id="c2ce9-649">Microsoft.PenAndInputDevices</span></span>                                | <span data-ttu-id="c2ce9-650">畫筆和輸入裝置</span><span class="sxs-lookup"><span data-stu-id="c2ce9-650">Pen and Input Devices</span></span>             | <span data-ttu-id="c2ce9-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span> | <span data-ttu-id="c2ce9-652">與 Windows 7 的 [PenAndTouch](#pen-and-touch) 對應。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-652">Maps to [Microsoft.PenAndTouch](#pen-and-touch) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c2ce9-653">PeopleNearMe</span><span class="sxs-lookup"><span data-stu-id="c2ce9-653">Microsoft.PeopleNearMe</span></span>                                      | <span data-ttu-id="c2ce9-654">近端分享</span><span class="sxs-lookup"><span data-stu-id="c2ce9-654">People Near Me</span></span>                    | <span data-ttu-id="c2ce9-655">{5224F545-A443-4859-BA23-7B5A95BDC8EF}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-655">{5224F545-A443-4859-BA23-7B5A95BDC8EF}</span></span> | <span data-ttu-id="c2ce9-656">從 Windows 8 移除。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-656">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c2ce9-657">PerformanceInformationAndTools</span><span class="sxs-lookup"><span data-stu-id="c2ce9-657">Microsoft.PerformanceInformationAndTools</span></span>                    | <span data-ttu-id="c2ce9-658">效能資訊和工具</span><span class="sxs-lookup"><span data-stu-id="c2ce9-658">Performance Information and Tools</span></span> | <span data-ttu-id="c2ce9-659">{78F3955E-3B90-4184-BD14-5397C15F1EFC}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-659">{78F3955E-3B90-4184-BD14-5397C15F1EFC}</span></span> | <span data-ttu-id="c2ce9-660">從 Windows 8.1 移除。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-660">Removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="c2ce9-661">PhoneAndModemOptions</span><span class="sxs-lookup"><span data-stu-id="c2ce9-661">Microsoft.PhoneAndModemOptions</span></span>                              | <span data-ttu-id="c2ce9-662">電話和數據機</span><span class="sxs-lookup"><span data-stu-id="c2ce9-662">Phone and Modem</span></span>                   | <span data-ttu-id="c2ce9-663">{40419485-C444-4567-851A-2DD7BFA1684D}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-663">{40419485-C444-4567-851A-2DD7BFA1684D}</span></span> | <span data-ttu-id="c2ce9-664">與 Windows 7 的 [PhoneAndModem](#phone-and-modem) 對應。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-664">Maps to [Microsoft.PhoneAndModem](#phone-and-modem) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c2ce9-665">Microsoft 印表機</span><span class="sxs-lookup"><span data-stu-id="c2ce9-665">Microsoft.Printers</span></span>                                          | <span data-ttu-id="c2ce9-666">印表機</span><span class="sxs-lookup"><span data-stu-id="c2ce9-666">Printers</span></span>                          | <span data-ttu-id="c2ce9-667">{2227A280-3AEA-1069-A2DE-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-667">{2227A280-3AEA-1069-A2DE-08002B30309D}</span></span> | <span data-ttu-id="c2ce9-668">與 Windows 7 的 [DevicesAndPrinters](#devices-and-printers) 對應。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-668">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="c2ce9-669">ProblemReportsAndSolutions</span><span class="sxs-lookup"><span data-stu-id="c2ce9-669">Microsoft.ProblemReportsAndSolutions</span></span>                        | <span data-ttu-id="c2ce9-670">問題報告與解決方案</span><span class="sxs-lookup"><span data-stu-id="c2ce9-670">Problem Reports and Solutions</span></span>     | <span data-ttu-id="c2ce9-671">{FCFEECAE-EE1B-4849-AE50-685DCF7717EC}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-671">{FCFEECAE-EE1B-4849-AE50-685DCF7717EC}</span></span> | <span data-ttu-id="c2ce9-672">與 Windows 7 的 [ActionCenter](#action-center) 對應。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-672">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="c2ce9-673">RegionalAndLanguageOptions</span><span class="sxs-lookup"><span data-stu-id="c2ce9-673">Microsoft.RegionalAndLanguageOptions</span></span>                        | <span data-ttu-id="c2ce9-674">地區及語言選項</span><span class="sxs-lookup"><span data-stu-id="c2ce9-674">Regional and Language Options</span></span>     | <span data-ttu-id="c2ce9-675">{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-675">{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span> | <span data-ttu-id="c2ce9-676">與 Windows 7 的 [RegionAndLanguage](#region) 對應。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-676">Maps to [Microsoft.RegionAndLanguage](#region) as of Windows 7.</span></span> <span data-ttu-id="c2ce9-677">請注意，從 Windows 8，區域和語言都有各自的主控台專案。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-677">Note that as of Windows 8, Region and Language were each given their own Control Panel item.</span></span> <span data-ttu-id="c2ce9-678">RegionalAndLanguageOptions 和 Microsoft RegionAndLanguage 目前都會開啟區域專案。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-678">Both Microsoft.RegionalAndLanguageOptions and Microsoft.RegionAndLanguage currently open the Region item.</span></span> <span data-ttu-id="c2ce9-679">您必須使用 [Microsoft 語言](#location-settings) 來存取語言專案。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-679">You must use [Microsoft.Language](#location-settings) to access the Language item.</span></span> |
| <span data-ttu-id="c2ce9-680">SecurityCenter</span><span class="sxs-lookup"><span data-stu-id="c2ce9-680">Microsoft.SecurityCenter</span></span>                                    | <span data-ttu-id="c2ce9-681">Windows 資訊安全中心</span><span class="sxs-lookup"><span data-stu-id="c2ce9-681">Windows Security Center</span></span>           | <span data-ttu-id="c2ce9-682">{087DA31B-0DD3-4537-8E23-64A18591F88B}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-682">{087DA31B-0DD3-4537-8E23-64A18591F88B}</span></span> | <span data-ttu-id="c2ce9-683">與 Windows 7 的 [ActionCenter](#action-center) 對應。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-683">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="c2ce9-684">SpeechRecognitionOptions</span><span class="sxs-lookup"><span data-stu-id="c2ce9-684">Microsoft.SpeechRecognitionOptions</span></span>                          | <span data-ttu-id="c2ce9-685">語音辨識選項</span><span class="sxs-lookup"><span data-stu-id="c2ce9-685">Speech Recognition Options</span></span>        | <span data-ttu-id="c2ce9-686">{58E3C745-D971-4081-9034-86E34B30836A}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-686">{58E3C745-D971-4081-9034-86E34B30836A}</span></span> | <span data-ttu-id="c2ce9-687">與 Windows 7 的 [SpeechRecognition](#speech-recognition) 對應。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-687">Maps to [Microsoft.SpeechRecognition](#speech-recognition) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="c2ce9-688">TaskbarAndStartMenu</span><span class="sxs-lookup"><span data-stu-id="c2ce9-688">Microsoft.TaskbarAndStartMenu</span></span>                               | <span data-ttu-id="c2ce9-689">工作列和 [開始] 功能表</span><span class="sxs-lookup"><span data-stu-id="c2ce9-689">Taskbar and Start Menu</span></span>            | <span data-ttu-id="c2ce9-690">{0DF44EAA-FF21-4412-828E-260A8728E7F1}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-690">{0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span> | <span data-ttu-id="c2ce9-691">從 Windows 8 對應到 [Microsoft 的工作列](#speech-recognition) 。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-691">Maps to [Microsoft.Taskbar](#speech-recognition) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="c2ce9-692">WelcomeCenter</span><span class="sxs-lookup"><span data-stu-id="c2ce9-692">Microsoft.WelcomeCenter</span></span>                                     | <span data-ttu-id="c2ce9-693">迎賓中心</span><span class="sxs-lookup"><span data-stu-id="c2ce9-693">Welcome Center</span></span>                    | <span data-ttu-id="c2ce9-694">{CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-694">{CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1}</span></span> | <span data-ttu-id="c2ce9-695">對應至 Windows 7 中的 GettingStarted。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-695">Maps to Microsoft.GettingStarted in Windows 7.</span></span> <span data-ttu-id="c2ce9-696">從 Windows 8 啟動主控台首頁。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-696">Launches the Control Panel home page as of Windows 8.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c2ce9-697">WindowsSidebarProperties</span><span class="sxs-lookup"><span data-stu-id="c2ce9-697">Microsoft.WindowsSidebarProperties</span></span>                          | <span data-ttu-id="c2ce9-698">Windows 提要欄位屬性</span><span class="sxs-lookup"><span data-stu-id="c2ce9-698">Windows Sidebar Properties</span></span>        | <span data-ttu-id="c2ce9-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="c2ce9-700">對應至 Windows 7 中的 DesktopGadgets。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-700">Maps to Microsoft.DesktopGadgets in Windows 7.</span></span> <span data-ttu-id="c2ce9-701">從 Windows 8 移除。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-701">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c2ce9-702">WindowsSideShow</span><span class="sxs-lookup"><span data-stu-id="c2ce9-702">Microsoft.WindowsSideShow</span></span>                                   | <span data-ttu-id="c2ce9-703">Windows SideShow</span><span class="sxs-lookup"><span data-stu-id="c2ce9-703">Windows SideShow</span></span>                  | <span data-ttu-id="c2ce9-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span><span class="sxs-lookup"><span data-stu-id="c2ce9-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span></span> | <span data-ttu-id="c2ce9-705">Windows 8 中已淘汰的功能，已從 Windows 8.1 移除。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-705">Feature deprecated in Windows 8, removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a><span data-ttu-id="c2ce9-706">使用本機群組原則中的正式名稱</span><span class="sxs-lookup"><span data-stu-id="c2ce9-706">Using Canonical Names in Local Group Policy</span></span>

<span data-ttu-id="c2ce9-707">從 Windows 7，您可以使用標準名稱，透過群組原則來限制對個別主控台專案的存取。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-707">As of Windows 7, you can use canonical names to restrict access to individual Control Panel items through group policy.</span></span> <span data-ttu-id="c2ce9-708">這相同的程式可以在 Windows Vista 中使用，但您必須使用模組名稱，而不是正式名稱。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-708">This same procedure can be used in Windows Vista, but you have to use the module name instead of the canonical name.</span></span>

### <a name="hiding-individual-control-panel-items"></a><span data-ttu-id="c2ce9-709">隱藏個別主控台專案</span><span class="sxs-lookup"><span data-stu-id="c2ce9-709">Hiding individual Control Panel items</span></span>

<span data-ttu-id="c2ce9-710">如果您想要顯示比您想要隱藏更多主控台專案，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-710">Use this method if you want to show more Control Panel items than you want to hide.</span></span>

1.  <span data-ttu-id="c2ce9-711">執行 Gpedit.msc 檔案以啟動本機群組原則編輯器。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-711">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="c2ce9-712">您也可以在 Windows 8.1 開始畫面中輸入「群組原則」，然後從搜尋結果中選取 [ **編輯群組原則** ]。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-712">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="c2ce9-713">選取 [**使用者** 設定]  >  **系統管理範本**  >  **主控台**。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-713">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="c2ce9-714">選取 [ **隱藏指定的主控台專案**]。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-714">Select **Hide specified Control Panel items**.</span></span>
4.  <span data-ttu-id="c2ce9-715">在 [ **隱藏開啟的指定主控台專案** ] 視窗中，按一下 [ **已啟用**]。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-715">In the **Hide Specified Control Panel Items** window that opens, click **Enabled**.</span></span>
5.  <span data-ttu-id="c2ce9-716">按一下 [選項] 面板中的 [ **顯示** ] 按鈕，以顯示不允許的主控台專案清單。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-716">Click the **Show** button in the Options panel to show the list of disallowed Control Panel items.</span></span>
6.  <span data-ttu-id="c2ce9-717">在開啟的 [ **顯示內容** ] 視窗中，于 [ **值** ] 資料行中輸入正式名稱。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-717">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="c2ce9-718">請依需要重複步驟。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-718">Repeat as necessary.</span></span>
7.  <span data-ttu-id="c2ce9-719">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-719">Click **OK**.</span></span>

### <a name="showing-individual-control-panel-items"></a><span data-ttu-id="c2ce9-720">顯示個別主控台專案</span><span class="sxs-lookup"><span data-stu-id="c2ce9-720">Showing individual Control Panel items</span></span>

<span data-ttu-id="c2ce9-721">如果您想要隱藏超過您要顯示的主控台專案，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-721">Use this method if you want to hide more Control Panel items than you want to show.</span></span>

1.  <span data-ttu-id="c2ce9-722">執行 Gpedit.msc 檔案以啟動本機群組原則編輯器。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-722">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="c2ce9-723">您也可以在 Windows 8.1 開始畫面中輸入「群組原則」，然後從搜尋結果中選取 [ **編輯群組原則** ]。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-723">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="c2ce9-724">選取 [**使用者** 設定]  >  **系統管理範本**  >  **主控台**。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-724">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="c2ce9-725">選取 [ **只顯示指定的主控台專案**]。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-725">Select **Show only specified Control Panel items**.</span></span>
4.  <span data-ttu-id="c2ce9-726">在 [ **只顯示開啟的指定主控台專案** ] 視窗中，按一下 [ **已啟用**]。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-726">In the **Show Only Specified Control Panel Items** window that opens, click **Enabled**.</span></span> <span data-ttu-id="c2ce9-727">這會隱藏主控台中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-727">This hides everything in the Control Panel.</span></span>
5.  <span data-ttu-id="c2ce9-728">按一下 [選項] 面板中的 [ **顯示** ] 按鈕，以顯示允許的主控台專案清單。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-728">Click the **Show** button in the Options panel to show the list of allowed Control Panel items.</span></span>
6.  <span data-ttu-id="c2ce9-729">在開啟的 [ **顯示內容** ] 視窗中，于 [ **值** ] 資料行中輸入正式名稱。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-729">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="c2ce9-730">請依需要重複步驟。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-730">Repeat as necessary.</span></span>
7.  <span data-ttu-id="c2ce9-731">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-731">Click **OK**.</span></span>

<span data-ttu-id="c2ce9-732">如果您想要移除已新增至顯示或隱藏主控台專案清單中的所有專案，請返回步驟4中的畫面，然後選取 [ **未設定** ] 以清除清單。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-732">If you want to remove all of the entries that you've added to a Show or Hide Control Panel items list, return to the screen in step 4 and select **Not Configured** to clear the list.</span></span> <span data-ttu-id="c2ce9-733">如果您想要保留您的專案，但要暫止限制，請選取 [ **停用**]。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-733">If you want to retain your entries but suspend the restrictions, select **Disabled**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2ce9-734">備註</span><span class="sxs-lookup"><span data-stu-id="c2ce9-734">Remarks</span></span>

<span data-ttu-id="c2ce9-735">您可能會在主控台中看到未列在其中的專案。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-735">You might see items in your Control Panel that are not listed here.</span></span> <span data-ttu-id="c2ce9-736">這些專案不是 Windows 的一部分，而是在安裝各種軟體和硬體（例如 Microsoft Office 或視訊卡）期間新增。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-736">Those items are not part of Windows, but instead are added during the installation of various software and hardware, such as Microsoft Office or a video card.</span></span> <span data-ttu-id="c2ce9-737">非 Windows 主控台專案不一定會有正式名稱。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-737">Non-Windows Control Panel items may or may not have a canonical name.</span></span> <span data-ttu-id="c2ce9-738">若要找出此處未列出的主控台專案的正式名稱，請在下列路徑中查看登錄：</span><span class="sxs-lookup"><span data-stu-id="c2ce9-738">To find the canonical name of a Control Panel item not listed here, look in the registry under these paths:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

<span data-ttu-id="c2ce9-739">如需可協助您探索必要 Clsid 的詳細資訊，請參閱 [如何註冊可執行檔主控台專案](how-to-register-an-executable-control-panel-item-registration-.md) ，以及 [如何註冊 DLL 主控台專案](how-to-register-dll-control-panel-item-registration-.md)。</span><span class="sxs-lookup"><span data-stu-id="c2ce9-739">For more information that can help you discover the necessary CLSIDs, see [How to Register Executable Control Panel Items](how-to-register-an-executable-control-panel-item-registration-.md) and [How to Register DLL Control Panel Items](how-to-register-dll-control-panel-item-registration-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2ce9-740">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2ce9-740">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2ce9-741">執行主控台專案</span><span class="sxs-lookup"><span data-stu-id="c2ce9-741">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="c2ce9-742">**IOpenControlPanel**</span><span class="sxs-lookup"><span data-stu-id="c2ce9-742">**IOpenControlPanel**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



