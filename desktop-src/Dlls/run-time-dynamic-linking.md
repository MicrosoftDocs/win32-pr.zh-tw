---
description: 當應用程式呼叫 LoadLibrary 或 LoadLibraryEx 函式時，系統會嘗試找出 DLL (如需詳細資訊，請參閱 Dynamic-Link 程式庫搜尋順序) 。
ms.assetid: 81e237a9-3c32-46a5-88d3-c978f43dad54
title: Run-Time 動態連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e215ac83ecdc0615b8030e2e215857c67fe6e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997500"
---
# <a name="run-time-dynamic-linking"></a>Run-Time 動態連結

當應用程式呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 函式時，系統會嘗試找出 DLL (如需詳細資訊，請參閱 [動態連結程式庫搜尋順序](dynamic-link-library-search-order.md)) 。 如果搜尋成功，系統會將 DLL 模組對應到進程的虛擬位址空間，並遞增參考計數。 如果呼叫 **LoadLibrary** 或 **LOADLIBRARYEX** 指定的 DLL 的程式碼已經對應到呼叫進程的虛擬位址空間，則函式只會傳回 dll 的控制碼，並遞增 dll 參考計數。 請注意，兩個具有相同基底檔案名和副檔名但在不同目錄中找到的 Dll，不會被視為相同的 DLL。

系統會在呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)的執行緒內容中呼叫進入點函數。 如果 DLL 已經透過呼叫 **LoadLibrary** 或 **LoadLibraryEx** ，但沒有對應的 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式呼叫，就不會呼叫進入點函數。

如果系統找不到 DLL 或進入點函數傳回 FALSE，則 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LOADLIBRARYEX**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 會傳回 Null。 如果 **LoadLibrary** 或 **LoadLibraryEx** 成功，它會將控制碼傳回至 DLL 模組。 此程式可以使用此控制碼來識別對 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)、 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)或 [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread) 函數的呼叫中的 DLL。

[**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)函數會傳回在 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)、 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)或 [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)中使用的控制碼。 只有當 DLL 模組已經透過載入時間連結或先前對 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)的呼叫，對應到進程的位址空間時， **GetModuleHandle** 函數才會成功。 不同于 **LoadLibrary** 或 **LoadLibraryEx**， **GetModuleHandle** 不會遞增模組參考計數。 [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)函式會抓取與 **GetModuleHandle**、 **LoadLibrary** 或 **LoadLibraryEx** 所傳回之控制碼相關聯之模組的完整路徑。

此程式可以使用 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 來取得 dll 中匯出函式的位址，方法是使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)、 [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)所傳回的 dll 模組控制碼。

當不再需要 DLL 模組時，此處理程式可以呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 或 [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)。 如果參考計數為零，則這些函式會遞減模組參考計數，並取消對應進程的虛擬位址空間中的 DLL 程式碼。

執行時間動態連結可讓進程繼續執行，即使 DLL 無法使用也是一樣。 然後，程式可以使用替代方法來完成其目標。 例如，如果處理常式找不到一個 DLL，它可以嘗試使用另一個 DLL，也可以通知使用者發生錯誤。 如果使用者可以提供遺失 DLL 的完整路徑，此程式可以使用這項資訊載入 DLL，即使它不在一般搜尋路徑中也一樣。 這種情況與載入時間連結相反，因為系統會在找不到 DLL 時，直接終止進程。

如果 DLL 使用 [**DllMain**](dllmain.md) 函式為進程的每個執行緒執行初始化，則執行時間動態連結可能會造成問題，因為呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 之前已存在的執行緒不會呼叫進入點。 如需示範如何處理此問題的範例，請參閱 [使用 Dynamic-Link 程式庫中的執行緒區域儲存區](using-thread-local-storage-in-a-dynamic-link-library.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用執行時間動態連結](using-run-time-dynamic-linking.md)
</dt> </dl>

 

 
