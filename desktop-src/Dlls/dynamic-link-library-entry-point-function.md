---
description: DLL 可以選擇性地指定進入點函數。
ms.assetid: ec035fc6-0a6f-4e52-a4cc-8d7a25a94366
title: Dynamic-Link 程式庫 Entry-Point 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62bff557bfa2aa792b420e8fe1856bbe0726921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691564"
---
# <a name="dynamic-link-library-entry-point-function"></a><span data-ttu-id="1abbf-103">Dynamic-Link 程式庫 Entry-Point 函數</span><span class="sxs-lookup"><span data-stu-id="1abbf-103">Dynamic-Link Library Entry-Point Function</span></span>

<span data-ttu-id="1abbf-104">DLL 可以選擇性地指定進入點函數。</span><span class="sxs-lookup"><span data-stu-id="1abbf-104">A DLL can optionally specify an entry-point function.</span></span> <span data-ttu-id="1abbf-105">如果有的話，每當進程或執行緒載入或卸載 DLL 時，系統就會呼叫進入點函數。</span><span class="sxs-lookup"><span data-stu-id="1abbf-105">If present, the system calls the entry-point function whenever a process or thread loads or unloads the DLL.</span></span> <span data-ttu-id="1abbf-106">可以用來執行簡單的初始化和清除工作。</span><span class="sxs-lookup"><span data-stu-id="1abbf-106">It can be used to perform simple initialization and cleanup tasks.</span></span> <span data-ttu-id="1abbf-107">例如，它可以在建立新的執行緒時設定執行緒區域儲存區，並線上程終止時將它清除。</span><span class="sxs-lookup"><span data-stu-id="1abbf-107">For example, it can set up thread local storage when a new thread is created, and clean it up when the thread is terminated.</span></span>

<span data-ttu-id="1abbf-108">如果您要將 DLL 連結到 C 執行時間程式庫，它可能會為您提供進入點函式，並可讓您提供個別的初始化函數。</span><span class="sxs-lookup"><span data-stu-id="1abbf-108">If you are linking your DLL with the C run-time library, it may provide an entry-point function for you, and allow you to provide a separate initialization function.</span></span> <span data-ttu-id="1abbf-109">如需詳細資訊，請參閱執行時間程式庫的檔。</span><span class="sxs-lookup"><span data-stu-id="1abbf-109">Check the documentation for your run-time library for more information.</span></span>

<span data-ttu-id="1abbf-110">如果您要提供自己的進入點，請參閱 [**DllMain**](dllmain.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="1abbf-110">If you are providing your own entry-point, see the [**DllMain**](dllmain.md) function.</span></span> <span data-ttu-id="1abbf-111">名稱 **DllMain** 是使用者定義函數的預留位置。</span><span class="sxs-lookup"><span data-stu-id="1abbf-111">The name **DllMain** is a placeholder for a user-defined function.</span></span> <span data-ttu-id="1abbf-112">您必須指定建立 DLL 時使用的實際名稱。</span><span class="sxs-lookup"><span data-stu-id="1abbf-112">You must specify the actual name you use when you build your DLL.</span></span> <span data-ttu-id="1abbf-113">如需詳細資訊，請參閱您的開發工具隨附的檔。</span><span class="sxs-lookup"><span data-stu-id="1abbf-113">For more information, see the documentation included with your development tools.</span></span>

## <a name="calling-the-entry-point-function"></a><span data-ttu-id="1abbf-114">呼叫 Entry-Point 函式</span><span class="sxs-lookup"><span data-stu-id="1abbf-114">Calling the Entry-Point Function</span></span>

<span data-ttu-id="1abbf-115">每當發生下列任何一個事件時，系統就會呼叫進入點函數：</span><span class="sxs-lookup"><span data-stu-id="1abbf-115">The system calls the entry-point function whenever any one of the following events occurs:</span></span>

-   <span data-ttu-id="1abbf-116">進程會載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="1abbf-116">A process loads the DLL.</span></span> <span data-ttu-id="1abbf-117">針對使用載入時間動態連結的進程，會在處理常式初始化期間載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="1abbf-117">For processes using load-time dynamic linking, the DLL is loaded during process initialization.</span></span> <span data-ttu-id="1abbf-118">針對使用執行時間連結的進程，會在 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 傳回之前載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="1abbf-118">For processes using run-time linking, the DLL is loaded before [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) returns.</span></span>
-   <span data-ttu-id="1abbf-119">進程卸載 DLL。</span><span class="sxs-lookup"><span data-stu-id="1abbf-119">A process unloads the DLL.</span></span> <span data-ttu-id="1abbf-120">當進程終止或呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式，且參考計數變成零時，就會卸載 DLL。</span><span class="sxs-lookup"><span data-stu-id="1abbf-120">The DLL is unloaded when the process terminates or calls the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function and the reference count becomes zero.</span></span> <span data-ttu-id="1abbf-121">如果進程因為 [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) 或 [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) 函式而終止，則系統不會呼叫 DLL 進入點函式。</span><span class="sxs-lookup"><span data-stu-id="1abbf-121">If the process terminates as a result of the [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) or [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) function, the system does not call the DLL entry-point function.</span></span>
-   <span data-ttu-id="1abbf-122">已載入 DLL 的進程中會建立新的執行緒。</span><span class="sxs-lookup"><span data-stu-id="1abbf-122">A new thread is created in a process that has loaded the DLL.</span></span> <span data-ttu-id="1abbf-123">您可以使用 [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) 函數，在建立執行緒時停用通知。</span><span class="sxs-lookup"><span data-stu-id="1abbf-123">You can use the [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) function to disable notification when threads are created.</span></span>
-   <span data-ttu-id="1abbf-124">已載入 DLL 之進程的執行緒會正常終止，而不是使用 [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) 或 [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)。</span><span class="sxs-lookup"><span data-stu-id="1abbf-124">A thread of a process that has loaded the DLL terminates normally, not using [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) or [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="1abbf-125">當進程卸載 DLL 時，只會針對整個進程呼叫進入點函數一次，而不是針對進程的每個現有線程呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="1abbf-125">When a process unloads the DLL, the entry-point function is called only once for the entire process, rather than once for each existing thread of the process.</span></span> <span data-ttu-id="1abbf-126">您可以使用 [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) 來停用執行緒終止時的通知。</span><span class="sxs-lookup"><span data-stu-id="1abbf-126">You can use [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) to disable notification when threads are terminated.</span></span>

<span data-ttu-id="1abbf-127">一次只有一個執行緒可以呼叫進入點函數。</span><span class="sxs-lookup"><span data-stu-id="1abbf-127">Only one thread at a time can call the entry-point function.</span></span>

<span data-ttu-id="1abbf-128">系統會在造成呼叫函式的進程或執行緒內容中呼叫進入點函數。</span><span class="sxs-lookup"><span data-stu-id="1abbf-128">The system calls the entry-point function in the context of the process or thread that caused the function to be called.</span></span> <span data-ttu-id="1abbf-129">這可讓 DLL 使用其進入點函式，在呼叫進程的虛擬位址空間中配置記憶體，或開啟進程可存取的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1abbf-129">This allows a DLL to use its entry-point function for allocating memory in the virtual address space of the calling process or to open handles accessible to the process.</span></span> <span data-ttu-id="1abbf-130">進入點函式也可以使用執行緒區域儲存 (TLS) ，配置私用至新執行緒的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1abbf-130">The entry-point function can also allocate memory that is private to a new thread by using thread local storage (TLS).</span></span> <span data-ttu-id="1abbf-131">如需執行緒區域儲存區的詳細資訊，請參閱 [執行緒區域儲存區](/windows/desktop/ProcThread/thread-local-storage)。</span><span class="sxs-lookup"><span data-stu-id="1abbf-131">For more information about thread local storage, see [Thread Local Storage](/windows/desktop/ProcThread/thread-local-storage).</span></span>

## <a name="entry-point-function-definition"></a><span data-ttu-id="1abbf-132">Entry-Point 函式定義</span><span class="sxs-lookup"><span data-stu-id="1abbf-132">Entry-Point Function Definition</span></span>

<span data-ttu-id="1abbf-133">DLL 進入點函數必須使用標準呼叫呼叫慣例來宣告。</span><span class="sxs-lookup"><span data-stu-id="1abbf-133">The DLL entry-point function must be declared with the standard-call calling convention.</span></span> <span data-ttu-id="1abbf-134">如果 DLL 進入點未正確宣告，就不會載入 DLL，系統會顯示一則訊息，指出必須使用 WINAPI 來宣告 DLL 進入點。</span><span class="sxs-lookup"><span data-stu-id="1abbf-134">If the DLL entry point is not declared correctly, the DLL is not loaded, and the system displays a message indicating that the DLL entry point must be declared with WINAPI.</span></span>

<span data-ttu-id="1abbf-135">在函式主體中，您可以處理下列案例的任何組合，其中已呼叫 DLL 進入點：</span><span class="sxs-lookup"><span data-stu-id="1abbf-135">In the body of the function, you may handle any combination of the following scenarios in which the DLL entry point has been called:</span></span>

-   <span data-ttu-id="1abbf-136">進程會載入 DLL (**dll \_ 進程 \_ 附加**) 。</span><span class="sxs-lookup"><span data-stu-id="1abbf-136">A process loads the DLL (**DLL\_PROCESS\_ATTACH**).</span></span>
-   <span data-ttu-id="1abbf-137">目前的進程會建立新的執行緒， (**DLL \_ 執行緒 \_ 附加**) 。</span><span class="sxs-lookup"><span data-stu-id="1abbf-137">The current process creates a new thread (**DLL\_THREAD\_ATTACH**).</span></span>
-   <span data-ttu-id="1abbf-138">執行緒會正常結束 (**DLL \_ 執行緒卸 \_ 離**) 。</span><span class="sxs-lookup"><span data-stu-id="1abbf-138">A thread exits normally (**DLL\_THREAD\_DETACH**).</span></span>
-   <span data-ttu-id="1abbf-139">進程卸載 DLL (**dll 進程卸 \_ \_ 離**) 。</span><span class="sxs-lookup"><span data-stu-id="1abbf-139">A process unloads the DLL (**DLL\_PROCESS\_DETACH**).</span></span>

<span data-ttu-id="1abbf-140">進入點函式應該只執行簡單的初始化工作。</span><span class="sxs-lookup"><span data-stu-id="1abbf-140">The entry-point function should perform only simple initialization tasks.</span></span> <span data-ttu-id="1abbf-141">它不能呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 函式 (或) 的函式，因為這可能會以 DLL 載入順序建立相依性迴圈。</span><span class="sxs-lookup"><span data-stu-id="1abbf-141">It must not call the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) function (or a function that calls these functions), because this may create dependency loops in the DLL load order.</span></span> <span data-ttu-id="1abbf-142">這可能會導致在系統執行初始化程式碼之前，使用了 DLL。</span><span class="sxs-lookup"><span data-stu-id="1abbf-142">This can result in a DLL being used before the system has executed its initialization code.</span></span> <span data-ttu-id="1abbf-143">同樣地，進入點函數不能呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式 (或在進程終止期間呼叫 **FreeLibrary**) 的函式，因為這可能會導致系統在系統執行終止程式碼之後，使用 DLL。</span><span class="sxs-lookup"><span data-stu-id="1abbf-143">Similarly, the entry-point function must not call the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function (or a function that calls **FreeLibrary**) during process termination, because this can result in a DLL being used after the system has executed its termination code.</span></span>

<span data-ttu-id="1abbf-144">由於呼叫進入點函式時，保證會將 Kernel32.dll 載入至進程位址空間，因此在 Kernel32.dll 中呼叫函式並不會導致在執行初始化程式碼之前使用 DLL。</span><span class="sxs-lookup"><span data-stu-id="1abbf-144">Because Kernel32.dll is guaranteed to be loaded in the process address space when the entry-point function is called, calling functions in Kernel32.dll does not result in the DLL being used before its initialization code has been executed.</span></span> <span data-ttu-id="1abbf-145">因此，進入點函數可以建立同步處理 [物件](/windows/desktop/Sync/synchronization-objects) （例如重要區段和 mutex），並使用 TLS，因為這些函式位於 Kernel32.dll 中。</span><span class="sxs-lookup"><span data-stu-id="1abbf-145">Therefore, the entry-point function can create [synchronization objects](/windows/desktop/Sync/synchronization-objects) such as critical sections and mutexes, and use TLS, because these functions are located in Kernel32.dll.</span></span> <span data-ttu-id="1abbf-146">例如，呼叫登錄函式並不安全，因為它們位於 Advapi32.dll 中。</span><span class="sxs-lookup"><span data-stu-id="1abbf-146">It is not safe to call the registry functions, for example, because they are located in Advapi32.dll.</span></span>

<span data-ttu-id="1abbf-147">呼叫其他函式可能會導致難以診斷的問題。</span><span class="sxs-lookup"><span data-stu-id="1abbf-147">Calling other functions may result in problems that are difficult to diagnose.</span></span> <span data-ttu-id="1abbf-148">例如，呼叫使用者、Shell 和 COM 函式可能會造成存取違規錯誤，因為其 Dll 中的某些函式會呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 來載入其他系統元件。</span><span class="sxs-lookup"><span data-stu-id="1abbf-148">For example, calling User, Shell, and COM functions can cause access violation errors, because some functions in their DLLs call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to load other system components.</span></span> <span data-ttu-id="1abbf-149">相反地，在終止期間呼叫這些函式可能會造成存取違規錯誤，因為對應的元件可能已經卸載或未初始化。</span><span class="sxs-lookup"><span data-stu-id="1abbf-149">Conversely, calling those functions during termination can cause access violation errors because the corresponding component may already have been unloaded or uninitialized.</span></span>

<span data-ttu-id="1abbf-150">下列範例示範如何結構 DLL 進入點函數。</span><span class="sxs-lookup"><span data-stu-id="1abbf-150">The following example demonstrates how to structure the DLL entry-point function.</span></span>

``` syntax
BOOL WINAPI DllMain(
    HINSTANCE hinstDLL,  // handle to DLL module
    DWORD fdwReason,     // reason for calling function
    LPVOID lpReserved )  // reserved
{
    // Perform actions based on the reason for calling.
    switch( fdwReason ) 
    { 
        case DLL_PROCESS_ATTACH:
         // Initialize once for each new process.
         // Return FALSE to fail DLL load.
            break;

        case DLL_THREAD_ATTACH:
         // Do thread-specific initialization.
            break;

        case DLL_THREAD_DETACH:
         // Do thread-specific cleanup.
            break;

        case DLL_PROCESS_DETACH:
         // Perform any necessary cleanup.
            break;
    }
    return TRUE;  // Successful DLL_PROCESS_ATTACH.
}
```

## <a name="entry-point-function-return-value"></a><span data-ttu-id="1abbf-151">Entry-Point 函數傳回值</span><span class="sxs-lookup"><span data-stu-id="1abbf-151">Entry-Point Function Return Value</span></span>

<span data-ttu-id="1abbf-152">當呼叫 DLL 進入點函式，因為進程正在載入時，此函數會傳回 **TRUE** 以表示成功。</span><span class="sxs-lookup"><span data-stu-id="1abbf-152">When a DLL entry-point function is called because a process is loading, the function returns **TRUE** to indicate success.</span></span> <span data-ttu-id="1abbf-153">針對使用載入時間連結的進程，傳回值 **FALSE** 會導致進程初始化失敗，而且進程會終止。</span><span class="sxs-lookup"><span data-stu-id="1abbf-153">For processes using load-time linking, a return value of **FALSE** causes the process initialization to fail and the process terminates.</span></span> <span data-ttu-id="1abbf-154">如果是使用執行時間連結的進程，傳回值 FALSE 會導致 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 函數傳回 **Null**，表示失敗。</span><span class="sxs-lookup"><span data-stu-id="1abbf-154">For processes using run-time linking, a return value of FALSE causes the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) function to return **NULL**, indicating failure.</span></span> <span data-ttu-id="1abbf-155"> (系統立即以 **dll \_ 進程卸 \_ 離** 和卸載 dll 來呼叫您的進入點函式。 ) 基於任何其他原因呼叫函式時，會忽略進入點函數的傳回值。</span><span class="sxs-lookup"><span data-stu-id="1abbf-155">(The system immediately calls your entry-point function with **DLL\_PROCESS\_DETACH** and unloads the DLL.) The return value of the entry-point function is disregarded when the function is called for any other reason.</span></span>

 

 
