---
title: SIS 連結和重新分析點
description: SIS 是 NTFS 篩選器驅動程式，可將重複的檔案取代為複製時寫入連結 (稱為 SIS 連結) 指向單一備份檔，以減少這些檔案的磁片和快取額外負荷。
ms.assetid: 1600a9ff-413c-4059-b04c-c862f6cf8f32
keywords:
- 重新分析點備份
- 單一實例存放區 (SIS) 備份，SIS 連結
- 儲存 (SIS) 備份、重新分析點的單一實例存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4987e7c64a83e7d0b02ed91899a182616be7943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093060"
---
# <a name="sis-links-and-reparse-points"></a><span data-ttu-id="b5565-106">SIS 連結和重新分析點</span><span class="sxs-lookup"><span data-stu-id="b5565-106">SIS Links and Reparse Points</span></span>

<span data-ttu-id="b5565-107">SIS 是 NTFS 篩選器驅動程式，可將重複的檔案取代為複製時寫入連結 (稱為 SIS 連結) 指向單一備份檔，以減少這些檔案的磁片和快取額外負荷。</span><span class="sxs-lookup"><span data-stu-id="b5565-107">SIS is an NTFS filter driver that replaces duplicate files with copy-on-write links (referred to as SIS links) that point to a single backing file, reducing the disk and cache overhead of those files.</span></span> <span data-ttu-id="b5565-108">此備份檔案包含在 [通用存放區](the-sis-common-store-and-common-store-files.md)中。</span><span class="sxs-lookup"><span data-stu-id="b5565-108">This backing file is contained in a [common store](the-sis-common-store-and-common-store-files.md).</span></span> <span data-ttu-id="b5565-109">SIS 架構的執行會利用包含 SIS 連結相關資訊的重新 [分析點](/windows/desktop/FileIO/reparse-points) 。</span><span class="sxs-lookup"><span data-stu-id="b5565-109">The implementation of the SIS architecture makes use of [reparse points](/windows/desktop/FileIO/reparse-points) that contain information about the SIS links.</span></span>

<span data-ttu-id="b5565-110">SIS 連結會實作為稀疏檔案，通常會有大部分未配置的檔案範圍，以及重新分析點。</span><span class="sxs-lookup"><span data-stu-id="b5565-110">SIS links are implemented as sparse files, usually with most ranges of the file unallocated, and a reparse point.</span></span> <span data-ttu-id="b5565-111">重新分析點的結構和內容對備份和還原應用程式而言是不透明的;不過，您的應用程式會將這些重新分析點內的資料，以及處理它們中資訊的 SIS API 函式，傳送和取出。</span><span class="sxs-lookup"><span data-stu-id="b5565-111">The structure and contents of a reparse point is opaque to your backup and restore applications; however, your applications send and retrieve the data within these reparse points to and from SIS API functions that process the information in them.</span></span> <span data-ttu-id="b5565-112">重新分析點中的資訊是指包含實際檔案資料的單一備份檔案。</span><span class="sxs-lookup"><span data-stu-id="b5565-112">The information in a reparse point refers to a single backing file that contains the actual file data.</span></span> <span data-ttu-id="b5565-113">這個備份檔稱為 [通用存放區](the-sis-common-store-and-common-store-files.md)檔案，而且存在於一般存放區中。</span><span class="sxs-lookup"><span data-stu-id="b5565-113">This backing file is called a [common-store file](the-sis-common-store-and-common-store-files.md), and it exists in the common store.</span></span>

<span data-ttu-id="b5565-114">還原 SIS 連結時，您的還原應用程式應該執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b5565-114">When restoring a SIS link, your restore application should perform the following steps:</span></span>

1.  <span data-ttu-id="b5565-115">判斷 SIS 連結所指向的一般存放區檔案。</span><span class="sxs-lookup"><span data-stu-id="b5565-115">Determine the common-store file or files to which the SIS link points.</span></span>
2.  <span data-ttu-id="b5565-116">如果檔案不存在於一般存放區中，請將該檔案連同 SIS 連結一起還原。</span><span class="sxs-lookup"><span data-stu-id="b5565-116">If the file or files do not exist in the common store, restore the file or files along with the SIS link.</span></span>
3.  <span data-ttu-id="b5565-117">如果 SIS 連結指向存在於磁片上的通用存放區檔案，則只還原 SIS 連結。</span><span class="sxs-lookup"><span data-stu-id="b5565-117">If the SIS link points to a common-store file or files that exist on the disk, then restore only the SIS link.</span></span> <span data-ttu-id="b5565-118">回想一下，一般存放區檔案中的資料永遠不會變更，因此，如果指定的一般存放區檔案在還原時仍在磁片上，它會與備份時的內容相同，因此不需要覆寫它。</span><span class="sxs-lookup"><span data-stu-id="b5565-118">Recall that the data in common-store files never changes, so if a given common-store file is still on the disk at restore time, it has the same contents as when it was backed up and there is no need to overwrite it.</span></span>

<span data-ttu-id="b5565-119">SIS 輔助備份所需的唯一額外負荷，是您的備份應用程式必須備份 SIS 連結和與備份檔案相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="b5565-119">The only additional overhead required for SIS-assisted backups is that your backup application must back up the SIS link and the data associated with the backing files.</span></span> <span data-ttu-id="b5565-120">所有 SIS 備份和還原作業都是特定磁片區的本機。</span><span class="sxs-lookup"><span data-stu-id="b5565-120">All SIS backup and restore operations are local to a specific volume.</span></span>

 

 