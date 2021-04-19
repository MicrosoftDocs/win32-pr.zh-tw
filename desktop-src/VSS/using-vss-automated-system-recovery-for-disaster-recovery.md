---
description: 執行嚴重損壞修復的 VSS 備份和復原應用程式 (也稱為裸機復原) 可以搭配使用自動系統復原 (ASR) 寫入器和 Windows 預先安裝環境 (Windows PE) ，來備份及還原重要磁片區和可開機系統狀態的其他元件。 備份應用程式會實作為 VSS 要求者。
ms.assetid: 13adfd79-f26a-4385-9b59-129d06fa72eb
title: 使用 VSS 自動化系統復原進行嚴重損壞修復
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e31ef8ba223f40928e2422fa92240656f94592d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972041"
---
# <a name="using-vss-automated-system-recovery-for-disaster-recovery"></a>使用 VSS 自動化系統復原進行嚴重損壞修復

執行嚴重損壞修復的 VSS 備份和復原應用程式 (也稱為裸機復原) 可以搭配使用自動系統復原 (ASR) 寫入器和 Windows 預先安裝環境 (Windows PE) ，來備份及還原重要磁片區和可開機系統狀態的其他元件。 備份應用程式會實作為 VSS 要求者。

**注意**  使用 ASR 的應用程式必須 Windows PE 授權。

**Windows Server 2003 和 WINDOWS XP：** ASR 不會實作為 VSS 寫入器。

如需可搭配 ASR 使用之追蹤工具的相關資訊，請參閱搭配 [使用追蹤工具與 VSS Asr 應用程式](using-tracing-tools-with-vss-asr-applications.md)。

**本文內容：**

-   [備份階段工作總覽](#overview-of-backup-phase-tasks)
-   [選擇要備份的重要元件](#choosing-which-critical-components-to-back-up)
-   [還原階段工作的總覽](#overview-of-restore-phase-tasks)
-   [排除磁片區的所有磁片](#excluding-all-disks-for-a-volume)

## <a name="overview-of-backup-phase-tasks"></a>備份階段工作總覽

在備份時，要求者會執行下列步驟。

> [!Note]  
> 除非另有指示，否則所有步驟都是必要的。

 

1.  呼叫 [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) 函數來建立 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面的實例，並呼叫 [**>ivssbackupcomponents：： InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) 方法來初始化實例，以管理備份。
2.  呼叫 [**>ivssbackupcomponents：： SetCoNtext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) 來設定陰影複製作業的內容。
3.  呼叫 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) 來設定備份。 將 *bBackupBootableSystemState* 參數設定為 **true** ，表示備份將包含可開機的系統狀態。
4.  選擇 ASR 寫入器的寫入器元資料檔案中要備份的重要元件，並為每個元件呼叫 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 。
5.  呼叫 [**>ivssbackupcomponents：： StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) 來建立新的空白陰影複製集。
6.  呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) ，以起始與寫入器的非同步連絡人。
7.  呼叫 [**>ivssbackupcomponents：： GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) ，以取出 ASR 寫入器的寫入器元資料檔案。 ASR 寫入器的寫入器識別碼是 BE000CBE-11FE-4426-9C58-531AA6355FC4，而寫入器名稱字串是「ASR Writer」。
8.  呼叫 [**IVssExamineWriterMetadata：： SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) ，以儲存 ASR 寫入器的寫入器元資料檔案的複本。
9.  針對可參與陰影複製的每個磁片區呼叫 [**>ivssbackupcomponents：： AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) ，以將磁片區新增至陰影複製集。
10. 呼叫 [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) 通知寫入器，以準備進行備份作業。
11. 呼叫 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 和 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (或 [**IVssBackupComponentsEx3：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex3-getwriterstatusex)) 驗證 ASR 寫入器的狀態。
12. 此時，您可以查詢作者在其 [**CVssWriter：： OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) 方法中所設定的失敗訊息。 如需顯示如何查看這些訊息的範例程式碼，請參閱 [**IVssComponentEx：： GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg)。
13. 呼叫 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 來建立磁片區陰影複製。
14. 呼叫 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 和 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) ，以驗證 ASR 寫入器的狀態。
15. 備份資料。
16. 藉由呼叫 [**>ivssbackupcomponents：： SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)來指出備份作業是否成功。
17. 呼叫 [**>ivssbackupcomponents：： BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) ，表示備份作業已完成。
18. 呼叫 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 和 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)。 寫入器會話狀態記憶體是有限的資源，而寫入器最後必須重複使用會話狀態。 此步驟會將寫入器的備份會話狀態標示為已完成，並通知 VSS 此備份會話位置可以由後續的備份作業重複使用。
    > [!Note]  
    > 只有在 Windows Server 2008 Service Pack 2 (SP2) 及更早版本才需要此功能。

     

19. 呼叫 [**>ivssbackupcomponents：： SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) ，以儲存要求者備份元件檔的複本。 當要求者呼叫 [**>ivssbackupcomponents：： InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) 方法時，會在還原時使用備份元件檔中的資訊。

## <a name="choosing-which-critical-components-to-back-up"></a>選擇要備份的重要元件

在備份初始化階段中，ASR 寫入器會在其寫入器元資料檔案中報告下列類型的元件：

-   重要磁片區，例如開機、系統和 Windows 修復環境 (Windows RE) 磁片區，以及與目前正在執行的 Windows Vista 或 Windows Server 2008 實例相關聯的 Windows RE 磁碟分割。 如果磁片區包含系統狀態資訊，磁片區就是 *重要磁片* 區。 開機和系統磁碟區會自動包含在內。 要求者必須包含包含寫入器所報告之系統關鍵元件的所有磁片區，例如包含 Active Directory 的磁片區。 系統關鍵元件會標示為「無法針對備份進行選取」。 在 VSS 中，「不可選取」表示「非選擇性」。 因此，要求者必須將它們備份為系統狀態的一部分。 如需詳細資訊，請參閱 [備份和還原系統狀態](locating-additional-system-files.md)。 未 \_ 設定 VSS CF \_ 非 \_ 系統 \_ 狀態旗標的元件不是系統關鍵的。
    > [!Note]  
    > ASR 元件是 ASR 寫入器所報告的系統關鍵元件。

     

-   磁片。 電腦上的每個固定磁片都會公開為 ASR 中的元件。 如果在備份期間未排除磁片，則會在還原期間指派磁片，並且可以重新建立和重新格式化。 請注意，在還原期間，要求者仍然可以藉由呼叫 [**>ivssbackupcomponents：： SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) 方法，重新建立在備份期間排除的磁片。 如果選取了動態磁碟套件中的一個磁片，則也必須選取該套件中的所有其他磁片。 如果選取磁片區是因為磁片區是重要磁片區 (也就是包含系統狀態資訊的磁片區) ，也必須選取包含該磁片區範圍的每個磁片。 若要尋找磁片區的範圍，請使用 [**[ \_ IOCTL \_ \_ \_ 磁片區磁片 \_ 區磁片區**](/windows/win32/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents) 控制程式代碼]。

    > [!Note]  
    > 在備份期間，要求者應包含所有固定磁片。 如果包含要求者備份組的磁片是本機磁片，則應包含此磁片。 在還原期間，要求者必須排除包含要求者之備份組的磁片，以防止其遭到覆寫。

     

    在叢集環境中，ASR 不會重新建立叢集共用磁片的版面配置。 在 Windows RE 中還原作業系統之後，應該將這些磁片還原至線上。

-   開機設定資料 (BCD) 存放區。 此元件指定包含 BCD 存放區之目錄的路徑。 要求者必須指定此元件，並備份 BCD 存放區目錄中的所有檔案。 如需 BCD 存放區的詳細資訊，請參閱 [關於 bcd](/previous-versions/windows/desktop/bcd/about-bcd)。
    > [!Note]  
    > 在使用擴充固件介面 (EFI) 的電腦上，EFI 系統磁碟分割 (ESP) 一律會隱藏，不能包含在磁片區陰影複製中。 要求者必須備份此分割區的內容。 由於此分割區不能包含在磁片區陰影複製中，因此只能從實際磁片區執行備份，而不是從陰影複製執行。 如需有關 EFI 和 ESP 的詳細資訊，請參閱 [帶出指南](/windows-hardware/drivers/bringup/)。

元件名稱使用下列格式：

-   若是磁片元件，格式為

    <COMPONENT logicalPath="Disks" componentName="harddisk*n*" componentType="filegroup" />

    其中 *n* 是磁片編號。 只記錄磁片編號。 若要取得磁片編號，請使用 [**IOCTL \_ 儲存體 \_ 取得 \_ 裝置 \_ 編號**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) 控制程式代碼。

-   若是磁片區元件，格式為

    <COMPONENT logicalPath="Volumes" componentName="Volume{*GUID*}" componentType="filegroup" />

    其中 *guid* 是磁片區 guid。

-   針對 BCD 存放區元件，格式為

    <COMPONENT logicalPath="BCD" componentName="BCD" componentType="filegroup" componentCaption = "This is the path to the boot BCD store and the boot managers...All the files in this directory need to be backed up...">

    如果系統磁碟分割具有磁片區 GUID 名稱，此元件是可選取的。 否則，就無法選取。

    > [!Note]  
    > ASR 會將檔案新增至 BCD 存放區元件的檔案群組，如下所示：
    >
    > -   EFI 磁片的 ASR 新增
    >
    >     *SystemPartitionPath* \\EFI \\ Microsoft \\ 開機 \\ \* 。\*
    >
    >     其中 *SystemPartitionPath* 是系統磁碟分割的路徑。
    >
    > -   針對 GPT 磁片，ASR 新增
    >
    >     *SystemPartitionPath* \\開機 \\ \* 。\*
    >
    >     其中 *SystemPartitionPath* 是系統磁碟分割的路徑。
    >
    > -   您可以在下列登錄機碼下找到系統磁碟分割路徑： **HKEY \_ LOCAL \_ MACHINE** \\ **system** \\ **Setup** \\ **SystemPartition**

     

還原時，標記為重要磁片區的所有元件都必須還原。 如果無法還原一或多個重要磁片區，則還原作業會失敗。

在還原順序的 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) 階段中，不會重新建立備份期間未排除的磁片，並且預設會重新格式化。 但是，如果它們符合下列條件，則不會重新建立或重新格式化它們：

-   如果未變更磁片的磁片配置或只對其進行加法變更，則不會重新建立基本磁碟。 如果下列條件成立，則磁片配置會保持不變：
    -   磁片簽章、磁片樣式 (GPT 或 MBR) 、邏輯磁區大小和磁片區開始位移都不會變更。
    -   磁片區大小不會減少。
    -   若為 GPT 磁片，則不會變更分割區識別碼。
-   如果動態磁碟的磁片配置完好無損，或只對其進行了附加的變更，就不會重新建立動態磁碟。 若要讓動態磁碟保持不變，必須符合基本磁碟的所有條件。 此外，整個磁片套件的磁片區結構必須保持不變。 如果磁片套件符合下列條件（同時適用于 MBR 和 GPT 磁片），則磁片區的磁片區結構會保持不變：
    -   在還原期間，實體套件中可用的磁片區數目，必須大於或等於在備份期間于 ASR 寫入器中繼資料中指定的磁片區數目。
    -   每個磁片區的 [*plex*](../vds/virtual-disk-service-glossary-all.md) 數目必須保持不變。
    -   [*成員*](../vds/virtual-disk-service-glossary-all.md)數目必須保持不變。
    -   實體磁片區的數目必須大於 ASR 寫入器中繼資料中指定的磁片區數目。
    -   當新增其他磁片區，或將套件中的磁片區延伸 (例如，從簡單磁片區到跨距磁片區) 時，不完整的套件會維持不變。
        > [!Note]  
        > 如果簡單磁片區已鏡像，套件就不會完整，並且會重新建立，以確保 BCD 和開機磁碟區狀態在還原之後仍維持一致。 如果刪除磁片區，則會重新建立該套件。

         
-   如果動態磁碟套件的磁片區結構不完整，而且只對其進行了附加的變更，則不會重新建立套件中的磁片。

    **Windows Vista：** 系統一律會重新建立動態磁碟。 請注意，在 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 中，這種行為已有所變更。

在還原階段開始之前的任何時間，要求者可以藉由設定 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** 登錄機碼，來指定磁片應快速格式化。 在此機碼下，有一個名為 **QuickFormat** 的值，其資料類型為 REG \_ DWORD。 如果此值不存在，您應該建立它。 將 **QuickFormat** 值的資料設定為1以進行快速格式化，或設定為0表示慢速格式。

如果 **QuickFormat** 值不存在，磁片的格式會變慢。

快速格式化的速度比慢速格式的速度快很多 (也稱為完整格式) 。 不過，快速格式化不會驗證磁片區上的每個磁區。

## <a name="overview-of-restore-phase-tasks"></a>還原階段工作的總覽

在還原時，要求者會執行下列步驟：

> [!Note]  
> 除非另有指示，否則所有步驟都是必要的。

 

1.  呼叫 [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) 函式來建立 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面的實例，並呼叫 [**>ivssbackupcomponents：： InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) 方法，藉由將要求者的備份元件檔載入至實例，初始化實例以進行還原。
2.  \[只有當要求者需要變更是否為一或多個磁片指定 "IncludeDisk" 或 ">excludedisk.ps1" 時，才需要執行此步驟。 \] 呼叫 [**>ivssbackupcomponents：： SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) 來設定 ASR 寫入器元件的還原選項。 ASR 寫入器支援下列選項：「IncludeDisk」可讓要求者在目標系統上包含要考慮用於還原的磁片，即使在備份階段期間未選取該磁片也是如此。 ">excludedisk.ps1" 可讓要求者防止目標系統上的磁片重新建立。 請注意，如果為包含重要磁片區的磁片指定 ">excludedisk.ps1"，後續對 [**>ivssbackupcomponents：:P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) 的呼叫將會失敗。

    下列範例示範如何使用 [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) 來防止重新建立磁片0和磁片1，並將協力廠商驅動程式插入還原的開機磁碟區中。

    **Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援插入協力廠商驅動程式。

    此範例假設 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 指標 m \_ pBackupComponents 有效。

    ```C++
        m_pBackupComponents->SetRestoreOptions(
            AsrWriterId,
            VSS_CT_FILEGROUP,
            NULL,
            TEXT("ASR"),
            TEXT("\"ExcludeDisk\"=\"0\", \"ExcludeDisk\"=\"1\" "),
            TEXT("\"InjectDrivers\"=\"1\" ")
            );
    ```

    

    若要排除指定磁片區的所有磁片，請參閱下列「排除磁片區的所有磁片」。

3.  呼叫 [**>ivssbackupcomponents：:P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) ，以通知 ASR 寫入器準備進行還原作業。 視需要呼叫 [**IVssAsync：： QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) ，直到 *pHrResult* 參數中傳回的狀態值不是 VSS \_ S \_ 非同步 \_ 暫止。
4.  還原資料。 在還原階段中，ASR 會將磁片區 GUID 路徑重新配置 (\\ \\ ？ \\磁片區 {GUID} ) 每個磁片區，以符合備份階段期間所使用的磁片區 GUID 路徑。 但是，不會保留磁碟機號，因為這會導致與復原環境中自動指派的磁碟機號發生衝突。 因此，當還原資料時，要求者必須使用磁片區 GUID 路徑，而不是磁碟機號，以存取磁片區。
5.  設定 **HKLM** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** 登錄機碼，以指出已還原或重新格式化的磁片區集合。

    在此機碼下，有一個名為 **RestoredVolumes** 的值，其資料類型為 REG \_ 多重 \_ SZ。 如果此值不存在，您應該建立它。 在此值下，您的要求者應該針對已還原的每個磁片區建立磁片區 GUID 專案。 此專案應該採用下列格式： \\ \\ ？ \\磁片區 {78618c8f-aefd-11da-a898-806e6f6e6963}。 每次執行裸機復原時，ASR 都會將 **RestoredVolumes** 值設定為 asr 還原的磁片區集合。 如果要求者已還原其他磁片區，則應該將此值設定為要求者還原之磁片區集的聯集，以及 ASR 還原的磁片區集合。 如果要求者未使用 ASR，則應取代磁片區清單。

    您也應該建立名為 **LastInstance** 的值，其資料類型為 REG \_ SZ。 此索引鍵應該包含可唯一識別目前還原作業的隨機 cookie。 您可以使用 [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) 和 [**UuidToString**](/windows/win32/api/rpcdce/nf-rpcdce-uuidtostring) 函數來建立這類 cookie。 每次執行裸機復原時，ASR 都會重設此登錄值，以通知要求者和非 VSS 備份應用程式已發生復原。

6.  呼叫 [**>ivssbackupcomponents：:P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) 指出還原作業的結束。 視需要呼叫 [**IVssAsync：： QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) ，直到 *pHrResult* 參數中傳回的狀態值不是 VSS \_ S \_ 非同步 \_ 暫止。

在還原階段中，ASR 可能會建立或移除磁碟分割，以將電腦還原為先前的狀態。 要求者不能嘗試將備份階段的磁片編號對應到還原階段。

在還原時，要求者必須排除包含要求者之備份組的磁片。 否則，還原作業可能會覆寫備份組。

還原時，如果在備份期間未將磁片選為元件，或在還原期間以 ">excludedisk.ps1" 選項呼叫 [**>ivssbackupcomponents：： SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) 來明確排除磁片，則會排除該磁片。

請務必注意，在 WinPE 嚴重損壞修復期間，ASR 寫入器功能存在，但沒有其他寫入器可供使用，且 VSS 服務未執行。 在 WinPE 嚴重損壞修復完成之後，電腦就會重新開機，而 Windows 作業系統會正常執行，VSS 服務可以啟動，而且要求者可以執行任何額外的還原作業，而這些作業需要使用 ASR 寫入器以外的寫入器。

如果在還原會話期間，備份應用程式會偵測到磁片區唯一識別碼未變更，因此，從備份時間開始的所有磁片區在 WinPE 中都是不變的，因此備份應用程式可以繼續只復原磁碟區的內容，而不涉及 ASR。 在此情況下，備份應用程式應該會在還原的作業系統中設定下列登錄機碼來指出電腦已還原： **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession**

在此機碼下，指定值名稱的 **LastInstance** 、實 \_ 值型別的 REG SZ，以及隨機的 Cookie (例如 [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate)) 函數針對值資料所建立的 GUID。

如果在還原會話期間，備份應用程式會偵測到一或多個磁片區已變更或遺失，則備份應用程式應該使用 ASR 來執行還原。 ASR 會在備份時以完全相同的方式重新建立磁片區，並設定 **RestoreSession** 登錄機碼。

## <a name="excluding-all-disks-for-a-volume"></a>排除磁片區的所有磁片

下列範例顯示如何排除指定磁片區的所有磁片。


```C++
HRESULT BuildRestoreOptionString
(
    const WCHAR             *pwszVolumeNamePath,
    CMyString               *pstrExclusionList
)
{
    HANDLE                  hVolume           = INVALID_HANDLE_VALUE;
    DWORD                   cbSize            = 0;
    VOLUME_DISK_EXTENTS     * pExtents        = NULL;
    DISK_EXTENT             * pExtent         = NULL;
    ULONG                   i                 = 0;
    BOOL                    fIoRet            = FALSE;
    WCHAR                   wszDest[MAX_PATH] = L"";
    CMyString               strVolumeName;
    CMyString               strRestoreOption;

    // Open a handle to the volume device.
    strVolumeName.Set( pwszVolumeNamePath );
    // If the volume name contains a trailing backslash, remove it.
    strVolumeName.UnTrailing( L'\\' );
    hVolume = ::CreateFile(strVolumeName, 0, FILE_SHARE_READ | FILE_SHARE_WRITE, NULL, OPEN_EXISTING, NULL, 0);
    // Check whether the call to CreateFile succeeded.

    // Get the list of disks used by this volume.
    cbSize = sizeof(VOLUME_DISK_EXTENTS);
    pExtents = (VOLUME_DISK_EXTENTS *)::CoTaskMemAlloc(cbSize);

    ::ZeroMemory(pExtents, cbSize);

    fIoRet = ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
    if ( !fIoRet && GetLastError() == ERROR_MORE_DATA )
    {
        // Allocate more memory.
        cbSize = FIELD_OFFSET(VOLUME_DISK_EXTENTS, Extents) + pExtents->NumberOfDiskExtents * sizeof(DISK_EXTENT);
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;

        pExtents = (VOLUME_DISK_EXTENTS *) ::CoTaskMemAlloc(cbSize);
        // Check whether CoTaskMemAlloc returned an out-of-memory error.
        ::ZeroMemory(pExtents, cbSize);

        // Now the buffer should be big enough.
        ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
        // Check whether the IOCTL succeeded.
    }
    // Check for errors; note that the IOCTL can fail for a reason other than insufficient memory.

    // For each disk, mark it to be excluded in the Restore Option string.
    for (i = 0; i < pExtents->NumberOfDiskExtents; i++)
    {
        pExtent = &pExtents->Extents[i];

        *wszDest = L'\0';
        StringCchPrintf(wszDest, MAX_PATH, L"\"ExcludeDisk\"=\"%d\", ", pExtent->DiskNumber); // check errors

        strRestoreOption.Append(wszDest);
        // Check for an out-of-memory error.
    }

    // Remove the trailing comma.
    strRestoreOption.TrimRight();
    strRestoreOption.UnTrailing(',');

    // Set the output parameter.
    strRestoreOption.Transfer( pstrExclusionList );

Exit:
    if( pExtents )
    {
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;
    }

    if( hVolume != INVALID_HANDLE_VALUE )
    {
        ::CloseHandle(hVolume);
        hVolume = INVALID_HANDLE_VALUE;
    }

    return ( hr );
}

```



 

 
