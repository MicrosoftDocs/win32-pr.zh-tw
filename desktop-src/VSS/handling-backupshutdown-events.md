---
description: 備份應用程式 (要求者) 可能會終止，而不會產生 BackupComplete 事件。
ms.assetid: 8e6a1f4f-ba62-46ea-965e-b0c6526ece89
title: 處理 BackupShutdown 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e60a063a11f0a492407daed31ace4a62aec2a13fe824e110de272d58b84bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998248"
---
# <a name="handling-backupshutdown-events"></a>處理 BackupShutdown 事件

備份應用程式 (要求者) 可能會終止，而不會產生 [*BackupComplete*](vssgloss-b.md) 事件。 備份應用程式可能會損毀，或從工作管理員終止 (（例如) ，且無法呼叫 [**>ivssbackupcomponents：： BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)）。

因此，只要釋放參與備份的 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)實例（無論是由要求者或系統發行），VSS 基礎結構 (而不是要求者) 就會產生 [*BackupShutdown*](vssgloss-b.md)事件。

如果備份正常進行，寫入器將會收到 BackupComplete 事件，後面接著 BackupShutdown 事件。

如果作業中止 (要求者藉由呼叫 [**>ivssbackupcomponents：： AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) 來產生 [*中止事件*](vssgloss-a.md)，或是突然失敗，寫入器可能只會收到 BackupShutdown 事件，而且可能不會收到執行清除作業的其他事件。 寫入器會判斷 BackupShutdown 事件是否遵循適當的事件順序，或是表示備份作業的非預期失敗。

BackupShutdown 事件處理常式（ [**CVssWriter：： OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)）會接收 \_ 要關閉的備份作業之陰影複製集的 VSS 識別碼 (GUID) 。 寫入器可以使用它來判斷正在關閉的備份作業，如果它在其備份順序中儲存了陰影複製集識別碼 (例如，從 [**CVssWriter：： OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)、 [**CVssWriter：： OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)或 [**CVssWriter：：**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) OnPostSnapshot) 使用 [**CVssWriter：： GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid)。

不過，寫入器不應該從 [**CVssWriter：： OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)內呼叫 [**CVssWriter：： GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid) 。 此外，在 [**CVssWriter：： OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)傳回之後，就無法呼叫 **CVssWriter：： GetCurrentSnapshotSetId** 。

寫入器有可能涉及多個備份作業，而且如果因為要求者突然關機而呼叫 BackupShutdown 事件，則傳回的 VSS \_ 識別碼可能是寫入器所參與的另一個備份作業。

 

 



