---
description: 應用程式可以使用 GetFileTime 和 SetFileTime 函式來取得和設定檔案的建立日期和時間、上次修改時間或上次存取的時間。
ms.assetid: f8930be6-7c2a-4e50-a7a1-d25f6e2a3951
title: 設定和取得檔案的時間戳記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34735994dd3017662f517a8c0a57be1d5c0e3096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191512"
---
# <a name="setting-and-getting-the-timestamp-of-a-file"></a><span data-ttu-id="ce1eb-103">設定和取得檔案的時間戳記</span><span class="sxs-lookup"><span data-stu-id="ce1eb-103">Setting and Getting the Timestamp of a File</span></span>

<span data-ttu-id="ce1eb-104">應用程式可以使用 [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) 和 [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) 函式來取得和設定檔案的建立日期和時間、上次修改時間或上次存取的時間。</span><span class="sxs-lookup"><span data-stu-id="ce1eb-104">Applications can retrieve and set the date and time a file is created, last modified, or last accessed by using the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) and [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) functions.</span></span> <span data-ttu-id="ce1eb-105">如需詳細資訊，請參閱檔案 [時間](/windows/desktop/SysInfo/file-times)。</span><span class="sxs-lookup"><span data-stu-id="ce1eb-105">For more information, see [File Times](/windows/desktop/SysInfo/file-times).</span></span>

> [!Note]  
> <span data-ttu-id="ce1eb-106">並非所有檔案系統都可以記錄建立和上次存取時間，而且並非所有檔案系統都會以相同的方式記錄它們。</span><span class="sxs-lookup"><span data-stu-id="ce1eb-106">Not all file systems can record creation and last access times, and not all file systems record them in the same manner.</span></span> <span data-ttu-id="ce1eb-107">例如，在 FAT 檔案系統上，建立時間的解析度為10毫秒、寫入時間的解析度為2秒，而存取時間的解析為1天 (真的是存取日期) 。</span><span class="sxs-lookup"><span data-stu-id="ce1eb-107">For example, on FAT file system, create time has a resolution of 10 milliseconds, write time has a resolution of 2 seconds, and access time has a resolution of 1 day (really, the access date).</span></span> <span data-ttu-id="ce1eb-108">NTFS 檔案系統會在上次存取後的最多一小時內，延遲檔案上次存取時間的更新。</span><span class="sxs-lookup"><span data-stu-id="ce1eb-108">The NTFS file system delays update to the last access time for a file by up to one hour after the last access.</span></span>

 

 

 
