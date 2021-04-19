---
description: 用來列舉磁片區上所裝載之資料夾的函式。
ms.assetid: 052a363f-adfd-4f66-a8b0-5d9d37eedcb0
title: 列舉裝載的資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29585100a4b8a94e1b7b78d36b6f0fda228094d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984213"
---
# <a name="enumerating-mounted-folders"></a><span data-ttu-id="53738-103">列舉裝載的資料夾</span><span class="sxs-lookup"><span data-stu-id="53738-103">Enumerating Mounted Folders</span></span>

<span data-ttu-id="53738-104">下列函式可用來列舉指定 NTFS 磁片區上的已掛接資料夾：</span><span class="sxs-lookup"><span data-stu-id="53738-104">The following functions are used to enumerate the mounted folders on a specified NTFS volume:</span></span>

-   [<span data-ttu-id="53738-105">**FindFirstVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="53738-105">**FindFirstVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [<span data-ttu-id="53738-106">**FindNextVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="53738-106">**FindNextVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [<span data-ttu-id="53738-107">**FindVolumeMountPointClose**</span><span class="sxs-lookup"><span data-stu-id="53738-107">**FindVolumeMountPointClose**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)

<span data-ttu-id="53738-108">這些函式的運作方式非常類似 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)、 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)和 [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) 函數。</span><span class="sxs-lookup"><span data-stu-id="53738-108">These functions operate in a manner very similar to the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span>

<span data-ttu-id="53738-109">若要列舉磁片區上裝載的資料夾，請先找出磁片區是否支援掛接的資料夾。</span><span class="sxs-lookup"><span data-stu-id="53738-109">To enumerate mounted folders on a volume, first find out if the volume supports mounted folders.</span></span> <span data-ttu-id="53738-110">若要這樣做，請使用 [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) 和 [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) 函數所傳回的磁片區名稱來呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式。</span><span class="sxs-lookup"><span data-stu-id="53738-110">To do so, use the volume name returned by the [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) and [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) functions to call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function.</span></span> <span data-ttu-id="53738-111">傳回的名稱會包含尾端的反斜線 (\) ，以與 [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) 函式和相關函數相容。</span><span class="sxs-lookup"><span data-stu-id="53738-111">The names returned include a trailing backslash (\) to be compatible with the [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) function and related functions.</span></span> <span data-ttu-id="53738-112">如需有關用來掃描電腦上磁片區之函式的詳細資訊，請參閱 [列舉磁片](enumerating-volumes.md)區。</span><span class="sxs-lookup"><span data-stu-id="53738-112">For more information on the functions used to scan the volumes on a computer, see [Enumerating Volumes](enumerating-volumes.md).</span></span> <span data-ttu-id="53738-113">當您呼叫 **GetVolumeInformation** 函式時，如果 *lpFileSystemNameBuffer* 參數中傳回 "NTFS"，則磁片區是 NTFS 磁片區。</span><span class="sxs-lookup"><span data-stu-id="53738-113">When you call the **GetVolumeInformation** function, if "NTFS" is returned in the *lpFileSystemNameBuffer* parameter, the volume is an NTFS volume.</span></span> <span data-ttu-id="53738-114">NTFS 檔案系統支援裝載的資料夾。</span><span class="sxs-lookup"><span data-stu-id="53738-114">The NTFS file system supports mounted folders.</span></span>

<span data-ttu-id="53738-115">如果磁片區是 NTFS 磁片區，請呼叫 [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)來開始搜尋裝載的資料夾。</span><span class="sxs-lookup"><span data-stu-id="53738-115">If the volume is an NTFS volume, begin a search for the mounted folders by calling [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).</span></span> <span data-ttu-id="53738-116">如果搜尋成功，請根據您的應用程式需求來處理結果。</span><span class="sxs-lookup"><span data-stu-id="53738-116">If the search is successful, process the results according to your application's requirements.</span></span> <span data-ttu-id="53738-117">然後在迴圈中使用 [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa) ，以一次尋找並處理一個掛接的資料夾。</span><span class="sxs-lookup"><span data-stu-id="53738-117">Then use [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa) in a loop to locate and process the mounted folders one at a time.</span></span> <span data-ttu-id="53738-118">如果沒有其他已載入的資料夾要列舉，請呼叫 [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)來關閉搜尋控制碼。</span><span class="sxs-lookup"><span data-stu-id="53738-118">When there are no more mounted folders to be enumerated, close the search handle by calling [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose).</span></span> <span data-ttu-id="53738-119">請注意，搜尋只會尋找指定磁片區上所裝載的資料夾。</span><span class="sxs-lookup"><span data-stu-id="53738-119">Note that the search will find only the mounted folders that are on the specified volume.</span></span>

<span data-ttu-id="53738-120">您不應該假設這些函式所傳回的已掛接資料夾順序與其他函式或工具傳回的裝載資料夾順序之間的任何關聯性。</span><span class="sxs-lookup"><span data-stu-id="53738-120">You should not assume any correlation between the order of the mounted folders that are returned by these functions and the order of the mounted folders that are returned by other functions or tools.</span></span>

 

 



