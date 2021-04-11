---
description: 管理目錄專案資料表、目錄控制碼、重新分析點的目錄。
title: 本機檔案系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f624ef1999b81adb63ba1d5b7e349259cabd53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692256"
---
# <a name="local-file-systems"></a><span data-ttu-id="2ab4a-103">本機檔案系統</span><span class="sxs-lookup"><span data-stu-id="2ab4a-103">Local File Systems</span></span>

<span data-ttu-id="2ab4a-104">*檔案系統* 可讓應用程式儲存和取出儲存裝置上的檔案。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-104">A *file system* enables applications to store and retrieve files on storage devices.</span></span> <span data-ttu-id="2ab4a-105">檔案會以階層式結構放置。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-105">Files are placed in a hierarchical structure.</span></span> <span data-ttu-id="2ab4a-106">檔案系統會指定檔案的命名慣例，並使用格式來指定樹狀結構中檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-106">The file system specifies naming conventions for files and the format for specifying the path to a file in the tree structure.</span></span>

<span data-ttu-id="2ab4a-107">每個檔案系統都包含一或多個驅動程式和動態連結程式庫，可定義檔案系統的資料格式和功能。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-107">Each file system consists of one or more drivers and dynamic-link libraries that define the data formats and features of the file system.</span></span> <span data-ttu-id="2ab4a-108">檔案系統可存在於許多不同類型的存放裝置上，包括硬碟、自動播放程式、卸載式磁片、磁帶備份單元和記憶卡。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-108">File systems can exist on many different types of storage devices, including hard disks, jukeboxes, removable optical disks, tape back-up units, and memory cards.</span></span>

<span data-ttu-id="2ab4a-109">Windows 支援的所有檔案系統都有下列儲存元件：</span><span class="sxs-lookup"><span data-stu-id="2ab4a-109">All file systems supported by Windows have the following storage components:</span></span>

-   <span data-ttu-id="2ab4a-110">卷。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-110">Volumes.</span></span> <span data-ttu-id="2ab4a-111">*磁片* 區是目錄和檔案的集合。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-111">A *volume* is a collection of directories and files.</span></span>
-   <span data-ttu-id="2ab4a-112">目錄。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-112">Directories.</span></span> <span data-ttu-id="2ab4a-113">*目錄* 是目錄和檔案的階層式集合。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-113">A *directory* is a hierarchical collection of directories and files.</span></span>
-   <span data-ttu-id="2ab4a-114">檔案</span><span class="sxs-lookup"><span data-stu-id="2ab4a-114">Files.</span></span> <span data-ttu-id="2ab4a-115">檔案 *是相關資料的邏輯* 群組。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-115">A *file* is a logical grouping of related data.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2ab4a-116">本節內容</span><span class="sxs-lookup"><span data-stu-id="2ab4a-116">In this section</span></span>



| <span data-ttu-id="2ab4a-117">主題</span><span class="sxs-lookup"><span data-stu-id="2ab4a-117">Topic</span></span>                                                                | <span data-ttu-id="2ab4a-118">描述</span><span class="sxs-lookup"><span data-stu-id="2ab4a-118">Description</span></span>                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ab4a-119">目錄管理</span><span class="sxs-lookup"><span data-stu-id="2ab4a-119">Directory Management</span></span>](directory-management.md)<br/>          | <span data-ttu-id="2ab4a-120">*目錄* 是目錄和檔案的階層式集合。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-120">A *directory* is a hierarchical collection of directories and files.</span></span> <span data-ttu-id="2ab4a-121">單一目錄中可包含之檔案數目的唯一條件約束，是目錄所在磁片的實體大小。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-121">The only constraint on the number of files that can be contained in a single directory is the physical size of the disk on which the directory is located.</span></span><br/> |
| [<span data-ttu-id="2ab4a-122">磁碟管理</span><span class="sxs-lookup"><span data-stu-id="2ab4a-122">Disk Management</span></span>](disk-management.md)<br/>                    | <span data-ttu-id="2ab4a-123">硬碟是電腦內的 *固定* 磁片，可儲存並提供相對快速的大量資料存取。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-123">A *hard disk* is a rigid disk inside a computer that stores and provides relatively quick access to large amounts of data.</span></span> <span data-ttu-id="2ab4a-124">這是最常用於 Windows 的儲存體類型。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-124">It is the type of storage most often used with Windows.</span></span> <span data-ttu-id="2ab4a-125">系統也支援卸載式媒體。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-125">The system also supports removable media.</span></span><br/>    |
| [<span data-ttu-id="2ab4a-126">檔案管理</span><span class="sxs-lookup"><span data-stu-id="2ab4a-126">File Management</span></span>](file-management.md)<br/>                    | <span data-ttu-id="2ab4a-127">*File 物件* 提供資源的表示 (實體裝置或實體裝置上的資源，可由 i/o 系統管理) 。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-127">A *file object* provides a representation of a resource (either a physical device or a resource located on a physical device) that can be managed by the I/O system.</span></span><br/>                                                            |
| [<span data-ttu-id="2ab4a-128">交易式 NTFS (TxF) </span><span class="sxs-lookup"><span data-stu-id="2ab4a-128">Transactional NTFS (TxF)</span></span>](transactional-ntfs-portal.md)<br/> | <span data-ttu-id="2ab4a-129">交易式 NTFS (TxF) 允許在一筆交易中執行 NTFS 檔案系統磁片區上的檔案作業。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-129">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="2ab4a-130">磁碟區管理</span><span class="sxs-lookup"><span data-stu-id="2ab4a-130">Volume Management</span></span>](volume-management.md)<br/>                | <span data-ttu-id="2ab4a-131">檔案系統中的最高層級組織是 *磁片* 區。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-131">The highest level of organization in the file system is the *volume*.</span></span> <span data-ttu-id="2ab4a-132">檔案系統位於磁片區上。</span><span class="sxs-lookup"><span data-stu-id="2ab4a-132">A file system resides on a volume.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="2ab4a-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ab4a-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2ab4a-134">[FAT 技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2ab4a-134">[FAT Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="2ab4a-135">[檔案系統技術](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2ab4a-135">[File Systems Technologies](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="2ab4a-136">[NTFS 技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2ab4a-136">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

