---
description: VSS 備份中的寫入器參與設計，是為了讓應用程式能夠控制要如何使用其還原資料。
ms.assetid: 076b2e6f-c2ca-4129-8827-1b18a655d634
title: 不含寫入器參與的還原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896cbe81a2c3487bb00b01379b6b5bbe4760ecbb28c1bf94c661eeb0049a3d37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056366"
---
# <a name="restores-without-writer-participation"></a>不含寫入器參與的還原

VSS 備份中的寫入器參與設計，是為了讓應用程式能夠控制要如何使用其還原資料。

一般來說，如果系統上有寫入器，建議您不要將資料還原至其原始位置，而不需要撰寫參與。 這樣的還原可能會遇到鎖定的目的地檔案，而且會造成損毀資料的重大風險。

不過，備份應用程式可能會想要或需要還原 VSS 備份而不需要撰寫參與的原因如下：

-   資料是由不受 VSS 感知的應用程式所管理。 幾乎每個系統都有一些應用程式（文字編輯器、郵件讀取器、文字處理器等等）不是 VSS 感知。 無法使用寫入器參與來還原此資料。

    一般而言，這種類型的資料不是系統或服務關鍵，而還原它應該不會有問題，或至少在傳統還原期間沒有任何問題。

    如同傳統還原的準備工作，還原操作員應該在啟動 VSS 還原之前，嘗試暫停或終止這類應用程式。

-   遺漏 VSS 寫入器。 在還原損毀的系統狀態時，這種情況可能相當常見。 備份作業必須判斷是否需要還原遺失寫入器的檔案。 如果需要還原，可以還原檔案，就像傳統備份會還原這些檔案一樣。
-   寫入器資料的私用還原。 要求者可以選擇將執行中的寫入器資料還原到某個私用位置，而不會通知寫入器。 其中一個範例可能會還原寫入器的資料，以支援離線比較。 在這種情況下，要求者不會想要在進行還原時使用 [*新的目標位置*](vssgloss-n.md) ，因為它不希望寫入器存取資料。
-   在還原過程中不會包含寫入器。 寫入器會藉由 \_ \_ 針對 [**IVssCreateWriterMetadata：： SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)的 *writerRestore* 參數傳遞 VSS WRE，來指出這一點。
-   寫入器需要自訂的還原方法。 寫入器表示它需要自訂還原， \_ \_ 方法是針對 [**IVssCreateWriterMetadata：： SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)的 *方法* 參數傳遞 VSS RME 自訂。 在此情況下，除非該寫入器的自訂還原檔另有指示，否則這個寫入器不應該參與還原程式。

要求者牽涉到還原程式中的寫入器，方法是在呼叫 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)時指定其中一個寫入器的元件。 在 **>ivssbackupcomponents：： SetSelectedForRestore** 的呼叫中不指定任何該寫入器的元件時，可以還原寫入器的資料而不涉及寫入器。 如果寫入器不預期有任何還原事件，則在還原程式中牽涉到該寫入器可能會造成該寫入器回報的錯誤。

 

 



