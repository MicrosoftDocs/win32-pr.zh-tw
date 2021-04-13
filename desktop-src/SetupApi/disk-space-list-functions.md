---
description: 下列函式會搭配磁碟空間清單使用。
ms.assetid: 18693b2d-6b0f-4f9c-b3cf-e50c36e2f2e1
title: Disk-Space 清單函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f520cc7a3ddcd0b12b27bd11768a95231a8ed4b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319583"
---
# <a name="disk-space-list-functions"></a><span data-ttu-id="398bd-103">Disk-Space 清單函數</span><span class="sxs-lookup"><span data-stu-id="398bd-103">Disk-Space List Functions</span></span>

<span data-ttu-id="398bd-104">下列函式會搭配磁碟空間清單使用。</span><span class="sxs-lookup"><span data-stu-id="398bd-104">The following functions are used with the disk-space list.</span></span>



| <span data-ttu-id="398bd-105">函式</span><span class="sxs-lookup"><span data-stu-id="398bd-105">Function</span></span>                                                                                         | <span data-ttu-id="398bd-106">描述</span><span class="sxs-lookup"><span data-stu-id="398bd-106">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="398bd-107">**SetupAdjustDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="398bd-107">**SetupAdjustDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)                                     | <span data-ttu-id="398bd-108">調整指定磁片磁碟機所需的空間量。</span><span class="sxs-lookup"><span data-stu-id="398bd-108">Adjusts the amount of required space for a specified drive.</span></span>                                                                          |
| [<span data-ttu-id="398bd-109">**SetupCreateDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="398bd-109">**SetupCreateDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)                                     | <span data-ttu-id="398bd-110">建立磁碟空間清單，並將資源配置給它。</span><span class="sxs-lookup"><span data-stu-id="398bd-110">Creates a disk-space list and allocates resources to it.</span></span>                                                                             |
| [<span data-ttu-id="398bd-111">**SetupDestroyDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="398bd-111">**SetupDestroyDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)                                   | <span data-ttu-id="398bd-112">終結磁碟空間清單，釋放配置給它的資源。</span><span class="sxs-lookup"><span data-stu-id="398bd-112">Destroys a disk-space list, freeing the resources allocated to it.</span></span>                                                                   |
| [<span data-ttu-id="398bd-113">**SetupDuplicateDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="398bd-113">**SetupDuplicateDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)                               | <span data-ttu-id="398bd-114">將磁碟空間清單複製為新的獨立磁碟空間清單。</span><span class="sxs-lookup"><span data-stu-id="398bd-114">Duplicates a disk-space list as a new independent disk-space list.</span></span>                                                                   |
| [<span data-ttu-id="398bd-115">**SetupQueryDrivesInDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="398bd-115">**SetupQueryDrivesInDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)                       | <span data-ttu-id="398bd-116">針對 [磁碟空間] 清單中所列的所有磁片磁碟機，以磁片磁碟機規格填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="398bd-116">Fills a buffer with the drive specifications for all the drives listed in the disk-space list.</span></span>                                       |
| [<span data-ttu-id="398bd-117">**SetupQuerySpaceRequiredOnDrive**</span><span class="sxs-lookup"><span data-stu-id="398bd-117">**SetupQuerySpaceRequiredOnDrive**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)                         | <span data-ttu-id="398bd-118">傳回在 [磁碟空間] 清單中所列的特定磁片磁碟機上完成檔案作業所需的磁碟空間總量。</span><span class="sxs-lookup"><span data-stu-id="398bd-118">Returns the total amount of disk space required to complete the file operations on a particular drive listed in the disk-space list.</span></span> |
| [<span data-ttu-id="398bd-119">**SetupAddToDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="398bd-119">**SetupAddToDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)                                       | <span data-ttu-id="398bd-120">將檔案複製或刪除操作新增至磁碟空間清單。</span><span class="sxs-lookup"><span data-stu-id="398bd-120">Adds a file copy or delete operation to the disk-space list.</span></span>                                                                         |
| [<span data-ttu-id="398bd-121">**SetupAddSectionToDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="398bd-121">**SetupAddSectionToDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)                         | <span data-ttu-id="398bd-122">將 INF 檔案的 [ **複製** 檔案] 或 [ **刪除** 檔案] 區段中的所有檔案作業新增至磁碟空間清單。</span><span class="sxs-lookup"><span data-stu-id="398bd-122">Adds all the file operations in a **Copy Files** or **Delete Files** section of an INF file to a disk-space list.</span></span>                    |
| [<span data-ttu-id="398bd-123">**SetupAddInstallSectionToDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="398bd-123">**SetupAddInstallSectionToDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)           | <span data-ttu-id="398bd-124">將 INF 檔案的 [ **安裝** ] 區段中的所有檔案作業新增至 [磁碟空間] 清單。</span><span class="sxs-lookup"><span data-stu-id="398bd-124">Adds all the file operations in an **Install** section of an INF file to the disk-space list.</span></span>                                        |
| [<span data-ttu-id="398bd-125">**SetupRemoveFromDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="398bd-125">**SetupRemoveFromDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)                             | <span data-ttu-id="398bd-126">從磁碟空間清單中移除檔案複製或刪除操作。</span><span class="sxs-lookup"><span data-stu-id="398bd-126">Removes a file copy or delete operation from a disk-space list.</span></span>                                                                      |
| [<span data-ttu-id="398bd-127">**SetupRemoveSectionFromDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="398bd-127">**SetupRemoveSectionFromDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)               | <span data-ttu-id="398bd-128">從磁碟空間清單中移除 INF 檔案的 [ **複製** 檔案] 或 [ **刪除** 檔案] 區段中的所有檔案作業。</span><span class="sxs-lookup"><span data-stu-id="398bd-128">Removes all the file operations in a **Copy Files** or **Delete Files** section of an INF file from a disk-space list.</span></span>               |
| [<span data-ttu-id="398bd-129">**SetupRemoveInstallSectionFromDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="398bd-129">**SetupRemoveInstallSectionFromDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) | <span data-ttu-id="398bd-130">從磁碟空間清單中移除 INF 檔案的 [ **安裝** ] 區段中的所有檔案作業。</span><span class="sxs-lookup"><span data-stu-id="398bd-130">Removes all the file operations in the **Install** section of an INF file from the disk-space list.</span></span>                                  |



 

 

 



