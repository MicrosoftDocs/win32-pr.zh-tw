---
description: 當應用程式以動態方式載入動態連結程式庫，但未指定完整路徑名稱時，Windows 會嘗試依特定順序搜尋定義完善的目錄集來尋找 DLL，如 Dynamic-Link 程式庫搜尋順序中所述。 如果攻擊者取得 DLL 搜尋路徑上其中一個目錄的控制權，就可以在該目錄中放置 DLL 的惡意複本。 這有時稱為 DLL preloading 攻擊或 binary planting 攻擊。
ms.assetid: 9493F299-789D-4CBC-9822-96EEAE39B494
title: Dynamic-Link 程式庫安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4016139762461784702ac0190c1ee65d8bc6e72d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980662"
---
# <a name="dynamic-link-library-security"></a>Dynamic-Link 程式庫安全性

當應用程式以動態方式載入動態連結程式庫，但未指定完整路徑名稱時，Windows 會嘗試依特定順序搜尋定義完善的目錄集來尋找 DLL，如 [動態連結程式庫搜尋順序](dynamic-link-library-search-order.md)中所述。 如果攻擊者取得 DLL 搜尋路徑上其中一個目錄的控制權，就可以在該目錄中放置 DLL 的惡意複本。 這有時稱為 *DLL preloading 攻擊* 或 *binary planting 攻擊*。 如果系統在搜尋遭入侵的目錄之前找不到 DLL 的合法複本，它會載入惡意 DLL。 如果應用程式是以系統管理員許可權執行，攻擊者可能會在本機權限提高時成功。

例如，假設應用程式是設計用來從使用者的目前的目錄載入 DLL，並且在找不到 DLL 時正常地失敗。 應用程式只會以 DLL 的名稱呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，讓系統搜尋 dll。 假設啟用安全 DLL 搜尋模式，而應用程式未使用替代搜尋順序，則系統會依下列順序搜尋目錄：

1.  應用程式載入的來原始目錄。
2.  系統目錄。
3.  16位系統目錄。
4.  Windows 目錄。
5.  目前的目錄。
6.  PATH 環境變數中所列的目錄。

繼續進行此範例，具有應用程式知識的攻擊者會取得當前目錄的控制權，並在該目錄中放置 DLL 的惡意複本。 當應用程式發出 **LoadLibrary** 呼叫時，系統會搜尋 dll、在目前的目錄中尋找 dll 的惡意複本，然後將它載入。 DLL 的惡意複本接著會在應用程式中執行，並取得使用者的許可權。

開發人員可以遵循下列指導方針，以協助保護應用程式免于 DLL preloading 的攻擊：

-   若有可能，請在使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)、 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)、 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)或 [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) 函數時，指定完整路徑。
-   使用「載入連結 \_ 庫 \_ 搜尋」旗標搭配 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 函式，或使用這些旗標搭配 [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) 函式來建立進程的 DLL 搜尋順序，然後使用 [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) 或 [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) 函數修改清單。 如需詳細資訊，請參閱 [動態連結程式庫搜尋順序](dynamic-link-library-search-order.md)。

    **Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 這些旗標和功能可在已安裝 [KB2533623](https://support.microsoft.com/kb/2533623) 的系統上使用。

-   在已安裝 [KB2533623](https://support.microsoft.com/kb/2533623) 的系統上，使用「載入連結 \_ 庫 \_ 搜尋」旗標搭配 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 函式，或搭配 [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) 函式使用這些旗標來建立進程的 DLL 搜尋順序，然後使用 [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) 或 [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) 函數修改清單。 如需詳細資訊，請參閱 [動態連結程式庫搜尋順序](dynamic-link-library-search-order.md)。
-   請考慮使用 [dll](dynamic-link-library-redirection.md) 重新導向或 [資訊清單](/windows/desktop/SbsCs/manifests) ，以確保您的應用程式使用正確的 dll。
-   使用標準搜尋順序時，請確定已啟用「安全 DLL 搜尋」模式。 這會將使用者的目前目錄放在搜尋順序中，增加 Windows 在惡意複本之前找到合法 DLL 複本的機會。 從 Windows XP Service Pack 2 (SP2) 開始，預設會啟用安全的 DLL 搜尋模式，並且是由 **HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Session Manager** \\ **SafeDllSearchMode** registry 值所控制。 如需詳細資訊，請參閱 [動態連結程式庫搜尋順序](dynamic-link-library-search-order.md)。
-   請考慮使用 ( "" ) 的空字串來呼叫 [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) ，以移除標準搜尋路徑中的目前的目錄。 這應該在程式初始化初期完成，而不是在呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)之前和之後完成。 請注意， **SetDllDirectory** 會影響整個程式，而多個呼叫具有不同值之 **SetDllDirectory** 的執行緒可能會導致未定義的行為。 如果您的應用程式載入協力廠商 Dll，請仔細測試以找出任何不相容的問題。
-   除非啟用安全進程搜尋模式，否則請勿使用 [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) 函式來抓取後續 [**LOADLIBRARY**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 呼叫的 DLL 路徑。 未啟用安全程式搜尋模式時， **SearchPath** 函式會使用與 **LoadLibrary** 不同的搜尋順序，而且可能會先在使用者的目前目錄中搜尋指定的 DLL。 若要啟用 **SearchPath** 函式的安全程式搜尋模式，請使用 [**SetSearchPathMode**](/windows/desktop/api/winbase/nf-winbase-setsearchpathmode) 函式搭配基底 \_ 搜尋 \_ 路徑 \_ 啟用 \_ safe \_ SEARCHMODE。 這會將目前目錄移至 **SearchPath** 搜尋清單的結尾，以進行進程的存留期。 請注意，目前的目錄不會從搜尋路徑中移除，因此，如果系統在到達目前目錄之前找不到合法的 DLL 複本，則應用程式仍然很容易受到攻擊。 如同 [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)，呼叫 **SetSearchPathMode** 在處理常式初始化時應該提早完成，而且會影響整個進程。 如果您的應用程式載入協力廠商 Dll，請仔細測試以找出任何不相容的問題。
-   請勿根據搜尋 DLL 的 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 呼叫，來提出作業系統版本的假設。 如果應用程式是在 DLL 未合法存在的環境中執行，但是在搜尋路徑中有惡意的 DLL 複本，則可能會載入 DLL 的惡意複本。 請改用 [取得系統版本](/windows/desktop/SysInfo/getting-the-system-version)中所述的建議技術。

進程監視器工具可用來協助識別可能容易受到攻擊的 DLL 載入作業。 您可以從下載進程監視工具 <https://technet.microsoft.com/sysinternals/bb896645.aspx> 。

下列程式描述如何使用進程監視器來檢查應用程式中的 DLL 載入作業。

**使用進程監視器來檢查應用程式中的 DLL 載入作業**

1.  啟動進程監視。
2.  在 [進程監視器] 中，包含下列篩選：
    -   作業 CreateFile
    -   作業 LoadImage
    -   路徑包含 cpl
    -   路徑包含 .dll
    -   路徑包含. winspool.drv
    -   路徑包含 .exe
    -   路徑包含 .ocx
    -   路徑包含 .scr
    -   路徑包含 sys
3.  排除下列篩選準則：
    -   進程名稱是 procmon.exe
    -   進程名稱是 Procmon64.exe
    -   進程名稱為 System
    -   作業從 IRP \_ MJ 開始\_
    -   作業的開頭為 FASTIO\_
    -   結果成功
    -   路徑結尾為 pagefile.sys
4.  嘗試啟動您的應用程式，並將目前的目錄設為特定目錄。 例如，按兩下副檔名已指派給應用程式的檔案。
5.  檢查流程監視器輸出中是否有可疑的路徑，例如呼叫目前的目錄以載入 DLL。 這種呼叫可能表示您的應用程式中有弱點。

 

 
