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
# <a name="in-box-vss-writers"></a>內建 VSS 寫入器

Windows 作業系統包含一組 VSS 寫入器，負責列舉各種 Windows 功能所需的資料。 這些稱為「內建」的寫入器。

> [!Note]  
> Windows Vista、Windows Server 2008 及更新版本中無法使用 MSDE 的內建寫入器。 相反地，您應該使用 SQL 寫入器來備份 SQL Server 資料庫。 Windows Vista、Windows Server 2008 和更新版本僅支援 SQL Server 2005 SP2 和更新版本。

 

-   [Active Directory Domain Services (NTDS) VSS 寫入器](#active-directory-domain-services-ntds-vss-writer)
-   [Active Directory 同盟服務寫入器](#active-directory-federation-services-writer)
-   [Active Directory 輕量型目錄服務 (LDS) VSS 寫入器](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [Active Directory Rights Management Services (AD RMS) 寫入器](#active-directory-rights-management-services-ad-rms-writer)
-   [自動系統復原 (ASR) 寫入器](#automated-system-recovery-asr-writer)
-   [背景智慧型傳送服務 (位) 寫入器](#background-intelligent-transfer-service-bits-writer)
-   [憑證授權單位單位寫入器](#certificate-authority-writer)
-   [叢集服務寫入器](#cluster-service-writer)
-   [叢集共用磁碟區 (CSV) VSS 寫入器](#cluster-shared-volume-csv-vss-writer)
-   [COM + 類別註冊資料庫寫入器](#com-class-registration-database-writer)
-   [重復資料刪除寫入器](#data-deduplication-writer)
-   [分散式檔案系統複寫 (DFSR)](#distributed-file-system-replication-dfsr)
-   [動態主機設定通訊協定 (DHCP) 寫入器](#dynamic-host-configuration-protocol-dhcp-writer)
-   [檔案複寫服務 (FRS)](#file-replication-service-frs)
-   [檔案伺服器 Resource Manager (FSRM) 寫入器](#file-server-resource-manager-fsrm-writer)
-   [Hyper-v 寫入器](#hyper-v-writer)
-   [IIS 設定寫入器](#iis-configuration-writer)
-   [IIS 元資料庫寫入器](#iis-metabase-writer)
-   [Microsoft Message Queuing (MSMQ) 寫入器](#microsoft-message-queuing-msmq-writer)
-   [MSSearch 服務寫入器](#mssearch-service-writer)
-   [NPS VSS 寫入器](#nps-vss-writer)
-   [效能計數器寫入器](#performance-counters-writer)
-   [登錄寫入器](#registry-writer)
-   [遠端桌面服務 (終端機服務) 閘道 VSS 寫入器](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [遠端桌面服務 (終端機服務) 授權 VSS 寫入器](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [陰影複製優化寫入器](#shadow-copy-optimization-writer)
-   [同步共用服務寫入器](#sync-share-service-writer)
-   [系統寫入器](#system-writer)
-   [工作排程器寫入器](#task-scheduler-writer)
-   [VSS 中繼資料存放區寫入器](#vss-metadata-store-writer)
-   [Windows 部署服務 (WDS) 寫入器](#windows-deployment-services-wds-writer)
-   [Windows 內部資料庫 (WID) 寫入器](#windows-internal-database-wid-writer)
-   [Windows 網際網路名稱服務 (WINS) Writer](#windows-internet-name-service-wins-writer)
-   [WMI 寫入器](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a>Active Directory Domain Services (NTDS) VSS 寫入器

此寫入器會報告 NTDS 資料庫檔案 (ntds.dit) 和相關聯的記錄檔。 您必須要有這些檔案，才能正確還原 Active Directory。

每個網域控制站只有一個 ntds.dit 檔案，而且會在寫入器中繼資料中報告，如下列範例所示：

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

以下範例顯示如何在寫入器的中繼資料中列出元件：

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

在備份時，寫入器會設定寫入器備份中繼資料中的備份到期時間。 要求者應該使用 [**>ivsscomponent：： GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) 來取得此中繼資料，以判斷資料庫是否已過期。 過期的資料庫無法還原。

如果包含 NTDS 資料庫的電腦是網域控制站，則備份應用程式應一律在包含重要系統狀態資訊的所有磁片區上執行系統狀態備份。 在還原時，應用程式應該先以目錄服務還原模式重新開機電腦，然後執行系統狀態還原。

此寫入器的寫入器名稱字串為 "NTDS"。

此寫入器的寫入器識別碼是 B2014C9E-8711-4C5C-A5A9-3CF384484757。

## <a name="active-directory-federation-services-writer"></a>Active Directory 同盟服務寫入器

此寫入器會報告 ADFS) 資料檔案的 Active Directory 同盟服務 (。

**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。

此寫入器的寫入器名稱字串為 "ADFS VSS Writer"。

此寫入器的寫入器識別碼是772C45F8-AE01-4F94-940C-94961864ACAD。

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a>Active Directory 輕量型目錄服務 (LDS) VSS 寫入器

此寫入器會針對% program files% Microsoft ADAM instance N data 中的每個實例報告 ADAM 資料庫檔案 (adamntds.dit) 和相關聯的記錄檔 \\ \\  \\ ，其中 *N* 是 ADAM 實例號碼。 需要這些資料庫記錄檔才能還原 ADAM 實例。

**WINDOWS XP：** 這是不支援的寫入器。

以下範例顯示如何在寫入器的中繼資料中列出元件：

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

在備份時，寫入器會設定備份中繼資料中的備份到期時間。 備份應用程式應該使用 [**>ivsscomponent：： GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) 方法來取得此中繼資料，以判斷資料庫是否已過期。 過期的資料庫無法還原。

此寫入器的寫入器名稱字串是 "ADAM (instance *N*) writer"，其中 *N* 是 adam 實例號碼，例如 "Adam (instance1) WRITER"、"Adam (instance2) writer" 等等。

此寫入器的寫入器識別碼是 DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD。 所有實例的寫入器識別碼都相同。

## <a name="active-directory-rights-management-services-ad-rms-writer"></a>Active Directory Rights Management Services (AD RMS) 寫入器

此寫入器會報告 Active Directory Rights Management 服務 (AD RMS) 資料檔案。

**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。

此寫入器的寫入器名稱字串是「AD RMS Writer」。

此寫入器的寫入器識別碼是886C43B1-D455-4428-A37F-4D6B9E43F50F。

## <a name="automated-system-recovery-asr-writer"></a>自動系統復原 (ASR) 寫入器

ASR 寫入器會在系統上儲存磁片的設定。 此寫入器會報告開機設定資料庫 (BCD) ，而且也負責在陰影複製建立期間，卸載代表 BCD 的登錄區。 ASR 寫入器必須包含在裸機復原所需的任何備份中。 如需 ASR 的詳細資訊，請參閱 [使用 VSS 自動化系統復原進行](using-vss-automated-system-recovery-for-disaster-recovery.md)嚴重損壞修復。

**Windows Server 2003 和 WINDOWS XP：** 這是不支援的寫入器。

此寫入器的寫入器名稱字串是「ASR Writer」。

ASR 寫入器的寫入器識別碼是 BE000CBE-11FE-4426-9C58-531AA6355FC4。

## <a name="background-intelligent-transfer-service-bits-writer"></a>背景智慧型傳送服務 (位) 寫入器

BITS 寫入器會使用 **FilesNotToBackup** 登錄機碼來排除 BITS 快取資料夾中的檔案。 預設快取位置為% AllUsersProfile% \\ Microsoft \\ 網路 \\ 下載程式快取 \\ 。

**Windows Server 2003 和 WINDOWS XP：** 這是不支援的寫入器。

此外，BITS 寫入器會從備份中排除下列檔案： BITS 狀態檔案 (qmgr0 .dat 和) qmgr1、BITS debug 記錄檔和 BITS 部分下載的檔案。

如果 BITS 下載目的地檔案是 SMB 檔案，則用戶端帳戶必須與伺服器有信任關係，否則備份可能會失敗。

此寫入器的寫入器名稱字串為 "BITS Writer"。

BITS 寫入器的寫入器識別碼是4969D978-BE47-48B0-B100-F328F07AC1E0。

## <a name="certificate-authority-writer"></a>憑證授權單位單位寫入器

此寫入器負責列舉憑證伺服器的資料檔案。

此寫入器的寫入器名稱字串是「憑證授權單位單位」。

**WINDOWS XP：** 此寫入器的寫入器名稱字串是「憑證伺服器寫入器」。

寫入器的寫入器識別碼是6F5B15B5-DA24-4D88-B737-63063E3A1F86。

## <a name="cluster-service-writer"></a>叢集服務寫入器

Cluster service VSS 寫入器記載于叢集 [服務](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) API 檔中。

**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista Service Pack 1 (SP1) 和 Windows Server 2008 之前，不支援這個寫入器。

## <a name="cluster-shared-volume-csv-vss-writer"></a>叢集共用磁碟區 (CSV) VSS 寫入器

此寫入器會報告叢集共用磁碟區的 (CSV) 資料檔案。 此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。

**Windows server 2008 R2、Windows server 2008 和 Windows server 2003：** 這是不支援的寫入器。

此寫入器的寫入器名稱字串是「叢集共用磁碟區 VSS 寫入器」。

寫入器的寫入器識別碼是1072AE1C-E5A7-4EA1-9E4A-6F7964656570。

## <a name="com-class-registration-database-writer"></a>COM + 類別註冊資料庫寫入器

此寫入器負責% SystemRoot% \\ 註冊目錄的內容。 COM + 類別目錄是% SystemRoot% 登錄中的檔案，其 \\ 名稱遵循模式的 Rget-help，其中的名稱是12位數的十六進位數位。 如果電腦上已設定 COM + 應用程式，可能會有多個這類檔案。 包含目前 COM + 類別目錄的檔案是具有最大值的 *檔案。*

**Windows Server 2003 和 WINDOWS XP：** 這是不支援的寫入器。

COM + 類別註冊資料庫取決於正在備份的登錄機碼，因此需要與登錄一起備份和還原。

若要還原 COM + 註冊資料庫， (要求者) 的備份應用程式必須呼叫 [**ICOMAdminCatalog：： RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) 方法。

此寫入器的寫入器名稱字串為 "COM + REGDB Writer"。

COM + 類別註冊資料庫寫入器的寫入器識別碼是542DA469-D3E1-473C-9F4F-7847F01FC64F。

## <a name="data-deduplication-writer"></a>重復資料刪除寫入器

重復資料刪除 VSS 寫入器記載于 [重復資料刪除](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) API 檔中。 此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。

**Windows server 2008 R2、Windows server 2008 和 Windows server 2003：** 這是不支援的寫入器。

## <a name="distributed-file-system-replication-dfsr"></a>分散式檔案系統複寫 (DFSR)

下列元件包含 VSS 寫入器： [分散式檔案系統複寫 (DFSR) ](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)

**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista SP1 和 Windows Server 2008 之前，不支援這個寫入器。

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a>動態主機設定通訊協定 (DHCP) 寫入器

此寫入器負責列舉 DHCP 伺服器角色所需的檔案。 此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。

此寫入器的寫入器名稱字串是「Dhcp Jet Writer」。

此寫入器的寫入器識別碼是 BE9AC81E-3619-421F-920F-4C6FEA9E93AD。

## <a name="file-replication-service-frs"></a>檔案複寫服務 (FRS)

檔案複寫服務寫入器記錄在 [備份和還原 FRS-Replicated SYSVOL 資料夾](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md)中。

**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista SP1 和 Windows Server 2008 之前，不支援這個寫入器。

## <a name="file-server-resource-manager-fsrm-writer"></a>檔案伺服器 Resource Manager (FSRM) 寫入器

此寫入器會列舉用來進行系統狀態備份的 FSRM 設定檔。 在還原作業期間，它會防止 FSRM 設定中的變更，並暫時中止配額和檔案檢測的強制執行。 還原完成之後，寫入器會使用已還原的設定來重新整理 FSRM。 只有當 FSRM (一部分的檔案服務角色) 已安裝且正在執行時，才會出現這個寫入器。 此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。

**Windows Server 2003：** 在 Windows Server 2003 R2 之前，不支援這個寫入器。

此寫入器的寫入器名稱字串為 "FSRM Writer"。

此寫入器的寫入器識別碼是12CE4370-5BB7-4C58-A76A-E5D5097E3674。

## <a name="hyper-v-writer"></a>Hyper-v 寫入器

[Hyper-v API 檔](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines)中記載了 hyper-v VSS 寫入器。 此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。

**Windows Server 2003：** 在 Windows Server 2008 之前，不支援這個寫入器。

## <a name="iis-configuration-writer"></a>IIS 設定寫入器

IIS 設定寫入器負責列舉 IIS 設定檔。

**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista SP1 和 Windows Server 2008 之前，不支援這個寫入器。 要求者必須備份 IIS 設定檔，包括 .NET FX machine.config 檔或 ASP.NET 根目錄 web.config 檔。

此寫入器不會備份 .NET FX machine.config 檔或 ASP.NET 根 web.config 檔案，因為這些檔案是由系統寫入器所列舉。

此寫入器會備份% windir% \\ system32 \\ inetsrv 設定 \\ \\ 架構和% windir% \\ system32 inetsrv config 目錄中的所有檔案 \\ \\ ，但系統寫入器所列舉的檔案除外。

IIS 設定寫入器的寫入器識別碼是2A40FD15-DFCA-4aa8-A654-1F8C654603F6。

## <a name="iis-metabase-writer"></a>IIS 元資料庫寫入器

Internet Information Server (IIS) 的「中繼資料寫入器」負責列舉 IIS 中繼檔。

**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista SP1 和 Windows Server 2008 之前，不支援這個寫入器。 要求者必須備份 IIS 的中繼檔。

IIS 元資料庫寫入器的寫入器識別碼是59B1f0CF-90EF-465F-9609-6CA8B2938366。

## <a name="microsoft-message-queuing-msmq-writer"></a>Microsoft Message Queuing (MSMQ) 寫入器

此寫入器會報告 MSMQ) 資料檔案的 Microsoft Message Queuing (。

**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。

此寫入器的寫入器名稱字串是「MSMQ 寫入器 (*SvcName*) 」，其中 *SvcName* 是與寫入器相關聯的 msmq 服務名稱。 針對預設安裝，服務名稱為 "MSMQ"。 若為叢集實例，服務名稱為 MSMQ $*coNtext.resourcename* *，其中的資源名稱為叢集* msmq 資源名稱。

此寫入器的寫入器識別碼是7E47B561-971A-46E6-96B9-696EEAA53B2A。

## <a name="mssearch-service-writer"></a>MSSearch 服務寫入器

此寫入器存在於建立後從陰影複製中刪除搜尋索引檔案。 這是為了將在陰影複製的磁片區上這些檔案的一般 i/o 中，寫入時複製 i/o 的影響降到最低。

**Windows Server 2003：** 這是不支援的寫入器。

若要在伺服器上安裝這個寫入器，您必須安裝檔案服務角色，並啟用 Windows Search 服務。

此寫入器的寫入器名稱字串為 "MSSearch Service Writer"。

MSSearch 服務寫入器的寫入器識別碼是 CD3F2362-8BEF-46C7-9181-D62844CDC0B2。

## <a name="nps-vss-writer"></a>NPS VSS 寫入器

NPS 寫入器負責針對已安裝網路原則和存取服務角色的伺服器， (NPS) 設定檔來列舉網路原則伺服器。

**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista SP1 和 Windows Server 2008 之前，不支援這個寫入器。

此寫入器的寫入器名稱字串是「NPS VSS 寫入器」。

NPS VSS 寫入器的寫入器識別碼是 0x35E81631-13E1-48DB-97FC-D5BC721BB18A。

## <a name="performance-counters-writer"></a>效能計數器寫入器

此寫入器會報告效能計數器設定檔案。 這些檔案只會在應用程式安裝期間進行修改，而且應該在系統狀態備份和還原期間進行備份和還原。

**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。 要求者必須手動備份這些檔案。  (參閱 [備份及還原系統狀態](locating-additional-system-files.md)。 ) 

此寫入器的寫入器名稱字串是「效能計數器寫入器」。

效能計數器寫入器的寫入器識別碼是0BADA1DE-01A9-4625-8278-69E735F39DD2。

## <a name="registry-writer"></a>登錄寫入器

登錄寫入器會報告 Windows 登錄檔，以啟用登錄的就地備份和還原。 它不會報告使用者 hive。

**Windows Server 2003：** 在 Windows Server 2003 中，此寫入器使用中繼存放庫檔案 (有時稱為「算檔案」 ) 來儲存登錄資料。  (查看 [VSS 下的登錄備份和還原作業](registry-backup-and-restore-operations-under-vss.md)。 ) 

**WINDOWS XP：** 這是不支援的寫入器。  (查看 [VSS 下的登錄備份和還原作業](registry-backup-and-restore-operations-under-vss.md)。 ) 

此寫入器的寫入器名稱字串為 "Registry Writer"。

登錄寫入器的寫入器識別碼是 AFBAB4A2-367D-4D15-A586-71DBB18F8485。

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a>遠端桌面服務 (終端機服務) 閘道 VSS 寫入器

此寫入器負責列舉遠端桌面服務 (終端機服務) 閘道檔案，適用于已安裝遠端桌面閘道、subrole 為遠端桌面服務角色的伺服器。

**Windows Server 2003：** 這是不支援的寫入器。

此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。

遠端桌面服務閘道相依于要備份的數個登錄機碼，因此需要與登錄一起備份和還原。

此寫入器的寫入器名稱字串是「TS 閘道寫入器」。

此寫入器的寫入器識別碼是368753EC-572E-4FC7-B4B9-CCD9BDC624CB。

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a>遠端桌面服務 (終端機服務) 授權 VSS 寫入器

此寫入器負責列舉遠端桌面服務授權 (RD 授權) 或終端機服務授權 (已安裝) 角色 subrole 之伺服器的 TS 授權遠端桌面授權檔。

**Windows Server 2003：** 這是不支援的寫入器。

此寫入器是 Windows Server 作業系統版本的現成寫入器;它並未隨附于 Windows 用戶端。

遠端桌面服務授權取決於多個備份的登錄機碼，因此需要與登錄一起備份和還原。

此寫入器的寫入器名稱字串為 "TermServLicensing"。

此寫入器的寫入器識別碼是5382579C-98DF-47A7-AC6C-98A6D7106E09。

## <a name="shadow-copy-optimization-writer"></a>陰影複製優化寫入器

此寫入器會刪除磁片區陰影複製中的特定檔案。 這是為了將在陰影複製的磁片區上這些檔案的一般 i/o 中，寫入時複製 i/o 的影響降到最低。 刪除的檔案通常是暫存檔案或不包含使用者或系統狀態的檔案。

**Windows Server 2003 和 WINDOWS XP：** 這是不支援的寫入器。

此寫入器的寫入器名稱字串是「陰影複製優化寫入器」。

陰影複製優化寫入器的寫入器識別碼是4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F。

## <a name="sync-share-service-writer"></a>同步共用服務寫入器

**Windows Server 2012 R2：** 此寫入器隨附于 Windows Server 2012 R2 和更新版本的伺服器。 它與桌上出版本不相容。

此寫入器負責列舉已安裝同步共用服務之伺服器上的同步共用，以及確保其中繼資料和資料在備份和還原期間維持一致。

只有當同步共用服務已安裝且正在執行時，才會出現這個寫入器。

每個同步共用都有一個 VSS 寫入器元件。 這包括中繼資料和資料路徑。 這些必須同時備份以保持一致性。

寫入器名稱字串是「同步共用服務 VSS 寫入器」。

寫入器識別碼是 D46BF321-FDBA-4A35-8EC3-454DF03BC86A。

## <a name="system-writer"></a>系統寫入器

系統寫入器會列舉所有作業系統和驅動程式二進位檔，並且必須進行系統狀態備份。

**Windows Server 2003 和 WINDOWS XP：** 這是不支援的寫入器。

此寫入器會在 (CryptSvc) 服務的密碼編譯服務中執行。 系統寫入器會產生包含下列檔案的檔案清單：

-   所有已安裝的靜態檔案。 靜態檔案是在元件資訊清單中列出的檔案，其中 **writeableType** 檔案屬性設定為 "static" 或 ""。 靜態檔案包含受 Windows 資源保護 (WRP) 保護的所有檔案。 不過，並非所有靜態檔案都是受 WRP 保護的檔案。 例如，遊戲檔案是靜態的，但不是受 WRP 保護，因此系統管理員可以變更家長監護設定。
-   Windows 並存 (WinSxS) 目錄的內容，包括所有資訊清單、選擇性元件和協力廠商 Win32 檔案。
    > [!Note]  
    > % Windir% system32 目錄中的許多檔案 \\ 都是 WinSxS 目錄中檔案的永久連結。

     

-   已安裝驅動程式的所有 PnP 檔案 (由 PnP) 擁有。
-   所有使用者模式服務和非 PnP 驅動程式。
-   CryptSvc 所擁有的所有目錄。

還原應用程式負責設定檔案和登錄，並設定 Acl 以符合系統陰影複製。 您也必須建立適當的永久連結，系統狀態還原才能成功。

此寫入器的寫入器名稱字串是「系統寫入器」。

系統寫入器的寫入器識別碼是 E8132975-6F93-4464-A53E-1050253AE220。

## <a name="task-scheduler-writer"></a>工作排程器寫入器

此寫入器會報告工作排程器的工作檔案。

**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。 要求者必須手動備份這些檔案。  (參閱 [備份及還原系統狀態](locating-additional-system-files.md)。 ) 

此寫入器的寫入器名稱字串是「工作排程器 Writer」。

寫入器的寫入器識別碼是 D61D61C8-D73A-4EEE-8CDD-F6F9786B7124。

## <a name="vss-metadata-store-writer"></a>VSS 中繼資料存放區寫入器

此寫入器會報告所有 VSS express 寫入器的寫入器中繼資料檔案。

**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。

此寫入器的寫入器名稱字串是「VSS Express 寫入器中繼資料存放區寫入器」。

寫入器的寫入器識別碼是75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06。

## <a name="windows-deployment-services-wds-writer"></a>Windows 部署服務 (WDS) 寫入器

此寫入器會報告 WDS) 資料檔案的 Windows 部署服務 (。

**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。

此寫入器的寫入器名稱字串是「WDS VSS 寫入器」。

此寫入器的寫入器識別碼是82CB5521-68DB-4626-83A4-7FC6F88853E9。

## <a name="windows-internal-database-wid-writer"></a>Windows 內部資料庫 (WID) 寫入器

此寫入器會報告 WID) 資料檔案的 Windows 內部資料庫 (。

**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 這是不支援的寫入器。

此寫入器的寫入器名稱字串為 "WIDWriter"。

此寫入器的寫入器識別碼是8D5194E1-E455-434A-B2E5-51296CCE67DF。

## <a name="windows-internet-name-service-wins-writer"></a>Windows 網際網路名稱服務 (WINS) Writer

此寫入器負責列舉 WINS 所需的檔案。

**WINDOWS XP：** 這是不支援的寫入器。

此寫入器的寫入器名稱字串是「WINS Jet Writer」。

此寫入器的寫入器識別碼是 F08C1483-8407-4A26-8C26-6C267A629741。

## <a name="wmi-writer"></a>WMI 寫入器

此寫入器是用來識別備份作業期間的 WMI 特定狀態和資料。 資料包含來自 WBEM 存放庫的檔案。

**Windows Server 2003 和 WINDOWS XP：** 這是不支援的寫入器。

此寫入器的寫入器名稱字串是「WMI 寫入器」。

此寫入器的寫入器識別碼是 A6AD56C2-B509-4E6C-BB19-49D8F43532F0。

 

 
