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
# <a name="dynamic-link-library-entry-point-function"></a>Dynamic-Link 程式庫 Entry-Point 函數

DLL 可以選擇性地指定進入點函數。 如果有的話，每當進程或執行緒載入或卸載 DLL 時，系統就會呼叫進入點函數。 可以用來執行簡單的初始化和清除工作。 例如，它可以在建立新的執行緒時設定執行緒區域儲存區，並線上程終止時將它清除。

如果您要將 DLL 連結到 C 執行時間程式庫，它可能會為您提供進入點函式，並可讓您提供個別的初始化函數。 如需詳細資訊，請參閱執行時間程式庫的檔。

如果您要提供自己的進入點，請參閱 [**DllMain**](dllmain.md) 函數。 名稱 **DllMain** 是使用者定義函數的預留位置。 您必須指定建立 DLL 時使用的實際名稱。 如需詳細資訊，請參閱您的開發工具隨附的檔。

## <a name="calling-the-entry-point-function"></a>呼叫 Entry-Point 函式

每當發生下列任何一個事件時，系統就會呼叫進入點函數：

-   進程會載入 DLL。 針對使用載入時間動態連結的進程，會在處理常式初始化期間載入 DLL。 針對使用執行時間連結的進程，會在 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 傳回之前載入 DLL。
-   進程卸載 DLL。 當進程終止或呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式，且參考計數變成零時，就會卸載 DLL。 如果進程因為 [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) 或 [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) 函式而終止，則系統不會呼叫 DLL 進入點函式。
-   已載入 DLL 的進程中會建立新的執行緒。 您可以使用 [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) 函數，在建立執行緒時停用通知。
-   已載入 DLL 之進程的執行緒會正常終止，而不是使用 [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) 或 [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)。 當進程卸載 DLL 時，只會針對整個進程呼叫進入點函數一次，而不是針對進程的每個現有線程呼叫一次。 您可以使用 [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) 來停用執行緒終止時的通知。

一次只有一個執行緒可以呼叫進入點函數。

系統會在造成呼叫函式的進程或執行緒內容中呼叫進入點函數。 這可讓 DLL 使用其進入點函式，在呼叫進程的虛擬位址空間中配置記憶體，或開啟進程可存取的控制碼。 進入點函式也可以使用執行緒區域儲存 (TLS) ，配置私用至新執行緒的記憶體。 如需執行緒區域儲存區的詳細資訊，請參閱 [執行緒區域儲存區](/windows/desktop/ProcThread/thread-local-storage)。

## <a name="entry-point-function-definition"></a>Entry-Point 函式定義

DLL 進入點函數必須使用標準呼叫呼叫慣例來宣告。 如果 DLL 進入點未正確宣告，就不會載入 DLL，系統會顯示一則訊息，指出必須使用 WINAPI 來宣告 DLL 進入點。

在函式主體中，您可以處理下列案例的任何組合，其中已呼叫 DLL 進入點：

-   進程會載入 DLL (**dll \_ 進程 \_ 附加**) 。
-   目前的進程會建立新的執行緒， (**DLL \_ 執行緒 \_ 附加**) 。
-   執行緒會正常結束 (**DLL \_ 執行緒卸 \_ 離**) 。
-   進程卸載 DLL (**dll 進程卸 \_ \_ 離**) 。

進入點函式應該只執行簡單的初始化工作。 它不能呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 函式 (或) 的函式，因為這可能會以 DLL 載入順序建立相依性迴圈。 這可能會導致在系統執行初始化程式碼之前，使用了 DLL。 同樣地，進入點函數不能呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式 (或在進程終止期間呼叫 **FreeLibrary**) 的函式，因為這可能會導致系統在系統執行終止程式碼之後，使用 DLL。

由於呼叫進入點函式時，保證會將 Kernel32.dll 載入至進程位址空間，因此在 Kernel32.dll 中呼叫函式並不會導致在執行初始化程式碼之前使用 DLL。 因此，進入點函數可以建立同步處理 [物件](/windows/desktop/Sync/synchronization-objects) （例如重要區段和 mutex），並使用 TLS，因為這些函式位於 Kernel32.dll 中。 例如，呼叫登錄函式並不安全，因為它們位於 Advapi32.dll 中。

呼叫其他函式可能會導致難以診斷的問題。 例如，呼叫使用者、Shell 和 COM 函式可能會造成存取違規錯誤，因為其 Dll 中的某些函式會呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 來載入其他系統元件。 相反地，在終止期間呼叫這些函式可能會造成存取違規錯誤，因為對應的元件可能已經卸載或未初始化。

下列範例示範如何結構 DLL 進入點函數。

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

## <a name="entry-point-function-return-value"></a>Entry-Point 函數傳回值

當呼叫 DLL 進入點函式，因為進程正在載入時，此函數會傳回 **TRUE** 以表示成功。 針對使用載入時間連結的進程，傳回值 **FALSE** 會導致進程初始化失敗，而且進程會終止。 如果是使用執行時間連結的進程，傳回值 FALSE 會導致 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 函數傳回 **Null**，表示失敗。  (系統立即以 **dll \_ 進程卸 \_ 離** 和卸載 dll 來呼叫您的進入點函式。 ) 基於任何其他原因呼叫函式時，會忽略進入點函數的傳回值。

 

 
