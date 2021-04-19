---
description: 建立裝載的資料夾是兩個步驟的程式。
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: 建立載入的資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d64630716be6e85ac323c80e89dda0500ba6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982744"
---
# <a name="creating-mounted-folders"></a><span data-ttu-id="1f18b-103">建立載入的資料夾</span><span class="sxs-lookup"><span data-stu-id="1f18b-103">Creating Mounted Folders</span></span>

<span data-ttu-id="1f18b-104">建立裝載的資料夾是兩個步驟的程式。</span><span class="sxs-lookup"><span data-stu-id="1f18b-104">Creating a mounted folder is a two-step process.</span></span> <span data-ttu-id="1f18b-105">首先，使用掛接點來呼叫 [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) ， (磁碟機號、磁片區 GUID 路徑，或要指派給掛接資料夾之磁片區的已掛接資料夾) 。</span><span class="sxs-lookup"><span data-stu-id="1f18b-105">First, call [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) with the mount point (drive letter, volume GUID path, or mounted folder) of the volume to be assigned to the mounted folder.</span></span> <span data-ttu-id="1f18b-106">然後使用 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 函式，將傳回的磁片區 GUID 路徑與另一個磁片區上所需的目錄產生關聯。</span><span class="sxs-lookup"><span data-stu-id="1f18b-106">Then use the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function to associate the returned volume GUID path with the desired directory on another volume.</span></span> <span data-ttu-id="1f18b-107">如需範例程式碼，請參閱 [建立載入的資料夾](mounting-a-volume-at-a-mount-point.md)。</span><span class="sxs-lookup"><span data-stu-id="1f18b-107">For example code, see [Creating a Mounted Folder](mounting-a-volume-at-a-mount-point.md).</span></span>

<span data-ttu-id="1f18b-108">您的應用程式可以指定磁片區上的任何空白目錄，而非根節點做為裝載的資料夾。</span><span class="sxs-lookup"><span data-stu-id="1f18b-108">Your application can designate any empty directory on a volume other than the root as a mounted folder.</span></span> <span data-ttu-id="1f18b-109">當您呼叫 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 函式時，該目錄會成為裝載的資料夾。</span><span class="sxs-lookup"><span data-stu-id="1f18b-109">When you call the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, that directory becomes the mounted folder.</span></span> <span data-ttu-id="1f18b-110">您可以將相同的磁片區指派給多個裝載的資料夾。</span><span class="sxs-lookup"><span data-stu-id="1f18b-110">You can assign the same volume to multiple mounted folders.</span></span>

<span data-ttu-id="1f18b-111">建立掛接的資料夾之後，它會透過電腦自動重新開機進行維護。</span><span class="sxs-lookup"><span data-stu-id="1f18b-111">After the mounted folder has been established, it is maintained through computer restarts automatically.</span></span>

<span data-ttu-id="1f18b-112">如果磁片區失敗，任何已指派給該磁片區上掛接之資料夾的磁片區，都無法再透過這些掛接的資料夾存取。</span><span class="sxs-lookup"><span data-stu-id="1f18b-112">If a volume fails, any volumes that have been assigned to mounted folders on that volume can no longer be accessed through those mounted folders.</span></span> <span data-ttu-id="1f18b-113">例如，假設您有兩個磁片區： C：和 D：，而該 D：與裝載的資料夾 C： MountD 相關聯 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="1f18b-113">For example, suppose you have two volumes, C: and D:, and that D: is associated with the mounted folder C:\\MountD\\.</span></span> <span data-ttu-id="1f18b-114">如果磁片區 C：失敗，則無法再透過路徑 C： MountD 存取磁片區 D \\ ： \\ 。</span><span class="sxs-lookup"><span data-stu-id="1f18b-114">If volume C: fails, volume D: can no longer be accessed through the path C:\\MountD\\.</span></span>

<span data-ttu-id="1f18b-115">只有 NTFS 檔案系統磁片區可以有掛接的資料夾，但裝載資料夾的目標磁片區可以是非 NTFS 磁片區。</span><span class="sxs-lookup"><span data-stu-id="1f18b-115">Only NTFS file system volumes can have mounted folders, but the target volumes for the mounted folders can be non-NTFS volumes.</span></span>

<span data-ttu-id="1f18b-116">裝載的資料夾是使用重新分析點來執行，並受限於其限制。</span><span class="sxs-lookup"><span data-stu-id="1f18b-116">Mounted folders are implemented by using reparse points and are subject to their restrictions.</span></span> <span data-ttu-id="1f18b-117">如需詳細資訊，請參閱重新 [分析點](reparse-points.md)。</span><span class="sxs-lookup"><span data-stu-id="1f18b-117">For more information, see [Reparse Points](reparse-points.md).</span></span> <span data-ttu-id="1f18b-118">不需要操作重新分析點來使用掛接的資料夾; [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 等函數會為您處理所有的重新分析點詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1f18b-118">It is not necessary to manipulate reparse points to use mounted folders; functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) handle all the reparse point details for you.</span></span>

<span data-ttu-id="1f18b-119">因為掛接的資料夾是目錄，您可以重新命名、移除、移動和操作它們，就像其他目錄一樣。</span><span class="sxs-lookup"><span data-stu-id="1f18b-119">Because mounted folders are directories, you can rename, remove, move, and otherwise manipulate them, as you would other directories.</span></span>

<span data-ttu-id="1f18b-120"> (附注： TechNet 檔會使用一詞掛接的 *磁片磁碟機* 來參考 *裝載的資料夾*。 ) </span><span class="sxs-lookup"><span data-stu-id="1f18b-120">(Note: The TechNet documentation uses the term *mounted drives* to refer to *mounted folders*.)</span></span>

 

 



