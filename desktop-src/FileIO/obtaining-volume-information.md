---
description: 存取指定磁片區上的檔案和目錄之前，您應該使用 GetVolumeInformation 函式來判斷檔案系統的功能。
ms.assetid: 008e0cc4-bc12-47e8-a8b7-d4fa9395fceb
title: 取得磁片區資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc5323c3f82db1115a81902f156e9366abad31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512024"
---
# <a name="obtaining-volume-information"></a><span data-ttu-id="3c104-103">取得磁片區資訊</span><span class="sxs-lookup"><span data-stu-id="3c104-103">Obtaining Volume Information</span></span>

<span data-ttu-id="3c104-104">[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)函式會取得指定磁片區上檔案系統的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3c104-104">The [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function retrieves information about the file system on a given volume.</span></span> <span data-ttu-id="3c104-105">這項資訊包括磁片區名稱、磁片區序號、檔案系統名稱、檔案系統旗標、檔案名的最大長度等等。</span><span class="sxs-lookup"><span data-stu-id="3c104-105">This information includes the volume name, volume serial number, file system name, file system flags, maximum length of a file name, and so on.</span></span> <span data-ttu-id="3c104-106">存取指定磁片區上的檔案和目錄之前，您應該使用 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式來判斷檔案系統的功能。</span><span class="sxs-lookup"><span data-stu-id="3c104-106">Before you access files and directories on a given volume, you should determine the capabilities of the file system by using the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function.</span></span> <span data-ttu-id="3c104-107">此函式會傳回值，您可以使用這些值來調整應用程式，以有效地與檔案系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="3c104-107">This function returns values that you can use to adapt your application to work effectively with the file system.</span></span>

<span data-ttu-id="3c104-108">一般而言，您應該避免使用靜態緩衝區作為檔案名和路徑。</span><span class="sxs-lookup"><span data-stu-id="3c104-108">In general, you should avoid using static buffers for file names and paths.</span></span> <span data-ttu-id="3c104-109">相反地，請使用 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 傳回的值，以在需要時配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3c104-109">Instead, use the values returned by [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) to allocate buffers as you need them.</span></span> <span data-ttu-id="3c104-110">如果您必須使用靜態緩衝區，請保留256個字元的檔案名和260個字元的路徑。</span><span class="sxs-lookup"><span data-stu-id="3c104-110">If you must use static buffers, reserve 256 characters for file names and 260 characters for paths.</span></span>

<span data-ttu-id="3c104-111">[**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)和 [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)函式會分別取出系統目錄和 Windows 目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="3c104-111">The [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) and [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) functions retrieve the paths to the system directory and the Windows directory, respectively.</span></span>

<span data-ttu-id="3c104-112">[**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)函式會抓取有關磁片區的組織資訊，包括每個磁區的位元組數目、每個叢集的磁區數目、可用叢集的數目，以及叢集總數。</span><span class="sxs-lookup"><span data-stu-id="3c104-112">The [**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea) function retrieves organizational information about a volume, including the number of bytes per sector, the number of sectors per cluster, the number of free clusters, and the total number of clusters.</span></span> <span data-ttu-id="3c104-113">不過， **GetDiskFreeSpace** 無法報告大於 2 GB 的磁片區大小。</span><span class="sxs-lookup"><span data-stu-id="3c104-113">However, **GetDiskFreeSpace** cannot report volume sizes that are greater than 2 GB.</span></span> <span data-ttu-id="3c104-114">若要確保您的應用程式能與大型容量硬碟搭配運作，請使用 [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) 函式。</span><span class="sxs-lookup"><span data-stu-id="3c104-114">To ensure that your application works with large capacity hard drives, use the [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) function.</span></span>

<span data-ttu-id="3c104-115">[**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea)函式會指出指定的磁碟機號所參照的磁片區是卸載式、固定、CD-ROM、RAM 或網路磁碟機機。</span><span class="sxs-lookup"><span data-stu-id="3c104-115">The [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) function indicates whether the volume referenced by the specified drive letter is a removable, fixed, CD-ROM, RAM, or network drive.</span></span>

<span data-ttu-id="3c104-116">[**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives)函式會識別目前的磁片區。</span><span class="sxs-lookup"><span data-stu-id="3c104-116">The [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) function identifies the volumes present.</span></span> <span data-ttu-id="3c104-117">[**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw)函式會針對存在的每個磁片區，抓取以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="3c104-117">The [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw) function retrieves a null-terminated string for each volume present.</span></span> <span data-ttu-id="3c104-118">當需要根目錄時，請使用這些字串。</span><span class="sxs-lookup"><span data-stu-id="3c104-118">Use these strings whenever a root directory is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c104-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c104-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c104-120">檔案系統識別</span><span class="sxs-lookup"><span data-stu-id="3c104-120">File System Recognition</span></span>](file-system-recognition.md)
</dt> </dl>

 

 
