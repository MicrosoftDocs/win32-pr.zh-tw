---
description: Windows 8、Windows Server 2012 及更新版本包含新的連線管理員功能，可讓使用者輕鬆地連接到網際網路和其他網路 (工作和家用網路，例如) 。
ms.assetid: 6b2f5a50-fabd-4c80-acc8-a0883c939632
title: 無線消費者介面 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5814ea8daa55ab3ec1bf431543174cf57fdfa7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514192"
---
# <a name="wireless-user-interface-apis"></a>無線消費者介面 Api

Windows 8、Windows Server 2012 及更新版本包含新的連線管理員功能，可讓使用者輕鬆地連接到網際網路和其他網路 (工作和家用網路，例如) 。 這項新的連線管理員功能取代了較舊的 **網路** 連線，以及管理舊版 Windows 隨附的 **無線網路** 使用者介面，以管理原生 Wifi 連線。

在 Windows 7、Windows Server 2008 和 Windows Vista 上，有許多使用者介面 (Ui) 用來連接或設定無線網路。 這些 Ui 可以在使用原生 Wifi 和 Windows Shell 函式的應用程式中啟動。 這些 Ui 無法在 Windows 8、Windows Server 2012 及更新版本上使用。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 您無法在應用程式中以程式設計方式啟動用來連接或設定無線網路的任何 UI。

## <a name="connect-to-a-network"></a>連線至網路

在 Windows 8、Windows Server 2012、Windows 7、Windows Server 2008 和 Windows Vista 上，[ **連接到網路** ] 嚮導可以用來建立無線網路的連線。 您可以使用 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) 函式來啟動 [ **連接到網路** ] wizard。

下列程式碼顯示的 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) 呼叫會啟動 [ **連接到網路** ] wizard。


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

void wmain()
{
   ShellExecute(
      NULL, 
      L"open", 
      L"shell:::{21EC2020-3AEA-1069-A2DD-08002B30309D}\\::{38a98528-6cbf-4ca9-8dc0-b1e1d10f7b1b}",
      NULL,
      NULL,
      SW_SHOWNORMAL);
}
```



## <a name="manage-wireless-networks"></a>**管理無線網路**

在 Windows 7、Windows Server 2008 和 Windows Vista 上，[ **管理無線網路** ] 主控台專案用來管理無線網路設定檔。 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)函數也可以用來啟動 [**管理無線網路**] 專案。 在 Windows 7 和 Windows Vista 上呼叫 **ShellExecute** 時所要使用的路徑如下：

`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.

下列範例程式碼示範如何使用 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) 從應用程式啟動 [ **受控無線網路** ] wizard。


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>
#include <stdio.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

int wmain()
{

    //-----------------------------------------
    // Declare and initialize variables
    HINSTANCE nResult;

    PCWSTR lpOperation = L"open";    
    PCWSTR lpFile= 
        L"shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\\3\\::{1fa9085f-25a2-489b-85d4-86326eedcd87}";

    nResult = ShellExecute(
        NULL,   // Hwnd
        lpOperation, // do not request elevation unless needed
        lpFile,
        NULL, // no parameters 
        NULL, // use current working directory 
        SW_SHOWNORMAL);

    if((int)nResult == SE_ERR_ACCESSDENIED)
    {
        wprintf(L"ShellExecute returned access denied\n");
        wprintf(L"  Executing the ShellExecute command elevated\n"); 

        nResult = ShellExecute(
            NULL,
            L"runas", // Trick for requesting elevation
            lpFile,
            NULL, // no parameters 
            NULL, // use current working directory 
            SW_HIDE);
    }

    if ( (int) nResult < 32) {
        wprintf(L" ShellExecute failed with error %d\n", (int) nResult);
        return 1;
    }    
    else {    
        wprintf(L" ShellExecute succeeded and returned value %d\n", (int) nResult);
        return 0;
    }
}

```



## <a name="advanced-settings-for-wireless-network-profiles"></a>無線網路設定檔的 Advanced Settings

Windows Vista 和更新版本包含 advanced 使用者介面，可用來查看和編輯無線網路設定檔的 advanced 設定。 您可以藉由呼叫 [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) 函數來啟動這個 advanced UI。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用原生 Wifi](using-native-wifi.md)
</dt> <dt>

[無線設定檔範例](wireless-profile-samples.md)
</dt> <dt>

[**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
