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
# <a name="determining-writer-status"></a><span data-ttu-id="e22b5-103">判斷寫入器狀態</span><span class="sxs-lookup"><span data-stu-id="e22b5-103">Determining Writer Status</span></span>

<span data-ttu-id="e22b5-104">要求者在建立陰影複製時，以及在備份和還原作業期間，都必須有充分定義的寫入器狀態。</span><span class="sxs-lookup"><span data-stu-id="e22b5-104">A requester needs to have a well-defined understanding about the status of the writer that participates with it during shadow copy creation, and during backup and restore operations.</span></span> <span data-ttu-id="e22b5-105">若要這樣做，建議您：</span><span class="sxs-lookup"><span data-stu-id="e22b5-105">To do so, it is recommended:</span></span>

-   <span data-ttu-id="e22b5-106">要求者會使用 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus)、 [**>ivssbackupcomponents：： GetWriterStatusCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount)和 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)。</span><span class="sxs-lookup"><span data-stu-id="e22b5-106">Requesters use [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents::GetWriterStatusCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount), and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).</span></span>
-   <span data-ttu-id="e22b5-107">如如何 [處理 Vss 下的備份](overview-of-processing-a-backup-under-vss.md) 和在 [Vss 下處理還原](overview-of-processing-a-restore-under-vss.md)的總覽所述，這些方法在以妥善定義的備份或還原順序呼叫時最為有用。</span><span class="sxs-lookup"><span data-stu-id="e22b5-107">As described in [Overview of Processing a Backup Under VSS](overview-of-processing-a-backup-under-vss.md) and [Overview of Processing a Restore Under VSS](overview-of-processing-a-restore-under-vss.md), these methods are most useful when called in a well-defined backup or restore sequence.</span></span> <span data-ttu-id="e22b5-108">一般來說，這表示在要求者完成其中一個工作並產生 VSS 事件之後，就應該查詢寫入器。</span><span class="sxs-lookup"><span data-stu-id="e22b5-108">Typically, this means that the writers should be queried after a requester has completed one of its tasks and generated a VSS event.</span></span>

    <span data-ttu-id="e22b5-109">處理備份時，要求者應在完成下列方法之後查詢寫入器。</span><span class="sxs-lookup"><span data-stu-id="e22b5-109">When processing a backup, a requester should query a writer following the completion of the following methods.</span></span> <span data-ttu-id="e22b5-110">要求者必須在呼叫 [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)之後呼叫 [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) ，使寫入器會話設定為已完成狀態。</span><span class="sxs-lookup"><span data-stu-id="e22b5-110">Requesters must call [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) after calling [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) to cause the writer session to be set to a completed state.</span></span>

    > [!Note]  
    > <span data-ttu-id="e22b5-111">只有在 Windows Server 2008 Service Pack 2 (SP2) 及更早版本才需要此功能。</span><span class="sxs-lookup"><span data-stu-id="e22b5-111">This is only necessary on Windows Server 2008 with Service Pack 2 (SP2) and earlier.</span></span>

     

    <dl> <dt>

[<span data-ttu-id="e22b5-112">**>ivssbackupcomponents：:P repareForBackup**</span><span class="sxs-lookup"><span data-stu-id="e22b5-112">**IVssBackupComponents::PrepareForBackup**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)
</dt> <dt>

[<span data-ttu-id="e22b5-113">**>ivssbackupcomponents：:D oSnapshotSet**</span><span class="sxs-lookup"><span data-stu-id="e22b5-113">**IVssBackupComponents::DoSnapshotSet**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
</dt> <dt>

[<span data-ttu-id="e22b5-114">**>ivssbackupcomponents：： BackupComplete**</span><span class="sxs-lookup"><span data-stu-id="e22b5-114">**IVssBackupComponents::BackupComplete**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
</dt> </dl>

<span data-ttu-id="e22b5-115">在還原作業期間，要求者應該在完成這些方法之後查詢寫入器：</span><span class="sxs-lookup"><span data-stu-id="e22b5-115">During restore operations, a requester should query a writer after completion of these methods:</span></span>
<dl> <dt>

[<span data-ttu-id="e22b5-116">**>ivssbackupcomponents：:P reRestore**</span><span class="sxs-lookup"><span data-stu-id="e22b5-116">**IVssBackupComponents::PreRestore**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
</dt> <dt>

[<span data-ttu-id="e22b5-117">**>ivssbackupcomponents：:P ostRestore**</span><span class="sxs-lookup"><span data-stu-id="e22b5-117">**IVssBackupComponents::PostRestore**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)
</dt> </dl>

-   <span data-ttu-id="e22b5-118">[**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus)的呼叫不是定義完善之備份或還原順序的一部分，因此不會提供寫入器狀態的可靠圖片，因為它們可能會反映不表示目前作業失敗的條件，例如：</span><span class="sxs-lookup"><span data-stu-id="e22b5-118">Calls to [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) that are not part of a well-defined backup or restore sequence do not provide a reliable picture of writer status, because they might reflect conditions that do not indicate failure in the current operation, such as:</span></span>
    -   <span data-ttu-id="e22b5-119">先前的陰影複製建立失敗</span><span class="sxs-lookup"><span data-stu-id="e22b5-119">A failure of a previous shadow copy creation</span></span>
    -   <span data-ttu-id="e22b5-120">提早備份或還原作業發生錯誤</span><span class="sxs-lookup"><span data-stu-id="e22b5-120">An error in an early backup or restore operation</span></span>
    -   <span data-ttu-id="e22b5-121">目前正在處理事件的沒有回應的寫入器</span><span class="sxs-lookup"><span data-stu-id="e22b5-121">An unresponsive writer currently processing an event</span></span>

<span data-ttu-id="e22b5-122">因此，開發人員不應該依賴進程的其他處理常式傳回的寫入器狀態，然後再嘗試以另一個 (可能在不同的執行緒) 來監視 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面的某個實例的進度。</span><span class="sxs-lookup"><span data-stu-id="e22b5-122">Therefore, developers should not rely on writer status returned by processes other then the requester or attempt to monitor the progress of one instance of the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface with another (possibly in a separate thread).</span></span>

<span data-ttu-id="e22b5-123">請注意，針對備份作業（需要檢查寫入器的寫入器元資料檔案），在產生和處理 [**>ivssbackupcomponents：： GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)所造成的 [*識別*](vssgloss-i.md)事件之後，不需要要求者呼叫 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus)和 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) 。</span><span class="sxs-lookup"><span data-stu-id="e22b5-123">Note that for backup operations, where it is necessary to examine writers' Writer Metadata Documents, there is no need for a requester call to [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) following the generation and handling of the [*Identify*](vssgloss-i.md) event caused by [**IVssBackupComponents::GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).</span></span>

<span data-ttu-id="e22b5-124">[**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) 只會報告這些寫入器的狀態，而這些寫入器的中繼資料是由寫入器 [*識別*](vssgloss-i.md) 事件處理常式（ [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (，並由 [**>ivssbackupcomponents：： GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) 和 [**>ivssbackupcomponents：： GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)) 傳回給要求者。</span><span class="sxs-lookup"><span data-stu-id="e22b5-124">[**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) reports only the status of those writers whose metadata was provided to VSS by writers' [*Identify*](vssgloss-i.md) event handlers, [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (and returned to the requester by [**IVssBackupComponents::GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) and [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)).</span></span>

<span data-ttu-id="e22b5-125">如果寫入器的 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 執行失敗，該寫入器的中繼資料將不會是提供給 VSS 的寫入器元資料檔案清單的一部分，也不會提供任何狀態資訊，而且呼叫會是多餘的。</span><span class="sxs-lookup"><span data-stu-id="e22b5-125">If a writer's implementation of [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) fails, that writer's metadata will not be part of the list of Writer Metadata Documents provided to VSS, no status information will be available, and the call would be redundant.</span></span>

<span data-ttu-id="e22b5-126">若為還原作業，要求者不需要檢查執行中寫入器的寫入器元資料檔案，則呼叫 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 和 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) 可能是更有效率的方式來判斷正在執行的寫入器。</span><span class="sxs-lookup"><span data-stu-id="e22b5-126">For restore operations, where the requester does not need to examine Writer Metadata Documents of executing writers, calling [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) may be a more efficient way to determine which writers are executing.</span></span>

 

 



