---
description: 在還原之後，寫入器會檢查作業的狀態，使其可以利用還原的資料並處理錯誤。
ms.assetid: f9def67a-c4ea-4014-929f-51fbd10d770a
title: 還原清除和終止的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8ad0b7d40f3c0e5322810f96bb120f28effe4ec3f0d4e278af924962713b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122030"
---
# <a name="overview-of-restore-clean-up-and-termination"></a>還原清除和終止的總覽

在還原之後，寫入器會檢查作業的狀態，使其可以利用還原的資料並處理錯誤。 要求者必須等待此活動完成。 如需詳細資訊，請參閱 [在 VSS 下處理還原的總覽](overview-of-processing-a-restore-under-vss.md)。

下表顯示執行還原作業之後所需的動作和事件的順序。



| 要求者動作                                                                                                                                                                                                                                                                                                                                                              | 事件                                                           | 寫入器動作                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 要求者指出還原 (的結尾，請參閱 [**>ivssbackupcomponents：:P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)) 。                                                                                                                                                                                                                                           | [*PostRestore*](vssgloss-p.md) | 寫入器會在還原後進行清除，並處理還原至非標準位置的還原失敗和檔案 (請參閱 [**CVssWriter：： OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)、 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)) 。 |
| 要求者等候寫入器處理具有 [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)的 [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)事件。 它也應該驗證寫入器狀態 (請參閱 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus)， [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)) 。 | 無                                                            | 無                                                                                                                                                                                                                                               |
| 要求者會釋放 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面。                                                                                                                                                                                                                                                                                    | 無                                                            | 無                                                                                                                                                                                                                                               |



 

## <a name="requester-actions-during-cleanup-and-termination"></a>清除和終止期間的要求者動作

此時，要求者會藉由呼叫 [**>ivssbackupcomponents：:P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)來產生 [*PostRestore*](vssgloss-p.md)事件，以指出其檔案還原活動的結尾。

要求者的動作僅限於等候寫入器，這可能需要執行一些最終清除和處理還原錯誤，並在所有寫入器從處理 [*PostRestore*](vssgloss-p.md)事件傳回之後釋放 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)介面。

## <a name="writer-actions-during-cleanup-and-termination"></a>清除和終止期間的寫入器動作

[*PostRestore*](vssgloss-p.md)事件是由虛擬方法 [**CVssWriter：： OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)所處理。 預設的實值只會傳回 **true** ，而不採取任何動作。 如果寫入器需要更充分掌控還原後的情況，它可以覆寫這個方法。

除了任何一般清除 (，例如移除寫入器可能在 [**CVssWriter：： OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)中執行的暫存檔案) ，它可以處理還原作業成功或失敗。

它如何處理還原錯誤、還原到替代位置的檔案，以及未來的還原需求，完全是作者的決定。 一般動作可能包括將替代或新位置中的檔案與目前使用中的檔案進行比較、合併多個檔案的資料，或開始新的會話連接到新的資料檔案。 VSS 提供下列機制，可依元件分別支援此項：

-   您可以使用 [**>ivsscomponent：： GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)，找到還原任何元件的成功或失敗。
-   [**>Ivsscomponent：： GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)會指出在還原檔案中使用替代位置對應的方式。
-   藉由呼叫 [**>ivsscomponent：： GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores)，來判斷還原是否為累加式，以及是否需要進一步的還原。 需要完整還原其資料的寫入器不應重新開機，直到此方法傳回 false 為止。
-   寫入器可以使用 [**>ivsscomponent：： GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount)和 [**>ivsscomponent：： GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget) ，判斷要求者是否需要將檔案還原至先前未指定的位置

 (如需將檔案還原至非預設位置的詳細資訊，請參閱 [非預設備份和還原位置](non-default-backup-and-restore-locations.md)。 ) 

如同任何 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 方法，指定實例所傳回的資訊會套用至 [*明確包含*](vssgloss-e.md) 用於備份的元件，以及其針對備份子元件 [*隱含*](vssgloss-i.md) 包含的元件，包括要求者使用 [**>ivssbackupcomponents：： (AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) 所明確包含子群組件， [以及](working-with-selectability-for-restore-and-subcomponents.md) 詳細資料) 的子元件。

因為寫入器需要存取備份元件檔，所以要求者必須等到寫入器完成處理之後，才能釋放 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面。

 

 



