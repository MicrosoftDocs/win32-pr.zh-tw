---
title: 新的 API 可讓應用程式將「修剪和取消對應」提示傳送至存放裝置媒體
description: 新的 API 可讓應用程式傳送 \ 0034;修剪和取消對應 \ 0034;存放裝置媒體的提示
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e043c1188bda790b4ed151e8a79e1f7b4c6f0f9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "106965257"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a><span data-ttu-id="61348-103">新的 API 可讓應用程式將「修剪和取消對應」提示傳送至存放裝置媒體</span><span class="sxs-lookup"><span data-stu-id="61348-103">New API allows apps to send "TRIM and Unmap" hints to storage media</span></span>

## <a name="platforms"></a><span data-ttu-id="61348-104">平台</span><span class="sxs-lookup"><span data-stu-id="61348-104">Platforms</span></span>

<span data-ttu-id="61348-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="61348-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="61348-106">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61348-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="61348-107">Description</span><span class="sxs-lookup"><span data-stu-id="61348-107">Description</span></span>

<span data-ttu-id="61348-108">TRIM 提示會通知磁片磁碟機，應用程式不再需要先前配置的某些磁區，且可以清除。</span><span class="sxs-lookup"><span data-stu-id="61348-108">TRIM hints notify the drive that certain sectors that previously were allocated are no longer needed by the app and can be purged.</span></span> <span data-ttu-id="61348-109">當應用程式透過檔案進行大量配置，然後自行管理檔案的配置 (例如虛擬硬碟檔案) 時，通常會使用這種方式。</span><span class="sxs-lookup"><span data-stu-id="61348-109">This is typically used when an app makes large space allocations via a file and then self-manages the allocations to the file (for example, Virtual Hard Disk files).</span></span>

<span data-ttu-id="61348-110">**什麼是 TRIM？**</span><span class="sxs-lookup"><span data-stu-id="61348-110">**What is TRIM?**</span></span>

<span data-ttu-id="61348-111">固態硬碟 (Ssd) 通常是以 flash 記憶體為基礎的區塊清除裝置;這表示當資料寫入 SSD 時，不能就地寫入，必須在其他地方寫入，直到封鎖可進行垃圾收集為止。</span><span class="sxs-lookup"><span data-stu-id="61348-111">Solid state drives (SSDs) are typically flash memory based block-erased devices; this means that when data is written to the SSD, it cannot be over-written in place and must be written elsewhere until the block can be garbage collected.</span></span> <span data-ttu-id="61348-112">由於 SSD 沒有任何內部機制可判斷特定區塊已移除，而且需要其他區塊。</span><span class="sxs-lookup"><span data-stu-id="61348-112">Since the SSD has no internal mechanism for determining that certain blocks are removed and others are needed.</span></span> <span data-ttu-id="61348-113">SSD 可將磁區標示為「已變更」的唯一時機是在過度寫入時。</span><span class="sxs-lookup"><span data-stu-id="61348-113">The only time the SSD can mark a sector ‘dirty’ is when it is over-written.</span></span> <span data-ttu-id="61348-114">在其他情況下（例如，當檔案被刪除時）會保留這些磁區，因為刪除作業會以主要檔案資料表的形式 () 只變更，而不是對檔案的所有磁區進行作業。</span><span class="sxs-lookup"><span data-stu-id="61348-114">In other cases, such as when a file is deleted, the SSD retains these sectors because the deletion is performed as a master file table (MFT) change only, and not as an operation to all the sectors of the file.</span></span> <span data-ttu-id="61348-115">在 Windows 7 中，我們引進了一種標準方式來與 Ssd 通訊，而不需要任何其他的磁區。</span><span class="sxs-lookup"><span data-stu-id="61348-115">In Windows 7, we introduced a standard way of communicating with SSDs about sectors that are not needed any more.</span></span> <span data-ttu-id="61348-116">此命令會在 [T13 規格](https://www.t13.org/Standards/Default.aspx?DocumentType=3) 中定義為 TRIM 命令;NTFS 會傳送一些一般內嵌作業（例如 "deletefile"）的 TRIM 命令。</span><span class="sxs-lookup"><span data-stu-id="61348-116">This command is defined in the [T13 specification](https://www.t13.org/Standards/Default.aspx?DocumentType=3) as the TRIM command; NTFS sends the TRIM command for some normal inline operations such as “deletefile.”</span></span>

<span data-ttu-id="61348-117">**儲存體世界中的其他修剪用途**</span><span class="sxs-lookup"><span data-stu-id="61348-117">**Other uses of TRIM in the storage world**</span></span>

<span data-ttu-id="61348-118">如同 Ssd，存放區域網路 (San) 和新的 Windows 8 功能軟體空間實作為在精簡布建的環境中管理其空間的方式。</span><span class="sxs-lookup"><span data-stu-id="61348-118">Like SSDs, storage area networks (SANs) and the new Windows 8 feature Software Spaces implementations consume TRIM command hints to manage their spaces in thinly provisioned environments.</span></span> <span data-ttu-id="61348-119">San 和軟體空間會以大於磁區或叢集的大小來配置儲存體的區域， (從1MB 到 1GB) 的任何位置。</span><span class="sxs-lookup"><span data-stu-id="61348-119">SANs and Software Spaces allocate regions of storage in sizes that are greater than sectors or clusters (anywhere from 1MB to 1GB).</span></span> <span data-ttu-id="61348-120">當它們收到配置大小的 TRIM 提示 (或大於配置大小) 時，SAN/SSD 可以取消配置區域以釋出其他檔案的空間。</span><span class="sxs-lookup"><span data-stu-id="61348-120">When they receive TRIM hints for its allocation size (or greater than the allocation size), the SAN/SSD can de-allocate a region to free up the space for other files.</span></span> <span data-ttu-id="61348-121">它們通常會將所有的 TRIM 提示傳遞給基礎媒體 (SSD 或 HDD) ，讓它們可以適當地使用釋放的空間。</span><span class="sxs-lookup"><span data-stu-id="61348-121">They typically pass through all TRIM hints to the underlying media (SSD or HDD) so that they can consume the freed up space as appropriate.</span></span> <span data-ttu-id="61348-122">它們通常不會將資料移至取消配置區域，也不會在區域是空的) 時，追蹤取消配置區域 (的修剪區域。</span><span class="sxs-lookup"><span data-stu-id="61348-122">They do not typically move data around to de-allocate regions, nor do they keep track of TRIM areas to de-allocated regions (when the region is empty).</span></span>

<span data-ttu-id="61348-123">精簡布建的 San 會使用傳遞給它們的修剪提示，以協助降低整體實體儲存體的使用量，進而降低成本。</span><span class="sxs-lookup"><span data-stu-id="61348-123">Thinly provisioned SANs use the TRIM hints that are passed to them to help reduce the overall physical storage footprint, hence reducing cost.</span></span> <span data-ttu-id="61348-124">[T10 SCSI 規格](https://www.t10.org)會定義「取消對應」命令 (類似于 TRIM 命令) ;此命令適用于所有種類的儲存體，包括 Hdd、Ssd 和其他類型。</span><span class="sxs-lookup"><span data-stu-id="61348-124">The [T10 SCSI specification](https://www.t10.org) defines the ‘Unmap’ command (similar to the TRIM command); here the command is applicable to all kinds of storage including HDDs, SSDs, and others.</span></span> <span data-ttu-id="61348-125">取消對應命令可協助移除 SAN 配置中的實體區塊。</span><span class="sxs-lookup"><span data-stu-id="61348-125">The UnMap command helps to remove physical blocks from the SAN’s allocation.</span></span>

## <a name="how-to-use-the-new-api"></a><span data-ttu-id="61348-126">如何使用新的 API</span><span class="sxs-lookup"><span data-stu-id="61348-126">How to use the new API</span></span>


```
#define FSCTL_FILE_LEVEL_TRIM CTL_CODE(FILE_DEVICE_FILE_SYSTEM, 130, METHOD_BUFFERED, FILE_WRITE_DATA)

Where 
typedef struct _EXTENT_PAIR {
    ULONGLONG Offset;
    ULONGLONG Length;
} EXTENT_PAIR, *PEXTENT_PAIR;

typedef struct _FILE_LEVEL_TRIM {
    //
    // A count of how many Offset:Length pairs are given
    //
    DWORD PairCount;
    //
    // All the pairs.
    //
    EXTENT_PAIR Pairs[1];
} FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM;
```



<span data-ttu-id="61348-127">如果可能或非同步 (非緩衝) 至裝置 IOCTL DSM 命令修剪，則會透過緩衝區傳遞檔案修剪。</span><span class="sxs-lookup"><span data-stu-id="61348-127">File TRIM is passed via the buffer if possible or asynchronously (non-buffered) to the Device IOCTL DSM command TRIM.</span></span> <span data-ttu-id="61348-128">這會對應至適用于 ATA 裝置的 TRIM 命令和 SCSI 裝置的取消對應命令。</span><span class="sxs-lookup"><span data-stu-id="61348-128">This is mapped to the TRIM command for ATA devices and UnMap command for SCSI devices.</span></span> <span data-ttu-id="61348-129">檔案修剪程式碼會逐一傳送區域，如同上方的範圍所指定。</span><span class="sxs-lookup"><span data-stu-id="61348-129">The file TRIM code sends the regions one-by-one as specified by the extents above.</span></span>

<span data-ttu-id="61348-130">檔案修剪不會等待裝置的傳回，因為 TRIM 和取消對應命令會定義為基礎儲存媒體的提示，而且不需要傳回碼。</span><span class="sxs-lookup"><span data-stu-id="61348-130">File TRIM does not wait for returns from the device, because the TRIM and Unmap commands are defined as hints to the underlying storage media and return codes are not expected.</span></span>

<span data-ttu-id="61348-131">**端對端工作流程：**</span><span class="sxs-lookup"><span data-stu-id="61348-131">**End-to-end workflow:**</span></span>

1.  <span data-ttu-id="61348-132">呼叫檔案修剪</span><span class="sxs-lookup"><span data-stu-id="61348-132">Call File Trim</span></span>
    1.  <span data-ttu-id="61348-133">檔案修剪會檢查輸入的錯誤</span><span class="sxs-lookup"><span data-stu-id="61348-133">File TRIM examines inputs for errors</span></span>
    2.  <span data-ttu-id="61348-134">檔案修剪將範圍細分為 LCN 區域</span><span class="sxs-lookup"><span data-stu-id="61348-134">File TRIM breaks up the extents into LCN regions</span></span>
    3.  <span data-ttu-id="61348-135">檔案修剪會向上和向下調整傳遞給 TRIM 的錯誤對齊區域</span><span class="sxs-lookup"><span data-stu-id="61348-135">File TRIM rounds up and down for mis-aligned regions that are passed into TRIM</span></span>
    4.  <span data-ttu-id="61348-136">檔案修剪：清除快取中與修剪區域相關的專案</span><span class="sxs-lookup"><span data-stu-id="61348-136">File TRIM purges entries in the cache that relate to the TRIM areas</span></span>
    5.  <span data-ttu-id="61348-137">檔案修剪會將 IOCTL \_ DSM (TRIM) 每個區域傳遞</span><span class="sxs-lookup"><span data-stu-id="61348-137">File TRIM passes IOCTL\_DSM (Trim) per region</span></span>
2.  <span data-ttu-id="61348-138">檔案修剪傳回或錯誤</span><span class="sxs-lookup"><span data-stu-id="61348-138">File TRIM returns or errors</span></span>
    1.  <span data-ttu-id="61348-139">針對輸入有效性進行錯誤檢查</span><span class="sxs-lookup"><span data-stu-id="61348-139">Error checking is done on input validity</span></span>
    2.  <span data-ttu-id="61348-140">如果只有部分範圍有效，則會傳回完整 API 呼叫的一個錯誤</span><span class="sxs-lookup"><span data-stu-id="61348-140">If only some of the extents are valid, one error is returned for the complete API call</span></span>

<span data-ttu-id="61348-141">**使用案例**</span><span class="sxs-lookup"><span data-stu-id="61348-141">**Use cases**</span></span>

<span data-ttu-id="61348-142">**取用者虛擬硬碟 (VHD) 掛接在 SSD 上：**</span><span class="sxs-lookup"><span data-stu-id="61348-142">**Consumer virtual hard disk (VHD) mounted on an SSD:**</span></span>

<span data-ttu-id="61348-143">VHD 一開始是在「清理」未使用的媒體上掛接。</span><span class="sxs-lookup"><span data-stu-id="61348-143">The VHD is initially mounted on ‘clean’ unused media.</span></span> <span data-ttu-id="61348-144">使用 VHD 時，VHD 會取用檔案的部分儲存媒體等等。當它刪除儲存體媒體中的檔案時，不會從 SSD 移除這些檔案，因為完整的 VHD 會儲存為 SSD 上的一個檔案。</span><span class="sxs-lookup"><span data-stu-id="61348-144">As the VHD is used, the VHD consumes parts of the storage media for files, etc. When it deletes files in the storage media, these files are not removed from the SSD since the complete VHD is stored as one file on the SSD.</span></span> <span data-ttu-id="61348-145">Hyper-v 環境會針對在 VHD 環境中刪除檔案時刪除的所有區域呼叫檔案修剪。</span><span class="sxs-lookup"><span data-stu-id="61348-145">The Hyper-V environment calls File TRIM for all regions that are deleted when delete-file occurs in the VHD environment.</span></span> <span data-ttu-id="61348-146">檔案 \_ 修剪會轉譯成 ssd，讓 ssd 效能可以優化。</span><span class="sxs-lookup"><span data-stu-id="61348-146">The File\_TRIMs are translated to the SSD so that the SSD performance can be optimized.</span></span>

<span data-ttu-id="61348-147">**在精簡布建的 SAN 上掛接的取用者 VHD：**</span><span class="sxs-lookup"><span data-stu-id="61348-147">**Consumer VHD mounted on a thinly provisioned SAN:**</span></span>

<span data-ttu-id="61348-148">VHD 一開始會掛接在精簡布建環境的最小值板上。</span><span class="sxs-lookup"><span data-stu-id="61348-148">The VHD is initially mounted on one minimum slab of a thinly provisioned environment.</span></span> <span data-ttu-id="61348-149">當檔案儲存在 VHD 時，VHD 的儲存空間使用量會以 slab 的倍數成長。</span><span class="sxs-lookup"><span data-stu-id="61348-149">As files are stored in the VHD, the storage footprint of the VHD grows in multiples of slabs.</span></span> <span data-ttu-id="61348-150">移除 VHD 中的檔案時，Hyper-v 會將檔案 \_ 修剪到基礎精簡布建的 SAN。</span><span class="sxs-lookup"><span data-stu-id="61348-150">When files are removed in the VHD, the Hyper-V calls File\_TRIM to the underlying thinly provisioned SAN.</span></span> <span data-ttu-id="61348-151">如果修剪大於樓板的資料細微性，SAN 現在可以移除一個小板，進而減少該 SAN 上的 VHD 使用量。</span><span class="sxs-lookup"><span data-stu-id="61348-151">If the TRIMs are bigger than the SLAB granularity, the SAN can now remove a SLAB and hence reduce the footprint of the VHD on that SAN.</span></span>

<span data-ttu-id="61348-152">如果 VHD 位於 Windows 8 型伺服器上，儲存體優化器也會傳送修剪，以降低 VHD 從掛接的 VHD 內的碳足跡。</span><span class="sxs-lookup"><span data-stu-id="61348-152">If the VHD is resident on a Windows 8 based server, the Storage Optimizer will also send TRIMs to reduce the slab footprint of the VHD from within the mounted VHD.</span></span>

## <a name="tests"></a><span data-ttu-id="61348-153">測試</span><span class="sxs-lookup"><span data-stu-id="61348-153">Tests</span></span>

<span data-ttu-id="61348-154">舊版作業系統版本中沒有任何可比較的 Api。</span><span class="sxs-lookup"><span data-stu-id="61348-154">There are no comparable APIs in earlier operating system releases.</span></span> <span data-ttu-id="61348-155">實際的 API 本身應該不會有任何效能影響，不過如果儲存媒體 (正確地執行，) 可能會顯示更佳的寫入效能。</span><span class="sxs-lookup"><span data-stu-id="61348-155">There should be no performance impact from the actual API itself, though the storage media (if implemented correctly) can show better write performance.</span></span> <span data-ttu-id="61348-156">應謹慎使用 API;因為這些範圍將會從儲存體媒體永久移除，所以只應將不再需要的範圍傳遞給您。</span><span class="sxs-lookup"><span data-stu-id="61348-156">The API should be used very carefully; only extents that are no longer needed should be passed down as those extents will be permanently removed from the storage media.</span></span>

## <a name="resources"></a><span data-ttu-id="61348-157">資源</span><span class="sxs-lookup"><span data-stu-id="61348-157">Resources</span></span>

-   [<span data-ttu-id="61348-158">T13 規格</span><span class="sxs-lookup"><span data-stu-id="61348-158">T13 specification</span></span>](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [<span data-ttu-id="61348-159">T10 SCSI 規格</span><span class="sxs-lookup"><span data-stu-id="61348-159">T10 SCSI specification</span></span>](https://www.t10.org/)

 

 




