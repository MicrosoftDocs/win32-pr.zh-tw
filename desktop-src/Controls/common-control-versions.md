---
title: 通用控制項版本
description: 本主題列出通用控制項程式庫 (ComCtl32.dll) 的可用版本，說明如何識別您應用程式所使用的版本，並說明如何以特定版本的應用程式為目標。
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1131466bd4d3afcaae3a241a6f7854fd5a49450
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423958"
---
# <a name="common-control-versions"></a>通用控制項版本

本主題列出通用控制項程式庫 (ComCtl32.dll) 的可用版本，說明如何識別您應用程式所使用的版本，並說明如何以特定版本的應用程式為目標。

本主題包含下列各節。

-   [通用控制項 DLL 版本號碼](#common-control-dll-versions-numbers)
-   [不同通用控制項版本的結構大小](#structure-sizes-for-different-common-control-versions)
-   [使用 DllGetVersion 來判斷版本號碼](#using-dllgetversion-to-determine-the-version-number)
-   [專案版本](#project-versions)
-   [相關主題](#related-topics)

## <a name="common-control-dll-versions-numbers"></a>通用控制項 DLL 版本號碼

通用控制項的支援是由 ComCtl32.dll 所提供，所有32位和64位版本的 Windows 都包含在內。 每個後續版本的 DLL 都支援舊版的功能和 API，並加入新功能。

因為不同版本的 ComCtl32.dll 是隨著 Internet Explorer 散發，所以作用中的版本有時會與作業系統隨附的版本不同。 因此，您的應用程式必須直接判斷存在的 ComCtl32.dll 版本。

在通用控制項參考檔中，許多程式設計專案會指定支援的最低 DLL 版本號碼。 此版本號碼表示程式設計專案會在該版本和後續 DLL 版本中執行，除非另有指定。 如果未指定版本號碼，則會在所有現有版本的 DLL 中執行程式設計專案。

下表概述不同的 DLL 版本，以及它們在支援的作業系統上的散發方式。



ComCtl32.dll

版本

散發平臺

5.81

Microsoft Internet Explorer 5.01、Microsoft Internet Explorer 5.5 和 Microsoft Internet Explorer 6

5.82

Windows Server 2003、Windows Vista、Windows Server 2008 和 Windows 7

6.0

Windows Server 2003

6.10

Windows Vista、Windows Server 2008 和 Windows 7



 

## <a name="structure-sizes-for-different-common-control-versions"></a>不同通用控制項版本的結構大小

對通用控制項進行持續的增強，會導致需要擴充許多結構。 基於這個理由，結構的大小在不同版本的 Commctrl 之間已變更。 因為大部分的通用控制項結構都採用結構大小做為其中一個參數，所以如果無法辨識大小，訊息或函式可能會失敗。 為了解決這個情況，已定義結構大小常數以協助以不同版本的 ComCtl32.dll 為目標。 下列清單會定義結構大小常數。



|    結構大小常數                           |     定義                                                                                         |
|-------------------------------|----------------------------------------------------------------------------------------------|
| HDITEM \_ V1 \_ 大小              | 4.0 版中 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構的大小。                           |
| IMAGELISTDRAWPARAMS \_ V3 \_ 大小 | 5.9 版中 [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) 結構的大小。 |
| LVCOLUMN \_ V1 \_ 大小            | 4.0 版中 [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) 結構的大小。                       |
| LVGROUP \_ V5 \_ 大小             | 6.0 版中 [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) 結構的大小。                         |
| LVHITTESTINFO \_ V1 \_ 大小       | 4.0 版中 [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) 結構的大小。             |
| LVITEM \_ V1 \_ 大小              | 4.0 版中 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構的大小。                           |
| LVITEM \_ V5 \_ 大小              | 6.0 版中 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構的大小。                           |
| LVTILEINFO \_ V5 \_ 大小          | 6.0 版中 [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) 結構的大小。                   |
| MCHITTESTINFO \_ V1 \_ 大小       | 4.0 版中 [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) 結構的大小。             |
| NMLVCUSTOMDRAW \_ V3 \_ 大小      | 4.7 版中 [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) 結構的大小。           |
| NMTTDISPINFO \_ V1 \_ 大小        | 4.0 版中 [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) 結構的大小。               |
| NMTVCUSTOMDRAW \_ V3 \_ 大小      | 4.7 版中 [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) 結構的大小。           |
| PROPSHEETHEADER \_ V1 \_ 大小     | 4.0 版中 [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) 結構的大小。         |
| PROPSHEETPAGE \_ V1 \_ 大小       | 4.0 版中 [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) 結構的大小。             |
| REBARBANDINFO \_ V3 \_ 大小       | 4.7 版中 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) 結構的大小。             |
| REBARBANDINFO \_ V6 \_ 大小       | 6.0 版中 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) 結構的大小。             |
| TTTOOLINFO \_ V1 \_ 大小          | 4.0 版中 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構的大小。                       |
| TTTOOLINFO \_ V2 \_ 大小          | 4.7 版中 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構的大小。                       |
| TTTOOLINFO \_ V3 \_ 大小          | 6.0 版中 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構的大小。                       |
| TVINSERTSTRUCT \_ V1 \_ 大小      | 4.0 版中 [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) 結構的大小。           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a>使用 DllGetVersion 來判斷版本號碼

應用程式可以呼叫 [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) 函式來判斷系統上有哪些 DLL 版本。

[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) 會傳回 [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) 結構。 除了透過 [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo)提供的資訊之外， **DLLVERSIONINFO2** 也會提供可識別最新安裝 service pack 的修正程式編號，以提供更健全的方式來比較版本號碼。 由於 **DLLVERSIONINFO2** 的第一個成員是 **DLLVERSIONINFO** 結構，因此之後的結構會回溯相容。


下列範例函數 `GetVersion` 會載入指定的 DLL，並嘗試呼叫其 [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) 函式。 如果成功，它會使用宏將 [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) 結構中的主要和次要版本號碼，封裝至傳回給呼叫應用程式的 **DWORD** 。 如果 DLL 未匯出 **DllGetVersion**，函數會傳回零。 您可以修改函數來處理 **DllGetVersion** 傳回 [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) 結構的可能性。 如果是的話，請使用該 **DLLVERSIONINFO2** 結構的 **ullVersion** 成員中的資訊來比較版本、組建編號和 service pack 版本。 [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull)宏可簡化將這些值與 **ullVersion** 中的值進行比較的工作。

> [!Note]  
> 不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會造成安全性風險。 請參閱 **LoadLibrary** 檔，以取得如何使用不同版本的 Windows 正確載入 dll 的相關資訊。

 


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

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

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



下列程式碼範例會示範如何使用 `GetVersion` 來測試 ComCtl32.dll 是否為6.0 版或更新版本。


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a>專案版本

為了確保您的應用程式與 .dll 檔案的不同目標版本相容，版本宏會出現在標頭檔中。 這些宏可用來定義、排除或重新定義不同版本 DLL 的特定定義。 如需這些宏的深入說明，請參閱 [使用 Windows 標頭](/windows/desktop/WinProg/using-the-windows-headers) 。

例如，宏名稱 **\_ WIN32 \_ IE** 通常會在較舊的標頭中找到。 您必須負責將巨集定義為十六進位數位。 此版本號碼會定義使用 DLL 的應用程式目標版本。 下表顯示可用的版本號碼，以及每一個應用程式的效果。



| 版本 | 描述                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0300  | 應用程式與 ComCtl32.dll 4.70 版和更新版本相容。 應用程式無法執行4.70 版之後加入的功能。 |
| 0x0400  | 應用程式與 ComCtl32.dll 4.71 版和更新版本相容。 應用程式無法執行4.71 版之後加入的功能。 |
| 0x0401  | 應用程式與 ComCtl32.dll 4.72 版和更新版本相容。 應用程式無法執行4.72 版之後加入的功能。 |
| 0x0500  | 應用程式與 ComCtl32.dll 5.80 版和更新版本相容。 應用程式無法執行5.80 版之後加入的功能。 |
| 0x0501  | 應用程式與 ComCtl32.dll 5.81 版和更新版本相容。 應用程式無法執行5.81 版之後加入的功能。 |
| 0x0600  | 應用程式與 ComCtl32.dll 6.0 版和更新版本相容。 應用程式無法執行6.0 版之後加入的功能。   |



 

如果您未在專案中定義 **\_ WIN32 \_ IE** 宏，則會自動將其定義為0x0500。 若要定義不同的值，您可以將下列程式檔加入至 make 檔案中的編譯器指示詞。以所需的0x0400 版本號碼取代。


```C++
/D _WIN32_IE=0x0400
```



另一種方法是在包含 Shell 標頭檔之前，在原始程式碼中加入類似下列的程式程式碼。 以所需的0x0400 版本號碼取代。


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於通用控制項](common-controls-intro.md)
</dt> </dl>

 

 