---
description: 寫入器參與增量和差異備份時，通常會在處理 (CVssWriter：： OnIdentify) 、PrepareForBackup (CVssWriter： OnPrepareBackup) 和 PostSnapshot (CVssWriter： OnPostSnapshot) 事件時進行。
ms.assetid: 85c4e003-b531-4283-83aa-dd5cc53f35b1
title: VSS 增量和差異備份中的寫入器角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3c84245c21a47ba5535eccdfcbf10e988cf72b30ea99ee92086a9ca8f65647
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863868"
---
# <a name="writer-role-in-vss-incremental-and-differential-backups"></a>VSS 增量和差異備份中的寫入器角色

寫入器參與增量和差異備份時，通常會 [*在處理 (*](vssgloss-i.md) [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) 、 [*PrepareForBackup*](vssgloss-p.md) ([**CVssWriter： OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)) 和 *PostSnapshot* ([**CVssWriter： OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) 事件時進行。 寫入器的參與方式取決於它是否支援備份戳記和上次修改時間，以及執行備份的要求者是否支援 [*部分檔案作業*](vssgloss-p.md)。

## <a name="handling-identify-events-during-incremental-and-differential-backups"></a>處理增量和差異備份期間的識別事件

在處理識別事件時，寫入器會透過備份架構 ([**vss \_ 備份 \_ 架構**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)) 和檔案規格備份類型 ([**vss 檔案 \_ \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) 遮罩，來建立增量和差異備份作業的基本架構。

寫入器會藉由建立 [**VSS \_ 備份 \_ 架構**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) 值的位遮罩，並將其傳遞至 [**IVssCreateWriterMetadata：： SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) 方法，來指出它在寫入器元資料檔案中支援的作業。 藉此，寫入器可以指出它是否支援下列各項：

-   增量備份 (**VSS \_ BS \_ 增量**) 
-    (**VSS \_ BS \_ 差異**) 的差異備份
-   增量和差異備份無法混合 (**VSS \_ BS \_ 專有 \_ 增量 \_ 差異**) 
-   使用備份戳記 (**VSS \_ BS 時間 \_ 戳**) 的增量和差異備份
-   以檔案上次修改的相關資訊為基礎的增量和差異備份 (**VSS \_ BS \_ 上次 \_ 修改**) 

寫入器會使用檔案規格備份類型遮罩來提供檔案集層級資訊給要求者，以說明如何在增量或差異備份中包含檔案。

當寫入器將檔案集新增至元件時，可以藉由建立「 [**VSS 檔案 \_ 規格」 \_ \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) 值的位元遮罩，然後將它傳遞給 [**IVssCreateWriterMetadata：： AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)、 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)或 [**IVssCreateWriterMetadata：： AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)，來設定檔案集的檔案規格備份類型遮罩。

[**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)列舉有三個「需要備份」值，會影響差異和增量備份：

-   **VSS \_ FSBT \_ \_ 需要所有備份 \_**
-   **\_需要 VSS FSBT \_ 增量 \_ 備份 \_**
-   **\_需要 VSS FSBT \_ 差異 \_ 備份 \_**

有三個「需要陰影複製」值：

-   **VSS \_ FSBT \_ 需要所有的 \_ 快照 \_ 集**
-   **\_需要 VSS FSBT \_ 增量 \_ 快照 \_ 集**
-   **\_需要 VSS FSBT \_ 差異 \_ 快照 \_ 集**

標記檔案規格備份類型為「需要陰影複製」的檔案集，指出當執行增量、差異或所有 (（包括累加和差異作業) 備份作業）時，要求者是否需要從陰影複製複製資料。

套用至累加式、差異或所有備份作業的「需要備份」旗標，表示寫入器預期在還原任何備份作業之後，可以使用目前版本的檔案集。 一般而言，這表示如果檔案集標記為「需要備份」，則在增量或差異備份期間，其所有成員都會複製到備份媒體，而不論其備份或修改何時上次發生。

依預設，會將檔案集新增至具有 vss 的檔案規格備份類型的元件 **\_ FSBT \_ 所有 \_ \_** 需要的備份 \| **vss \_ FSBT \_ \_ \_ 需要所有的快照** 集。 因此，除非寫入器開發人員決定不使用預設 (藉由選擇其他檔案規格備份類型、使用部分檔案作業，或使用差異檔案) ，否則大部分檔集中的檔案通常會複製到備份媒體中。

此時，寫入器的寫入器元資料檔案完全填入了要求者啟動差異或增量備份所需的大部分資訊。 在 [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) 事件期間，將會處理用來支援備份的檔案集或檔案層級資訊的額外規格。

## <a name="handling-prepareforbackup-events-during-incremental-and-differential-backups"></a>在累加式和差異備份期間處理 PrepareForBackup 事件

在要求者繼續進行實際的備份作業之前，寫入器可以透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)介面改變要求者的備份元件檔，以修改 [*增量*](vssgloss-i.md)或 [*差異*](vssgloss-d.md)備份的規格。

因為寫入器會使用 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面，所以它們通常會在處理 [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) 事件時執行這些準備工作。

在 [**CVssWriter： OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)中，寫入器可以更精確地指定要如何評估某些檔案以進行備份、指定備份時應該使用哪些機制，以及可能設定備份戳記。

<dl> <dt>

<span id="Partial_Files"></span><span id="partial_files"></span><span id="PARTIAL_FILES"></span>部分檔案
</dt> <dd>

如果要求者支援它們，寫入器可以選擇使用部分檔案作業來實作為增量或差異備份。  (寫入器可以藉由呼叫 [**CVssWriter：： IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)來判斷要求者是否支援部分檔案作業。 ) 

寫入器會使用 [**>ivsscomponent：： AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) 來指出要在增量或差異作業期間備份所選檔案的部分。 要求者必須遵守此規格，而且一定要備份檔案的指定區段。  (如需部分檔案作業的詳細資訊，請參閱 [使用部分](working-with-partial-files.md) 檔案。 ) 

藉由使用 [**>ivsscomponent：： AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)，寫入器可以將檔案加入至先前尚未新增至其中一個元件集的備份， (由 [**IVssCreateWriterMetadata：： AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)、 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)或 [**IVssCreateWriterMetadata：： AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) 為部分檔案。 以這種方式新增至備份的任何新檔案，都必須在已為此備份進行陰影複製的磁片區上。

如果檔案牽涉到部分檔案作業，這會取代任何已忽略的檔案規格備份類型。

</dd> <dt>

<span id="Differenced_Files"></span><span id="differenced_files"></span><span id="DIFFERENCED_FILES"></span>差異檔案
</dt> <dd>

支援上次修改的備份架構 (**VSS \_ BS \_ 架構**) 的寫入器可以將 [*差異*](vssgloss-d.md) 檔案新增至增量或差異備份。

在指定差異檔案時，寫入器會使用 [**>ivsscomponent：： AddDifferencedFileByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) ，並指定路徑、檔案名和遞迴旗標，但不需要符合任何元件中包含的檔案集。

事實上，寫入器可以將先前未加入的檔案新增至其中一個元件集， ([**IVssCreateWriterMetadata：： AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)、 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)或 [**IVssCreateWriterMetadata：： AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) 備份為差異檔案。 以這種方式新增至備份的任何新檔案，都必須在已為此備份進行陰影複製的磁片區上。

一般而言，寫入器也會在加入差異檔案時，指定上次修改的時間，以編寫器自己的歷程記錄機制為基礎。 上次修改時間（如果有指定）必須一律由要求者用來判斷檔案是否需要包含在增量或差異備份中。

將差異檔案新增至增量或差異備份集時，寫入器可能會選擇不指定上次修改時間。 如果是這種情況，要求者可以自由使用自己的機制（例如，先前的備份或檔案系統資訊的記錄）來判斷差異檔案是否應該包含在增量或差異備份中。

任何差異檔案的檔案規格備份類型都會被忽略。

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>備份戳記
</dt> <dd>

支援備份戳記的寫入器 (**VSS \_ BS \_ 時間戳記**) 有自己的私用格式，可用於儲存上次備份時的相關資訊。 這項資訊是由寫入器在備份期間產生的。

備份戳記會以字串的形式儲存在備份元件檔中，並以 [**>ivsscomponent：： SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) 方法作為字串。 備份戳記會套用至元件 (或元件集中的所有檔集，) 對應至 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)的實例。

如果要求者可以存取先前備份的備份戳記，它就會藉由呼叫 [**>ivssbackupcomponents：： SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)，將其提供給寫入器。

然後，寫入器可以使用 [**>ivsscomponent：： GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)檢查這個時間戳記。

請注意，要求者只會儲存並傳回包含備份戳記的字串。 它並不知道字串格式或使用方式的任何資訊;只有寫入器具有該資訊。

寫入器在呼叫 [**>ivsscomponent：： GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)之後，可能會選擇使用 [**>ivsscomponent：： SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)來更新目前的備份戳記，因此會以其本身的格式記錄目前增量或差異備份作業的日期。

</dd> </dl>

 

 



