---
description: 您必須先使用 SetupCreateDiskSpaceList 函式來建立檔案作業，才能從磁碟空間清單中新增或移除檔案作業。
ms.assetid: 287fd84a-dc8c-4a5c-b998-db5f2fbee5f1
title: 使用 Disk-Space 清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a19f100fd5190472f5f6bfebaf74affe1a789cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978914"
---
# <a name="using-the-disk-space-list"></a><span data-ttu-id="234b2-103">使用 Disk-Space 清單</span><span class="sxs-lookup"><span data-stu-id="234b2-103">Using the Disk-Space List</span></span>

<span data-ttu-id="234b2-104">您必須先使用 [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) 函式來建立檔案作業，才能從磁碟空間清單中新增或移除檔案作業。</span><span class="sxs-lookup"><span data-stu-id="234b2-104">Before you can add or remove file operations from the disk-space list, you must create it by using the [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) function.</span></span>

<span data-ttu-id="234b2-105">建立磁碟空間清單之後，您可以使用 [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)，將個別的檔案複製或刪除作業新增至清單。</span><span class="sxs-lookup"><span data-stu-id="234b2-105">After you create a disk-space list you can add individual file copy or delete operations to the list by using [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista).</span></span> <span data-ttu-id="234b2-106">若要在整個 INF 區段中新增所有檔案複製或刪除作業，請使用 [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) 或 [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) 函數。</span><span class="sxs-lookup"><span data-stu-id="234b2-106">To add all the file copy or delete operations in an entire INF section, use either the [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) or [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) function.</span></span>

<span data-ttu-id="234b2-107">將所有安裝操作新增到磁碟空間清單之後，您可以使用 [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) 函式來查詢它，以找出指定安裝所需的磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="234b2-107">After you add all the installation operations to the disk-space list, you can query it to find out how much disk space is required for the specified installation by using the [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) function.</span></span>

<span data-ttu-id="234b2-108">[**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)函式會傳回磁碟空間清單上，檔案作業中所參考之每個目標磁片磁碟機的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="234b2-108">The [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) function returns the drive specifications for each target drive referenced in the file operations on the disk-space list.</span></span> <span data-ttu-id="234b2-109">您可以使用這項資訊，以程式設計方式將這些磁片磁碟機上的可用空間與安裝所需的空間進行比較。</span><span class="sxs-lookup"><span data-stu-id="234b2-109">You can use this information to programmatically compare the available space on these drives with the space required by the installation.</span></span>

<span data-ttu-id="234b2-110">若要從磁碟空間清單中移除檔案作業，請使用 [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) 函數。</span><span class="sxs-lookup"><span data-stu-id="234b2-110">To remove a file operation from the disk-space list, use the [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) function.</span></span> <span data-ttu-id="234b2-111">若要從整個 INF 區段中移除所有檔案複製或刪除作業，請使用 [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) 或 [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) 函數。</span><span class="sxs-lookup"><span data-stu-id="234b2-111">To remove all file copy or delete operations from an entire INF section, use the [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) or [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) function.</span></span>

<span data-ttu-id="234b2-112">不再需要磁碟空間清單之後，您可以藉由呼叫 [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) 函式來釋放配置給它的資源。</span><span class="sxs-lookup"><span data-stu-id="234b2-112">After the disk-space list is no longer required, you can release the resources allocated to it by calling the [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) function.</span></span>

 

 



