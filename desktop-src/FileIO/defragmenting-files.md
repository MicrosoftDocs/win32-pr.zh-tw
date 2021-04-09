---
description: 磁碟重組是指將檔案的部分移到磁片上以重組檔案的程式，也就是在磁片上移動檔案叢集以使其成為連續的進程。
ms.assetid: 27ccaab7-ec89-489b-80dc-df9beb7969bc
title: 磁碟重組檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b2d079f58ec98f320356a477531616788f84ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848674"
---
# <a name="defragmenting-files"></a><span data-ttu-id="1f1bc-103">磁碟重組檔案</span><span class="sxs-lookup"><span data-stu-id="1f1bc-103">Defragmenting Files</span></span>

<span data-ttu-id="1f1bc-104">當檔案寫入磁片時，有時檔案無法寫入連續的叢集中。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-104">When a file is written to a disk, sometimes the file cannot be written in contiguous clusters.</span></span> <span data-ttu-id="1f1bc-105">非連續的叢集會減緩讀取和寫入檔案的程式。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-105">Noncontiguous clusters slow down the process of reading and writing a file.</span></span> <span data-ttu-id="1f1bc-106">這是不連續叢集的磁片上的進一步的，這是因為移動硬碟的讀取/寫入標頭所需的時間，所以問題越糟。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-106">The further apart on a disk the noncontiguous clusters are, the worse the issue, because of the time it takes to move the read/write head of a hard disk drive.</span></span> <span data-ttu-id="1f1bc-107">具有非連續叢集的檔案會 *分散*。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-107">A file with noncontiguous clusters is *fragmented*.</span></span> <span data-ttu-id="1f1bc-108">為了將檔案優化以進行快速存取，磁片區可進行磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-108">To optimize files for fast access, a volume can be defragmented.</span></span>

<span data-ttu-id="1f1bc-109">*磁碟重組* 是指將檔案的部分移到磁片上以重組檔案的程式，也就是在磁片上移動檔案叢集以使其成為連續的進程。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-109">*Defragmentation* is the process of moving portions of files around on a disk to defragment files, that is, the process of moving file clusters on a disk to make them contiguous.</span></span> <span data-ttu-id="1f1bc-110">如需詳細資訊，請參閱下列各節：</span><span class="sxs-lookup"><span data-stu-id="1f1bc-110">For more information, see the following sections:</span></span>

-   [<span data-ttu-id="1f1bc-111">磁碟重組檔案</span><span class="sxs-lookup"><span data-stu-id="1f1bc-111">Defragmenting a file</span></span>](#defragmenting-a-file)
-   [<span data-ttu-id="1f1bc-112">將磁碟重組與陰影複製之間的互動降至最低</span><span class="sxs-lookup"><span data-stu-id="1f1bc-112">Minimizing interactions between defragmentation and shadow copies</span></span>](#minimizing-interactions-between-defragmentation-and-shadow-copies)
-   [<span data-ttu-id="1f1bc-113">支援磁碟重組的檔案、資料流程和資料流程類型</span><span class="sxs-lookup"><span data-stu-id="1f1bc-113">Files, streams, and stream types supported for defragmentation</span></span>](#files-streams-and-stream-types-supported-for-defragmentation)

## <a name="defragmenting-a-file"></a><span data-ttu-id="1f1bc-114">磁碟重組檔案</span><span class="sxs-lookup"><span data-stu-id="1f1bc-114">Defragmenting a file</span></span>

<span data-ttu-id="1f1bc-115">在簡單的單一工作作業系統中，重組軟體是唯一的工作，而且沒有其他進程可讀取或寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-115">In a simple single-tasking operating system, the defragmentation software is the only task, and there are no other processes to read from or write to the disk.</span></span> <span data-ttu-id="1f1bc-116">不過，在多工作業系統中，某些進程可以讀取和寫入硬碟，而另一個進程則會將該硬碟的磁片磁碟機進行磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-116">However, in a multitasking operating system, some processes can be reading from and writing to a hard disk drive while another process is defragmenting that hard disk drive.</span></span> <span data-ttu-id="1f1bc-117">秘訣是避免寫入正在進行磁碟重組的檔案，而不需要停止撰寫程式很長的時間。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-117">The trick is to avoid writes to a file that is being defragmented without stopping the writing process for very long.</span></span> <span data-ttu-id="1f1bc-118">解決這個問題並不容易，但還是有可能發生。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-118">Solving this problem is not trivial, but it is possible.</span></span>

<span data-ttu-id="1f1bc-119">若要允許重組而不需要詳細瞭解檔案系統磁片結構，則會提供一組三個控制項代碼。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-119">To allow defragmentation without requiring detailed knowledge of a file system disk structure, a set of three control codes is provided.</span></span> <span data-ttu-id="1f1bc-120">控制碼提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="1f1bc-120">The control codes provide the following functionality:</span></span>

-   <span data-ttu-id="1f1bc-121">讓應用程式找出空的叢集</span><span class="sxs-lookup"><span data-stu-id="1f1bc-121">Enable applications to locate empty clusters</span></span>
-   <span data-ttu-id="1f1bc-122">判斷檔案叢集的磁片位置</span><span class="sxs-lookup"><span data-stu-id="1f1bc-122">Determine the disk location of file clusters</span></span>
-   <span data-ttu-id="1f1bc-123">移動磁片上的叢集</span><span class="sxs-lookup"><span data-stu-id="1f1bc-123">Move clusters on a disk</span></span>

<span data-ttu-id="1f1bc-124">控制程式代碼也會以透明的方式處理抑制的問題，並允許其他進程在移動期間讀取和寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-124">The control codes also transparently handle the problem of inhibiting and allowing other processes to read from and write to files during moves.</span></span>

<span data-ttu-id="1f1bc-125">您可以執行這些作業，而不需要抑制其他進程執行。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-125">These operations can be performed without inhibiting other processes from running.</span></span> <span data-ttu-id="1f1bc-126">不過，當磁片磁碟機正在進行磁碟重組時，其他進程會有較慢的回應時間。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-126">However, the other processes have slower response times while a disk drive is being defragmented.</span></span>

<span data-ttu-id="1f1bc-127">**重組檔案**</span><span class="sxs-lookup"><span data-stu-id="1f1bc-127">**To defragment a file**</span></span>

1.  <span data-ttu-id="1f1bc-128">使用 [**FSCTL \_ 取得磁片 \_ 區 \_ 點陣圖**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap) 控制項程式碼，找出磁片區上夠大的位置，以接受整個檔案。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-128">Use the [**FSCTL\_GET\_VOLUME\_BITMAP**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap) control code to find a place on the volume that is large enough to accept an entire file.</span></span>
    > [!Note]  
    > <span data-ttu-id="1f1bc-129">必要時，請將其他檔案移至夠大的位置。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-129">If necessary, move other files to make a place that is large enough.</span></span> <span data-ttu-id="1f1bc-130">在理想的情況下，在檔案的第一個範圍之後，您可以將後續範圍移到第一個範圍之後的空間中，有足夠的未配置叢集。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-130">Ideally, there is enough unallocated clusters after the first extent of the file that you can move subsequent extents into the space after the first extent.</span></span>

     

2.  <span data-ttu-id="1f1bc-131">使用 [**FSCTL \_ get 抓取 \_ \_ 指標**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers) 控制項程式碼，取得磁片上檔案目前配置的對應。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-131">Use the [**FSCTL\_GET\_RETRIEVAL\_POINTERS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers) control code to get a map of the current layout of the file on the disk.</span></span>
3.  <span data-ttu-id="1f1bc-132">逐步解說 [**FSCTL \_ GET 抓取 \_ \_ 指標**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers)所傳回的抓取 [**\_ 指標 \_ 緩衝區**](/windows/desktop/api/WinIoCtl/ns-winioctl-retrieval_pointers_buffer)結構。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-132">Walk the [**RETRIEVAL\_POINTERS\_BUFFER**](/windows/desktop/api/WinIoCtl/ns-winioctl-retrieval_pointers_buffer) structure returned by [**FSCTL\_GET\_RETRIEVAL\_POINTERS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers).</span></span>
4.  <span data-ttu-id="1f1bc-133">當您逐步執行結構時，請使用 [**FSCTL \_ move \_ FILE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) control 程式碼來移動每個叢集。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-133">Use the [**FSCTL\_MOVE\_FILE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) control code to move each cluster as you walk the structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="1f1bc-134">當其他進程寫入磁片時，您可能需要在不同的時間更新點陣圖或抓取結構。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-134">You may need to renew either the bitmap or the retrieval structure, or both at various times as other processes write to the disk.</span></span>

     

<span data-ttu-id="1f1bc-135">重組程式中使用的兩個作業需要磁片區的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-135">Two of the operations that are used in the defragmentation process require a handle to a volume.</span></span> <span data-ttu-id="1f1bc-136">只有系統管理員可以取得磁片區的控制碼，因此只有系統管理員可以重組磁片區。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-136">Only administrators can obtain a handle to a volume, so only administrators can defragment a volume.</span></span> <span data-ttu-id="1f1bc-137">應用程式應該檢查嘗試執行磁碟重組軟體之使用者的許可權，如果使用者沒有適當的許可權，就不應該允許使用者重組磁片區。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-137">An application should check the rights of a user who attempts to run defragmentation software, and it should not allow a user to defragment a volume if the user does not have the appropriate rights.</span></span>

<span data-ttu-id="1f1bc-138">當您在 FAT 或 FAT32 檔案系統磁片區的磁碟重組期間使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 來開啟目錄時，請指定 **一般 \_ 讀取** 存取遮罩值。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-138">When using [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to open a directory during defragmentation of a FAT or FAT32 file system volume, specify the **GENERIC\_READ** access mask value.</span></span> <span data-ttu-id="1f1bc-139">請勿指定 **\_ 允許** 的存取遮罩值上限。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-139">Do not specify the **MAXIMUM\_ALLOWED** access mask value.</span></span> <span data-ttu-id="1f1bc-140">如果已完成，就會拒絕存取目錄。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-140">Access to the directory is denied if that is done.</span></span>

<span data-ttu-id="1f1bc-141">請勿嘗試在 NTFS 檔案系統中移動延伸超過叢集舍入檔案大小的已配置叢集，因為結果會是錯誤。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-141">Do not attempt to move allocated clusters in an NTFS file system that extend beyond the cluster rounded file size, because the result is an error.</span></span>

<span data-ttu-id="1f1bc-142">您可以針對 NTFS 檔案系統磁片區中的重新剖析點、點陣圖和屬性清單進行磁碟重組、開啟以供讀取和同步處理，以及使用 *file*：*name*：*type* 語法來命名。例如， *dirname*： $i 30： $INDEX \_ 配置、 *mrp*：： $DATA、 *mrp*：： $REPARSE \_ 點和 *mrp*：： $ATTRIBUTE \_ 清單。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-142">Re-parse points, bitmaps, and attribute lists in NTFS file system volumes can be defragmented, opened for reading and synchronization, and named using the *file*:*name*:*type* syntax; for example, *dirname*:$i30:$INDEX\_ALLOCATION, *mrp*::$DATA, *mrp*::$REPARSE\_POINT, and *mrp*::$ATTRIBUTE\_LIST.</span></span>

<span data-ttu-id="1f1bc-143">對 NTFS 檔案系統磁片區進行磁碟重組時，允許重組超過檔案配置大小的虛擬叢集。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-143">When defragmenting NTFS file system volumes, defragmenting a virtual cluster beyond the allocation size of a file is allowed.</span></span>

## <a name="minimizing-interactions-between-defragmentation-and-shadow-copies"></a><span data-ttu-id="1f1bc-144">將磁碟重組與陰影複製之間的互動降至最低</span><span class="sxs-lookup"><span data-stu-id="1f1bc-144">Minimizing interactions between defragmentation and shadow copies</span></span>

<span data-ttu-id="1f1bc-145">可能的話，請以 16 kb 的 (KB) 遞增方式，在彼此相對的區塊中移動資料。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-145">When possible, move data in blocks aligned relative to each other in 16-kilobyte (KB) increments.</span></span> <span data-ttu-id="1f1bc-146">這可在啟用陰影複製時減少複製時的額外負荷，因為陰影複製空間會增加，而且當發生下列狀況時，效能會降低：</span><span class="sxs-lookup"><span data-stu-id="1f1bc-146">This reduces copy-on-write overhead when shadow copies are enabled, because shadow copy space is increased and performance is reduced when the following conditions occur:</span></span>

-   <span data-ttu-id="1f1bc-147">移動要求區塊大小小於或等於 16 KB。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-147">The move request block size is less than or equal to 16 KB.</span></span>
-   <span data-ttu-id="1f1bc-148">移動差異不是以 16 KB 為單位遞增。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-148">The move delta is not in increments of 16 KB.</span></span>

<span data-ttu-id="1f1bc-149">移動 delta 是來源區塊開始與目標區塊開頭之間的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-149">The move delta is the number of bytes between the start of the source block and the start of the target block.</span></span> <span data-ttu-id="1f1bc-150">換句話說，如果 X 減 Y 的絕對值是 16 KB 的倍數，則從位移 X 開始 (磁片) 的區塊可以移至起始位移 Y。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-150">In other words, a block starting at offset X (on-disk) can be moved to a starting offset Y if the absolute value of X minus Y is an even multiple of 16 KB.</span></span> <span data-ttu-id="1f1bc-151">因此，假設有 4 KB 的叢集，從叢集3移至叢集27的動作將會優化，但從叢集18移至叢集24則不會。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-151">So, assuming 4-KB clusters, a move from cluster 3 to cluster 27 will be optimized, but a move from cluster 18 to cluster 24 will not.</span></span> <span data-ttu-id="1f1bc-152">請注意，mod (3，4) = 3 = mod (27，4) 。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-152">Note that mod(3,4) = 3 = mod(27,4).</span></span> <span data-ttu-id="1f1bc-153">因為 4 KB 的四個叢集都相當於 16 KB，所以選擇了 Mod 4。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-153">Mod 4 is chosen because four clusters at 4 KB each is equivalent to 16 KB.</span></span> <span data-ttu-id="1f1bc-154">因此，格式化為 16 KB 叢集大小的磁片區會導致所有的移動檔案都經過優化。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-154">Therefore, a volume formatted to a 16-KB cluster size will result in all move files being optimized.</span></span>

<span data-ttu-id="1f1bc-155">如需陰影複製的詳細資訊，請參閱 [磁碟區陰影複製服務](/windows/desktop/VSS/about-the-volume-shadow-copy-service)。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-155">For more information about shadow copies, see [Volume Shadow Copy Service](/windows/desktop/VSS/about-the-volume-shadow-copy-service).</span></span>

## <a name="files-streams-and-stream-types-supported-for-defragmentation"></a><span data-ttu-id="1f1bc-156">支援磁碟重組的檔案、資料流程和資料流程類型</span><span class="sxs-lookup"><span data-stu-id="1f1bc-156">Files, streams, and stream types supported for defragmentation</span></span>

<span data-ttu-id="1f1bc-157">雖然大部分的檔案都可以使用 [**FSCTL \_ 移動 \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) 檔案控制程式代碼來移動，但並非全部都可以移動。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-157">While most files can be moved using the [**FSCTL\_MOVE\_FILE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) control code, not all can be moved.</span></span> <span data-ttu-id="1f1bc-158">以下是檔案、資料流程和資料流程類型的清單 (也稱為「屬性類型代碼」（ **FSCTL \_ MOVE \_ FILE**）支援) 。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-158">Below is the list of files, streams, and stream types (also called attribute type codes) supported by **FSCTL\_MOVE\_FILE**.</span></span> <span data-ttu-id="1f1bc-159">**FSCTL \_ 移動 \_** 檔案不支援其他檔案、資料流程和資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-159">Other files, streams, and stream types are not supported by **FSCTL\_MOVE\_FILE**.</span></span>

<span data-ttu-id="1f1bc-160">支援任何檔案或目錄的資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-160">Stream types supported for any file or directory.</span></span>

-   <span data-ttu-id="1f1bc-161">：： $DATA</span><span class="sxs-lookup"><span data-stu-id="1f1bc-161">::$DATA</span></span>
-   <span data-ttu-id="1f1bc-162">：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-162">::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-163">：： $REPARSE \_ 點</span><span class="sxs-lookup"><span data-stu-id="1f1bc-163">::$REPARSE\_POINT</span></span>
-   <span data-ttu-id="1f1bc-164">：： $EA</span><span class="sxs-lookup"><span data-stu-id="1f1bc-164">::$EA</span></span>
-   <span data-ttu-id="1f1bc-165">：： $LOGGED \_ 公用程式 \_ 資料流程</span><span class="sxs-lookup"><span data-stu-id="1f1bc-165">::$LOGGED\_UTILITY\_STREAM</span></span>

<span data-ttu-id="1f1bc-166">\* \* Windows 7、Windows Server 2008 R2、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP： \* \*：： $EA 與：： $LOGGED \_ 公用程式 \_ 串流在 Windows 8 和 Windows Server 2012 之前都不受支援</span><span class="sxs-lookup"><span data-stu-id="1f1bc-166">\*\*Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  \*\*::$EA and ::$LOGGED\_UTILITY\_STREAM are not supported before Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="1f1bc-167">支援任何目錄的資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-167">Stream types supported for any directory.</span></span>

-   <span data-ttu-id="1f1bc-168">：： $BITMAP</span><span class="sxs-lookup"><span data-stu-id="1f1bc-168">::$BITMAP</span></span>
-   <span data-ttu-id="1f1bc-169">：： $INDEX \_ 配置</span><span class="sxs-lookup"><span data-stu-id="1f1bc-169">::$INDEX\_ALLOCATION</span></span>

<span data-ttu-id="1f1bc-170">以下是 [**FSCTL \_ MOVE \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) 檔案在 "*filename*：*streamname*： $*typename*" 格式中所支援的系統檔案、資料流程和資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="1f1bc-170">Following are the system file, stream, and stream types supported by [**FSCTL\_MOVE\_FILE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) in "*filename*:*streamname*:$*typename*" format.</span></span>

-   <span data-ttu-id="1f1bc-171">$MFT：： $DATA</span><span class="sxs-lookup"><span data-stu-id="1f1bc-171">$MFT::$DATA</span></span>
-   <span data-ttu-id="1f1bc-172">$MFT：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-172">$MFT::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-173">$MFT：： $BITMAP</span><span class="sxs-lookup"><span data-stu-id="1f1bc-173">$MFT::$BITMAP</span></span>
-   <span data-ttu-id="1f1bc-174">$AttrDef：： $DATA</span><span class="sxs-lookup"><span data-stu-id="1f1bc-174">$AttrDef::$DATA</span></span>
-   <span data-ttu-id="1f1bc-175">$AttrDef：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-175">$AttrDef::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-176">$Secure： $SDS： $DATA</span><span class="sxs-lookup"><span data-stu-id="1f1bc-176">$Secure:$SDS:$DATA</span></span>
-   <span data-ttu-id="1f1bc-177">$Secure：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-177">$Secure::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-178">$Secure： $SDH： $INDEX \_ 配置</span><span class="sxs-lookup"><span data-stu-id="1f1bc-178">$Secure:$SDH:$INDEX\_ALLOCATION</span></span>
-   <span data-ttu-id="1f1bc-179">$Secure： $SDH： $BITMAP</span><span class="sxs-lookup"><span data-stu-id="1f1bc-179">$Secure:$SDH:$BITMAP</span></span>
-   <span data-ttu-id="1f1bc-180">$Secure： $SII： $INDEX \_ 配置</span><span class="sxs-lookup"><span data-stu-id="1f1bc-180">$Secure:$SII:$INDEX\_ALLOCATION</span></span>
-   <span data-ttu-id="1f1bc-181">$Secure： $SII： $BITMAP</span><span class="sxs-lookup"><span data-stu-id="1f1bc-181">$Secure:$SII:$BITMAP</span></span>
-   <span data-ttu-id="1f1bc-182">$UpCase：： $DATA</span><span class="sxs-lookup"><span data-stu-id="1f1bc-182">$UpCase::$DATA</span></span>
-   <span data-ttu-id="1f1bc-183">$UpCase：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-183">$UpCase::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-184">$Extend： $I 30： $INDEX \_ 配置</span><span class="sxs-lookup"><span data-stu-id="1f1bc-184">$Extend:$I30:$INDEX\_ALLOCATION</span></span>
-   <span data-ttu-id="1f1bc-185">$Extend：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-185">$Extend::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-186">$Extend： $I 30： $BITMAP</span><span class="sxs-lookup"><span data-stu-id="1f1bc-186">$Extend:$I30:$BITMAP</span></span>
-   <span data-ttu-id="1f1bc-187">$Extend \\ $UsnJrnl： $J： $DATA</span><span class="sxs-lookup"><span data-stu-id="1f1bc-187">$Extend\\$UsnJrnl:$J:$DATA</span></span>
-   <span data-ttu-id="1f1bc-188">$Extend \\ $UsnJrnl：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-188">$Extend\\$UsnJrnl::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-189">$Extend \\ $UsnJrnl： $Max： $DATA</span><span class="sxs-lookup"><span data-stu-id="1f1bc-189">$Extend\\$UsnJrnl:$Max:$DATA</span></span>
-   <span data-ttu-id="1f1bc-190">$Extend \\ $Quota： $Q： $INDEX \_ 配置</span><span class="sxs-lookup"><span data-stu-id="1f1bc-190">$Extend\\$Quota:$Q:$INDEX\_ALLOCATION</span></span>
-   <span data-ttu-id="1f1bc-191">$Extend \\ $Quota：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-191">$Extend\\$Quota::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-192">$Extend \\ $Quota： $Q： $BITMAP</span><span class="sxs-lookup"><span data-stu-id="1f1bc-192">$Extend\\$Quota:$Q:$BITMAP</span></span>
-   <span data-ttu-id="1f1bc-193">$Extend \\ $Quota： $O： $INDEX \_ 配置</span><span class="sxs-lookup"><span data-stu-id="1f1bc-193">$Extend\\$Quota:$O:$INDEX\_ALLOCATION</span></span>
-   <span data-ttu-id="1f1bc-194">$Extend \\ $Quota： $O： $BITMAP</span><span class="sxs-lookup"><span data-stu-id="1f1bc-194">$Extend\\$Quota:$O:$BITMAP</span></span>
-   <span data-ttu-id="1f1bc-195">$Extend \\ $ObjId： $O： $INDEX \_ 配置</span><span class="sxs-lookup"><span data-stu-id="1f1bc-195">$Extend\\$ObjId:$O:$INDEX\_ALLOCATION</span></span>
-   <span data-ttu-id="1f1bc-196">$Extend \\ $ObjId：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-196">$Extend\\$ObjId::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-197">$Extend \\ $ObjId： $O： $BITMAP</span><span class="sxs-lookup"><span data-stu-id="1f1bc-197">$Extend\\$ObjId:$O:$BITMAP</span></span>
-   <span data-ttu-id="1f1bc-198">$Extend \\ $Reparse： $R： $INDEX \_ 配置</span><span class="sxs-lookup"><span data-stu-id="1f1bc-198">$Extend\\$Reparse:$R:$INDEX\_ALLOCATION</span></span>
-   <span data-ttu-id="1f1bc-199">$Extend \\ $Reparse：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-199">$Extend\\$Reparse::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-200">$Extend \\ $Reparse： $R： $BITMAP</span><span class="sxs-lookup"><span data-stu-id="1f1bc-200">$Extend\\$Reparse:$R:$BITMAP</span></span>
-   <span data-ttu-id="1f1bc-201">$Extend \\ $RmMetadata： $I 30： $INDEX \_ 配置</span><span class="sxs-lookup"><span data-stu-id="1f1bc-201">$Extend\\$RmMetadata:$I30:$INDEX\_ALLOCATION</span></span>
-   <span data-ttu-id="1f1bc-202">$Extend \\ $RmMetadata： $I 30： $BITMAP</span><span class="sxs-lookup"><span data-stu-id="1f1bc-202">$Extend\\$RmMetadata:$I30:$BITMAP</span></span>
-   <span data-ttu-id="1f1bc-203">$Extend \\ $RmMetadata：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-203">$Extend\\$RmMetadata::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-204">$Extend \\ $RmMetadata \\ $Repair：： $DATA</span><span class="sxs-lookup"><span data-stu-id="1f1bc-204">$Extend\\$RmMetadata\\$Repair::$DATA</span></span>
-   <span data-ttu-id="1f1bc-205">$Extend \\ $RmMetadata \\ $Repair：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-205">$Extend\\$RmMetadata\\$Repair::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-206">$Extend \\ $RmMetadata \\ $Repair： $Config： $DATA</span><span class="sxs-lookup"><span data-stu-id="1f1bc-206">$Extend\\$RmMetadata\\$Repair:$Config:$DATA</span></span>
-   <span data-ttu-id="1f1bc-207">$Extend \\ $RmMetadata \\ $Txf： $I 30： $INDEX \_ 配置</span><span class="sxs-lookup"><span data-stu-id="1f1bc-207">$Extend\\$RmMetadata\\$Txf:$I30:$INDEX\_ALLOCATION</span></span>
-   <span data-ttu-id="1f1bc-208">$Extend \\ $RmMetadata \\ $Txf：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-208">$Extend\\$RmMetadata\\$Txf::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-209">$Extend \\ $RmMetadata \\ $Txf： $I 30： $BITMAP</span><span class="sxs-lookup"><span data-stu-id="1f1bc-209">$Extend\\$RmMetadata\\$Txf:$I30:$BITMAP</span></span>
-   <span data-ttu-id="1f1bc-210">$Extend \\ $RmMetadata \\ $Txf： $TXF \_ 資料： $LOGGED \_ 公用程式 \_ 資料流程</span><span class="sxs-lookup"><span data-stu-id="1f1bc-210">$Extend\\$RmMetadata\\$Txf:$TXF\_DATA:$LOGGED\_UTILITY\_STREAM</span></span>
-   <span data-ttu-id="1f1bc-211">$Extend \\ $RmMetadata \\ $TxfLog： $I 30： $INDEX \_ 配置</span><span class="sxs-lookup"><span data-stu-id="1f1bc-211">$Extend\\$RmMetadata\\$TxfLog:$I30:$INDEX\_ALLOCATION</span></span>
-   <span data-ttu-id="1f1bc-212">$Extend \\ $RmMetadata \\ $TxfLog：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-212">$Extend\\$RmMetadata\\$TxfLog::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-213">$Extend \\ $RmMetadata \\ $TxfLog： $I 30： $BITMAP</span><span class="sxs-lookup"><span data-stu-id="1f1bc-213">$Extend\\$RmMetadata\\$TxfLog:$I30:$BITMAP</span></span>
-   <span data-ttu-id="1f1bc-214">$Extend \\ $RmMetadata \\ $TxfLog \\ $Tops：： $DATA</span><span class="sxs-lookup"><span data-stu-id="1f1bc-214">$Extend\\$RmMetadata\\$TxfLog\\$Tops::$DATA</span></span>
-   <span data-ttu-id="1f1bc-215">$Extend \\ $RmMetadata \\ $TxfLog \\ $Tops：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-215">$Extend\\$RmMetadata\\$TxfLog\\$Tops::$ATTRIBUTE\_LIST</span></span>
-   <span data-ttu-id="1f1bc-216">$Extend \\ $RmMetadata \\ $TxfLog \\ $Tops： $T： $DATA</span><span class="sxs-lookup"><span data-stu-id="1f1bc-216">$Extend\\$RmMetadata\\$TxfLog\\$Tops:$T:$DATA</span></span>
-   <span data-ttu-id="1f1bc-217">$Extend \\ $RmMetadata \\ $TxfLog \\ $TxfLog. blf：： $DATA</span><span class="sxs-lookup"><span data-stu-id="1f1bc-217">$Extend\\$RmMetadata\\$TxfLog\\$TxfLog.blf::$DATA</span></span>
-   <span data-ttu-id="1f1bc-218">$Extend \\ $RmMetadata \\ $TxfLog \\ $TxfLog. blf：： $ATTRIBUTE \_ 清單</span><span class="sxs-lookup"><span data-stu-id="1f1bc-218">$Extend\\$RmMetadata\\$TxfLog\\$TxfLog.blf::$ATTRIBUTE\_LIST</span></span>

 

 
