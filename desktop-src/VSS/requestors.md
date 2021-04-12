---
description: 要求者是使用 VSS API 的任何應用程式 (特別是 >ivssbackupcomponents 介面) 要求磁碟區陰影複製服務的服務，以建立和管理一或多個磁片區的陰影複製和陰影複製集。
ms.assetid: e49920d0-5b66-4aa1-b3ca-641629df5f8a
title: 要求者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b676b8cd287365b257e3b6ee85a7e47a70f88ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192288"
---
# <a name="requesters"></a><span data-ttu-id="ab69a-103">要求者</span><span class="sxs-lookup"><span data-stu-id="ab69a-103">Requesters</span></span>

<span data-ttu-id="ab69a-104">要求 [*者是使用*](vssgloss-r.md) VSS API 的任何應用程式 (特別是 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面) 要求磁碟區陰影複製服務的服務，以建立和管理一或多個磁片區的陰影複製和陰影複製集。</span><span class="sxs-lookup"><span data-stu-id="ab69a-104">A [*requester*](vssgloss-r.md) is any application that uses the VSS API (specifically the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface) to request the services of the Volume Shadow Copy Service to create and manage shadow copies and shadow copy sets of one or more volumes.</span></span>

<span data-ttu-id="ab69a-105">要求者 (的最常見範例和本檔中所述的唯一) 是 VSS 感知的備份/還原應用程式，它會使用陰影複製的資料做為其備份作業的穩定來源。</span><span class="sxs-lookup"><span data-stu-id="ab69a-105">The most typical example of a requester (and the only one addressed in this documentation) is a VSS-aware backup/restore application, which uses shadow-copied data as a stable source for its backup operations.</span></span>

<span data-ttu-id="ab69a-106">除了初始陰影複製之外，備份/復原要求者應用程式還會與資料產生者 (寫入器通訊) 收集系統資訊，以及指示寫入器準備資料進行備份。</span><span class="sxs-lookup"><span data-stu-id="ab69a-106">In addition to initiating shadow copies, backup/recover requester applications communicate with data producers (writers) to gather information on the system and to signal writers to prepare their data for backup.</span></span>

## <a name="requester-state"></a><span data-ttu-id="ab69a-107">要求者狀態</span><span class="sxs-lookup"><span data-stu-id="ab69a-107">Requester State</span></span>

<span data-ttu-id="ab69a-108">要求者會將其狀態資訊保留在名為「備份元件」檔的 XML 中繼資料物件中。</span><span class="sxs-lookup"><span data-stu-id="ab69a-108">A requester maintains its state information in an XML-based metadata object called the Backup Components Document.</span></span> <span data-ttu-id="ab69a-109">要求者中繼資料是必要的，但不足以允許要求者進行備份，然後還原檔案系統。</span><span class="sxs-lookup"><span data-stu-id="ab69a-109">The requester metadata is necessary, but not sufficient to allow a requester to back up and then restore a file system.</span></span> <span data-ttu-id="ab69a-110">原因如下：</span><span class="sxs-lookup"><span data-stu-id="ab69a-110">The reasons for this are the following:</span></span>

-   <span data-ttu-id="ab69a-111">在備份作業期間，只會在備份中包含的所有元件的子集：[*其*](vssgloss-s.md) 備份元件，而不是可針對備份的備份元件進行選取，並且可針對已在備份中 [*明確包含*](vssgloss-e.md) 的備份元件進行選擇，也就是將其資訊新增至要求者的備份元件檔。</span><span class="sxs-lookup"><span data-stu-id="ab69a-111">During a backup operation, only a subset of all the components involved in the backup—[*nonselectable for backup*](vssgloss-s.md) components without selectable for backup ancestors and selectable for backup components that have been [*included explicitly*](vssgloss-e.md) in the backup—have had their information added to the requester's Backup Components Document.</span></span>
-   <span data-ttu-id="ab69a-112">即使是新增至備份元件檔的元件，也不完整的資訊，也不會包含檔案和路徑規格。</span><span class="sxs-lookup"><span data-stu-id="ab69a-112">The information even for those components added to the Backup Components Document is incomplete—file and path specifications are not included.</span></span>
-   <span data-ttu-id="ab69a-113">在還原作業期間，可 [*針對還原選取*](vssgloss-s.md)[*隱含包含*](vssgloss-i.md)在備份中的元件，因此可以明確地包含在還原中。</span><span class="sxs-lookup"><span data-stu-id="ab69a-113">During restore operations, a component [*implicitly included*](vssgloss-i.md) in the backup may be [*selectable for restore*](vssgloss-s.md) and therefore can be explicitly included in the restore.</span></span> <span data-ttu-id="ab69a-114">這將需要更新要求者的備份元件檔，並提供來自寫入器寫入器元資料檔案之預存複本的資訊。</span><span class="sxs-lookup"><span data-stu-id="ab69a-114">This will require the updating of the requester's Backup Components Document with information from stored copies of a writer's Writer Metadata Document.</span></span>

<span data-ttu-id="ab69a-115">若要允許完整的備份或還原作業規格，VSS API 可讓要求者在備份期間查詢執行中的寫入器中繼資料 () 或在還原) 期間檢查儲存的寫入器中繼資料 (。</span><span class="sxs-lookup"><span data-stu-id="ab69a-115">To allow for full specification of a backup or restore operation, the VSS API allows the requester to query running writers' metadata (during backups) or examine stored writer metadata (during restores).</span></span> <span data-ttu-id="ab69a-116">此外，寫入器可以在備份或還原作業期間，修改備份元件檔中的元件資訊。</span><span class="sxs-lookup"><span data-stu-id="ab69a-116">In addition, a writer can modify component information in the Backup Components Document in the course of a backup or restore operation.</span></span>

<span data-ttu-id="ab69a-117">使用已針對備份和還原選取哪些元件的相關資訊，以及有關元件選取的規則 (如需詳細資訊，請參閱 [設定元件組織](definition-of-components-by-writers.md) 和 [使用 Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md)) ，要求者可以判斷需要備份或還原的寫入器檔案，以及可在何處找到這些檔案。</span><span class="sxs-lookup"><span data-stu-id="ab69a-117">Using the information about which components have been selected for backup and restore and the rules regarding component selection (for more information, see [Setting up Component Organization](definition-of-components-by-writers.md) and [Working with Selectability and Logical Paths](working-with-selectability-and-logical-paths.md)), a requester can determine which files of which writer it needs to back up or restore, and where it can find those files.</span></span>

<span data-ttu-id="ab69a-118">在備份過程中，要求者和寫入器中繼資料必須儲存，才能用於還原。</span><span class="sxs-lookup"><span data-stu-id="ab69a-118">As part of a backup, both requester and writer metadata must be stored so that it can be used in the restore.</span></span> <span data-ttu-id="ab69a-119">相反地，還原作業需要抓取舊的備份元件和寫入器元資料檔案，以取得還原檔案的完整指示。</span><span class="sxs-lookup"><span data-stu-id="ab69a-119">Conversely, restore operations require the retrieval of the old Backup Components and Writer Metadata Documents to obtain full instructions on restoring files.</span></span>

## <a name="requester-interprocess-communication"></a><span data-ttu-id="ab69a-120">要求者處理序間通訊</span><span class="sxs-lookup"><span data-stu-id="ab69a-120">Requester Interprocess Communication</span></span>

<span data-ttu-id="ab69a-121">要求者會藉由在要求者 API 中透過各種呼叫產生 COM 事件，來維持對 VSS 備份和還原作業的控制權。</span><span class="sxs-lookup"><span data-stu-id="ab69a-121">The requester maintains control over VSS backup and restore operations by generating COM events through various calls in the requester API.</span></span> <span data-ttu-id="ab69a-122">這些呼叫可以執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="ab69a-122">These calls can do the following:</span></span>

-   <span data-ttu-id="ab69a-123">要求提供者（例如， [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) ）會讓提供者建立所選磁片區的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="ab69a-123">Make requests of the providers, for example, [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) causes the provider to create a shadow copy of the selected volume.</span></span>
-   <span data-ttu-id="ab69a-124">觸發寫入器以傳回信息，例如， [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) 可讓要求者取得每個寫入器的寫入器元資料檔案。</span><span class="sxs-lookup"><span data-stu-id="ab69a-124">Trigger the writers to return information, for example, [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) enables the requester to obtain each writer's Writer Metadata Document.</span></span>
-   <span data-ttu-id="ab69a-125">需要寫入器來準備或處理陰影複製和備份作業的各個階段，例如， [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) 會發出 i/o 凍結的寫入器。</span><span class="sxs-lookup"><span data-stu-id="ab69a-125">Require writers to prepare for or handle various phases of the shadow copy and backup operations, for example, [**IVssBackupComponents::PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) signals writers to set up for the I/O freeze.</span></span>

<span data-ttu-id="ab69a-126">要求者會透過即時或儲存的寫入器元資料檔案，以及透過使用 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面（可供寫入器進行更新），從寫入器接收資訊。</span><span class="sxs-lookup"><span data-stu-id="ab69a-126">A requester receives information from the writers through live or stored Writer Metadata Documents and through the use of the [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface, which the writer can update.</span></span>

## <a name="life-cycle-of-a-requester-during-backup"></a><span data-ttu-id="ab69a-127">備份期間要求者的生命週期</span><span class="sxs-lookup"><span data-stu-id="ab69a-127">Life Cycle of a Requester during Backup</span></span>

<span data-ttu-id="ab69a-128">以下是備份的要求者生命週期摘要：</span><span class="sxs-lookup"><span data-stu-id="ab69a-128">The following is a summary of the requester life cycle for backup:</span></span>

1.  <span data-ttu-id="ab69a-129">具現化並初始化 VSS API 介面。</span><span class="sxs-lookup"><span data-stu-id="ab69a-129">Instantiate and initialize VSS API interfaces.</span></span>
2.  <span data-ttu-id="ab69a-130">聯絡寫入器並取得其資訊。</span><span class="sxs-lookup"><span data-stu-id="ab69a-130">Contact writers and retrieve their information.</span></span>
3.  <span data-ttu-id="ab69a-131">選擇要備份的資料。</span><span class="sxs-lookup"><span data-stu-id="ab69a-131">Choose data to back up.</span></span>
4.  <span data-ttu-id="ab69a-132">要求提供者的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="ab69a-132">Request a shadow copy of the provider.</span></span>
5.  <span data-ttu-id="ab69a-133">備份資料。</span><span class="sxs-lookup"><span data-stu-id="ab69a-133">Back up the data.</span></span>
6.  <span data-ttu-id="ab69a-134">釋放介面和陰影複製。</span><span class="sxs-lookup"><span data-stu-id="ab69a-134">Release the interface and the shadow copy.</span></span>

## <a name="life-cycle-of-a-requester-during-restore"></a><span data-ttu-id="ab69a-135">在還原期間要求者的生命週期</span><span class="sxs-lookup"><span data-stu-id="ab69a-135">Life Cycle of a Requester during Restore</span></span>

<span data-ttu-id="ab69a-136">還原生命週期不需要陰影複製，但仍需要寫入合作：</span><span class="sxs-lookup"><span data-stu-id="ab69a-136">The restore life cycle does not require a shadow copy, but still requires writer cooperation:</span></span>

1.  <span data-ttu-id="ab69a-137">具現化 VSS API 介面。</span><span class="sxs-lookup"><span data-stu-id="ab69a-137">Instantiate VSS API interfaces.</span></span>
2.  <span data-ttu-id="ab69a-138">藉由載入儲存的備份元件檔，初始化還原作業的要求者。</span><span class="sxs-lookup"><span data-stu-id="ab69a-138">Initialize the requester for the restore operation by loading a stored Backup Components Document.</span></span>
3.  <span data-ttu-id="ab69a-139">取出儲存的寫入器中繼資料和備份元件檔。</span><span class="sxs-lookup"><span data-stu-id="ab69a-139">Retrieve stored Writer Metadata and Backup Components Documents.</span></span>
4.  <span data-ttu-id="ab69a-140">請聯絡寫入器以初始化合作。</span><span class="sxs-lookup"><span data-stu-id="ab69a-140">Contact the writers to initialize cooperation.</span></span>
5.  <span data-ttu-id="ab69a-141">檢查備份元件檔的寫入器更新。</span><span class="sxs-lookup"><span data-stu-id="ab69a-141">Check for writer updates to the Backup Components Document.</span></span>
6.  <span data-ttu-id="ab69a-142">還原資料。</span><span class="sxs-lookup"><span data-stu-id="ab69a-142">Restore the data.</span></span>

 

 



