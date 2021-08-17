---
title: 偵測安裝狀態
description: 偵測安裝狀態
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- Windows媒體格式 SDK，軟體轉散發
- Advanced Systems Format (ASF) 、軟體轉散發
- ASF (Advanced Systems Format) ，軟體轉散發
- Windows媒體格式 SDK，轉散發
- Advanced Systems Format (ASF) ，轉散發
- ASF (Advanced Systems Format) ，轉散發
- 軟體轉散發，偵測安裝狀態
- 重新發佈，偵測設定狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250ab87fd81592b868e1dbf13106577f83e680796310aff246f0c1483fa847cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931388"
---
# <a name="detecting-setup-status"></a>偵測安裝狀態

當重新發佈可執行檔在電腦上執行時，它會將其安裝狀態記錄在登錄中作為 **HRESULT** 值。 安裝狀態會儲存在 **InstallResult** 登錄專案的下列子機碼底下：

**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ 安裝程式**

**InstallResult** 登錄專案具有下列格式。



| 名稱              | 類型           | 值                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **REG \_ DWORD** | **HRESULT** ，指出 Windows Media Player 安裝是否成功，以及是否需要重新開機。 |



 

下列程式碼會根據元件轉散發套件中 Windows 媒體安裝程式所寫入的 **HRESULT** 值，適當地將 *fSucess* 和 *fRebootNeeded* 變數設為 **True** 或 **False**。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**軟體轉散發**](software-redistribution.md)
</dt> </dl>

 

 




