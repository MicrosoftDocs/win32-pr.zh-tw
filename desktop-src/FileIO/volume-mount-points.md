---
description: 您可以使用掛接的資料夾，將不同的檔案系統（例如 NTFS 檔案系統、16位 FAT 檔案系統，以及在 CD-ROM 光碟機上的 ISO-9660 檔案系統）統一成單一 NTFS 磁片區上的一個邏輯檔案系統。
ms.assetid: 6de526cd-5537-4411-b43f-3c0bdac70d64
title: 裝載的資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0f0c937ded5f7a6b78f19b17b4c098178f254f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995844"
---
# <a name="mounted-folders"></a><span data-ttu-id="55b50-103">裝載的資料夾</span><span class="sxs-lookup"><span data-stu-id="55b50-103">Mounted Folders</span></span>

<span data-ttu-id="55b50-104">NTFS 檔案系統支援裝載的資料夾。</span><span class="sxs-lookup"><span data-stu-id="55b50-104">The NTFS file system supports mounted folders.</span></span> <span data-ttu-id="55b50-105">*裝載的資料夾* 是磁片區與另一個磁片區上的目錄之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="55b50-105">A *mounted folder* is an association between a volume and a directory on another volume.</span></span> <span data-ttu-id="55b50-106">建立掛接的資料夾時，使用者和應用程式可以使用掛接的資料夾路徑，或使用磁片區的磁碟機號，來存取目標磁片區。</span><span class="sxs-lookup"><span data-stu-id="55b50-106">When a mounted folder is created, users and applications can access the target volume either by using the path to the mounted folder or by using the volume's drive letter.</span></span> <span data-ttu-id="55b50-107">例如，使用者可以建立已掛接的資料夾，將磁片磁碟機 D：與 \\ \\ 磁片磁碟機 c 上的 C： Mnt DDrive 資料夾產生關聯。建立掛接的資料夾之後，使用者可以使用 "C： \\ Mnt \\ DDrive" 路徑來存取磁片磁碟機 D：如同磁片磁碟機 c：的資料夾一樣：</span><span class="sxs-lookup"><span data-stu-id="55b50-107">For example, a user can create a mounted folder to associate drive D: with the C:\\Mnt\\DDrive folder on drive C. After creating the mounted folder, the user can use the "C:\\Mnt\\DDrive" path to access drive D: as if it were a folder on drive C:.</span></span>

<span data-ttu-id="55b50-108">您可以使用掛接的資料夾，將不同的檔案系統（例如 NTFS 檔案系統、16位 FAT 檔案系統，以及在 CD-ROM 光碟機上的 ISO-9660 檔案系統）統一成單一 NTFS 磁片區上的一個邏輯檔案系統。</span><span class="sxs-lookup"><span data-stu-id="55b50-108">Using mounted folders, you can unify disparate file systems such as the NTFS file system, a 16-bit FAT file system, and an ISO-9660 file system on a CD-ROM drive into one logical file system on a single NTFS volume.</span></span> <span data-ttu-id="55b50-109">使用者或應用程式都不需要特定檔案所在目標磁片區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="55b50-109">Neither users nor applications need information about the target volume on which a specific file is located.</span></span> <span data-ttu-id="55b50-110">尋找指定檔案所需的所有資訊都是使用 NTFS 磁片區上掛接之資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="55b50-110">All the information they need to locate a specified file is a complete path using a mounted folder on the NTFS volume.</span></span> <span data-ttu-id="55b50-111">磁片區可以重新排列、替代或細分為許多磁片區，而不需要變更設定的使用者或應用程式。</span><span class="sxs-lookup"><span data-stu-id="55b50-111">Volumes can be rearranged, substituted, or subdivided into many volumes without users or applications needing to change settings.</span></span>

<span data-ttu-id="55b50-112">如需有關已掛接資料夾的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="55b50-112">For information on mounted folders, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="55b50-113">本節內容</span><span class="sxs-lookup"><span data-stu-id="55b50-113">In this section</span></span>



| <span data-ttu-id="55b50-114">主題</span><span class="sxs-lookup"><span data-stu-id="55b50-114">Topic</span></span>                                                                                                                         | <span data-ttu-id="55b50-115">描述</span><span class="sxs-lookup"><span data-stu-id="55b50-115">Description</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55b50-116">建立載入的資料夾</span><span class="sxs-lookup"><span data-stu-id="55b50-116">Creating Mounted Folders</span></span>](mounting-and-dismounting-a-volume.md)<br/>                                                  | <span data-ttu-id="55b50-117">建立裝載的資料夾是兩個步驟的程式。</span><span class="sxs-lookup"><span data-stu-id="55b50-117">Creating a mounted folder is a two-step process.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="55b50-118">列舉裝載的資料夾</span><span class="sxs-lookup"><span data-stu-id="55b50-118">Enumerating Mounted Folders</span></span>](enumerating-volume-mount-points.md)<br/>                                                 | <span data-ttu-id="55b50-119">用來列舉磁片區上所裝載之資料夾的函式。</span><span class="sxs-lookup"><span data-stu-id="55b50-119">Functions to use to enumerate mounted folders on a volume.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="55b50-120">判斷目錄是否為裝載的資料夾</span><span class="sxs-lookup"><span data-stu-id="55b50-120">Determining Whether a Directory Is a Mounted Folder</span></span>](determining-whether-a-directory-is-a-volume-mount-point.md)<br/> | <span data-ttu-id="55b50-121">如何判斷指定的目錄是否為裝載的資料夾。</span><span class="sxs-lookup"><span data-stu-id="55b50-121">How to determine whether a specified directory is a mounted folder.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="55b50-122">指派磁碟機號給磁片區</span><span class="sxs-lookup"><span data-stu-id="55b50-122">Assigning a Drive Letter to a Volume</span></span>](assigning-a-drive-letter-to-a-volume.md)<br/>                                   | <span data-ttu-id="55b50-123">如果沒有 \) 已指派給該磁碟機號的磁片區，您可以使用 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 函式，將磁碟機號 (例如 X：指派給本機磁片區。</span><span class="sxs-lookup"><span data-stu-id="55b50-123">You can assign a drive letter (for example, X:\) to a local volume by using the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, provided there is no volume already assigned to that drive letter.</span></span><br/> |
| [<span data-ttu-id="55b50-124">裝載的資料夾函式</span><span class="sxs-lookup"><span data-stu-id="55b50-124">Mounted Folder Functions</span></span>](volume-mount-point-functions.md)<br/>                                                       | <span data-ttu-id="55b50-125">用來管理裝載資料夾的函式。</span><span class="sxs-lookup"><span data-stu-id="55b50-125">Functions used to manage mounted folders.</span></span><br/>                                                                                                                                                                        |



 

<span data-ttu-id="55b50-126">如需範例，請參閱 [裝載的資料夾範例](volume-mount-point-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="55b50-126">For examples, see [Mounted Folder Examples](volume-mount-point-examples.md).</span></span>

 

 




