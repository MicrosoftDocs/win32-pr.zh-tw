---
description: 備份元件檔是由 >ivssbackupcomponents 介面的實例所維護。
ms.assetid: 8c7ebba8-58c4-4733-ba59-802abf902c5e
title: 備份元件檔內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c844f2e9e106817c8201822d000c2f6cb94c0fa272bb5b165d98e4cc48b1c21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248338"
---
# <a name="backup-components-document-contents"></a>備份元件檔內容

備份元件檔是由 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面的實例所維護。 此介面也包含許多用來控制備份作業、操作陰影複製，以及查詢系統狀態的方法。 但是，並非所有檔的資訊都可以透過這個介面直接存取。

備份元件檔是由數個資料集所組成：

-   備份或還原作業中明確包含哪些元件的相關資訊
-   預存元件和寫入器資訊的標記法
-   備份/復原操作的相關狀態資訊

雖然要求者和寫入器都可以使用元件資訊，但是只有寫入器可以存取狀態資訊。

## <a name="component-inclusion-information"></a>元件包含資訊

備份元件檔包含由要求者明確包含在備份和還原中的元件清單。 此清單包含下列各項：

-   明確包含可 [*選取的元件*](vssgloss-s.md)。

    在備份作業中包含這些檔案，是由 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 和 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)的 restore 作業所表示。

-   適用于備份子元件的其，沒有可選取的備份元件上階。

    如果要在作業中包含任何寫入器元件，則必須包含所有這些元件。 在備份作業中包含這些檔案，是由 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 和 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)的 restore 作業所表示。

-   隱含新增至備份 ([*子*](vssgloss-s.md) 元件的元件) 可 [*供還原*](vssgloss-s.md) 並明確地新增至還原。

    這些元件可以是可選取的或其，但是具有可選取的上階，用來以隱含方式選取它們進行備份。 [**>Ivssbackupcomponents：： AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)會將它們新增至備份元件檔。

還原中隱含包含的元件身分識別不會儲存在備份元件檔中。

VSS 可以存取元件包含的資訊：在還原或備份中未明確包含任何元件的寫入器，在產生 [*PrepareForBackup*](vssgloss-p.md) 或 [*PreRestore*](vssgloss-p.md) 事件之後，不會收到任何 VSS 事件。

寫入器無法直接查詢此資訊。 這並不是很大的限制，因為依設計，個別的 VSS 寫入器應該不需要有關系統上其他寫入器狀態的詳細資訊，如上面所述，沒有包含元件的系統將不需要參與 VSS 作業。

要求者可以判斷哪些元件已明確包含在作業中。

[**>Ivssbackupcomponents：： GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount)方法會傳回 (儲存在備份元件檔中之元件資訊的寫入器數目，而不是檔) 中的元件數目。

要求者會使用 [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)透過預存寫入器資訊來編制索引，以傳回 [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) 介面的實例。 **IVssWriterComponentsExt** 介面可讓要求者取得參與寫入 [*器的寫入器類別*](vssgloss-w.md)和 [*寫入器實例*](vssgloss-w.md)，以及存取儲存在備份元件檔中之元件的相關資訊。

## <a name="information-on-included-components"></a>內含元件的資訊

備份元件檔表示元件資料 (，其中不包含路徑和檔案規格資訊) ，可透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面的實例來存取。

要求者和寫入器會以不同方式取得 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面實例的存取權。

要求者會使用 [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)所傳回之 [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext)介面的實例，依寫入器檢查寫入器上的元件資料。

除了寫入器識別資訊之外， [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) 介面還提供 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面實例的陣列，每個所選的寫入器包含元件各一個。

如 [備份元件檔生命週期](backup-components-document-life-cycle.md)所述，寫入器可在處理 PrepareForBackup、PrepareForSnapshot、PostSnapshot、BackupComplete、PreRestore 或 PostRestore 事件時，透過 [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) 介面取得相同資訊的存取權。

[**>Ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 可讓寫入器和要求者取得下列資訊：

-   元件的名稱、類型和 [*邏輯路徑*](vssgloss-l.md) ([**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponentname)、 [**GetComponentType**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponenttype)、 [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath)) 
-   如何依照 [*還原目標*](vssgloss-r.md) 的指示還原元件 ([**>ivsscomponent：： GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)) 
-   如果還原檔案時使用替代位置 ([**GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)， [**GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount)) 
-   新的目標資訊，如果有任何 ([**GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)、 [**GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount)) 
-   還原前和還原後的錯誤訊息 ([**GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg)、 [**GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg)) 
-   如果已選取用於定義元件集的可 [*選取的備份*](vssgloss-s.md) 元件 ([**IsSelectedForRestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore)) 
-   備份或還原是否成功 ([**GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)、 [**GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)) 
-   任何可能由 [**>ivssbackupcomponents：： SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) 或 [**>ivssbackupcomponents：： SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) 設定的寫入器特定備份或還原選項， ([**GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)， [**GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)) 
-   任何寫入器專屬的元資料備份或還原中繼資料 ([**GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)) 、 [**GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)) 
-   時間戳記資訊 ([**GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)、 [**GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)) 
-   Restore ([**GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent)， [**GetRestoreSubcomponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount)) 中明確包含之備份子元件的相關資訊

與要求者不同的是，寫入器可以透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面變更備份元件檔中的特定資訊：

-   如何依照還原目標的指示還原元件 ([**>ivsscomponent：： SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)) 
-   寫入器特定的備份和還原中繼資料 ([**>ivsscomponent：： SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)， [**>ivsscomponent：： SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)) 
-   時間戳記資訊 ([**SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)) 
-   還原前和還原後的錯誤訊息 ([**SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)、 [**SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)) 

## <a name="requester-state-information"></a>要求者狀態資訊

要求者會使用 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面，將備份或還原作業的狀態相關資訊插入備份元件檔中。 寫入器應用程式可以透過 [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) 類別來查詢這類資訊。

儲存在備份元件檔中的狀態資訊包括下列各項：

備份的一般資訊

-   整體備份類型 (增量、差異或完整) <dl> <dt>

由要求者使用 [ **>ivssbackupcomponents：： SetBackupState** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

由寫入器使用 [ **CVssWriter：： GetBackupType** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)
</dt> </dl>
-   Whether component operations are supported<dl> <dt>

由要求者使用 [ **>ivssbackupcomponents：： SetBackupState** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

由寫入器使用 [ **CVssWriter：： AreComponentsSelected** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)
</dt> </dl>
-   Whether the bootable system state is backed up<dl> <dt>

由要求者使用 [ **>ivssbackupcomponents：： SetBackupState** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

由寫入器使用 [ **CVssWriter：： IsBootableStateBackedUp** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)
</dt> </dl>
-   Whether partial file operations are supported<dl> <dt>

由要求者使用 [ **>ivssbackupcomponents：： SetBackupState** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

由寫入器使用 [ **CVssWriter：： IsPartialFileSupportEnabled** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)
</dt> </dl>

有關還原的一般資訊

-   整體還原類型 (還原是透過複製或匯入) <dl> <dt>

由要求者使用 [ **>ivssbackupcomponents：： SetRestoreState** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)
</dt> <dt>

由寫入器使用 [ **CVssWriter：： GetRestoreType** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)
</dt> </dl>

支援檔案的相關資訊

-   特定元件在部分檔案作業中使用的範圍檔案位置<dl> <dt>

由要求者使用 [ **>ivssbackupcomponents：： SetRangesFilePath** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)
</dt> <dt>

由寫入器 (或要求者) 使用 [ **>ivsscomponent：： GetPartialFile** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)
</dt> </dl>

資訊的狀態

-   指出是否已成功備份其中一個指定的寫入器元件<dl> <dt>

由要求者使用 [ **>ivssbackupcomponents：： SetBackupSucceeded** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)
</dt> <dt>

由寫入器和要求者使用 [ **>ivsscomponent：： GetBackupSucceeded** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)
</dt> </dl>
-   Indicate whether one of a given writer's components was successfully restored<dl> <dt>

由要求者使用 [ **>ivssbackupcomponents：： SetFileRestoreStatus** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)
</dt> <dt>

由寫入器和要求者使用 [ **>ivsscomponent：： GetFileRestoreStatus** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)
</dt> </dl>

Writer-Settable 資訊

-   其中一個指定的寫入器元件的其他備份規格<dl> <dt>

由使用 [ **>ivsscomponent：： SetBackupMetadata** 的寫入器設定](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)
</dt> <dt>

由寫入器和要求者使用 [ **>ivsscomponent：： GetBackupMetadata** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)
</dt> </dl>
-   Additional restore specification for one of a given writer's components<dl> <dt>

由使用 [ **>ivsscomponent：： SetRestoreMetadata** 的寫入器設定](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)
</dt> <dt>

由寫入器和要求者使用 [ **>ivsscomponent：： GetRestoreMetadata** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the current backup of one of its component's backups<dl> <dt>

由使用 [ **>ivsscomponent：： SetBackupStamp** 的寫入器設定](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)
</dt> <dt>

由寫入器和要求者使用 [ **>ivsscomponent：： GetBackupStamp** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the last backup of one of its components' backups using a backup stamp initially set by <a href="/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp">>ivsscomponent：： SetBackupStamp</a><dl> <dt>

使用 [ **>ivssbackupcomponents：： SetPreviousBackupStamp** ，由要求者儲存並設定特定元件的要求者](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)
</dt> <dt>

由寫入器和要求者使用 [ **>ivsscomponent：： GetPreviousBackupStamp** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)
</dt> </dl>
-   Error messages for failure before and after restore operations<dl> <dt>

由使用 [**>ivsscomponent：： SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)或 [**>ivsscomponent：： SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)的寫入器設定
</dt> <dt>

由寫入器和要求者使用 [**>ivsscomponent：： GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg)或 [**>ivsscomponent：： GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg)抓取
</dt> </dl>

 

 
