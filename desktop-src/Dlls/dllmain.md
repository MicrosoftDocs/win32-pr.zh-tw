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
# <a name="dllmain-entry-point"></a>DllMain 進入點

動態連結程式庫 (DLL) 的選擇性進入點。 當系統啟動或終止進程或執行緒時，它會使用進程的第一個執行緒，為每個載入的 DLL 呼叫進入點函數。 系統也會在使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式載入或卸載 DLL 時，呼叫該 DLL 的進入點函數。

## <a name="example"></a>範例

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

這是 [動態連結程式庫 Entry-Point](dynamic-link-library-entry-point-function.md)函式的範例。


> [!WARNING]
> 您可以在 DLL 進入點中安全地進行的作業有很大的限制。 請參閱特定 Windows Api 的 [一般最佳作法](dynamic-link-library-best-practices.md) ，這些是在 DllMain 中不安全的呼叫。 如果您需要任何功能，但最簡單的初始化會在 DLL 的初始化函式中進行。 您可以要求應用程式在 DllMain 執行之後，以及在呼叫 DLL 中的任何其他函式之前，呼叫初始化函數。

 

## <a name="syntax"></a>語法


```C++
BOOL WINAPI DllMain(
  _In_ HINSTANCE hinstDLL,
  _In_ DWORD     fdwReason,
  _In_ LPVOID    lpvReserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hinstDLL* \[在\]
</dt> <dd>

DLL 模組的控制碼。 值是 DLL 的基底位址。 DLL 的 **HINSTANCE** 與 Dll 的 **HMODULE** 相同，因此 *hinstDLL* 可用於呼叫需要模組控制碼的函式。

</dd> <dt>

*fdwReason* \[在\]
</dt> <dd>

指出如何呼叫 DLL 進入點函數的原因代碼。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**DLL \_進程 \_ 附加**</dt> <dt>1</dt> </dl> | 將 DLL 載入至目前進程的虛擬位址空間中，是因為進程啟動或呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)所造成的結果。 Dll 可以使用此機會初始化任何實例資料，或使用 [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) 函式來配置執行緒區域儲存 (TLS) 索引。<br/> *LpReserved* 參數會指出 DLL 是以靜態或動態方式載入。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**DLL \_進程卸 \_ 離**</dt> <dt>0</dt> </dl> | 正在從呼叫進程的虛擬位址空間卸載 DLL，因為它載入失敗，或是參考計數已達到零 (進程已在每次呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)) 時終止或呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)一次。<br/> *LpReserved* 參數會指出 DLL 是否因為 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)呼叫、載入失敗或進程終止的結果而卸載。<br/> DLL 可以使用這個機會呼叫 [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) 函式，以釋放任何使用 [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) 所配置的 TLS 索引，以及釋放任何執行緒區域資料。<br/> 請注意，接收 **dll \_ 進程卸 \_ 離** 通知的執行緒不一定是收到 **dll \_ 進程 \_ 附加** 通知的相同執行緒。<br/> |
| <span id="DLL_THREAD_ATTACH"></span><span id="dll_thread_attach"></span><dl> <dt>**DLL \_執行緒 \_ 附加**</dt> <dt>2</dt> </dl>    | 目前的進程正在建立新的執行緒。 發生這種情況時，系統會呼叫目前附加至進程之所有 Dll 的進入點函數。 呼叫會在新執行緒的內容中進行。 Dll 可以使用這個機會初始化執行緒的 TLS 位置。 以 dll **\_ 進程 \_ 附加** 呼叫 dll 進入點函式的執行緒，不會以 **DLL \_ 執行緒 \_ 附加** 來呼叫 dll 進入點函數。 <br/> 請注意，DLL 的進入點函式只會由進程載入 DLL 之後所建立的執行緒，以此值來呼叫。 使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)載入 DLL 時，現有的執行緒不會呼叫新載入之 DLL 的進入點函數。<br/>                                                                                                                                                                       |
| <span id="DLL_THREAD_DETACH"></span><span id="dll_thread_detach"></span><dl> <dt>**DLL \_執行緒卸 \_ 離**</dt> <dt>3</dt> </dl>    | 執行緒已完全結束。 如果 DLL 已將配置的記憶體指標儲存在 TLS 位置中，則應該使用這個機會來釋放記憶體。 系統會以這個值呼叫所有目前載入之 Dll 的進入點函數。 呼叫會在結束執行緒的內容中進行。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*lpvReserved* \[在\]
</dt> <dd>

如果 *fdwReason* 是 **DLL \_ 進程 \_ 附加**，則動態載入的 *lpvReserved* 是 Null，而靜態載入的非 Null 則為 **null** 。

如果 *fdwReason* 是 **DLL \_ 進程卸 \_ 離**，則如果已呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)或 dll 載入失敗，則 *lpvReserved* 為 **Null** ，如果進程正在終止，則為非 **null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

當系統以 **DLL \_ 進程 \_ 附加** 值呼叫 **DllMain** 函式時，如果初始化失敗，函式會傳回 **TRUE** ，否則傳回 **FALSE** 。 如果呼叫 **DllMain** 時傳回值為 **FALSE** ，因為進程使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)函式， **LoadLibrary** 會傳回 Null。  (系統立即以 **dll \_ 進程卸 \_ 離** 和卸載 dll 來呼叫您的進入點函式。 ) 如果在處理常式初始化期間呼叫 **DllMain** 時，傳回值為 **FALSE** ，進程就會終止，並出現錯誤。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

當系統以 **DLL \_ 進程 \_ 附加** 以外的任何值來呼叫 **DllMain** 函數時，會忽略傳回值。

## <a name="remarks"></a>備註

**DllMain** 是程式庫定義函數名稱的預留位置。 您必須指定建立 DLL 時使用的實際名稱。 如需詳細資訊，請參閱您的開發工具隨附的檔。

在初始進程啟動期間，或呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)之後，系統會掃描已載入的 dll 清單以進行處理。 針對尚未以 **dll \_ 進程 \_ 附加** 值呼叫的每個 dll，系統會呼叫 dll 的進入點函數。 此呼叫是在造成進程位址空間變更的執行緒內容中進行，例如進程的主要執行緒或呼叫 **LoadLibrary** 的執行緒。 進入點的存取權是由系統以整個進程為基礎進行序列化。 *DllMain* 中的執行緒會持有載入器鎖定，因此無法動態載入或初始化任何額外的 dll。

如果 DLL 的進入點函式在 **dll \_ 進程 \_ 附加** 通知之後傳回 FALSE，則會收到 **dll \_ 進程卸 \_ 離** 通知，並且會立即卸載 dll。 但是，如果 **DLL \_ 進程 \_ 附加** 程式碼擲回例外狀況，進入點函數將不會收到 **DLL 進程卸 \_ \_ 離** 通知。

在某些情況下，會針對終止執行緒呼叫進入點函式，即使從未以執行緒的 **DLL \_ 執行緒 \_ 附加** 呼叫進入點函數亦同：

-   執行緒是進程中的初始執行緒，因此系統會以 **DLL \_ 進程 \_ 附加** 值來呼叫進入點函數。
-   呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式時，執行緒已在執行中，因此系統永遠不會呼叫它的進入點函數。

當 dll 無法載入 DLL、進程終止或呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)時，從進程中卸載 dll 時，系統不會使用進程之個別執行緒的 **dll \_ 執行緒卸 \_ 離** 值來呼叫 dll 的進入點函數。 DLL 只會傳送 **dll 進程卸 \_ \_ 離** 通知。 Dll 可以利用這個機會來清除 DLL 已知所有線程的所有資源。

處理 **dll \_ 進程卸 \_ 離** 時，只有在動態卸載 dll 時，dll 才應該釋放資源，例如堆積記憶體 (*lpReserved* 參數為 **Null**) 。 如果進程正在結束 (*lpvReserved* 參數不是 **Null**) ，進程中的所有線程（除了目前的執行緒已結束），或已透過呼叫 [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) 函式明確地終止，這可能會讓某些進程資源（例如堆積處於不一致的狀態）。 在此情況下，DLL 無法安全地清除資源。 相反地，DLL 應該允許作業系統回收記憶體。

如果您藉由呼叫 [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) 或 [**TerminateJobObject**](/windows/desktop/api/jobapi2/nf-jobapi2-terminatejobobject)來終止進程，該進程的 dll 將不會收到 **DLL 進程卸 \_ \_ 離** 通知。 如果您藉由呼叫 [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread)來終止執行緒，該執行緒的 dll 將不會收到 **DLL 執行緒卸 \_ \_ 離** 通知。

進入點函式應該只執行簡單的初始化或終止工作。 它不能呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 函式 (或) 的函式，因為這可能會以 DLL 載入順序建立相依性迴圈。 這可能會導致在系統執行初始化程式碼之前，使用了 DLL。 同樣地，進入點函數不能呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式 (或在進程終止期間呼叫 **FreeLibrary**) 的函式，因為這可能會導致系統在系統執行終止程式碼之後，使用 DLL。

由於呼叫進入點函式時，保證會將 Kernel32.dll 載入至進程位址空間，因此在 Kernel32.dll 中呼叫函式並不會導致在執行初始化程式碼之前使用 DLL。 因此，進入點函數可以在 Kernel32.dll 中呼叫不會載入其他 Dll 的函式。 例如， *DllMain* 可以建立 [同步處理物件](/windows/desktop/Sync/synchronization-objects) （例如重要區段和 mutex），並使用 TLS。 可惜的是，Kernel32.dll 中並沒有完整的安全功能清單。

呼叫需要 Kernel32.dll 以外之 Dll 的函式可能會導致難以診斷的問題。 例如，呼叫 User、Shell 和 COM 函式可能會造成存取違規錯誤，因為有些函式會載入其他的系統元件。 相反地，在終止期間呼叫函式可能會造成存取違規錯誤，因為對應的元件可能已經卸載或未初始化。

由於 DLL 通知已序列化，因此進入點函式不應該嘗試與其他執行緒或進程通訊。 結果可能會產生鎖死。

如需撰寫 DLL 時最佳作法的詳細資訊，請參閱 https://docs.microsoft.com/windows/win32/dlls/dynamic-link-library-best-practices 。

如果您的 DLL 與 C 執行時間程式庫連結 (CRT) ，CRT 提供的進入點會呼叫全域和靜態 c + + 物件的函式和析構函數。 因此， *DllMain* 的這些限制也適用于函式和析構函式，以及從中呼叫的任何程式碼。

除非您的 DLL 與靜態 C 執行時間程式庫 (CRT) 連結，否則請考慮在接收 **dll \_ 進程 \_ 附加** 時呼叫 [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) 。


## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>處理。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[動態連結程式庫 Entry-Point 函式](dynamic-link-library-entry-point-function.md)
</dt> <dt>

[動態連結程式庫函數](dynamic-link-library-functions.md)
</dt> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> <dt>

[**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc)
</dt> <dt>

[**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree)
</dt> <dt>

[**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls)





</dt> </dl>
