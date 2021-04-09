---
title: 偵測安裝狀態
description: 偵測安裝狀態
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- Windows Media Format SDK，軟體轉散發
- Advanced Systems Format (ASF) 、軟體轉散發
- ASF (Advanced Systems Format) ，軟體轉散發
- Windows Media Format SDK，轉散發
- Advanced Systems Format (ASF) ，轉散發
- ASF (Advanced Systems Format) ，轉散發
- 軟體轉散發，偵測安裝狀態
- 重新發佈，偵測設定狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6add696f2b2989de1e77d48504a1d540634213d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675679"
---
# <a name="detecting-setup-status"></a><span data-ttu-id="e094f-111">偵測安裝狀態</span><span class="sxs-lookup"><span data-stu-id="e094f-111">Detecting Setup Status</span></span>

<span data-ttu-id="e094f-112">當重新發佈可執行檔在電腦上執行時，它會將其安裝狀態記錄在登錄中作為 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e094f-112">When the redistribution executable runs on a computer, it records its installation status in the registry as an **HRESULT** value.</span></span> <span data-ttu-id="e094f-113">安裝狀態會儲存在 **InstallResult** 登錄專案的下列子機碼底下：</span><span class="sxs-lookup"><span data-stu-id="e094f-113">The installation status is stored in the **InstallResult** registry entry under the following subkey:</span></span>

<span data-ttu-id="e094f-114">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ 安裝程式**</span><span class="sxs-lookup"><span data-stu-id="e094f-114">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Setup**</span></span>

<span data-ttu-id="e094f-115">**InstallResult** 登錄專案具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="e094f-115">The **InstallResult** registry entry has the following form.</span></span>



| <span data-ttu-id="e094f-116">名稱</span><span class="sxs-lookup"><span data-stu-id="e094f-116">Name</span></span>              | <span data-ttu-id="e094f-117">類型</span><span class="sxs-lookup"><span data-stu-id="e094f-117">Type</span></span>           | <span data-ttu-id="e094f-118">值</span><span class="sxs-lookup"><span data-stu-id="e094f-118">Value</span></span>                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e094f-119">**InstallResult**</span><span class="sxs-lookup"><span data-stu-id="e094f-119">**InstallResult**</span></span> | <span data-ttu-id="e094f-120">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e094f-120">**REG\_DWORD**</span></span> | <span data-ttu-id="e094f-121">**HRESULT** ，指出 Windows Media Player 安裝是否成功，以及是否需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="e094f-121">An **HRESULT** that indicates whether Windows Media Player installation was successful and whether a restart is needed.</span></span> |



 

<span data-ttu-id="e094f-122">下列程式碼會根據元件轉散發套件中的 Windows Media 安裝程式所寫入的 **HRESULT** 值，適當地將 *fSucess* 和 *fRebootNeeded* 變數設為 **True** 或 **False**。</span><span class="sxs-lookup"><span data-stu-id="e094f-122">The following code will set the *fSucess* and *fRebootNeeded* variables to **True** or **False**, as appropriate, based on the **HRESULT** value written by Windows Media setup in the component redistribution package.</span></span>


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

    LONG lResult = RegOpenKeyEx( 
        HKEY_CURRENT_USER, 
        TEXT("Software\\Microsoft\\MediaPlayer\\Setup"), 
        0, 
        KEY_QUERY_VALUE, 
        &hKey 
        );

    if ( lResult == ERROR_SUCCESS )
    {
        DWORD dwRegType = 0;   // Registry value type.
        DWORD dwValue = 0;     // Registry value.
        DWORD cbValue = sizeof( dwValue );  // Size of the value in bytes.

        lResult = RegQueryValueEx( 
            hKey, 
            TEXT("InstallResult"), 
            NULL, 
            &dwRegType, 
            (LPBYTE)&dwValue, 
            &cbValue
            );

        if( lResult == ERROR_SUCCESS )
        {
            if (dwRegType == REG_DWORD)
            {
                fSuccess = SUCCEEDED( dwValue );
                fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwValue );
            }
        }

        RegCloseKey( hKey );
    }

    if( fSuccess )
    {
        printf( "Setup succeeded." );
    }
    else
    {
        printf( "Setup failed." );
    }

    if( fRebootNeeded )
    {
        printf( "A reboot IS required.\n" );
    }
    else
    {
        printf( "A reboot IS NOT required.\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="e094f-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="e094f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e094f-124">**軟體轉散發**</span><span class="sxs-lookup"><span data-stu-id="e094f-124">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




