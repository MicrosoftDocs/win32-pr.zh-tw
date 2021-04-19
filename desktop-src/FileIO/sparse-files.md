---
description: 檔案壓縮大部分的檔案，可有效率地使用磁碟空間。
ms.assetid: 7326041d-f11e-4b80-ac4e-07173e418ce7
title: 疏鬆檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c282ca89c9dc9e44800a2a7fc969c3f883006b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998461"
---
# <a name="sparse-files"></a><span data-ttu-id="0df25-103">疏鬆檔案</span><span class="sxs-lookup"><span data-stu-id="0df25-103">Sparse Files</span></span>

<span data-ttu-id="0df25-104">其中許多資料都是零的檔案，稱為包含 *稀疏資料集*。</span><span class="sxs-lookup"><span data-stu-id="0df25-104">A file in which much of the data is zeros is said to contain a *sparse data set*.</span></span> <span data-ttu-id="0df25-105">這類檔案通常很大，例如，包含要處理之影像資料的檔案，或高速資料庫中的矩陣。</span><span class="sxs-lookup"><span data-stu-id="0df25-105">Files like these are typically very large for example, a file that contains image data to be processed or a matrix within a high-speed database.</span></span> <span data-ttu-id="0df25-106">包含稀疏資料集的檔案有個問題，那就是大部分的檔案都不包含有用的資料，因此因為這樣，磁碟空間的使用效率不佳。</span><span class="sxs-lookup"><span data-stu-id="0df25-106">The problem with files that contain sparse data sets is that the majority of the file does not contain useful data and, because of this, they are an inefficient use of disk space.</span></span>

<span data-ttu-id="0df25-107">NTFS 檔案系統中的檔案壓縮是問題的部分解決方案。</span><span class="sxs-lookup"><span data-stu-id="0df25-107">The file compression in the NTFS file system is a partial solution to the problem.</span></span> <span data-ttu-id="0df25-108">未明確寫入之檔案中的所有資料都會明確設定為零。</span><span class="sxs-lookup"><span data-stu-id="0df25-108">All data in the file that is not explicitly written is explicitly set to zero.</span></span> <span data-ttu-id="0df25-109">檔案壓縮會壓縮這些範圍的零。</span><span class="sxs-lookup"><span data-stu-id="0df25-109">File compression compacts these ranges of zeros.</span></span> <span data-ttu-id="0df25-110">不過，檔案壓縮的缺點是因為資料壓縮和解壓縮，存取時間可能會增加。</span><span class="sxs-lookup"><span data-stu-id="0df25-110">However, a drawback of file compression is that access time may increase due to data compression and decompression.</span></span>

<span data-ttu-id="0df25-111">NTFS 檔案系統中導入了稀疏檔案的支援，做為讓磁碟空間使用量更有效率的另一種方式。</span><span class="sxs-lookup"><span data-stu-id="0df25-111">Support for sparse files is introduced in the NTFS file system as another way to make disk space usage more efficient.</span></span> <span data-ttu-id="0df25-112">啟用稀疏檔案功能時，系統不會將硬碟空間配置給檔案，但包含非零資料的區域除外。</span><span class="sxs-lookup"><span data-stu-id="0df25-112">When sparse file functionality is enabled, the system does not allocate hard disk drive space to a file except in regions where it contains nonzero data.</span></span> <span data-ttu-id="0df25-113">當嘗試寫入作業時，如果緩衝區中有大量資料為零，則不會將零寫入至檔案。</span><span class="sxs-lookup"><span data-stu-id="0df25-113">When a write operation is attempted where a large amount of the data in the buffer is zeros, the zeros are not written to the file.</span></span> <span data-ttu-id="0df25-114">相反地，檔案系統會建立包含檔案中零位置的內部清單，而這份清單會在所有讀取作業期間進行參考。</span><span class="sxs-lookup"><span data-stu-id="0df25-114">Instead, the file system creates an internal list containing the locations of the zeros in the file, and this list is consulted during all read operations.</span></span> <span data-ttu-id="0df25-115">在檔案所在區域內執行讀取作業時，檔案系統會在為讀取作業配置的緩衝區中傳回適當的零數目。</span><span class="sxs-lookup"><span data-stu-id="0df25-115">When a read operation is performed in areas of the file where zeros were located, the file system returns the appropriate number of zeros in the buffer allocated for the read operation.</span></span> <span data-ttu-id="0df25-116">如此一來，在存取它的所有程式中，就不會對稀疏檔案進行維護，而且比壓縮用於此特定案例更有效率。</span><span class="sxs-lookup"><span data-stu-id="0df25-116">In this way, maintenance of the sparse file is transparent to all processes that access it, and is more efficient than compression for this particular scenario.</span></span>

<span data-ttu-id="0df25-117">稀疏檔案的預設資料值為零。不過，它可以設定為其他值。</span><span class="sxs-lookup"><span data-stu-id="0df25-117">The default data value of a sparse file is zero; however, it can be set to other values.</span></span>

<span data-ttu-id="0df25-118">如需有關稀疏檔案的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="0df25-118">For more information about sparse files, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0df25-119">本節內容</span><span class="sxs-lookup"><span data-stu-id="0df25-119">In this section</span></span>



| <span data-ttu-id="0df25-120">主題</span><span class="sxs-lookup"><span data-stu-id="0df25-120">Topic</span></span>                                                                                     | <span data-ttu-id="0df25-121">描述</span><span class="sxs-lookup"><span data-stu-id="0df25-121">Description</span></span>                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0df25-122">稀疏檔案作業</span><span class="sxs-lookup"><span data-stu-id="0df25-122">Sparse File Operations</span></span>](sparse-file-operations.md)<br/>                           | <span data-ttu-id="0df25-123">藉由呼叫 GetVolumeInformation 函數，判斷檔案系統是否支援稀疏檔案。</span><span class="sxs-lookup"><span data-stu-id="0df25-123">Determine whether a file system supports sparse files by calling the GetVolumeInformation function.</span></span><br/>                                                                                |
| [<span data-ttu-id="0df25-124">取得稀疏檔案的大小</span><span class="sxs-lookup"><span data-stu-id="0df25-124">Obtaining the Size of a Sparse File</span></span>](obtaining-the-size-of-a-sparse-file.md)<br/> | <span data-ttu-id="0df25-125">使用 [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) 或 [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) 函式，取得設定檔案大小或檔案的大小總計。</span><span class="sxs-lookup"><span data-stu-id="0df25-125">Get the allocated size or the total size for a file by using either the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) or the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function.</span></span><br/> |
| [<span data-ttu-id="0df25-126">稀疏檔案和磁片配額</span><span class="sxs-lookup"><span data-stu-id="0df25-126">Sparse Files and Disk Quotas</span></span>](sparse-files-and-disk-quota.md)<br/>                | <span data-ttu-id="0df25-127">稀疏檔案會依檔案的名義大小來影響使用者配額，而不是實際配置的磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="0df25-127">A sparse file affects user quotas by the nominal size of the file, not the actual allocated amount of disk space.</span></span><br/>                                                                  |



 

 

 




