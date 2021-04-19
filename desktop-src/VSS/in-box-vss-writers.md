---
description: Windows 作業系統包含一組 VSS 寫入器，負責列舉各種 Windows 功能所需的資料。 這些稱為 &\# 0034; 內建&\# 0034; 寫入器。
ms.assetid: e20a303d-9440-42be-b383-85f6fad89157
title: 內建 VSS 寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc256cfe72f3653d4af282148c87c2b45bcac51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986873"
---
# <a name="in-box-vss-writers"></a><span data-ttu-id="2656d-104">內建 VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-104">In-Box VSS Writers</span></span>

<span data-ttu-id="2656d-105">Windows 作業系統包含一組 VSS 寫入器，負責列舉各種 Windows 功能所需的資料。</span><span class="sxs-lookup"><span data-stu-id="2656d-105">The Windows operating system includes a set of VSS writers that are responsible for enumerating the data that is required by various Windows features.</span></span> <span data-ttu-id="2656d-106">這些稱為「內建」的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-106">These are referred to as "in-box" writers.</span></span>

> [!Note]  
> <span data-ttu-id="2656d-107">Windows Vista、Windows Server 2008 及更新版本中無法使用 MSDE 的內建寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-107">The MSDE in-box writer is not available in Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="2656d-108">相反地，您應該使用 SQL 寫入器來備份 SQL Server 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2656d-108">Instead, the SQL Writer should be used to back up SQL Server databases.</span></span> <span data-ttu-id="2656d-109">Windows Vista、Windows Server 2008 和更新版本僅支援 SQL Server 2005 SP2 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="2656d-109">Only SQL Server 2005 SP2 and later are supported on Windows Vista, Windows Server 2008, and later.</span></span>

 

-   [<span data-ttu-id="2656d-110">Active Directory Domain Services (NTDS) VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-110">Active Directory Domain Services (NTDS) VSS Writer</span></span>](#active-directory-domain-services-ntds-vss-writer)
-   [<span data-ttu-id="2656d-111">Active Directory 同盟服務寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-111">Active Directory Federation Services Writer</span></span>](#active-directory-federation-services-writer)
-   [<span data-ttu-id="2656d-112">Active Directory 輕量型目錄服務 (LDS) VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-112">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [<span data-ttu-id="2656d-113">Active Directory Rights Management Services (AD RMS) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-113">Active Directory Rights Management Services (AD RMS) Writer</span></span>](#active-directory-rights-management-services-ad-rms-writer)
-   [<span data-ttu-id="2656d-114">自動系統復原 (ASR) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-114">Automated System Recovery (ASR) Writer</span></span>](#automated-system-recovery-asr-writer)
-   [<span data-ttu-id="2656d-115">背景智慧型傳送服務 (位) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-115">Background Intelligent Transfer Service (BITS) Writer</span></span>](#background-intelligent-transfer-service-bits-writer)
-   [<span data-ttu-id="2656d-116">憑證授權單位單位寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-116">Certificate Authority Writer</span></span>](#certificate-authority-writer)
-   [<span data-ttu-id="2656d-117">叢集服務寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-117">Cluster Service Writer</span></span>](#cluster-service-writer)
-   [<span data-ttu-id="2656d-118">叢集共用磁碟區 (CSV) VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-118">Cluster Shared Volume (CSV) VSS Writer</span></span>](#cluster-shared-volume-csv-vss-writer)
-   [<span data-ttu-id="2656d-119">COM + 類別註冊資料庫寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-119">COM+ Class Registration Database Writer</span></span>](#com-class-registration-database-writer)
-   [<span data-ttu-id="2656d-120">重復資料刪除寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-120">Data Deduplication Writer</span></span>](#data-deduplication-writer)
-   [<span data-ttu-id="2656d-121">分散式檔案系統複寫 (DFSR)</span><span class="sxs-lookup"><span data-stu-id="2656d-121">Distributed File System Replication (DFSR)</span></span>](#distributed-file-system-replication-dfsr)
-   [<span data-ttu-id="2656d-122">動態主機設定通訊協定 (DHCP) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-122">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>](#dynamic-host-configuration-protocol-dhcp-writer)
-   [<span data-ttu-id="2656d-123">檔案複寫服務 (FRS)</span><span class="sxs-lookup"><span data-stu-id="2656d-123">File Replication Service (FRS)</span></span>](#file-replication-service-frs)
-   [<span data-ttu-id="2656d-124">檔案伺服器 Resource Manager (FSRM) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-124">File Server Resource Manager (FSRM) Writer</span></span>](#file-server-resource-manager-fsrm-writer)
-   [<span data-ttu-id="2656d-125">Hyper-v 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-125">Hyper-V Writer</span></span>](#hyper-v-writer)
-   [<span data-ttu-id="2656d-126">IIS 設定寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-126">IIS Configuration Writer</span></span>](#iis-configuration-writer)
-   [<span data-ttu-id="2656d-127">IIS 元資料庫寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-127">IIS Metabase Writer</span></span>](#iis-metabase-writer)
-   [<span data-ttu-id="2656d-128">Microsoft Message Queuing (MSMQ) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-128">Microsoft Message Queuing (MSMQ) Writer</span></span>](#microsoft-message-queuing-msmq-writer)
-   [<span data-ttu-id="2656d-129">MSSearch 服務寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-129">MSSearch Service Writer</span></span>](#mssearch-service-writer)
-   [<span data-ttu-id="2656d-130">NPS VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-130">NPS VSS Writer</span></span>](#nps-vss-writer)
-   [<span data-ttu-id="2656d-131">效能計數器寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-131">Performance Counters Writer</span></span>](#performance-counters-writer)
-   [<span data-ttu-id="2656d-132">登錄寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-132">Registry Writer</span></span>](#registry-writer)
-   [<span data-ttu-id="2656d-133">遠端桌面服務 (終端機服務) 閘道 VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-133">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [<span data-ttu-id="2656d-134">遠端桌面服務 (終端機服務) 授權 VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-134">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [<span data-ttu-id="2656d-135">陰影複製優化寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-135">Shadow Copy Optimization Writer</span></span>](#shadow-copy-optimization-writer)
-   [<span data-ttu-id="2656d-136">同步共用服務寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-136">Sync Share Service Writer</span></span>](#sync-share-service-writer)
-   [<span data-ttu-id="2656d-137">系統寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-137">System Writer</span></span>](#system-writer)
-   [<span data-ttu-id="2656d-138">工作排程器寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-138">Task Scheduler Writer</span></span>](#task-scheduler-writer)
-   [<span data-ttu-id="2656d-139">VSS 中繼資料存放區寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-139">VSS Metadata Store Writer</span></span>](#vss-metadata-store-writer)
-   [<span data-ttu-id="2656d-140">Windows 部署服務 (WDS) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-140">Windows Deployment Services (WDS) Writer</span></span>](#windows-deployment-services-wds-writer)
-   [<span data-ttu-id="2656d-141">Windows 內部資料庫 (WID) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-141">Windows Internal Database (WID) Writer</span></span>](#windows-internal-database-wid-writer)
-   [<span data-ttu-id="2656d-142">Windows 網際網路名稱服務 (WINS) Writer</span><span class="sxs-lookup"><span data-stu-id="2656d-142">Windows Internet Name Service (WINS) Writer</span></span>](#windows-internet-name-service-wins-writer)
-   [<span data-ttu-id="2656d-143">WMI 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-143">WMI Writer</span></span>](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a><span data-ttu-id="2656d-144">Active Directory Domain Services (NTDS) VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-144">Active Directory Domain Services (NTDS) VSS Writer</span></span>

<span data-ttu-id="2656d-145">此寫入器會報告 NTDS 資料庫檔案 (ntds.dit) 和相關聯的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="2656d-145">This writer reports the NTDS database file (ntds.dit) and the associated log files.</span></span> <span data-ttu-id="2656d-146">您必須要有這些檔案，才能正確還原 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="2656d-146">These files are required to restore the Active Directory correctly.</span></span>

<span data-ttu-id="2656d-147">每個網域控制站只有一個 ntds.dit 檔案，而且會在寫入器中繼資料中報告，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="2656d-147">There is only one ntds.dit file per domain controller, and it is reported in the writer metadata as in the following example:</span></span>

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

<span data-ttu-id="2656d-148">以下範例顯示如何在寫入器的中繼資料中列出元件：</span><span class="sxs-lookup"><span data-stu-id="2656d-148">Here is an example that shows how to list components in the writer's metadata:</span></span>

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Windows_NTDS" 
                     componentName="ntds" 
                     caption="" restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/> 
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

<span data-ttu-id="2656d-149">在備份時，寫入器會設定寫入器備份中繼資料中的備份到期時間。</span><span class="sxs-lookup"><span data-stu-id="2656d-149">At backup time, the writer sets the backup expiration time in the writer's backup metadata.</span></span> <span data-ttu-id="2656d-150">要求者應該使用 [**>ivsscomponent：： GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) 來取得此中繼資料，以判斷資料庫是否已過期。</span><span class="sxs-lookup"><span data-stu-id="2656d-150">Requesters should retrieve this metadata by using [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) to determine whether the database has expired.</span></span> <span data-ttu-id="2656d-151">過期的資料庫無法還原。</span><span class="sxs-lookup"><span data-stu-id="2656d-151">Expired databases cannot be restored.</span></span>

<span data-ttu-id="2656d-152">如果包含 NTDS 資料庫的電腦是網域控制站，則備份應用程式應一律在包含重要系統狀態資訊的所有磁片區上執行系統狀態備份。</span><span class="sxs-lookup"><span data-stu-id="2656d-152">If the computer that contains the NTDS database is a domain controller, the backup application should always perform a system state backup across all volumes containing critical system state information.</span></span> <span data-ttu-id="2656d-153">在還原時，應用程式應該先以目錄服務還原模式重新開機電腦，然後執行系統狀態還原。</span><span class="sxs-lookup"><span data-stu-id="2656d-153">At restore time, the application should first restart the computer in Directory Services Restore Mode and then perform a system state restore.</span></span>

<span data-ttu-id="2656d-154">此寫入器的寫入器名稱字串為 "NTDS"。</span><span class="sxs-lookup"><span data-stu-id="2656d-154">The writer name string for this writer is "NTDS".</span></span>

<span data-ttu-id="2656d-155">此寫入器的寫入器識別碼是 B2014C9E-8711-4C5C-A5A9-3CF384484757。</span><span class="sxs-lookup"><span data-stu-id="2656d-155">The writer ID for this writer is B2014C9E-8711-4C5C-A5A9-3CF384484757.</span></span>

## <a name="active-directory-federation-services-writer"></a><span data-ttu-id="2656d-156">Active Directory 同盟服務寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-156">Active Directory Federation Services Writer</span></span>

<span data-ttu-id="2656d-157">此寫入器會報告 ADFS) 資料檔案的 Active Directory 同盟服務 (。</span><span class="sxs-lookup"><span data-stu-id="2656d-157">This writer reports the Active Directory Federation Services (ADFS) data files.</span></span>

<span data-ttu-id="2656d-158">**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-158">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-159">此寫入器的寫入器名稱字串為 "ADFS VSS Writer"。</span><span class="sxs-lookup"><span data-stu-id="2656d-159">The writer name string for this writer is "ADFS VSS Writer".</span></span>

<span data-ttu-id="2656d-160">此寫入器的寫入器識別碼是772C45F8-AE01-4F94-940C-94961864ACAD。</span><span class="sxs-lookup"><span data-stu-id="2656d-160">The writer ID for this writer is 772C45F8-AE01-4F94-940C-94961864ACAD.</span></span>

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a><span data-ttu-id="2656d-161">Active Directory 輕量型目錄服務 (LDS) VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-161">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>

<span data-ttu-id="2656d-162">此寫入器會針對% program files% Microsoft ADAM instance N data 中的每個實例報告 ADAM 資料庫檔案 (adamntds.dit) 和相關聯的記錄檔 \\ \\  \\ ，其中 *N* 是 ADAM 實例號碼。</span><span class="sxs-lookup"><span data-stu-id="2656d-162">This writer reports the ADAM database file (adamntds.dit) and the associated log files for each instance in %program files%\\Microsoft ADAM\\instance *N*\\data, where *N* is the ADAM instance number.</span></span> <span data-ttu-id="2656d-163">需要這些資料庫記錄檔才能還原 ADAM 實例。</span><span class="sxs-lookup"><span data-stu-id="2656d-163">These database log files are required to restore ADAM instances.</span></span>

<span data-ttu-id="2656d-164">**WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-164">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-165">以下範例顯示如何在寫入器的中繼資料中列出元件：</span><span class="sxs-lookup"><span data-stu-id="2656d-165">Here is an example that shows how to list components in the writer's metadata:</span></span>

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Program Files_Microsoft ADAM_instance1_data" 
                     componentName="adamntds" 
                     caption="" 
                     restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="adamntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

<span data-ttu-id="2656d-166">在備份時，寫入器會設定備份中繼資料中的備份到期時間。</span><span class="sxs-lookup"><span data-stu-id="2656d-166">At backup time, the writer sets the backup expiration time in the backup metadata.</span></span> <span data-ttu-id="2656d-167">備份應用程式應該使用 [**>ivsscomponent：： GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) 方法來取得此中繼資料，以判斷資料庫是否已過期。</span><span class="sxs-lookup"><span data-stu-id="2656d-167">Backup applications should retrieve this metadata by using the [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) method to determine whether the database has expired.</span></span> <span data-ttu-id="2656d-168">過期的資料庫無法還原。</span><span class="sxs-lookup"><span data-stu-id="2656d-168">Expired databases cannot be restored.</span></span>

<span data-ttu-id="2656d-169">此寫入器的寫入器名稱字串是 "ADAM (instance *N*) writer"，其中 *N* 是 adam 實例號碼，例如 "Adam (instance1) WRITER"、"Adam (instance2) writer" 等等。</span><span class="sxs-lookup"><span data-stu-id="2656d-169">The writer name string for this writer is "ADAM (instance *N*) Writer", where *N* is the ADAM instance number, for example, "ADAM (instance1) Writer", "ADAM (instance2) Writer", and so on.</span></span>

<span data-ttu-id="2656d-170">此寫入器的寫入器識別碼是 DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD。</span><span class="sxs-lookup"><span data-stu-id="2656d-170">The writer ID for this writer is DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD.</span></span> <span data-ttu-id="2656d-171">所有實例的寫入器識別碼都相同。</span><span class="sxs-lookup"><span data-stu-id="2656d-171">This writer ID is the same for all instances.</span></span>

## <a name="active-directory-rights-management-services-ad-rms-writer"></a><span data-ttu-id="2656d-172">Active Directory Rights Management Services (AD RMS) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-172">Active Directory Rights Management Services (AD RMS) Writer</span></span>

<span data-ttu-id="2656d-173">此寫入器會報告 Active Directory Rights Management 服務 (AD RMS) 資料檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-173">This writer reports the Active Directory Rights Management Service (AD RMS) data files.</span></span>

<span data-ttu-id="2656d-174">**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-174">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-175">此寫入器的寫入器名稱字串是「AD RMS Writer」。</span><span class="sxs-lookup"><span data-stu-id="2656d-175">The writer name string for this writer is "AD RMS Writer".</span></span>

<span data-ttu-id="2656d-176">此寫入器的寫入器識別碼是886C43B1-D455-4428-A37F-4D6B9E43F50F。</span><span class="sxs-lookup"><span data-stu-id="2656d-176">The writer ID for this writer is 886C43B1-D455-4428-A37F-4D6B9E43F50F.</span></span>

## <a name="automated-system-recovery-asr-writer"></a><span data-ttu-id="2656d-177">自動系統復原 (ASR) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-177">Automated System Recovery (ASR) Writer</span></span>

<span data-ttu-id="2656d-178">ASR 寫入器會在系統上儲存磁片的設定。</span><span class="sxs-lookup"><span data-stu-id="2656d-178">The ASR writer stores the configuration of disks on the system.</span></span> <span data-ttu-id="2656d-179">此寫入器會報告開機設定資料庫 (BCD) ，而且也負責在陰影複製建立期間，卸載代表 BCD 的登錄區。</span><span class="sxs-lookup"><span data-stu-id="2656d-179">This writer reports the Boot Configuration Database (BCD) and is also responsible for dismounting the registry hive that represents the BCD during shadow copy creation.</span></span> <span data-ttu-id="2656d-180">ASR 寫入器必須包含在裸機復原所需的任何備份中。</span><span class="sxs-lookup"><span data-stu-id="2656d-180">The ASR writer must be included in any backups required for bare-metal recovery.</span></span> <span data-ttu-id="2656d-181">如需 ASR 的詳細資訊，請參閱 [使用 VSS 自動化系統復原進行](using-vss-automated-system-recovery-for-disaster-recovery.md)嚴重損壞修復。</span><span class="sxs-lookup"><span data-stu-id="2656d-181">For more information about ASR, see [Using VSS Automated System Recovery for Disaster Recovery](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span>

<span data-ttu-id="2656d-182">**Windows Server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-182">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-183">此寫入器的寫入器名稱字串是「ASR Writer」。</span><span class="sxs-lookup"><span data-stu-id="2656d-183">The writer name string for this writer is "ASR Writer".</span></span>

<span data-ttu-id="2656d-184">ASR 寫入器的寫入器識別碼是 BE000CBE-11FE-4426-9C58-531AA6355FC4。</span><span class="sxs-lookup"><span data-stu-id="2656d-184">The writer ID for the ASR writer is BE000CBE-11FE-4426-9C58-531AA6355FC4.</span></span>

## <a name="background-intelligent-transfer-service-bits-writer"></a><span data-ttu-id="2656d-185">背景智慧型傳送服務 (位) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-185">Background Intelligent Transfer Service (BITS) Writer</span></span>

<span data-ttu-id="2656d-186">BITS 寫入器會使用 **FilesNotToBackup** 登錄機碼來排除 BITS 快取資料夾中的檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-186">The BITS writer uses the **FilesNotToBackup** registry key to exclude files from the BITS cache folder.</span></span> <span data-ttu-id="2656d-187">預設快取位置為% AllUsersProfile% \\ Microsoft \\ 網路 \\ 下載程式快取 \\ 。</span><span class="sxs-lookup"><span data-stu-id="2656d-187">The default cache location is %AllUsersProfile%\\Microsoft\\Network\\Downloader\\Cache.</span></span>

<span data-ttu-id="2656d-188">**Windows Server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-188">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-189">此外，BITS 寫入器會從備份中排除下列檔案： BITS 狀態檔案 (qmgr0 .dat 和) qmgr1、BITS debug 記錄檔和 BITS 部分下載的檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-189">In addition, the BITS writer excludes the following files from backup: the BITS state files (qmgr0.dat and qmgr1.dat), the BITS debug log file, and BITS partially downloaded files.</span></span>

<span data-ttu-id="2656d-190">如果 BITS 下載目的地檔案是 SMB 檔案，則用戶端帳戶必須與伺服器有信任關係，否則備份可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="2656d-190">If the BITS download destination file is an SMB file, the client account must have a trust relationship to the server, or else backups may fail.</span></span>

<span data-ttu-id="2656d-191">此寫入器的寫入器名稱字串為 "BITS Writer"。</span><span class="sxs-lookup"><span data-stu-id="2656d-191">The writer name string for this writer is "BITS Writer".</span></span>

<span data-ttu-id="2656d-192">BITS 寫入器的寫入器識別碼是4969D978-BE47-48B0-B100-F328F07AC1E0。</span><span class="sxs-lookup"><span data-stu-id="2656d-192">The writer ID for the BITS writer is 4969D978-BE47-48B0-B100-F328F07AC1E0.</span></span>

## <a name="certificate-authority-writer"></a><span data-ttu-id="2656d-193">憑證授權單位單位寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-193">Certificate Authority Writer</span></span>

<span data-ttu-id="2656d-194">此寫入器負責列舉憑證伺服器的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-194">This writer is responsible for enumerating the data files for the Certificate Server.</span></span>

<span data-ttu-id="2656d-195">此寫入器的寫入器名稱字串是「憑證授權單位單位」。</span><span class="sxs-lookup"><span data-stu-id="2656d-195">The writer name string for this writer is "Certificate Authority".</span></span>

<span data-ttu-id="2656d-196">**WINDOWS XP：** 此寫入器的寫入器名稱字串是「憑證伺服器寫入器」。</span><span class="sxs-lookup"><span data-stu-id="2656d-196">**Windows XP:** The writer name string for this writer is "Certificate Server Writer".</span></span>

<span data-ttu-id="2656d-197">寫入器的寫入器識別碼是6F5B15B5-DA24-4D88-B737-63063E3A1F86。</span><span class="sxs-lookup"><span data-stu-id="2656d-197">The writer ID for the writer is 6F5B15B5-DA24-4D88-B737-63063E3A1F86.</span></span>

## <a name="cluster-service-writer"></a><span data-ttu-id="2656d-198">叢集服務寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-198">Cluster Service Writer</span></span>

<span data-ttu-id="2656d-199">Cluster service VSS 寫入器記載于叢集 [服務](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) API 檔中。</span><span class="sxs-lookup"><span data-stu-id="2656d-199">The Cluster Service VSS writer is documented in the [Cluster Service](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) API documentation.</span></span>

<span data-ttu-id="2656d-200">**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista Service Pack 1 (SP1) 和 Windows Server 2008 之前，不支援這個寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-200">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with Service Pack 1 (SP1) and Windows Server 2008.</span></span>

## <a name="cluster-shared-volume-csv-vss-writer"></a><span data-ttu-id="2656d-201">叢集共用磁碟區 (CSV) VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-201">Cluster Shared Volume (CSV) VSS Writer</span></span>

<span data-ttu-id="2656d-202">此寫入器會報告叢集共用磁碟區的 (CSV) 資料檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-202">This writer reports the Cluster Shared Volume (CSV) data files.</span></span> <span data-ttu-id="2656d-203">此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。</span><span class="sxs-lookup"><span data-stu-id="2656d-203">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="2656d-204">**Windows server 2008 R2、Windows server 2008 和 Windows server 2003：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-204">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-205">此寫入器的寫入器名稱字串是「叢集共用磁碟區 VSS 寫入器」。</span><span class="sxs-lookup"><span data-stu-id="2656d-205">The writer name string for this writer is "Cluster Shared Volume VSS Writer".</span></span>

<span data-ttu-id="2656d-206">寫入器的寫入器識別碼是1072AE1C-E5A7-4EA1-9E4A-6F7964656570。</span><span class="sxs-lookup"><span data-stu-id="2656d-206">The writer ID for the writer is 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.</span></span>

## <a name="com-class-registration-database-writer"></a><span data-ttu-id="2656d-207">COM + 類別註冊資料庫寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-207">COM+ Class Registration Database Writer</span></span>

<span data-ttu-id="2656d-208">此寫入器負責% SystemRoot% \\ 註冊目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="2656d-208">This writer is responsible for the contents of the %SystemRoot%\\Registration directory.</span></span> <span data-ttu-id="2656d-209">COM + 類別目錄是% SystemRoot% 登錄中的檔案，其 \\ 名稱遵循模式的 Rget-help，其中的名稱是12位數的十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="2656d-209">The COM+ catalog is a file in %SystemRoot%\\Registration with a name that follows the pattern R *xxxxxxxxxxxx*.clb, where *xxxxxxxxxxxx* is a 12-digit hexadecimal number.</span></span> <span data-ttu-id="2656d-210">如果電腦上已設定 COM + 應用程式，可能會有多個這類檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-210">There can potentially be multiple such files if COM+ applications have been configured on the computer.</span></span> <span data-ttu-id="2656d-211">包含目前 COM + 類別目錄的檔案是具有最大值的 *檔案。*</span><span class="sxs-lookup"><span data-stu-id="2656d-211">The file that contains the current COM+ catalog is the file with the largest value of *xxxxxxxxxxxx*.</span></span>

<span data-ttu-id="2656d-212">**Windows Server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-212">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-213">COM + 類別註冊資料庫取決於正在備份的登錄機碼，因此需要與登錄一起備份和還原。</span><span class="sxs-lookup"><span data-stu-id="2656d-213">The COM+ class registration database depends on a registry key being backed up and hence needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="2656d-214">若要還原 COM + 註冊資料庫， (要求者) 的備份應用程式必須呼叫 [**ICOMAdminCatalog：： RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) 方法。</span><span class="sxs-lookup"><span data-stu-id="2656d-214">To restore the COM+ Registration Database, a backup application (requester) must call the [**ICOMAdminCatalog::RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) method.</span></span>

<span data-ttu-id="2656d-215">此寫入器的寫入器名稱字串為 "COM + REGDB Writer"。</span><span class="sxs-lookup"><span data-stu-id="2656d-215">The writer name string for this writer is "COM+ REGDB Writer".</span></span>

<span data-ttu-id="2656d-216">COM + 類別註冊資料庫寫入器的寫入器識別碼是542DA469-D3E1-473C-9F4F-7847F01FC64F。</span><span class="sxs-lookup"><span data-stu-id="2656d-216">The writer ID for the COM+ class registration database writer is 542DA469-D3E1-473C-9F4F-7847F01FC64F.</span></span>

## <a name="data-deduplication-writer"></a><span data-ttu-id="2656d-217">重復資料刪除寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-217">Data Deduplication Writer</span></span>

<span data-ttu-id="2656d-218">重復資料刪除 VSS 寫入器記載于 [重復資料刪除](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) API 檔中。</span><span class="sxs-lookup"><span data-stu-id="2656d-218">The Data Deduplication VSS writer is documented in the [Data Deduplication](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) API documentation.</span></span> <span data-ttu-id="2656d-219">此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。</span><span class="sxs-lookup"><span data-stu-id="2656d-219">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="2656d-220">**Windows server 2008 R2、Windows server 2008 和 Windows server 2003：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-220">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

## <a name="distributed-file-system-replication-dfsr"></a><span data-ttu-id="2656d-221">分散式檔案系統複寫 (DFSR)</span><span class="sxs-lookup"><span data-stu-id="2656d-221">Distributed File System Replication (DFSR)</span></span>

<span data-ttu-id="2656d-222">下列元件包含 VSS 寫入器： [分散式檔案系統複寫 (DFSR) ](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)</span><span class="sxs-lookup"><span data-stu-id="2656d-222">The following component includes a VSS writer: [Distributed File System Replication (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)</span></span>

<span data-ttu-id="2656d-223">**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista SP1 和 Windows Server 2008 之前，不支援這個寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-223">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a><span data-ttu-id="2656d-224">動態主機設定通訊協定 (DHCP) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-224">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>

<span data-ttu-id="2656d-225">此寫入器負責列舉 DHCP 伺服器角色所需的檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-225">This writer is responsible for enumerating files required for the DHCP server role.</span></span> <span data-ttu-id="2656d-226">此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。</span><span class="sxs-lookup"><span data-stu-id="2656d-226">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="2656d-227">此寫入器的寫入器名稱字串是「Dhcp Jet Writer」。</span><span class="sxs-lookup"><span data-stu-id="2656d-227">The writer name string for this writer is "Dhcp Jet Writer".</span></span>

<span data-ttu-id="2656d-228">此寫入器的寫入器識別碼是 BE9AC81E-3619-421F-920F-4C6FEA9E93AD。</span><span class="sxs-lookup"><span data-stu-id="2656d-228">The writer ID for this writer is BE9AC81E-3619-421F-920F-4C6FEA9E93AD.</span></span>

## <a name="file-replication-service-frs"></a><span data-ttu-id="2656d-229">檔案複寫服務 (FRS)</span><span class="sxs-lookup"><span data-stu-id="2656d-229">File Replication Service (FRS)</span></span>

<span data-ttu-id="2656d-230">檔案複寫服務寫入器記錄在 [備份和還原 FRS-Replicated SYSVOL 資料夾](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md)中。</span><span class="sxs-lookup"><span data-stu-id="2656d-230">The File Replication Service writer is documented in [Backing Up and Restoring an FRS-Replicated SYSVOL Folder](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).</span></span>

<span data-ttu-id="2656d-231">**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista SP1 和 Windows Server 2008 之前，不支援這個寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-231">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="file-server-resource-manager-fsrm-writer"></a><span data-ttu-id="2656d-232">檔案伺服器 Resource Manager (FSRM) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-232">File Server Resource Manager (FSRM) Writer</span></span>

<span data-ttu-id="2656d-233">此寫入器會列舉用來進行系統狀態備份的 FSRM 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2656d-233">This writer enumerates the FSRM configuration files that are used for system state backup.</span></span> <span data-ttu-id="2656d-234">在還原作業期間，它會防止 FSRM 設定中的變更，並暫時中止配額和檔案檢測的強制執行。</span><span class="sxs-lookup"><span data-stu-id="2656d-234">During restore operations it prevents changes in FSRM configuration and temporarily halts enforcement of quotas and file screens.</span></span> <span data-ttu-id="2656d-235">還原完成之後，寫入器會使用已還原的設定來重新整理 FSRM。</span><span class="sxs-lookup"><span data-stu-id="2656d-235">After the restore is complete, the writer refreshes FSRM with the configuration that was restored.</span></span> <span data-ttu-id="2656d-236">只有當 FSRM (一部分的檔案服務角色) 已安裝且正在執行時，才會出現這個寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-236">This writer is only present when FSRM (part of File Services role) is both installed and running.</span></span> <span data-ttu-id="2656d-237">此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。</span><span class="sxs-lookup"><span data-stu-id="2656d-237">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="2656d-238">**Windows Server 2003：** 在 Windows Server 2003 R2 之前，不支援這個寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-238">**Windows Server 2003:** This writer is not supported until Windows Server 2003 R2.</span></span>

<span data-ttu-id="2656d-239">此寫入器的寫入器名稱字串為 "FSRM Writer"。</span><span class="sxs-lookup"><span data-stu-id="2656d-239">The writer name string for this writer is "FSRM Writer".</span></span>

<span data-ttu-id="2656d-240">此寫入器的寫入器識別碼是12CE4370-5BB7-4C58-A76A-E5D5097E3674。</span><span class="sxs-lookup"><span data-stu-id="2656d-240">The writer ID for this writer is 12CE4370-5BB7-4C58-A76A-E5D5097E3674.</span></span>

## <a name="hyper-v-writer"></a><span data-ttu-id="2656d-241">Hyper-v 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-241">Hyper-V Writer</span></span>

<span data-ttu-id="2656d-242">[Hyper-v API 檔](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines)中記載了 hyper-v VSS 寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-242">The Hyper-V VSS writer is documented in the [Hyper-V](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) API documentation.</span></span> <span data-ttu-id="2656d-243">此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。</span><span class="sxs-lookup"><span data-stu-id="2656d-243">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="2656d-244">**Windows Server 2003：** 在 Windows Server 2008 之前，不支援這個寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-244">**Windows Server 2003:** This writer is not supported until Windows Server 2008.</span></span>

## <a name="iis-configuration-writer"></a><span data-ttu-id="2656d-245">IIS 設定寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-245">IIS Configuration Writer</span></span>

<span data-ttu-id="2656d-246">IIS 設定寫入器負責列舉 IIS 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2656d-246">The IIS configuration writer is responsible for enumerating the IIS configuration files.</span></span>

<span data-ttu-id="2656d-247">**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista SP1 和 Windows Server 2008 之前，不支援這個寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-247">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="2656d-248">要求者必須備份 IIS 設定檔，包括 .NET FX machine.config 檔或 ASP.NET 根目錄 web.config 檔。</span><span class="sxs-lookup"><span data-stu-id="2656d-248">Requesters are required to back up the IIS configuration files, including the .NET FX machine.config file or the ASP.NET root web.config file.</span></span>

<span data-ttu-id="2656d-249">此寫入器不會備份 .NET FX machine.config 檔或 ASP.NET 根 web.config 檔案，因為這些檔案是由系統寫入器所列舉。</span><span class="sxs-lookup"><span data-stu-id="2656d-249">This writer does not back up the .NET FX machine.config file or the ASP.NET root web.config file because these files are enumerated by the System Writer.</span></span>

<span data-ttu-id="2656d-250">此寫入器會備份% windir% \\ system32 \\ inetsrv 設定 \\ \\ 架構和% windir% \\ system32 inetsrv config 目錄中的所有檔案 \\ \\ ，但系統寫入器所列舉的檔案除外。</span><span class="sxs-lookup"><span data-stu-id="2656d-250">This writer backs up all files that are in the %windir%\\system32\\inetsrv\\config\\schema and %windir%\\system32\\inetsrv\\config directories, except for files that are enumerated by the System Writer.</span></span>

<span data-ttu-id="2656d-251">IIS 設定寫入器的寫入器識別碼是2A40FD15-DFCA-4aa8-A654-1F8C654603F6。</span><span class="sxs-lookup"><span data-stu-id="2656d-251">The writer ID for the IIS configuration writer is 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.</span></span>

## <a name="iis-metabase-writer"></a><span data-ttu-id="2656d-252">IIS 元資料庫寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-252">IIS Metabase Writer</span></span>

<span data-ttu-id="2656d-253">Internet Information Server (IIS) 的「中繼資料寫入器」負責列舉 IIS 中繼檔。</span><span class="sxs-lookup"><span data-stu-id="2656d-253">The Internet Information Server (IIS) metabase writer is responsible for enumerating the IIS metabase file.</span></span>

<span data-ttu-id="2656d-254">**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista SP1 和 Windows Server 2008 之前，不支援這個寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-254">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="2656d-255">要求者必須備份 IIS 的中繼檔。</span><span class="sxs-lookup"><span data-stu-id="2656d-255">Requesters are required to back up the IIS metabase file.</span></span>

<span data-ttu-id="2656d-256">IIS 元資料庫寫入器的寫入器識別碼是59B1f0CF-90EF-465F-9609-6CA8B2938366。</span><span class="sxs-lookup"><span data-stu-id="2656d-256">The writer ID for the IIS metabase writer is 59B1f0CF-90EF-465F-9609-6CA8B2938366.</span></span>

## <a name="microsoft-message-queuing-msmq-writer"></a><span data-ttu-id="2656d-257">Microsoft Message Queuing (MSMQ) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-257">Microsoft Message Queuing (MSMQ) Writer</span></span>

<span data-ttu-id="2656d-258">此寫入器會報告 MSMQ) 資料檔案的 Microsoft Message Queuing (。</span><span class="sxs-lookup"><span data-stu-id="2656d-258">This writer reports the Microsoft Message Queuing (MSMQ) data files.</span></span>

<span data-ttu-id="2656d-259">**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-259">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-260">此寫入器的寫入器名稱字串是「MSMQ 寫入器 (*SvcName*) 」，其中 *SvcName* 是與寫入器相關聯的 msmq 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="2656d-260">The writer name string for this writer is "MSMQ Writer (*SvcName*)", where *SvcName* is the name of the MSMQ service the writer is associated with.</span></span> <span data-ttu-id="2656d-261">針對預設安裝，服務名稱為 "MSMQ"。</span><span class="sxs-lookup"><span data-stu-id="2656d-261">For default installation, the service name is "MSMQ".</span></span> <span data-ttu-id="2656d-262">若為叢集實例，服務名稱為 MSMQ $*coNtext.resourcename* *，其中的資源名稱為叢集* msmq 資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2656d-262">For clustered instances, the service name is MSMQ$*ResourceName*, where *ResourceName* is the clustered MSMQ resource name.</span></span>

<span data-ttu-id="2656d-263">此寫入器的寫入器識別碼是7E47B561-971A-46E6-96B9-696EEAA53B2A。</span><span class="sxs-lookup"><span data-stu-id="2656d-263">The writer ID for this writer is 7E47B561-971A-46E6-96B9-696EEAA53B2A.</span></span>

## <a name="mssearch-service-writer"></a><span data-ttu-id="2656d-264">MSSearch 服務寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-264">MSSearch Service Writer</span></span>

<span data-ttu-id="2656d-265">此寫入器存在於建立後從陰影複製中刪除搜尋索引檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-265">This writer exists to delete search index files from shadow copies after creation.</span></span> <span data-ttu-id="2656d-266">這是為了將在陰影複製的磁片區上這些檔案的一般 i/o 中，寫入時複製 i/o 的影響降到最低。</span><span class="sxs-lookup"><span data-stu-id="2656d-266">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span>

<span data-ttu-id="2656d-267">**Windows Server 2003：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-267">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-268">若要在伺服器上安裝這個寫入器，您必須安裝檔案服務角色，並啟用 Windows Search 服務。</span><span class="sxs-lookup"><span data-stu-id="2656d-268">To install this writer on the server, you must install the File Services role and enable the Windows Search Service.</span></span>

<span data-ttu-id="2656d-269">此寫入器的寫入器名稱字串為 "MSSearch Service Writer"。</span><span class="sxs-lookup"><span data-stu-id="2656d-269">The writer name string for this writer is "MSSearch Service Writer".</span></span>

<span data-ttu-id="2656d-270">MSSearch 服務寫入器的寫入器識別碼是 CD3F2362-8BEF-46C7-9181-D62844CDC0B2。</span><span class="sxs-lookup"><span data-stu-id="2656d-270">The writer ID for the MSSearch service writer is CD3F2362-8BEF-46C7-9181-D62844CDC0B2.</span></span>

## <a name="nps-vss-writer"></a><span data-ttu-id="2656d-271">NPS VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-271">NPS VSS Writer</span></span>

<span data-ttu-id="2656d-272">NPS 寫入器負責針對已安裝網路原則和存取服務角色的伺服器， (NPS) 設定檔來列舉網路原則伺服器。</span><span class="sxs-lookup"><span data-stu-id="2656d-272">The NPS writer is responsible for enumerating the Network Policy Server (NPS) configuration files for servers that have the Network Policy and Access Services role installed.</span></span>

<span data-ttu-id="2656d-273">**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista SP1 和 Windows Server 2008 之前，不支援這個寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-273">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

<span data-ttu-id="2656d-274">此寫入器的寫入器名稱字串是「NPS VSS 寫入器」。</span><span class="sxs-lookup"><span data-stu-id="2656d-274">The writer name string for this writer is "NPS VSS Writer".</span></span>

<span data-ttu-id="2656d-275">NPS VSS 寫入器的寫入器識別碼是 0x35E81631-13E1-48DB-97FC-D5BC721BB18A。</span><span class="sxs-lookup"><span data-stu-id="2656d-275">The writer ID for the NPS VSS writer is 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.</span></span>

## <a name="performance-counters-writer"></a><span data-ttu-id="2656d-276">效能計數器寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-276">Performance Counters Writer</span></span>

<span data-ttu-id="2656d-277">此寫入器會報告效能計數器設定檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-277">This writer reports the performance counter configuration files.</span></span> <span data-ttu-id="2656d-278">這些檔案只會在應用程式安裝期間進行修改，而且應該在系統狀態備份和還原期間進行備份和還原。</span><span class="sxs-lookup"><span data-stu-id="2656d-278">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

<span data-ttu-id="2656d-279">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-279">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="2656d-280">要求者必須手動備份這些檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-280">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="2656d-281"> (參閱 [備份及還原系統狀態](locating-additional-system-files.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="2656d-281">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="2656d-282">此寫入器的寫入器名稱字串是「效能計數器寫入器」。</span><span class="sxs-lookup"><span data-stu-id="2656d-282">The writer name string for this writer is "Performance Counters Writer".</span></span>

<span data-ttu-id="2656d-283">效能計數器寫入器的寫入器識別碼是0BADA1DE-01A9-4625-8278-69E735F39DD2。</span><span class="sxs-lookup"><span data-stu-id="2656d-283">The writer ID for the Performance Counters Writer is 0BADA1DE-01A9-4625-8278-69E735F39DD2.</span></span>

## <a name="registry-writer"></a><span data-ttu-id="2656d-284">登錄寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-284">Registry Writer</span></span>

<span data-ttu-id="2656d-285">登錄寫入器會報告 Windows 登錄檔，以啟用登錄的就地備份和還原。</span><span class="sxs-lookup"><span data-stu-id="2656d-285">The registry writer is reports the Windows registry files to enable in-place backups and restores of the registry.</span></span> <span data-ttu-id="2656d-286">它不會報告使用者 hive。</span><span class="sxs-lookup"><span data-stu-id="2656d-286">It does not report user hives.</span></span>

<span data-ttu-id="2656d-287">**Windows Server 2003：** 在 Windows Server 2003 中，此寫入器使用中繼存放庫檔案 (有時稱為「算檔案」 ) 來儲存登錄資料。</span><span class="sxs-lookup"><span data-stu-id="2656d-287">**Windows Server 2003:** In Windows Server 2003, this writer uses an intermediate repository file (sometimes called a "spit file") to store registry data.</span></span> <span data-ttu-id="2656d-288"> (查看 [VSS 下的登錄備份和還原作業](registry-backup-and-restore-operations-under-vss.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="2656d-288">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="2656d-289">**WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-289">**Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="2656d-290"> (查看 [VSS 下的登錄備份和還原作業](registry-backup-and-restore-operations-under-vss.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="2656d-290">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="2656d-291">此寫入器的寫入器名稱字串為 "Registry Writer"。</span><span class="sxs-lookup"><span data-stu-id="2656d-291">The writer name string for this writer is "Registry Writer".</span></span>

<span data-ttu-id="2656d-292">登錄寫入器的寫入器識別碼是 AFBAB4A2-367D-4D15-A586-71DBB18F8485。</span><span class="sxs-lookup"><span data-stu-id="2656d-292">The writer ID for the registry writer is AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span></span>

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a><span data-ttu-id="2656d-293">遠端桌面服務 (終端機服務) 閘道 VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-293">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>

<span data-ttu-id="2656d-294">此寫入器負責列舉遠端桌面服務 (終端機服務) 閘道檔案，適用于已安裝遠端桌面閘道、subrole 為遠端桌面服務角色的伺服器。</span><span class="sxs-lookup"><span data-stu-id="2656d-294">This writer is responsible for enumerating the Remote Desktop Services (Terminal Services) Gateway files for servers that have Remote Desktop Gateway, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="2656d-295">**Windows Server 2003：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-295">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-296">此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。</span><span class="sxs-lookup"><span data-stu-id="2656d-296">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="2656d-297">遠端桌面服務閘道相依于要備份的數個登錄機碼，因此需要與登錄一起備份和還原。</span><span class="sxs-lookup"><span data-stu-id="2656d-297">The Remote Desktop Services Gateway depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="2656d-298">此寫入器的寫入器名稱字串是「TS 閘道寫入器」。</span><span class="sxs-lookup"><span data-stu-id="2656d-298">The writer name string for this writer is "TS Gateway Writer".</span></span>

<span data-ttu-id="2656d-299">此寫入器的寫入器識別碼是368753EC-572E-4FC7-B4B9-CCD9BDC624CB。</span><span class="sxs-lookup"><span data-stu-id="2656d-299">The writer ID for this writer is 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.</span></span>

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a><span data-ttu-id="2656d-300">遠端桌面服務 (終端機服務) 授權 VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-300">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="2656d-301">此寫入器負責列舉遠端桌面服務授權 (RD 授權) 或終端機服務授權 (已安裝) 角色 subrole 之伺服器的 TS 授權遠端桌面授權檔。</span><span class="sxs-lookup"><span data-stu-id="2656d-301">This writer is responsible for enumerating the Remote Desktop Services Licensing (RD Licensing) or Terminal Services Licensing (TS Licensing) files for servers that have Remote Desktop Licensing, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="2656d-302">**Windows Server 2003：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-302">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-303">此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。</span><span class="sxs-lookup"><span data-stu-id="2656d-303">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="2656d-304">遠端桌面服務授權取決於多個備份的登錄機碼，因此需要與登錄一起備份和還原。</span><span class="sxs-lookup"><span data-stu-id="2656d-304">Remote Desktop Services Licensing depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="2656d-305">此寫入器的寫入器名稱字串為 "TermServLicensing"。</span><span class="sxs-lookup"><span data-stu-id="2656d-305">The writer name string for this writer is "TermServLicensing".</span></span>

<span data-ttu-id="2656d-306">此寫入器的寫入器識別碼是5382579C-98DF-47A7-AC6C-98A6D7106E09。</span><span class="sxs-lookup"><span data-stu-id="2656d-306">The writer ID for this writer is 5382579C-98DF-47A7-AC6C-98A6D7106E09.</span></span>

## <a name="shadow-copy-optimization-writer"></a><span data-ttu-id="2656d-307">陰影複製優化寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-307">Shadow Copy Optimization Writer</span></span>

<span data-ttu-id="2656d-308">此寫入器會刪除磁片區陰影複製中的特定檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-308">This writer deletes certain files from volume shadow copies.</span></span> <span data-ttu-id="2656d-309">這是為了將在陰影複製的磁片區上這些檔案的一般 i/o 中，寫入時複製 i/o 的影響降到最低。</span><span class="sxs-lookup"><span data-stu-id="2656d-309">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span> <span data-ttu-id="2656d-310">刪除的檔案通常是暫存檔案或不包含使用者或系統狀態的檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-310">The files that are deleted are typically temporary files or files that do not contain user or system state.</span></span>

<span data-ttu-id="2656d-311">**Windows Server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-311">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-312">此寫入器的寫入器名稱字串是「陰影複製優化寫入器」。</span><span class="sxs-lookup"><span data-stu-id="2656d-312">The writer name string for this writer is "Shadow Copy Optimization Writer".</span></span>

<span data-ttu-id="2656d-313">陰影複製優化寫入器的寫入器識別碼是4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F。</span><span class="sxs-lookup"><span data-stu-id="2656d-313">The writer ID for the shadow copy optimization writer is 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.</span></span>

## <a name="sync-share-service-writer"></a><span data-ttu-id="2656d-314">同步共用服務寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-314">Sync Share Service Writer</span></span>

<span data-ttu-id="2656d-315">**Windows Server 2012 R2：** 此寫入器隨附于 Windows Server 2012 R2 和更新版本的伺服器。</span><span class="sxs-lookup"><span data-stu-id="2656d-315">**Windows Server 2012 R2:** This writer is included with Windows Server 2012 R2 and newer server versions.</span></span> <span data-ttu-id="2656d-316">它與桌上出版本不相容。</span><span class="sxs-lookup"><span data-stu-id="2656d-316">It is not compatible with desktop versions.</span></span>

<span data-ttu-id="2656d-317">此寫入器負責列舉已安裝同步共用服務之伺服器上的同步共用，以及確保其中繼資料和資料在備份和還原期間維持一致。</span><span class="sxs-lookup"><span data-stu-id="2656d-317">This writer is responsible for enumerating the sync shares on servers that have the Sync Share Service installed, and for ensuring that their metadata and data remain consistent during backup and restore.</span></span>

<span data-ttu-id="2656d-318">只有當同步共用服務已安裝且正在執行時，才會出現這個寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-318">This writer is only present when Sync Share Service is both installed and running.</span></span>

<span data-ttu-id="2656d-319">每個同步共用都有一個 VSS 寫入器元件。</span><span class="sxs-lookup"><span data-stu-id="2656d-319">There will be one VSS writer component for each sync share.</span></span> <span data-ttu-id="2656d-320">這包括中繼資料和資料路徑。</span><span class="sxs-lookup"><span data-stu-id="2656d-320">This includes the metadata and data paths.</span></span> <span data-ttu-id="2656d-321">這些必須同時備份以保持一致性。</span><span class="sxs-lookup"><span data-stu-id="2656d-321">These must be backed up together for consistency.</span></span>

<span data-ttu-id="2656d-322">寫入器名稱字串是「同步共用服務 VSS 寫入器」。</span><span class="sxs-lookup"><span data-stu-id="2656d-322">The writer name string is "Sync Share Service VSS writer".</span></span>

<span data-ttu-id="2656d-323">寫入器識別碼是 D46BF321-FDBA-4A35-8EC3-454DF03BC86A。</span><span class="sxs-lookup"><span data-stu-id="2656d-323">The writer ID is D46BF321-FDBA-4A35-8EC3-454DF03BC86A.</span></span>

## <a name="system-writer"></a><span data-ttu-id="2656d-324">系統寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-324">System Writer</span></span>

<span data-ttu-id="2656d-325">系統寫入器會列舉所有作業系統和驅動程式二進位檔，並且必須進行系統狀態備份。</span><span class="sxs-lookup"><span data-stu-id="2656d-325">The system writer enumerates all operating system and driver binaries and it is required for a system state backup.</span></span>

<span data-ttu-id="2656d-326">**Windows Server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-326">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-327">此寫入器會在 (CryptSvc) 服務的密碼編譯服務中執行。</span><span class="sxs-lookup"><span data-stu-id="2656d-327">This writer runs as part of the Cryptographic Services (CryptSvc) service.</span></span> <span data-ttu-id="2656d-328">系統寫入器會產生包含下列檔案的檔案清單：</span><span class="sxs-lookup"><span data-stu-id="2656d-328">The system writer generates a file list that contains the following files:</span></span>

-   <span data-ttu-id="2656d-329">所有已安裝的靜態檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-329">All static files that have been installed.</span></span> <span data-ttu-id="2656d-330">靜態檔案是在元件資訊清單中列出的檔案，其中 **writeableType** 檔案屬性設定為 "static" 或 ""。</span><span class="sxs-lookup"><span data-stu-id="2656d-330">A static file is a file that is listed in the component manifest with the **writeableType** file attribute set to "static" or "".</span></span> <span data-ttu-id="2656d-331">靜態檔案包含受 Windows 資源保護 (WRP) 保護的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-331">Static files include all files that are protected by Windows Resource Protection (WRP).</span></span> <span data-ttu-id="2656d-332">不過，並非所有靜態檔案都是受 WRP 保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-332">However, not all static files are WRP-protected files.</span></span> <span data-ttu-id="2656d-333">例如，遊戲檔案是靜態的，但不是受 WRP 保護，因此系統管理員可以變更家長監護設定。</span><span class="sxs-lookup"><span data-stu-id="2656d-333">For example, game files are static but not WRP-protected so that administrators can change parental control settings.</span></span>
-   <span data-ttu-id="2656d-334">Windows 並存 (WinSxS) 目錄的內容，包括所有資訊清單、選擇性元件和協力廠商 Win32 檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-334">The contents of the Windows Side-by-Side (WinSxS) directory, including all manifests, optional components, and third-party Win32 files.</span></span>
    > [!Note]  
    > <span data-ttu-id="2656d-335">% Windir% system32 目錄中的許多檔案 \\ 都是 WinSxS 目錄中檔案的永久連結。</span><span class="sxs-lookup"><span data-stu-id="2656d-335">Many of the files in the %windir%\\system32 directory are hard links to files in the WinSxS directory.</span></span>

     

-   <span data-ttu-id="2656d-336">已安裝驅動程式的所有 PnP 檔案 (由 PnP) 擁有。</span><span class="sxs-lookup"><span data-stu-id="2656d-336">All PnP files for installed drivers (owned by PnP).</span></span>
-   <span data-ttu-id="2656d-337">所有使用者模式服務和非 PnP 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="2656d-337">All user-mode services and non-PnP drivers.</span></span>
-   <span data-ttu-id="2656d-338">CryptSvc 所擁有的所有目錄。</span><span class="sxs-lookup"><span data-stu-id="2656d-338">All catalogs owned by CryptSvc.</span></span>

<span data-ttu-id="2656d-339">還原應用程式負責設定檔案和登錄，並設定 Acl 以符合系統陰影複製。</span><span class="sxs-lookup"><span data-stu-id="2656d-339">The restore application is responsible for laying down the files and registry and setting ACLs to match the system shadow copy.</span></span> <span data-ttu-id="2656d-340">您也必須建立適當的永久連結，系統狀態還原才能成功。</span><span class="sxs-lookup"><span data-stu-id="2656d-340">The appropriate hard links must also be created for a system state restore to succeed.</span></span>

<span data-ttu-id="2656d-341">此寫入器的寫入器名稱字串是「系統寫入器」。</span><span class="sxs-lookup"><span data-stu-id="2656d-341">The writer name string for this writer is "System Writer".</span></span>

<span data-ttu-id="2656d-342">系統寫入器的寫入器識別碼是 E8132975-6F93-4464-A53E-1050253AE220。</span><span class="sxs-lookup"><span data-stu-id="2656d-342">The writer ID for the system writer is E8132975-6F93-4464-A53E-1050253AE220.</span></span>

## <a name="task-scheduler-writer"></a><span data-ttu-id="2656d-343">工作排程器寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-343">Task Scheduler Writer</span></span>

<span data-ttu-id="2656d-344">此寫入器會報告工作排程器的工作檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-344">This writer reports the task scheduler's task files.</span></span>

<span data-ttu-id="2656d-345">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-345">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="2656d-346">要求者必須手動備份這些檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-346">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="2656d-347"> (參閱 [備份及還原系統狀態](locating-additional-system-files.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="2656d-347">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="2656d-348">此寫入器的寫入器名稱字串是「工作排程器 Writer」。</span><span class="sxs-lookup"><span data-stu-id="2656d-348">The writer name string for this writer is "Task Scheduler Writer".</span></span>

<span data-ttu-id="2656d-349">寫入器的寫入器識別碼是 D61D61C8-D73A-4EEE-8CDD-F6F9786B7124。</span><span class="sxs-lookup"><span data-stu-id="2656d-349">The writer ID for the writer is D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.</span></span>

## <a name="vss-metadata-store-writer"></a><span data-ttu-id="2656d-350">VSS 中繼資料存放區寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-350">VSS Metadata Store Writer</span></span>

<span data-ttu-id="2656d-351">此寫入器會報告所有 VSS express 寫入器的寫入器中繼資料檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-351">This writer reports the writer metadata files for all VSS express writers.</span></span>

<span data-ttu-id="2656d-352">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-352">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-353">此寫入器的寫入器名稱字串是「VSS Express 寫入器中繼資料存放區寫入器」。</span><span class="sxs-lookup"><span data-stu-id="2656d-353">The writer name string for this writer is "VSS Express Writer Metadata Store Writer".</span></span>

<span data-ttu-id="2656d-354">寫入器的寫入器識別碼是75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06。</span><span class="sxs-lookup"><span data-stu-id="2656d-354">The writer ID for the writer is 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.</span></span>

## <a name="windows-deployment-services-wds-writer"></a><span data-ttu-id="2656d-355">Windows 部署服務 (WDS) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-355">Windows Deployment Services (WDS) Writer</span></span>

<span data-ttu-id="2656d-356">此寫入器會報告 WDS) 資料檔案的 Windows 部署服務 (。</span><span class="sxs-lookup"><span data-stu-id="2656d-356">This writer reports the Windows Deployment Services (WDS) data files.</span></span>

<span data-ttu-id="2656d-357">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-357">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-358">此寫入器的寫入器名稱字串是「WDS VSS 寫入器」。</span><span class="sxs-lookup"><span data-stu-id="2656d-358">The writer name string for this writer is "WDS VSS Writer".</span></span>

<span data-ttu-id="2656d-359">此寫入器的寫入器識別碼是82CB5521-68DB-4626-83A4-7FC6F88853E9。</span><span class="sxs-lookup"><span data-stu-id="2656d-359">The writer ID for this writer is 82CB5521-68DB-4626-83A4-7FC6F88853E9.</span></span>

## <a name="windows-internal-database-wid-writer"></a><span data-ttu-id="2656d-360">Windows 內部資料庫 (WID) 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-360">Windows Internal Database (WID) Writer</span></span>

<span data-ttu-id="2656d-361">此寫入器會報告 WID) 資料檔案的 Windows 內部資料庫 (。</span><span class="sxs-lookup"><span data-stu-id="2656d-361">This writer reports the Windows Internal Database (WID) data files.</span></span>

<span data-ttu-id="2656d-362">**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-362">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-363">此寫入器的寫入器名稱字串為 "WIDWriter"。</span><span class="sxs-lookup"><span data-stu-id="2656d-363">The writer name string for this writer is "WIDWriter".</span></span>

<span data-ttu-id="2656d-364">此寫入器的寫入器識別碼是8D5194E1-E455-434A-B2E5-51296CCE67DF。</span><span class="sxs-lookup"><span data-stu-id="2656d-364">The writer ID for this writer is 8D5194E1-E455-434A-B2E5-51296CCE67DF.</span></span>

## <a name="windows-internet-name-service-wins-writer"></a><span data-ttu-id="2656d-365">Windows 網際網路名稱服務 (WINS) Writer</span><span class="sxs-lookup"><span data-stu-id="2656d-365">Windows Internet Name Service (WINS) Writer</span></span>

<span data-ttu-id="2656d-366">此寫入器負責列舉 WINS 所需的檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-366">This writer is responsible for enumerating files required for WINS.</span></span>

<span data-ttu-id="2656d-367">**WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-367">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-368">此寫入器的寫入器名稱字串是「WINS Jet Writer」。</span><span class="sxs-lookup"><span data-stu-id="2656d-368">The writer name string for this writer is "WINS Jet Writer".</span></span>

<span data-ttu-id="2656d-369">此寫入器的寫入器識別碼是 F08C1483-8407-4A26-8C26-6C267A629741。</span><span class="sxs-lookup"><span data-stu-id="2656d-369">The writer ID for this writer is F08C1483-8407-4A26-8C26-6C267A629741.</span></span>

## <a name="wmi-writer"></a><span data-ttu-id="2656d-370">WMI 寫入器</span><span class="sxs-lookup"><span data-stu-id="2656d-370">WMI Writer</span></span>

<span data-ttu-id="2656d-371">此寫入器是用來識別備份作業期間的 WMI 特定狀態和資料。</span><span class="sxs-lookup"><span data-stu-id="2656d-371">This writer is used for identifying WMI-specific state and data during backup operations.</span></span> <span data-ttu-id="2656d-372">資料包含來自 WBEM 存放庫的檔案。</span><span class="sxs-lookup"><span data-stu-id="2656d-372">The data includes files from the WBEM repository.</span></span>

<span data-ttu-id="2656d-373">**Windows Server 2003 和 WINDOWS XP：** 這是不支援的寫入器。</span><span class="sxs-lookup"><span data-stu-id="2656d-373">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="2656d-374">此寫入器的寫入器名稱字串是「WMI 寫入器」。</span><span class="sxs-lookup"><span data-stu-id="2656d-374">The writer name string for this writer is "WMI Writer".</span></span>

<span data-ttu-id="2656d-375">此寫入器的寫入器識別碼是 A6AD56C2-B509-4E6C-BB19-49D8F43532F0。</span><span class="sxs-lookup"><span data-stu-id="2656d-375">The writer ID for this writer is A6AD56C2-B509-4E6C-BB19-49D8F43532F0.</span></span>

 

 
