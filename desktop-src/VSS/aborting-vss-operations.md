---
description: 在下列任何情況下，可以在備份作業期間產生中止事件：
ms.assetid: c2e39cdd-0ff8-4030-9bec-9e003b4d9520
title: 中止 VSS 作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120ef8fb16c23d77a24526aad0fd62e56c1888a76dc2de884140094c6591cd78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998268"
---
# <a name="aborting-vss-operations"></a>中止 VSS 作業

在下列任何情況下，可以在備份作業期間產生 [*中止*](vssgloss-a.md)事件：

-   要求者會藉由呼叫 [**>ivssbackupcomponents：： AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)明確產生 [*中止事件*](vssgloss-a.md)。
-   寫入器的 [*凍結*](vssgloss-f.md) 和 [*解除凍結*](vssgloss-t.md) 事件處理常式 ([**CVssWriter：： OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) 和 [**CVssWriter：： OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) 傳回 **false**，或無法在 [**CVssWriter：： Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)中指定的時間範圍內完成。
-   在 [*PrepareForSnapshot*](vssgloss-p.md) 事件之後建立陰影複製時，提供者或 VSS 有任何失敗。

還原作業不支援中止。

## <a name="requester-handling-and-creation-of-abort-events"></a>要求者處理和建立中止事件

[**>Ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)介面的實例只能用於一個備份，因此，如果在處理備份時發生錯誤，通常最好是釋放目前的實例，然後重新開始。

要求者應該明確地表示它正在中止備份作業 (使用 [**>ivssbackupcomponents：： AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) 只有在進行備份的實際準備、涉及寫入器或建立陰影複製時才會發生。

實際上，這表示當要求者在產生 [*PrepareForBackup*](vssgloss-p.md) 事件之後，藉由呼叫 [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)來停止備份作業時，它應該呼叫 [**>ivssbackupcomponents：： AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) ，並等候其在釋放目前 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 實例之前的傳回。

例如，如果寫入器拒絕備份作業，要求者應該使用 [**>ivssbackupcomponents：： AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) 通知所有其他寫入器，備份作業將不會完成。

在呼叫 [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)之前，或呼叫 **PrepareForBackup** 失敗時，要求者可以釋放目前的 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面實例，而不需要產生 Abort 事件。

例如，如果 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 的目前實例只是用來藉由呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) 來取得資訊，並產生 [*識別*](vssgloss-i.md) 事件，則在傳回信息之後，就可以直接釋出 **>ivssbackupcomponents** 實例。

要求者在呼叫 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)時，會產生許多事件 ([*PrepareForSnapshot*](vssgloss-p.md)、[*凍結*](vssgloss-f.md)、[*解凍*](vssgloss-t.md)和 [*PostSnapshot*](vssgloss-p.md)) 。 處理凍結和解除凍結事件時，寫入器可能會失敗，並可自行產生中止事件。 無法處理 PrepareForSnapshot 和 PostSnapshot 事件時，不會產生中止事件。

要求者必須知道在 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 指出失敗時是否產生了 Abort 事件。 因此，需要終止備份作業的要求者，因為 **>ivssbackupcomponents：:D osnapshotset** 的狀態指出問題仍應呼叫 [**>ivssbackupcomponents：： AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)。

如果要求者已呼叫 [**>ivssbackupcomponents：： AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)，則在釋放 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)的實例之前，不需要呼叫 [**>ivssbackupcomponents：： BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) 。

## <a name="writer-handling-and-creation-of-abort-events"></a>寫入器處理和建立中止事件

如先前所述，寫入器可以接收來自要求者的中止事件，或是提供者可以觸發一個本身。 此外，寫入器可能會在特定情況下接收多個中止事件。 寫入器開發人員應該將 [**CVssWriter：： OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) 的任何執行程式碼撰寫成這一點。

在處理中止事件時，寫入器應該嘗試還原其所管理的任何處理程式，以做為其正常執行狀態，以及執行任何錯誤處理和記錄。

這可能表示， [**CVssWriter：： OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) 的執行可能必須執行許多（如果不是全部）與解凍事件處理常式相同的工作 ([**CVssWriter：： OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) 和 PostSnapshot 事件處理常式 ([**CVssWriter：： OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) ，而且可以從 **CVssWriter：： OnAbort** 中呼叫這些處理常式。

 

 



