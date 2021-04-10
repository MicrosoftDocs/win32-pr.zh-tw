---
description: 執行 VSS 備份或還原時，會將 Windows 系統狀態定義為數個主要作業系統元素及其檔案的集合。 備份和還原作業應該一律將這些元素視為一個單位。
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: 備份與還原系統狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed61c3ccad51ebd8cd632fab292160c795741c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692448"
---
# <a name="backing-up-and-restoring-system-state"></a><span data-ttu-id="11e38-104">備份與還原系統狀態</span><span class="sxs-lookup"><span data-stu-id="11e38-104">Backing Up and Restoring System State</span></span>

> [!Note]  
> <span data-ttu-id="11e38-105">本主題適用于 Windows Vista、Windows Server 2008 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="11e38-105">This topic applies to Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="11e38-106">如需 Windows Server 2003 的相關資訊，請參閱 [在 Windows server 2003 R2 和 Windows server 2003 SP1 中備份和還原系統狀態](backing-up-and-restoring-system-state-under-vss.md)</span><span class="sxs-lookup"><span data-stu-id="11e38-106">For information about Windows Server 2003, see [Backing Up and Restoring System State in Windows Server 2003 R2 and Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)</span></span>

 

<span data-ttu-id="11e38-107">執行 VSS 備份或還原時，會將 Windows 系統狀態定義為數個主要作業系統元素及其檔案的集合。</span><span class="sxs-lookup"><span data-stu-id="11e38-107">When performing a VSS backup or restore, the Windows system state is defined as being a collection of several key operating system elements and their files.</span></span> <span data-ttu-id="11e38-108">備份和還原作業應該一律將這些元素視為一個單位。</span><span class="sxs-lookup"><span data-stu-id="11e38-108">These elements should always be treated as a unit by backup and restore operations.</span></span>

> [!Note]  
> <span data-ttu-id="11e38-109">Microsoft 不會提供開發人員或 IT 專業人員技術支援，以在 Windows (所有版本) 上執行線上系統狀態還原。</span><span class="sxs-lookup"><span data-stu-id="11e38-109">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

 

<span data-ttu-id="11e38-110">備份和復原系統狀態時，建議的策略是除了系統狀態寫入器所列舉的檔案之外，還會備份和復原系統和開機磁碟區。</span><span class="sxs-lookup"><span data-stu-id="11e38-110">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span> <span data-ttu-id="11e38-111">系統狀態寫入器是將 [ [**vss \_ 使用 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) ] 屬性設為 [vss \_ BOOTABLESYSTEMSTATE] 或 [ \_ vss SYSTEMSERVICE] 的寫入器 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="11e38-111">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11e38-112">如果 VSS 寫入器以其 [**vss \_ 使用 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) 識別為系統狀態寫入器，則必須將它包含在系統狀態備份中，即使它是可選取的。</span><span class="sxs-lookup"><span data-stu-id="11e38-112">If a VSS Writer is identified by its [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) as a system state writer it must be included in a system state backup even if it is selectable.</span></span>

 

<span data-ttu-id="11e38-113">除了列舉的作業系統和系統狀態寫入器所列舉的驅動程式二進位檔案之外，還必須在系統狀態下備份某些其他檔案。</span><span class="sxs-lookup"><span data-stu-id="11e38-113">In addition to the enumerated operating system and driver binary files that are enumerated by the system state writers, there are certain other files that must be backed up as part of system state.</span></span>

<span data-ttu-id="11e38-114">VSS 系統狀態寫入器所報告的所有元件都是系統狀態的一部分，除了未設定 VSS \_ CF \_ 非 \_ 系統 \_ 狀態旗標的元件之外。</span><span class="sxs-lookup"><span data-stu-id="11e38-114">All the components reported by a VSS system state writer are part of system state except those for which the VSS\_CF\_NOT\_SYSTEM\_STATE flag is set.</span></span>

<span data-ttu-id="11e38-115">備份程式也應該設定 **LastRestoreId** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="11e38-115">Backup programs should also set the **LastRestoreId** registry key.</span></span> <span data-ttu-id="11e38-116">如需詳細資訊，請參閱 [備份和還原的登錄機碼和值](../backup/registry-keys-for-backup-and-restore.md)。</span><span class="sxs-lookup"><span data-stu-id="11e38-116">For more information, see [Registry Keys and Values for Backup and Restore](../backup/registry-keys-for-backup-and-restore.md).</span></span>

> [!Note]  
> <span data-ttu-id="11e38-117">在 Windows Vista、Windows Server 2008 和更新版本中，某些系統檔案的名稱和位置已變更，如下所示。</span><span class="sxs-lookup"><span data-stu-id="11e38-117">In Windows Vista, Windows Server 2008, and later, the names and locations of some system files have been changed as follows.</span></span>

 

## <a name="system-state"></a><span data-ttu-id="11e38-118">系統狀態</span><span class="sxs-lookup"><span data-stu-id="11e38-118">System State</span></span>

<span data-ttu-id="11e38-119">針對 Windows Server 2012 和更新版本，除了各種 VSS 系統狀態寫入器所報告的檔案以外，只需要明確包含下列授權檔案，且必須明確排除下列 DRM 檔案。</span><span class="sxs-lookup"><span data-stu-id="11e38-119">For Windows Server 2012 and later, in addition to the files reported by the various VSS system-state writers, only the following licensing files need to be included explicitly, and the following DRM files need to be excluded explicitly.</span></span>

## <a name="windows-media-digital-rights-management-files"></a><span data-ttu-id="11e38-120">Windows Media 數位 Rights Management 檔案</span><span class="sxs-lookup"><span data-stu-id="11e38-120">Windows Media Digital Rights Management Files</span></span>

<span data-ttu-id="11e38-121">在 Windows Server 2008 和更新版本中，下列檔案（包括下列路徑下的所有子目錄）會從系統狀態中排除，而且不得備份：</span><span class="sxs-lookup"><span data-stu-id="11e38-121">In Windows Server 2008 and later, the following files, including all subdirectories under the following path, are excluded from system state and must not be backed up:</span></span>

-   <span data-ttu-id="11e38-122">% ProgramData% \\ Microsoft \\ Windows \\ DRM</span><span class="sxs-lookup"><span data-stu-id="11e38-122">%ProgramData%\\Microsoft\\Windows\\DRM</span></span>\\

<span data-ttu-id="11e38-123">這會取代 [使用檔案系統和安全性功能](working-with-file-system-and-security-features.md)的 Windows Media 數位 Rights Management 一節中的資訊。</span><span class="sxs-lookup"><span data-stu-id="11e38-123">This supersedes the information in the Windows Media Digital Rights Management section of [Working with File System and Security Features](working-with-file-system-and-security-features.md).</span></span>

## <a name="performance-counter-configuration-files"></a><span data-ttu-id="11e38-124">效能計數器設定檔案</span><span class="sxs-lookup"><span data-stu-id="11e38-124">Performance Counter Configuration Files</span></span>

<span data-ttu-id="11e38-125">效能計數器設定檔位於% SystemRoot% \\ System32 \\ 目錄中，並具有下列名稱：</span><span class="sxs-lookup"><span data-stu-id="11e38-125">The performance counter configuration files are located in the %SystemRoot%\\System32\\ directory and have the following names:</span></span>

<dl> <span data-ttu-id="11e38-126">效能？00？。Dat</span><span class="sxs-lookup"><span data-stu-id="11e38-126">Perf?00?.dat</span></span>  
<span data-ttu-id="11e38-127">Perfc0??。Dat</span><span class="sxs-lookup"><span data-stu-id="11e38-127">Perfc0??.dat</span></span>  
<span data-ttu-id="11e38-128">Perfd0??。Dat</span><span class="sxs-lookup"><span data-stu-id="11e38-128">Perfd0??.dat</span></span>  
<span data-ttu-id="11e38-129">Perfh0??。Dat</span><span class="sxs-lookup"><span data-stu-id="11e38-129">Perfh0??.dat</span></span>  
<span data-ttu-id="11e38-130">Perfi0??。Dat</span><span class="sxs-lookup"><span data-stu-id="11e38-130">Perfi0??.dat</span></span>  
<span data-ttu-id="11e38-131">Prfc0???。Dat</span><span class="sxs-lookup"><span data-stu-id="11e38-131">Prfc0???.dat</span></span>  
<span data-ttu-id="11e38-132">Prfd0???。Dat</span><span class="sxs-lookup"><span data-stu-id="11e38-132">Prfd0???.dat</span></span>  
<span data-ttu-id="11e38-133">Prfh0???。Dat</span><span class="sxs-lookup"><span data-stu-id="11e38-133">Prfh0???.dat</span></span>  
<span data-ttu-id="11e38-134">Prfi0???。Dat</span><span class="sxs-lookup"><span data-stu-id="11e38-134">Prfi0???.dat</span></span>  
</dl>

<span data-ttu-id="11e38-135">這些檔案只會在應用程式安裝期間進行修改，而且應該在系統狀態備份和還原期間進行備份和還原。</span><span class="sxs-lookup"><span data-stu-id="11e38-135">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

## <a name="iis-configuration-files"></a><span data-ttu-id="11e38-136">IIS 設定檔案</span><span class="sxs-lookup"><span data-stu-id="11e38-136">IIS Configuration Files</span></span>

> [!Note]  
> <span data-ttu-id="11e38-137">在 Windows Vista Service Pack 1 (SP1) 和更新版本中，您不應該備份這些檔案。</span><span class="sxs-lookup"><span data-stu-id="11e38-137">In Windows Vista with Service Pack 1 (SP1) and later, you should not back up these files.</span></span> <span data-ttu-id="11e38-138">相反地，請使用內建的 IIS 設定寫入器。</span><span class="sxs-lookup"><span data-stu-id="11e38-138">Instead, use the in-box IIS configuration writer.</span></span> <span data-ttu-id="11e38-139">如需此寫入器的詳細資訊，請參閱 [內建的 VSS 寫入](in-box-vss-writers.md)器。</span><span class="sxs-lookup"><span data-stu-id="11e38-139">For more information about this writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

<span data-ttu-id="11e38-140">相關的 IIS 設定檔和其位置如下所示：</span><span class="sxs-lookup"><span data-stu-id="11e38-140">The relevant IIS configuration files and their locations are listed below:</span></span>

-   <span data-ttu-id="11e38-141">.NET FX machine.config 檔案位於 framework 版本目錄。</span><span class="sxs-lookup"><span data-stu-id="11e38-141">The .NET FX machine.config file is located in the framework version directory.</span></span>
-   <span data-ttu-id="11e38-142">ASP.NET 根目錄 web.config 檔案位於 framework 版本目錄。</span><span class="sxs-lookup"><span data-stu-id="11e38-142">The ASP.NET root web.config file is located in the framework version directory.</span></span>
    > [!Note]  
    > <span data-ttu-id="11e38-143">.NET FX 和 ASP.NET 的設定檔都位於 framework 版本目錄中。</span><span class="sxs-lookup"><span data-stu-id="11e38-143">The configuration files for both .NET FX and ASP.NET are in the framework version directory.</span></span> <span data-ttu-id="11e38-144">如果電腦上安裝了多個版本的架構，此目錄將會包含每個已安裝版本的一個設定檔案。</span><span class="sxs-lookup"><span data-stu-id="11e38-144">If multiple versions of the framework are installed on the computer, this directory will contain one configuration file for each installed version.</span></span>

     

-   <span data-ttu-id="11e38-145">IIS applicationHost.config 中央設定檔案位於% windir% \\ system32 \\ inetsrv \\ config 目錄中。</span><span class="sxs-lookup"><span data-stu-id="11e38-145">The IIS applicationHost.config central configuration file is located in the %windir%\\system32\\inetsrv\\config directory.</span></span> <span data-ttu-id="11e38-146">為了讓伺服器瞭解這個設定檔，有架構檔案可決定其文法和結構。</span><span class="sxs-lookup"><span data-stu-id="11e38-146">For the server to understand this configuration file, there are schema files that determine its grammar and structure.</span></span> <span data-ttu-id="11e38-147">這些檔案位於% windir% \\ system32 \\ inetsrv \\ config \\ schema 目錄中。</span><span class="sxs-lookup"><span data-stu-id="11e38-147">These files are located in the %windir%\\system32\\inetsrv\\config\\schema directory.</span></span>

<span data-ttu-id="11e38-148">Framework 版本目錄路徑會儲存在下列登錄機碼中：</span><span class="sxs-lookup"><span data-stu-id="11e38-148">The framework version directory path is stored in the following registry key:</span></span>

<span data-ttu-id="11e38-149">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 。.Netframework \\ InstallRoot**</span><span class="sxs-lookup"><span data-stu-id="11e38-149">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\.NETFramework\\InstallRoot**</span></span>

<span data-ttu-id="11e38-150">此外，您必須備份下列密碼編譯金鑰：</span><span class="sxs-lookup"><span data-stu-id="11e38-150">In addition, the following cryptography keys must be backed up:</span></span><dl> <span data-ttu-id="11e38-151">% ProgramData% \\ Microsoft \\ 加密 \\ RSA \\ MachineKeys\\\*</span><span class="sxs-lookup"><span data-stu-id="11e38-151">%ProgramData%\\Microsoft\\Crypto\\RSA\\MachineKeys\\\*</span></span>  
<span data-ttu-id="11e38-152">% SystemRoot% \\ System32 \\ Microsoft \\ 保護\\\*</span><span class="sxs-lookup"><span data-stu-id="11e38-152">%SystemRoot%\\System32\\Microsoft\\Protect\\\*</span></span>  
</dl>

## <a name="framework-files"></a><span data-ttu-id="11e38-153">架構檔案</span><span class="sxs-lookup"><span data-stu-id="11e38-153">Framework Files</span></span>

<span data-ttu-id="11e38-154">您必須備份所有的 .NET framework 版本。</span><span class="sxs-lookup"><span data-stu-id="11e38-154">All versions of the .NET framework must be backed up.</span></span> <span data-ttu-id="11e38-155">這些檔案位於下列其中一個或兩個目錄：</span><span class="sxs-lookup"><span data-stu-id="11e38-155">The files are located in one or both of the following directories:</span></span>

<dl> <span data-ttu-id="11e38-156">% windir% \\ Microsoft.Net \\ Framework</span><span class="sxs-lookup"><span data-stu-id="11e38-156">%windir%\\Microsoft.Net\\Framework</span></span>  
<span data-ttu-id="11e38-157">% windir% \\ Microsoft.Net \\ \microsoft.net\framework64\v4.0.30319\</span><span class="sxs-lookup"><span data-stu-id="11e38-157">%windir%\\Microsoft.Net\\Framework64</span></span>  
</dl>

<span data-ttu-id="11e38-158">此外，也必須備份元件檔。</span><span class="sxs-lookup"><span data-stu-id="11e38-158">In addition, the assembly files must be backed up.</span></span> <span data-ttu-id="11e38-159">這些檔案位於下列目錄：</span><span class="sxs-lookup"><span data-stu-id="11e38-159">These files are located in the following directory:</span></span><dl> <span data-ttu-id="11e38-160">% windir% \\ 元件</span><span class="sxs-lookup"><span data-stu-id="11e38-160">%windir%\\assembly</span></span>  
</dl>

## <a name="task-scheduler-task-files"></a><span data-ttu-id="11e38-161">工作排程器任務檔</span><span class="sxs-lookup"><span data-stu-id="11e38-161">Task Scheduler Task Files</span></span>

<span data-ttu-id="11e38-162">必須備份工作排程器的工作檔案。</span><span class="sxs-lookup"><span data-stu-id="11e38-162">The task scheduler's task files must be backed up.</span></span> <span data-ttu-id="11e38-163">這些檔案位於下列其中一個或兩個位置：</span><span class="sxs-lookup"><span data-stu-id="11e38-163">The files are located in one or both of the following locations:</span></span>

<dl> <span data-ttu-id="11e38-164">% windir% \\ system32 工作 \\ 和任何子目錄 (遞迴) </span><span class="sxs-lookup"><span data-stu-id="11e38-164">%windir%\\system32\\tasks and any subdirectories (recursively)</span></span>  
<span data-ttu-id="11e38-165">% windir% 工作 \\ (沒有任何子目錄) </span><span class="sxs-lookup"><span data-stu-id="11e38-165">%windir%\\tasks (no subdirectories)</span></span>  
</dl>

 

 
