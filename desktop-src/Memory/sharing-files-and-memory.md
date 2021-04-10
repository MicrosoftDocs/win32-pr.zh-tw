---
description: 檔案對應可以用來在兩個或多個進程之間共用檔案或記憶體。 若要共用檔案或記憶體，所有進程都必須使用相同檔案對應物件的名稱或控制碼。
ms.assetid: 942cb50d-df07-444f-bba5-58194556ae66
title: 共用檔案和記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d402eba3f87f1f799593ae0d6b23fba06124a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690540"
---
# <a name="sharing-files-and-memory"></a><span data-ttu-id="3bcb2-104">共用檔案和記憶體</span><span class="sxs-lookup"><span data-stu-id="3bcb2-104">Sharing Files and Memory</span></span>

<span data-ttu-id="3bcb2-105">檔案對應可以用來在兩個或多個進程之間共用檔案或記憶體。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-105">File mapping can be used to share a file or memory between two or more processes.</span></span> <span data-ttu-id="3bcb2-106">若要共用檔案或記憶體，所有進程都必須使用相同檔案對應物件的名稱或控制碼。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-106">To share a file or memory, all of the processes must use the name or the handle of the same file mapping object.</span></span>

<span data-ttu-id="3bcb2-107">為了共用檔案，第一個進程會使用 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) 函數來建立或開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-107">To share a file, the first process creates or opens a file by using the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="3bcb2-108">接著，它會使用 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) 函式來建立檔案對應物件，並指定檔案控制代碼和檔案對應物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-108">Next, it creates a file mapping object by using the [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) function, specifying the file handle and a name for the file mapping object.</span></span> <span data-ttu-id="3bcb2-109">事件、信號、mutex、可等候計時器、作業和檔案對應物件的名稱會共用相同的命名空間。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-109">The names of event, semaphore, mutex, waitable timer, job, and file mapping objects share the same namespace.</span></span> <span data-ttu-id="3bcb2-110">因此，如果 **CreateFileMapping** 和 [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) 函式指定的名稱是由其他類型的物件所使用，則這些函數會失敗。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-110">Therefore, the **CreateFileMapping** and [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) functions fail if they specify a name that is in use by an object of another type.</span></span>

<span data-ttu-id="3bcb2-111">若要共用與檔案沒有關聯的記憶體，處理常式必須使用 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) 函式，並將不正確 \_ 控制碼 \_ 值指定為 *hFile* 參數，而不是現有的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-111">To share memory that is not associated with a file, a process must use the [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) function and specify INVALID\_HANDLE\_VALUE as the *hFile* parameter instead of an existing file handle.</span></span> <span data-ttu-id="3bcb2-112">對應的檔案對應物件會存取系統分頁檔案所支援的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-112">The corresponding file mapping object accesses memory backed by the system paging file.</span></span> <span data-ttu-id="3bcb2-113">當您 \_ \_ 在呼叫 **CreateFileMapping** 時指定了不正確控制碼值 hFile 時，您必須指定大於零的大小。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-113">You must specify a size greater than zero when you specify an *hFile* of INVALID\_HANDLE\_VALUE in a call to **CreateFileMapping**.</span></span>

<span data-ttu-id="3bcb2-114">若要讓其他進程取得第一個進程所建立之檔案對應物件的控制碼，最簡單的方式是使用 [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) 函式，並指定物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-114">The easiest way for other processes to obtain a handle of the file mapping object created by the first process is to use the [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) function and specify the object's name.</span></span> <span data-ttu-id="3bcb2-115">這稱為「 *共用記憶體*」。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-115">This is referred to as *named shared memory*.</span></span> <span data-ttu-id="3bcb2-116">如果檔案對應物件沒有名稱，則處理常式必須透過繼承或重複來取得它的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-116">If the file mapping object does not have a name, the process must obtain a handle to it through inheritance or duplication.</span></span> <span data-ttu-id="3bcb2-117">如需繼承和重複的詳細資訊，請參閱 [繼承](../procthread/inheritance.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-117">For more information on inheritance and duplication, see [Inheritance](../procthread/inheritance.md).</span></span>

<span data-ttu-id="3bcb2-118">共用檔案或記憶體的進程必須使用 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) 或 [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) 函數來建立檔案。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-118">Processes that share files or memory must create file views by using the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) or [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) function.</span></span> <span data-ttu-id="3bcb2-119">它們必須使用信號、mutex、事件或其他其他互斥技巧來協調其存取。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-119">They must coordinate their access using semaphores, mutexes, events, or some other mutual exclusion technique.</span></span> <span data-ttu-id="3bcb2-120">如需詳細資訊，請參閱 [同步](../sync/synchronization.md)處理。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-120">For more information, see [Synchronization](../sync/synchronization.md).</span></span>

<span data-ttu-id="3bcb2-121">除非使用 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 函式，否則共用檔案對應物件將不會被終結，直到使用它的所有進程關閉其控制碼為止。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-121">A shared file mapping object will not be destroyed until all processes that use it close their handles to it by using the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="3bcb2-122">如需檔案對應物件安全性的詳細資訊，請參閱檔案 [對應安全性和存取權限](file-mapping-security-and-access-rights.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcb2-122">For information about file mapping object security, see [File Mapping Security and Access Rights](file-mapping-security-and-access-rights.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bcb2-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="3bcb2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bcb2-124">建立命名的共用記憶體</span><span class="sxs-lookup"><span data-stu-id="3bcb2-124">Creating Named Shared Memory</span></span>](creating-named-shared-memory.md)
</dt> </dl>

 

 
