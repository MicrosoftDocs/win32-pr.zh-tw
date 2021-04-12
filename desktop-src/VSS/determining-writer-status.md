---
description: 要求者在建立陰影複製時，以及在備份和還原作業期間，都必須有充分定義的寫入器狀態。
ms.assetid: 676d5cff-bd28-43f0-a402-d184c96f0061
title: 判斷寫入器狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719322a18808748e92d412c48c7b7628fdac9d51
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195859"
---
# <a name="determining-writer-status"></a>判斷寫入器狀態

要求者在建立陰影複製時，以及在備份和還原作業期間，都必須有充分定義的寫入器狀態。 若要這樣做，建議您：

-   要求者會使用 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus)、 [**>ivssbackupcomponents：： GetWriterStatusCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount)和 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)。
-   如如何 [處理 Vss 下的備份](overview-of-processing-a-backup-under-vss.md) 和在 [Vss 下處理還原](overview-of-processing-a-restore-under-vss.md)的總覽所述，這些方法在以妥善定義的備份或還原順序呼叫時最為有用。 一般來說，這表示在要求者完成其中一個工作並產生 VSS 事件之後，就應該查詢寫入器。

    處理備份時，要求者應在完成下列方法之後查詢寫入器。 要求者必須在呼叫 [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)之後呼叫 [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) ，使寫入器會話設定為已完成狀態。

    > [!Note]  
    > 只有在 Windows Server 2008 Service Pack 2 (SP2) 及更早版本才需要此功能。

     

    <dl> <dt>

[**>ivssbackupcomponents：:P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)
</dt> <dt>

[**>ivssbackupcomponents：:D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
</dt> <dt>

[**>ivssbackupcomponents：： BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
</dt> </dl>

在還原作業期間，要求者應該在完成這些方法之後查詢寫入器：
<dl> <dt>

[**>ivssbackupcomponents：:P reRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
</dt> <dt>

[**>ivssbackupcomponents：:P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)
</dt> </dl>

-   [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus)的呼叫不是定義完善之備份或還原順序的一部分，因此不會提供寫入器狀態的可靠圖片，因為它們可能會反映不表示目前作業失敗的條件，例如：
    -   先前的陰影複製建立失敗
    -   提早備份或還原作業發生錯誤
    -   目前正在處理事件的沒有回應的寫入器

因此，開發人員不應該依賴進程的其他處理常式傳回的寫入器狀態，然後再嘗試以另一個 (可能在不同的執行緒) 來監視 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面的某個實例的進度。

請注意，針對備份作業（需要檢查寫入器的寫入器元資料檔案），在產生和處理 [**>ivssbackupcomponents：： GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)所造成的 [*識別*](vssgloss-i.md)事件之後，不需要要求者呼叫 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus)和 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) 。

[**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) 只會報告這些寫入器的狀態，而這些寫入器的中繼資料是由寫入器 [*識別*](vssgloss-i.md) 事件處理常式（ [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (，並由 [**>ivssbackupcomponents：： GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) 和 [**>ivssbackupcomponents：： GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)) 傳回給要求者。

如果寫入器的 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 執行失敗，該寫入器的中繼資料將不會是提供給 VSS 的寫入器元資料檔案清單的一部分，也不會提供任何狀態資訊，而且呼叫會是多餘的。

若為還原作業，要求者不需要檢查執行中寫入器的寫入器元資料檔案，則呼叫 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 和 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) 可能是更有效率的方式來判斷正在執行的寫入器。

 

 



