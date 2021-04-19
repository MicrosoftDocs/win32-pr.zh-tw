---
description: 下列範例會使用 VerifyVersionInfo 函數來判斷指定的產品套件 (s) 是否安裝在本機電腦上。
ms.assetid: 9f405e99-28f5-4415-a274-682b87ae6842
title: 偵測產品套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594acbe22283e1c2a3be3ce60116076b2de6f3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997284"
---
# <a name="detecting-a-product-suite"></a><span data-ttu-id="92a9b-103">偵測產品套件</span><span class="sxs-lookup"><span data-stu-id="92a9b-103">Detecting a Product Suite</span></span>

<span data-ttu-id="92a9b-104">下列範例會使用 [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) 函數來判斷指定的產品套件 (s) 是否安裝在本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="92a9b-104">The following example uses the [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) function to determine whether the specified product suite(s) are installed on the local computer.</span></span>

<span data-ttu-id="92a9b-105">此範例會使用 VER \_ 和旗標。</span><span class="sxs-lookup"><span data-stu-id="92a9b-105">This example uses the VER\_AND flag.</span></span> <span data-ttu-id="92a9b-106">如果套件遮罩中指定了兩個旗標，則只有在兩個產品套件都存在時，函式才會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="92a9b-106">If two flags are specified in the suite mask, the function returns **TRUE** only if both product suites are present.</span></span> <span data-ttu-id="92a9b-107">如果範例已變更為使用 VER \_ 或旗標，則如果有任何一個產品套件， [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="92a9b-107">If the example were changed to use the VER\_OR flag, [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) would return **TRUE** if either product suite were present.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL CheckProductSuite ( WORD wSuite ) 
{
  OSVERSIONINFOEX osvi;
  DWORDLONG dwlConditionMask = 0;

  // Initialize the OSVERSIONINFOEX structure.

  ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
  osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
  osvi.wSuiteMask = wSuite;

  // Set up the condition mask.

  VER_SET_CONDITION( dwlConditionMask, 
          VER_SUITENAME, VER_AND );

  // Perform the test.

  return VerifyVersionInfo(
          &osvi, 
          VER_SUITENAME,
          dwlConditionMask);
}

void main()
{
    if( CheckProductSuite(VER_SUITE_ENTERPRISE) )
        printf( "The system meets the requirements.\n" );
    else printf( "The system does not meet the requirements.\n");
}
```



 

 



