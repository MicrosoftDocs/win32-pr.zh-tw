---
description: MyHandleError 函式是用來列印錯誤訊息並結束呼叫程式的工具函式範例。
ms.assetid: 7b28509f-a77f-4b60-90d4-18edaa6d1a2d
title: MyHandleError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 047c9642a1b19c2af4a6e5ef2134ca305c472c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988987"
---
# <a name="myhandleerror"></a>MyHandleError

**MyHandleError** 函式是用來列印錯誤訊息並結束呼叫程式的工具函式範例。 在 [密碼編譯參考](cryptography-reference.md) 中，有數個 CryptoAPI 函式的範例，以及 [使用加密](using-cryptography.md) 功能的更多擴充範例都會執行此函式。 實際的應用程式可能需要更複雜的錯誤處理功能。


```C++
#include <stdio.h>
#include <tchar.h>
#include <windows.h>

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError

```



 

 



