---
description: 寫入器可能會因為許多程式設計的原因而失敗。
ms.assetid: 50eced73-3917-4d7e-96cc-2d793b448738
title: 寫入器錯誤和 Vetoes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c24c15ad10766fc6ec395ed058ab3cb72a689d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191358"
---
# <a name="writer-errors-and-vetoes"></a>寫入器錯誤和 Vetoes

寫入器可能會因為許多程式設計的原因而失敗。 發生這種情況時，它應該會在其中一個處理常式方法中呼叫 [**CVssWriter：： SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure) 方法，以禁止進行中的備份、還原或陰影複製作業 (例如， [**CVssWriter：： OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) 或 [**CVssWriter：： OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) 並傳回 **TRUE**。 它也可以選擇性地使用 [**IVssComponentEx：： SetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setprepareforbackupfailuremsg)、 [**IVssComponentEx：： SetPostSnapshotFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setpostsnapshotfailuremsg)、 [**>ivsscomponent：： SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)和 [**>ivsscomponent：： SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg) 方法，以回應特定處理常式方法中的失敗狀況。 要求者可以接受拒絕或繼續進行備份，忽略拒絕。

要求者應該使用 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 和 [**>ivssbackupcomponents：：) GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) ，在它產生的每個事件之後，檢查寫入器狀態 (。

在某些情況下，您可以使用 [**IVssComponentEx：： GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg)、 [**>ivsscomponent：： GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg)、 [**IVssComponentEx：： GetPostSnapshotFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getpostsnapshotfailuremsg)和 [**>ivsscomponent：： GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg) 方法) ，從這些失敗中取出錯誤訊息 (，否則寫入器可能會選擇使用 [**>ivsscomponent：： SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata) 和 [**>ivsscomponent：： SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) （具有錯誤狀態資訊) ）來設定中繼資料 (。 如需顯示如何查看這類錯誤訊息的範例程式碼，請參閱 [**IVssComponentEx：： GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg)。

根據錯誤狀態，要求者或其操作員可以使用備份作業或系統狀態的任何必要修改，重新開機備份和陰影複製。

例如，假設 [**GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) 傳回下列內容：

-   **VSS \_E \_ WRITERERROR \_ INCONSISTENTSNAPSHOT** 建議要求者可能會將其他磁片區新增至陰影複製
-   **VSS \_E \_ WRITERERROR \_** 可重試表示重試而不重新設定可能會正常運作。 如果寫入器在數次重試之後仍繼續傳回錯誤，請嘗試重新開機裝載寫入器的服務。 下列寫入器裝載于 VSS 服務：登錄寫入器、COM + 類別註冊資料庫寫入器、陰影複製優化寫入器，以及自動系統復原 (ASR) 寫入器中。 如果寫入器屬於在它自己的進程中裝載寫入器的應用程式，請嘗試重新開機應用程式。

    **Windows Server 2003 和 WINDOWS XP：** 下列寫入器裝載于 VSS 服務：登錄寫入器、COM + 類別註冊資料庫寫入器、應用程式事件記錄檔寫入器，以及 Microsoft SQL Server 2000 桌面引擎 (MSDE) 寫入器。

-   VSS \_ E \_ 寫入器 \_ 狀態 \_ 無法 \_ 使用指出寫入器可能已達可用備份和還原會話的數目上限，而且當系統較不忙碌時，重試可能會正常運作。
-   **VSS \_E \_ WRITERERROR \_ OUTOFRESOURCES** 或 **VSS \_ e \_ WRITERERROR \_ TIMEOUT** 可能會建議您在重試之前先降低系統負載
-   **VSS \_E \_ WRITERERROR \_ NONRETRYABLE** 或 **VSS \_ E \_ 寫入 \_ 器沒有 \_ 回應** 可能會指出寫入器錯誤，因此嚴重的原因是不會嘗試使用 VSS 來備份其資料。

根據所產生的寫入器和哪些元件而定，備份應用程式不一定需要在拒絕或錯誤之後中止。

例如，要求者可能會決定陰影複製的目的是要備份應用程式 A，並且已從備份應用程式 B 的寫入器收到拒絕。在此情況下，您可以在略過拒絕時繼續備份應用程式 A。

以下是寫入器否決的範例：

-   當寫入器在建立陰影複製時無法暫停其活動時，寫入器會 vetoes 陰影複製建立程式。 這表示由於在凍結狀態期間發生寫入作業，導致陰影複製不正確機率很高。
-   備份應用程式要求僅限磁片區 C 的陰影複製，而寫入器會判斷 C：和 D：的陰影複製是要備份其資料。 在此情況下，寫入器將會被拒絕。 備份應用程式可能會檢查中繼資料，並判斷是否要忽略寫入器，或是將會中止陰影複製建立程式，並于稍後重新開機。

 

 



