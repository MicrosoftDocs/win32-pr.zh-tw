---
description: 寫入器是一種應用程式或服務，會將持續性資訊儲存在磁片上的檔案中，並使用陰影複製介面，將這些檔案的名稱和位置提供給要求者。
ms.assetid: 24fc2d7c-f8d6-49ca-9bb5-0179bef68e78
title: 寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abf748d0c6c4533c81c0f8a8d0c0c5aa9125c92334a1c09d4ab40fad299067b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863788"
---
# <a name="writers"></a>寫入器

[*寫入*](vssgloss-w.md) 器是一種應用程式或服務，會將持續性資訊儲存在磁片上的檔案中，並使用陰影複製介面，將這些檔案的名稱和位置提供給要求者。

在備份作業期間，寫入器可確保其資料為靜止且穩定，適用于陰影複製和備份。 寫入器會在可能的情況下解除鎖定檔案，並在必要時指出替代位置，以與還原共同作業

如果 VSS 備份作業期間沒有任何寫入器存在，仍然可以建立陰影複製。 在此情況下，陰影複製之磁片區上的所有資料都會處於損 [*毀一致狀態*](vssgloss-c.md)。

## <a name="writer-state"></a>寫入器狀態

寫入器會在以 XML 為基礎的中繼資料物件（ [*寫入器元資料檔案*](vssgloss-w.md)）中維護其狀態。

此寫入器中繼資料是唯一的資料結構，其中包含要備份和還原的資料 [*檔集*](vssgloss-f.md)（路徑、檔案規格和遞迴旗標）。

寫入器元資料檔案會將寫入器的檔案集組織成群組或 [*元件*](vssgloss-c.md)。 這些元件在備份和還原作業期間的關聯性，是由元件的 [*selectability for backup*](vssgloss-s.md)、其 [*selectability for restore*](vssgloss-s.md)和其 [*邏輯路徑*](vssgloss-l.md)，在寫入器元資料檔案中說明。  (需詳細資訊，請參閱 [設定元件組織](definition-of-components-by-writers.md) 和 [使用 Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md)。 ) 

此檔也包含控制檔案還原和其他問題的其他資訊。

要求者需要寫入器中繼資料，以及其本身的備份元件檔，以處理備份或還原。

不同于備份元件檔，寫入器元資料檔案應該視為唯讀結構。 一旦寫入器建立它之後，就不會變更檔。

## <a name="writer-event-handling"></a>寫入器事件處理

寫入器的 VSS 作業是透過接收 COM 事件起始。

當沒有任何事件存在時，寫入器不會執行 VSS 作業 (例如 VSS 備份或還原) 。 相反地，它會執行其一般工作，例如回應資料庫查詢、管理使用者資料，或提供其他服務。

為了確保會正確執行多個平行備份和還原會話的錯誤處理，並確保一個備份或還原會話沒有損毀，您必須執行下列動作：

-   如果寫入器的事件處理常式 (例如 [**CVssWriter：： OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)) 呼叫 [**CVssWriterEx2：： GetSessionId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-getsessionid)、 [**CVssWriter：： SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure)或 [**CVssWriterEx2：： SetWriterFailureEx**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-setwriterfailureex) 方法，則事件處理常式必須在呼叫事件處理常式的相同執行緒中呼叫方法。
-   只要每個背景工作執行緒將任何需要的錯誤報表封送處理回原始的事件處理常式執行緒，就可以視需要將工作的事件處理常式（例如 [**OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) ）的執行作業卸載至背景工作執行緒。

## <a name="handling-identify-events"></a>處理識別事件

除了識別事件之外，寫入器所接收之事件的類型和順序，會根據目前進行中的 VSS 作業類型而有所不同。

識別事件需要寫入器提供有關其設定及其透過其 [*寫入器中繼資料*](vssgloss-w.md)檔管理之檔案的系統資訊。 系統會產生識別事件，以支援幾乎任何 VSS 作業，包括系統查詢，以及陰影複製和備份和還原作業。 因此，任何寫入器的識別事件處理常式 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 執行都必須能夠隨時處理識別事件，包括處理另一個 VSS 作業（例如備份或還原）的過程。 您永遠都不應該將識別事件視為 VSS 作業生命週期的一部分，即使在作業開始之前，可能也需要產生它。

在 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)中不會修改 VSS 作業的相關狀態資訊，這點特別重要，因為收到順序外的事件會重設該資訊。

## <a name="backup-and-restore-events"></a>備份與還原事件

根據它是否參與備份或還原，寫入器除了初始識別事件之外，也會在兩個和七個事件之間收到。

處理這些事件的 (從寫入器的觀點來看，) 備份或還原作業的生命週期。

在一般的備份作業中 (查看在 [VSS) 下處理備份的總覽](overview-of-processing-a-backup-under-vss.md) ，寫入器除了初始識別事件) 之外，還會處理下列事件 (：

-   PrepareForBackup
-   PrepareForSnapshot
-   凍結
-   解除凍結
-   PostSnapshot
-   BackupComplete
-   BackupShutdown

在一般的還原作業中 (查看 [在 VSS) 處理還原的總覽](overview-of-processing-a-restore-under-vss.md) ，寫入器會處理下列事件：

-   PreRestore
-   PostRestore

 

 



