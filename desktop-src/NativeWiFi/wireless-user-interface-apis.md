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
# <a name="wireless-user-interface-apis"></a><span data-ttu-id="9076a-103">無線消費者介面 Api</span><span class="sxs-lookup"><span data-stu-id="9076a-103">Wireless User Interface APIs</span></span>

<span data-ttu-id="9076a-104">Windows 8、Windows Server 2012 及更新版本包含新的連線管理員功能，可讓使用者輕鬆地連接到網際網路和其他網路 (工作和家用網路，例如) 。</span><span class="sxs-lookup"><span data-stu-id="9076a-104">Windows 8, Windows Server 2012, and later include a new Connection Manager feature that allows users to easily connect to the Internet and to other networks (work and home networks, for example).</span></span> <span data-ttu-id="9076a-105">這項新的連線管理員功能取代了較舊的 **網路** 連線，以及管理舊版 Windows 隨附的 **無線網路** 使用者介面，以管理原生 Wifi 連線。</span><span class="sxs-lookup"><span data-stu-id="9076a-105">This new Connection Manager feature replaces the older **Connect to a network** and **Manage Wireless Networks** user interfaces included with older versions of Windows for managing Native Wifi connections.</span></span>

<span data-ttu-id="9076a-106">在 Windows 7、Windows Server 2008 和 Windows Vista 上，有許多使用者介面 (Ui) 用來連接或設定無線網路。</span><span class="sxs-lookup"><span data-stu-id="9076a-106">On Windows 7, Windows Server 2008, and Windows Vista, there are a number of user interfaces (UIs) used to connect to or configure a wireless network.</span></span> <span data-ttu-id="9076a-107">這些 Ui 可以在使用原生 Wifi 和 Windows Shell 函式的應用程式中啟動。</span><span class="sxs-lookup"><span data-stu-id="9076a-107">These UIs can be started in an application using Native Wifi and Windows Shell functions.</span></span> <span data-ttu-id="9076a-108">這些 Ui 無法在 Windows 8、Windows Server 2012 及更新版本上使用。</span><span class="sxs-lookup"><span data-stu-id="9076a-108">These UIs are not available on Windows 8, Windows Server 2012, and later.</span></span>

<span data-ttu-id="9076a-109">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 您無法在應用程式中以程式設計方式啟動用來連接或設定無線網路的任何 UI。</span><span class="sxs-lookup"><span data-stu-id="9076a-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** You cannot start any UI used to connect to or configure a wireless network in an application programmatically.</span></span>

## <a name="connect-to-a-network"></a><span data-ttu-id="9076a-110">連線至網路</span><span class="sxs-lookup"><span data-stu-id="9076a-110">Connect to a network</span></span>

<span data-ttu-id="9076a-111">在 Windows 8、Windows Server 2012、Windows 7、Windows Server 2008 和 Windows Vista 上，[ **連接到網路** ] 嚮導可以用來建立無線網路的連線。</span><span class="sxs-lookup"><span data-stu-id="9076a-111">On Windows 8, Windows Server 2012, Windows 7, Windows Server 2008, and Windows Vista, the **Connect to a network** wizard can be used to establish a connection to a wireless network.</span></span> <span data-ttu-id="9076a-112">您可以使用 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) 函式來啟動 [ **連接到網路** ] wizard。</span><span class="sxs-lookup"><span data-stu-id="9076a-112">You can use the [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function to start the **Connect to a network** wizard.</span></span>

<span data-ttu-id="9076a-113">下列程式碼顯示的 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) 呼叫會啟動 [ **連接到網路** ] wizard。</span><span class="sxs-lookup"><span data-stu-id="9076a-113">The following code shows a [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) call that starts the **Connect to a network** wizard.</span></span>


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



## <a name="manage-wireless-networks"></a><span data-ttu-id="9076a-114">**管理無線網路**</span><span class="sxs-lookup"><span data-stu-id="9076a-114">**Manage Wireless Networks**</span></span>

<span data-ttu-id="9076a-115">在 Windows 7、Windows Server 2008 和 Windows Vista 上，[ **管理無線網路** ] 主控台專案用來管理無線網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="9076a-115">On Windows 7, Windows Server 2008, and Windows Vista, the **Manage Wireless Networks** Control Panel item is used to manage wireless network profiles.</span></span> <span data-ttu-id="9076a-116">[**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)函數也可以用來啟動 [**管理無線網路**] 專案。</span><span class="sxs-lookup"><span data-stu-id="9076a-116">The [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function can also be used to start the **Manage Wireless Networks** item.</span></span> <span data-ttu-id="9076a-117">在 Windows 7 和 Windows Vista 上呼叫 **ShellExecute** 時所要使用的路徑如下：</span><span class="sxs-lookup"><span data-stu-id="9076a-117">The path to use when calling **ShellExecute** on Windows 7 and Windows Vista is the following:</span></span>

<span data-ttu-id="9076a-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span><span class="sxs-lookup"><span data-stu-id="9076a-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span></span>

<span data-ttu-id="9076a-119">下列範例程式碼示範如何使用 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) 從應用程式啟動 [ **受控無線網路** ] wizard。</span><span class="sxs-lookup"><span data-stu-id="9076a-119">The following sample code shows how to use [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to start the **Managed Wireless Networks** wizard from an application.</span></span>


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



## <a name="advanced-settings-for-wireless-network-profiles"></a><span data-ttu-id="9076a-120">無線網路設定檔的 Advanced Settings</span><span class="sxs-lookup"><span data-stu-id="9076a-120">Advanced Settings for Wireless Network Profiles</span></span>

<span data-ttu-id="9076a-121">Windows Vista 和更新版本包含 advanced 使用者介面，可用來查看和編輯無線網路設定檔的 advanced 設定。</span><span class="sxs-lookup"><span data-stu-id="9076a-121">Windows Vista and later include an advanced user interface that is used to view and edit advanced settings of a wireless network profile.</span></span> <span data-ttu-id="9076a-122">您可以藉由呼叫 [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) 函數來啟動這個 advanced UI。</span><span class="sxs-lookup"><span data-stu-id="9076a-122">You can start this advanced UI by calling the [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9076a-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="9076a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9076a-124">使用原生 Wifi</span><span class="sxs-lookup"><span data-stu-id="9076a-124">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="9076a-125">無線設定檔範例</span><span class="sxs-lookup"><span data-stu-id="9076a-125">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

[<span data-ttu-id="9076a-126">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="9076a-126">**ShellExecute**</span></span>](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[<span data-ttu-id="9076a-127">**WlanUIEditProfile**</span><span class="sxs-lookup"><span data-stu-id="9076a-127">**WlanUIEditProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
