---
description: 用來取得和設定檔案資訊的函式。
ms.assetid: 3b5fb709-c699-4651-8072-97210c8cf763
title: 取得和設定檔案資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c6eb6abf2554e1945e0782c667245ea0eaa99be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852796"
---
# <a name="obtaining-and-setting-file-information"></a><span data-ttu-id="71dee-103">取得和設定檔案資訊</span><span class="sxs-lookup"><span data-stu-id="71dee-103">Obtaining and Setting File Information</span></span>

<span data-ttu-id="71dee-104">下列主題描述如何取得和設定檔案資訊。</span><span class="sxs-lookup"><span data-stu-id="71dee-104">The following topics describe how to get and set file information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="71dee-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="71dee-105">In this section</span></span>



| <span data-ttu-id="71dee-106">主題</span><span class="sxs-lookup"><span data-stu-id="71dee-106">Topic</span></span>                                                                                                             | <span data-ttu-id="71dee-107">描述</span><span class="sxs-lookup"><span data-stu-id="71dee-107">Description</span></span>                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71dee-108">正在取出檔案類型資訊</span><span class="sxs-lookup"><span data-stu-id="71dee-108">Retrieving File Type Information</span></span>](retrieving-file-type-information.md)<br/>                               | <span data-ttu-id="71dee-109">[**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)函式會抓取檔案的類型：磁片、字元 (例如主控台) 、管道或不明。</span><span class="sxs-lookup"><span data-stu-id="71dee-109">The [**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype) function retrieves the type of a file: disk, character (such as a console), pipe, or unknown.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="71dee-110">判斷檔案的大小</span><span class="sxs-lookup"><span data-stu-id="71dee-110">Determining the Size of a File</span></span>](determining-the-size-of-a-file.md)<br/>                                   | <span data-ttu-id="71dee-111">[**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)函式會捕獲檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="71dee-111">The [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function retrieves the size of a file.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="71dee-112">搜尋一個或多個檔案</span><span class="sxs-lookup"><span data-stu-id="71dee-112">Searching for One or More Files</span></span>](searching-for-one-or-more-files.md)<br/>                                 | <span data-ttu-id="71dee-113">應用程式可以使用 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)、 [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)、 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)和 [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) 函數，在目前的目錄中搜尋符合指定模式的所有檔案名。</span><span class="sxs-lookup"><span data-stu-id="71dee-113">An application can search the current directory for all file names that match a given pattern by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span><br/> |
| [<span data-ttu-id="71dee-114">設定和取得檔案的時間戳記</span><span class="sxs-lookup"><span data-stu-id="71dee-114">Setting and Getting the Timestamp of a File</span></span>](setting-and-getting-the-timestamp-of-a-file.md)<br/>         | <span data-ttu-id="71dee-115">應用程式可以使用 [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) 和 [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) 函式來取得和設定檔案的建立日期和時間、上次修改時間或上次存取的時間。</span><span class="sxs-lookup"><span data-stu-id="71dee-115">Applications can retrieve and set the date and time a file is created, last modified, or last accessed by using the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) and [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) functions.</span></span><br/>                                                                         |
| [<span data-ttu-id="71dee-116">判斷目前的字元集字碼頁</span><span class="sxs-lookup"><span data-stu-id="71dee-116">Determining the Current Character Set Code Page</span></span>](determining-the-current-character-set-code-page.md)<br/> | <span data-ttu-id="71dee-117">[**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi)函式會判斷檔案 i/o 函數是否使用 ANSI 或 OEM 字元集字碼頁。</span><span class="sxs-lookup"><span data-stu-id="71dee-117">The [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) function determines whether the file I/O functions are using the ANSI or OEM character set code page.</span></span><br/>                                                                                                                               |



 

 

