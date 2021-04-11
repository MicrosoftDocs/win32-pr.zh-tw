---
description: 備份元件檔是由 >ivssbackupcomponents 介面的實例所維護。
ms.assetid: 8c7ebba8-58c4-4733-ba59-802abf902c5e
title: 備份元件檔內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e12c88ebffa0037702e1f30dd818d4fd23fe4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852655"
---
# <a name="backup-components-document-contents"></a><span data-ttu-id="b20db-103">備份元件檔內容</span><span class="sxs-lookup"><span data-stu-id="b20db-103">Backup Components Document Contents</span></span>

<span data-ttu-id="b20db-104">備份元件檔是由 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面的實例所維護。</span><span class="sxs-lookup"><span data-stu-id="b20db-104">The Backup Components Document is maintained by instances of the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface.</span></span> <span data-ttu-id="b20db-105">此介面也包含許多用來控制備份作業、操作陰影複製，以及查詢系統狀態的方法。</span><span class="sxs-lookup"><span data-stu-id="b20db-105">This interface also contains numerous methods for controlling backup operations, manipulating shadow copies, and querying the system state.</span></span> <span data-ttu-id="b20db-106">但是，並非所有檔的資訊都可以透過這個介面直接存取。</span><span class="sxs-lookup"><span data-stu-id="b20db-106">However, not all of the document's information is directly accessible through this interface.</span></span>

<span data-ttu-id="b20db-107">備份元件檔是由數個資料集所組成：</span><span class="sxs-lookup"><span data-stu-id="b20db-107">The Backup Components Document consists of several sets of data:</span></span>

-   <span data-ttu-id="b20db-108">備份或還原作業中明確包含哪些元件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b20db-108">Information about which components were explicitly included in a backup or restore operation</span></span>
-   <span data-ttu-id="b20db-109">預存元件和寫入器資訊的標記法</span><span class="sxs-lookup"><span data-stu-id="b20db-109">A representation of the stored component and writer information</span></span>
-   <span data-ttu-id="b20db-110">備份/復原操作的相關狀態資訊</span><span class="sxs-lookup"><span data-stu-id="b20db-110">State information about the backup/recover operation</span></span>

<span data-ttu-id="b20db-111">雖然要求者和寫入器都可以使用元件資訊，但是只有寫入器可以存取狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="b20db-111">While the component information is available to both the requester and the writer, only the writer has access to the state information.</span></span>

## <a name="component-inclusion-information"></a><span data-ttu-id="b20db-112">元件包含資訊</span><span class="sxs-lookup"><span data-stu-id="b20db-112">Component Inclusion Information</span></span>

<span data-ttu-id="b20db-113">備份元件檔包含由要求者明確包含在備份和還原中的元件清單。</span><span class="sxs-lookup"><span data-stu-id="b20db-113">The Backup Components Document contains a list of those components explicitly included in backup and restore by the requester.</span></span> <span data-ttu-id="b20db-114">此清單包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="b20db-114">The list contains the following:</span></span>

-   <span data-ttu-id="b20db-115">明確包含可 [*選取的元件*](vssgloss-s.md)。</span><span class="sxs-lookup"><span data-stu-id="b20db-115">Explicitly included [*selectable components*](vssgloss-s.md).</span></span>

    <span data-ttu-id="b20db-116">在備份作業中包含這些檔案，是由 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 和 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)的 restore 作業所表示。</span><span class="sxs-lookup"><span data-stu-id="b20db-116">The inclusion of these files in backup operations is indicated by [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) and in restore operations by [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).</span></span>

-   <span data-ttu-id="b20db-117">適用于備份子元件的其，沒有可選取的備份元件上階。</span><span class="sxs-lookup"><span data-stu-id="b20db-117">Nonselectable for backup subcomponents without a selectable for backup component ancestor.</span></span>

    <span data-ttu-id="b20db-118">如果要在作業中包含任何寫入器元件，則必須包含所有這些元件。</span><span class="sxs-lookup"><span data-stu-id="b20db-118">All of these components must be included if any components of the writer are to be included in the operation.</span></span> <span data-ttu-id="b20db-119">在備份作業中包含這些檔案，是由 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 和 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)的 restore 作業所表示。</span><span class="sxs-lookup"><span data-stu-id="b20db-119">The inclusion of these files in backup operations is indicated by [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) and in restore operations by [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).</span></span>

-   <span data-ttu-id="b20db-120">隱含新增至備份 ([*子*](vssgloss-s.md) 元件的元件) 可 [*供還原*](vssgloss-s.md) 並明確地新增至還原。</span><span class="sxs-lookup"><span data-stu-id="b20db-120">Components implicitly added to the backup ([*subcomponents*](vssgloss-s.md)) that are [*selectable for restore*](vssgloss-s.md) and are explicitly added to the restore.</span></span>

    <span data-ttu-id="b20db-121">這些元件可以是可選取的或其，但是具有可選取的上階，用來以隱含方式選取它們進行備份。</span><span class="sxs-lookup"><span data-stu-id="b20db-121">These components may be either selectable or nonselectable, but have a selectable ancestor that was used to implicitly select them for backup.</span></span> <span data-ttu-id="b20db-122">[**>ivssbackupcomponents：： AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)會將它們新增至備份元件檔。</span><span class="sxs-lookup"><span data-stu-id="b20db-122">They are added to the Backup Components Document by [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).</span></span>

<span data-ttu-id="b20db-123">還原中隱含包含的元件身分識別不會儲存在備份元件檔中。</span><span class="sxs-lookup"><span data-stu-id="b20db-123">The identities of components implicitly included in the restore are not stored in the Backup Components Document.</span></span>

<span data-ttu-id="b20db-124">VSS 可以存取元件包含的資訊：在還原或備份中未明確包含任何元件的寫入器，在產生 [*PrepareForBackup*](vssgloss-p.md) 或 [*PreRestore*](vssgloss-p.md) 事件之後，不會收到任何 VSS 事件。</span><span class="sxs-lookup"><span data-stu-id="b20db-124">VSS has access to information about component inclusion: writers with no components explicitly included in a restore or backup receive no VSS events following the generation of the [*PrepareForBackup*](vssgloss-p.md) or [*PreRestore*](vssgloss-p.md) events.</span></span>

<span data-ttu-id="b20db-125">寫入器無法直接查詢此資訊。</span><span class="sxs-lookup"><span data-stu-id="b20db-125">Writers cannot directly query this information.</span></span> <span data-ttu-id="b20db-126">這並不是很大的限制，因為依設計，個別的 VSS 寫入器應該不需要有關系統上其他寫入器狀態的詳細資訊，如上面所述，沒有包含元件的系統將不需要參與 VSS 作業。</span><span class="sxs-lookup"><span data-stu-id="b20db-126">This is not a significant limitation because by design, individual VSS writers should not require detailed information about the status of other writers on the system and, as noted above, those with no included components will not have to participate in the VSS operation.</span></span>

<span data-ttu-id="b20db-127">要求者可以判斷哪些元件已明確包含在作業中。</span><span class="sxs-lookup"><span data-stu-id="b20db-127">A requester can determine which components have been explicitly included in an operation.</span></span>

<span data-ttu-id="b20db-128">[**>ivssbackupcomponents：： GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount)方法會傳回 (儲存在備份元件檔中之元件資訊的寫入器數目，而不是檔) 中的元件數目。</span><span class="sxs-lookup"><span data-stu-id="b20db-128">The [**IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) method returns the number of writers with component information stored in the Backup Components Document (and not the number of components in the document).</span></span>

<span data-ttu-id="b20db-129">要求者會使用 [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)透過預存寫入器資訊來編制索引，以傳回 [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="b20db-129">The requester indexes through the stored writer information using [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents), which returns instances of the [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) interface.</span></span> <span data-ttu-id="b20db-130">**IVssWriterComponentsExt** 介面可讓要求者取得參與寫入 [*器的寫入器類別*](vssgloss-w.md)和 [*寫入器實例*](vssgloss-w.md)，以及存取儲存在備份元件檔中之元件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b20db-130">The **IVssWriterComponentsExt** interface allows the requester to obtain the [*writer class*](vssgloss-w.md) and [*writer instance*](vssgloss-w.md) of participating writers, as well as to access information about those of its components stored in the Backup Components Document.</span></span>

## <a name="information-on-included-components"></a><span data-ttu-id="b20db-131">內含元件的資訊</span><span class="sxs-lookup"><span data-stu-id="b20db-131">Information on Included Components</span></span>

<span data-ttu-id="b20db-132">備份元件檔表示元件資料 (，其中不包含路徑和檔案規格資訊) ，可透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面的實例來存取。</span><span class="sxs-lookup"><span data-stu-id="b20db-132">The Backup Components Document's representation of the component data (which does not include path and file specification information), which is accessed through instances of the [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface.</span></span>

<span data-ttu-id="b20db-133">要求者和寫入器會以不同方式取得 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面實例的存取權。</span><span class="sxs-lookup"><span data-stu-id="b20db-133">Requesters and writers obtain access to instances of the [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface in different ways.</span></span>

<span data-ttu-id="b20db-134">要求者會使用 [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)所傳回之 [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext)介面的實例，依寫入器檢查寫入器上的元件資料。</span><span class="sxs-lookup"><span data-stu-id="b20db-134">A requester examines component data on a writer by writer basis by using instances of the [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) interface returned by [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).</span></span>

<span data-ttu-id="b20db-135">除了寫入器識別資訊之外， [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) 介面還提供 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面實例的陣列，每個所選的寫入器包含元件各一個。</span><span class="sxs-lookup"><span data-stu-id="b20db-135">In addition to the writer identification information, the [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) interface provides an array of instances of the [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface—one for each of the selected writers included components.</span></span>

<span data-ttu-id="b20db-136">如 [備份元件檔生命週期](backup-components-document-life-cycle.md)所述，寫入器可在處理 PrepareForBackup、PrepareForSnapshot、PostSnapshot、BackupComplete、PreRestore 或 PostRestore 事件時，透過 [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) 介面取得相同資訊的存取權。</span><span class="sxs-lookup"><span data-stu-id="b20db-136">As noted in [Backup Components Document Life Cycle](backup-components-document-life-cycle.md), the writers can gain access to the same information through the [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) interface when handling the PrepareForBackup, PrepareForSnapshot, PostSnapshot, BackupComplete, PreRestore, or PostRestore event.</span></span>

<span data-ttu-id="b20db-137">[**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 可讓寫入器和要求者取得下列資訊：</span><span class="sxs-lookup"><span data-stu-id="b20db-137">[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) allows both writer and requesters to get the following information:</span></span>

-   <span data-ttu-id="b20db-138">元件的名稱、類型和 [*邏輯路徑*](vssgloss-l.md) ([**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponentname)、 [**GetComponentType**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponenttype)、 [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath)) </span><span class="sxs-lookup"><span data-stu-id="b20db-138">A component's name, type, and [*logical path*](vssgloss-l.md) ([**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponentname), [**GetComponentType**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponenttype), [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath))</span></span>
-   <span data-ttu-id="b20db-139">如何依照 [*還原目標*](vssgloss-r.md) 的指示還原元件 ([**>ivsscomponent：： GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)) </span><span class="sxs-lookup"><span data-stu-id="b20db-139">How a component should be restored as indicated by the [*restore target*](vssgloss-r.md) ([**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget))</span></span>
-   <span data-ttu-id="b20db-140">如果還原檔案時使用替代位置 ([**GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)， [**GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount)) </span><span class="sxs-lookup"><span data-stu-id="b20db-140">If an alternate location was used in restoring a file ([**GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping), [**GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount))</span></span>
-   <span data-ttu-id="b20db-141">新的目標資訊，如果有任何 ([**GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)、 [**GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount)) </span><span class="sxs-lookup"><span data-stu-id="b20db-141">New target information, if any ([**GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget), [**GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount))</span></span>
-   <span data-ttu-id="b20db-142">還原前和還原後的錯誤訊息 ([**GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg)、 [**GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg)) </span><span class="sxs-lookup"><span data-stu-id="b20db-142">Pre-and post-restore error messages ([**GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg))</span></span>
-   <span data-ttu-id="b20db-143">如果已選取用於定義元件集的可 [*選取的備份*](vssgloss-s.md) 元件 ([**IsSelectedForRestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore)) </span><span class="sxs-lookup"><span data-stu-id="b20db-143">If a [*selectable for backup*](vssgloss-s.md) component defining a component set has been selected for restore ([**IsSelectedForRestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore))</span></span>
-   <span data-ttu-id="b20db-144">備份或還原是否成功 ([**GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)、 [**GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)) </span><span class="sxs-lookup"><span data-stu-id="b20db-144">Whether a backup or restore succeeded ([**GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded), [**GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus))</span></span>
-   <span data-ttu-id="b20db-145">任何可能由 [**>ivssbackupcomponents：： SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) 或 [**>ivssbackupcomponents：： SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) 設定的寫入器特定備份或還原選項， ([**GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)， [**GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)) </span><span class="sxs-lookup"><span data-stu-id="b20db-145">Any writer-specific backup or restore options that may have been set by [**IVssBackupComponents::SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) or [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) ([**GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions), [**GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions))</span></span>
-   <span data-ttu-id="b20db-146">任何寫入器專屬的元資料備份或還原中繼資料 ([**GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)) 、 [**GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)) </span><span class="sxs-lookup"><span data-stu-id="b20db-146">Any writer-specific metadata backup or restore metadata ([**GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)), [**GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata))</span></span>
-   <span data-ttu-id="b20db-147">時間戳記資訊 ([**GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)、 [**GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)) </span><span class="sxs-lookup"><span data-stu-id="b20db-147">Time-stamp information ([**GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp), [**GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp))</span></span>
-   <span data-ttu-id="b20db-148">Restore ([**GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent)， [**GetRestoreSubcomponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount)) 中明確包含之備份子元件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b20db-148">Information about backup subcomponents explicitly included in a restore ([**GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent), [**GetRestoreSubcomponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount))</span></span>

<span data-ttu-id="b20db-149">與要求者不同的是，寫入器可以透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面變更備份元件檔中的特定資訊：</span><span class="sxs-lookup"><span data-stu-id="b20db-149">Unlike requesters, writers can change certain information in the Backup Components Document via the [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface:</span></span>

-   <span data-ttu-id="b20db-150">如何依照還原目標的指示還原元件 ([**>ivsscomponent：： SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)) </span><span class="sxs-lookup"><span data-stu-id="b20db-150">How a component should be restored as indicated by the restore target ([**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget))</span></span>
-   <span data-ttu-id="b20db-151">寫入器特定的備份和還原中繼資料 ([**>ivsscomponent：： SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)， [**>ivsscomponent：： SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)) </span><span class="sxs-lookup"><span data-stu-id="b20db-151">Writer-specific backup and restore metadata ([**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata), [**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata))</span></span>
-   <span data-ttu-id="b20db-152">時間戳記資訊 ([**SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)) </span><span class="sxs-lookup"><span data-stu-id="b20db-152">Time-stamp information ([**SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp))</span></span>
-   <span data-ttu-id="b20db-153">還原前和還原後的錯誤訊息 ([**SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)、 [**SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)) </span><span class="sxs-lookup"><span data-stu-id="b20db-153">Pre- and post-restore error messages ([**SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg), [**SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg))</span></span>

## <a name="requester-state-information"></a><span data-ttu-id="b20db-154">要求者狀態資訊</span><span class="sxs-lookup"><span data-stu-id="b20db-154">Requester State Information</span></span>

<span data-ttu-id="b20db-155">要求者會使用 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面，將備份或還原作業的狀態相關資訊插入備份元件檔中。</span><span class="sxs-lookup"><span data-stu-id="b20db-155">Requesters insert information about the state of a backup or restore operation into the Backup Components Document using the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface.</span></span> <span data-ttu-id="b20db-156">寫入器應用程式可以透過 [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) 類別來查詢這類資訊。</span><span class="sxs-lookup"><span data-stu-id="b20db-156">Writer applications are able to query for this information through the [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) class.</span></span>

<span data-ttu-id="b20db-157">儲存在備份元件檔中的狀態資訊包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="b20db-157">State information stored in the Backup Components Document includes the following:</span></span>

<span data-ttu-id="b20db-158">備份的一般資訊</span><span class="sxs-lookup"><span data-stu-id="b20db-158">General Information about the Backup</span></span>

-   <span data-ttu-id="b20db-159">整體備份類型 (增量、差異或完整) </span><span class="sxs-lookup"><span data-stu-id="b20db-159">The overall backup type (incremental, differential, or full)</span></span><dl> <dt>

<span data-ttu-id="b20db-160">由要求者使用 [ **>ivssbackupcomponents：： SetBackupState** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)</span><span class="sxs-lookup"><span data-stu-id="b20db-160">Set by requesters using [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)</span></span>
</dt> <dt>

<span data-ttu-id="b20db-161">由寫入器使用 [ **CVssWriter：： GetBackupType** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)</span><span class="sxs-lookup"><span data-stu-id="b20db-161">Retrieved by writers using [**CVssWriter::GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)</span></span>
</dt> </dl>
-   Whether component operations are supported<dl> <dt>

<span data-ttu-id="b20db-162">由要求者使用 [ **>ivssbackupcomponents：： SetBackupState** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)</span><span class="sxs-lookup"><span data-stu-id="b20db-162">Set by requesters using [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)</span></span>
</dt> <dt>

<span data-ttu-id="b20db-163">由寫入器使用 [ **CVssWriter：： AreComponentsSelected** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)</span><span class="sxs-lookup"><span data-stu-id="b20db-163">Retrieved by writers using [**CVssWriter::AreComponentsSelected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)</span></span>
</dt> </dl>
-   Whether the bootable system state is backed up<dl> <dt>

<span data-ttu-id="b20db-164">由要求者使用 [ **>ivssbackupcomponents：： SetBackupState** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)</span><span class="sxs-lookup"><span data-stu-id="b20db-164">Set by requesters using [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)</span></span>
</dt> <dt>

<span data-ttu-id="b20db-165">由寫入器使用 [ **CVssWriter：： IsBootableStateBackedUp** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)</span><span class="sxs-lookup"><span data-stu-id="b20db-165">Retrieved by writers using [**CVssWriter::IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)</span></span>
</dt> </dl>
-   Whether partial file operations are supported<dl> <dt>

<span data-ttu-id="b20db-166">由要求者使用 [ **>ivssbackupcomponents：： SetBackupState** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)</span><span class="sxs-lookup"><span data-stu-id="b20db-166">Set by requesters using [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)</span></span>
</dt> <dt>

<span data-ttu-id="b20db-167">由寫入器使用 [ **CVssWriter：： IsPartialFileSupportEnabled** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)</span><span class="sxs-lookup"><span data-stu-id="b20db-167">Retrieved by writers using [**CVssWriter::IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)</span></span>
</dt> </dl>

<span data-ttu-id="b20db-168">有關還原的一般資訊</span><span class="sxs-lookup"><span data-stu-id="b20db-168">General Information about the Restore</span></span>

-   <span data-ttu-id="b20db-169">整體還原類型 (還原是透過複製或匯入) </span><span class="sxs-lookup"><span data-stu-id="b20db-169">The overall restore type (whether restore is by copy or import)</span></span><dl> <dt>

<span data-ttu-id="b20db-170">由要求者使用 [ **>ivssbackupcomponents：： SetRestoreState** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)</span><span class="sxs-lookup"><span data-stu-id="b20db-170">Set by requesters using [**IVssBackupComponents::SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)</span></span>
</dt> <dt>

<span data-ttu-id="b20db-171">由寫入器使用 [ **CVssWriter：： GetRestoreType** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)</span><span class="sxs-lookup"><span data-stu-id="b20db-171">Retrieved by writers using [**CVssWriter::GetRestoreType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)</span></span>
</dt> </dl>

<span data-ttu-id="b20db-172">支援檔案的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b20db-172">Information about Supporting Files</span></span>

-   <span data-ttu-id="b20db-173">特定元件在部分檔案作業中使用的範圍檔案位置</span><span class="sxs-lookup"><span data-stu-id="b20db-173">The location of ranges files used by a specific component in partial file operations</span></span><dl> <dt>

<span data-ttu-id="b20db-174">由要求者使用 [ **>ivssbackupcomponents：： SetRangesFilePath** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)</span><span class="sxs-lookup"><span data-stu-id="b20db-174">Set by requesters using [**IVssBackupComponents::SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)</span></span>
</dt> <dt>

<span data-ttu-id="b20db-175">由寫入器 (或要求者) 使用 [ **>ivsscomponent：： GetPartialFile** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)</span><span class="sxs-lookup"><span data-stu-id="b20db-175">Retrieved by writers (or requesters) using [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)</span></span>
</dt> </dl>

<span data-ttu-id="b20db-176">資訊的狀態</span><span class="sxs-lookup"><span data-stu-id="b20db-176">Status of Information</span></span>

-   <span data-ttu-id="b20db-177">指出是否已成功備份其中一個指定的寫入器元件</span><span class="sxs-lookup"><span data-stu-id="b20db-177">Indicate whether one of a given writer's components was successfully backed up</span></span><dl> <dt>

<span data-ttu-id="b20db-178">由要求者使用 [ **>ivssbackupcomponents：： SetBackupSucceeded** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)</span><span class="sxs-lookup"><span data-stu-id="b20db-178">Set by requesters using [**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)</span></span>
</dt> <dt>

<span data-ttu-id="b20db-179">由寫入器和要求者使用 [ **>ivsscomponent：： GetBackupSucceeded** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)</span><span class="sxs-lookup"><span data-stu-id="b20db-179">Retrieved by writers and requesters using [**IVssComponent::GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)</span></span>
</dt> </dl>
-   Indicate whether one of a given writer's components was successfully restored<dl> <dt>

<span data-ttu-id="b20db-180">由要求者使用 [ **>ivssbackupcomponents：： SetFileRestoreStatus** 設定](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)</span><span class="sxs-lookup"><span data-stu-id="b20db-180">Set by requesters using [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)</span></span>
</dt> <dt>

<span data-ttu-id="b20db-181">由寫入器和要求者使用 [ **>ivsscomponent：： GetFileRestoreStatus** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)</span><span class="sxs-lookup"><span data-stu-id="b20db-181">Retrieved by writers and requester using [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)</span></span>
</dt> </dl>

<span data-ttu-id="b20db-182">Writer-Settable 資訊</span><span class="sxs-lookup"><span data-stu-id="b20db-182">Writer-Settable Information</span></span>

-   <span data-ttu-id="b20db-183">其中一個指定的寫入器元件的其他備份規格</span><span class="sxs-lookup"><span data-stu-id="b20db-183">Additional backup specification for one of a given writer's components</span></span><dl> <dt>

<span data-ttu-id="b20db-184">由使用 [ **>ivsscomponent：： SetBackupMetadata** 的寫入器設定](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)</span><span class="sxs-lookup"><span data-stu-id="b20db-184">Set by writers using [**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)</span></span>
</dt> <dt>

<span data-ttu-id="b20db-185">由寫入器和要求者使用 [ **>ivsscomponent：： GetBackupMetadata** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)</span><span class="sxs-lookup"><span data-stu-id="b20db-185">Retrieved by writers and requesters using [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)</span></span>
</dt> </dl>
-   Additional restore specification for one of a given writer's components<dl> <dt>

<span data-ttu-id="b20db-186">由使用 [ **>ivsscomponent：： SetRestoreMetadata** 的寫入器設定](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)</span><span class="sxs-lookup"><span data-stu-id="b20db-186">Set by writers using [**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)</span></span>
</dt> <dt>

<span data-ttu-id="b20db-187">由寫入器和要求者使用 [ **>ivsscomponent：： GetRestoreMetadata** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)</span><span class="sxs-lookup"><span data-stu-id="b20db-187">Retrieved by writers and requesters using [**IVssComponent::GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)</span></span>
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the current backup of one of its component's backups<dl> <dt>

<span data-ttu-id="b20db-188">由使用 [ **>ivsscomponent：： SetBackupStamp** 的寫入器設定](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)</span><span class="sxs-lookup"><span data-stu-id="b20db-188">Set by writers using [**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)</span></span>
</dt> <dt>

<span data-ttu-id="b20db-189">由寫入器和要求者使用 [ **>ivsscomponent：： GetBackupStamp** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)</span><span class="sxs-lookup"><span data-stu-id="b20db-189">Retrieved by writers and requesters using [**IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)</span></span>
<span data-ttu-id="b20db-190"></dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the last backup of one of its components' backups using a backup stamp initially set by <a href="/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp">>ivsscomponent：： SetBackupStamp</a></span><span class="sxs-lookup"><span data-stu-id="b20db-190"></dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the last backup of one of its components' backups using a backup stamp initially set by <a href="/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp">IVssComponent::SetBackupStamp</a></span></span><dl> <dt>

<span data-ttu-id="b20db-191">使用 [ **>ivssbackupcomponents：： SetPreviousBackupStamp** ，由要求者儲存並設定特定元件的要求者](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)</span><span class="sxs-lookup"><span data-stu-id="b20db-191">Stored and set by requesters for a specific component using [**IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)</span></span>
</dt> <dt>

<span data-ttu-id="b20db-192">由寫入器和要求者使用 [ **>ivsscomponent：： GetPreviousBackupStamp** 抓取](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)</span><span class="sxs-lookup"><span data-stu-id="b20db-192">Retrieved by writers and requesters using [**IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)</span></span>
</dt> </dl>
-   Error messages for failure before and after restore operations<dl> <dt>

<span data-ttu-id="b20db-193">由使用 [**>ivsscomponent：： SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)或 [**>ivsscomponent：： SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)的寫入器設定</span><span class="sxs-lookup"><span data-stu-id="b20db-193">Set by writers using [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg) or [**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)</span></span>
</dt> <dt>

<span data-ttu-id="b20db-194">由寫入器和要求者使用 [**>ivsscomponent：： GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg)或 [**>ivsscomponent：： GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg)抓取</span><span class="sxs-lookup"><span data-stu-id="b20db-194">Retrieved by writers and requesters using [**IVssComponent::GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg) or [**IVssComponent::GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg)</span></span>
</dt> </dl>

 

 
