---
description: 動態連結中會使用下列函數。
ms.assetid: 29e50bd5-1712-407f-bcb3-50a0a22ab8b5
title: Dynamic-Link 程式庫函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47ce37b6f91570ce9f3314fc329b5e85cde310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852143"
---
# <a name="dynamic-link-library-functions"></a>Dynamic-Link 程式庫函數

動態連結中會使用下列函數。



| 函式                                                       | 描述                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)                     | 將目錄新增至進程 DLL 搜尋路徑。                                                                                                               |
| [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) | 停用指定之 DLL 的執行緒附加和執行緒卸離通知。                                                                                  |
| [**DllMain**](dllmain.md)                                     | DLL 中選擇性的進入點。                                                                                                                            |
| [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)                             | 遞減載入之 DLL 的參考計數。 當參考計數到達零時，模組就會從呼叫進程的位址空間中取消對應。 |
| [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)   | 將已載入 DLL 的參考計數遞減1，然後呼叫 [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) 來結束通話的執行緒。                       |
| [**GetDllDirectory**](/windows/desktop/api/WinBase/nf-winbase-getdlldirectorya)                     | 抓取用來尋找應用程式 Dll 之搜尋路徑的應用程式特定部分。                                                         |
| [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)                 | 抓取包含指定模組之檔案的完整路徑。                                                                               |
| [**GetModuleFileNameEx**](/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa)            | 抓取包含指定模組之檔案的完整路徑。                                                                               |
| [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)                     | 抓取指定模組的模組控制碼。                                                                                                            |
| [**GetModuleHandleEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandleexa)                 | 抓取指定模組的模組控制碼。                                                                                                            |
| [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)                       | 從指定的 DLL 抓取匯出的函式或變數的位址。                                                                              |
| [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                             | 將指定的可執行模組對應至呼叫進程的位址空間。                                                                            |
| [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)                         | 將指定的可執行模組對應至呼叫進程的位址空間。                                                                            |
| [**>loadpackagedlibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)             | 將指定的封裝模組及其相依性對應至呼叫進程的位址空間。 只有 Windows Store 應用程式可以呼叫此函數。         |
| [**RemoveDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-removedlldirectory)               | 使用 [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)移除已加入至進程 DLL 搜尋路徑的目錄。                                         |
| [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)   | 指定當呼叫進程載入 DLL 時，要搜尋的一組預設目錄。                                                                         |
| [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)                     | 修改用來尋找應用程式 Dll 的搜尋路徑。                                                                                              |



 

## <a name="obsolete-functions"></a>過時的函式

這些函式僅提供給 Windows 的16位版本的相容性。

[**LoadModule**](/windows/desktop/api/Winbase/nf-winbase-loadmodule)

 

 
