---
description: 當使用 CreateFile 函式的進程開啟檔案時，檔案控制代碼會與其相關聯，直到進程終止或使用 CloseHandle 函數關閉控制碼為止。
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: 檔案控制代碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a54db1935108ab18666fb460a071d77c50f793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852128"
---
# <a name="file-handles"></a><span data-ttu-id="3d1cf-103">檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="3d1cf-103">File Handles</span></span>

<span data-ttu-id="3d1cf-104">當使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式的進程開啟檔案時， *檔案控制代碼* 會與其相關聯，直到進程終止或使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函數關閉控制碼為止。</span><span class="sxs-lookup"><span data-stu-id="3d1cf-104">When a file is opened by a process using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, a *file handle* is associated with it until either the process terminates or the handle is closed using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="3d1cf-105">檔案控制代碼用來識別許多函式呼叫中的檔案。</span><span class="sxs-lookup"><span data-stu-id="3d1cf-105">The file handle is used to identify the file in many function calls.</span></span>

<span data-ttu-id="3d1cf-106">每個檔案控制代碼和檔案物件通常都是開啟檔案的每個處理常式所特有的，唯一的例外是當處理常式所持有的檔案控制代碼重複，或子進程繼承父進程的檔案控制代碼時。</span><span class="sxs-lookup"><span data-stu-id="3d1cf-106">Each file handle and file object is generally unique to each process that opens a file—the only exceptions to this are when a file handle held by a process is duplicated, or when a child process inherits the file handles of the parent process.</span></span> <span data-ttu-id="3d1cf-107">在這些情況下，這些檔案控制代碼是唯一的，但會看到單一的共用檔案物件。</span><span class="sxs-lookup"><span data-stu-id="3d1cf-107">In these situations, these file handles are unique, but see a single, shared file object.</span></span> <span data-ttu-id="3d1cf-108">如需有關複製進程所持有之檔案控制代碼的詳細資訊，請參閱 [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) 。</span><span class="sxs-lookup"><span data-stu-id="3d1cf-108">See [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) for more information on duplicating file handles held by processes.</span></span>

<span data-ttu-id="3d1cf-109">請注意，雖然檔案控制代碼通常是處理常式的私用，但檔案處理的檔案資料則不是。</span><span class="sxs-lookup"><span data-stu-id="3d1cf-109">Note that while the file handles are typically private to a process, the file data that the file handles point to is not.</span></span> <span data-ttu-id="3d1cf-110">因此，共用相同檔案的進程和執行緒必須同步處理其存取。</span><span class="sxs-lookup"><span data-stu-id="3d1cf-110">Therefore, processes and threads that share the same file must synchronize their access.</span></span> <span data-ttu-id="3d1cf-111">針對檔案的大部分作業，進程會透過其私用的控制碼集區來識別該檔案。</span><span class="sxs-lookup"><span data-stu-id="3d1cf-111">For most operations on a file, a process identifies the file through its private pool of handles.</span></span>

 

 
