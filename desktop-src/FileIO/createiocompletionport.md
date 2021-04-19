---
description: 建立輸入/輸出 (i/o) 完成埠，並將其與指定的檔案控制代碼建立關聯，或建立尚未與檔案控制代碼相關聯的 i/o 完成埠，以便於稍後建立關聯。
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: 'CreateIoCompletionPort 函式 (IoAPI) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateIoCompletionPort
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: b85ec931e740de192655ada091a990cd97180b6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979180"
---
# <a name="createiocompletionport-function"></a><span data-ttu-id="988ce-103">CreateIoCompletionPort 函式</span><span class="sxs-lookup"><span data-stu-id="988ce-103">CreateIoCompletionPort function</span></span>

<span data-ttu-id="988ce-104">建立輸入/輸出 (i/o) 完成埠，並將其與指定的檔案控制代碼建立關聯，或建立尚未與檔案控制代碼相關聯的 i/o 完成埠，以便於稍後建立關聯。</span><span class="sxs-lookup"><span data-stu-id="988ce-104">Creates an input/output (I/O) completion port and associates it with a specified file handle, or creates an I/O completion port that is not yet associated with a file handle, allowing association at a later time.</span></span>

<span data-ttu-id="988ce-105">將開啟的檔案控制代碼的實例與 i/o 完成埠相關聯，可讓進程接收與該檔案控制代碼相關之非同步 i/o 作業的完成通知。</span><span class="sxs-lookup"><span data-stu-id="988ce-105">Associating an instance of an opened file handle with an I/O completion port allows a process to receive notification of the completion of asynchronous I/O operations involving that file handle.</span></span>

> [!Note]
>
> <span data-ttu-id="988ce-106">此處所用的詞彙 *檔案控制代碼* 是指代表重迭 i/o 端點的系統抽象，而不只是磁片上的檔案。</span><span class="sxs-lookup"><span data-stu-id="988ce-106">The term *file handle* as used here refers to a system abstraction that represents an overlapped I/O endpoint, not only a file on disk.</span></span> <span data-ttu-id="988ce-107">任何支援重迭 i/o 的系統物件（例如網路端點、TCP 通訊端、具名管道和郵件位置）都可以用來做為檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="988ce-107">Any system objects that support overlapped I/O such as network endpoints, TCP sockets, named pipes, and mail slots can be used as file handles.</span></span> <span data-ttu-id="988ce-108">如需詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="988ce-108">For additional information, see the Remarks section.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="988ce-109">語法</span><span class="sxs-lookup"><span data-stu-id="988ce-109">Syntax</span></span>


```C++
HANDLE WINAPI CreateIoCompletionPort(
  _In_     HANDLE    FileHandle,
  _In_opt_ HANDLE    ExistingCompletionPort,
  _In_     ULONG_PTR CompletionKey,
  _In_     DWORD     NumberOfConcurrentThreads
);
```



## <a name="parameters"></a><span data-ttu-id="988ce-110">參數</span><span class="sxs-lookup"><span data-stu-id="988ce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="988ce-111">*FileHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="988ce-111">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="988ce-112">開啟的檔案控制代碼或 **不正確 \_ 控制碼 \_ 值**。</span><span class="sxs-lookup"><span data-stu-id="988ce-112">An open file handle or **INVALID\_HANDLE\_VALUE**.</span></span>

<span data-ttu-id="988ce-113">控制碼必須是支援重迭 i/o 的物件。</span><span class="sxs-lookup"><span data-stu-id="988ce-113">The handle must be to an object that supports overlapped I/O.</span></span>

<span data-ttu-id="988ce-114">如果有提供控制碼，它必須已針對重迭的 i/o 完成開啟。</span><span class="sxs-lookup"><span data-stu-id="988ce-114">If a handle is provided, it has to have been opened for overlapped I/O completion.</span></span> <span data-ttu-id="988ce-115">例如，使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函數取得控制碼時，您必須指定檔案 **\_ 旗 \_** 標重迭旗標。</span><span class="sxs-lookup"><span data-stu-id="988ce-115">For example, you must specify the **FILE\_FLAG\_OVERLAPPED** flag when using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function to obtain the handle.</span></span>

<span data-ttu-id="988ce-116">如果指定了 **不正確 \_ 控制碼 \_ 值** ，函式就會建立 i/o 完成埠，而不會將它與檔案控制代碼建立關聯。</span><span class="sxs-lookup"><span data-stu-id="988ce-116">If **INVALID\_HANDLE\_VALUE** is specified, the function creates an I/O completion port without associating it with a file handle.</span></span> <span data-ttu-id="988ce-117">在此情況下， *ExistingCompletionPort* 參數必須為 **Null** ，而且會忽略 *CompletionKey* 參數。</span><span class="sxs-lookup"><span data-stu-id="988ce-117">In this case, the *ExistingCompletionPort* parameter must be **NULL** and the *CompletionKey* parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="988ce-118">*ExistingCompletionPort* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="988ce-118">*ExistingCompletionPort* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="988ce-119">現有 i/o 完成埠的控制碼或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="988ce-119">A handle to an existing I/O completion port or **NULL**.</span></span>

<span data-ttu-id="988ce-120">如果這個參數指定現有的 i/o 完成通訊埠，則函式會將它與 *FileHandle* 參數所指定的控制碼產生關聯。</span><span class="sxs-lookup"><span data-stu-id="988ce-120">If this parameter specifies an existing I/O completion port, the function associates it with the handle specified by the *FileHandle* parameter.</span></span> <span data-ttu-id="988ce-121">如果成功，函數會傳回現有 i/o 完成埠的控制碼;它不會建立新的 i/o 完成通訊埠。</span><span class="sxs-lookup"><span data-stu-id="988ce-121">The function returns the handle of the existing I/O completion port if successful; it does not create a new I/O completion port.</span></span>

<span data-ttu-id="988ce-122">如果此參數為 **Null**，此函式會建立新的 i/o 完成埠，而且如果 *FileHandle* 參數有效，就會將它與新的 i/o 完成通訊埠產生關聯。</span><span class="sxs-lookup"><span data-stu-id="988ce-122">If this parameter is **NULL**, the function creates a new I/O completion port and, if the *FileHandle* parameter is valid, associates it with the new I/O completion port.</span></span> <span data-ttu-id="988ce-123">否則，就不會發生檔案控制代碼關聯。</span><span class="sxs-lookup"><span data-stu-id="988ce-123">Otherwise no file handle association occurs.</span></span> <span data-ttu-id="988ce-124">如果成功，函數會將控制碼傳回至新的 i/o 完成埠。</span><span class="sxs-lookup"><span data-stu-id="988ce-124">The function returns the handle to the new I/O completion port if successful.</span></span>

</dd> <dt>

<span data-ttu-id="988ce-125">*CompletionKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="988ce-125">*CompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="988ce-126">針對指定檔案控制代碼，每個 i/o 完成封包中包含的每個處理常式使用者定義的完成索引鍵。</span><span class="sxs-lookup"><span data-stu-id="988ce-126">The per-handle user-defined completion key that is included in every I/O completion packet for the specified file handle.</span></span> <span data-ttu-id="988ce-127">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="988ce-127">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="988ce-128">*NumberOfConcurrentThreads* \[在\]</span><span class="sxs-lookup"><span data-stu-id="988ce-128">*NumberOfConcurrentThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="988ce-129">作業系統可允許同時處理 i/o 完成埠之 i/o 完成封包的執行緒數目上限。</span><span class="sxs-lookup"><span data-stu-id="988ce-129">The maximum number of threads that the operating system can allow to concurrently process I/O completion packets for the I/O completion port.</span></span> <span data-ttu-id="988ce-130">如果 *ExistingCompletionPort* 參數不是 **Null**，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="988ce-130">This parameter is ignored if the *ExistingCompletionPort* parameter is not **NULL**.</span></span>

<span data-ttu-id="988ce-131">如果此參數為零，則系統會允許多個同時執行的執行緒，就像系統中的處理器一樣。</span><span class="sxs-lookup"><span data-stu-id="988ce-131">If this parameter is zero, the system allows as many concurrently running threads as there are processors in the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="988ce-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="988ce-132">Return value</span></span>

<span data-ttu-id="988ce-133">如果函式成功，則傳回值是 i/o 完成埠的控制碼：</span><span class="sxs-lookup"><span data-stu-id="988ce-133">If the function succeeds, the return value is the handle to an I/O completion port:</span></span>

-   <span data-ttu-id="988ce-134">如果 *ExistingCompletionPort* 參數為 **Null**，則傳回值為新的控制碼。</span><span class="sxs-lookup"><span data-stu-id="988ce-134">If the *ExistingCompletionPort* parameter was **NULL**, the return value is a new handle.</span></span>

-   <span data-ttu-id="988ce-135">如果 *ExistingCompletionPort* 參數是有效的 i/o 完成通訊埠控制碼，則傳回值會是相同的控制碼。</span><span class="sxs-lookup"><span data-stu-id="988ce-135">If the *ExistingCompletionPort* parameter was a valid I/O completion port handle, the return value is that same handle.</span></span>

-   <span data-ttu-id="988ce-136">如果 *FileHandle* 參數是有效的控制碼，該檔案控制代碼現在會與傳回的 i/o 完成埠相關聯。</span><span class="sxs-lookup"><span data-stu-id="988ce-136">If the *FileHandle* parameter was a valid handle, that file handle is now associated with the returned I/O completion port.</span></span>

<span data-ttu-id="988ce-137">如果函式失敗，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="988ce-137">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="988ce-138">若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。</span><span class="sxs-lookup"><span data-stu-id="988ce-138">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="988ce-139">備註</span><span class="sxs-lookup"><span data-stu-id="988ce-139">Remarks</span></span>

<span data-ttu-id="988ce-140">系統可以指示 i/o 系統將 i/o 完成通知封包傳送至 i/o 完成埠，以將它們排入佇列。</span><span class="sxs-lookup"><span data-stu-id="988ce-140">The I/O system can be instructed to send I/O completion notification packets to I/O completion ports, where they are queued.</span></span> <span data-ttu-id="988ce-141">**CreateIoCompletionPort** 函式會提供這種功能。</span><span class="sxs-lookup"><span data-stu-id="988ce-141">The **CreateIoCompletionPort** function provides this functionality.</span></span>

<span data-ttu-id="988ce-142">I/o 完成埠及其控制碼會與建立它的進程相關聯，而且在進程間無法共用。</span><span class="sxs-lookup"><span data-stu-id="988ce-142">An I/O completion port and its handle are associated with the process that created it and is not sharable between processes.</span></span> <span data-ttu-id="988ce-143">不過，在相同進程中的執行緒之間可共用單一控制碼。</span><span class="sxs-lookup"><span data-stu-id="988ce-143">However, a single handle is sharable between threads in the same process.</span></span>

<span data-ttu-id="988ce-144">**CreateIoCompletionPort** 可用於三種不同的模式：</span><span class="sxs-lookup"><span data-stu-id="988ce-144">**CreateIoCompletionPort** can be used in three distinct modes:</span></span>

-   <span data-ttu-id="988ce-145">只建立 i/o 完成埠，而不將它與檔案控制代碼建立關聯。</span><span class="sxs-lookup"><span data-stu-id="988ce-145">Create only an I/O completion port without associating it with a file handle.</span></span>
-   <span data-ttu-id="988ce-146">將現有的 i/o 完成埠與檔案控制代碼建立關聯。</span><span class="sxs-lookup"><span data-stu-id="988ce-146">Associate an existing I/O completion port with a file handle.</span></span>
-   <span data-ttu-id="988ce-147">在單一呼叫中執行建立和關聯。</span><span class="sxs-lookup"><span data-stu-id="988ce-147">Perform both creation and association in a single call.</span></span>

<span data-ttu-id="988ce-148">若要建立 i/o 完成埠而不建立其關聯，請將 *FileHandle* 參數設定 **為不正確 \_ 控制碼 \_ 值**、將 *ExistingCompletionPort* 參數設定為 **Null**，並將 *CompletionKey* 參數設定為零 (在此情況下會忽略) 。</span><span class="sxs-lookup"><span data-stu-id="988ce-148">To create an I/O completion port without associating it, set the *FileHandle* parameter to **INVALID\_HANDLE\_VALUE**, the *ExistingCompletionPort* parameter to **NULL**, and the *CompletionKey* parameter to zero (which is ignored in this case).</span></span> <span data-ttu-id="988ce-149">針對新的 i/o 完成通訊埠，將 *NumberOfConcurrentThreads* 參數設定為所需的並行值，或針對預設 (系統) 中的處理器數目為零。</span><span class="sxs-lookup"><span data-stu-id="988ce-149">Set the *NumberOfConcurrentThreads* parameter to the desired concurrency value for the new I/O completion port, or zero for the default (the number of processors in the system).</span></span>

<span data-ttu-id="988ce-150">在 *FileHandle* 參數中傳遞的控制碼可以是任何支援重迭 i/o 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="988ce-150">The handle passed in the *FileHandle* parameter can be any handle that supports overlapped I/O.</span></span> <span data-ttu-id="988ce-151">最常見的情況是，這是 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式使用檔案 **\_ 旗 \_** 標重迭旗標所開啟的控制碼 (例如，檔案、郵件位置和管道) 。</span><span class="sxs-lookup"><span data-stu-id="988ce-151">Most commonly, this is a handle opened by the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function using the **FILE\_FLAG\_OVERLAPPED** flag (for example, files, mail slots, and pipes).</span></span> <span data-ttu-id="988ce-152">其他函式（例如 [**通訊端**](/windows/desktop/api/winsock2/nf-winsock2-socket) ）所建立的物件也可以與 i/o 完成埠相關聯。</span><span class="sxs-lookup"><span data-stu-id="988ce-152">Objects created by other functions such as [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) can also be associated with an I/O completion port.</span></span> <span data-ttu-id="988ce-153">如需使用通訊端的範例，請參閱 [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex)。</span><span class="sxs-lookup"><span data-stu-id="988ce-153">For an example using sockets, see [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex).</span></span> <span data-ttu-id="988ce-154">控制碼只能與一個 i/o 完成埠相關聯，且在建立關聯之後，控制碼會維持與該 i/o 完成埠相關聯，直到它關閉為止。</span><span class="sxs-lookup"><span data-stu-id="988ce-154">A handle can be associated with only one I/O completion port, and after the association is made, the handle remains associated with that I/O completion port until it is closed.</span></span>

<span data-ttu-id="988ce-155">如需 i/o 完成埠理論、使用方式和相關聯函式的詳細資訊，請參閱 [I/o 完成埠](i-o-completion-ports.md)。</span><span class="sxs-lookup"><span data-stu-id="988ce-155">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="988ce-156">多個檔案控制代碼可以與單一 i/o 完成埠相關聯，方法是使用 *ExistingCompletionPort* 參數中的相同 i/o 完成埠控制碼多次呼叫 **CreateIoCompletionPort** ，以及每次 *FileHandle* 參數中的不同檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="988ce-156">Multiple file handles can be associated with a single I/O completion port by calling **CreateIoCompletionPort** multiple times with the same I/O completion port handle in the *ExistingCompletionPort* parameter and a different file handle in the *FileHandle* parameter each time.</span></span>

<span data-ttu-id="988ce-157">使用 *CompletionKey* 參數有助於您的應用程式追蹤已完成的 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="988ce-157">Use the *CompletionKey* parameter to help your application track which I/O operations have completed.</span></span> <span data-ttu-id="988ce-158">**CreateIoCompletionPort** 不會使用此值來進行功能控制;相反地，它會附加至與 i/o 完成埠關聯時，在 *FileHandle* 參數中指定的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="988ce-158">This value is not used by **CreateIoCompletionPort** for functional control; rather, it is attached to the file handle specified in the *FileHandle* parameter at the time of association with an I/O completion port.</span></span> <span data-ttu-id="988ce-159">此完成索引鍵對於每個檔案控制代碼都應該是唯一的，而且在整個內部完成佇列程式中都隨附檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="988ce-159">This completion key should be unique for each file handle, and it accompanies the file handle throughout the internal completion queuing process.</span></span> <span data-ttu-id="988ce-160">當完成封包抵達時，它會在 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函式呼叫中傳回。</span><span class="sxs-lookup"><span data-stu-id="988ce-160">It is returned in the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function call when a completion packet arrives.</span></span> <span data-ttu-id="988ce-161">[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)函式也會使用 *CompletionKey* 參數，將您自己的特殊用途完成封包排入佇列。</span><span class="sxs-lookup"><span data-stu-id="988ce-161">The *CompletionKey* parameter is also used by the [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) function to queue your own special-purpose completion packets.</span></span>

<span data-ttu-id="988ce-162">開啟控制碼的實例與 i/o 完成埠相關聯之後，就無法在 [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) 或 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) 函式中使用，因為這些函式有自己的非同步 i/o 機制。</span><span class="sxs-lookup"><span data-stu-id="988ce-162">After an instance of an open handle is associated with an I/O completion port, it cannot be used in the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function because these functions have their own asynchronous I/O mechanisms.</span></span>

<span data-ttu-id="988ce-163">最好不要使用控制碼繼承或 [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) 函式的呼叫，與 i/o 完成埠共用相關聯的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="988ce-163">It is best not to share a file handle associated with an I/O completion port by using either handle inheritance or a call to the [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) function.</span></span> <span data-ttu-id="988ce-164">使用這類重複的控制碼執行的作業會產生完成通知。</span><span class="sxs-lookup"><span data-stu-id="988ce-164">Operations performed with such duplicate handles generate completion notifications.</span></span> <span data-ttu-id="988ce-165">建議您仔細考慮。</span><span class="sxs-lookup"><span data-stu-id="988ce-165">Careful consideration is advised.</span></span>

<span data-ttu-id="988ce-166">I/o 完成通訊埠控制碼，以及與該特定 i/o 完成埠相關聯的每個檔案控制代碼，稱為 *i/o 完成埠的參考*。</span><span class="sxs-lookup"><span data-stu-id="988ce-166">The I/O completion port handle and every file handle associated with that particular I/O completion port are known as *references to the I/O completion port*.</span></span> <span data-ttu-id="988ce-167">當 i/o 完成通訊埠沒有其他參考時，就會釋放它。</span><span class="sxs-lookup"><span data-stu-id="988ce-167">The I/O completion port is released when there are no more references to it.</span></span> <span data-ttu-id="988ce-168">因此，所有這些控制碼都必須適當地關閉，才能釋放 i/o 完成埠及其相關聯的系統資源。</span><span class="sxs-lookup"><span data-stu-id="988ce-168">Therefore, all of these handles must be properly closed to release the I/O completion port and its associated system resources.</span></span> <span data-ttu-id="988ce-169">滿足這些條件之後，請呼叫 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式來關閉 i/o 完成埠控制碼。</span><span class="sxs-lookup"><span data-stu-id="988ce-169">After these conditions are satisfied, close the I/O completion port handle by calling the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="988ce-170">在 Windows 8 和 Windows Server 2012 中，下列技術支援此功能。</span><span class="sxs-lookup"><span data-stu-id="988ce-170">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="988ce-171">技術</span><span class="sxs-lookup"><span data-stu-id="988ce-171">Technology</span></span>                                           | <span data-ttu-id="988ce-172">支援</span><span class="sxs-lookup"><span data-stu-id="988ce-172">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="988ce-173">伺服器訊息區 (SMB) 3.0 通訊協定</span><span class="sxs-lookup"><span data-stu-id="988ce-173">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="988ce-174">Yes</span><span class="sxs-lookup"><span data-stu-id="988ce-174">Yes</span></span><br/> |
| <span data-ttu-id="988ce-175">SMB 3.0 透明容錯移轉 (TFO) </span><span class="sxs-lookup"><span data-stu-id="988ce-175">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="988ce-176">Yes</span><span class="sxs-lookup"><span data-stu-id="988ce-176">Yes</span></span><br/> |
| <span data-ttu-id="988ce-177">具有向外延展檔案共用的 SMB 3.0 (因此) </span><span class="sxs-lookup"><span data-stu-id="988ce-177">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="988ce-178">Yes</span><span class="sxs-lookup"><span data-stu-id="988ce-178">Yes</span></span><br/> |
| <span data-ttu-id="988ce-179">叢集共用磁碟區檔案系統 (CsvFS) </span><span class="sxs-lookup"><span data-stu-id="988ce-179">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="988ce-180">Yes</span><span class="sxs-lookup"><span data-stu-id="988ce-180">Yes</span></span><br/> |
| <span data-ttu-id="988ce-181">彈性檔案系統 (ReFS)</span><span class="sxs-lookup"><span data-stu-id="988ce-181">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="988ce-182">Yes</span><span class="sxs-lookup"><span data-stu-id="988ce-182">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="988ce-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="988ce-183">Requirements</span></span>



| <span data-ttu-id="988ce-184">需求</span><span class="sxs-lookup"><span data-stu-id="988ce-184">Requirement</span></span> | <span data-ttu-id="988ce-185">值</span><span class="sxs-lookup"><span data-stu-id="988ce-185">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="988ce-186">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="988ce-186">Minimum supported client</span></span><br/> | <span data-ttu-id="988ce-187">Windows XP \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="988ce-187">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="988ce-188">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="988ce-188">Minimum supported server</span></span><br/> | <span data-ttu-id="988ce-189">Windows Server 2003 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="988ce-189">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="988ce-190">標頭</span><span class="sxs-lookup"><span data-stu-id="988ce-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="988ce-191"><dt>IoAPI (包含 Windows .h) ;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP (的 WinBase，包括 windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="988ce-191"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="988ce-192">程式庫</span><span class="sxs-lookup"><span data-stu-id="988ce-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="988ce-193"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="988ce-193"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="988ce-194">DLL</span><span class="sxs-lookup"><span data-stu-id="988ce-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="988ce-195"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="988ce-195"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="988ce-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="988ce-196">See also</span></span>

<dl> <dt>

<span data-ttu-id="988ce-197">**總覽主題**</span><span class="sxs-lookup"><span data-stu-id="988ce-197">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="988ce-198">檔案管理功能</span><span class="sxs-lookup"><span data-stu-id="988ce-198">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="988ce-199">I/o 完成埠</span><span class="sxs-lookup"><span data-stu-id="988ce-199">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="988ce-200">使用 Windows 標頭</span><span class="sxs-lookup"><span data-stu-id="988ce-200">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

[<span data-ttu-id="988ce-201">Windows 通訊端2</span><span class="sxs-lookup"><span data-stu-id="988ce-201">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

<span data-ttu-id="988ce-202">**函數**</span><span class="sxs-lookup"><span data-stu-id="988ce-202">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="988ce-203">**AcceptEx**</span><span class="sxs-lookup"><span data-stu-id="988ce-203">**AcceptEx**</span></span>](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[<span data-ttu-id="988ce-204">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="988ce-204">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="988ce-205">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="988ce-205">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="988ce-206">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="988ce-206">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="988ce-207">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="988ce-207">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="988ce-208">**PostQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="988ce-208">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="988ce-209">**ReadFileEx**</span><span class="sxs-lookup"><span data-stu-id="988ce-209">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="988ce-210">**WriteFileEx**</span><span class="sxs-lookup"><span data-stu-id="988ce-210">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

