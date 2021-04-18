---
title: '使用色彩管理模組 (CMM) '
description: 色彩管理模組 (Cmm) 是 WCS 程式碼的模組，該程式碼會使用裝置設定檔中的資訊來執行色彩轉換和色彩對應。
ms.assetid: df119e1a-b6f5-40a3-8852-8a57b21483d0
keywords:
- 'Windows Color System (WCS) 、色彩管理模組 (CMM) '
- 'WCS (Windows 色彩系統) 、色彩管理模組 (CMM) '
- '影像色彩管理、色彩管理模組 (CMM) '
- '色彩管理、色彩管理模組 (CMM) '
- '色彩、色彩管理模組 (CMM) '
- '色彩管理模組 (CMM) '
- " (色彩管理模組) 的 CMM"
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518558305639f0699358f22fb3544698741cfedf
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/02/2021
ms.locfileid: "106976387"
---
# <a name="using-color-management-modules-cmm"></a>使用色彩管理模組 (CMM) 

色彩管理模組 (Cmm) 是 WCS 程式碼的模組，該程式碼會使用裝置設定檔中的資訊來執行色彩轉換和色彩對應。 應用程式開發人員應該不需要執行 Cmm。 Microsoft 提供預設的 CMM。 但是，如果您需要使用特殊色彩轉換和色彩對應演算法來撰寫軟體，您可以建立一個。

> [!Note]  
> CMM 進入點 *並非* API 函式，而且不應該由應用程式呼叫。

 

當安裝 Cmm 時，安裝程式會在 Windows 登錄中註冊它們。 應用程式可以列舉已註冊的 Cmm，並使用 [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) 函式選取其中一個。 下列範例應用程式示範如何列舉所有已註冊的 Cmm。


```C++
#include <stdio.h>
#include <stdlib.h>
#include <stddef.h>
#include <string.h>
#include <mbstring.h>
#include <windows.h>
#include <icm.h>

#ifdef WINDOWS_98
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\ICM\\ICMatchers");
#else
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ICMatchers");
#endif

_CRTAPI1 main (int argc, char *argv[])
{
    DWORD dwNumCMM = 0;

    HANDLE hkCMM;
    DWORD dwErr = RegCreateKey(HKEY_LOCAL_MACHINE,
                 gszICMatcher, &amp;hkCMM);
    DWORD dwMaxName, dwMaxValue;
    DWORD dwInfoErr = RegQueryInfoKey(&amp;hkCMM, NULL, NULL,
                                NULL, NULL, NULL, NULL, NULL,
                                &amp;dwMaxName, &amp;dwMaxValue,
                                NULL, NULL);
    TCHAR chCMM[dwMaxName];
    ULONG cjCMM = sizeof(chCMM)/sizeof(chCMM[0]);
    DWORD dwType;
    TCHAR chCMMFile[dwMaxValue];
    ULONG cjCMMFile = sizeof(chCMMFile)/sizeof(chCMMFile[0]);

    if (dwErr != ERROR_SUCCESS)
    {
        printf("Could not open ICMatcher registry key: %d\n", dwErr);
    }

    if (dwErr == ERROR_SUCCESS)
    {
        while (RegEnumValue(
                   hkCMM,dwNumCMM,chCMM,
                   &amp;cjCMM,NULL,&amp;dwType,
                   chCMMFile,&amp;cjCMMFile) == ERROR_SUCCESS)
        {
            if (dwType == REG_SZ)
            {
                printf("%d: %-80s - %-80s\n",dwNumCMM,chCMM,chCMMFile);
            }
            else
            {
                printf("%d: error\n");
            }

            dwNumCMM++;
            cjCMM = sizeof(chCMM);
            cjCMMFile = sizeof(chCMMFile);
        }
    }

    RegCloseKey(hkCMM);
}
```



 

 




