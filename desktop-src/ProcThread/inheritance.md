---
description: 子進程可以繼承其父進程的數個屬性和資源。
ms.assetid: c530e723-2d40-4022-a259-dfc650604e44
title: " (進程和執行緒的繼承) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f50b191ee24783f7213ac15f61c435ebd696175a3042d79e2f359ef61097fe0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032588"
---
# <a name="inheritance"></a>繼承

子進程可以繼承其父進程的數個屬性和資源。 您也可以防止子進程繼承其父進程的屬性。 您可以繼承下列內容：

-   [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)函數所傳回的開啟控制碼。 這包括檔案的控制碼、主控台輸入緩衝區、主控台螢幕緩衝區、具名管道、串列通訊裝置，以及 mailslots。
-   開啟進程、執行緒、mutex、事件、信號、具名管道、匿名管道和檔案對應物件的控制碼。 這些會分別由 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)、 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)、 [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa)、 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)、 [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea)、 [**CreateNamedPipe**](/windows/desktop/api/winbase/nf-winbase-createnamedpipea)、 [**CreatePipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe)和 [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) 函式傳回。
-   環境變數。
-   目前的目錄。
-   主控台，除非已卸離進程或建立新的主控台。 子主控台進程也可以繼承父代的標準控制碼，以及存取輸入緩衝區和動態螢幕緩衝區。
-   [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode)函數所設定的錯誤模式。
-   處理器親和性遮罩。
-   與工作的關聯。

子進程不會繼承下列內容：

-   Priority 類別。
-   [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc)、 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc)、 [**HeapCreate**](/windows/desktop/api/heapapi/nf-heapapi-heapcreate)和 [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)所傳回的控制碼。
-   虛擬控制碼，如同 [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) 或 [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) 函數所傳回的控制碼一樣。 這些控制碼只對呼叫進程有效。
-   [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)函數所傳回的 DLL 模組控制碼。
-   GDI 或使用者控制碼，例如 **HBITMAP** 或 **HMENU**。

## <a name="inheriting-handles"></a>繼承控制碼

子進程可以繼承其父代的控制碼，但不會繼承其他控制碼。 若要使控制碼成為繼承的，您必須執行兩項作業：

-   指定當您建立、開啟或複製控制碼時，要繼承控制碼。 建立函式通常會使用 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構的 **bInheritHandle** 成員做為此用途。 [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) 使用 *bInheritHandles* 參數。
-   指定在呼叫 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)函式時，將 *bInheritHandles* 參數設定為 TRUE，以繼承可繼承的控制碼。 此外，若要繼承標準輸入、標準輸出和標準錯誤控制碼， [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)結構的 **dwFlags** 成員必須包含 STARTF \_ USESTDHANDLES。

若要指定特定子進程應繼承的控制碼清單，請使用 *PROC_THREAD_ATTRIBUTE_HANDLE_LIST* 旗標來呼叫 [**UpdateProcThreadAttribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute)函數。

繼承的控制碼會參考子進程中的相同物件，如同在父進程中一樣。 它也具有相同的值和存取權限。 因此，當某個進程變更物件的狀態時，變更會影響這兩個處理常式。 若要使用控制碼，子進程必須取出控制碼值，並「知道」它所參考的物件。 父進程通常會透過命令列、環境區塊或某種形式的 [處理序間通訊](/windows/desktop/ipc/interprocess-communications)，將這項資訊傳達給子進程。

您可以使用 [**SetHandleInformation**](/windows/win32/api/handleapi/nf-handleapi-sethandleinformation) 函數來控制現有的控制碼是否為可繼承。

## <a name="inheriting-environment-variables"></a>繼承環境變數

子進程預設會繼承其父進程的環境變數。 不過， [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 可讓父系進程指定不同的環境變數區塊。 如需詳細資訊，請參閱 [環境變數](environment-variables.md)。

## <a name="inheriting-the-current-directory"></a>繼承當前目錄

[**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory)函式會捕獲呼叫進程的目前的目錄。 子進程預設會繼承其父進程的目前的目錄。 不過， [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 可讓父系進程為子進程指定不同的目前的目錄。 若要變更呼叫進程的目前的目錄，請使用 [**>setcurrentdirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) 函數。
