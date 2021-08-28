---
description: 執行還原初始化和準備還原的總覽中所述的動作之後，要求者有足夠的資訊來開始還原檔案。
ms.assetid: 15df39fa-1eb1-4e96-9e26-14470f391de4
title: 實際檔案還原的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2cc1b74f7beae7f5686dc36ce741428cad97ae62c62c8895122ec8a639e46f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998238"
---
# <a name="overview-of-actual-file-restoration"></a>實際檔案還原的總覽

執行 [還原初始化](overview-of-restore-initialization.md) 和 [準備還原的](overview-of-preparing-for-restore.md)總覽中所述的動作之後，要求者有足夠的資訊來開始還原檔案。 檔案還原不涉及寫入器互動或事件產生。 如需詳細資訊，請參閱 [在 VSS 下處理還原的總覽](overview-of-processing-a-restore-under-vss.md)。

下表顯示還原檔案所需的動作和事件順序。



| 要求者動作                                                                                                                                                                                                                                                                                                          | 事件 | 寫入器動作 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|---------------|
| 針對備份媒體上的檔案產生還原集清單。                                                                                                                                                                                                                                                                 | 無  | 無          |
| 處理 [*導向目標*](vssgloss-d.md) 或 [*部分檔*](vssgloss-p.md) 還原 (請參閱 [**>ivsscomponent：： GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)， [**>ivsscomponent：： GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)) 。 | 無  | 無          |
| 如有必要，請忽略所有指定的還原位置，並還原至先前呼叫 [**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)所指定的新位置。                                                                                                                       | 無  | 無          |
| 如果還原是累加的，而且需要進一步的還原，請指出 (參閱 [**>ivssbackupcomponents：： SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) 和累加 [式和差異備份](incremental-and-differential-backups.md)) 。                                                     | 無  | 無          |
| 若要瞭解寫入器是否已修改備份元件檔的內容，請呼叫 [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)。 例如，寫入器可能已變更還原目標。                                                                 | 無  | 無          |



 

## <a name="requester-actions-during-restoring-files"></a>還原檔案期間的要求者動作

對於備份媒體上的大部分檔案，要求者必須判斷其原始位置，以及套用至這些位置的任何新位置或替代位置對應。  (請參閱 [產生還原集](generating-a-restore-set.md) ，以瞭解如何判斷要還原的檔案，以及要將哪些檔案還原至何處的最佳作法討論。 ) 

此外，某些檔案可能會有 [*導向目標*](vssgloss-d.md) 或支援 [*部分檔*](vssgloss-p.md) 還原。 您可以藉由呼叫 [**>ivsscomponent：： GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) 和 [**>ivsscomponent：： GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)來找到這類檔案的數目，以及藉由呼叫 [**>ivsscomponent：： AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) 和 [**>ivsscomponent：： GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)來找到詳細還原指示的相關資訊。  (部分和導向的檔案可以是隱含或明確新增至原始備份之元件的一部分，請參閱 [使用 Selectability 進行還原和子元件](working-with-selectability-for-restore-and-subcomponents.md) 以取得詳細資訊。 ) 

使用 [**>ivssbackupcomponents：： SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)，以元件為基礎來指出還原的成功或失敗。 在增量或差異還原的情況下，需要進一步的還原作業 () 也會以元件為基礎，使用 [**>ivssbackupcomponents：： SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores)來表示。

一般而言，VSS 不會指定從儲存體媒體抓取資料的機制、存放裝置媒體的選擇，或如何判斷應該在何處還原的檔案。

不過，對於特定的寫入器，還原檔案可能牽涉到使用記載的自訂介面和程式。 Windows 的系統寫入器（目前需要這類支援）記載于[特殊的 VSS 使用案例](special-vss-usage-cases.md)中。

一般情況下，建議您將每個 [*寫入器實例*](vssgloss-w.md) 的每個元件檔案當作一個單位來處理。 這需要下列各項：

-   將每個檔案與其管理的元件產生關聯。 這需要使用寫入器元資料檔案。
-   取得正確的還原目標資訊。 這需要備份元件檔中的資訊。

 

 



