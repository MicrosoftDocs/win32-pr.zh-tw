---
description: 如同 VSS 下的所有重要作業，增量和差異備份都需要在要求者和寫入器之間密切合作。
ms.assetid: 3cf5dd1f-dc58-42bc-925f-fee7d34053c5
title: 備份複雜存放區的寫入器角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80864256b9a19c25a2f0dce0d0c929ed19fd7269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113152"
---
# <a name="writer-role-in-backing-up-complex-stores"></a>備份複雜存放區的寫入器角色

如同 VSS 下的所有重要作業， [*增量*](vssgloss-i.md) 和 [*差異*](vssgloss-d.md) 備份都需要在要求者和寫入器之間密切合作。

## <a name="backup-types"></a>備份類型

基礎結構提供五種備份類型的特殊支援。 這些步驟的說明如下：

-   Full (**VSS \_ BT \_ 完整**) 。 檔案將會備份，不論其上次備份日期為何。 將會更新每個檔案的備份歷程記錄，而這種類型的備份可作為增量或差異備份的基礎使用。 如果有記錄檔，這些檔案可能會因此備份而被截斷。

    還原完整備份只需要單一備份映射。

-   差異 (**VSS \_ BT \_ 差異**) 。 VSS API 是用來確保只有自上次完整備份後已變更或新增的檔案才會複製到儲存媒體;所有中繼備份資訊都會被忽略。 這可能包括整個檔案，或檔案內的特定範圍。 差異備份會與完整備份相關聯，而且通常在還原完整備份之前無法還原。 如果有記錄檔，則通常不會因為這項備份而被截斷。

    還原差異備份需要原始備份映射，以及自上次完整備份之後所做的最新差異備份映射。

-   增量 (**VSS \_ BT \_ 增量**) 。 VSS API 是用來確保只有在上一次完整或增量備份之後變更或新增的檔案才會複製到儲存媒體中。 這可能包括整個檔案，或檔案內的特定範圍。 有些寫入器不允許將增量備份與差異備份混合使用。 如果有記錄檔，這些檔案可能會因此備份而被截斷。

    還原增量備份需要原始備份映射，以及自初始備份之後所做的所有增量備份映射。

-   記錄備份 (**VSS \_ BT \_ 記錄**) 。 只有寫入器的記錄檔 (使用 [**IVssCreateWriterMetadata：： AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) 方法新增至元件的檔案，並由 [**IVssWMComponent：： GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)) 的呼叫所取出。 這是 VSS 專用的備份類型。 記錄備份的執行頻率通常很高。 一般來說，記錄檔會因為此備份而被截斷。
-    (**VSS \_ BT \_ 複製**) 複本備份。 就像 VSS \_ BT \_ 完整備份類型一樣，會備份檔案，不論其上次備份日期為何。 不過，每個檔案的備份歷程記錄將不會更新，而且這種類型的備份無法當做增量或差異備份的基礎使用。 由於複本備份的結果，記錄檔永遠不會被截斷。

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>部分檔案支援
</dt> <dd>

有些寫入器支援透過覆寫所管理之檔案的部分來還原檔。 要求者可以設計來利用這種方式，如果是，則會藉由設定 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)中的資訊來指出這一點。

</dd> </dl>

寫入器會指出在處理 [*識別*](vssgloss-i.md)事件時呼叫 [**IVssCreateWriterMetadata：： SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)所支援的備份類型。 **IVssCreateWriterMetadata：： SetBackupSchema** 方法的 *dsSchemaMask* 參數是位元遮罩，表示支援的備份類型。 所有寫入器都必須支援完整備份。

<dl> <dt>

<span id="VSS_BS_DIFFERENTIAL"></span><span id="vss_bs_differential"></span>**VSS \_ BS \_ 差異**
</dt> <dd>

表示支援差異備份。

</dd> <dt>

<span id="VSS_BS_INCREMENTAL"></span><span id="vss_bs_incremental"></span>**VSS \_ BS \_ 增量**
</dt> <dd>

表示支援增量備份。

</dd> <dt>

<span id="VSS_BS_LOG"></span><span id="vss_bs_log"></span>**VSS \_ BS \_ 記錄檔**
</dt> <dd>

指出支援記錄備份。

</dd> <dt>

<span id="VSS_BS_COPY"></span><span id="vss_bs_copy"></span>**VSS \_ BS \_ 複製**
</dt> <dd>

表示支援複本備份。

</dd> <dt>

<span id="VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL"></span><span id="vss_bs_exclusive_incremental_differential"></span>**VSS \_ BS \_ 獨佔 \_ 增量 \_ 差異**
</dt> <dd>

指出寫入器不支援混合增量備份與差異備份。

</dd> </dl>

寫入器可以藉由呼叫 [**CVssWriter：： GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)來判斷正在執行哪一種類型的備份。 可以執行此作業的最早點是在處理 PrepareForBackup 事件時。 **CVssWriter：： GetBackupType** 會傳回 [**VSS \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) 列舉的成員。 如果寫入器不支援備份類型，寫入器應該將備份視為完整備份。

## <a name="backup-stamps"></a>備份戳記

增量和差異備份一律會系結至先前的備份。 有兩種方式可以結合備份。 針對簡單的資料存放區，要求者可以追蹤備份之間的相互關聯。 不過，對於更複雜的資料存放區，寫入器必須以備份維護自己的時間戳記;這個時間戳記可能會追蹤記錄位置、檢查點資訊等等。 寫入器會藉由在呼叫 [**IVssCreateWriterMetadata：： SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)時設定 **VSS \_ BS 時間 \_ 戳** 位，來指出它需要自己的時間戳記。

寫入器可以儲存每個要備份的元件的時間戳記。 寫入器會藉由呼叫 [**>ivsscomponent：： SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)，並傳入 *wszBackupStamp* 參數之戳記的字串表示，來儲存時間戳記。 一般而言，寫入器會在處理 [*PostSnapshot*](vssgloss-p.md) 事件時呼叫這個方法。 不過，對於不牽涉到陰影複製的備份，將不會傳送 PostSnapshot 事件。 在此情況下， **>ivsscomponent：： SetBackupStamp** 必須在處理 [*PrepareForBackup*](vssgloss-p.md) 事件時呼叫。

當執行增量或差異備份時，要求者會向寫入器指出先前備份的備份戳記，作為此備份的基底。 寫入器可在處理 PrepareForBackup 或 PostSnapshot 事件時，藉由呼叫 [**>ivsscomponent：： GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)來存取這個先前的備份戳記。 寫入器可以使用傳回的戳記來判斷需要備份的內容。

## <a name="backup-strategies"></a>備份策略

### <a name="file-backup-files-strategies"></a>檔案備份檔策略

通常，只有在執行特定類型的備份時，才需要備份寫入器中繼資料中報告的某些檔案。 某些檔案可能只有在執行完整備份時才需要。 執行增量或差異備份時，可能只需要其他檔案。 VSS 提供一個方法，讓寫入器向要求者指出此資訊。 使用 [**IVssCreateWriterMetadata：： AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)、 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)或 [**IVssCreateWriterMetadata：： AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)將檔案新增至元件時， *dwBackupTypeMask* 參數會指出必須備份這些檔案的備份類型。 遮罩可以包含下列一或多個值：

<dl> <dt>

<span id="VSS_FSBT_FULL_BACKUP_REQUIRED"></span><span id="vss_fsbt_full_backup_required"></span>**VSS \_ FSBT \_ \_ 需要完整備份 \_**
</dt> <dd>

完整備份的必要參數。

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_differential_backup_required"></span>**\_需要 VSS FSBT \_ 差異 \_ 備份 \_**
</dt> <dd>

差異備份的必要參數。

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_incremental_backup_required"></span>**\_需要 VSS FSBT \_ 增量 \_ 備份 \_**
</dt> <dd>

增量備份的必要參數。

</dd> <dt>

<span id="VSS_FSBT_LOG_BACKUP_REQUIRED"></span><span id="vss_fsbt_log_backup_required"></span>**\_需要 VSS FSBT \_ 記錄 \_ 備份 \_**
</dt> <dd>

記錄備份的必要參數。

</dd> <dt>

<span id="VSS_FSBT_ALL_BACKUP_REQUIRED"></span><span id="vss_fsbt_all_backup_required"></span>**VSS \_ FSBT \_ \_ 需要所有備份 \_**
</dt> <dd>

所有備份類型都需要：這是預設值。

</dd> </dl>

此規格會覆寫元件的選擇性規格。 例如，假設有一個元件的檔案已標示為 **需要 vss \_ FSBT \_ 記錄 \_ 備份 \_** ，但不 **需要 vss \_ FSBT \_ 完整 \_ 備份 \_**。 假設無法選取此元件進行備份 (*bSelectable* 在呼叫 [**IVssCreateWriterMetadata：： AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)) 時為 false。 在記錄備份的情況下，這表示此元件中的所有檔案都必須一律進行備份。 不過，在完整備份的情況下，即使元件的選擇性暗示應備份，也不需要備份任何檔案。

### <a name="backup-by-last-modify-time"></a>上次修改時間的備份

寫入器用來指出哪些檔案已變更的其中一種方式，是使用差異的檔案機制。 寫入器可以指定元件中的某些檔案在特定時間之後已經過修改，因此只能備份。 寫入器會呼叫 [**>ivsscomponent：： AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) 與檔案規格和上次修改時間。 **>ivsscomponent：： AddDifferencedFilesByLastModifyTime** 通常會在處理 PostSnapshot 事件時呼叫，雖然它可以在處理 PrepareForBackup 事件時呼叫。 然後，要求者必須備份符合指定時間之後變更之檔案規格的所有檔案。 如果寫入器使用備份戳記機制，則會根據備份檔案中先前的備份戳記來決定上次修改時間。 寫入器也可以在上次修改時間傳入零，這表示要求者須負責判斷上次備份的時間，以及自該時間以來變更的檔案。

### <a name="partial-file-backup"></a>部分檔案備份

寫入器用來表示變更要求者的另一種方式是使用部分檔案機制。 寫入器可以在需要備份的元件檔案內指定位元組範圍;寫入器可能會在處理 PostSnapshot 或 PrepareForBackup 事件時指定這些檔案範圍。 寫入器會呼叫 [**>ivsscomponent：： AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) ，以將部分檔案規格新增至備份。 部分檔案規格包含路徑和檔案名，以及檔案中需要備份之範圍的相關資訊。

### <a name="file-specification-rules"></a>檔案規格規則

[**>ivsscomponent：： AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) 或 [**>ivsscomponent：： AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) 可以用來修改在識別事件期間指定的檔案規格，或將全新的檔案新增至規格。 如果寫入器正在使用 **>ivsscomponent：： AddDifferencedFilesByLastModifyTime** 來修改識別事件期間所設定的資訊，則檔規格必須完全符合目前元件中的其中一個檔案規格。 檔案規格不能部分重迭目前元件中的檔案，而且它不能與任何其他元件中的檔案相符。 不過，使用 **>ivsscomponent：： AddPartialFile** 指定的檔案可以部分重迭另一個檔案規格。 **>ivsscomponent：： AddDifferencedFilesByLastModifyTime** 或 **>ivsscomponent：： AddPartialFile** 設定的資訊會覆寫先前使用 [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)介面來回應識別事件的資訊集。

一般檔案規格可以有替代位置值 (由 [**IVssCreateWriterMetadata：：) AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)的 *WszAlternateLocation* 參數設定，這表示在備份時取得檔案的替代位置。 如果透過差異檔案或部分檔案機制設定的檔案規格符合具有替代位置的現有檔案規格，則備份應用程式將會從這個替代位置取得資料。

如果在 [**>ivsscomponent：： AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) 或 [**>ivsscomponent：： AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) 中設定的檔案規格不相符，且元件中的檔案正在進行備份，則所有相符的檔案現在都會新增至備份中。 請務必小心，寫入器只會在執行此動作時，新增已存在於陰影複製之磁片區上的檔案;否則，要求者可能無法備份這些檔案。 如果在處理 PostSnapshot 事件時呼叫這些函式，您可以使用 [**CVssWriter：： IsPathAffected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispathaffected) 方法來判斷這項功能。 如果在處理 PrepareForBackup 事件時呼叫，寫入器必須使用其他方法進行這項判斷。

### <a name="backup-without-a-shadow-copy"></a>不含陰影複製的備份

某些類型的檔案可能不需要從陰影複製磁片區備份。 例如，這通常會是資料庫記錄檔的值。 由於記錄檔會單純成長，而且寫入器可以使用部分檔案確切地指定要備份的檔案部分，因此通常可能會將記錄備份至原始磁片區。 作為優化，寫入器可以使用 [**IVssCreateWriterMetadata：： AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)、 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)或 [**IVssCreateWriterMetadata：： AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)的 *dwBackupTypeMask* 參數中所設定的旗標，來標示哪些檔案需要不同備份類型的陰影複製。 支援的旗標包含下列各項：

<dl> <dt>

<span id="VSS_FSBT_FULL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_full_snapshot_required"></span>**VSS \_ FSBT \_ \_ 需要完整快照 \_ 集**
</dt> <dd>

完整備份所需的陰影複製。

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_differential_snapshot_required"></span>**\_需要 VSS FSBT \_ 差異 \_ 快照 \_ 集**
</dt> <dd>

差異備份所需的陰影複製。

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_incremental_snapshot_required"></span>**\_需要 VSS FSBT \_ 增量 \_ 快照 \_ 集**
</dt> <dd>

增量備份所需的陰影複製。

</dd> <dt>

<span id="VSS_FSBT_LOG_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_log_snapshot_required"></span>**\_需要 VSS FSBT \_ 記錄 \_ 快照 \_ 集**
</dt> <dd>

記錄備份所需的陰影複製。

</dd> <dt>

<span id="VSS_FSBT_ALL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_all_snapshot_required"></span>**VSS \_ FSBT \_ 需要所有的 \_ 快照 \_ 集**
</dt> <dd>

所有備份類型都需要陰影複製;這是預設值。

</dd> </dl>

如果特定磁片區只包含此備份不需要陰影複製的元件，則要求者可以略過為此磁片區建立陰影複製的步驟。 此磁片區上的所有資料都可以直接從原始磁片區複製到備份媒體中。

## <a name="backup-cleanup"></a>備份清除

如果寫入器需要執行記錄截斷或其他備份後清除，則在處理 [*BackupComplete*](vssgloss-b.md) 事件時要執行此作業的適當位置。 [*BackupShutdown*](vssgloss-b.md)事件會在 BackupComplete 之後傳送一些時間，因此可能也會在 BackupShutdown 事件處理常式中完成一些清除。

BackupShutdown 事件一律會在終止備份之後傳送。 如果在執行備份時，要求者異常終止，則會立即傳送 BackupShutdown，而不需要先傳送 BackupComplete。 如果寫入器需要清除任何狀態，可以在這裡完成;不過，此事件不應該發生記錄截斷，因為備份不一定要完成。

## <a name="restore-strategies"></a>還原策略

在還原時，寫入器的基本工作是確認還原可能會在處理 PreRestore 事件，以及在處理 PostRestore 事件時發生還原。 更複雜的存放區也會在 PostRestore 處理常式中執行復原程式。 如果還原是增量或差異還原的一部分，寫入器通常會想要延遲此復原程式，直到完成所有增量或差異還原為止。 [**>ivsscomponent：： GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) 會指出這是否為此元件的最終還原，或是否有更多的還原。 如果 **>ivsscomponent：： GetAdditionalRestores** 傳回 **true**，寫入器不應該在該元件上執行其復原程式。

## <a name="new-targets"></a>新目標

如果寫入器支援，要求者可以將資料檔案還原到原始備份時間位置以外的位置。 寫入器會在呼叫 [**IVssCreateWriterMetadata：： SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)時，藉由設定 **VSS \_ BS \_ 寫入器 \_ 支援 \_ \_** *dsSchemaMask* 參數中的新目標位，來指出此還原模式的支援。 寫入器會藉由呼叫 [**>ivsscomponent：： GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) 和 [**>ivsscomponent：： GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)，在還原時取得元件檔案的新位置。

## <a name="directed-targets"></a>導向的目標

針對複雜的還原案例，寫入器可能會想要將已備份檔案的範圍對應到相同或不同檔案的不同範圍。 這可以藉由使用導向目的機制來完成。 若要這樣做，寫入器必須先藉由呼叫 [**>ivsscomponent：： SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)，並傳入針對 *目標* 參數 **\_ \_ 導向的 VSS RT** ，來指出這是發生的。 然後，針對每個對應，寫入器會呼叫 [**>ivsscomponent：： AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)。 這個方法會取得備份上原始程式檔的完整路徑，以及要還原至之目的地檔案的完整路徑。 它也會針對每個檔案使用範圍清單。 寫入器會在處理 PreRestore 事件時呼叫這些函式，然後要求者負責將原始程式檔中指定的範圍還原到目的地檔案中的對應範圍。 範圍字串的格式與 [ **>ivsscomponent：： AddPartialFile** 中的格式相同](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)

## <a name="private-writer-metadata"></a>私用寫入器中繼資料

寫入器使用備份來維護私用中繼資料，以正確執行增量或差異還原，通常會很有用。 寫入器可能會在處理 PrepareForBackup 或 PostSnapshot 時，呼叫 [**>ivsscomponent：： SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) 來儲存中繼資料。 藉由呼叫 [**>ivsscomponent：： GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)，寫入器在 PreRestore 或 PostRestore 期間可以存取此中繼資料。 您也可以使用 [**>ivsscomponent：： AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile); 的 *wszMetadata* 參數，以部分檔案規格來儲存中繼資料。此中繼資料可透過 [**>ivsscomponent：： GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)的 *pbstrMetadata* 參數來存取。 寫入器也可以在 [**CVssWriter：： OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore) 和 [**CVssWriter：： OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)之間傳遞中繼資料本身。 在 **CVssWriter：： OnPreRestore** 中，中繼資料是藉由呼叫 [**>ivsscomponent：： SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)來設定。 在 **CVssWriter：： OnPostRestore** 中，藉由呼叫 [**>ivsscomponent：： GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)來取出中繼資料。

-   [VSS 增量和差異備份中的寫入器角色](writer-role-in-vss-incremental-and-differential-backups.md)
-   [VSS 增量和差異備份中的要求者角色](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 



