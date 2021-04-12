---
description: 本節說明如何判斷您的應用程式在哪一個版本的 Shell Dll 上執行，以及如何以特定版本的應用程式為目標。
title: 命令介面和 Shlwapi DLL 版本
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 49fb1767b7074da6480a47c52eb1384fb935317b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192674"
---
# <a name="shell-and-shlwapi-dll-versions"></a>命令介面和 Shlwapi DLL 版本

本節說明如何判斷您的應用程式在哪一個版本的 Shell Dll 上執行，以及如何以特定版本的應用程式為目標。

-   [DLL 版本號碼](#dll-version-numbers)
-   [使用 DllGetVersion 來判斷版本號碼](#using-dllgetversion-to-determine-the-version-number)
    -   [使用 DllGetVersion](#using-dllgetversion)
-   [專案版本](#project-versions)

## <a name="dll-version-numbers"></a>DLL 版本號碼

Shell 檔中所討論的所有程式設計項目，都包含在兩個 Dll 中： Shell32.dll 和 Shlwapi.dll。 由於持續的增強功能，這些 Dll 的不同版本會執行不同的功能。 在整個 Shell 參考檔中，每個程式設計項目都會指定支援的最低 DLL 版本號碼。 此版本號碼表示程式設計專案會在該版本和後續 DLL 版本中執行，除非另有指定。 如果未指定版本號碼，則會在所有現有版本的 DLL 中執行程式設計專案。

在 Windows XP 之前，新的 Shell32.dll 和 Shlwapi.dll 版本有時會隨著新版本的 Windows Internet Explorer 而提供。 從 Windows XP 版以來，這些 Dll 不再提供為新版 Windows 本身以外的可轉散發檔案。 下表概述不同的 DLL 版本，以及它們如何散發回可追溯至 Microsoft Internet Explorer 3.0、Windows 95 和 Microsoft Windows NT 4.0。

您可以在 Windows 95 和 Microsoft Windows NT 4.0 的原始版本中找到 Shell32.dll 4.0 版。 Shell 未隨 Internet Explorer 3.0 版本更新，因此 Shell32.dll 沒有4.70 版。 Shell32.dll 版本4.71 和4.72 隨附于對應的 Internet Explorer 版本，但不一定會安裝 (請參閱附注 1) 。 若為 Microsoft Internet Explorer 4.01 和 Windows 98 的發行版本，Shell32.dll 和 Shlwapi.dll 分離的版本號碼。 一般而言，您應該假設 Dll 具有不同的版本號碼，並個別測試每一個。

#### <a name="shell32dll"></a>Shell32.dll

| 版本 | 散發平臺                                                       |
|---------|-----------------------------------------------------------------------------|
| 4.0     | Windows 95 和 Microsoft Windows NT 4。0                                     |
| 4.71    | Microsoft Internet Explorer 4.0。 請參閱注意 1。                                |
| 4.72    | Internet Explorer 4.01 和 Windows 98。 請參閱注意 1。                          |
| 5.0     | Windows 2000 和 Windows Millennium Edition (Windows Me) 。 請參閱附注2。       |
| 6.0     | Windows XP                                                                  |
| 6.0.1   | Windows Vista                                                               |
| 6.1     | Windows 7                                                                   |

#### <a name="shlwapidll"></a>Shlwapi.dll

| 版本 | 散發平臺                                                       |
|---------|-----------------------------------------------------------------------------|
| 4.0     | Windows 95 和 Microsoft Windows NT 4。0                                     |
| 4.71    | Internet Explorer 4.0。 請參閱注意 1。                                          |
| 4.72    | Internet Explorer 4.01 和 Windows 98。 請參閱注意 1。                          |
| 4.7     | Internet Explorer 3。x                                                       |
| 5.0     | Microsoft Internet Explorer 5 與 Windows 98 SE。 請參閱附注2。                |
| 5.5     | Microsoft Internet Explorer 5.5 和 Windows Millennium Edition (Windows Me)  |
| 6.0     | Windows XP 和 Windows Vista                                                |



**附注1：** 所有具有 Internet Explorer 4.0 或4.01 的系統都會分別) Shlwapi.dll (4.71 或4.72 的相關版本。 不過，對於 Windows 98 之前的系統，Internet Explorer 4.0 和4.01 可以安裝，或不使用所謂的 *整合式 Shell*。 如果 Internet Explorer 是與整合式 Shell 一起安裝，則也會安裝 Shell32.dll (4.71 或 4.72) 相關聯的版本。 如果 Internet Explorer 是在沒有整合式 Shell 的情況下安裝，Shell32.dll 會保持為4.0 版。 換句話說，系統上的 Shlwapi.dll 版本4.71 或4.72 不保證 Shell32.dll 具有相同的版本號碼。 所有 Windows 98 系統都有4.72 版的 Shell32.dll。

**附注2：** Shlwapi.dll 的5.0 版是以 Internet Explorer 5 散發，並在安裝 Internet Explorer 5 的所有系統上找到，但 Windows 2000 除外。 5.0 版的 Shell32.dll 是以 Windows 2000 和 Windows Millennium Edition 原生散發， (Windows Me) ，以及 Shlwapi.dll 版本5.0。

## <a name="using-dllgetversion-to-determine-the-version-number"></a>使用 DllGetVersion 來判斷版本號碼

從版本4.71 開始，Shell Dll 和其他版本會開始匯出 [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc)。 應用程式可以呼叫這個函式來判斷系統上有哪些 DLL 版本。

> [!Note]  
> Dll 不一定會匯出 [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc)。 請一律先測試它，再嘗試使用它。

針對 windows 2000 之前的 Windows 版本， [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) 會傳回 [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) 結構，其中包含主要和次要版本號碼、組建編號和平臺識別碼。 如果是 Windows 2000 和更新版本的系統， **DllGetVersion** 可能會傳回 [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) 結構。 除了透過 **DLLVERSIONINFO** 提供的資訊之外， **DLLVERSIONINFO2** 也會提供可識別最新安裝 service pack 的修正程式編號，以提供更健全的方式來比較版本號碼。 由於 **DLLVERSIONINFO2** 的第一個成員是 **DLLVERSIONINFO** 結構，因此之後的結構會回溯相容。

### <a name="using-dllgetversion"></a>使用 DllGetVersion

下列範例函數 `GetVersion` 會載入指定的 DLL，並嘗試呼叫其 [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) 函式。 如果成功，它會使用宏將 [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) 結構中的主要和次要版本號碼，封裝至傳回給呼叫應用程式的 **DWORD** 。 如果 DLL 未匯出 **DllGetVersion**，函數會傳回零。 在 Windows 2000 和更新版本的系統中，您可以修改函式來處理 **DllGetVersion** 傳回 [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) 結構的可能性。 如果是的話，請使用該 **DLLVERSIONINFO2** 結構的 **ullVersion** 成員中的資訊來比較版本、組建編號和 service pack 版本。 [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull)宏可簡化將這些值與 **ullVersion** 中的值進行比較的工作。

> [!Note]  
> 不當使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會造成安全性風險。 請參閱 **LoadLibrary** 檔，以取得如何使用不同版本的 Windows 正確載入 dll 的相關資訊。


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```


下列程式碼範例說明如何使用 `GetVersion` 來測試 Shell32.dll 是否為6.0 版或更新版本。


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a>專案版本

為了確保您的應用程式與 .dll 檔案的不同目標版本相容，版本宏會出現在標頭檔中。 這些宏可用來定義、排除或重新定義不同版本 DLL 的特定定義。 如需這些宏的深入說明，請參閱 [使用 Windows 標頭](../winprog/using-the-windows-headers.md) 。

例如，宏名稱 **\_ WIN32 \_ IE** 通常會在較舊的標頭中找到。 您必須負責將巨集定義為十六進位數位。 此版本號碼會定義使用 DLL 的應用程式目標版本。 下表顯示可用的版本號碼，以及每一個應用程式的效果。


| 版本 | 描述                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0200  | 應用程式與 Shell32.dll 4.00 版和更新版本相容。 應用程式無法執行4.00 版之後加入的功能。                                              |
| 0x0300  | 應用程式與 Shell32.dll 4.70 版和更新版本相容。 應用程式無法執行4.70 版之後加入的功能。                                              |
| 0x0400  | 應用程式與 Shell32.dll 4.71 版和更新版本相容。 應用程式無法執行4.71 版之後加入的功能。                                              |
| 0x0401  | 應用程式與 Shell32.dll 4.72 版和更新版本相容。 應用程式無法執行4.72 版之後加入的功能。                                              |
| 0x0500  | 應用程式與 Shell32.dll 和 Shlwapi.dll 5.0 版和更新版本相容。 應用程式無法執行在5.0 版的 Shell32.dll 和 Shlwapi.dll 之後加入的功能。 |
| 0x0501  | 應用程式與 Shell32.dll 和 Shlwapi.dll 5.0 版和更新版本相容。 應用程式無法執行在5.0 版的 Shell32.dll 和 Shlwapi.dll 之後加入的功能。 |
| 0x0600  | 應用程式與 Shell32.dll 和 Shlwapi.dll 6.0 版和更新版本相容。 應用程式無法執行在6.0 版的 Shell32.dll 和 Shlwapi.dll 之後加入的功能。 |


如果您未在專案中定義 **\_ WIN32 \_ IE** 宏，則會自動將其定義為0x0500。 若要定義不同的值，您可以將下列程式檔加入至 make 檔案中的編譯器指示詞。以所需的0x0400 版本號碼取代。

```
/D _WIN32_IE=0x0400
```

另一種方法是在包含 Shell 標頭檔之前，在原始程式碼中加入類似下列的程式程式碼。 以所需的0x0400 版本號碼取代。

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
