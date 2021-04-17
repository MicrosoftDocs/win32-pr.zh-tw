---
description: 區塊複製作業會指示檔案系統代表應用程式複製某範圍的檔案位元組。
ms.assetid: E18E8D79-3985-40B8-A4C5-A73A21E5C527
title: 封鎖複製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33aa1c1eee693b6ed4b502aedc6da6176ece3e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514000"
---
# <a name="block-cloning"></a><span data-ttu-id="f6daf-103">封鎖複製</span><span class="sxs-lookup"><span data-stu-id="f6daf-103">Block Cloning</span></span>

<span data-ttu-id="f6daf-104">*區塊複製* 作業會指示檔案系統代表應用程式複製某範圍的檔案位元組。</span><span class="sxs-lookup"><span data-stu-id="f6daf-104">A *block clone* operation instructs the file system to copy a range of file bytes on behalf of an application.</span></span> <span data-ttu-id="f6daf-105">目的地檔案可能與來源檔案相同或不同。</span><span class="sxs-lookup"><span data-stu-id="f6daf-105">The destination file may be the same as, or different from, the source file.</span></span>

<span data-ttu-id="f6daf-106">檔案系統會管理叢集 [和延伸區](clusters-and-extents.md)的對應，而且可以藉由將虛擬叢集編號 (VCN) 變更為邏輯叢集號碼， (LCN) 對應作為低成本的中繼資料作業，而不是讀取和寫入基礎檔案資料，來執行複製。</span><span class="sxs-lookup"><span data-stu-id="f6daf-106">A file system manages the mappings of [Clusters and Extents](clusters-and-extents.md), and may be able to perform the copy by altering the virtual cluster number (VCN) to logical cluster number (LCN) mappings as a low-cost metadata operation, rather than reading and writing the underlying file data.</span></span> <span data-ttu-id="f6daf-107">這可讓複本以較快的速度完成，並產生較少的 i/o 給基礎儲存體。</span><span class="sxs-lookup"><span data-stu-id="f6daf-107">This allows the copy to complete faster and generates less I/O to the underlying storage.</span></span> <span data-ttu-id="f6daf-108">此外，多個檔案現在可能會在區塊複製後共用邏輯叢集，而不會在磁片上多次儲存相同的叢集來節省容量。</span><span class="sxs-lookup"><span data-stu-id="f6daf-108">Moreover, multiple files may now share logical clusters after the block clone, saving capacity by not storing identical clusters multiple times on disk.</span></span>

<span data-ttu-id="f6daf-109">區塊複製作業不會中斷檔案之間提供的隔離。</span><span class="sxs-lookup"><span data-stu-id="f6daf-109">A block clone operation does not break the isolation provided between files.</span></span> <span data-ttu-id="f6daf-110">在區塊複製完成之後，寫入來源檔案的作業不會出現在目的地中，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="f6daf-110">After a block clone completes, writes to the source file do not appear in the destination, or vice versa.</span></span>

<span data-ttu-id="f6daf-111">區塊複製僅適用于從 Windows Server 2016 開始的 [ReFS 檔案系統](/windows/desktop/w8cookbook/resilient-file-system--refs-) 類型。</span><span class="sxs-lookup"><span data-stu-id="f6daf-111">Block cloning is available only on the [ReFS file system](/windows/desktop/w8cookbook/resilient-file-system--refs-) type beginning with Windows Server 2016.</span></span>

## <a name="block-cloning-on-refs"></a><span data-ttu-id="f6daf-112">在 ReFS 上進行區塊複製</span><span class="sxs-lookup"><span data-stu-id="f6daf-112">Block Cloning on ReFS</span></span>

<span data-ttu-id="f6daf-113">Windows Server 2016 上的 ReFS 會藉由將邏輯叢集 (也就是磁片區上的實體位置) 從來源區域到目的地區域，來實行區塊複製。</span><span class="sxs-lookup"><span data-stu-id="f6daf-113">ReFS on Windows Server 2016 implements block cloning by remapping logical clusters (that is, physical locations on a volume) from the source region to the destination region.</span></span> <span data-ttu-id="f6daf-114">然後，它會使用以配置為依據的寫入機制，以確保這些區域之間的隔離。</span><span class="sxs-lookup"><span data-stu-id="f6daf-114">It then uses an allocate-on-write mechanism to ensure isolation between those regions.</span></span> <span data-ttu-id="f6daf-115">來源和目的地區域可以位於相同或不同的檔案中。</span><span class="sxs-lookup"><span data-stu-id="f6daf-115">The source and destination regions may be in the same, or different, files.</span></span>

<span data-ttu-id="f6daf-116">此執行需要將開始和結束檔案位移對齊叢集界限。</span><span class="sxs-lookup"><span data-stu-id="f6daf-116">This implementation requires that the starting and ending file offsets be aligned to cluster boundaries.</span></span> <span data-ttu-id="f6daf-117">在 Windows Server 2016 的 ReFS 中，叢集預設的大小為 4 KB，但可以選擇性地設定為64KB。</span><span class="sxs-lookup"><span data-stu-id="f6daf-117">In ReFS on Windows Server 2016, clusters are 4KB in size by default, but can optionally be set to 64KB.</span></span> <span data-ttu-id="f6daf-118">叢集大小是以格式時間設定的全磁片區參數。</span><span class="sxs-lookup"><span data-stu-id="f6daf-118">The cluster size is a volume-wide parameter set at format time.</span></span>

## <a name="restrictions-and-remarks"></a><span data-ttu-id="f6daf-119">限制和備註</span><span class="sxs-lookup"><span data-stu-id="f6daf-119">Restrictions and Remarks</span></span>

-   <span data-ttu-id="f6daf-120">來源和目的地區域必須在叢集界限的開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="f6daf-120">The source and destination regions must begin and end at a cluster boundary.</span></span>
-   <span data-ttu-id="f6daf-121">複製的區域長度必須小於 4GB。</span><span class="sxs-lookup"><span data-stu-id="f6daf-121">The cloned region must be less than 4GB in length.</span></span>
-   <span data-ttu-id="f6daf-122">目的地區域不得延伸超過檔案結尾。</span><span class="sxs-lookup"><span data-stu-id="f6daf-122">The destination region must not extend past the end of file.</span></span> <span data-ttu-id="f6daf-123">如果應用程式想要使用複製的資料來擴充目的地，它必須先呼叫 [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)。</span><span class="sxs-lookup"><span data-stu-id="f6daf-123">If the application wishes to extend the destination with cloned data, it must first call [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span></span>
-   <span data-ttu-id="f6daf-124">若來源與目的地區域位於相同檔案，其不得重疊。</span><span class="sxs-lookup"><span data-stu-id="f6daf-124">If the source and destination regions are in the same file, they must not overlap.</span></span> <span data-ttu-id="f6daf-125"> (應用程式可以將區塊複製作業分割成多個不再重迭的區塊複製，以繼續進行。 ) </span><span class="sxs-lookup"><span data-stu-id="f6daf-125">(The application may able to proceed by splitting up the block clone operation into multiple block clones that no longer overlap.)</span></span>
-   <span data-ttu-id="f6daf-126">來源與目的檔案必須位於相同的 ReFS 磁碟區。</span><span class="sxs-lookup"><span data-stu-id="f6daf-126">The source and destination files must be on the same ReFS volume.</span></span>
-   <span data-ttu-id="f6daf-127">來源和目的地檔案必須有相同的 [**完整性資料流程**](file-attribute-constants.md) 設定 (也就是說，必須在這兩個檔案中啟用完整性資料流程，或是在兩個檔案) 中都停用。</span><span class="sxs-lookup"><span data-stu-id="f6daf-127">The source and destination files must have the same [**Integrity Streams**](file-attribute-constants.md) setting (that is, Integrity Streams must be enabled in both files, or disabled in both files).</span></span>
-   <span data-ttu-id="f6daf-128">若來源檔案為疏鬆，目的檔案也必須為疏鬆。</span><span class="sxs-lookup"><span data-stu-id="f6daf-128">If the source file is sparse, the destination file must also be sparse.</span></span>
-   <span data-ttu-id="f6daf-129">區塊複製作業會中斷共用的隨機鎖定 (也稱為 [層級 2](types-of-opportunistic-locks.md) 的隨機鎖定) 。</span><span class="sxs-lookup"><span data-stu-id="f6daf-129">The block clone operation will break Shared Opportunistic Locks (also known as [Level 2 Opportunistic Locks](types-of-opportunistic-locks.md)).</span></span>
-   <span data-ttu-id="f6daf-130">ReFS 磁片區必須已格式化為 Windows Server 2016，如果 Windows 容錯移轉叢集正在使用中，則叢集功能等級必須是 Windows Server 2016 或更新版本（格式時間）。</span><span class="sxs-lookup"><span data-stu-id="f6daf-130">The ReFS volume must have been formatted with Windows Server 2016, and if Windows Failover Clustering is in use, the Clustering Functional Level must have been Windows Server 2016 or later at format time.</span></span>

## <a name="example"></a><span data-ttu-id="f6daf-131">範例</span><span class="sxs-lookup"><span data-stu-id="f6daf-131">Example</span></span>

<span data-ttu-id="f6daf-132">假設我們有兩個檔案 X 和 Y，其中每個檔案都是由三個不同的區域所組成。</span><span class="sxs-lookup"><span data-stu-id="f6daf-132">Suppose we have two files, X and Y, where each file is composed of 3 distinct regions.</span></span> <span data-ttu-id="f6daf-133">每個檔案區域都儲存在磁片區的不同區域。</span><span class="sxs-lookup"><span data-stu-id="f6daf-133">Each file region is stored on a distinct region of the volume.</span></span> <span data-ttu-id="f6daf-134">檔案系統會儲存每一個檔案區域中所參考的每個磁片區區域的知識：</span><span class="sxs-lookup"><span data-stu-id="f6daf-134">The file system stores the knowledge that each of those volume regions is referenced in one file region:</span></span>

![複製前](images/before-clone.png)

<span data-ttu-id="f6daf-136">現在假設應用程式會從檔案 X （在檔案區域 A 和 B）對檔案 Y 發出區塊複製作業，該作業是在 E 目前為的位移處的檔案 Y。</span><span class="sxs-lookup"><span data-stu-id="f6daf-136">Now suppose an application issues a block clone operation from File X, over file regions A and B, to File Y at the offset where E currently is.</span></span> <span data-ttu-id="f6daf-137">將會產生下列檔案系統狀態：</span><span class="sxs-lookup"><span data-stu-id="f6daf-137">The following file system state would result:</span></span>

![複製後](images/after-clone.png)

<span data-ttu-id="f6daf-139">區域 A 和 B 中的資料實際上是從檔案 X 複製到檔案 Y （藉由將 VCN 變更為 ReFS 磁片區內的 LCN 對應）。</span><span class="sxs-lookup"><span data-stu-id="f6daf-139">The data in regions A and B were effectively duplicated from File X to File Y by altering the VCN to LCN mappings within the ReFS volume.</span></span> <span data-ttu-id="f6daf-140">磁片區支援區域 A 和 B 未讀取，也不是支援在作業期間覆寫舊區域 E 和 F 的磁片區。</span><span class="sxs-lookup"><span data-stu-id="f6daf-140">The disk extents backing regions A and B were not read, nor were the disk extents backing the old regions E and F overwritten during the operation.</span></span>

<span data-ttu-id="f6daf-141">檔案 X 和 Y 現在會在磁片上共用邏輯群集。</span><span class="sxs-lookup"><span data-stu-id="f6daf-141">Files X and Y now share logical clusters on disk.</span></span> <span data-ttu-id="f6daf-142">這會反映在資料表所顯示的參考計數中。</span><span class="sxs-lookup"><span data-stu-id="f6daf-142">This is reflected in the reference counts shown in the table.</span></span> <span data-ttu-id="f6daf-143">共用會導致磁片區容量耗用量較低，因為基礎磁片區上的區域 A 和 B 已複製。</span><span class="sxs-lookup"><span data-stu-id="f6daf-143">The sharing results in lower volume capacity consumption than if regions A and B were duplicated on the underlying volume.</span></span>

<span data-ttu-id="f6daf-144">現在，假設應用程式會覆寫檔案 X 中的區域 A。 ReFS 會產生重複的複本，現在我們將會呼叫 g.，然後將 G 對應到檔案 X，並套用修改。</span><span class="sxs-lookup"><span data-stu-id="f6daf-144">Now, suppose the application overwrites region A in File X. ReFS makes a duplicate copy of A, which we’ll now call G. ReFS then maps G into File X, and applies the modification.</span></span> <span data-ttu-id="f6daf-145">如此可確保維持檔案間的隔離。</span><span class="sxs-lookup"><span data-stu-id="f6daf-145">This ensures that isolation between the files is preserved.</span></span> <span data-ttu-id="f6daf-146">參考計數會適當地更新：</span><span class="sxs-lookup"><span data-stu-id="f6daf-146">Reference counts are updated appropriately:</span></span>

![修改寫入之後](images/after-modifying-write.png)

<span data-ttu-id="f6daf-148">修改寫入之後，區域 B 仍會在磁片上共用。</span><span class="sxs-lookup"><span data-stu-id="f6daf-148">After the modifying write, region B is still shared on disk.</span></span> <span data-ttu-id="f6daf-149">注意，若區域 A 大於叢集，便僅會複製修改的叢集，且剩餘的部分會維持為共用。</span><span class="sxs-lookup"><span data-stu-id="f6daf-149">Note that if region A were larger than a cluster, only the modified cluster would have been duplicated, and the remaining portion would have remained shared.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6daf-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="f6daf-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6daf-151">**重複的 \_ 延伸區 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="f6daf-151">**DUPLICATE\_EXTENTS\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-duplicate_extents_data)
</dt> <dt>

[<span data-ttu-id="f6daf-152">**\_將重複 \_ 的範圍 FSCTL \_ 至 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="f6daf-152">**FSCTL\_DUPLICATE\_EXTENTS\_TO\_FILE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)
</dt> </dl>

 

 
