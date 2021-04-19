---
description: 執行嚴重損壞修復的 VSS 備份和復原應用程式 (也稱為裸機復原) 可以搭配使用自動系統復原 (ASR) 寫入器和 Windows 預先安裝環境 (Windows PE) ，來備份及還原重要磁片區和可開機系統狀態的其他元件。 備份應用程式會實作為 VSS 要求者。
ms.assetid: 13adfd79-f26a-4385-9b59-129d06fa72eb
title: 使用 VSS 自動化系統復原進行嚴重損壞修復
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e31ef8ba223f40928e2422fa92240656f94592d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972041"
---
# <a name="using-vss-automated-system-recovery-for-disaster-recovery"></a><span data-ttu-id="c8fad-104">使用 VSS 自動化系統復原進行嚴重損壞修復</span><span class="sxs-lookup"><span data-stu-id="c8fad-104">Using VSS Automated System Recovery for Disaster Recovery</span></span>

<span data-ttu-id="c8fad-105">執行嚴重損壞修復的 VSS 備份和復原應用程式 (也稱為裸機復原) 可以搭配使用自動系統復原 (ASR) 寫入器和 Windows 預先安裝環境 (Windows PE) ，來備份及還原重要磁片區和可開機系統狀態的其他元件。</span><span class="sxs-lookup"><span data-stu-id="c8fad-105">A VSS backup-and-recovery application that performs disaster recovery (also called bare-metal recovery) can use the Automated System Recovery (ASR) writer together with Windows Preinstallation Environment (Windows PE) to back up and restore critical volumes and other components of the bootable system state.</span></span> <span data-ttu-id="c8fad-106">備份應用程式會實作為 VSS 要求者。</span><span class="sxs-lookup"><span data-stu-id="c8fad-106">The backup application is implemented as a VSS requester.</span></span>

<span data-ttu-id="c8fad-107">**注意**  使用 ASR 的應用程式必須 Windows PE 授權。</span><span class="sxs-lookup"><span data-stu-id="c8fad-107">**Note**  Applications that use ASR must license Windows PE.</span></span>

<span data-ttu-id="c8fad-108">**Windows Server 2003 和 WINDOWS XP：** ASR 不會實作為 VSS 寫入器。</span><span class="sxs-lookup"><span data-stu-id="c8fad-108">**Windows Server 2003 and Windows XP:** ASR is not implemented as a VSS writer.</span></span>

<span data-ttu-id="c8fad-109">如需可搭配 ASR 使用之追蹤工具的相關資訊，請參閱搭配 [使用追蹤工具與 VSS Asr 應用程式](using-tracing-tools-with-vss-asr-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="c8fad-109">For information about tracing tools that you can use with ASR, see [Using Tracing Tools with VSS ASR Applications](using-tracing-tools-with-vss-asr-applications.md).</span></span>

<span data-ttu-id="c8fad-110">**本文內容：**</span><span class="sxs-lookup"><span data-stu-id="c8fad-110">**In this article:**</span></span>

-   [<span data-ttu-id="c8fad-111">備份階段工作總覽</span><span class="sxs-lookup"><span data-stu-id="c8fad-111">Overview of Backup Phase Tasks</span></span>](#overview-of-backup-phase-tasks)
-   [<span data-ttu-id="c8fad-112">選擇要備份的重要元件</span><span class="sxs-lookup"><span data-stu-id="c8fad-112">Choosing Which Critical Components to Back Up</span></span>](#choosing-which-critical-components-to-back-up)
-   [<span data-ttu-id="c8fad-113">還原階段工作的總覽</span><span class="sxs-lookup"><span data-stu-id="c8fad-113">Overview of Restore Phase Tasks</span></span>](#overview-of-restore-phase-tasks)
-   [<span data-ttu-id="c8fad-114">排除磁片區的所有磁片</span><span class="sxs-lookup"><span data-stu-id="c8fad-114">Excluding All Disks for a Volume</span></span>](#excluding-all-disks-for-a-volume)

## <a name="overview-of-backup-phase-tasks"></a><span data-ttu-id="c8fad-115">備份階段工作總覽</span><span class="sxs-lookup"><span data-stu-id="c8fad-115">Overview of Backup Phase Tasks</span></span>

<span data-ttu-id="c8fad-116">在備份時，要求者會執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="c8fad-116">At backup time, the requester performs the following steps.</span></span>

> [!Note]  
> <span data-ttu-id="c8fad-117">除非另有指示，否則所有步驟都是必要的。</span><span class="sxs-lookup"><span data-stu-id="c8fad-117">All steps are required unless otherwise indicated.</span></span>

 

1.  <span data-ttu-id="c8fad-118">呼叫 [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) 函數來建立 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面的實例，並呼叫 [**>ivssbackupcomponents：： InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) 方法來初始化實例，以管理備份。</span><span class="sxs-lookup"><span data-stu-id="c8fad-118">Call the [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) function to create an instance of the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface and call the [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) method to initialize the instance to manage a backup.</span></span>
2.  <span data-ttu-id="c8fad-119">呼叫 [**>ivssbackupcomponents：： SetCoNtext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) 來設定陰影複製作業的內容。</span><span class="sxs-lookup"><span data-stu-id="c8fad-119">Call [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) to set the context for the shadow copy operation.</span></span>
3.  <span data-ttu-id="c8fad-120">呼叫 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) 來設定備份。</span><span class="sxs-lookup"><span data-stu-id="c8fad-120">Call [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) to configure the backup.</span></span> <span data-ttu-id="c8fad-121">將 *bBackupBootableSystemState* 參數設定為 **true** ，表示備份將包含可開機的系統狀態。</span><span class="sxs-lookup"><span data-stu-id="c8fad-121">Set the *bBackupBootableSystemState* parameter to **true** to indicate that the backup will include a bootable system state.</span></span>
4.  <span data-ttu-id="c8fad-122">選擇 ASR 寫入器的寫入器元資料檔案中要備份的重要元件，並為每個元件呼叫 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 。</span><span class="sxs-lookup"><span data-stu-id="c8fad-122">Choose which critical components in the ASR writer's Writer Metadata Document to back up and call [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) for each of them.</span></span>
5.  <span data-ttu-id="c8fad-123">呼叫 [**>ivssbackupcomponents：： StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) 來建立新的空白陰影複製集。</span><span class="sxs-lookup"><span data-stu-id="c8fad-123">Call [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) to create a new, empty shadow copy set.</span></span>
6.  <span data-ttu-id="c8fad-124">呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) ，以起始與寫入器的非同步連絡人。</span><span class="sxs-lookup"><span data-stu-id="c8fad-124">Call [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) to initiate asynchronous contact with writers.</span></span>
7.  <span data-ttu-id="c8fad-125">呼叫 [**>ivssbackupcomponents：： GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) ，以取出 ASR 寫入器的寫入器元資料檔案。</span><span class="sxs-lookup"><span data-stu-id="c8fad-125">Call [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) to retrieve the ASR writer's Writer Metadata Document.</span></span> <span data-ttu-id="c8fad-126">ASR 寫入器的寫入器識別碼是 BE000CBE-11FE-4426-9C58-531AA6355FC4，而寫入器名稱字串是「ASR Writer」。</span><span class="sxs-lookup"><span data-stu-id="c8fad-126">The writer ID for the ASR writer is BE000CBE-11FE-4426-9C58-531AA6355FC4, and the writer name string is "ASR Writer".</span></span>
8.  <span data-ttu-id="c8fad-127">呼叫 [**IVssExamineWriterMetadata：： SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) ，以儲存 ASR 寫入器的寫入器元資料檔案的複本。</span><span class="sxs-lookup"><span data-stu-id="c8fad-127">Call [**IVssExamineWriterMetadata::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) to save a copy of the ASR writer's Writer Metadata Document.</span></span>
9.  <span data-ttu-id="c8fad-128">針對可參與陰影複製的每個磁片區呼叫 [**>ivssbackupcomponents：： AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) ，以將磁片區新增至陰影複製集。</span><span class="sxs-lookup"><span data-stu-id="c8fad-128">Call [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) for each volume that can participate in shadow copies to add the volume to the shadow copy set.</span></span>
10. <span data-ttu-id="c8fad-129">呼叫 [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) 通知寫入器，以準備進行備份作業。</span><span class="sxs-lookup"><span data-stu-id="c8fad-129">Call [**IVssBackupComponents::PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) to notify writers to prepare for a backup operation.</span></span>
11. <span data-ttu-id="c8fad-130">呼叫 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 和 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (或 [**IVssBackupComponentsEx3：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex3-getwriterstatusex)) 驗證 ASR 寫入器的狀態。</span><span class="sxs-lookup"><span data-stu-id="c8fad-130">Call [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (or [**IVssBackupComponentsEx3::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex3-getwriterstatusex)) to verify the status of the ASR writer.</span></span>
12. <span data-ttu-id="c8fad-131">此時，您可以查詢作者在其 [**CVssWriter：： OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) 方法中所設定的失敗訊息。</span><span class="sxs-lookup"><span data-stu-id="c8fad-131">At this point, you can query for failure messages that were set by the writer in its [**CVssWriter::OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) method.</span></span> <span data-ttu-id="c8fad-132">如需顯示如何查看這些訊息的範例程式碼，請參閱 [**IVssComponentEx：： GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg)。</span><span class="sxs-lookup"><span data-stu-id="c8fad-132">For example code that shows how to view these messages, see [**IVssComponentEx::GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).</span></span>
13. <span data-ttu-id="c8fad-133">呼叫 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 來建立磁片區陰影複製。</span><span class="sxs-lookup"><span data-stu-id="c8fad-133">Call [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) to create a volume shadow copy.</span></span>
14. <span data-ttu-id="c8fad-134">呼叫 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 和 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) ，以驗證 ASR 寫入器的狀態。</span><span class="sxs-lookup"><span data-stu-id="c8fad-134">Call [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) to verify the status of the ASR writer.</span></span>
15. <span data-ttu-id="c8fad-135">備份資料。</span><span class="sxs-lookup"><span data-stu-id="c8fad-135">Back up the data.</span></span>
16. <span data-ttu-id="c8fad-136">藉由呼叫 [**>ivssbackupcomponents：： SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)來指出備份作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="c8fad-136">Indicate whether the backup operation succeeded by calling [**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded).</span></span>
17. <span data-ttu-id="c8fad-137">呼叫 [**>ivssbackupcomponents：： BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) ，表示備份作業已完成。</span><span class="sxs-lookup"><span data-stu-id="c8fad-137">Call [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) to indicate that the backup operation has completed.</span></span>
18. <span data-ttu-id="c8fad-138">呼叫 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 和 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)。</span><span class="sxs-lookup"><span data-stu-id="c8fad-138">Call [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).</span></span> <span data-ttu-id="c8fad-139">寫入器會話狀態記憶體是有限的資源，而寫入器最後必須重複使用會話狀態。</span><span class="sxs-lookup"><span data-stu-id="c8fad-139">The writer session state memory is a limited resource, and writers must eventually reuse session states.</span></span> <span data-ttu-id="c8fad-140">此步驟會將寫入器的備份會話狀態標示為已完成，並通知 VSS 此備份會話位置可以由後續的備份作業重複使用。</span><span class="sxs-lookup"><span data-stu-id="c8fad-140">This step marks the writer’s backup session state as completed and notifies VSS that this backup session slot can be reused by a subsequent backup operation.</span></span>
    > [!Note]  
    > <span data-ttu-id="c8fad-141">只有在 Windows Server 2008 Service Pack 2 (SP2) 及更早版本才需要此功能。</span><span class="sxs-lookup"><span data-stu-id="c8fad-141">This is only necessary on Windows Server 2008 with Service Pack 2 (SP2) and earlier.</span></span>

     

19. <span data-ttu-id="c8fad-142">呼叫 [**>ivssbackupcomponents：： SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) ，以儲存要求者備份元件檔的複本。</span><span class="sxs-lookup"><span data-stu-id="c8fad-142">Call [**IVssBackupComponents::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) to save a copy of the requester's Backup Components Document.</span></span> <span data-ttu-id="c8fad-143">當要求者呼叫 [**>ivssbackupcomponents：： InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) 方法時，會在還原時使用備份元件檔中的資訊。</span><span class="sxs-lookup"><span data-stu-id="c8fad-143">The information in the Backup Components Document is used at restore time when the requester calls the [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) method.</span></span>

## <a name="choosing-which-critical-components-to-back-up"></a><span data-ttu-id="c8fad-144">選擇要備份的重要元件</span><span class="sxs-lookup"><span data-stu-id="c8fad-144">Choosing Which Critical Components to Back Up</span></span>

<span data-ttu-id="c8fad-145">在備份初始化階段中，ASR 寫入器會在其寫入器元資料檔案中報告下列類型的元件：</span><span class="sxs-lookup"><span data-stu-id="c8fad-145">In the backup initialization phase, the ASR writer reports the following types of components in its Writer Metadata Document:</span></span>

-   <span data-ttu-id="c8fad-146">重要磁片區，例如開機、系統和 Windows 修復環境 (Windows RE) 磁片區，以及與目前正在執行的 Windows Vista 或 Windows Server 2008 實例相關聯的 Windows RE 磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="c8fad-146">Critical volumes, such as the boot, system, and Windows Recovery Environment (Windows RE) volumes and the Windows RE partition that is associated with the instance of Windows Vista or Windows Server 2008 that is currently running.</span></span> <span data-ttu-id="c8fad-147">如果磁片區包含系統狀態資訊，磁片區就是 *重要磁片* 區。</span><span class="sxs-lookup"><span data-stu-id="c8fad-147">A volume is a *critical volume* if it contains system state information.</span></span> <span data-ttu-id="c8fad-148">開機和系統磁碟區會自動包含在內。</span><span class="sxs-lookup"><span data-stu-id="c8fad-148">The boot and system volumes are included automatically.</span></span> <span data-ttu-id="c8fad-149">要求者必須包含包含寫入器所報告之系統關鍵元件的所有磁片區，例如包含 Active Directory 的磁片區。</span><span class="sxs-lookup"><span data-stu-id="c8fad-149">The requester must include all volumes that contain system-critical components reported by writers, such as the volumes that contain the Active Directory.</span></span> <span data-ttu-id="c8fad-150">系統關鍵元件會標示為「無法針對備份進行選取」。</span><span class="sxs-lookup"><span data-stu-id="c8fad-150">System-critical components are marked as "not selectable for backup."</span></span> <span data-ttu-id="c8fad-151">在 VSS 中，「不可選取」表示「非選擇性」。</span><span class="sxs-lookup"><span data-stu-id="c8fad-151">In VSS, "not selectable" means "not optional."</span></span> <span data-ttu-id="c8fad-152">因此，要求者必須將它們備份為系統狀態的一部分。</span><span class="sxs-lookup"><span data-stu-id="c8fad-152">Thus, the requester is required to back them up as part of system state.</span></span> <span data-ttu-id="c8fad-153">如需詳細資訊，請參閱 [備份和還原系統狀態](locating-additional-system-files.md)。</span><span class="sxs-lookup"><span data-stu-id="c8fad-153">For more information, see [Backing Up and Restoring System State](locating-additional-system-files.md).</span></span> <span data-ttu-id="c8fad-154">未 \_ 設定 VSS CF \_ 非 \_ 系統 \_ 狀態旗標的元件不是系統關鍵的。</span><span class="sxs-lookup"><span data-stu-id="c8fad-154">Components for which the VSS\_CF\_NOT\_SYSTEM\_STATE flag is set are not system-critical.</span></span>
    > [!Note]  
    > <span data-ttu-id="c8fad-155">ASR 元件是 ASR 寫入器所報告的系統關鍵元件。</span><span class="sxs-lookup"><span data-stu-id="c8fad-155">The ASR component is a system-critical component that is reported by the ASR writer.</span></span>

     

-   <span data-ttu-id="c8fad-156">磁片。</span><span class="sxs-lookup"><span data-stu-id="c8fad-156">Disks.</span></span> <span data-ttu-id="c8fad-157">電腦上的每個固定磁片都會公開為 ASR 中的元件。</span><span class="sxs-lookup"><span data-stu-id="c8fad-157">Every fixed disk on the computer is exposed as a component in ASR.</span></span> <span data-ttu-id="c8fad-158">如果在備份期間未排除磁片，則會在還原期間指派磁片，並且可以重新建立和重新格式化。</span><span class="sxs-lookup"><span data-stu-id="c8fad-158">If a disk was not excluded during backup, it will be assigned during restore and can be re-created and reformatted.</span></span> <span data-ttu-id="c8fad-159">請注意，在還原期間，要求者仍然可以藉由呼叫 [**>ivssbackupcomponents：： SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) 方法，重新建立在備份期間排除的磁片。</span><span class="sxs-lookup"><span data-stu-id="c8fad-159">Note that during restore, the requester can still re-create a disk that was excluded during backup by calling the [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method.</span></span> <span data-ttu-id="c8fad-160">如果選取了動態磁碟套件中的一個磁片，則也必須選取該套件中的所有其他磁片。</span><span class="sxs-lookup"><span data-stu-id="c8fad-160">If one disk in a dynamic disk pack is selected, all other disks in that pack must also be selected.</span></span> <span data-ttu-id="c8fad-161">如果選取磁片區是因為磁片區是重要磁片區 (也就是包含系統狀態資訊的磁片區) ，也必須選取包含該磁片區範圍的每個磁片。</span><span class="sxs-lookup"><span data-stu-id="c8fad-161">If a volume is selected because it is a critical volume (that is, a volume that contains system state information), every disk that contains an extent for that volume must also be selected.</span></span> <span data-ttu-id="c8fad-162">若要尋找磁片區的範圍，請使用 [**[ \_ IOCTL \_ \_ \_ 磁片區磁片 \_ 區磁片區**](/windows/win32/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents) 控制程式代碼]。</span><span class="sxs-lookup"><span data-stu-id="c8fad-162">To find the extents for a volume, use the [**IOCTL\_VOLUME\_GET\_VOLUME\_DISK\_EXTENTS**](/windows/win32/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents) control code.</span></span>

    > [!Note]  
    > <span data-ttu-id="c8fad-163">在備份期間，要求者應包含所有固定磁片。</span><span class="sxs-lookup"><span data-stu-id="c8fad-163">During backup, the requester should include all fixed disks.</span></span> <span data-ttu-id="c8fad-164">如果包含要求者備份組的磁片是本機磁片，則應包含此磁片。</span><span class="sxs-lookup"><span data-stu-id="c8fad-164">If the disk that contains the requester's backup set is a local disk, this disk should be included.</span></span> <span data-ttu-id="c8fad-165">在還原期間，要求者必須排除包含要求者之備份組的磁片，以防止其遭到覆寫。</span><span class="sxs-lookup"><span data-stu-id="c8fad-165">During restore, the requester must exclude the disk that contains the requester's backup set to prevent it from being overwritten.</span></span>

     

    <span data-ttu-id="c8fad-166">在叢集環境中，ASR 不會重新建立叢集共用磁片的版面配置。</span><span class="sxs-lookup"><span data-stu-id="c8fad-166">In a clustering environment, ASR does not re-create the layout of the cluster's shared disks.</span></span> <span data-ttu-id="c8fad-167">在 Windows RE 中還原作業系統之後，應該將這些磁片還原至線上。</span><span class="sxs-lookup"><span data-stu-id="c8fad-167">Those disks should be restored online after the operating system is restored in the Windows RE.</span></span>

-   <span data-ttu-id="c8fad-168">開機設定資料 (BCD) 存放區。</span><span class="sxs-lookup"><span data-stu-id="c8fad-168">Boot Configuration Data (BCD) store.</span></span> <span data-ttu-id="c8fad-169">此元件指定包含 BCD 存放區之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="c8fad-169">This component specifies the path of the directory that contains the BCD store.</span></span> <span data-ttu-id="c8fad-170">要求者必須指定此元件，並備份 BCD 存放區目錄中的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="c8fad-170">The requester must specify this component and back up all of the files in the BCD store directory.</span></span> <span data-ttu-id="c8fad-171">如需 BCD 存放區的詳細資訊，請參閱 [關於 bcd](/previous-versions/windows/desktop/bcd/about-bcd)。</span><span class="sxs-lookup"><span data-stu-id="c8fad-171">For more information about the BCD store, see [About BCD](/previous-versions/windows/desktop/bcd/about-bcd).</span></span>
    > [!Note]  
    > <span data-ttu-id="c8fad-172">在使用擴充固件介面 (EFI) 的電腦上，EFI 系統磁碟分割 (ESP) 一律會隱藏，不能包含在磁片區陰影複製中。</span><span class="sxs-lookup"><span data-stu-id="c8fad-172">On computers that use the Extended Firmware Interface (EFI), the EFI System Partition (ESP) is always hidden and cannot be included in a volume shadow copy.</span></span> <span data-ttu-id="c8fad-173">要求者必須備份此分割區的內容。</span><span class="sxs-lookup"><span data-stu-id="c8fad-173">The requester must back up the contents of this partition.</span></span> <span data-ttu-id="c8fad-174">由於此分割區不能包含在磁片區陰影複製中，因此只能從實際磁片區執行備份，而不是從陰影複製執行。</span><span class="sxs-lookup"><span data-stu-id="c8fad-174">Because this partition cannot be included in a volume shadow copy, the backup can only be performed from the live volume, not from the shadow copy.</span></span> <span data-ttu-id="c8fad-175">如需有關 EFI 和 ESP 的詳細資訊，請參閱 [帶出指南](/windows-hardware/drivers/bringup/)。</span><span class="sxs-lookup"><span data-stu-id="c8fad-175">For more information about EFI and ESP, see [Bring up guide](/windows-hardware/drivers/bringup/).</span></span>

<span data-ttu-id="c8fad-176">元件名稱使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="c8fad-176">The component names use the following formats:</span></span>

-   <span data-ttu-id="c8fad-177">若是磁片元件，格式為</span><span class="sxs-lookup"><span data-stu-id="c8fad-177">For disk components, the format is</span></span>

    <COMPONENT logicalPath="Disks" componentName="harddisk*n*" componentType="filegroup" />

    <span data-ttu-id="c8fad-178">其中 *n* 是磁片編號。</span><span class="sxs-lookup"><span data-stu-id="c8fad-178">where *n* is the disk number.</span></span> <span data-ttu-id="c8fad-179">只記錄磁片編號。</span><span class="sxs-lookup"><span data-stu-id="c8fad-179">Only the disk number is recorded.</span></span> <span data-ttu-id="c8fad-180">若要取得磁片編號，請使用 [**IOCTL \_ 儲存體 \_ 取得 \_ 裝置 \_ 編號**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) 控制程式代碼。</span><span class="sxs-lookup"><span data-stu-id="c8fad-180">To get the disk number, use the [**IOCTL\_STORAGE\_GET\_DEVICE\_NUMBER**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) control code.</span></span>

-   <span data-ttu-id="c8fad-181">若是磁片區元件，格式為</span><span class="sxs-lookup"><span data-stu-id="c8fad-181">For volume components, the format is</span></span>

    <COMPONENT logicalPath="Volumes" componentName="Volume{*GUID*}" componentType="filegroup" />

    <span data-ttu-id="c8fad-182">其中 *guid* 是磁片區 guid。</span><span class="sxs-lookup"><span data-stu-id="c8fad-182">where *GUID* is the volume GUID.</span></span>

-   <span data-ttu-id="c8fad-183">針對 BCD 存放區元件，格式為</span><span class="sxs-lookup"><span data-stu-id="c8fad-183">For the BCD store component, the format is</span></span>

    <COMPONENT logicalPath="BCD" componentName="BCD" componentType="filegroup" componentCaption = "This is the path to the boot BCD store and the boot managers...All the files in this directory need to be backed up...">

    <span data-ttu-id="c8fad-184">如果系統磁碟分割具有磁片區 GUID 名稱，此元件是可選取的。</span><span class="sxs-lookup"><span data-stu-id="c8fad-184">If the system partition has a volume GUID name, this component is selectable.</span></span> <span data-ttu-id="c8fad-185">否則，就無法選取。</span><span class="sxs-lookup"><span data-stu-id="c8fad-185">Otherwise, it is not selectable.</span></span>

    > [!Note]  
    > <span data-ttu-id="c8fad-186">ASR 會將檔案新增至 BCD 存放區元件的檔案群組，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c8fad-186">ASR adds the files to the BCD store component's file group as follows:</span></span>
    >
    > -   <span data-ttu-id="c8fad-187">EFI 磁片的 ASR 新增</span><span class="sxs-lookup"><span data-stu-id="c8fad-187">For EFI disks, ASR adds</span></span>
    >
    >     <span data-ttu-id="c8fad-188">*SystemPartitionPath* \\EFI \\ Microsoft \\ 開機 \\ \* 。\*</span><span class="sxs-lookup"><span data-stu-id="c8fad-188">*SystemPartitionPath*\\EFI\\Microsoft\\Boot\\\*.\*</span></span>
    >
    >     <span data-ttu-id="c8fad-189">其中 *SystemPartitionPath* 是系統磁碟分割的路徑。</span><span class="sxs-lookup"><span data-stu-id="c8fad-189">where *SystemPartitionPath* is the path to the system partition.</span></span>
    >
    > -   <span data-ttu-id="c8fad-190">針對 GPT 磁片，ASR 新增</span><span class="sxs-lookup"><span data-stu-id="c8fad-190">For GPT disks, ASR adds</span></span>
    >
    >     <span data-ttu-id="c8fad-191">*SystemPartitionPath* \\開機 \\ \* 。\*</span><span class="sxs-lookup"><span data-stu-id="c8fad-191">*SystemPartitionPath*\\Boot\\\*.\*</span></span>
    >
    >     <span data-ttu-id="c8fad-192">其中 *SystemPartitionPath* 是系統磁碟分割的路徑。</span><span class="sxs-lookup"><span data-stu-id="c8fad-192">where *SystemPartitionPath* is the path to the system partition.</span></span>
    >
    > -   <span data-ttu-id="c8fad-193">您可以在下列登錄機碼下找到系統磁碟分割路徑： **HKEY \_ LOCAL \_ MACHINE** \\ **system** \\ **Setup** \\ **SystemPartition**</span><span class="sxs-lookup"><span data-stu-id="c8fad-193">The system partition path can be found under the following registry key: **HKEY\_LOCAL\_MACHINE**\\**System**\\**Setup**\\**SystemPartition**</span></span>

     

<span data-ttu-id="c8fad-194">還原時，標記為重要磁片區的所有元件都必須還原。</span><span class="sxs-lookup"><span data-stu-id="c8fad-194">On restore, all components that are marked as critical volumes must be restored.</span></span> <span data-ttu-id="c8fad-195">如果無法還原一或多個重要磁片區，則還原作業會失敗。</span><span class="sxs-lookup"><span data-stu-id="c8fad-195">If one or more critical volumes cannot be restored, the restore operation fails.</span></span>

<span data-ttu-id="c8fad-196">在還原順序的 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) 階段中，不會重新建立備份期間未排除的磁片，並且預設會重新格式化。</span><span class="sxs-lookup"><span data-stu-id="c8fad-196">In the [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) phase of the restore sequence, disks that were not excluded during backup are re-created and reformatted by default.</span></span> <span data-ttu-id="c8fad-197">但是，如果它們符合下列條件，則不會重新建立或重新格式化它們：</span><span class="sxs-lookup"><span data-stu-id="c8fad-197">However, they are not re-created or reformatted if they meet the following conditions:</span></span>

-   <span data-ttu-id="c8fad-198">如果未變更磁片的磁片配置或只對其進行加法變更，則不會重新建立基本磁碟。</span><span class="sxs-lookup"><span data-stu-id="c8fad-198">A basic disk is not re-created if its disk layout is intact or only additive changes have been made to it.</span></span> <span data-ttu-id="c8fad-199">如果下列條件成立，則磁片配置會保持不變：</span><span class="sxs-lookup"><span data-stu-id="c8fad-199">The disk layout is intact if the following conditions are true:</span></span>
    -   <span data-ttu-id="c8fad-200">磁片簽章、磁片樣式 (GPT 或 MBR) 、邏輯磁區大小和磁片區開始位移都不會變更。</span><span class="sxs-lookup"><span data-stu-id="c8fad-200">The disk signature, disk style (GPT or MBR), logical sector size, and volume start offset are not changed.</span></span>
    -   <span data-ttu-id="c8fad-201">磁片區大小不會減少。</span><span class="sxs-lookup"><span data-stu-id="c8fad-201">The volume size is not decreased.</span></span>
    -   <span data-ttu-id="c8fad-202">若為 GPT 磁片，則不會變更分割區識別碼。</span><span class="sxs-lookup"><span data-stu-id="c8fad-202">For GPT disks, the partition identifier is not changed.</span></span>
-   <span data-ttu-id="c8fad-203">如果動態磁碟的磁片配置完好無損，或只對其進行了附加的變更，就不會重新建立動態磁碟。</span><span class="sxs-lookup"><span data-stu-id="c8fad-203">A dynamic disk is not re-created if its disk layout is intact or only additive changes have been made to it.</span></span> <span data-ttu-id="c8fad-204">若要讓動態磁碟保持不變，必須符合基本磁碟的所有條件。</span><span class="sxs-lookup"><span data-stu-id="c8fad-204">For a dynamic disk to be intact, all of the conditions for a basic disk must be met.</span></span> <span data-ttu-id="c8fad-205">此外，整個磁片套件的磁片區結構必須保持不變。</span><span class="sxs-lookup"><span data-stu-id="c8fad-205">In addition, the entire disk pack's volume structure must be intact.</span></span> <span data-ttu-id="c8fad-206">如果磁片套件符合下列條件（同時適用于 MBR 和 GPT 磁片），則磁片區的磁片區結構會保持不變：</span><span class="sxs-lookup"><span data-stu-id="c8fad-206">The disk pack's volume structure is intact if it meets the following conditions, which apply to both MBR and GPT disks:</span></span>
    -   <span data-ttu-id="c8fad-207">在還原期間，實體套件中可用的磁片區數目，必須大於或等於在備份期間于 ASR 寫入器中繼資料中指定的磁片區數目。</span><span class="sxs-lookup"><span data-stu-id="c8fad-207">The number of volumes that are available in the physical pack during restore must be greater than or equal to the number of volumes that were specified in the ASR writer metadata during backup.</span></span>
    -   <span data-ttu-id="c8fad-208">每個磁片區的 [*plex*](../vds/virtual-disk-service-glossary-all.md) 數目必須保持不變。</span><span class="sxs-lookup"><span data-stu-id="c8fad-208">The number of [*plexes*](../vds/virtual-disk-service-glossary-all.md) per volume must be unchanged.</span></span>
    -   <span data-ttu-id="c8fad-209">[*成員*](../vds/virtual-disk-service-glossary-all.md)數目必須保持不變。</span><span class="sxs-lookup"><span data-stu-id="c8fad-209">The number of [*members*](../vds/virtual-disk-service-glossary-all.md) must be unchanged.</span></span>
    -   <span data-ttu-id="c8fad-210">實體磁片區的數目必須大於 ASR 寫入器中繼資料中指定的磁片區數目。</span><span class="sxs-lookup"><span data-stu-id="c8fad-210">The number of physical disk extents must be greater than the number of disk extents specified in the ASR writer metadata.</span></span>
    -   <span data-ttu-id="c8fad-211">當新增其他磁片區，或將套件中的磁片區延伸 (例如，從簡單磁片區到跨距磁片區) 時，不完整的套件會維持不變。</span><span class="sxs-lookup"><span data-stu-id="c8fad-211">An intact pack remains intact when additional volumes are added, or if a volume in the pack is extended (for example, from a simple volume to a spanned volume).</span></span>
        > [!Note]  
        > <span data-ttu-id="c8fad-212">如果簡單磁片區已鏡像，套件就不會完整，並且會重新建立，以確保 BCD 和開機磁碟區狀態在還原之後仍維持一致。</span><span class="sxs-lookup"><span data-stu-id="c8fad-212">If a simple volume is mirrored, the pack is not intact and will be re-created to ensure that the BCD and boot volume state remain consistent after restore.</span></span> <span data-ttu-id="c8fad-213">如果刪除磁片區，則會重新建立該套件。</span><span class="sxs-lookup"><span data-stu-id="c8fad-213">If volumes are deleted, the pack is re-created.</span></span>

         
-   <span data-ttu-id="c8fad-214">如果動態磁碟套件的磁片區結構不完整，而且只對其進行了附加的變更，則不會重新建立套件中的磁片。</span><span class="sxs-lookup"><span data-stu-id="c8fad-214">If the dynamic disk pack's volume structure is intact and only additive changes have been made to it, the disks in the pack are not re-created.</span></span>

    <span data-ttu-id="c8fad-215">**Windows Vista：** 系統一律會重新建立動態磁碟。</span><span class="sxs-lookup"><span data-stu-id="c8fad-215">**Windows Vista:** Dynamic disks are always re-created.</span></span> <span data-ttu-id="c8fad-216">請注意，在 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 中，這種行為已有所變更。</span><span class="sxs-lookup"><span data-stu-id="c8fad-216">Note that this behavior has changed with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="c8fad-217">在還原階段開始之前的任何時間，要求者可以藉由設定 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** 登錄機碼，來指定磁片應快速格式化。</span><span class="sxs-lookup"><span data-stu-id="c8fad-217">At any time before the beginning of the restore phase, the requester can specify that the disks should be quick-formatted by setting the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**ASR**\\**RestoreSession** registry key.</span></span> <span data-ttu-id="c8fad-218">在此機碼下，有一個名為 **QuickFormat** 的值，其資料類型為 REG \_ DWORD。</span><span class="sxs-lookup"><span data-stu-id="c8fad-218">Under this key, there is a value named **QuickFormat** with the data type REG\_DWORD.</span></span> <span data-ttu-id="c8fad-219">如果此值不存在，您應該建立它。</span><span class="sxs-lookup"><span data-stu-id="c8fad-219">If this value does not exist, you should create it.</span></span> <span data-ttu-id="c8fad-220">將 **QuickFormat** 值的資料設定為1以進行快速格式化，或設定為0表示慢速格式。</span><span class="sxs-lookup"><span data-stu-id="c8fad-220">Set the data of the **QuickFormat** value to 1 for quick formatting or 0 for slow formatting.</span></span>

<span data-ttu-id="c8fad-221">如果 **QuickFormat** 值不存在，磁片的格式會變慢。</span><span class="sxs-lookup"><span data-stu-id="c8fad-221">If the **QuickFormat** value does not exist, the disks will be slow-formatted.</span></span>

<span data-ttu-id="c8fad-222">快速格式化的速度比慢速格式的速度快很多 (也稱為完整格式) 。</span><span class="sxs-lookup"><span data-stu-id="c8fad-222">Quick formatting is significantly faster than slow formatting (also called full formatting).</span></span> <span data-ttu-id="c8fad-223">不過，快速格式化不會驗證磁片區上的每個磁區。</span><span class="sxs-lookup"><span data-stu-id="c8fad-223">However, quick formatting does not verify each sector on the volume.</span></span>

## <a name="overview-of-restore-phase-tasks"></a><span data-ttu-id="c8fad-224">還原階段工作的總覽</span><span class="sxs-lookup"><span data-stu-id="c8fad-224">Overview of Restore Phase Tasks</span></span>

<span data-ttu-id="c8fad-225">在還原時，要求者會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="c8fad-225">At restore time, the requester performs the following steps:</span></span>

> [!Note]  
> <span data-ttu-id="c8fad-226">除非另有指示，否則所有步驟都是必要的。</span><span class="sxs-lookup"><span data-stu-id="c8fad-226">All steps are required unless otherwise indicated.</span></span>

 

1.  <span data-ttu-id="c8fad-227">呼叫 [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) 函式來建立 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面的實例，並呼叫 [**>ivssbackupcomponents：： InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) 方法，藉由將要求者的備份元件檔載入至實例，初始化實例以進行還原。</span><span class="sxs-lookup"><span data-stu-id="c8fad-227">Call the [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) function to create an instance of the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface and call the [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) method to initialize the instance for restore by loading the requester's Backup Components Document into the instance.</span></span>
2.  <span data-ttu-id="c8fad-228">\[只有當要求者需要變更是否為一或多個磁片指定 "IncludeDisk" 或 ">excludedisk.ps1" 時，才需要執行此步驟。 \] 呼叫 [**>ivssbackupcomponents：： SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) 來設定 ASR 寫入器元件的還原選項。</span><span class="sxs-lookup"><span data-stu-id="c8fad-228">\[This step is required only if the requester needs to change whether "IncludeDisk" or "ExcludeDisk" is specified for one or more disks.\] Call [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) to set the restore options for the ASR writer components.</span></span> <span data-ttu-id="c8fad-229">ASR 寫入器支援下列選項：「IncludeDisk」可讓要求者在目標系統上包含要考慮用於還原的磁片，即使在備份階段期間未選取該磁片也是如此。</span><span class="sxs-lookup"><span data-stu-id="c8fad-229">The ASR writer supports the following options: "IncludeDisk" allows the requester to include a disk on the target system to be considered for restore, even if it was not selected during the backup phase.</span></span> <span data-ttu-id="c8fad-230">">excludedisk.ps1" 可讓要求者防止目標系統上的磁片重新建立。</span><span class="sxs-lookup"><span data-stu-id="c8fad-230">"ExcludeDisk" allows the requester to prevent a disk on the target system from being re-created.</span></span> <span data-ttu-id="c8fad-231">請注意，如果為包含重要磁片區的磁片指定 ">excludedisk.ps1"，後續對 [**>ivssbackupcomponents：:P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) 的呼叫將會失敗。</span><span class="sxs-lookup"><span data-stu-id="c8fad-231">Note that if "ExcludeDisk" is specified for a disk that contains a critical volume, the subsequent call to [**IVssBackupComponents::PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) will fail.</span></span>

    <span data-ttu-id="c8fad-232">下列範例示範如何使用 [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) 來防止重新建立磁片0和磁片1，並將協力廠商驅動程式插入還原的開機磁碟區中。</span><span class="sxs-lookup"><span data-stu-id="c8fad-232">The following example shows how to use [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) to prevent disk 0 and disk 1 from being re-created and inject third-party drivers into the restored boot volume.</span></span>

    <span data-ttu-id="c8fad-233">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援插入協力廠商驅動程式。</span><span class="sxs-lookup"><span data-stu-id="c8fad-233">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** Injection of third-party drivers is not supported.</span></span>

    <span data-ttu-id="c8fad-234">此範例假設 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 指標 m \_ pBackupComponents 有效。</span><span class="sxs-lookup"><span data-stu-id="c8fad-234">The example assumes that the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) pointer, m\_pBackupComponents, is valid.</span></span>

    ```C++
        m_pBackupComponents->SetRestoreOptions(
            AsrWriterId,
            VSS_CT_FILEGROUP,
            NULL,
            TEXT("ASR"),
            TEXT("\"ExcludeDisk\"=\"0\", \"ExcludeDisk\"=\"1\" "),
            TEXT("\"InjectDrivers\"=\"1\" ")
            );
    ```

    

    <span data-ttu-id="c8fad-235">若要排除指定磁片區的所有磁片，請參閱下列「排除磁片區的所有磁片」。</span><span class="sxs-lookup"><span data-stu-id="c8fad-235">To exclude all disks for a specified volume, see the following "Excluding All Disks for a Volume."</span></span>

3.  <span data-ttu-id="c8fad-236">呼叫 [**>ivssbackupcomponents：:P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) ，以通知 ASR 寫入器準備進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="c8fad-236">Call [**IVssBackupComponents::PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) to notify the ASR writer to prepare for a restore operation.</span></span> <span data-ttu-id="c8fad-237">視需要呼叫 [**IVssAsync：： QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) ，直到 *pHrResult* 參數中傳回的狀態值不是 VSS \_ S \_ 非同步 \_ 暫止。</span><span class="sxs-lookup"><span data-stu-id="c8fad-237">Call [**IVssAsync::QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) as many times as necessary until the status value returned in the *pHrResult* parameter is not VSS\_S\_ASYNC\_PENDING.</span></span>
4.  <span data-ttu-id="c8fad-238">還原資料。</span><span class="sxs-lookup"><span data-stu-id="c8fad-238">Restore the data.</span></span> <span data-ttu-id="c8fad-239">在還原階段中，ASR 會將磁片區 GUID 路徑重新配置 (\\ \\ ？ \\磁片區 {GUID} ) 每個磁片區，以符合備份階段期間所使用的磁片區 GUID 路徑。</span><span class="sxs-lookup"><span data-stu-id="c8fad-239">In the restore phase, ASR reconfigures the volume GUID path (\\\\?\\Volume{GUID}) for each volume to match the volume GUID path that was used during the backup phase.</span></span> <span data-ttu-id="c8fad-240">但是，不會保留磁碟機號，因為這會導致與復原環境中自動指派的磁碟機號發生衝突。</span><span class="sxs-lookup"><span data-stu-id="c8fad-240">However, drive letters are not preserved, because this would cause collisions with the drive letters that are automatically assigned in the recovery environment.</span></span> <span data-ttu-id="c8fad-241">因此，當還原資料時，要求者必須使用磁片區 GUID 路徑，而不是磁碟機號，以存取磁片區。</span><span class="sxs-lookup"><span data-stu-id="c8fad-241">Thus, when restoring data, the requester must use volume GUID paths, not drive letters, to access the volumes.</span></span>
5.  <span data-ttu-id="c8fad-242">設定 **HKLM** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** 登錄機碼，以指出已還原或重新格式化的磁片區集合。</span><span class="sxs-lookup"><span data-stu-id="c8fad-242">Set the **HKLM**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**ASR**\\**RestoreSession** registry key to indicate the set of volumes that have been restored or reformatted.</span></span>

    <span data-ttu-id="c8fad-243">在此機碼下，有一個名為 **RestoredVolumes** 的值，其資料類型為 REG \_ 多重 \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="c8fad-243">Under this key, there is a value named **RestoredVolumes** with the data type REG\_MULTI\_SZ.</span></span> <span data-ttu-id="c8fad-244">如果此值不存在，您應該建立它。</span><span class="sxs-lookup"><span data-stu-id="c8fad-244">If this value does not exist, you should create it.</span></span> <span data-ttu-id="c8fad-245">在此值下，您的要求者應該針對已還原的每個磁片區建立磁片區 GUID 專案。</span><span class="sxs-lookup"><span data-stu-id="c8fad-245">Under this value, your requester should create a volume GUID entry for each volume that has been restored.</span></span> <span data-ttu-id="c8fad-246">此專案應該採用下列格式： \\ \\ ？ \\磁片區 {78618c8f-aefd-11da-a898-806e6f6e6963}。</span><span class="sxs-lookup"><span data-stu-id="c8fad-246">This entry should be in the following format: \\\\?\\Volume{78618c8f-aefd-11da-a898-806e6f6e6963}.</span></span> <span data-ttu-id="c8fad-247">每次執行裸機復原時，ASR 都會將 **RestoredVolumes** 值設定為 asr 還原的磁片區集合。</span><span class="sxs-lookup"><span data-stu-id="c8fad-247">Each time a bare-metal recovery is performed, ASR sets the **RestoredVolumes** value to the set of volumes that ASR restored.</span></span> <span data-ttu-id="c8fad-248">如果要求者已還原其他磁片區，則應該將此值設定為要求者還原之磁片區集的聯集，以及 ASR 還原的磁片區集合。</span><span class="sxs-lookup"><span data-stu-id="c8fad-248">If the requester restored additional volumes, it should set this value to the union of the set of volumes that the requester restored and the set of volumes that ASR restored.</span></span> <span data-ttu-id="c8fad-249">如果要求者未使用 ASR，則應取代磁片區清單。</span><span class="sxs-lookup"><span data-stu-id="c8fad-249">If the requester did not use ASR, it should replace the list of volumes.</span></span>

    <span data-ttu-id="c8fad-250">您也應該建立名為 **LastInstance** 的值，其資料類型為 REG \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="c8fad-250">You should also create a value named **LastInstance** with the data type REG\_SZ.</span></span> <span data-ttu-id="c8fad-251">此索引鍵應該包含可唯一識別目前還原作業的隨機 cookie。</span><span class="sxs-lookup"><span data-stu-id="c8fad-251">This key should contain a random cookie that uniquely identifies the current restore operation.</span></span> <span data-ttu-id="c8fad-252">您可以使用 [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) 和 [**UuidToString**](/windows/win32/api/rpcdce/nf-rpcdce-uuidtostring) 函數來建立這類 cookie。</span><span class="sxs-lookup"><span data-stu-id="c8fad-252">Such a cookie can be created by using the [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) and [**UuidToString**](/windows/win32/api/rpcdce/nf-rpcdce-uuidtostring) functions.</span></span> <span data-ttu-id="c8fad-253">每次執行裸機復原時，ASR 都會重設此登錄值，以通知要求者和非 VSS 備份應用程式已發生復原。</span><span class="sxs-lookup"><span data-stu-id="c8fad-253">Each time a bare-metal recovery is performed, ASR resets this registry value to notify requesters and non-VSS backup applications that the recovery has occurred.</span></span>

6.  <span data-ttu-id="c8fad-254">呼叫 [**>ivssbackupcomponents：:P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) 指出還原作業的結束。</span><span class="sxs-lookup"><span data-stu-id="c8fad-254">Call [**IVssBackupComponents::PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) to indicate the end of the restore operation.</span></span> <span data-ttu-id="c8fad-255">視需要呼叫 [**IVssAsync：： QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) ，直到 *pHrResult* 參數中傳回的狀態值不是 VSS \_ S \_ 非同步 \_ 暫止。</span><span class="sxs-lookup"><span data-stu-id="c8fad-255">Call [**IVssAsync::QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) as many times as necessary until the status value returned in the *pHrResult* parameter is not VSS\_S\_ASYNC\_PENDING.</span></span>

<span data-ttu-id="c8fad-256">在還原階段中，ASR 可能會建立或移除磁碟分割，以將電腦還原為先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="c8fad-256">In the restore phase, ASR may create or remove partitions to restore the computer to its previous state.</span></span> <span data-ttu-id="c8fad-257">要求者不能嘗試將備份階段的磁片編號對應到還原階段。</span><span class="sxs-lookup"><span data-stu-id="c8fad-257">Requesters must not attempt to map disk numbers from the backup phase to the restore phase.</span></span>

<span data-ttu-id="c8fad-258">在還原時，要求者必須排除包含要求者之備份組的磁片。</span><span class="sxs-lookup"><span data-stu-id="c8fad-258">On restore, the requester must exclude the disk that contains the requester's backup set.</span></span> <span data-ttu-id="c8fad-259">否則，還原作業可能會覆寫備份組。</span><span class="sxs-lookup"><span data-stu-id="c8fad-259">Otherwise, the backup set can be overwritten by the restore operation.</span></span>

<span data-ttu-id="c8fad-260">還原時，如果在備份期間未將磁片選為元件，或在還原期間以 ">excludedisk.ps1" 選項呼叫 [**>ivssbackupcomponents：： SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) 來明確排除磁片，則會排除該磁片。</span><span class="sxs-lookup"><span data-stu-id="c8fad-260">On restore, a disk is excluded if it was not selected as a component during backup, or if it is explicitly excluded by calling [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) with the "ExcludeDisk" option during restore.</span></span>

<span data-ttu-id="c8fad-261">請務必注意，在 WinPE 嚴重損壞修復期間，ASR 寫入器功能存在，但沒有其他寫入器可供使用，且 VSS 服務未執行。</span><span class="sxs-lookup"><span data-stu-id="c8fad-261">It is important to note that during WinPE disaster recovery, ASR writer functionality is present, but no other writers are available, and the VSS service is not running.</span></span> <span data-ttu-id="c8fad-262">在 WinPE 嚴重損壞修復完成之後，電腦就會重新開機，而 Windows 作業系統會正常執行，VSS 服務可以啟動，而且要求者可以執行任何額外的還原作業，而這些作業需要使用 ASR 寫入器以外的寫入器。</span><span class="sxs-lookup"><span data-stu-id="c8fad-262">After WinPE disaster recovery has completed, the computer has restarted, and the Windows operating system is running normally, the VSS service can be started, and the requester can perform any additional restore operations that require participation of writers other than the ASR writer.</span></span>

<span data-ttu-id="c8fad-263">如果在還原會話期間，備份應用程式會偵測到磁片區唯一識別碼未變更，因此，從備份時間開始的所有磁片區在 WinPE 中都是不變的，因此備份應用程式可以繼續只復原磁碟區的內容，而不涉及 ASR。</span><span class="sxs-lookup"><span data-stu-id="c8fad-263">If during the restore session the backup application detects that the volume unique IDs are unchanged, and therefore all volumes from the time of the backup are present and intact in WinPE, the backup application can proceed to restore only the contents of the volumes, without involving ASR.</span></span> <span data-ttu-id="c8fad-264">在此情況下，備份應用程式應該會在還原的作業系統中設定下列登錄機碼來指出電腦已還原： **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession**</span><span class="sxs-lookup"><span data-stu-id="c8fad-264">In this case, the backup application should indicate that the computer was restored by setting the following registry key in the restored operating system: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**ASR**\\**RestoreSession**</span></span>

<span data-ttu-id="c8fad-265">在此機碼下，指定值名稱的 **LastInstance** 、實 \_ 值型別的 REG SZ，以及隨機的 Cookie (例如 [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate)) 函數針對值資料所建立的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c8fad-265">Under this key, specify **LastInstance** for the value name, REG\_SZ for the value type, and a random cookie (such as a GUID created by the [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) function) for the value data.</span></span>

<span data-ttu-id="c8fad-266">如果在還原會話期間，備份應用程式會偵測到一或多個磁片區已變更或遺失，則備份應用程式應該使用 ASR 來執行還原。</span><span class="sxs-lookup"><span data-stu-id="c8fad-266">If during the restore session the backup application detects that one or more volumes are changed or missing, the backup application should use ASR to perform the restore.</span></span> <span data-ttu-id="c8fad-267">ASR 會在備份時以完全相同的方式重新建立磁片區，並設定 **RestoreSession** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="c8fad-267">ASR will re-create the volumes exactly the way they were at the time of the backup and set the **RestoreSession** registry key.</span></span>

## <a name="excluding-all-disks-for-a-volume"></a><span data-ttu-id="c8fad-268">排除磁片區的所有磁片</span><span class="sxs-lookup"><span data-stu-id="c8fad-268">Excluding All Disks for a Volume</span></span>

<span data-ttu-id="c8fad-269">下列範例顯示如何排除指定磁片區的所有磁片。</span><span class="sxs-lookup"><span data-stu-id="c8fad-269">The following example shows how to exclude all disks for a specified volume.</span></span>


```C++
HRESULT BuildRestoreOptionString
(
    const WCHAR             *pwszVolumeNamePath,
    CMyString               *pstrExclusionList
)
{
    HANDLE                  hVolume           = INVALID_HANDLE_VALUE;
    DWORD                   cbSize            = 0;
    VOLUME_DISK_EXTENTS     * pExtents        = NULL;
    DISK_EXTENT             * pExtent         = NULL;
    ULONG                   i                 = 0;
    BOOL                    fIoRet            = FALSE;
    WCHAR                   wszDest[MAX_PATH] = L"";
    CMyString               strVolumeName;
    CMyString               strRestoreOption;

    // Open a handle to the volume device.
    strVolumeName.Set( pwszVolumeNamePath );
    // If the volume name contains a trailing backslash, remove it.
    strVolumeName.UnTrailing( L'\\' );
    hVolume = ::CreateFile(strVolumeName, 0, FILE_SHARE_READ | FILE_SHARE_WRITE, NULL, OPEN_EXISTING, NULL, 0);
    // Check whether the call to CreateFile succeeded.

    // Get the list of disks used by this volume.
    cbSize = sizeof(VOLUME_DISK_EXTENTS);
    pExtents = (VOLUME_DISK_EXTENTS *)::CoTaskMemAlloc(cbSize);

    ::ZeroMemory(pExtents, cbSize);

    fIoRet = ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
    if ( !fIoRet && GetLastError() == ERROR_MORE_DATA )
    {
        // Allocate more memory.
        cbSize = FIELD_OFFSET(VOLUME_DISK_EXTENTS, Extents) + pExtents->NumberOfDiskExtents * sizeof(DISK_EXTENT);
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;

        pExtents = (VOLUME_DISK_EXTENTS *) ::CoTaskMemAlloc(cbSize);
        // Check whether CoTaskMemAlloc returned an out-of-memory error.
        ::ZeroMemory(pExtents, cbSize);

        // Now the buffer should be big enough.
        ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
        // Check whether the IOCTL succeeded.
    }
    // Check for errors; note that the IOCTL can fail for a reason other than insufficient memory.

    // For each disk, mark it to be excluded in the Restore Option string.
    for (i = 0; i < pExtents->NumberOfDiskExtents; i++)
    {
        pExtent = &pExtents->Extents[i];

        *wszDest = L'\0';
        StringCchPrintf(wszDest, MAX_PATH, L"\"ExcludeDisk\"=\"%d\", ", pExtent->DiskNumber); // check errors

        strRestoreOption.Append(wszDest);
        // Check for an out-of-memory error.
    }

    // Remove the trailing comma.
    strRestoreOption.TrimRight();
    strRestoreOption.UnTrailing(',');

    // Set the output parameter.
    strRestoreOption.Transfer( pstrExclusionList );

Exit:
    if( pExtents )
    {
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;
    }

    if( hVolume != INVALID_HANDLE_VALUE )
    {
        ::CloseHandle(hVolume);
        hVolume = INVALID_HANDLE_VALUE;
    }

    return ( hr );
}

```



 

 
