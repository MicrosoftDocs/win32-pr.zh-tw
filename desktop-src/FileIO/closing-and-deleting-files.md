---
description: 若要有效率地使用作業系統資源，應用程式應該在不再需要使用 CloseHandle 函式時關閉檔案。 如果在應用程式終止時開啟檔案，系統會自動將它關閉。
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: 關閉和刪除檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3da31fe7ff38a1bbd1555e2685ceab9ae432574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987360"
---
# <a name="closing-and-deleting-files"></a><span data-ttu-id="8f7c6-104">關閉和刪除檔案</span><span class="sxs-lookup"><span data-stu-id="8f7c6-104">Closing and Deleting Files</span></span>

<span data-ttu-id="8f7c6-105">若要有效率地使用作業系統資源，應用程式應該在不再需要使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式時關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="8f7c6-105">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="8f7c6-106">如果在應用程式終止時開啟檔案，系統會自動將它關閉。</span><span class="sxs-lookup"><span data-stu-id="8f7c6-106">If a file is open when an application terminates, the system closes it automatically.</span></span>

<span data-ttu-id="8f7c6-107">[**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)函式可以在關閉時用來刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="8f7c6-107">The [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function can be used to delete a file on close.</span></span> <span data-ttu-id="8f7c6-108">您必須先關閉檔案的所有控制碼，才能刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="8f7c6-108">A file cannot be deleted until all handles to it are closed.</span></span> <span data-ttu-id="8f7c6-109">如果無法刪除檔案，則無法重複使用其名稱。</span><span class="sxs-lookup"><span data-stu-id="8f7c6-109">If a file cannot be deleted, its name cannot be reused.</span></span> <span data-ttu-id="8f7c6-110">若要立即重複使用檔案名，請重新命名現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="8f7c6-110">To reuse a file name immediately, rename the existing file.</span></span>

<span data-ttu-id="8f7c6-111">如果您要在遠端電腦上刪除開啟的檔案或目錄，但在遠端電腦上已開啟該檔案或目錄，但未設定「讀取共用」許可權，請不要呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 或 [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) 來開啟檔案或目錄以供先刪除。</span><span class="sxs-lookup"><span data-stu-id="8f7c6-111">If you are deleting an open file or directory on a remote machine and it has already been opened on the remote machine without the read share permission set, do not call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) to open the file or directory for deletion first.</span></span> <span data-ttu-id="8f7c6-112">這麼做會導致共用違規。</span><span class="sxs-lookup"><span data-stu-id="8f7c6-112">Doing so will result in a sharing violation.</span></span>

 

 
