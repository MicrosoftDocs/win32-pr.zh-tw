---
description: 若要支援增量或差異備份作業，要求者必須執行下列操作：
ms.assetid: a77700e3-8217-460e-bec9-1041d03eec41
title: VSS 增量和差異備份中的要求者角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637d4bf97b97d484080c85a2345599a05e4bbd89f88a0c1786b5bda911a83331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122003"
---
# <a name="requester-role-in-vss-incremental-and-differential-backups"></a>VSS 增量和差異備份中的要求者角色

若要支援 [*增量*](vssgloss-i.md) 或 [*差異*](vssgloss-d.md) 備份作業，要求者必須執行下列操作：

1.  判斷 (使用 [**>ivssbackupcomponents：： GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) 來取得寫入器元資料檔案中資訊的存取權，以判斷支援的寫入器支援程度) —特別是決定 ([**VSS \_ 備份 \_ 架構**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)) 支援的備份架構。
2.  設定適當的備份狀態。
3.  取得增量或差異備份的檔案和檔案集層級規格。
4.  執行備份。

## <a name="requester-determination-of-incremental-and-differential-support-and-configuration"></a>要求者判斷增量和差異支援和設定

要求者在選取要包含在增量或差異備份中的元件之前，必須先取得寫入器支援的相關資訊，或是設定其本身的狀態。

<dl> <dt>

<span id="Determining_Writer_Support"></span><span id="determining_writer_support"></span><span id="DETERMINING_WRITER_SUPPORT"></span>判斷寫入器支援
</dt> <dd>

要求者會使用 [**IVssExamineWriterMetadata：： GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema) 方法來取得寫入器的備份架構遮罩，以判斷指定的寫入器是否支援 VSS 增量或差異備份。

支援 VSS 增量或差異技術之寫入器的備份架構遮罩，將包含 **vss \_ BS \_ 增量** 或 **vss \_ BS \_ 差異**，或兩者都包含。 寫入者也可以使用 **VSS \_ BS \_ 獨佔 \_ 增量 \_ 差異** 旗標來表示其參與的限制。 如需有關備份架構) 的詳細資訊， (參閱 [**VSS \_ 備份 \_ 架構**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) 。

</dd> <dt>

<span id="Setting_Requester_Backup_State"></span><span id="setting_requester_backup_state"></span><span id="SETTING_REQUESTER_BACKUP_STATE"></span>設定要求者備份狀態
</dt> <dd>

要求者表示備份是增量或差異備份，方法是在產生 [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)事件之前，使用 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)方法將備份類型設定為 **vss \_ bt \_ 增量** 或 **vss \_ bt \_ 差異**。

[**>Ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)方法也用來指出要求者是否提供部分檔案 [*支援*](vssgloss-p.md)，這通常用來執行特定的增量備份和還原作業。

</dd> </dl>

## <a name="getting-writer-specifications-for-incremental-and-differential-backups"></a>取得增量和差異備份的寫入器規格

[**>Ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)成功傳回之後，每個寫入器的寫入器元資料檔案中包含的檔案集層級檔案備份規格資訊 ([**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) 可供檢查。

不過，寫入器可以加入 [*差異*](vssgloss-d.md) 檔案，或要求 [*部分檔案支援*](vssgloss-p.md) ，直到其成功處理 [*PostSnapshot*](vssgloss-p.md) 事件為止。

差異檔案與部分檔案支援規格可以覆寫檔案規格備份類型，因此，要求者可能會想要在成功傳回 >ivssbackupcomponents 之後，延遲對增量和差異備份的所有寫入器規格的完整分析 [**：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)。

<dl> <dt>

<span id="Getting_File_Backup_Specification_Information"></span><span id="getting_file_backup_specification_information"></span><span id="GETTING_FILE_BACKUP_SPECIFICATION_INFORMATION"></span>取得檔案備份規格資訊
</dt> <dd>

每個寫入器的寫入器元資料檔案中都包含檔案集層級檔案備份規格資訊 ([**VSS 檔案 \_ \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) ，而且可以在成功傳回 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)之後立即檢查。

要求者必須針對每個寫入器元件的每個檔案集，取得檔案備份規格遮罩 ([**VSS 檔案 \_ \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) ，以納入增量或差異備份，不論元件是 [*明確*](vssgloss-e.md) 或 [*隱含*](vssgloss-i.md) 的包含。

要求者可以使用 [**>ivssbackupcomponents：： GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) 和 [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)，判斷必須查詢的寫入器元資料檔案。 由 **>ivssbackupcomponents：： GetWriterComponents** 傳回的 [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext)介面實例會透過 [**IVssWriterComponentsExt：： GetWriterInfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo)方法提供寫入器資訊。

要求者會使用 [**IVssExamineWriterMetadata：： GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent)，透過 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)介面的實例取得元件資訊，該介面對應于由指定寫入器所管理的包含元件。

您可以呼叫 [**IVssWMComponent：： GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile)、 [**IVssWMComponent：： GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)或 [**IVssWMComponent：： GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) (，以適當的) 來取得與 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)介面對應的元件所管理之檔案集的相關資訊。

這些呼叫可以針對元件的每個檔案集傳回 [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) 介面的實例。

藉由呼叫 [**IVssWMFiledesc：： GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)，即可取得檔集的檔案規格備份類型。

</dd> <dt>

<span id="Getting_Partial_File_and_Differenced_File_Information"></span><span id="getting_partial_file_and_differenced_file_information"></span><span id="GETTING_PARTIAL_FILE_AND_DIFFERENCED_FILE_INFORMATION"></span>取得部分檔案和差異檔案資訊
</dt> <dd>

要求者會透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面取得部分檔案和差異檔案資訊。

要求者可以使用 [**>ivssbackupcomponents：： GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) 和 [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)來反復查看備份中包含的所有寫入器。

由 [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)傳回之 [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext)介面的實例，可讓您透過 [**IVssWriterComponentsExt：： GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent)和 [**IVssWriterComponentsExt：： GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount)方法，存取對應至指定寫入器 [*明確包含*](vssgloss-e.md)之元件的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)介面的所有實例。

要求者必須針對其架構支援增量或差異備份的所有寫入器（也就是 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) [**：： GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)所傳回的備份架構遮罩）包括 vss BS 增量（當備份類型是 **vss \_ BT \_ 增量** 時）包含 **vss \_ \_ 增量**，或備份類型為 **vss \_ BS \_ 差異** 時的 **vss \_ BS \_ 差異**。

部分檔案資訊的取得方式是呼叫 [**>ivsscomponent：： GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) 和 [**>ivsscomponent：： GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) (參閱 [使用部分](working-with-partial-files.md) 檔案) 。

針對根據檔案的上次修改資料來支援備份作業的寫入器 (寫入器， [**IVssExamineWriterMetadata：： GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)所傳回的備份架構遮罩包含 **VSS \_ BS \_ 上次 \_ 修改**) ，藉由呼叫 [**>ivsscomponent：： GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) 和 [**>ivsscomponent：： GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)來取得差異檔案資訊。

請注意，差異檔案可能是新的檔案（也就是，不是目前在指定寫入器寫入器元資料檔案中之任何檔案集的成員）。

要求者不應找到部分檔案作業和檔案差異檔案中包含的檔案。 如果要求者遇到這類情況，則應該傳回並記錄寫入器錯誤。

要求者仍可能選擇繼續備份有問題的寫入器檔案，但在這種情況下，應該根據差異檔案資訊中找到的規格來進行。

</dd> </dl>

## <a name="implementing-incremental-or-differential-backups"></a>執行增量或差異備份

在執行備份之前，要求者應該有哪些寫入器支援 [*增量*](vssgloss-i.md) 或 [*差異*](vssgloss-d.md) 備份、所有要求的部分檔案作業、所有差異檔案，以及所有其他檔案的檔案規格備份類型的相關資訊。

<dl> <dt>

<span id="Nonsupporting_Writers"></span><span id="nonsupporting_writers"></span><span id="NONSUPPORTING_WRITERS"></span>Nonsupporting 寫入器
</dt> <dd>

如果寫入器的架構不支援增量或差異備份 (寫入器，而這些寫入器的備份架構遮罩（由 [**IVssExamineWriterMetadata：： GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)傳回）則在備份類型為 vss BT 增量或未包含 vss BS 差異時，備份類型是 vss **\_ BT \_ 增量** 或不包含 **vss \_ \_ 差異** 時，備份類型為 **vss \_ BS \_ 差異**) 無法對增量或差異備份作業提供直接支援。 **\_ \_**

這不一定表示寫入器的資料將不會包含在增量或差異備份作業中。 不過，要做的選擇是由要求者自行決定。 要求者可以執行下列任何一項動作：

-   備份任何屬於 nonsupporting 寫入器的檔案 (清楚地向使用者指出這一點) 
-   備份 nonsupporting 寫入器的所有檔案
-   使用檔案系統資料和要求者自己的歷程記錄記錄，執行增量備份。

最後一個替代方法應該謹慎使用，而且只有當要求者瞭解所涉及的寫入器是否可以支援增量或差異備份，以及還原與 VSS 機制無關的資料時。

</dd> <dt>

<span id="Supporting_Writers"></span><span id="supporting_writers"></span><span id="SUPPORTING_WRITERS"></span>支援的寫入器
</dt> <dd>

要求者必須處理 (，以) 所有寫入器的 [*差異*](vssgloss-d.md)檔案，然後處理任何 [*部分*](vssgloss-p.md) 檔案要求，然後根據檔案規格備份類型 ([**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) ，來備份剩餘的檔案。

1.  **備份差異檔案：**

    針對根據上次修改資料來支援備份作業的寫入器 (寫入器， [**IVssExamineWriterMetadata：： GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)傳回的寫入器包含 **VSS \_ BS \_ 上次 \_ 修改**) ，要求者使用 [**>ivsscomponent：： GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) 所傳回的路徑、檔案規格和遞迴旗標資訊，將檔案清單產生為增量備份或還原的候選項目。

    [**>Ivsscomponent：： GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) 也可以傳回上次修改的時間 (以 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構) 表示。

    如果寫入器提供的最後一項修改時間為非零值，則要求者會使用它做為基礎 (而不是檔案系統資訊或要求者自己的儲存資料) ，以判斷檔案是否應該包含在 [*增量*](vssgloss-i.md) 或 [*差異*](vssgloss-d.md) 備份中。

    比方說，如果寫入器傳回的檔案上次修改時間為：

    -   在上一次完整備份之後，檔案應該包含在累加式和差異備份中。
    -   在上一次完整備份之後，但在最後一次增量備份之前，檔案應該包含在增量備份作業中，而不是差異備份。

    如果寫入器提供的最後修改時間為零，則要求者必須使用檔案系統資訊及其本身儲存的資料，來判斷差異檔案的修改時間。

2.  **使用部分檔案作業：**

    如果寫入器要求使用部分檔案作業來備份檔案，要求者會使用檔案位移資訊，將指定的檔案區段儲存至備份媒體。  (如需部分檔案作業的詳細資訊，請參閱 [使用部分](working-with-partial-files.md) 檔案) 。

    如上面所述，寫入器不應將檔案指定為差異檔案，並在部分檔案作業中指定為參與者。 如果要求者遇到這類情況，則應該傳回並記錄寫入器錯誤。

    要求者仍可能選擇繼續備份有問題的寫入器檔案，但在這種情況下，應該根據差異檔案資訊中找到的規格來進行。

3.  **使用檔案規格備份類型：**

    處理完所有差異檔案與部分檔案作業之後，要求者現在會根據其檔案規格備份類型（ ([**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) ）來處理其備份組中的所有剩餘檔案。

    [**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)列舉有三個「需要備份」值，會影響差異和增量備份：

    -   VSS \_ FSBT \_ \_ 需要所有備份 \_
    -   \_需要 VSS FSBT \_ 增量 \_ 備份 \_
    -   \_需要 VSS FSBT \_ 差異 \_ 備份 \_

    有三個「需要陰影複製」值：

    -   VSS \_ FSBT \_ 需要所有的 \_ 快照 \_ 集
    -   \_需要 VSS FSBT \_ 增量 \_ 快照 \_ 集
    -   \_需要 VSS FSBT \_ 差異 \_ 快照 \_ 集

    標記檔案規格備份類型為「需要陰影複製」的檔案集，表示要求者在執行累加、差異或所有 (（包括累加和差異作業) 備份作業）時，必須從陰影複製複製資料。

    套用至累加式、差異或所有備份作業的「需要備份」旗標，表示寫入器預期在還原任何備份作業之後，可以使用目前版本的檔案集。 一般而言，這表示如果檔案集標記為「需要備份」，要求者會在增量或差異備份期間，將其所有成員複製到備份媒體，而不考慮其備份或修改上次發生的時間。

    依預設，會將檔案集新增至具有 VSS 的檔案規格備份類型的元件 \_ FSBT 所有需要的 \_ \_ 備份 \_ \| vss \_ FSBT \_ \_ 需要所有的快照集 \_ 。 因此，除非寫入器明確地設定檔案規格備份類型，否則要求者必須複製未由部分檔案工作處理的檔案，或大部分檔案集中指定的差異檔案，通常會完整地複製到備份媒體中。

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>備份戳記
</dt> <dd>

支援備份戳記 (VSS \_ BS \_ 時間戳記) 的寫入器可能會選擇產生用來支援未來增量和差異備份和還原作業的備份戳記資訊。

包含在包含備份戳記資訊之字串中的格式和資訊，對產生它們的寫入器而言是私用的。要求者不知道如何處理此資訊。

支援的寫入器會使用 [**>ivsscomponent：： SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) 方法，將備份元件檔中的備份戳記儲存為字串。

要求者處理備份戳記資訊的角色是 (如果) 存在，則在未來的備份或還原作業中呼叫 [**>ivssbackupcomponents：： SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) ，將其提供給寫入器。

</dd> </dl>

 

 
