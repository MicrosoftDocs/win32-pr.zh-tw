---
description: 用來建立、刪除和維護檔案的函數。
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: 建立、刪除和維護檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921388e84ac44a42e0c24880b1b56971ba84c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984711"
---
# <a name="creating-deleting-and-maintaining-files"></a><span data-ttu-id="08ac4-103">建立、刪除和維護檔案</span><span class="sxs-lookup"><span data-stu-id="08ac4-103">Creating, Deleting, and Maintaining Files</span></span>

<span data-ttu-id="08ac4-104">下列主題描述如何建立、刪除和維護檔案。</span><span class="sxs-lookup"><span data-stu-id="08ac4-104">The following topics describe how to create, delete, and maintain files.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="08ac4-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="08ac4-105">In this section</span></span>



| <span data-ttu-id="08ac4-106">主題</span><span class="sxs-lookup"><span data-stu-id="08ac4-106">Topic</span></span>                                                                   | <span data-ttu-id="08ac4-107">描述</span><span class="sxs-lookup"><span data-stu-id="08ac4-107">Description</span></span>                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08ac4-108">命名檔案、路徑和命名空間</span><span class="sxs-lookup"><span data-stu-id="08ac4-108">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)<br/>     | <span data-ttu-id="08ac4-109">檔案和目錄名稱的規則、慣例和限制，包括命名慣例、簡短檔案名與完整檔案名、完整路徑與相對路徑、最大路徑長度限制、8.3 檔案名和命名空間。</span><span class="sxs-lookup"><span data-stu-id="08ac4-109">Rules, conventions, and limitations of names for files and directories, including naming conventions, short file names vs. long file names, fully qualified paths vs. relative paths, maximum path length limitation, 8.3 file names, and namespaces.</span></span><br/>            |
| [<span data-ttu-id="08ac4-110">建立和開啟檔案</span><span class="sxs-lookup"><span data-stu-id="08ac4-110">Creating and Opening Files</span></span>](creating-and-opening-files.md)<br/> | <span data-ttu-id="08ac4-111">使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函數建立或開啟檔案的考慮。</span><span class="sxs-lookup"><span data-stu-id="08ac4-111">Considerations for creating or opening a file by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="08ac4-112">移動和取代檔案</span><span class="sxs-lookup"><span data-stu-id="08ac4-112">Moving and Replacing Files</span></span>](moving-and-replacing-files.md)<br/> | <span data-ttu-id="08ac4-113">使用 CopyFileEx、CreateFile、Replacefile 和 MoveFileEx 函數移動和取代檔案的考慮。</span><span class="sxs-lookup"><span data-stu-id="08ac4-113">Considerations for moving and replacing files by using the CopyFileEx, CreateFile, Replacefile, and MoveFileEx functions.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="08ac4-114">關閉和刪除檔案</span><span class="sxs-lookup"><span data-stu-id="08ac4-114">Closing and Deleting Files</span></span>](closing-and-deleting-files.md)<br/> | <span data-ttu-id="08ac4-115">若要有效率地使用作業系統資源，應用程式應該在不再需要使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式時關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="08ac4-115">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="08ac4-116">如果在應用程式終止時開啟檔案，系統會自動將它關閉。</span><span class="sxs-lookup"><span data-stu-id="08ac4-116">If a file is open when an application terminates, the system closes it automatically.</span></span><br/> |
| [<span data-ttu-id="08ac4-117">磁碟重組檔案</span><span class="sxs-lookup"><span data-stu-id="08ac4-117">Defragmenting Files</span></span>](defragmenting-files.md)<br/>               | <span data-ttu-id="08ac4-118">*磁碟重組* 是指將檔案的部分移到磁片上以重組檔案的程式，也就是在磁片上移動檔案叢集以使其成為連續的進程。</span><span class="sxs-lookup"><span data-stu-id="08ac4-118">*Defragmentation* is the process of moving portions of files around on a disk to defragment files, that is, the process of moving file clusters on a disk to make them contiguous.</span></span><br/>                                                                               |



 

 

