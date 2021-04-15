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
# <a name="detecting-the-remote-desktop-services-environment"></a><span data-ttu-id="1385e-103">偵測遠端桌面服務環境</span><span class="sxs-lookup"><span data-stu-id="1385e-103">Detecting the Remote Desktop Services environment</span></span>

<span data-ttu-id="1385e-104">為了將效能優化，應用程式可以偵測它們是否在遠端桌面服務用戶端會話中執行，是很好的作法。</span><span class="sxs-lookup"><span data-stu-id="1385e-104">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span> <span data-ttu-id="1385e-105">例如，當應用程式在遠端會話上執行時，應該消除不必要的圖形效果，如 [圖形效果](graphic-effects.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="1385e-105">For example, when an application is running on a remote session, it should eliminate unnecessary graphic effects, as described in [Graphic Effects](graphic-effects.md).</span></span> <span data-ttu-id="1385e-106">如果使用者在本機環境中執行應用程式，則應用程式不一定要將其行為優化。</span><span class="sxs-lookup"><span data-stu-id="1385e-106">If the user is running the application in a local environment, it is not as critical for the application to optimize its behavior.</span></span>

<span data-ttu-id="1385e-107">下列範例顯示的函式會在遠端會話中執行應用程式時傳回 **TRUE** ，如果應用程式是在主控台上執行，則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1385e-107">The following example shows a function that returns **TRUE** if the application is running in a remote session and **FALSE** if the application is running on the console.</span></span>


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



<span data-ttu-id="1385e-108">如需詳細資訊，請參閱 [執行時間連結至 Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md)。</span><span class="sxs-lookup"><span data-stu-id="1385e-108">For more information, see [Run-time Linking to Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span></span>

<span data-ttu-id="1385e-109">您不應該使用 **GetSystemMetrics (SM \_ REMOTESESSION)** 來判斷您的應用程式是否正在 Windows 8 和更新版本或 Windows Server 2012 及更新版本的遠端會話中執行，如果遠端會話也可以使用 Microsoft 遠端顯示通訊協定 (RDP) 的 RemoteFX vGPU 增強功能。</span><span class="sxs-lookup"><span data-stu-id="1385e-109">You should not use **GetSystemMetrics(SM\_REMOTESESSION)** to determine if your application is running in a remote session in Windows 8 and later or Windows Server 2012 and later if the remote session may also be using the RemoteFX vGPU improvements to the Microsoft Remote Display Protocol (RDP).</span></span> <span data-ttu-id="1385e-110">在此情況下， **GetSystemMetrics (SM \_ REMOTESESSION)** 會將遠端會話識別為本機會話。</span><span class="sxs-lookup"><span data-stu-id="1385e-110">In this case, **GetSystemMetrics(SM\_REMOTESESSION)** will identify the remote session as a local session.</span></span>

<span data-ttu-id="1385e-111">您的應用程式可以檢查下列登錄機碼，以判斷會話是否為使用 RemoteFX vGPU 的遠端會話。</span><span class="sxs-lookup"><span data-stu-id="1385e-111">Your application can check the following registry key to determine whether the session is a remote session that uses RemoteFX vGPU.</span></span> <span data-ttu-id="1385e-112">如果本機會話存在，此登錄機碼會提供本機會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1385e-112">If a local session exists, this registry key provides the ID of the local session.</span></span>

<span data-ttu-id="1385e-113">**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Terminal Server \\ GlassSessionId**</span><span class="sxs-lookup"><span data-stu-id="1385e-113">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Terminal Server\\GlassSessionId**</span></span>

<span data-ttu-id="1385e-114">如果目前正在執行應用程式的會話識別碼與登錄機碼中的識別碼相同，則表示應用程式正在本機會話中執行。</span><span class="sxs-lookup"><span data-stu-id="1385e-114">If the ID of the current session in which the application is running is the same as in the registry key, the application is running in a local session.</span></span> <span data-ttu-id="1385e-115">以這種方式識別為遠端會話的會話包含使用 RemoteFX vGPU 的遠端會話。</span><span class="sxs-lookup"><span data-stu-id="1385e-115">Sessions identified as remote session in this way include remote sessions that use RemoteFX vGPU.</span></span> <span data-ttu-id="1385e-116">下列範例程式碼示範這項功能。</span><span class="sxs-lookup"><span data-stu-id="1385e-116">The following sample code demonstrates this.</span></span>


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



 

 




