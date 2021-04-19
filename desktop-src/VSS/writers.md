---
description: 寫入器是一種應用程式或服務，會將持續性資訊儲存在磁片上的檔案中，並使用陰影複製介面，將這些檔案的名稱和位置提供給要求者。
ms.assetid: 24fc2d7c-f8d6-49ca-9bb5-0179bef68e78
title: 寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ca409e8dc6153a6b3e2b747dc23cc391055471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972224"
---
# <a name="writers"></a><span data-ttu-id="5c167-103">寫入器</span><span class="sxs-lookup"><span data-stu-id="5c167-103">Writers</span></span>

<span data-ttu-id="5c167-104">[*寫入*](vssgloss-w.md) 器是一種應用程式或服務，會將持續性資訊儲存在磁片上的檔案中，並使用陰影複製介面，將這些檔案的名稱和位置提供給要求者。</span><span class="sxs-lookup"><span data-stu-id="5c167-104">[*Writers*](vssgloss-w.md) are applications or services that store persistent information in files on disk and that provide the names and locations of these files to requesters by using the shadow copy interface.</span></span>

<span data-ttu-id="5c167-105">在備份作業期間，寫入器可確保其資料為靜止且穩定，適用于陰影複製和備份。</span><span class="sxs-lookup"><span data-stu-id="5c167-105">During backup operations, writers ensure that their data is quiescent and stable—suitable for shadow copy and backup.</span></span> <span data-ttu-id="5c167-106">寫入器會在可能的情況下解除鎖定檔案，並在必要時指出替代位置，以與還原共同作業</span><span class="sxs-lookup"><span data-stu-id="5c167-106">Writers collaborate with restores by unlocking files when possible and indicating alternate locations when necessary.</span></span>

<span data-ttu-id="5c167-107">如果 VSS 備份作業期間沒有任何寫入器存在，仍然可以建立陰影複製。</span><span class="sxs-lookup"><span data-stu-id="5c167-107">If no writers are present during a VSS backup operation, a shadow copy can still be created.</span></span> <span data-ttu-id="5c167-108">在此情況下，陰影複製之磁片區上的所有資料都會處於損 [*毀一致狀態*](vssgloss-c.md)。</span><span class="sxs-lookup"><span data-stu-id="5c167-108">In this case, all data on the shadow-copied volume will be in the [*crash-consistent state*](vssgloss-c.md).</span></span>

## <a name="writer-state"></a><span data-ttu-id="5c167-109">寫入器狀態</span><span class="sxs-lookup"><span data-stu-id="5c167-109">Writer State</span></span>

<span data-ttu-id="5c167-110">寫入器會在以 XML 為基礎的中繼資料物件（ [*寫入器元資料檔案*](vssgloss-w.md)）中維護其狀態。</span><span class="sxs-lookup"><span data-stu-id="5c167-110">Writers maintain their state in an XML-based metadata object, the [*Writer Metadata Document*](vssgloss-w.md).</span></span>

<span data-ttu-id="5c167-111">此寫入器中繼資料是唯一的資料結構，其中包含要備份和還原的資料 [*檔集*](vssgloss-f.md)（路徑、檔案規格和遞迴旗標）。</span><span class="sxs-lookup"><span data-stu-id="5c167-111">This writer metadata is the only data structure that contains the [*file set*](vssgloss-f.md)—path, file specification, and recursion flag—of the data to be backed up and restored.</span></span>

<span data-ttu-id="5c167-112">寫入器元資料檔案會將寫入器的檔案集組織成群組或 [*元件*](vssgloss-c.md)。</span><span class="sxs-lookup"><span data-stu-id="5c167-112">The Writer Metadata Document organizes the writer's file sets into groups or [*components*](vssgloss-c.md).</span></span> <span data-ttu-id="5c167-113">這些元件在備份和還原作業期間的關聯性，是由元件的 [*selectability for backup*](vssgloss-s.md)、其 [*selectability for restore*](vssgloss-s.md)和其 [*邏輯路徑*](vssgloss-l.md)，在寫入器元資料檔案中說明。</span><span class="sxs-lookup"><span data-stu-id="5c167-113">The relationship of one of these components during backup and restore operations to the other components managed by the writer is described in the Writer Metadata Document by the component's [*selectability for backup*](vssgloss-s.md), its [*selectability for restore*](vssgloss-s.md), and its [*logical paths*](vssgloss-l.md).</span></span> <span data-ttu-id="5c167-114"> (需詳細資訊，請參閱 [設定元件組織](definition-of-components-by-writers.md) 和 [使用 Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="5c167-114">(For more information, see [Setting up Component Organization](definition-of-components-by-writers.md) and [Working with Selectability and Logical Paths](working-with-selectability-and-logical-paths.md).)</span></span>

<span data-ttu-id="5c167-115">此檔也包含控制檔案還原和其他問題的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="5c167-115">Additional information that governs file restoration and other issues is also contained in this document.</span></span>

<span data-ttu-id="5c167-116">要求者需要寫入器中繼資料，以及其本身的備份元件檔，以處理備份或還原。</span><span class="sxs-lookup"><span data-stu-id="5c167-116">The requester needs the writer metadata, in conjunction with its own Backup Components Document, to process a backup or a restore.</span></span>

<span data-ttu-id="5c167-117">不同于備份元件檔，寫入器元資料檔案應該視為唯讀結構。</span><span class="sxs-lookup"><span data-stu-id="5c167-117">Unlike the Backup Components Document, the Writer Metadata Document should be thought of as a read-only structure.</span></span> <span data-ttu-id="5c167-118">一旦寫入器建立它之後，就不會變更檔。</span><span class="sxs-lookup"><span data-stu-id="5c167-118">Once a writer creates it, the document is not altered.</span></span>

## <a name="writer-event-handling"></a><span data-ttu-id="5c167-119">寫入器事件處理</span><span class="sxs-lookup"><span data-stu-id="5c167-119">Writer Event Handling</span></span>

<span data-ttu-id="5c167-120">寫入器的 VSS 作業是透過接收 COM 事件起始。</span><span class="sxs-lookup"><span data-stu-id="5c167-120">A writer's VSS operations are initiated through the receipt of COM events.</span></span>

<span data-ttu-id="5c167-121">當沒有任何事件存在時，寫入器不會執行 VSS 作業 (例如 VSS 備份或還原) 。</span><span class="sxs-lookup"><span data-stu-id="5c167-121">When no events are present, a writer does not perform VSS operations (such as a VSS backup or restore).</span></span> <span data-ttu-id="5c167-122">相反地，它會執行其一般工作，例如回應資料庫查詢、管理使用者資料，或提供其他服務。</span><span class="sxs-lookup"><span data-stu-id="5c167-122">Instead, it performs its normal work, such as responding to database queries, managing user data, or providing other services.</span></span>

<span data-ttu-id="5c167-123">為了確保會正確執行多個平行備份和還原會話的錯誤處理，並確保一個備份或還原會話沒有損毀，您必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="5c167-123">To ensure that error handling for multiple parallel backup and restore sessions is performed correctly, and to ensure that one backup or restore session does not corrupt another, you must do the following:</span></span>

-   <span data-ttu-id="5c167-124">如果寫入器的事件處理常式 (例如 [**CVssWriter：： OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)) 呼叫 [**CVssWriterEx2：： GetSessionId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-getsessionid)、 [**CVssWriter：： SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure)或 [**CVssWriterEx2：： SetWriterFailureEx**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-setwriterfailureex) 方法，則事件處理常式必須在呼叫事件處理常式的相同執行緒中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="5c167-124">If a writer's event handler (such as [**CVssWriter::OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)) calls the [**CVssWriterEx2::GetSessionId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-getsessionid), [**CVssWriter::SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure), or [**CVssWriterEx2::SetWriterFailureEx**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-setwriterfailureex) method, the event handler must call the method in the same thread that called the event handler.</span></span>
-   <span data-ttu-id="5c167-125">只要每個背景工作執行緒將任何需要的錯誤報表封送處理回原始的事件處理常式執行緒，就可以視需要將工作的事件處理常式（例如 [**OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) ）的執行作業卸載至背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="5c167-125">Your writer’s implementation of an event handler such as [**OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) can offload work to worker threads if desired, as long as each worker thread marshals any needed error reporting back to the original event handler thread.</span></span>

## <a name="handling-identify-events"></a><span data-ttu-id="5c167-126">處理識別事件</span><span class="sxs-lookup"><span data-stu-id="5c167-126">Handling Identify Events</span></span>

<span data-ttu-id="5c167-127">除了識別事件之外，寫入器所接收之事件的類型和順序，會根據目前進行中的 VSS 作業類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="5c167-127">With the exception of the Identify event, the type and order of the events a writer receives depends uniquely on the type of VSS operations that are currently ongoing.</span></span>

<span data-ttu-id="5c167-128">識別事件需要寫入器提供有關其設定及其透過其 [*寫入器中繼資料*](vssgloss-w.md)檔管理之檔案的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="5c167-128">The Identify event requires writers to provide the system information about their configuration and the files they manage through their [*Writer Metadata Document*](vssgloss-w.md).</span></span> <span data-ttu-id="5c167-129">系統會產生識別事件，以支援幾乎任何 VSS 作業，包括系統查詢，以及陰影複製和備份和還原作業。</span><span class="sxs-lookup"><span data-stu-id="5c167-129">An Identify event is generated in support of almost any VSS operation, including system queries as well as shadow copy and backup and restore operations.</span></span> <span data-ttu-id="5c167-130">因此，任何寫入器的識別事件處理常式 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 執行都必須能夠隨時處理識別事件，包括處理另一個 VSS 作業（例如備份或還原）的過程。</span><span class="sxs-lookup"><span data-stu-id="5c167-130">Therefore, any writer's implementation of the Identify event handler [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) must be able to handle an Identify event at any time—including in the middle of processing another VSS operation, such as a backup or restore.</span></span> <span data-ttu-id="5c167-131">您永遠都不應該將識別事件視為 VSS 作業生命週期的一部分，即使在作業開始之前，可能也需要產生它。</span><span class="sxs-lookup"><span data-stu-id="5c167-131">An Identify event should never be thought of as part of the life cycle of a VSS operation, even though its generation may be expected and required prior to the start of that operation.</span></span>

<span data-ttu-id="5c167-132">在 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)中不會修改 VSS 作業的相關狀態資訊，這點特別重要，因為收到順序外的事件會重設該資訊。</span><span class="sxs-lookup"><span data-stu-id="5c167-132">It is particularly important that state information about a VSS operation not be modified in [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), because receipt of an out-of-order event would reset that information.</span></span>

## <a name="backup-and-restore-events"></a><span data-ttu-id="5c167-133">備份與還原事件</span><span class="sxs-lookup"><span data-stu-id="5c167-133">Backup and Restore Events</span></span>

<span data-ttu-id="5c167-134">根據它是否參與備份或還原，寫入器除了初始識別事件之外，也會在兩個和七個事件之間收到。</span><span class="sxs-lookup"><span data-stu-id="5c167-134">Depending on whether it is participating in a backup or restore, a writer will receive between two and seven events, in addition to an initial Identify event.</span></span>

<span data-ttu-id="5c167-135">處理這些事件的 (從寫入器的觀點來看，) 備份或還原作業的生命週期。</span><span class="sxs-lookup"><span data-stu-id="5c167-135">Handling these events constitutes (from the point of view of a writer) the life cycle of a backup or restore operation.</span></span>

<span data-ttu-id="5c167-136">在一般的備份作業中 (查看在 [VSS) 下處理備份的總覽](overview-of-processing-a-backup-under-vss.md) ，寫入器除了初始識別事件) 之外，還會處理下列事件 (：</span><span class="sxs-lookup"><span data-stu-id="5c167-136">In a typical backup operation (see [Overview of Processing a Backup Under VSS](overview-of-processing-a-backup-under-vss.md)), a writer would handle the following events (in addition to an initial Identify event):</span></span>

-   <span data-ttu-id="5c167-137">PrepareForBackup</span><span class="sxs-lookup"><span data-stu-id="5c167-137">PrepareForBackup</span></span>
-   <span data-ttu-id="5c167-138">PrepareForSnapshot</span><span class="sxs-lookup"><span data-stu-id="5c167-138">PrepareForSnapshot</span></span>
-   <span data-ttu-id="5c167-139">凍結</span><span class="sxs-lookup"><span data-stu-id="5c167-139">Freeze</span></span>
-   <span data-ttu-id="5c167-140">解除凍結</span><span class="sxs-lookup"><span data-stu-id="5c167-140">Thaw</span></span>
-   <span data-ttu-id="5c167-141">PostSnapshot</span><span class="sxs-lookup"><span data-stu-id="5c167-141">PostSnapshot</span></span>
-   <span data-ttu-id="5c167-142">BackupComplete</span><span class="sxs-lookup"><span data-stu-id="5c167-142">BackupComplete</span></span>
-   <span data-ttu-id="5c167-143">BackupShutdown</span><span class="sxs-lookup"><span data-stu-id="5c167-143">BackupShutdown</span></span>

<span data-ttu-id="5c167-144">在一般的還原作業中 (查看 [在 VSS) 處理還原的總覽](overview-of-processing-a-restore-under-vss.md) ，寫入器會處理下列事件：</span><span class="sxs-lookup"><span data-stu-id="5c167-144">In a typical restore operation (see [Overview of Processing a Restore Under VSS](overview-of-processing-a-restore-under-vss.md)), a writer would handle the following events:</span></span>

-   <span data-ttu-id="5c167-145">PreRestore</span><span class="sxs-lookup"><span data-stu-id="5c167-145">PreRestore</span></span>
-   <span data-ttu-id="5c167-146">PostRestore</span><span class="sxs-lookup"><span data-stu-id="5c167-146">PostRestore</span></span>

 

 



