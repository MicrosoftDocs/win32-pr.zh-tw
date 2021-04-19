---
description: 處理元件的其中一個檔案集時，可能需要要求者以遞迴方式遍歷目錄樹狀結構，而這可能需要要求者處理掛接的資料夾和重新分析點 (例如指向不在目前磁片區上之資料的連結) 。
ms.assetid: d0e08598-a8a2-489b-9cb2-e989bed1ce53
title: 使用裝載的資料夾和重新分析點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a7aa88f39361f788f9aac882b4f9d337fd6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966715"
---
# <a name="working-with-mounted-folders-and-reparse-points"></a><span data-ttu-id="07824-103">使用裝載的資料夾和重新分析點</span><span class="sxs-lookup"><span data-stu-id="07824-103">Working with Mounted Folders and Reparse Points</span></span>

<span data-ttu-id="07824-104">處理元件的其中一個檔案集時，可能需要要求者以遞迴方式遍歷目錄樹狀結構，而這可能需要要求者處理掛接的資料夾和重新分析點 (例如指向不在目前磁片區上之資料的連結) 。</span><span class="sxs-lookup"><span data-stu-id="07824-104">Processing one of a component's file sets may require a requester to traverse a directory tree recursively, which can require the requester to handle mounted folders and reparse points (such as links) that point to data that is not on the current volume.</span></span>

<span data-ttu-id="07824-105">要求者在遍歷目錄樹狀結構時，應該遵循掛接的資料夾和重新分析點，而 VSS 則有妥善定義的指導方針來處理它們來進行備份和還原作業。</span><span class="sxs-lookup"><span data-stu-id="07824-105">Requesters are expected to follow mounted folders and reparse points when traversing a directory tree, and VSS has well-defined guidelines for handling them for backup and restore operations.</span></span>

<span data-ttu-id="07824-106">若要說明這些指導方針，請考慮下列範例：</span><span class="sxs-lookup"><span data-stu-id="07824-106">To illustrate these guidelines, consider the following example:</span></span>

-   <span data-ttu-id="07824-107">磁片區 \\ \\ ？ \\磁片區 {GUID \_ 1} 具有磁碟機號 C： \\ 。</span><span class="sxs-lookup"><span data-stu-id="07824-107">The volume \\\\?\\Volume{GUID\_1} has the drive letter C:\\.</span></span>
-   <span data-ttu-id="07824-108">檔案集的路徑為 C： \\ WriterData。</span><span class="sxs-lookup"><span data-stu-id="07824-108">A file set has a path of C:\\WriterData.</span></span>
-   <span data-ttu-id="07824-109">檔案規格 \* 。此檔案會使用 dat。</span><span class="sxs-lookup"><span data-stu-id="07824-109">A file specification \*.dat is used by the file set.</span></span>
-   <span data-ttu-id="07824-110">檔案集的遞迴會設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="07824-110">The file set's recursion is set to **TRUE**.</span></span>
-   <span data-ttu-id="07824-111">目錄 C： \\ WriterData 位於磁片區 \\ \\ ？ \\磁片區 {GUID \_ 1}。</span><span class="sxs-lookup"><span data-stu-id="07824-111">The directory C:\\WriterData is located on the volume \\\\?\\Volume{GUID\_1}.</span></span>
-   <span data-ttu-id="07824-112">目錄 C： \\ WriterData \\ Archive 是掛接的資料夾。</span><span class="sxs-lookup"><span data-stu-id="07824-112">The directory C:\\WriterData\\Archive is a mounted folder.</span></span>
-   <span data-ttu-id="07824-113">磁片區 \\ \\ ？ \\磁片區 {GUID \_ 2} 與裝載的資料夾 C： \\ WriterData Archive 相關聯 \\ 。</span><span class="sxs-lookup"><span data-stu-id="07824-113">The volume \\\\?\\Volume{GUID\_2} is associated with the mounted folder C:\\WriterData\\Archive.</span></span>

## <a name="handling-mounted-folders-and-reparse-points-during-backup"></a><span data-ttu-id="07824-114">在備份期間處理裝載的資料夾和重新分析點</span><span class="sxs-lookup"><span data-stu-id="07824-114">Handling Mounted Folders and Reparse Points during Backup</span></span>

<span data-ttu-id="07824-115">執行遞迴備份時，在 VSS 下處理裝載的資料夾和重新分析點的基本規則，可摘要如下：</span><span class="sxs-lookup"><span data-stu-id="07824-115">The basic rules for handling mounted folders and reparse points under VSS when performing a recursive backup can be summarized as follows:</span></span>

-   <span data-ttu-id="07824-116">路徑會在已裝載的資料夾和重新分析點上遵循。</span><span class="sxs-lookup"><span data-stu-id="07824-116">Paths are followed across mounted folders and reparse points.</span></span>
-   <span data-ttu-id="07824-117">如果載入的資料夾或重新分析點指向磁片區，該磁片區應該會被陰影複製。</span><span class="sxs-lookup"><span data-stu-id="07824-117">If a mounted folder or reparse point points to a volume, that volume should be shadow copied.</span></span>
-   <span data-ttu-id="07824-118">如果磁片區包含已掛接的資料夾或重新分析點，這些資料夾將會出現在磁片區的陰影複製中。</span><span class="sxs-lookup"><span data-stu-id="07824-118">If a volume contains mounted folders or reparse points, these will appear in the shadow copy of the volume.</span></span>
-   <span data-ttu-id="07824-119">裝載的資料夾或重新分析點下的資料會在掛接的資料夾或重新分析點指向之磁片區的陰影複製中捕捉。</span><span class="sxs-lookup"><span data-stu-id="07824-119">Data that is under the mounted folder or reparse point is captured in the shadow copy of the volume that the mounted folder or reparse point points to.</span></span>

<span data-ttu-id="07824-120">為了說明使用上述範例，因為已設定遞迴旗標，要求者必須檢查 C： WriterData Archive 下的所有資料， \\ \\ 以及以下的資料。</span><span class="sxs-lookup"><span data-stu-id="07824-120">To illustrate using the example above, because the recursive flag is set, the requester must examine all data under C:\\WriterData\\Archive and below.</span></span>

<span data-ttu-id="07824-121">要求者必須新增磁碟機號 C： (的磁片區 \\ \\ \\ ？ \\磁片區 {GUID \_ 1} ) ，以及與裝載的資料夾 C： \\ WriterData Archive (相關聯的磁片區 \\ \\ \\ ？ \\磁片區 {GUID \_ 2} 使用 [**>ivssbackupcomponents：： AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)) 至陰影複製集。</span><span class="sxs-lookup"><span data-stu-id="07824-121">The requester must add both the volume with drive letter C:\\ (\\\\?\\Volume{GUID\_1}) and the volume associated with the mounted folder C:\\WriterData\\Archive (\\\\?\\Volume{GUID\_2}) to the shadow copy set using [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).</span></span>

<span data-ttu-id="07824-122">載入的資料夾 C： \\ WriterData \\ Archive 會出現在磁片區的陰影複製中 \\ \\ ？ \\磁片區 {GUID \_ 1}，其具有名為 deviceObject1 的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="07824-122">The mounted folder C:\\WriterData\\Archive appears in the shadow copy of volume \\\\?\\Volume{GUID\_1}, which has a device object named deviceObject1.</span></span>

<span data-ttu-id="07824-123">不過，VSS 不會在該掛接的資料夾下複製任何資料 (資料 \\ \\ 嗎？ \\磁片區 {GUID \_ 2} ) 到 deviceObject1 所參考的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="07824-123">However, VSS will not copy any data under that mounted folder (data on \\\\?\\Volume{GUID\_2}) to the shadow copy referenced by deviceObject1.</span></span> <span data-ttu-id="07824-124">而是在的陰影複製中捕捉該資料 \\ \\ 嗎？ \\磁片區 {GUID \_ 2}，其具有名為 deviceObject2 的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="07824-124">Instead, that data is captured in the shadow copy of \\\\?\\Volume{GUID\_2}, which has a device object named deviceObject2.</span></span>

<span data-ttu-id="07824-125">因此，在 C： WriterData 下備份陰影複製檔案的要求者 \\ 將會使用 deviceObject1 WriterData 的路徑 \\ 來搜尋符合 C： WriterData 的檔案 \\ \\ \* 。</span><span class="sxs-lookup"><span data-stu-id="07824-125">Therefore, a requester that is backing up shadow copied files under C:\\WriterData will use a path of deviceObject1\\WriterData to search for files matching C:\\WriterData\\\*.dat.</span></span>

<span data-ttu-id="07824-126">若要備份 C： WriterData Archive 下的陰影複製 \\ \\ 檔案，要求者將會使用 deviceObject2 (的路徑，因為根目錄是 \\ \\ ？ \\磁片區 {GUID \_ 2} 與裝載的資料夾 C： Writer 封存) 建立關聯 \\ \\ ，以搜尋符合 C： \\ WriterData Archive 的檔案 \\ \\ \* 。</span><span class="sxs-lookup"><span data-stu-id="07824-126">To back up shadow copied files under C:\\WriterData\\Archive, the requester will use a path of deviceObject2 (because the root directory of \\\\?\\Volume{GUID\_2} was associated with the mounted folder C:\\Writer\\Archive) to search for files matching C:\\WriterData\\Archive\\\*.dat.</span></span>

<span data-ttu-id="07824-127">請注意，重新分析點的處理方式與裝載的資料夾相同。</span><span class="sxs-lookup"><span data-stu-id="07824-127">Note that a reparse point is handled in the same way as a mounted folder.</span></span> <span data-ttu-id="07824-128">重新分析點會出現在第一個磁片區的陰影複製中。</span><span class="sxs-lookup"><span data-stu-id="07824-128">The reparse point appears in the shadow copy of the first volume.</span></span> <span data-ttu-id="07824-129">重新分析點下的資料會出現在第二個磁片區的陰影複製中。</span><span class="sxs-lookup"><span data-stu-id="07824-129">The data under the reparse point appears in the shadow copy of the second volume.</span></span>

<span data-ttu-id="07824-130">在備份期間，要求者應儲存掛接的資料夾及其相關聯之磁片區的相關資訊，以及重新分析點及其目標，以確保所有資料都已正確備份和還原。</span><span class="sxs-lookup"><span data-stu-id="07824-130">During backup, requesters should store information about mounted folders and the volumes associated with them as well as reparse points and their targets to ensure that all data is backed up and restored correctly.</span></span>

## <a name="handling-mount-and-reparse-points-during-restore"></a><span data-ttu-id="07824-131">在還原期間處理掛接和重新分析點</span><span class="sxs-lookup"><span data-stu-id="07824-131">Handling Mount and Reparse Points during Restore</span></span>

<span data-ttu-id="07824-132">還原檔案時，要求者必須遵循與備份期間不同的指導方針 (忽略 [*替代位置對應*](vssgloss-a.md) 和 [*新的目標位置*](vssgloss-n.md)) 等問題：</span><span class="sxs-lookup"><span data-stu-id="07824-132">When restoring files, the requester must follow guidelines somewhat different from those that were used during backup (ignoring issues such as [*alternate location mapping*](vssgloss-a.md) and [*new target location*](vssgloss-n.md)):</span></span>

-   <span data-ttu-id="07824-133">如同之前，如果需要遞迴，則會在裝載的資料夾和重新分析點上遵循路徑。</span><span class="sxs-lookup"><span data-stu-id="07824-133">As before, if recursion is required, paths are followed across mounted folders and reparse points.</span></span>
-   <span data-ttu-id="07824-134">已載入的資料夾將會還原。</span><span class="sxs-lookup"><span data-stu-id="07824-134">Mounted folders are to be restored.</span></span>
-   <span data-ttu-id="07824-135">裝載的資料夾和重新分析點的還原位置是由其原始路徑所決定。</span><span class="sxs-lookup"><span data-stu-id="07824-135">The restoration locations of mounted folders and reparse points are those determined by their original paths.</span></span>

<span data-ttu-id="07824-136">如果備份與還原之間有磁片區名稱，也就是說，您不需要重新建立磁片區，則還原的已載入資料夾和重新分析點應該指向正確的磁片區。</span><span class="sxs-lookup"><span data-stu-id="07824-136">If the volume names persist between backup and restore—that is, you do not re-create the volumes—restored mounted folders and reparse points should point to the correct volumes.</span></span>

<span data-ttu-id="07824-137">因此，在上述範例中，如果已將裝載的資料夾 C： \\ WriterData \\ Archive 還原至 (\\ \\ ？ \\磁片區 {GUID \_ 1} ) ，且先前與其相關聯的磁片區已還原到 (\\ \\ 嗎？ \\磁片區 {GUID \_ 2} ) ，還原的檔案和檔案結構會是正確且一致的。</span><span class="sxs-lookup"><span data-stu-id="07824-137">Therefore, in the example discussed above, if the mounted folder C:\\WriterData\\Archive was restored to (\\\\?\\Volume{GUID\_1}) and the volume previously associated with it was restored to (\\\\?\\Volume{GUID\_2}), the restored files and file structure would be correct and consistent.</span></span>

<span data-ttu-id="07824-138">資料可能會在磁片區名稱變更的系統上還原。</span><span class="sxs-lookup"><span data-stu-id="07824-138">It may happen that data is restored to a system where volume names changed.</span></span> <span data-ttu-id="07824-139">這可能是因為磁片損毀，而您可能需要手動執行系統復原並重新建立磁片區。</span><span class="sxs-lookup"><span data-stu-id="07824-139">This could be due to disk crashes, where you might need to perform a manual system recovery and re-create volumes.</span></span> <span data-ttu-id="07824-140">在這種情況下，在還原之後，裝載的資料夾和重新分析點將不再有效。</span><span class="sxs-lookup"><span data-stu-id="07824-140">In this type of situation, mounted folders and reparse points will no longer be valid after restore.</span></span> <span data-ttu-id="07824-141">若要在還原的磁片區上重新建立檔案和檔案結構，將需要刪除已還原的已掛接資料夾和重新分析點，然後在磁片上重新建立它們。</span><span class="sxs-lookup"><span data-stu-id="07824-141">To re-create the files and file structure on the restored volume will require deleting the restored mounted folders and reparse points and re-creating them on disk.</span></span> <span data-ttu-id="07824-142">備份應用程式會決定是否適當。</span><span class="sxs-lookup"><span data-stu-id="07824-142">It is up to the backup application to decide whether this is appropriate.</span></span>

<span data-ttu-id="07824-143">請注意，已載入之資料夾的還原目的地可能已被佔用。</span><span class="sxs-lookup"><span data-stu-id="07824-143">Note that it is possible that the restore destination for a mounted folder is already occupied.</span></span> <span data-ttu-id="07824-144">例如，C： \\ WriterData \\ Archive 可能已經包含一些檔案。</span><span class="sxs-lookup"><span data-stu-id="07824-144">For example, C:\\WriterData\\Archive might already contain some files.</span></span> <span data-ttu-id="07824-145">備份應用程式會決定如何處理這種情況。</span><span class="sxs-lookup"><span data-stu-id="07824-145">It is up to the backup application to decide how to handle this situation.</span></span>

 

 



