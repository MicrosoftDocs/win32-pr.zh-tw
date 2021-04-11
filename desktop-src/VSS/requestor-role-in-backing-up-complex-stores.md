---
description: 如同 VSS 下的所有重要作業，增量和差異備份都需要在要求者和寫入器之間密切合作。
ms.assetid: 00391a49-8c81-4518-88a2-741ad5ee4ac3
title: 備份複雜存放區的要求者角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 197351e76b6861ee9b9d1e0589ef028c911430ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026578"
---
# <a name="requester-role-in-backing-up-complex-stores"></a>備份複雜存放區的要求者角色

如同 VSS 下的所有重要作業， [*增量*](vssgloss-i.md) 和 [*差異*](vssgloss-d.md) 備份都需要在要求者和寫入器之間密切合作。

## <a name="backup-type"></a>備份類型

基礎結構提供五種備份類型的特殊支援。 這些步驟的說明如下：

-   Full (**VSS \_ BT \_ 完整**) 。 檔案將會備份，不論其上次備份日期為何。 將會更新每個檔案的備份歷程記錄，而這種類型的備份可作為增量或差異備份的基礎使用。 如果有記錄檔，這些檔案可能會因此備份而被截斷。

    還原完整備份只需要單一備份映射。

-   差異 (**VSS \_ BT \_ 差異**) 。 VSS API 是用來確保只有自上次完整備份後已變更或新增的檔案才會複製到儲存媒體;所有中繼備份資訊都會被忽略。 這可能包括整個檔案，或檔案內的特定範圍。 差異備份會與完整備份相關聯，而且通常在還原完整備份之前無法還原。 如果有記錄檔，則通常不會因為這項備份而被截斷。

    還原差異備份需要原始備份映射，以及自上次完整備份之後所做的最新差異備份映射。

-   增量 (**VSS \_ BT \_ 增量**) 。 VSS API 是用來確保只有在上一次完整或增量備份之後變更或新增的檔案才會複製到儲存媒體中。 這可能包括整個檔案，或檔案內的特定範圍。 有些寫入器不允許將增量備份與差異備份混合使用。 如果有記錄檔，這些檔案可能會因此備份而被截斷。

    還原增量備份需要原始備份映射，以及自初始備份之後所做的所有增量備份映射。

-   記錄備份 (**VSS \_ BT \_ 記錄**) 。 只有寫入器的記錄檔 (使用 [**IVssCreateWriterMetadata：： AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) 方法新增至元件的檔案，並由 [**IVssWMComponent：： GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)) 的呼叫所取出。 這是 VSS 專用的備份類型。 記錄備份的執行頻率通常很高。 一般來說，記錄檔會因為此備份而被截斷。
-    (**VSS \_ BT \_ 複製**) 複本備份。 就像 VSS \_ BT \_ 完整備份類型一樣，會備份檔案，不論其上次備份日期為何。 不過，每個檔案的備份歷程記錄將不會更新，而且這類備份無法當做增量或差異備份的基礎。 由於複本備份的結果，記錄檔永遠不會被截斷。

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>部分檔案支援
</dt> <dd>

有些寫入器支援透過覆寫所管理之檔案的部分來還原檔。 要求者可以設計來利用這種方式，如果是，則會藉由設定 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)中的資訊來指出這一點。

</dd> </dl>

要求者會透過 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)的 *backupType* 參數來指定要執行哪種類型的備份。 不同的寫入器將支援不同類型的備份。 在呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) 之後，要求者可以藉由呼叫 [**IVssExamineWriterMetadata：： GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)，判斷指定的寫入器支援哪些備份類型。 傳回的值是位元遮罩，表示支援不同的備份類型。 **VSS \_BS \_ 差異** 表示支援差異備份、增量備份的 **vss \_ BS \_ 增量** 、記錄備份的 **vss \_ BS \_ 記錄** 檔，以及適用于複本備份的 **vss \_ BS \_ 複製** ; 所有寫入器都必須支援完整備份。 如果寫入器不支援搭配差異備份來混合增量備份，則也會新增 **VSS \_ BS \_ 獨佔 \_ 增量 \_ 差異** 旗標。 如果要求者正在執行增量或差異備份，而指定的寫入器不支援該備份類型，則應該在該寫入器上執行完整備份。

## <a name="backup-stamps"></a>備份戳記

增量和差異備份一律會系結至先前的備份。 有兩種方式可以結合備份。 針對簡單的資料存放區，要求者可以追蹤備份之間的相互關聯。 不過，對於更複雜的資料存放區，寫入器必須以備份維護自己的時間戳記;這個時間戳記可能會追蹤記錄位置、檢查點資訊等等。 要求者可以在 [**IVssExamineWriterMetadata：： GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)傳回的值中檢查 **VSS \_ BS 時間 \_ 戳** 位，以判斷指定的寫入器是否需要儲存自己的時間戳記。

將時間戳記儲存在備份中的寫入器會在處理 >ivssbackupcomponents 時新增時間戳記 [**：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) 或處理 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)時。 要求者可以藉由呼叫 [**>ivsscomponent：： GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)來取得此時間戳記。 執行增量或差異備份時，要求者必須將目前的備份系結至先前的備份。 若要完成此動作，請從先前的特定元件備份取得時間戳記，並將其傳遞至 [**>ivssbackupcomponents：： SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) 函式;這需要針對先前備份中所備份的每個元件進行。

## <a name="backing-up-files"></a>備份檔案

### <a name="backing-up-files-reported-by-writer"></a>備份寫入器所報告的檔

在 GatherWriterMetadata 階段期間，寫入器新增至其中繼資料的每個檔案規格都包含備份類型遮罩，以指定何時應備份檔案。 要求者會藉由呼叫 [**IVssWMFiledesc：： GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)來判斷此遮罩的意義。 此遮罩中的值可用來決定要備份檔案規格的備份類型。 遮罩可以包含下列一或多個位值：

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

[**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)階段中指定的檔案規格資訊，不會提供要求者有關上次備份後已變更之資訊的資訊。 寫入器用來指出變更要求者的其中一種方式，是使用差異的檔案機制。 寫入器可以指定元件中的特定檔案在經過一段時間之後已經過修改，因此應該備份這些檔案;寫入器可以在 [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) 或 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)中指定這些檔案。 要求者可以藉由呼叫 [**>ivsscomponent：： GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) 和 [**>ivsscomponent：： GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)來判斷這些檔案。 如果檔案規格符合 **>ivssbackupcomponents：： GatherWriterMetadata** (中的一個集合，而該集合目前根據備份類型遮罩來有效) 則差異檔案資訊會覆寫先前的資訊;也就是說，只有在指定時間之後修改過檔案規格的檔案時，才會備份這些檔案。 上次修改時間是使用 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構進行通訊。 如果此結構的值為零，則表示最後一次修改的時間應該取決於要求者的上次備份時間記錄。

### <a name="partial-file-backup"></a>部分檔案備份

寫入器用來表示變更要求者的另一種方式是使用部分檔案機制。 寫入器可以在需要備份的元件檔案內指定位元組範圍;寫入器可以在 [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) 或 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)中指定這些檔案範圍。 要求者可以藉由呼叫 [**>ivsscomponent：： GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) 和 [**>ivsscomponent：： GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)來判斷這些檔案。 **>ivsscomponent：： GetPartialFile** 會傳回指向檔案的路徑和檔案名，以及表示需要在檔案中備份的範圍字串。 如同差異檔案，如果路徑和檔案名符合 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)中的寫入器所設定的檔案規格，則部分檔案資訊會覆寫先前的設定。 範圍字串可以有兩種格式：可以直接指定範圍，也可以指定包含範圍資訊的檔案。 如果直接指定範圍，語法會是 offset1： array2d.length1，offset2： array3d.length2 格式的逗號分隔清單，其中每個位移和長度都是64位不帶正負號的整數。 如果指定範圍檔案，則範圍字串應設定為 File = *filename*，其中 *filename* 是範圍檔案的完整路徑。 範圍檔案本身是一種二進位檔案，格式為64位不帶正負號整數的清單。 第一個整數表示檔案中表示的範圍數目。 每個後續的整數配對表示範圍的位移和長度。 要求者也必須負責備份和還原此範圍檔案。

### <a name="file-specification-rules"></a>檔案規格規則

透過差異檔案與部分檔案機制新增的檔案規格，將會修改 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) 中設定的檔案規格，或新增新的檔案。 如果使用部分檔案機制來修改 **>ivssbackupcomponents：： GatherWriterMetadata** 中設定的檔案規格，則要求者可能會預期檔案規格與 **>ivssbackupcomponents：： GatherWriterMetadata** 元件中所設定的其中一個檔案規格完全相符。 檔案規格不會部分重迭另一個檔案規格，而且將不會比對該寫入器元件中任何其他的檔案規格。 不過，使用部分檔案機制新增的檔案規格，可能會部分重迭另一個檔案規格。 若為 true，則差異檔案或部分檔案規格會覆寫 **>ivssbackupcomponents：： GatherWriterMetadata** 中設定的規格。 一般檔案規格可以有 [**IVssWMFiledesc：：) GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) 所傳回的替代位置值 (，這表示在備份時取得檔案的替代位置。 如果透過差異檔案或部分檔案機制設定的檔案規格符合具有替代位置的現有檔案規格，則應該從這個替代位置挑選資料。 如果透過差異檔案或部分檔案機制設定的檔案規格不符合任何現有的元件規格，則這些檔案範圍現在應該會新增至備份中。 要求者可以預期只有已包含在陰影複製集中的磁片區上的檔案，才會使用這些機制的其中一種來新增。

### <a name="backup-without-a-shadow-copy"></a>不含陰影複製的備份

某些類型的檔案可能不需要從陰影複製磁片區備份。 例如，這通常會是資料庫記錄檔的值。 由於記錄檔會單純成長，而且寫入器可以使用部分檔案確切地指定要備份的檔案部分，因此通常可能會將記錄備份至原始磁片區。 作為優化，寫入器可以使用備份類型遮罩來標示哪些檔案需要不同備份類型的陰影複製。 從 [**IVssWMFiledesc：： GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) 傳回的值可以包含下列其中一個或多個位值：

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

## <a name="restoring-files"></a>還原檔案

### <a name="sequential-restores"></a>順序還原

在要求者完成執行還原作業之後，它會將 PostRestore 事件傳送給所有寫入器。 一般而言，寫入器會藉由執行復原或其他還原後作業來處理這個事件。 不過，還原增量備份通常是以一系列的還原作業（每個增量備份一個）來還原。 要求者必須通知寫入器正在進行這類還原，以防止發生復原或其他不想要的作業，直到還原完成為止。 這是藉由呼叫 [**>ivssbackupcomponents：： SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores)來完成。 每個元件都會呼叫這個方法，並向寫入器指出該元件有更多還原。 針對序列中的最後一個還原，必須將額外的還原旗標設為 false (預設值) ，表示這是該元件序列中的最後一個還原。

### <a name="new-targets"></a>新目標

如果寫入器支援，要求者可以將資料檔案還原到原始備份時間位置以外的位置。 要求者可以藉由呼叫 [**IVssExamineWriterMetadata：： GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)來檢查這項支援。 如果寫入器支援此行為，則 **VSS \_ BS \_ 寫入器 \_ 支援 \_ \_** 將會設定新的目標位。 要求者會針對每個重新放置的檔案規格呼叫 [**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) ，以通知寫入器新的位置。 要求者也可以決定將特定範圍的檔案還原至不同的位置。 要求者藉由呼叫 [**>ivssbackupcomponents：： SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)來通知寫入這項變更。

### <a name="directed-targets"></a>導向的目標

針對複雜的還原案例，寫入器可能會想要將已備份檔案的範圍對應到相同或不同檔案的不同範圍。 這可以藉由使用導向的目的機制來完成。 要求者可以藉由呼叫 [**>ivsscomponent：： GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) ，並檢查是否有 **\_ \_ 指向 VSS RT** 的傳回，在 [**>ivssbackupcomponents：:P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)階段之後判斷此機制用於元件。 要求者可以藉由呼叫 [**>ivsscomponent：： GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) 和 [**>ivsscomponent：： GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)，來取得所有這些重新導向的還原。 **>ivsscomponent：： GetDirectedTarget** 會傳回備份上原始程式檔的完整路徑，以及將還原至的目的地檔案的完整路徑。 它也會針對每個檔案傳回範圍清單。 接著，要求者會負責將來源檔案中指定的範圍還原到目的地檔案中的對應範圍。 範圍字串的格式與 [**>ivsscomponent：： GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)中的格式相同。

-   [VSS 增量和差異備份中的寫入器角色](writer-role-in-vss-incremental-and-differential-backups.md)
-   [VSS 增量和差異備份中的要求者角色](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 
