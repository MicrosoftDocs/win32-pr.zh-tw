---
description: 動態連結程式庫 (DLL) 的選擇性進入點。 當系統啟動或終止進程或執行緒時，它會使用進程的第一個執行緒，為每個載入的 DLL 呼叫進入點函數。
ms.assetid: 0c3e3083-9297-4626-b2a7-0062d1c2cf9e
title: 'DllMain 進入點 (進程 .h) '
ms.topic: reference
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: ee182fd54f11909e54e98f827904f1da5e46f557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974721"
---
# <a name="dllmain-entry-point"></a><span data-ttu-id="42f46-104">DllMain 進入點</span><span class="sxs-lookup"><span data-stu-id="42f46-104">DllMain entry point</span></span>

<span data-ttu-id="42f46-105">動態連結程式庫 (DLL) 的選擇性進入點。</span><span class="sxs-lookup"><span data-stu-id="42f46-105">An optional entry point into a dynamic-link library (DLL).</span></span> <span data-ttu-id="42f46-106">當系統啟動或終止進程或執行緒時，它會使用進程的第一個執行緒，為每個載入的 DLL 呼叫進入點函數。</span><span class="sxs-lookup"><span data-stu-id="42f46-106">When the system starts or terminates a process or thread, it calls the entry-point function for each loaded DLL using the first thread of the process.</span></span> <span data-ttu-id="42f46-107">系統也會在使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式載入或卸載 DLL 時，呼叫該 DLL 的進入點函數。</span><span class="sxs-lookup"><span data-stu-id="42f46-107">The system also calls the entry-point function for a DLL when it is loaded or unloaded using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) functions.</span></span>

## <a name="example"></a><span data-ttu-id="42f46-108">範例</span><span class="sxs-lookup"><span data-stu-id="42f46-108">Example</span></span>

```cpp
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

<span data-ttu-id="42f46-109">這是 [動態連結程式庫 Entry-Point](dynamic-link-library-entry-point-function.md)函式的範例。</span><span class="sxs-lookup"><span data-stu-id="42f46-109">This is an example from the [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).</span></span>


> [!WARNING]
> <span data-ttu-id="42f46-110">您可以在 DLL 進入點中安全地進行的作業有很大的限制。</span><span class="sxs-lookup"><span data-stu-id="42f46-110">There are significant limits on what you can safely do in a DLL entry point.</span></span> <span data-ttu-id="42f46-111">請參閱特定 Windows Api 的 [一般最佳作法](dynamic-link-library-best-practices.md) ，這些是在 DllMain 中不安全的呼叫。</span><span class="sxs-lookup"><span data-stu-id="42f46-111">See [General Best Practices](dynamic-link-library-best-practices.md) for specific Windows APIs that are unsafe to call in DllMain.</span></span> <span data-ttu-id="42f46-112">如果您需要任何功能，但最簡單的初始化會在 DLL 的初始化函式中進行。</span><span class="sxs-lookup"><span data-stu-id="42f46-112">If you need anything but the simplest initialization then do that in an initialization function for the DLL.</span></span> <span data-ttu-id="42f46-113">您可以要求應用程式在 DllMain 執行之後，以及在呼叫 DLL 中的任何其他函式之前，呼叫初始化函數。</span><span class="sxs-lookup"><span data-stu-id="42f46-113">You can require applications to call the initialization function after DllMain has run and before they call any other functions in the DLL.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="42f46-114">語法</span><span class="sxs-lookup"><span data-stu-id="42f46-114">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _In_ HINSTANCE hinstDLL,
  _In_ DWORD     fdwReason,
  _In_ LPVOID    lpvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="42f46-115">參數</span><span class="sxs-lookup"><span data-stu-id="42f46-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42f46-116">*hinstDLL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42f46-116">*hinstDLL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42f46-117">DLL 模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="42f46-117">A handle to the DLL module.</span></span> <span data-ttu-id="42f46-118">值是 DLL 的基底位址。</span><span class="sxs-lookup"><span data-stu-id="42f46-118">The value is the base address of the DLL.</span></span> <span data-ttu-id="42f46-119">DLL 的 **HINSTANCE** 與 Dll 的 **HMODULE** 相同，因此 *hinstDLL* 可用於呼叫需要模組控制碼的函式。</span><span class="sxs-lookup"><span data-stu-id="42f46-119">The **HINSTANCE** of a DLL is the same as the **HMODULE** of the DLL, so *hinstDLL* can be used in calls to functions that require a module handle.</span></span>

</dd> <dt>

<span data-ttu-id="42f46-120">*fdwReason* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42f46-120">*fdwReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42f46-121">指出如何呼叫 DLL 進入點函數的原因代碼。</span><span class="sxs-lookup"><span data-stu-id="42f46-121">The reason code that indicates why the DLL entry-point function is being called.</span></span> <span data-ttu-id="42f46-122">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="42f46-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="42f46-123">值</span><span class="sxs-lookup"><span data-stu-id="42f46-123">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="42f46-124">意義</span><span class="sxs-lookup"><span data-stu-id="42f46-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <span data-ttu-id="42f46-125"><dt>**DLL \_進程 \_ 附加**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="42f46-125"><dt>**DLL\_PROCESS\_ATTACH**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="42f46-126">將 DLL 載入至目前進程的虛擬位址空間中，是因為進程啟動或呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)所造成的結果。</span><span class="sxs-lookup"><span data-stu-id="42f46-126">The DLL is being loaded into the virtual address space of the current process as a result of the process starting up or as a result of a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span> <span data-ttu-id="42f46-127">Dll 可以使用此機會初始化任何實例資料，或使用 [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) 函式來配置執行緒區域儲存 (TLS) 索引。</span><span class="sxs-lookup"><span data-stu-id="42f46-127">DLLs can use this opportunity to initialize any instance data or to use the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a thread local storage (TLS) index.</span></span><br/> <span data-ttu-id="42f46-128">*LpReserved* 參數會指出 DLL 是以靜態或動態方式載入。</span><span class="sxs-lookup"><span data-stu-id="42f46-128">The *lpReserved* parameter indicates whether the DLL is being loaded statically or dynamically.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <span data-ttu-id="42f46-129"><dt>**DLL \_進程卸 \_ 離**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="42f46-129"><dt>**DLL\_PROCESS\_DETACH**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="42f46-130">正在從呼叫進程的虛擬位址空間卸載 DLL，因為它載入失敗，或是參考計數已達到零 (進程已在每次呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)) 時終止或呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)一次。</span><span class="sxs-lookup"><span data-stu-id="42f46-130">The DLL is being unloaded from the virtual address space of the calling process because it was loaded unsuccessfully or the reference count has reached zero (the processes has either terminated or called [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) one time for each time it called [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).</span></span><br/> <span data-ttu-id="42f46-131">*LpReserved* 參數會指出 DLL 是否因為 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)呼叫、載入失敗或進程終止的結果而卸載。</span><span class="sxs-lookup"><span data-stu-id="42f46-131">The *lpReserved* parameter indicates whether the DLL is being unloaded as a result of a [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) call, a failure to load, or process termination.</span></span><br/> <span data-ttu-id="42f46-132">DLL 可以使用這個機會呼叫 [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) 函式，以釋放任何使用 [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) 所配置的 TLS 索引，以及釋放任何執行緒區域資料。</span><span class="sxs-lookup"><span data-stu-id="42f46-132">The DLL can use this opportunity to call the [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) function to free any TLS indices allocated by using [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) and to free any thread local data.</span></span><br/> <span data-ttu-id="42f46-133">請注意，接收 **dll \_ 進程卸 \_ 離** 通知的執行緒不一定是收到 **dll \_ 進程 \_ 附加** 通知的相同執行緒。</span><span class="sxs-lookup"><span data-stu-id="42f46-133">Note that the thread that receives the **DLL\_PROCESS\_DETACH** notification is not necessarily the same thread that received the **DLL\_PROCESS\_ATTACH** notification.</span></span><br/> |
| <span id="DLL_THREAD_ATTACH"></span><span id="dll_thread_attach"></span><dl> <span data-ttu-id="42f46-134"><dt>**DLL \_執行緒 \_ 附加**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="42f46-134"><dt>**DLL\_THREAD\_ATTACH**</dt> <dt>2</dt></span></span> </dl>    | <span data-ttu-id="42f46-135">目前的進程正在建立新的執行緒。</span><span class="sxs-lookup"><span data-stu-id="42f46-135">The current process is creating a new thread.</span></span> <span data-ttu-id="42f46-136">發生這種情況時，系統會呼叫目前附加至進程之所有 Dll 的進入點函數。</span><span class="sxs-lookup"><span data-stu-id="42f46-136">When this occurs, the system calls the entry-point function of all DLLs currently attached to the process.</span></span> <span data-ttu-id="42f46-137">呼叫會在新執行緒的內容中進行。</span><span class="sxs-lookup"><span data-stu-id="42f46-137">The call is made in the context of the new thread.</span></span> <span data-ttu-id="42f46-138">Dll 可以使用這個機會初始化執行緒的 TLS 位置。</span><span class="sxs-lookup"><span data-stu-id="42f46-138">DLLs can use this opportunity to initialize a TLS slot for the thread.</span></span> <span data-ttu-id="42f46-139">以 dll **\_ 進程 \_ 附加** 呼叫 dll 進入點函式的執行緒，不會以 **DLL \_ 執行緒 \_ 附加** 來呼叫 dll 進入點函數。</span><span class="sxs-lookup"><span data-stu-id="42f46-139">A thread calling the DLL entry-point function with **DLL\_PROCESS\_ATTACH** does not call the DLL entry-point function with **DLL\_THREAD\_ATTACH**.</span></span> <br/> <span data-ttu-id="42f46-140">請注意，DLL 的進入點函式只會由進程載入 DLL 之後所建立的執行緒，以此值來呼叫。</span><span class="sxs-lookup"><span data-stu-id="42f46-140">Note that a DLL's entry-point function is called with this value only by threads created after the DLL is loaded by the process.</span></span> <span data-ttu-id="42f46-141">使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)載入 DLL 時，現有的執行緒不會呼叫新載入之 DLL 的進入點函數。</span><span class="sxs-lookup"><span data-stu-id="42f46-141">When a DLL is loaded using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), existing threads do not call the entry-point function of the newly loaded DLL.</span></span><br/>                                                                                                                                                                       |
| <span id="DLL_THREAD_DETACH"></span><span id="dll_thread_detach"></span><dl> <span data-ttu-id="42f46-142"><dt>**DLL \_執行緒卸 \_ 離**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="42f46-142"><dt>**DLL\_THREAD\_DETACH**</dt> <dt>3</dt></span></span> </dl>    | <span data-ttu-id="42f46-143">執行緒已完全結束。</span><span class="sxs-lookup"><span data-stu-id="42f46-143">A thread is exiting cleanly.</span></span> <span data-ttu-id="42f46-144">如果 DLL 已將配置的記憶體指標儲存在 TLS 位置中，則應該使用這個機會來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="42f46-144">If the DLL has stored a pointer to allocated memory in a TLS slot, it should use this opportunity to free the memory.</span></span> <span data-ttu-id="42f46-145">系統會以這個值呼叫所有目前載入之 Dll 的進入點函數。</span><span class="sxs-lookup"><span data-stu-id="42f46-145">The system calls the entry-point function of all currently loaded DLLs with this value.</span></span> <span data-ttu-id="42f46-146">呼叫會在結束執行緒的內容中進行。</span><span class="sxs-lookup"><span data-stu-id="42f46-146">The call is made in the context of the exiting thread.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="42f46-147">*lpvReserved* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42f46-147">*lpvReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42f46-148">如果 *fdwReason* 是 **DLL \_ 進程 \_ 附加**，則動態載入的 *lpvReserved* 是 Null，而靜態載入的非 Null 則為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="42f46-148">If *fdwReason* is **DLL\_PROCESS\_ATTACH**, *lpvReserved* is **NULL** for dynamic loads and non-NULL for static loads.</span></span>

<span data-ttu-id="42f46-149">如果 *fdwReason* 是 **DLL \_ 進程卸 \_ 離**，則如果已呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)或 dll 載入失敗，則 *lpvReserved* 為 **Null** ，如果進程正在終止，則為非 **null** 。</span><span class="sxs-lookup"><span data-stu-id="42f46-149">If *fdwReason* is **DLL\_PROCESS\_DETACH**, *lpvReserved* is **NULL** if [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) has been called or the DLL load failed and non-**NULL** if the process is terminating.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42f46-150">傳回值</span><span class="sxs-lookup"><span data-stu-id="42f46-150">Return value</span></span>

<span data-ttu-id="42f46-151">當系統以 **DLL \_ 進程 \_ 附加** 值呼叫 **DllMain** 函式時，如果初始化失敗，函式會傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="42f46-151">When the system calls the **DllMain** function with the **DLL\_PROCESS\_ATTACH** value, the function returns **TRUE** if it succeeds or **FALSE** if initialization fails.</span></span> <span data-ttu-id="42f46-152">如果呼叫 **DllMain** 時傳回值為 **FALSE** ，因為進程使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)函式， **LoadLibrary** 會傳回 Null。</span><span class="sxs-lookup"><span data-stu-id="42f46-152">If the return value is **FALSE** when **DllMain** is called because the process uses the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function, **LoadLibrary** returns NULL.</span></span> <span data-ttu-id="42f46-153"> (系統立即以 **dll \_ 進程卸 \_ 離** 和卸載 dll 來呼叫您的進入點函式。 ) 如果在處理常式初始化期間呼叫 **DllMain** 時，傳回值為 **FALSE** ，進程就會終止，並出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="42f46-153">(The system immediately calls your entry-point function with **DLL\_PROCESS\_DETACH** and unloads the DLL.) If the return value is **FALSE** when **DllMain** is called during process initialization, the process terminates with an error.</span></span> <span data-ttu-id="42f46-154">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="42f46-154">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="42f46-155">當系統以 **DLL \_ 進程 \_ 附加** 以外的任何值來呼叫 **DllMain** 函數時，會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="42f46-155">When the system calls the **DllMain** function with any value other than **DLL\_PROCESS\_ATTACH**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="42f46-156">備註</span><span class="sxs-lookup"><span data-stu-id="42f46-156">Remarks</span></span>

<span data-ttu-id="42f46-157">**DllMain** 是程式庫定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="42f46-157">**DllMain** is a placeholder for the library-defined function name.</span></span> <span data-ttu-id="42f46-158">您必須指定建立 DLL 時使用的實際名稱。</span><span class="sxs-lookup"><span data-stu-id="42f46-158">You must specify the actual name you use when you build your DLL.</span></span> <span data-ttu-id="42f46-159">如需詳細資訊，請參閱您的開發工具隨附的檔。</span><span class="sxs-lookup"><span data-stu-id="42f46-159">For more information, see the documentation included with your development tools.</span></span>

<span data-ttu-id="42f46-160">在初始進程啟動期間，或呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)之後，系統會掃描已載入的 dll 清單以進行處理。</span><span class="sxs-lookup"><span data-stu-id="42f46-160">During initial process startup or after a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), the system scans the list of loaded DLLs for the process.</span></span> <span data-ttu-id="42f46-161">針對尚未以 **dll \_ 進程 \_ 附加** 值呼叫的每個 dll，系統會呼叫 dll 的進入點函數。</span><span class="sxs-lookup"><span data-stu-id="42f46-161">For each DLL that has not already been called with the **DLL\_PROCESS\_ATTACH** value, the system calls the DLL's entry-point function.</span></span> <span data-ttu-id="42f46-162">此呼叫是在造成進程位址空間變更的執行緒內容中進行，例如進程的主要執行緒或呼叫 **LoadLibrary** 的執行緒。</span><span class="sxs-lookup"><span data-stu-id="42f46-162">This call is made in the context of the thread that caused the process address space to change, such as the primary thread of the process or the thread that called **LoadLibrary**.</span></span> <span data-ttu-id="42f46-163">進入點的存取權是由系統以整個進程為基礎進行序列化。</span><span class="sxs-lookup"><span data-stu-id="42f46-163">Access to the entry point is serialized by the system on a process-wide basis.</span></span> <span data-ttu-id="42f46-164">*DllMain* 中的執行緒會持有載入器鎖定，因此無法動態載入或初始化任何額外的 dll。</span><span class="sxs-lookup"><span data-stu-id="42f46-164">Threads in *DllMain* hold the loader lock so no additional DLLs can be dynamically loaded or initialized.</span></span>

<span data-ttu-id="42f46-165">如果 DLL 的進入點函式在 **dll \_ 進程 \_ 附加** 通知之後傳回 FALSE，則會收到 **dll \_ 進程卸 \_ 離** 通知，並且會立即卸載 dll。</span><span class="sxs-lookup"><span data-stu-id="42f46-165">If the DLL's entry-point function returns FALSE following a **DLL\_PROCESS\_ATTACH** notification, it receives a **DLL\_PROCESS\_DETACH** notification and the DLL is unloaded immediately.</span></span> <span data-ttu-id="42f46-166">但是，如果 **DLL \_ 進程 \_ 附加** 程式碼擲回例外狀況，進入點函數將不會收到 **DLL 進程卸 \_ \_ 離** 通知。</span><span class="sxs-lookup"><span data-stu-id="42f46-166">However, if the **DLL\_PROCESS\_ATTACH** code throws an exception, the entry-point function will not receive the **DLL\_PROCESS\_DETACH** notification.</span></span>

<span data-ttu-id="42f46-167">在某些情況下，會針對終止執行緒呼叫進入點函式，即使從未以執行緒的 **DLL \_ 執行緒 \_ 附加** 呼叫進入點函數亦同：</span><span class="sxs-lookup"><span data-stu-id="42f46-167">There are cases in which the entry-point function is called for a terminating thread even if the entry-point function was never called with **DLL\_THREAD\_ATTACH** for the thread:</span></span>

-   <span data-ttu-id="42f46-168">執行緒是進程中的初始執行緒，因此系統會以 **DLL \_ 進程 \_ 附加** 值來呼叫進入點函數。</span><span class="sxs-lookup"><span data-stu-id="42f46-168">The thread was the initial thread in the process, so the system called the entry-point function with the **DLL\_PROCESS\_ATTACH** value.</span></span>
-   <span data-ttu-id="42f46-169">呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式時，執行緒已在執行中，因此系統永遠不會呼叫它的進入點函數。</span><span class="sxs-lookup"><span data-stu-id="42f46-169">The thread was already running when a call to the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function was made, so the system never called the entry-point function for it.</span></span>

<span data-ttu-id="42f46-170">當 dll 無法載入 DLL、進程終止或呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)時，從進程中卸載 dll 時，系統不會使用進程之個別執行緒的 **dll \_ 執行緒卸 \_ 離** 值來呼叫 dll 的進入點函數。</span><span class="sxs-lookup"><span data-stu-id="42f46-170">When a DLL is unloaded from a process as a result of an unsuccessful load of the DLL, termination of the process, or a call to [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary), the system does not call the DLL's entry-point function with the **DLL\_THREAD\_DETACH** value for the individual threads of the process.</span></span> <span data-ttu-id="42f46-171">DLL 只會傳送 **dll 進程卸 \_ \_ 離** 通知。</span><span class="sxs-lookup"><span data-stu-id="42f46-171">The DLL is only sent a **DLL\_PROCESS\_DETACH** notification.</span></span> <span data-ttu-id="42f46-172">Dll 可以利用這個機會來清除 DLL 已知所有線程的所有資源。</span><span class="sxs-lookup"><span data-stu-id="42f46-172">DLLs can take this opportunity to clean up all resources for all threads known to the DLL.</span></span>

<span data-ttu-id="42f46-173">處理 **dll \_ 進程卸 \_ 離** 時，只有在動態卸載 dll 時，dll 才應該釋放資源，例如堆積記憶體 (*lpReserved* 參數為 **Null**) 。</span><span class="sxs-lookup"><span data-stu-id="42f46-173">When handling **DLL\_PROCESS\_DETACH**, a DLL should free resources such as heap memory only if the DLL is being unloaded dynamically (the *lpReserved* parameter is **NULL**).</span></span> <span data-ttu-id="42f46-174">如果進程正在結束 (*lpvReserved* 參數不是 **Null**) ，進程中的所有線程（除了目前的執行緒已結束），或已透過呼叫 [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) 函式明確地終止，這可能會讓某些進程資源（例如堆積處於不一致的狀態）。</span><span class="sxs-lookup"><span data-stu-id="42f46-174">If the process is terminating (the *lpvReserved* parameter is non-**NULL**), all threads in the process except the current thread either have exited already or have been explicitly terminated by a call to the [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) function, which might leave some process resources such as heaps in an inconsistent state.</span></span> <span data-ttu-id="42f46-175">在此情況下，DLL 無法安全地清除資源。</span><span class="sxs-lookup"><span data-stu-id="42f46-175">In this case, it is not safe for the DLL to clean up the resources.</span></span> <span data-ttu-id="42f46-176">相反地，DLL 應該允許作業系統回收記憶體。</span><span class="sxs-lookup"><span data-stu-id="42f46-176">Instead, the DLL should allow the operating system to reclaim the memory.</span></span>

<span data-ttu-id="42f46-177">如果您藉由呼叫 [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) 或 [**TerminateJobObject**](/windows/desktop/api/jobapi2/nf-jobapi2-terminatejobobject)來終止進程，該進程的 dll 將不會收到 **DLL 進程卸 \_ \_ 離** 通知。</span><span class="sxs-lookup"><span data-stu-id="42f46-177">If you terminate a process by calling [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) or [**TerminateJobObject**](/windows/desktop/api/jobapi2/nf-jobapi2-terminatejobobject), the DLLs of that process do not receive **DLL\_PROCESS\_DETACH** notifications.</span></span> <span data-ttu-id="42f46-178">如果您藉由呼叫 [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread)來終止執行緒，該執行緒的 dll 將不會收到 **DLL 執行緒卸 \_ \_ 離** 通知。</span><span class="sxs-lookup"><span data-stu-id="42f46-178">If you terminate a thread by calling [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread), the DLLs of that thread do not receive **DLL\_THREAD\_DETACH** notifications.</span></span>

<span data-ttu-id="42f46-179">進入點函式應該只執行簡單的初始化或終止工作。</span><span class="sxs-lookup"><span data-stu-id="42f46-179">The entry-point function should perform only simple initialization or termination tasks.</span></span> <span data-ttu-id="42f46-180">它不能呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 函式 (或) 的函式，因為這可能會以 DLL 載入順序建立相依性迴圈。</span><span class="sxs-lookup"><span data-stu-id="42f46-180">It must not call the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) function (or a function that calls these functions), because this may create dependency loops in the DLL load order.</span></span> <span data-ttu-id="42f46-181">這可能會導致在系統執行初始化程式碼之前，使用了 DLL。</span><span class="sxs-lookup"><span data-stu-id="42f46-181">This can result in a DLL being used before the system has executed its initialization code.</span></span> <span data-ttu-id="42f46-182">同樣地，進入點函數不能呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式 (或在進程終止期間呼叫 **FreeLibrary**) 的函式，因為這可能會導致系統在系統執行終止程式碼之後，使用 DLL。</span><span class="sxs-lookup"><span data-stu-id="42f46-182">Similarly, the entry-point function must not call the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function (or a function that calls **FreeLibrary**) during process termination, because this can result in a DLL being used after the system has executed its termination code.</span></span>

<span data-ttu-id="42f46-183">由於呼叫進入點函式時，保證會將 Kernel32.dll 載入至進程位址空間，因此在 Kernel32.dll 中呼叫函式並不會導致在執行初始化程式碼之前使用 DLL。</span><span class="sxs-lookup"><span data-stu-id="42f46-183">Because Kernel32.dll is guaranteed to be loaded in the process address space when the entry-point function is called, calling functions in Kernel32.dll does not result in the DLL being used before its initialization code has been executed.</span></span> <span data-ttu-id="42f46-184">因此，進入點函數可以在 Kernel32.dll 中呼叫不會載入其他 Dll 的函式。</span><span class="sxs-lookup"><span data-stu-id="42f46-184">Therefore, the entry-point function can call functions in Kernel32.dll that do not load other DLLs.</span></span> <span data-ttu-id="42f46-185">例如， *DllMain* 可以建立 [同步處理物件](/windows/desktop/Sync/synchronization-objects) （例如重要區段和 mutex），並使用 TLS。</span><span class="sxs-lookup"><span data-stu-id="42f46-185">For example, *DllMain* can create [synchronization objects](/windows/desktop/Sync/synchronization-objects) such as critical sections and mutexes, and use TLS.</span></span> <span data-ttu-id="42f46-186">可惜的是，Kernel32.dll 中並沒有完整的安全功能清單。</span><span class="sxs-lookup"><span data-stu-id="42f46-186">Unfortunately, there is not a comprehensive list of safe functions in Kernel32.dll.</span></span>

<span data-ttu-id="42f46-187">呼叫需要 Kernel32.dll 以外之 Dll 的函式可能會導致難以診斷的問題。</span><span class="sxs-lookup"><span data-stu-id="42f46-187">Calling functions that require DLLs other than Kernel32.dll may result in problems that are difficult to diagnose.</span></span> <span data-ttu-id="42f46-188">例如，呼叫 User、Shell 和 COM 函式可能會造成存取違規錯誤，因為有些函式會載入其他的系統元件。</span><span class="sxs-lookup"><span data-stu-id="42f46-188">For example, calling User, Shell, and COM functions can cause access violation errors, because some functions load other system components.</span></span> <span data-ttu-id="42f46-189">相反地，在終止期間呼叫函式可能會造成存取違規錯誤，因為對應的元件可能已經卸載或未初始化。</span><span class="sxs-lookup"><span data-stu-id="42f46-189">Conversely, calling functions such as these during termination can cause access violation errors because the corresponding component may already have been unloaded or uninitialized.</span></span>

<span data-ttu-id="42f46-190">由於 DLL 通知已序列化，因此進入點函式不應該嘗試與其他執行緒或進程通訊。</span><span class="sxs-lookup"><span data-stu-id="42f46-190">Because DLL notifications are serialized, entry-point functions should not attempt to communicate with other threads or processes.</span></span> <span data-ttu-id="42f46-191">結果可能會產生鎖死。</span><span class="sxs-lookup"><span data-stu-id="42f46-191">Deadlocks may occur as a result.</span></span>

<span data-ttu-id="42f46-192">如需撰寫 DLL 時最佳作法的詳細資訊，請參閱 https://docs.microsoft.com/windows/win32/dlls/dynamic-link-library-best-practices 。</span><span class="sxs-lookup"><span data-stu-id="42f46-192">For information on best practices when writing a DLL, see https://docs.microsoft.com/windows/win32/dlls/dynamic-link-library-best-practices.</span></span>

<span data-ttu-id="42f46-193">如果您的 DLL 與 C 執行時間程式庫連結 (CRT) ，CRT 提供的進入點會呼叫全域和靜態 c + + 物件的函式和析構函數。</span><span class="sxs-lookup"><span data-stu-id="42f46-193">If your DLL is linked with the C run-time library (CRT), the entry point provided by the CRT calls the constructors and destructors for global and static C++ objects.</span></span> <span data-ttu-id="42f46-194">因此， *DllMain* 的這些限制也適用于函式和析構函式，以及從中呼叫的任何程式碼。</span><span class="sxs-lookup"><span data-stu-id="42f46-194">Therefore, these restrictions for *DllMain* also apply to constructors and destructors and any code that is called from them.</span></span>

<span data-ttu-id="42f46-195">除非您的 DLL 與靜態 C 執行時間程式庫 (CRT) 連結，否則請考慮在接收 **dll \_ 進程 \_ 附加** 時呼叫 [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) 。</span><span class="sxs-lookup"><span data-stu-id="42f46-195">Consider calling [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) when receiving **DLL\_PROCESS\_ATTACH**, unless your DLL is linked with static C run-time library (CRT).</span></span>


## <a name="requirements"></a><span data-ttu-id="42f46-196">規格需求</span><span class="sxs-lookup"><span data-stu-id="42f46-196">Requirements</span></span>



| <span data-ttu-id="42f46-197">需求</span><span class="sxs-lookup"><span data-stu-id="42f46-197">Requirement</span></span> | <span data-ttu-id="42f46-198">值</span><span class="sxs-lookup"><span data-stu-id="42f46-198">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42f46-199">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42f46-199">Minimum supported client</span></span><br/> | <span data-ttu-id="42f46-200">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42f46-200">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="42f46-201">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42f46-201">Minimum supported server</span></span><br/> | <span data-ttu-id="42f46-202">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42f46-202">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="42f46-203">標頭</span><span class="sxs-lookup"><span data-stu-id="42f46-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="42f46-204"><dt>處理。h</dt></span><span class="sxs-lookup"><span data-stu-id="42f46-204"><dt>Process.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42f46-205">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42f46-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f46-206">動態連結程式庫 Entry-Point 函式</span><span class="sxs-lookup"><span data-stu-id="42f46-206">Dynamic-Link Library Entry-Point Function</span></span>](dynamic-link-library-entry-point-function.md)
</dt> <dt>

[<span data-ttu-id="42f46-207">動態連結程式庫函數</span><span class="sxs-lookup"><span data-stu-id="42f46-207">Dynamic-Link Library Functions</span></span>](dynamic-link-library-functions.md)
</dt> <dt>

[<span data-ttu-id="42f46-208">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="42f46-208">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> <dt>

[<span data-ttu-id="42f46-209">**GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="42f46-209">**GetModuleFileName**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> <dt>

[<span data-ttu-id="42f46-210">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="42f46-210">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="42f46-211">**TlsAlloc**</span><span class="sxs-lookup"><span data-stu-id="42f46-211">**TlsAlloc**</span></span>](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc)
</dt> <dt>

[<span data-ttu-id="42f46-212">**TlsFree**</span><span class="sxs-lookup"><span data-stu-id="42f46-212">**TlsFree**</span></span>](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree)
</dt> <dt>

[<span data-ttu-id="42f46-213">**DisableThreadLibraryCalls**</span><span class="sxs-lookup"><span data-stu-id="42f46-213">**DisableThreadLibraryCalls**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls)





</dt> </dl>
