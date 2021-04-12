---
title: 偵測 Windows Media 安裝程式的安裝狀態
description: 偵測 Windows Media 安裝程式的安裝狀態
ms.assetid: c3acc268-934b-4a10-aab5-4b1764cb4c87
keywords:
- Windows Media Player，偵測安裝狀態
- Windows Media Player，設定狀態
- Windows Media Player，轉散發軟體
- Windows Media Player，軟體轉散發
- 偵測安裝狀態
- 設定狀態
- 轉散發軟體
- 軟體轉散發
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28a4df9b842a1b6491a0ec98ca0a3182630c389
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372558"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a><span data-ttu-id="58931-111">偵測 Windows Media 安裝程式的安裝狀態</span><span class="sxs-lookup"><span data-stu-id="58931-111">Detecting Setup Status for Windows Media Setup</span></span>

<span data-ttu-id="58931-112">下列程式碼可搭配 Windows Media Player 轉散發套件使用。</span><span class="sxs-lookup"><span data-stu-id="58931-112">The following code can be used with the Windows Media Player redistribution packages.</span></span> <span data-ttu-id="58931-113">安裝狀態會儲存在 **InstallResult** 登錄專案的下列子機碼底下：</span><span class="sxs-lookup"><span data-stu-id="58931-113">The installation status is stored in the **InstallResult** registry entry under the following subkey:</span></span>

<span data-ttu-id="58931-114">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ 安裝程式**</span><span class="sxs-lookup"><span data-stu-id="58931-114">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Setup**</span></span>

<span data-ttu-id="58931-115">**InstallResult** 登錄專案具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="58931-115">The **InstallResult** registry entry has the following form.</span></span>



| <span data-ttu-id="58931-116">名稱</span><span class="sxs-lookup"><span data-stu-id="58931-116">Name</span></span>              | <span data-ttu-id="58931-117">類型</span><span class="sxs-lookup"><span data-stu-id="58931-117">Type</span></span>           | <span data-ttu-id="58931-118">值</span><span class="sxs-lookup"><span data-stu-id="58931-118">Value</span></span>                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58931-119">**InstallResult**</span><span class="sxs-lookup"><span data-stu-id="58931-119">**InstallResult**</span></span> | <span data-ttu-id="58931-120">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="58931-120">**REG\_DWORD**</span></span> | <span data-ttu-id="58931-121">**HRESULT** ，指出 Windows Media Player 安裝是否成功，以及是否需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="58931-121">An **HRESULT** that indicates whether Windows Media Player installation was successful and whether a restart is needed.</span></span> |



 

<span data-ttu-id="58931-122">以下是可併入呼叫安裝應用程式中的 c + + 程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="58931-122">Here is example C++ code that could be incorporated into a calling setup application.</span></span> <span data-ttu-id="58931-123">這段程式碼會 `fSuccess` `fRebootNeeded` 根據元件轉散發套件中 Windows Media Player 安裝程式所寫入的 **HRESULT** 值，適當地將和變數設為 **true** 或 **false**。</span><span class="sxs-lookup"><span data-stu-id="58931-123">This code will set the `fSuccess` and `fRebootNeeded` variables to **true** or **false**, as appropriate, based on the **HRESULT** value written by Windows Media Player Setup in the component redistribution package.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
 
// If NS_S_REBOOT_REQUIRED is undefined, use 0xD2AF9.
#ifndef NS_S_REBOOT_REQUIRED
#define NS_S_REBOOT_REQUIRED       0xd2af9
#endif
 
int main( void )
{
    HKEY hKey = NULL;
    BOOL fSuccess = FALSE;
    BOOL fRebootNeeded = FALSE;
 
if( ERROR_SUCCESS == RegOpenKeyExA( 
                         HKEY_CURRENT_USER, 
                         "Software\\Microsoft\\MediaPlayer\\Setup", 
                         0, KEY_QUERY_VALUE, &hKey ))
    {
        char szResult[64];
        DWORD dwResult = sizeof( szResult );
 
if( ERROR_SUCCESS == RegQueryValueExA( 
                         hKey, "InstallResult", NULL, NULL, 
                         (LPBYTE)szResult, &dwResult ) )
        {
            sscanf_s( szResult, "%x", &dwResult );
            fSuccess = SUCCEEDED( dwResult );
            fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwResult );
        }
 
        RegCloseKey( hKey );
    }
 
    if( fSuccess )
    {
        printf( "Setup Succeeded..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
    else
    {
        printf( "Setup Failed..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="58931-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="58931-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58931-125">**轉散發 Windows Media Player 軟體**</span><span class="sxs-lookup"><span data-stu-id="58931-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




