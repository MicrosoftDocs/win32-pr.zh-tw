---
description: 除了執行備份或還原，以及管理陰影複製之外，要求者還必須管理與其互動之寫入器元件的相關資訊。
ms.assetid: 641abfbe-fc72-4468-9ef6-69c452adb1b3
title: 要求者使用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83efdb9e80ac0331289c3b611978e66a58098de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511532"
---
# <a name="use-of-components-by-the-requester"></a>要求者使用元件

除了執行備份或還原，以及管理陰影複製之外，要求者還必須管理與其互動之寫入器元件的相關資訊。 元件 selectability 和邏輯路徑可用來包含或排除備份中的資料，並決定備份元件檔中包含的元件資訊。

## <a name="requester-component-selection-during-backup"></a>備份期間選取的要求者元件

在備份作業期間，要求者會使用 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) 和 [**>ivssbackupcomponents：： GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) 方法來匯入寫入器中繼資料元件資料 (如需詳細資訊) ，請參閱 [備份初始化的總覽](overview-of-backup-initialization.md) 。

在使用 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) 介面檢查寫入器資訊之後，要求者會決定要備份的寫入器，以及要備份的特定寫入器元件的範圍有限範圍。

備份寫入器時，要求者：

-   必須 [*明確包含*](vssgloss-e.md) 備份元件的所有寫入器其，而不是使用 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 可選取的備份元件，將元件新增至備份元件檔
-   可使用 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 明確包含任何寫入器可選取的備份元件，以將元件新增至備份元件檔
-   如果可選取的備份元件定義 [*元件集*](vssgloss-c.md)，則其明確的包含會 [*隱含地包含*](vssgloss-i.md) 所有元件集的成員—不論是否可針對備份進行選取。 這些元件不會加入至 [備份元件] 檔。

在新增可選取的備份元件或備份元件的其，而不是可在其備份元件檔中選擇備份的備份元件時，要求者會指定下列各項：

-   管理元件的寫入器實例
-   寫入器的類別識別碼
-   元件的 [*邏輯路徑*](vssgloss-l.md) (可能是 **Null**) 
-   元件的名稱

如果元件不符合規格，則會傳回錯誤。

如果有這類元件，VSS 會在備份元件檔中建立元件的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面。 寫入器和要求者將可存取及修改此資訊。 針對定義 [*元件集*](vssgloss-c.md)的可選取元件，它不僅會描述元件的屬性，也會描述它所包含的所有子元件。

在備份元件檔中無法使用隱含新增元件的相關資訊。 此外，[備份元件] 檔中沒有任何可用的檔案資訊。 若要取得這項資訊，要求者必須檢查寫入器元資料檔案 (在 [備份元件] 檔中選取之預存元件的內容中，已) 讀取這些檔。

## <a name="requester-component-selection-during-restore"></a>還原期間選取的要求者元件

在還原作業期間，要求者不應該透過 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)從目前在系統上作用的寫入器匯入元件資訊，因為目前執行中的處理常式狀態不一定會在進行備份時反映進程的狀態。

它仍應透過 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)產生 [*識別事件*](vssgloss-i.md)，以建立 *識別事件*，並判斷目前在系統上的寫入器和其狀態。

要求者會在初始化期間和儲存的寫入器元資料檔案中，抓取儲存的備份元件檔 (如需詳細資訊) ，請參閱 [還原初始化的總覽](overview-of-restore-initialization.md) 。

在備份期間包含元件與還原的方式大致相同，不同之處在于您必須考慮將可 [*選取的還原*](vssgloss-s.md) 和 [*邏輯路徑*](vssgloss-l.md)，而不是 [*針對備份而選擇*](vssgloss-s.md)。

但有一些差異：

-   如果在備份期間，元件已經 [*明確地包含*](vssgloss-e.md) 在備份元件檔中，則如果已將它包含在還原 (（明確或隱含地) ），則會使用 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) 來明確地將它加入至備份元件檔以進行還原。
-   如果元件隱含地 [*包含*](vssgloss-i.md) 在備份中，而且是其進行還原，而不是可選取的來還原祖系（在備份案例中，這表示需要明確包含）-元件不會明確包含 (也就是，它不會使用 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)) 加入至備份元件檔。 這類元件應該視為隱含選取以進行還原。
-   針對要在其中隱含選取以進行備份的那些元件 (無論該元件是否可供備份或未) ，都可以使用 [**>ivssbackupcomponents：： AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)，將該元件新增至備份元件檔。
-   可選取的還原元件可能會定義用於還原的 [*元件集*](vssgloss-c.md) ，就像備份元件所能選擇的一樣。 這可供還原元件選擇，然後針對還原作業定義此元件集。

未在產生 [*PreRestore*](vssgloss-p.md) 事件之前明確選取要還原的寫入器，將不會收到任何 VSS 事件。

要求者和寫入器可以使用 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面來存取儲存的元件資訊。 透過 **>ivsscomponent** 介面，寫入器可以修改某些明確包含在備份元件檔中之元件的設定，以支援還原 (，例如 [*還原目標*](vssgloss-r.md)) 。 如果它定義元件集，則明確包含元件的寫入器修改將會傳播到 [*其子元件。*](vssgloss-s.md) 此外，介面會提供一種機制，在寫入器與要求者之間傳遞還原成功和失敗的相關資訊。

在備份期間，備份元件檔本身的資訊不足以執行還原。 同樣地，寫入器元資料檔案也必須提供要還原之檔案的實際路徑資訊，以及探索哪些其元件是可選取元件元件集的一部分，因此需要還原。

如需 Selectability 類型及其用法的相關資訊，請參閱 [使用 Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md) 。

## <a name="use-of-writer-component-document-information-by-the-requester"></a>要求者使用寫入器元件檔資訊

每個元件都是由其父寫入器的 [*寫入器類別識別碼*](vssgloss-w.md) 、其名稱及其 [*邏輯路徑*](vssgloss-l.md)來唯一識別。

要求者可以使用 [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)方法所傳回的 [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext)介面，來取得每個預存元件的相關資訊。

元件的名稱和邏輯路徑 (可透過 [**IVssWriterComponentsExt：： GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent)傳回的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)介面，在其他) 專案中找到。

> [!Note]  
> 在還原階段，要求者必須在呼叫 [**>ivssbackupcomponents：:P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)之後，才呼叫 [**IVssWriterComponentsExt：： GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent)或 [**IVssWriterComponentsExt：： GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) ，以允許寫入器更新備份元件檔的時間。 這類更新的其中一個範例是變更還原目標。

 

您可以使用 [**IVssWriterComponentsExt：： GetWriterInfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo)，找到每個預存可選取元件的父寫入器的相關資訊。

您可以使用此資訊來查詢寫入器元資料檔案，並識別相符的檔。 然後，藉由使用 [*邏輯路徑*](vssgloss-l.md)，要求者可以識別每個可選取元件的相依其元件，也就是識別可選取元件 [*元件集合*](vssgloss-c.md)的所有成員。

使用 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) 介面時，要求者現在擁有完整的元件資訊（包括從 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) 介面 (的路徑規格) ），可供所需的可選取和其元件進行備份或還原。

這就是為什麼要求者要儲存本身的備份元件檔的狀態，以及正在備份之寫入器的寫入器元資料檔案，這是很重要的原因之一。

如需詳細資訊，請參閱使用 [Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md) 。

 

 
