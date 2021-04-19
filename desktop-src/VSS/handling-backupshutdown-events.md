---
description: 備份應用程式 (要求者) 可能會終止，而不會產生 BackupComplete 事件。
ms.assetid: 8e6a1f4f-ba62-46ea-965e-b0c6526ece89
title: 處理 BackupShutdown 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 939e8e64ca9ee463b0b8331e607f8068c3325d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979095"
---
# <a name="handling-backupshutdown-events"></a><span data-ttu-id="5451c-103">處理 BackupShutdown 事件</span><span class="sxs-lookup"><span data-stu-id="5451c-103">Handling BackupShutdown Events</span></span>

<span data-ttu-id="5451c-104">備份應用程式 (要求者) 可能會終止，而不會產生 [*BackupComplete*](vssgloss-b.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="5451c-104">It is possible for a backup application (requester) to terminate and not generate a [*BackupComplete*](vssgloss-b.md) event.</span></span> <span data-ttu-id="5451c-105">備份應用程式可能會損毀，或從工作管理員終止 (（例如) ，且無法呼叫 [**>ivssbackupcomponents：： BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)）。</span><span class="sxs-lookup"><span data-stu-id="5451c-105">The backup application could crash, or be terminated (from the Task Manager, for example) and not be able to call [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).</span></span>

<span data-ttu-id="5451c-106">因此，只要釋放參與備份的 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)實例（無論是由要求者或系統發行），VSS 基礎結構 (而不是要求者) 就會產生 [*BackupShutdown*](vssgloss-b.md)事件。</span><span class="sxs-lookup"><span data-stu-id="5451c-106">Therefore, the VSS infrastructure (rather than the requester) generates a [*BackupShutdown*](vssgloss-b.md) event whenever an instance of [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) participating in a backup is released, whether it is released by the requester or by the system.</span></span>

<span data-ttu-id="5451c-107">如果備份正常進行，寫入器將會收到 BackupComplete 事件，後面接著 BackupShutdown 事件。</span><span class="sxs-lookup"><span data-stu-id="5451c-107">If a backup proceeds properly, a writer will receive a BackupComplete event followed by a BackupShutdown event.</span></span>

<span data-ttu-id="5451c-108">如果作業中止 (要求者藉由呼叫 [**>ivssbackupcomponents：： AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) 來產生 [*中止事件*](vssgloss-a.md)，或是突然失敗，寫入器可能只會收到 BackupShutdown 事件，而且可能不會收到執行清除作業的其他事件。</span><span class="sxs-lookup"><span data-stu-id="5451c-108">If the operation aborts (the requester generates an [*Abort event*](vssgloss-a.md) by calling [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) or fails abruptly, a writer may receive only a BackupShutdown event, and it may not receive other events that perform cleanup operations.</span></span> <span data-ttu-id="5451c-109">寫入器會判斷 BackupShutdown 事件是否遵循適當的事件順序，或是表示備份作業的非預期失敗。</span><span class="sxs-lookup"><span data-stu-id="5451c-109">It is up to a writer to determine whether a BackupShutdown event follows a proper sequence of events, or represents an unexpected failure of the backup operations.</span></span>

<span data-ttu-id="5451c-110">BackupShutdown 事件處理常式（ [**CVssWriter：： OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)）會接收 \_ 要關閉的備份作業之陰影複製集的 VSS 識別碼 (GUID) 。</span><span class="sxs-lookup"><span data-stu-id="5451c-110">The BackupShutdown event handler, [**CVssWriter::OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown), receives the VSS\_ID (GUID) of the shadow copy set of the backup operation being shut down.</span></span> <span data-ttu-id="5451c-111">寫入器可以使用它來判斷正在關閉的備份作業，如果它在其備份順序中儲存了陰影複製集識別碼 (例如，從 [**CVssWriter：： OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)、 [**CVssWriter：： OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)或 [**CVssWriter：：**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) OnPostSnapshot) 使用 [**CVssWriter：： GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid)。</span><span class="sxs-lookup"><span data-stu-id="5451c-111">The writer can use this to determine which backup operation is being shut down, if it has stored the shadow copy set ID during its backup sequence (for example, from within [**CVssWriter::OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze), [**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw), or [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) by using [**CVssWriter::GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid).</span></span>

<span data-ttu-id="5451c-112">不過，寫入器不應該從 [**CVssWriter：： OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)內呼叫 [**CVssWriter：： GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid) 。</span><span class="sxs-lookup"><span data-stu-id="5451c-112">However, a writer should not call [**CVssWriter::GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid) from within [**CVssWriter::OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown).</span></span> <span data-ttu-id="5451c-113">此外，在 [**CVssWriter：： OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)傳回之後，就無法呼叫 **CVssWriter：： GetCurrentSnapshotSetId** 。</span><span class="sxs-lookup"><span data-stu-id="5451c-113">Also, **CVssWriter::GetCurrentSnapshotSetId** cannot be called after [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) returns.</span></span>

<span data-ttu-id="5451c-114">寫入器有可能涉及多個備份作業，而且如果因為要求者突然關機而呼叫 BackupShutdown 事件，則傳回的 VSS \_ 識別碼可能是寫入器所參與的另一個備份作業。</span><span class="sxs-lookup"><span data-stu-id="5451c-114">It is possible for the writer to be involved in multiple backup operations, and if a BackupShutdown event is called because of an abrupt shutdown of a requester, the VSS\_ID returned could be that of another backup operation the writer was participating in.</span></span>

 

 



