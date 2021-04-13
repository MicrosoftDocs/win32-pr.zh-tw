---
title: 虛擬化根中的快取狀態
description: 描述不同的快取狀態：提供者所管理的檔案或目錄可能具有。
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 43d62ceb1f5ef5bf07000666f336077270b1e86a
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/22/2020
ms.locfileid: "104374162"
---
# <a name="cache-state-in-the-virtualization-root"></a><span data-ttu-id="27aff-103">虛擬化根中的快取狀態</span><span class="sxs-lookup"><span data-stu-id="27aff-103">Cache State In the Virtualization Root</span></span>

<span data-ttu-id="27aff-104">提供者會使用虛擬根目錄下的本機檔案系統作為其所管理專案的快取。</span><span class="sxs-lookup"><span data-stu-id="27aff-104">The provider uses the local file system under the virtualization root as a cache of the items that it manages.</span></span>  <span data-ttu-id="27aff-105"> (檔案或目錄) 的專案可以在本機檔案系統上的六種狀態之一：</span><span class="sxs-lookup"><span data-stu-id="27aff-105">An item (file or directory) can be in one of six states on the local file system:</span></span>

* <span data-ttu-id="27aff-106">網路</span><span class="sxs-lookup"><span data-stu-id="27aff-106">Virtual</span></span>

  <span data-ttu-id="27aff-107">專案不存在於本機磁片上。</span><span class="sxs-lookup"><span data-stu-id="27aff-107">The item does not exist locally on disk.</span></span>  <span data-ttu-id="27aff-108">它會在其父目錄的列舉期間進行投影，例如合成。</span><span class="sxs-lookup"><span data-stu-id="27aff-108">It is projected, i.e. synthesized, during enumerations of its parent directory.</span></span>  <span data-ttu-id="27aff-109">虛擬專案會與可能存在於磁片上的任何專案合併，以呈現上層目錄的完整內容。</span><span class="sxs-lookup"><span data-stu-id="27aff-109">Virtual items are merged with any items that may exist on disk to present the full contents of the parent directory.</span></span>

* <span data-ttu-id="27aff-110">預留位置</span><span class="sxs-lookup"><span data-stu-id="27aff-110">Placeholder</span></span>

  <span data-ttu-id="27aff-111">對於檔案：檔案的內容 (主要資料流程) 不會出現在磁片上。</span><span class="sxs-lookup"><span data-stu-id="27aff-111">For files: The file's content (primary data stream) is not present on the disk.</span></span>  <span data-ttu-id="27aff-112">檔案的中繼資料 (名稱、大小、時間戳記、屬性等 ) 會快取在磁片上。</span><span class="sxs-lookup"><span data-stu-id="27aff-112">The file’s metadata (name, size, timestamps, attributes, etc.) is cached on the disk.</span></span>
  
  <span data-ttu-id="27aff-113">針對目錄：部分或所有目錄的直屬子系 (目錄) 中的檔案和目錄不存在於磁片上，也就是它們仍為虛擬。</span><span class="sxs-lookup"><span data-stu-id="27aff-113">For directories: Some or all of the directory’s immediate descendants (the files and directories in the directory) are not present on the disk, i.e. they are still virtual.</span></span>  <span data-ttu-id="27aff-114">目錄的中繼資料 (名稱、時間戳記、屬性等 ) 會快取在磁片上。</span><span class="sxs-lookup"><span data-stu-id="27aff-114">The directory’s metadata (name, timestamps, attributes, etc.) is cached on the disk.</span></span>

* <span data-ttu-id="27aff-115">水合預留位置</span><span class="sxs-lookup"><span data-stu-id="27aff-115">Hydrated placeholder</span></span>

  <span data-ttu-id="27aff-116">對於檔案：檔案的內容和中繼資料已快取到磁片。</span><span class="sxs-lookup"><span data-stu-id="27aff-116">For files: The file’s content and metadata have been cached to the disk.</span></span>  <span data-ttu-id="27aff-117">也稱為「部分檔案」。</span><span class="sxs-lookup"><span data-stu-id="27aff-117">Also referred to as a "partial file".</span></span>
  
  <span data-ttu-id="27aff-118">針對目錄：在磁片上以預留位置建立的目錄永遠不會變成水合的預留位置目錄。</span><span class="sxs-lookup"><span data-stu-id="27aff-118">For directories: A directory that was created on disk as a placeholder never becomes a hydrated placeholder directory.</span></span>  <span data-ttu-id="27aff-119">這可讓提供者在其備份存放區中新增或移除目錄中的專案，並讓這些變更反映在本機快取中。</span><span class="sxs-lookup"><span data-stu-id="27aff-119">This allows the provider to add or remove items from the directory in its backing store and have those changes be reflected in the local cache.</span></span>

* <span data-ttu-id="27aff-120"> (水合或不) 的中途預留位置</span><span class="sxs-lookup"><span data-stu-id="27aff-120">Dirty placeholder (hydrated or not)</span></span>

  <span data-ttu-id="27aff-121">專案的中繼資料已在本機修改，而且不再是提供者存放區中其狀態的快取。</span><span class="sxs-lookup"><span data-stu-id="27aff-121">The item's metadata has been locally modified and is no longer a cache of its state in the provider's store.</span></span> <span data-ttu-id="27aff-122">請注意，在預留位置目錄下建立或刪除檔案或目錄會導致該預留位置目錄變回。</span><span class="sxs-lookup"><span data-stu-id="27aff-122">Note that creating or deleting a file or directory under a placeholder directory causes that placeholder directory to become dirty.</span></span>

* <span data-ttu-id="27aff-123">完整檔案/目錄</span><span class="sxs-lookup"><span data-stu-id="27aff-123">Full file/directory</span></span>

  <span data-ttu-id="27aff-124">檔案：檔案的內容 (主要資料流程) 已修改。</span><span class="sxs-lookup"><span data-stu-id="27aff-124">For files: The file's content (primary data stream) has been modified.</span></span>  <span data-ttu-id="27aff-125">在提供者的存放區中，該檔案已不再是其狀態的快取。</span><span class="sxs-lookup"><span data-stu-id="27aff-125">The file is no longer a cache of its state in the provider's store.</span></span>  <span data-ttu-id="27aff-126">在本機檔案系統上建立的檔案 (亦即，在所有) 的提供者存放區中都不存在的檔案，也會被視為完整的檔案。</span><span class="sxs-lookup"><span data-stu-id="27aff-126">Files that have been created on the local file system (i.e. that do not exist in the provider's store at all) are also considered to be full files.</span></span>
  
  <span data-ttu-id="27aff-127">若為目錄：在本機檔案系統上建立的目錄 (亦即，在所有) 的提供者存放區中都不存在，則會被視為完整目錄。</span><span class="sxs-lookup"><span data-stu-id="27aff-127">For directories: Directories that have been created on the local file system (i.e. that do not exist in the provider's store at all) are considered to be full directories.</span></span>  <span data-ttu-id="27aff-128">在磁片上建立為預留位置的目錄永遠不會成為完整目錄。</span><span class="sxs-lookup"><span data-stu-id="27aff-128">A directory that was created on disk as a placeholder never becomes a full directory.</span></span>
  
* <span data-ttu-id="27aff-129">墓碑</span><span class="sxs-lookup"><span data-stu-id="27aff-129">Tombstone</span></span>

  <span data-ttu-id="27aff-130">表示已從本機檔案系統刪除之專案的特殊隱藏預留位置。</span><span class="sxs-lookup"><span data-stu-id="27aff-130">A special hidden placeholder that represents an item that has been deleted from the local file system.</span></span>  <span data-ttu-id="27aff-131">列舉目錄時 ProjFS 會將本機專案的集合 (預留位置、完整檔案等 ) 與一組虛擬投射專案合併。</span><span class="sxs-lookup"><span data-stu-id="27aff-131">When a directory is enumerated ProjFS merges the set of local items (placeholders, full files, etc.) with the set of virtual projected items.</span></span>  <span data-ttu-id="27aff-132">如果專案同時出現在本機和投射的集合中，則會優先使用本機專案。</span><span class="sxs-lookup"><span data-stu-id="27aff-132">If an item appears in both the local and projected sets, the local item takes precedence.</span></span>  <span data-ttu-id="27aff-133">如果檔案不存在於本機檔案系統中，就不會有本機狀態，因此它會出現在列舉中。</span><span class="sxs-lookup"><span data-stu-id="27aff-133">If a file does not exist in the local file system there is no local state, so it would appear in the enumeration.</span></span>  <span data-ttu-id="27aff-134">但是，如果該專案已被刪除，則將它顯示在列舉中會是非預期的。</span><span class="sxs-lookup"><span data-stu-id="27aff-134">However if that item had been deleted, having it appear in the enumeration would be unexpected.</span></span>  <span data-ttu-id="27aff-135">使用標記來取代已刪除的專案會產生下列效果：</span><span class="sxs-lookup"><span data-stu-id="27aff-135">Replacing a deleted item with a tombstone results in the following effects:</span></span>

  * <span data-ttu-id="27aff-136">不顯示專案的列舉。</span><span class="sxs-lookup"><span data-stu-id="27aff-136">Enumerations to not reveal the item.</span></span>
  * <span data-ttu-id="27aff-137">檔案開啟時，預期專案存在會失敗，例如「找不到檔案」。</span><span class="sxs-lookup"><span data-stu-id="27aff-137">File opens that expect the item to exist fail with e.g. "file not found".</span></span>
  * <span data-ttu-id="27aff-138">只有當專案不存在時，才會建立預期成功的檔案;ProjFS 會在作業中移除標記。</span><span class="sxs-lookup"><span data-stu-id="27aff-138">File creates that expect to succeed only if the item does not exist succeed; ProjFS removes the tombstone as part of the operation.</span></span>

<span data-ttu-id="27aff-139">若要說明上述狀態，請考慮下列順序（假設有一個 ProjFS 提供者，該提供者位於虛擬根目錄中的單一檔案 "foo.txt" C:\root。</span><span class="sxs-lookup"><span data-stu-id="27aff-139">To illustrate the above states, consider the following sequence, given a ProjFS provider that has a single file "foo.txt" located in the virtualization root C:\root.</span></span>

1. <span data-ttu-id="27aff-140">應用程式會列舉 C:\root。</span><span class="sxs-lookup"><span data-stu-id="27aff-140">An app enumerates C:\root.</span></span>  <span data-ttu-id="27aff-141">它會看到虛擬檔案「foo.txt」。</span><span class="sxs-lookup"><span data-stu-id="27aff-141">It sees the virtual file "foo.txt".</span></span>  <span data-ttu-id="27aff-142">由於尚未存取檔案，因此檔案不存在於磁片上。</span><span class="sxs-lookup"><span data-stu-id="27aff-142">Since the file has not yet been accessed, the file does not exist on disk.</span></span>
1. <span data-ttu-id="27aff-143">應用程式會開啟 C:\root\foo.txt 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="27aff-143">The app opens a handle to C:\root\foo.txt.</span></span>  <span data-ttu-id="27aff-144">ProjFS 會告訴提供者為它建立預留位置。</span><span class="sxs-lookup"><span data-stu-id="27aff-144">ProjFS tells the provider to create a placeholder for it.</span></span>
1. <span data-ttu-id="27aff-145">應用程式會讀取檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="27aff-145">The app reads the content of the file.</span></span>  <span data-ttu-id="27aff-146">提供者會將檔案內容提供給 ProjFS，並快取至 C:\root\foo.txt。</span><span class="sxs-lookup"><span data-stu-id="27aff-146">The provider provides the file content to ProjFS and it is cached to C:\root\foo.txt.</span></span>  <span data-ttu-id="27aff-147">檔案現在是水合預留位置。</span><span class="sxs-lookup"><span data-stu-id="27aff-147">The file is now a hydrated placeholder.</span></span>
1. <span data-ttu-id="27aff-148">應用程式會更新上次修改的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="27aff-148">The app updates the Last Modified timestamp.</span></span>  <span data-ttu-id="27aff-149">檔案現在是中途水合預留位置。</span><span class="sxs-lookup"><span data-stu-id="27aff-149">The file is now a dirty hydrated placeholder.</span></span>
1. <span data-ttu-id="27aff-150">應用程式會開啟檔案寫入存取的控制碼。</span><span class="sxs-lookup"><span data-stu-id="27aff-150">The app opens a handle for write access to the file.</span></span>  <span data-ttu-id="27aff-151">C:\root\foo.txt 現在是完整的檔案。</span><span class="sxs-lookup"><span data-stu-id="27aff-151">C:\root\foo.txt is now a full file.</span></span>
1. <span data-ttu-id="27aff-152">應用程式會刪除 C:\root\foo.txt。</span><span class="sxs-lookup"><span data-stu-id="27aff-152">The app deletes C:\root\foo.txt.</span></span>  <span data-ttu-id="27aff-153">ProjFS 會以標記取代檔案。</span><span class="sxs-lookup"><span data-stu-id="27aff-153">ProjFS replaces the file with a tombstone.</span></span>  <span data-ttu-id="27aff-154">現在，當應用程式列舉 C:\root 時，不會看到 foo.txt。</span><span class="sxs-lookup"><span data-stu-id="27aff-154">Now when the app enumerates C:\root it does not see foo.txt.</span></span>  <span data-ttu-id="27aff-155">如果它嘗試開啟檔案，開啟會失敗並 ERROR_FILE_NOT_FOUND。</span><span class="sxs-lookup"><span data-stu-id="27aff-155">If it tries to open the file, the open fails with ERROR_FILE_NOT_FOUND.</span></span>
