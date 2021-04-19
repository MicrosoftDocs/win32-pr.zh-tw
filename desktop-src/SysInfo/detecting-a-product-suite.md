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
# <a name="detecting-a-product-suite"></a>偵測產品套件

下列範例會使用 [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) 函數來判斷指定的產品套件 (s) 是否安裝在本機電腦上。

此範例會使用 VER \_ 和旗標。 如果套件遮罩中指定了兩個旗標，則只有在兩個產品套件都存在時，函式才會傳回 **TRUE** 。 如果範例已變更為使用 VER \_ 或旗標，則如果有任何一個產品套件， [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) 會傳回 **TRUE** 。


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



 

 



