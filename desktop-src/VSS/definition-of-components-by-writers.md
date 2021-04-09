---
description: 元件是由寫入器元資料檔案中的寫入器所定義和具現化，以回應在備份作業開始時的識別事件 (查看填入寫入器元資料檔案時) 備份初始化的總覽。
ms.assetid: 5e1c3f9b-ca83-4e70-963b-0a237c6f4b0d
title: 作者的元件定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5383e9bc87620f23bb2a3ab067c1913a323782
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852647"
---
# <a name="definition-of-components-by-writers"></a><span data-ttu-id="90269-103">作者的元件定義</span><span class="sxs-lookup"><span data-stu-id="90269-103">Definition of Components by Writers</span></span>

<span data-ttu-id="90269-104">元件是由寫入器元資料檔案中的寫入器所定義和具現化，以回應在備份作業開始時的 [*識別事件*](vssgloss-i.md) (查看填入寫入器元資料檔案時) [備份初始化的總覽](overview-of-backup-initialization.md) 。</span><span class="sxs-lookup"><span data-stu-id="90269-104">Components are defined by and instantiated by writers in their Writer Metadata Document in response to an [*Identify event*](vssgloss-i.md) at the start of a backup operation (see [Overview of Backup Initialization](overview-of-backup-initialization.md)) when the Writer Metadata Document is populated.</span></span>

<span data-ttu-id="90269-105">使用 [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) 和 [**IVssCreateWriterMetadata：： AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)在其寫入器元資料檔案中建立元件時，寫入器必須指定：</span><span class="sxs-lookup"><span data-stu-id="90269-105">When creating a component in its Writer Metadata Document, using [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) and [**IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), a writer must specify:</span></span>

-   <span data-ttu-id="90269-106">是否可選取元件 [*以進行備份*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="90269-106">Whether the component is [*selectable for backup*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="90269-107">元件類型</span><span class="sxs-lookup"><span data-stu-id="90269-107">A component type</span></span>
-   <span data-ttu-id="90269-108">元件名稱 (在指定的 [*寫入器實例*](vssgloss-w.md) 內必須是唯一的，但在所有的寫入器實例中必須是唯一的) </span><span class="sxs-lookup"><span data-stu-id="90269-108">A component name (which must be unique not only within a given [*writer instance*](vssgloss-w.md) but across all writer instances)</span></span>
-   <span data-ttu-id="90269-109">元件是否有任何與其相關聯的寫入器特定中繼資料</span><span class="sxs-lookup"><span data-stu-id="90269-109">Whether the component has any writer-specific metadata associated with it</span></span>
-   <span data-ttu-id="90269-110">寫入器是否需要成功備份之後的通知</span><span class="sxs-lookup"><span data-stu-id="90269-110">Whether the writer requires notification following a successful backup</span></span>

<span data-ttu-id="90269-111">寫入器可以選擇性地指定：</span><span class="sxs-lookup"><span data-stu-id="90269-111">Writers can optionally specify:</span></span>

-   <span data-ttu-id="90269-112">元件的 [*邏輯路徑*](vssgloss-l.md) (必須是唯一的，但不能只在指定的寫入器實例內，而是在所有的寫入器實例中) </span><span class="sxs-lookup"><span data-stu-id="90269-112">A component's [*logical path*](vssgloss-l.md) (which must be unique not only within a given writer instance but across all writer instances)</span></span>
-   <span data-ttu-id="90269-113">元件描述 (或標題) </span><span class="sxs-lookup"><span data-stu-id="90269-113">A component description (or caption)</span></span>
-   <span data-ttu-id="90269-114">用於 Gui 以表示元件的圖示</span><span class="sxs-lookup"><span data-stu-id="90269-114">An icon to be used with GUIs to indicate the component</span></span>

<span data-ttu-id="90269-115">元件不需要實際包含任何檔案。</span><span class="sxs-lookup"><span data-stu-id="90269-115">It is not necessary for a component to actually contain any files.</span></span> <span data-ttu-id="90269-116">這類空白或「虛擬」元件在組織元件方面很有用。</span><span class="sxs-lookup"><span data-stu-id="90269-116">This sort of empty or "dummy" component can be useful in organizing components.</span></span> <span data-ttu-id="90269-117">這類元件可以用來定義 [*元件集*](vssgloss-c.md) 和寫入器的元件 (請參閱) [元件的邏輯路徑](logical-pathing-of-components.md) 。</span><span class="sxs-lookup"><span data-stu-id="90269-117">Such a component can be used to define a [*component set*](vssgloss-c.md) and a writer's component (see [Logical Pathing of Components](logical-pathing-of-components.md)).</span></span>

## <a name="setting-up-component-organization"></a><span data-ttu-id="90269-118">設定元件組織</span><span class="sxs-lookup"><span data-stu-id="90269-118">Setting Up Component Organization</span></span>

<span data-ttu-id="90269-119">設定元件的 [*selectability*](vssgloss-s.md) (其 [*selectability 進行備份*](vssgloss-s.md)，並將它的 [*selectability 用於還原*](/windows)) 與其 [*邏輯路徑*](vssgloss-l.md) ，可讓寫入器在備份或還原作業中，強制或選擇性地包含特定元件，並將元件組成 [*元件集*](vssgloss-c.md) ，並將一個可選取的元件當做整個群組的進入點。</span><span class="sxs-lookup"><span data-stu-id="90269-119">Setting a component's [*selectability*](vssgloss-s.md) (its [*selectability for backup*](vssgloss-s.md), and its [*selectability for restore*](/windows)) and its [*logical paths*](vssgloss-l.md) allows a writer to mandate or make optional the inclusion of certain components in a backup or restore operation, and to group components into [*component sets*](vssgloss-c.md) with one selectable component acting as an entry point to the whole group.</span></span>

<span data-ttu-id="90269-120">這些群組中的成員資格會決定在備份和還原作業期間將使用哪些元件。</span><span class="sxs-lookup"><span data-stu-id="90269-120">Membership in these groupings determines which components will be used during backup and restore operations.</span></span> <span data-ttu-id="90269-121">使用「可選取」表示可針對備份作業選取，並可為還原作業選取還原，開發人員應該瞭解：</span><span class="sxs-lookup"><span data-stu-id="90269-121">Using "selectable" to mean selectable for back for backup operation, and selectable for restore for restore operation, developers should understand that:</span></span>

-   <span data-ttu-id="90269-122">如果由指定的寫入器管理任何元件，則要求者必須 [*明確地包含*](vssgloss-e.md) 所有其 [*元件*](vssgloss-c.md) ，而不需要在其對備份元件檔的 [*邏輯路徑*](vssgloss-l.md) 中選取祖系，然後以群組的方式備份和還原這些元件。</span><span class="sxs-lookup"><span data-stu-id="90269-122">If any components managed by a given writer are backed up, then a requester must [*explicitly include*](vssgloss-e.md) all nonselectable [*components*](vssgloss-c.md) without selectable ancestors in their [*logical path*](vssgloss-l.md) to the Backup Components Document and back up and restore those components as a group.</span></span>
-   <span data-ttu-id="90269-123">要求者可以選擇在備份和還原作業期間，將可選取的元件明確新增至備份元件檔;新增之後，必須備份或還原元件。</span><span class="sxs-lookup"><span data-stu-id="90269-123">A requester has the option of explicitly adding selectable components to the Backup Components Document during backup and restore operations; once added, the component must be backed up or restored.</span></span>
-   <span data-ttu-id="90269-124">如果元件是可選取的，則元件及其所有 [*子*](vssgloss-s.md) 元件 (如邏輯路徑所定義) 形成元件集，可視為可選擇性參與備份和還原作業的單一單位。</span><span class="sxs-lookup"><span data-stu-id="90269-124">If a component is selectable, the component and all of its [*subcomponents*](vssgloss-s.md) (as defined by logical paths) form a component set, which can be treated as a single unit that may optionally participate in backup and restore operations.</span></span>
-   <span data-ttu-id="90269-125">要求者絕對不會明確地在備份和還原作業期間，將可選取的祖系（元件集中的子元件）新增至其備份元件檔的其元件。</span><span class="sxs-lookup"><span data-stu-id="90269-125">A requester never explicitly adds a nonselectable component with selectable ancestors, a subcomponent in a component set, to its Backup Components Document during backup and restore operations.</span></span> <span data-ttu-id="90269-126">如果已明確加入這些元件，則必須以 [*隱含方式包含*](/windows) 這些元件，在此情況下，必須備份或還原它們 (請參閱要求 [者) 使用元件](use-of-components-by-the-requestor.md) 。</span><span class="sxs-lookup"><span data-stu-id="90269-126">These components must be [*implicitly included*](/windows) if their selectable ancestor is explicitly added, in which case they must be backed up or restored (see [Use of Components by the Requester](use-of-components-by-the-requestor.md)).</span></span>
-   <span data-ttu-id="90269-127">具有可選取上階的可選取元件仍然是元件 () 元件集的 [*子*](vssgloss-s.md) 元件，而且如果其可選取的上階明確包含在作業中，則可能會隱含地包含該元件。</span><span class="sxs-lookup"><span data-stu-id="90269-127">A selectable component with a selectable ancestor is still a [*subcomponent*](vssgloss-s.md) (a member of a component set) and may be implicitly included if its selectable ancestor is explicitly included in the operation.</span></span> <span data-ttu-id="90269-128">在此情況下，其資訊不會加入至備份元件檔。</span><span class="sxs-lookup"><span data-stu-id="90269-128">In this case, its information is not added to the Backup Components Document.</span></span> <span data-ttu-id="90269-129">如果作業中未包含可選取的上階，則可以明確選取該元件以包含在作業中，在這種情況下，它的資訊會包含在備份元件檔中。</span><span class="sxs-lookup"><span data-stu-id="90269-129">If its selectable ancestor is not included in the operation, the component can be explicitly selected for inclusion in the operation, in which case its information is included in the Backup Components Document.</span></span>
-   <span data-ttu-id="90269-130">如果任何可選取的上階是可選擇進行還原的，則可以明確地將包含在備份中的子元件包含在還原作業中，不論是否有任何可選取的上階狀態。</span><span class="sxs-lookup"><span data-stu-id="90269-130">A subcomponent implicitly included in a backup can be explicitly included in a restore operation, regardless of the status of any selectable ancestor, if it is selectable for restore.</span></span> <span data-ttu-id="90269-131">還原作業期間所包含的任何可選取的還原子元件，都必須將其資訊新增至備份元件檔。</span><span class="sxs-lookup"><span data-stu-id="90269-131">Any selectable for restore subcomponent included during a restore operation must have its information added to the Backup Components Document.</span></span>
-   <span data-ttu-id="90269-132">在產生 [*PrepareForBackup*](vssgloss-p.md) 和 [*PreRestore*](vssgloss-p.md) 事件之前，未明確將任何元件新增至備份元件檔的寫入器，將不會收到任何進一步的 VSS 事件。</span><span class="sxs-lookup"><span data-stu-id="90269-132">A writer that has had no component explicitly added to the Backup Components Document prior to the generation of [*PrepareForBackup*](vssgloss-p.md) and [*PreRestore*](vssgloss-p.md) events will not receive any further VSS events.</span></span>

<span data-ttu-id="90269-133">如需詳細資訊，請參閱 [使用 Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md)。</span><span class="sxs-lookup"><span data-stu-id="90269-133">For more information, see [Working with Selectability and Logical Paths](working-with-selectability-and-logical-paths.md).</span></span>

## <a name="adding-files-to-a-component"></a><span data-ttu-id="90269-134">將檔案新增至元件</span><span class="sxs-lookup"><span data-stu-id="90269-134">Adding Files to a Component</span></span>

<span data-ttu-id="90269-135">元件包含檔案格式的檔案資訊，其中包含下列檔案的檔 [*集*](vssgloss-f.md) ：</span><span class="sxs-lookup"><span data-stu-id="90269-135">A component contains file information in the form of a [*file set*](vssgloss-f.md) that contains:</span></span>

-   <span data-ttu-id="90269-136">元件中檔案的根目錄。</span><span class="sxs-lookup"><span data-stu-id="90269-136">A root directory of the files in the component.</span></span>
-   <span data-ttu-id="90269-137">元件中檔案的檔案規格。</span><span class="sxs-lookup"><span data-stu-id="90269-137">A file specification for the files in the component.</span></span>
-   <span data-ttu-id="90269-138">指出元件規格是否為遞迴的旗標。</span><span class="sxs-lookup"><span data-stu-id="90269-138">A flag that indicates whether the component's specification is recursive.</span></span>

<span data-ttu-id="90269-139">視元件類型而定，它可以是資料庫或檔案群組，而在資料庫元件的案例中 () 是否要載入的檔案是資料或記錄檔，寫入器會呼叫 [**IVssCreateWriterMetadata：： AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)、 [**IVssCreateWriterMetadata：： AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)或 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) 來新增檔案集。</span><span class="sxs-lookup"><span data-stu-id="90269-139">Depending on component type, which can be a database or a file group, and (in the case of database components) whether the files to be loaded are data or log files, a writer calls [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), or [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) to add a file set.</span></span>

<span data-ttu-id="90269-140">使用這些函式時，您應該指定要加入檔案集的檔案，如下所示：</span><span class="sxs-lookup"><span data-stu-id="90269-140">When using these functions, you should specify the files to be added to the file set as follows:</span></span>

-   <span data-ttu-id="90269-141">*wszPath*：這是包含要新增至檔案集之檔案的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="90269-141">*wszPath*: This is the path to the directory that contains the files to be added to the file set.</span></span> <span data-ttu-id="90269-142">如果 *bRecursive* 參數設定為 **true**， *wszPath* 參數會指定要以遞迴方式進行往返的目錄階層，並應重新建立所有目錄，包括空的目錄。</span><span class="sxs-lookup"><span data-stu-id="90269-142">If the *bRecursive* parameter is set to **true**, the *wszPath* parameter specifies a hierarchy of directories to be traversed recursively, and all directories should be recreated, including empty directories.</span></span>
-   <span data-ttu-id="90269-143">*wszFilespec*：這個字串會指定要新增至檔案集之每個目錄中的檔案。</span><span class="sxs-lookup"><span data-stu-id="90269-143">*wszFilespec*: This string specifies the files in each directory to be added to the file set.</span></span>

<span data-ttu-id="90269-144">例如，假設下列目錄結構存在：</span><span class="sxs-lookup"><span data-stu-id="90269-144">For example, suppose the following directory structure exists:</span></span>

<dl> <span data-ttu-id="90269-145">C： \\ Directory1 \\File1.txt</span><span class="sxs-lookup"><span data-stu-id="90269-145">C:\\Directory1\\File1.txt</span></span>  
<span data-ttu-id="90269-146">C： \\ Directory1 \\File2.txt</span><span class="sxs-lookup"><span data-stu-id="90269-146">C:\\Directory1\\File2.txt</span></span>  
<span data-ttu-id="90269-147">C： \\ Directory1 \\ Directory2 \\File1.txt</span><span class="sxs-lookup"><span data-stu-id="90269-147">C:\\Directory1\\Directory2\\File1.txt</span></span>  
<span data-ttu-id="90269-148">C： \\ Directory1 \\ Directory2 \\File2.txt</span><span class="sxs-lookup"><span data-stu-id="90269-148">C:\\Directory1\\Directory2\\File2.txt</span></span>  
<span data-ttu-id="90269-149">C： \\ Directory1 \\ Directory3</span><span class="sxs-lookup"><span data-stu-id="90269-149">C:\\Directory1\\Directory3</span></span>\\  
</dl>

<span data-ttu-id="90269-150">如果寫入器針對 WszPath 指定 "C： \\ Directory1 \*\*"，針對 WszFilespec 指定 "File1."，若為 bRecursive，則要求者 \* 應包含這些檔案：   </span><span class="sxs-lookup"><span data-stu-id="90269-150">If the writer specifies "C:\\Directory1" for *wszPath*, "File1.\*" for *wszFilespec*, and **true** for *bRecursive*, the requester should include these files:</span></span>

<dl> <span data-ttu-id="90269-151">C： \\ Directory1 \\File1.txt</span><span class="sxs-lookup"><span data-stu-id="90269-151">C:\\Directory1\\File1.txt</span></span>  
<span data-ttu-id="90269-152">C： \\ Directory1 \\ Directory2 \\File1.txt</span><span class="sxs-lookup"><span data-stu-id="90269-152">C:\\Directory1\\Directory2\\File1.txt</span></span>  
</dl>

<span data-ttu-id="90269-153">如果寫入器針對 WszPath 指定 "C： \\ Directory1" \*\*，針對 wszFilespec 指定 ""，如果是 \* *bRecursive*，則要求者應包含這些檔案：  </span><span class="sxs-lookup"><span data-stu-id="90269-153">If the writer instead specifies "C:\\Directory1" for *wszPath*, "\*" for *wszFilespec*, and **true** for *bRecursive*, the requester should include these files:</span></span>

<dl> <span data-ttu-id="90269-154">C： \\ Directory1 \\File1.txt</span><span class="sxs-lookup"><span data-stu-id="90269-154">C:\\Directory1\\File1.txt</span></span>  
<span data-ttu-id="90269-155">C： \\ Directory1 \\File2.txt</span><span class="sxs-lookup"><span data-stu-id="90269-155">C:\\Directory1\\File2.txt</span></span>  
<span data-ttu-id="90269-156">C： \\ Directory1 \\ Directory2 \\File1.txt</span><span class="sxs-lookup"><span data-stu-id="90269-156">C:\\Directory1\\Directory2\\File1.txt</span></span>  
<span data-ttu-id="90269-157">C： \\ Directory1 \\ Directory2 \\File2.txt</span><span class="sxs-lookup"><span data-stu-id="90269-157">C:\\Directory1\\Directory2\\File2.txt</span></span>  
</dl>

<span data-ttu-id="90269-158">如果寫入器針對 WszPath 指定 "C： \\ Directory1 \*\*"，針對 wszFilespec 指定 ""，如果 bRecursive，則要求者 \* 應包含下列檔案：  </span><span class="sxs-lookup"><span data-stu-id="90269-158">If the writer specifies "C:\\Directory1" for *wszPath*, "\*" for *wszFilespec*, and **false** for *bRecursive*, the requester should include these files:</span></span>

<dl> <span data-ttu-id="90269-159">C： \\ Directory1 \\File1.txt</span><span class="sxs-lookup"><span data-stu-id="90269-159">C:\\Directory1\\File1.txt</span></span>  
<span data-ttu-id="90269-160">C： \\ Directory1 \\File2.txt</span><span class="sxs-lookup"><span data-stu-id="90269-160">C:\\Directory1\\File2.txt</span></span>  
</dl>

<span data-ttu-id="90269-161">在上述所有範例中，每當寫入器針對 *bRecursive* 指定 **true** 時， \\ \\ 都應該重新建立空的目錄 C： Directory1 Directory3 \\ 。</span><span class="sxs-lookup"><span data-stu-id="90269-161">In all of the preceding examples, whenever the writer specifies **true** for *bRecursive*, the empty directory C:\\Directory1\\Directory3\\ should be recreated.</span></span>

<span data-ttu-id="90269-162">針對新增至檔案群組元件的檔案集，如果目前位於磁片上的檔案不在寫入器會考慮適當或預設位置的情況下，寫入器可以選擇新增替代路徑。</span><span class="sxs-lookup"><span data-stu-id="90269-162">For a file set added to a file group component, in cases where files currently on disk are not in what the writer would consider the appropriate or default location, a writer has the option of adding an alternate path.</span></span> <span data-ttu-id="90269-163">在這些情況下，檔案集的路徑定義會包含檔案的一般位置和檔案的還原位置，而替代路徑則包含要備份之檔案的目前位置。</span><span class="sxs-lookup"><span data-stu-id="90269-163">In these cases, the file set's definition of the path contains the normal location of the files and to where files should be restored, while the alternate path contains the current location of files to be backed up.</span></span>

<span data-ttu-id="90269-164">檔案集中的所有檔案都必須在備份時存在。</span><span class="sxs-lookup"><span data-stu-id="90269-164">All files in the file set must exist at the time of the backup.</span></span> <span data-ttu-id="90269-165">要求者必須假設檔案集中所列的所有檔案都需要進行備份，而且如果遺失任何檔案，備份將會失敗。</span><span class="sxs-lookup"><span data-stu-id="90269-165">Requesters must assume that all files listed in the file set are required for the backup and will fail the backup if any files are missing.</span></span> <span data-ttu-id="90269-166">請注意，為 \* *wszFilespec* 參數指定 "" 時，它可以比對零或多個檔案。</span><span class="sxs-lookup"><span data-stu-id="90269-166">Note that when "\*" is specified for the *wszFilespec* parameter, it can match zero or more files.</span></span>

<span data-ttu-id="90269-167">請注意，這類寫入器元資料檔案屬性是替代位置對應、明確包含和排除的檔案，而 restore 方法則是在寫入器層級設定，而不是在元件層級設定。</span><span class="sxs-lookup"><span data-stu-id="90269-167">Note that such Writer Metadata Document attributes as alternate location mappings, explicitly included and excluded files, and restore methods are set at the writer level, not the component level.</span></span> <span data-ttu-id="90269-168"> (需詳細資訊，請參閱 [使用寫入器元資料檔案](working-with-the-writer-metadata-document.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="90269-168">(For more information, see [Working with the Writer Metadata Document](working-with-the-writer-metadata-document.md).)</span></span>

## <a name="component-definition-for-backup-and-restore-operations"></a><span data-ttu-id="90269-169">備份和還原作業的元件定義</span><span class="sxs-lookup"><span data-stu-id="90269-169">Component Definition for Backup and Restore Operations</span></span>

<span data-ttu-id="90269-170">還原和備份作業都必須產生 [*識別事件*](vssgloss-i.md)，而針對這兩個備份和還原，則會由相同的 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 方法來處理。</span><span class="sxs-lookup"><span data-stu-id="90269-170">Both restore and backup operations necessarily generate an [*Identify event*](vssgloss-i.md), and for both backups and restores it will be handled by the same [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) method.</span></span>

<span data-ttu-id="90269-171">在備份作業期間，要求者會使用寫入器的 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 方法所傳回的資訊，來判斷系統上有哪些寫入器，然後判斷要備份的檔案。</span><span class="sxs-lookup"><span data-stu-id="90269-171">During backup operations, requesters use the information returned by a writer's [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) methods to determine which writers are present on the system and then to determine which of their files to back up.</span></span>

<span data-ttu-id="90269-172">在還原作業期間，寫入器的 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 事件所傳回的資訊只會用來建立目前存在於系統上之寫入器的身分識別和狀態;不會使用在還原期間產生的檔案規格資訊。</span><span class="sxs-lookup"><span data-stu-id="90269-172">During restore operations, the information returned by a writer's [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) event is used only to establish the identity and status of writers currently present on the system; the file specification information generated during a restore is not used.</span></span> <span data-ttu-id="90269-173">相反地，在備份時儲存的寫入器元資料檔案會用來取得此資料。</span><span class="sxs-lookup"><span data-stu-id="90269-173">Instead, Writer Metadata Documents stored at backup time are used to obtain this data.</span></span>

<span data-ttu-id="90269-174">一旦在備份作業期間產生，就會儲存寫入器元件資訊以及其餘的寫入器資訊，以支援還原作業。</span><span class="sxs-lookup"><span data-stu-id="90269-174">Once generated during a backup operation, the writer component information, along with the rest of the writer information, is saved to be retrieved to support restore operations.</span></span> <span data-ttu-id="90269-175">要求者必須負責儲存這項資訊。</span><span class="sxs-lookup"><span data-stu-id="90269-175">It is typically the responsibility of the requester to store this information.</span></span>

 

 
