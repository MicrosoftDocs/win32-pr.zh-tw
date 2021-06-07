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
ms.openlocfilehash: 9b12a087bfc972ffcbd7f9fb083a9d73d669f134
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386897"
---
# <a name="using-color-management-modules-cmm"></a><span data-ttu-id="9df1b-110">使用色彩管理模組 (CMM) </span><span class="sxs-lookup"><span data-stu-id="9df1b-110">Using Color Management Modules (CMM)</span></span>

<span data-ttu-id="9df1b-111">色彩管理模組 (Cmm) 是 WCS 程式碼的模組，該程式碼會使用裝置設定檔中的資訊來執行色彩轉換和色彩對應。</span><span class="sxs-lookup"><span data-stu-id="9df1b-111">Color Management Modules (CMMs) are modules of WCS code that use the information in device profiles to perform color conversion and color mapping.</span></span> <span data-ttu-id="9df1b-112">應用程式開發人員應該不需要執行 Cmm。</span><span class="sxs-lookup"><span data-stu-id="9df1b-112">Application developers should not have to implement CMMs.</span></span> <span data-ttu-id="9df1b-113">Microsoft 提供預設的 CMM。</span><span class="sxs-lookup"><span data-stu-id="9df1b-113">Microsoft provides the default CMM.</span></span> <span data-ttu-id="9df1b-114">但是，如果您需要使用特殊色彩轉換和色彩對應演算法來撰寫軟體，您可以建立一個。</span><span class="sxs-lookup"><span data-stu-id="9df1b-114">However, if you do write software that requires the use of specialized color conversion and color mapping algorithms, you may create one.</span></span>

> [!Note]  
> <span data-ttu-id="9df1b-115">CMM 進入點 *並非* API 函式，而且不應該由應用程式呼叫。</span><span class="sxs-lookup"><span data-stu-id="9df1b-115">CMM entry points are *not* API functions and should not be called by applications.</span></span>

 

<span data-ttu-id="9df1b-116">當安裝 Cmm 時，安裝程式會在 Windows 登錄中註冊它們。</span><span class="sxs-lookup"><span data-stu-id="9df1b-116">When CMMs are installed, the installation program registers them in the Windows registry.</span></span> <span data-ttu-id="9df1b-117">應用程式可以列舉已註冊的 Cmm，並使用 [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) 函式選取其中一個。</span><span class="sxs-lookup"><span data-stu-id="9df1b-117">Applications can enumerate the registered CMMs and select one using the [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) function.</span></span> <span data-ttu-id="9df1b-118">下列範例應用程式示範如何列舉所有已註冊的 Cmm。</span><span class="sxs-lookup"><span data-stu-id="9df1b-118">The following sample application demonstrates how to enumerate all registered CMMs.</span></span>


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
                 gszICMatcher, &hkCMM);
    DWORD dwMaxName, dwMaxValue;
    DWORD dwInfoErr = RegQueryInfoKey(&hkCMM, NULL, NULL,
                                NULL, NULL, NULL, NULL, NULL,
                                &dwMaxName, &dwMaxValue,
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
                   &cjCMM,NULL,&dwType,
                   chCMMFile,&cjCMMFile) == ERROR_SUCCESS)
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



 

 




