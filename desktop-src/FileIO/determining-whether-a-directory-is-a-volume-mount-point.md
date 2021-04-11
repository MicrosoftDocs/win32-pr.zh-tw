---
description: 如何判斷指定的目錄是否為裝載的資料夾。
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: 判斷目錄是否為裝載的資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7492a3114ff0c9c9ce0685c6d3e2b94724457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851580"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a><span data-ttu-id="add6e-103">判斷目錄是否為裝載的資料夾</span><span class="sxs-lookup"><span data-stu-id="add6e-103">Determining Whether a Directory Is a Mounted Folder</span></span>

<span data-ttu-id="add6e-104">例如，當您使用僅限一個磁片區的備份或搜尋應用程式時，判斷目錄是否為掛接的資料夾會很有用。</span><span class="sxs-lookup"><span data-stu-id="add6e-104">It is useful to determine whether a directory is a mounted folder when, for example, you are using a backup or search application that is limited to one volume.</span></span> <span data-ttu-id="add6e-105">如果您使用 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 之類的函式來為應用程式所限制的磁片區上的其他磁片區建立掛接的資料夾，則這類應用程式可以觸及多個磁片區的資訊。</span><span class="sxs-lookup"><span data-stu-id="add6e-105">Such an application can reach information on multiple volumes if you use functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) to create mounted folders for the other volumes on the volume that the application is limited to.</span></span> <span data-ttu-id="add6e-106">如需詳細資訊，請參閱 [建立裝載的資料夾](mounting-and-dismounting-a-volume.md)。</span><span class="sxs-lookup"><span data-stu-id="add6e-106">For more information, see [Creating Mounted Folders](mounting-and-dismounting-a-volume.md).</span></span>

<span data-ttu-id="add6e-107">若要判斷指定的目錄是否為裝載的資料夾，請先呼叫 [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) 函式，並檢查傳回值中的 **檔案屬性重新 \_ \_ 分析 \_ 點** 旗標，以查看目錄是否有相關聯的重新分析點。</span><span class="sxs-lookup"><span data-stu-id="add6e-107">To determine if a specified directory is a mounted folder, first call the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function and inspect the **FILE\_ATTRIBUTE\_REPARSE\_POINT** flag in the return value to see if the directory has an associated reparse point.</span></span> <span data-ttu-id="add6e-108">如果有的話，請使用 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)和 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)函數來取得 [**WIN32 \_ FIND \_ 資料**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa)結構的 **dwReserved0** 成員中的重新分析標記。</span><span class="sxs-lookup"><span data-stu-id="add6e-108">If it does, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) functions to obtain the reparse tag in the **dwReserved0** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="add6e-109">若要判斷重新分析點是否為掛接的資料夾 (而不是其他形式的重新分析點) ，請測試標記值是否等於值 **IO 重新 \_ 分析 \_ 標記 \_ 裝入 \_ 點**。</span><span class="sxs-lookup"><span data-stu-id="add6e-109">To determine if the reparse point is a mounted folder (and not some other form of reparse point), test whether the tag value equals the value **IO\_REPARSE\_TAG\_MOUNT\_POINT**.</span></span> <span data-ttu-id="add6e-110">如需詳細資訊，請參閱重新 [分析點](reparse-points.md)。</span><span class="sxs-lookup"><span data-stu-id="add6e-110">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="add6e-111">若要取得裝載資料夾的目標磁片區，請使用 [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) 函式。</span><span class="sxs-lookup"><span data-stu-id="add6e-111">To obtain the target volume of a mounted folder, use the [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) function.</span></span>

<span data-ttu-id="add6e-112">您可以使用類似的方式，藉由測試標記值是否為 **IO 重新 \_ 分析 \_ 標記 \_** 的符號連結，判斷重新分析點是否為符號連結。</span><span class="sxs-lookup"><span data-stu-id="add6e-112">In a similar manner, you can determine if a reparse point is a symbolic link by testing whether the tag value is **IO\_REPARSE\_TAG\_SYMLINK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="add6e-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="add6e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="add6e-114">**檔案屬性常數**</span><span class="sxs-lookup"><span data-stu-id="add6e-114">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 



