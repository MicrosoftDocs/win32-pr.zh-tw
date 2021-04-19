---
description: 藉由呼叫 GetVolumeInformation 函數，判斷檔案系統是否支援稀疏檔案。
ms.assetid: a08f6bbc-c139-4396-8964-4aa63285f3f5
title: 稀疏檔案作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c23d26fc1c52db32ca7674aec2fc487a826e9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972665"
---
# <a name="sparse-file-operations"></a><span data-ttu-id="be32d-103">稀疏檔案作業</span><span class="sxs-lookup"><span data-stu-id="be32d-103">Sparse File Operations</span></span>

<span data-ttu-id="be32d-104">若要判斷檔案系統是否支援稀疏檔案，請呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)函式，並檢查檔案是否支援透過 *lpFileSystemFlags* 參數傳回的 **\_ \_ 稀疏 \_** 檔案位旗標。</span><span class="sxs-lookup"><span data-stu-id="be32d-104">To determine whether a file system supports sparse files, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FILE\_SUPPORTS\_SPARSE\_FILES** bit flag returned through the *lpFileSystemFlags* parameter.</span></span>

<span data-ttu-id="be32d-105">大部分的應用程式不會察覺到稀疏檔案，也不會建立稀疏檔案。</span><span class="sxs-lookup"><span data-stu-id="be32d-105">Most applications are not aware of sparse files and will not create sparse files.</span></span> <span data-ttu-id="be32d-106">應用程式讀取稀疏檔案的事實是應用程式的透明。</span><span class="sxs-lookup"><span data-stu-id="be32d-106">The fact that an application is reading a sparse file is transparent to the application.</span></span> <span data-ttu-id="be32d-107">知道稀疏檔案的應用程式應該要判斷其資料集是否適合保存在稀疏檔案中。</span><span class="sxs-lookup"><span data-stu-id="be32d-107">An application that is aware of sparse-files should determine whether its data set is suitable to be kept in a sparse file.</span></span> <span data-ttu-id="be32d-108">進行這項判斷之後，應用程式必須使用 [**FSCTL \_ SET \_ sparse**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse) control 程式碼，將檔案明確宣告為稀疏。</span><span class="sxs-lookup"><span data-stu-id="be32d-108">After that determination is made, the application must explicitly declare a file as sparse, using the [**FSCTL\_SET\_SPARSE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse) control code.</span></span>

<span data-ttu-id="be32d-109">應用程式將檔案設定為稀疏之後，應用程式就可以使用 [**FSCTL \_ set \_ zero \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) control 程式碼，將檔案的區域設定為零。</span><span class="sxs-lookup"><span data-stu-id="be32d-109">After an application has set a file to be sparse, the application can use the [**FSCTL\_SET\_ZERO\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) control code to set a region of the file to zero.</span></span> <span data-ttu-id="be32d-110">此外，應用程式可以使用已配置 [**的 \_ FSCTL \_ 查詢 \_ 範圍**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges) 控制程式代碼，以加快搜尋稀疏檔案中非零資料的速度。</span><span class="sxs-lookup"><span data-stu-id="be32d-110">In addition, the application can use the [**FSCTL\_QUERY\_ALLOCATED\_RANGES**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges) control code to speed searches for nonzero data in the sparse file.</span></span>

<span data-ttu-id="be32d-111">當您使用 [**FSCTL \_ SET \_ ZERO \_ data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) 以外的函式或作業來執行 (寫入作業時，如果資料不是由零所組成，則會將整個寫入長度寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="be32d-111">When you perform a write operation (with a function or operation other than [**FSCTL\_SET\_ZERO\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) whose data consists of nothing but zeros, zeros will be written to the disk for the entire length of the write.</span></span> <span data-ttu-id="be32d-112">若要從零移出檔案範圍並維持疏鬆度，請使用 **FSCTL \_ 設定零的 \_ \_ 資料**。</span><span class="sxs-lookup"><span data-stu-id="be32d-112">To zero out a range of the file and maintain sparseness, use **FSCTL\_SET\_ZERO\_DATA**.</span></span>

<span data-ttu-id="be32d-113">疏鬆度感知的應用程式可能也會將現有的檔案設定為稀疏。</span><span class="sxs-lookup"><span data-stu-id="be32d-113">A sparseness-aware application may also set an existing file to be sparse.</span></span> <span data-ttu-id="be32d-114">如果應用程式將現有的檔案設定為稀疏，則應該針對包含零的區域掃描該檔案，然後使用 [**FSCTL \_ 設定 \_ 零 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) 來重設這些區域，因此可能會解除配置某些實體磁片儲存體。</span><span class="sxs-lookup"><span data-stu-id="be32d-114">If an application sets an existing file to be sparse, it should then scan the file for regions which contain zeros, and use [**FSCTL\_SET\_ZERO\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) to reset those regions, thereby possibly deallocating some physical disk storage.</span></span> <span data-ttu-id="be32d-115">升級為稀疏檔案感知的應用程式應該執行這種轉換。</span><span class="sxs-lookup"><span data-stu-id="be32d-115">An application upgraded to sparse file awareness should perform this conversion.</span></span>

<span data-ttu-id="be32d-116">當您從稀疏檔案的清空部分執行讀取作業時，作業系統可能無法從硬碟讀取。</span><span class="sxs-lookup"><span data-stu-id="be32d-116">When you perform a read operation from a zeroed-out portion of a sparse file, the operating system may not read from the hard disk drive.</span></span> <span data-ttu-id="be32d-117">相反地，系統會辨識要讀取之檔案的部分包含零，並傳回已滿零的緩衝區，而不會實際讀取磁片。</span><span class="sxs-lookup"><span data-stu-id="be32d-117">Instead, the system recognizes that the portion of the file to be read contains zeros, and it returns a buffer full of zeros without actually reading from the disk.</span></span>

<span data-ttu-id="be32d-118">就像任何其他檔案一樣，系統也可以將資料寫入至稀疏檔案中的任何位置或從中讀取資料。</span><span class="sxs-lookup"><span data-stu-id="be32d-118">As with any other file, the system can write data to or read data from any position in a sparse file.</span></span> <span data-ttu-id="be32d-119">寫入至先前的已清空檔案部分的非零資料可能會導致配置磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="be32d-119">Nonzero data being written to a previously zeroed portion of the file may result in allocation of disk space.</span></span> <span data-ttu-id="be32d-120">使用非零資料寫入零 (只有 [**FSCTL \_ 設定 \_ 零 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) 可能會導致磁碟空間解除配置。</span><span class="sxs-lookup"><span data-stu-id="be32d-120">Zeros being written over nonzero data (only with [**FSCTL\_SET\_ZERO\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) may result in a deallocation of disk space.</span></span>

> [!Note]  
> <span data-ttu-id="be32d-121">藉由在 [**FSCTL \_ 設定 \_ 零 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)的情況下寫入零，應用程式就能維護疏鬆度。</span><span class="sxs-lookup"><span data-stu-id="be32d-121">It is up to the application to maintain sparseness by writing zeros with [**FSCTL\_SET\_ZERO\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data).</span></span>

 

<span data-ttu-id="be32d-122">在 NTFS 檔案系統上處理壓縮檔案的磁碟重組工具，將會正確處理 NTFS 檔案系統磁片區上的稀疏檔。</span><span class="sxs-lookup"><span data-stu-id="be32d-122">Defragmentation tools that handle compressed files on NTFS file systems will correctly handle sparse files on NTFS file system volumes.</span></span> <span data-ttu-id="be32d-123">在使用可用空間之前，大型且高度分散的稀疏檔案可能會超過磁片範圍的 NTFS 限制。</span><span class="sxs-lookup"><span data-stu-id="be32d-123">Large and highly fragmented sparse files can exceed the NTFS limitation on disk extents before available space is used.</span></span> <span data-ttu-id="be32d-124">如需詳細資訊，請參閱 [擴充檔案可能會因為「磁片已滿」錯誤而失敗，即使磁片區具有可用空間也一樣](https://support.microsoft.com/default.aspx/kb/957180)。</span><span class="sxs-lookup"><span data-stu-id="be32d-124">For more information, see [Extending a File may fail with "Disk Full" Error even though Volume has Free Space](https://support.microsoft.com/default.aspx/kb/957180).</span></span>

 

 
