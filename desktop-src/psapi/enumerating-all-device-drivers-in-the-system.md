---
title: 列舉系統中的所有設備磁碟機
description: 下列範例程式碼使用 EnumDeviceDrivers 函式來列舉系統中目前的設備磁碟機。
ms.assetid: 047d8541-e17e-4738-8453-674db69365df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83c2d6629738e0668d2c0e95ec19f10ae0f3cabcb7b842747ae6dc97937c590f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884968"
---
# <a name="enumerating-all-device-drivers-in-the-system"></a>列舉系統中的所有設備磁碟機

下列範例程式碼使用 [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) 函式來列舉系統中目前的設備磁碟機。 它會將從此函式呼叫中抓取的載入位址傳遞至 [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) 函式，以取得可顯示的名稱。


```C++
#include <windows.h>
#include <psapi.h>
#include <tchar.h>
#include <stdio.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

#define ARRAY_SIZE 1024

int main( void )
{
   LPVOID drivers[ARRAY_SIZE];
   DWORD cbNeeded;
   int cDrivers, i;

   if( EnumDeviceDrivers(drivers, sizeof(drivers), &cbNeeded) && cbNeeded < sizeof(drivers))
   { 
      TCHAR szDriver[ARRAY_SIZE];

      cDrivers = cbNeeded / sizeof(drivers[0]);

      _tprintf(TEXT("There are %d drivers:\n"), cDrivers);      
      for (i=0; i < cDrivers; i++ )
      {
         if(GetDeviceDriverBaseName(drivers[i], szDriver, sizeof(szDriver) /              sizeof(szDriver[0])))
         {
            _tprintf(TEXT("%d: %s\n"), i+1, szDriver);
         }
      }
   }
   else 
   {
        _tprintf(TEXT("EnumDeviceDrivers failed; array size needed is %d\n"),             cbNeeded / sizeof(LPVOID));
        return 1;
   }

return 0;
}
```



 

 




