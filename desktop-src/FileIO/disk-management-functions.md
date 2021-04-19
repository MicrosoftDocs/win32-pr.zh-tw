---
description: 磁片管理中使用的函數。
ms.assetid: 301d3062-29a1-4b44-bbcd-e9d5b7d7823b
title: 磁片管理功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 677443c58aa8b9a60758d817e31e3804ef25ae66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997905"
---
# <a name="disk-management-functions"></a><span data-ttu-id="caa7e-103">磁片管理功能</span><span class="sxs-lookup"><span data-stu-id="caa7e-103">Disk Management Functions</span></span>

<span data-ttu-id="caa7e-104">下列功能用於磁片管理。</span><span class="sxs-lookup"><span data-stu-id="caa7e-104">The following functions are used in disk management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="caa7e-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="caa7e-105">In this section</span></span>



| <span data-ttu-id="caa7e-106">函式</span><span class="sxs-lookup"><span data-stu-id="caa7e-106">Function</span></span>                                                    | <span data-ttu-id="caa7e-107">描述</span><span class="sxs-lookup"><span data-stu-id="caa7e-107">Description</span></span>                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="caa7e-108">**GetDiskFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="caa7e-108">**GetDiskFreeSpace**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)<br/>     | <span data-ttu-id="caa7e-109">抓取指定磁片的相關資訊，包括磁片上的可用空間量。</span><span class="sxs-lookup"><span data-stu-id="caa7e-109">Retrieves information about the specified disk, including the amount of free space on the disk.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="caa7e-110">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="caa7e-110">**GetDiskFreeSpaceEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)<br/> | <span data-ttu-id="caa7e-111">抓取磁片區可用空間量的相關資訊，也就是總空間量、可用空間的總容量，以及與呼叫執行緒相關聯之使用者可用的可用空間總量。</span><span class="sxs-lookup"><span data-stu-id="caa7e-111">Retrieves information about the amount of space that is available on a disk volume, which is the total amount of space, the total amount of free space, and the total amount of free space available to the user that is associated with the calling thread.</span></span><br/> |



 

<span data-ttu-id="caa7e-112">磁片管理中使用的其他功能。</span><span class="sxs-lookup"><span data-stu-id="caa7e-112">Other functions used in disk management.</span></span>



| <span data-ttu-id="caa7e-113">函式</span><span class="sxs-lookup"><span data-stu-id="caa7e-113">Function</span></span>                         | <span data-ttu-id="caa7e-114">描述</span><span class="sxs-lookup"><span data-stu-id="caa7e-114">Description</span></span>                                                                                                                                                                                                                        |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="caa7e-115">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="caa7e-115">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) | <span data-ttu-id="caa7e-116">建立或開啟檔案或 i/o 裝置。</span><span class="sxs-lookup"><span data-stu-id="caa7e-116">Creates or opens a file or I/O device.</span></span> <span data-ttu-id="caa7e-117">最常使用的 i/o 裝置如下：檔案、檔案串流、目錄、實體磁片、磁片區、主控台緩衝區、磁帶機、通訊資源、郵筒和管道。</span><span class="sxs-lookup"><span data-stu-id="caa7e-117">The most commonly used I/O devices are as follows: file, file stream, directory, physical disk, volume, console buffer, tape drive, communications resource, mailslot, and pipe.</span></span><br/> |
| [<span data-ttu-id="caa7e-118">**DeleteFile**</span><span class="sxs-lookup"><span data-stu-id="caa7e-118">**DeleteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) | <span data-ttu-id="caa7e-119">刪除現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="caa7e-119">Deletes an existing file.</span></span><br/>                                                                                                                                                                                               |



 

 

 




