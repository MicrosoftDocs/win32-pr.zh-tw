---
title: 偵測遠端桌面服務環境
description: 為了將效能優化，應用程式可以偵測它們是否在遠端桌面服務用戶端會話中執行，是很好的作法。
ms.assetid: 9ba03801-8471-43a9-8e24-114a082d5776
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fde3263925a3b8bf4921dd0dfc95842a5dc5b4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507236"
---
# <a name="detecting-the-remote-desktop-services-environment"></a>偵測遠端桌面服務環境

為了將效能優化，應用程式可以偵測它們是否在遠端桌面服務用戶端會話中執行，是很好的作法。 例如，當應用程式在遠端會話上執行時，應該消除不必要的圖形效果，如 [圖形效果](graphic-effects.md)中所述。 如果使用者在本機環境中執行應用程式，則應用程式不一定要將其行為優化。

下列範例顯示的函式會在遠端會話中執行應用程式時傳回 **TRUE** ，如果應用程式是在主控台上執行，則會傳回 **FALSE** 。


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



如需詳細資訊，請參閱 [執行時間連結至 Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md)。

您不應該使用 **GetSystemMetrics (SM \_ REMOTESESSION)** 來判斷您的應用程式是否正在 Windows 8 和更新版本或 Windows Server 2012 及更新版本的遠端會話中執行，如果遠端會話也可以使用 Microsoft 遠端顯示通訊協定 (RDP) 的 RemoteFX vGPU 增強功能。 在此情況下， **GetSystemMetrics (SM \_ REMOTESESSION)** 會將遠端會話識別為本機會話。

您的應用程式可以檢查下列登錄機碼，以判斷會話是否為使用 RemoteFX vGPU 的遠端會話。 如果本機會話存在，此登錄機碼會提供本機會話的識別碼。

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Terminal Server \\ GlassSessionId**

如果目前正在執行應用程式的會話識別碼與登錄機碼中的識別碼相同，則表示應用程式正在本機會話中執行。 以這種方式識別為遠端會話的會話包含使用 RemoteFX vGPU 的遠端會話。 下列範例程式碼示範這項功能。


```C++
#define TERMINAL_SERVER_KEY _T("SYSTEM\\CurrentControlSet\\Control\\Terminal Server\\")
#define GLASS_SESSION_ID    _T("GlassSessionId")

BOOL
IsCurrentSessionRemoteable()
{
    BOOL fIsRemoteable = FALSE;
                                       
    if (GetSystemMetrics(SM_REMOTESESSION)) 
    {
        fIsRemoteable = TRUE;
    }
    else
    {
        HKEY hRegKey = NULL;
        LONG lResult;

        lResult = RegOpenKeyEx(
            HKEY_LOCAL_MACHINE,
            TERMINAL_SERVER_KEY,
            0, // ulOptions
            KEY_READ,
            &hRegKey
            );

        if (lResult == ERROR_SUCCESS)
        {
            DWORD dwGlassSessionId;
            DWORD cbGlassSessionId = sizeof(dwGlassSessionId);
            DWORD dwType;

            lResult = RegQueryValueEx(
                hRegKey,
                GLASS_SESSION_ID,
                NULL, // lpReserved
                &dwType,
                (BYTE*) &dwGlassSessionId,
                &cbGlassSessionId
                );

            if (lResult == ERROR_SUCCESS)
            {
                DWORD dwCurrentSessionId;

                if (ProcessIdToSessionId(GetCurrentProcessId(), &dwCurrentSessionId))
                {
                    fIsRemoteable = (dwCurrentSessionId != dwGlassSessionId);
                }
            }
        }

        if (hRegKey)
        {
            RegCloseKey(hRegKey);
        }
    }

    return fIsRemoteable;
}
```



 

 




