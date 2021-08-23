---
description: VSS 下的備份前工作著重于建立包含備份資料之磁片區的陰影複製。
ms.assetid: e6b082af-719b-4426-8217-0fc940f5884d
title: 備份前工作總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af8dd6ea99215d486b8be7d07d30bcbdb5258548078fd642028dd6a93ca42796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511738"
---
# <a name="overview-of-pre-backup-tasks"></a>備份前工作總覽

VSS 下的備份前工作著重于建立包含備份資料之磁片區的陰影複製。 備份應用程式會儲存來自陰影複製的資料，而不是實際磁碟區。 如需詳細資訊，請參閱 [在 VSS 下處理備份的總覽](overview-of-processing-a-backup-under-vss.md)。

要求者通常會等待寫入器準備備份並建立陰影複製。 寫入器必須判斷它是否要參與備份，如果是的話，請設定它的檔案，並準備好進行備份和陰影複製。 下表顯示針對備份作業進行準備所需的動作和事件順序。



| 要求者動作                                                                                                                                                                                                                                                                                                            | 事件                                                                      | 寫入器動作                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 要求者可以設定備份選項 (請參閱 [**>ivssbackupcomponents：： SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions))                                                                                                                                                                                           | 無                                                                       | 無                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 藉由檢查任何儲存的備份戳記來支援增量和差異備份作業 (請參閱 [**>ivsscomponent：： GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)， [**>ivssbackupcomponents：： SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp))                                                | 無                                                                       | 無                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 使用 [ **>ivssbackupcomponents：:P repareforbackup** 通知寫入器準備備份作業](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)                                                                                                                                                                              | [*PrepareForBackup*](vssgloss-p.md)  | 寫入器準備工作包括判斷要備份的檔案、寫入器是否會參與陰影複製凍結，以及建立寫入器專屬的中繼資料 (請參閱 [**CVssWriter：： OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)、 [**CVssWriter：： IsPathAffected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispathaffected)、 [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents)、 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)、 [**>ivsscomponent：： GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)、 [**CVssWriter：： AreComponentsSelected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)、 [**>ivsscomponent：： SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)和 [**>ivsscomponent：： GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)。 |
| 要求者會等待寫入器使用 [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)來設定備份。 它也應該驗證寫入器狀態 (請參閱 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus)， [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus))      | 無                                                                       | 無                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 要求者會使用 >ivssbackupcomponents 來要求陰影複製 [ **：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)                                                                                                                                                                                                    | 無                                                                       | 無                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 無                                                                                                                                                                                                                                                                                                                        | [*PrepareForSnapshot*](vssgloss-p.md) | [**CVssWriter：： OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot)：讓寫入器進入「陰影複製就緒」狀態。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 無                                                                                                                                                                                                                                                                                                                        | [*凍結*](vssgloss-f.md)                      | [**CVssWriter：： OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)：陰影複製之前的最終設定。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 無                                                                                                                                                                                                                                                                                                                        | [*解凍*](vssgloss-t.md)                          | [**CVssWriter：： OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)：正常運作 (包括 i/o) 可繼續。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 無                                                                                                                                                                                                                                                                                                                        | [*PostSnapshot*](vssgloss-p.md)          | [**CVssWriter：： OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)：陰影複製準備的最終清除。 請參閱 [**>ivsscomponent：： AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) 和 [**>ivsscomponent：： SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 要求者會使用： [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)來等候陰影複製完成，它也應該驗證寫入器狀態 (請參閱 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus)、 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)<br/> | 無                                                                       | 無                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

## <a name="requester-pre-backup-tasks"></a>要求者備份前工作

此外，在建立 [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) 事件之前，要求者也可以使用 [**>ivssbackupcomponents：： SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) 來設定個別寫入器的備份選項，視每個寫入器的細節和要求者是否知道這些寫入器而定。

為了支援累加和差異作業，現在可能會選擇使用 [**>ivsscomponent：： GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp) 來檢查先前備份作業的時間戳記的元件 (使用：：) ，並使用該資訊來設定寫入器的先前時間戳記，以使用 [**>ivssbackupcomponents：： SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)) 處理 (。 如需詳細資訊，請參閱 [增量和差異備份](incremental-and-differential-backups.md) 。

要求者現在可以導向系統的寫入器來完成備份前準備工作，以及處理陰影複製的建立。

首先，要求者會藉由呼叫 [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)來產生 [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)事件。

在所有參與的寫入器都從 [**處理 PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)事件之後，要求者藉由使用 **PrepareForBackup**) 所傳回之 [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)介面的實例來判斷事件 (，要求者可以藉由呼叫 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)來起始陰影複製，如此一來，就會為寫入器產生 [*PrepareForSnapshot*](vssgloss-p.md)、[*凍結*](vssgloss-f.md)、[*解凍*](vssgloss-t.md)和 [*PostSnapshot*](vssgloss-p.md)事件，以供寫入器處理。

在某些情況下，要求者可能不需要建立陰影複製。 具體而言，由其中一個指定的寫入器元件所管理的每個 [*檔案都有*](vssgloss-f.md)一個檔案規格備份遮罩， (在 [*識別*](vssgloss-i.md)事件期間) 設定的 [**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)值的位 or 表示。 這個遮罩除了會指定檔案集是否需要在執行備份之前，先將系統陰影複製。

如果任何磁片區上都沒有要備份的檔案，則需要有陰影複製，否則不需要呼叫 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 。

## <a name="writer-pre-backup-tasks"></a>寫入器的備份前工作

處理 [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) 事件時，VSS 會呼叫每個寫入器的 [**CVssWriter：： OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) 方法，這是一種虛擬方法，其預設只會傳回 true。

寫入器可以覆寫此預設值，並使用處理來尋找即將進行之備份的相關資訊，並採取動作。

寫入器可以使用下列方法來判斷備份作業 contemplated 的相關資訊：

1.  [**CVssWriter::GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)
2.  [**CVssWriter::IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)
3.  [**CVssWriter::AreComponentsSelected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)

寫入器會使用 [**CVssWriter：： IsPathAffected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispathaffected)，判斷其所管理的檔案是否會包含在陰影複製中。

更重要的是，當 VSS 呼叫 [**CVssWriter：： OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) 方法時，它會傳入 [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) 介面的實例，以允許透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面直接存取其在要求者的備份元件檔中 [*明確包含*](vssgloss-e.md) 的元件。 寫入器使用 **>ivsscomponent** 介面的實例來定義元件集合，以取得其 *隱含包含* 元件的存取權 (參閱 [Selectability 和使用元件屬性](selectability-and-working-with-component-properties.md)) 。

在處理 [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) 事件期間，寫入器會使用 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面來執行元件 (或元件集) 作業所設定的元件，包括：

1.  藉由呼叫 [**>ivsscomponent：： AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)，將 [*部分*](vssgloss-p.md)檔案新增 (（如果支援) ）。
2.  設定寫入器將處理還原所需的任何私用中繼資料。
3.  如果寫入器支援增量和差異備份 (請參閱) [增量和差異備份](incremental-and-differential-backups.md) ，執行下列步驟：
    -   藉由呼叫 [**>ivsscomponent：： GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)檢查先前的備份時間戳記。
    -   藉由呼叫 [**>ivsscomponent：： AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)來新增任何必要的 [*差異*](vssgloss-d.md)檔案。
    -   如果寫入器支援 **VSS \_ BS \_** 時間戳記架構，請使用 [**>ivsscomponent：： SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)，以寫入器本身的格式加入備份時間戳記字串。
4.  起始非常耗時的非同步作業，例如跨多個磁片同步處理資料。 這可讓寫入器在工作處理時繼續工作，包括處理其他 VSS 事件。 這些作業必須在 [*凍結*](vssgloss-f.md) 事件之前終止。

要求者呼叫 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 會起始陰影複製，並產生下列事件供寫入器處理：

-   [*PrepareForSnapshot*](vssgloss-p.md)
-   [*凍結*](vssgloss-f.md)
-   [*解凍*](vssgloss-t.md)
-   [*PostSnapshot*](vssgloss-p.md)

其中三個寫入器的處理常式（[**CVssWriter：： OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot)、 [**CVssWriter：： OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)和 [**CVssWriter：： OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)）是純虛擬方法，而且每個寫入器都必須執行它們，而不是依賴預設值。 視寫入器的需求而定，它們可能會編碼為虛擬方法，只是傳回 **TRUE**。

由於發出 [*凍結*](vssgloss-f.md) 事件和發出 [*解除凍結*](vssgloss-t.md) 事件之間通常會有很窄的時間範圍，因此在準備進行陰影複製時，大部分的主要工作（例如關閉進程、建立暫存檔案或清空 i/o 佇列）都是在 [**CVssWriter：： OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot)中處理。

在建立陰影複製之前，寫入器可能會如何使用 [**CVssWriter：： OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot) 來處理其 i/o，高度相依于寫入器本身的架構。

在 [*凍結*](vssgloss-f.md)之前，可承受保存所有寫入並將資料保持在絕對一致狀態的寫入器應該這麼做。

如果寫入器無法凍結其 i/o，則應該採取動作來建立穩定來源以進行備份，並減少陰影複製的復原時間。 這種情況的範例可能包括將傳入的 i/o 要求排入佇列，或在 [*替代路徑*](vssgloss-a.md) 中產生一組重複的檔案，做為備份的來源使用。

[**CVssWriter：： OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)方法會執行簡單、簡短的工作，例如確認 [**CVssWriter：： OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot)的左 i/o 是否處於正確的狀態，以及 [**CVssWriter：： OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)啟動的任何非同步工作是否已完成。 如果有問題 (查看 [寫入器錯誤和 Vetoes) ，](writer-errors-and-vetoes.md) 則此方法是寫入器在發生陰影複製時的最後機會。

寫入器通常可能會在 [*解凍*](vssgloss-t.md) 事件之後繼續正常作業：在解除凍結之後，陰影複製可能無法立即進行備份，但是寫入器應該能夠繼續正常操作。 因此，寫入器通常會使用 [**CVssWriter：： OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) 來回複為預先凍結狀態。 不過，為了支援陰影複製所建立的任何暫存檔，都應該留在 [*PostSnapshot*](vssgloss-p.md) 事件的位置。 一般來說，您會使用 [**CVssWriter：： OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) 來進行這類的清除。 因為許多應用程式都不需要這種清除，所以 **CVssWriter：： OnPostSnapshot** 是一種虛擬方法，其預設實作為只會傳回 **TRUE**。 如果正在執行增量或差異備份，寫入器可能會呼叫 [**>ivsscomponent：： GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp) 和 [**>ivsscomponent：： SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)。 如需詳細資訊，請參閱 [備份複雜存放區中的寫入器角色](writer-role-in-backing-up-complex-stores.md)。 此時可以呼叫的另一個方法是 [**>ivsscomponent：： AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)。

 

 




