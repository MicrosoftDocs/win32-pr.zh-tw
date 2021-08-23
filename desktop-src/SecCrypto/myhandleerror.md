---
description: MyHandleError 函式是用來列印錯誤訊息並結束呼叫程式的工具函式範例。
ms.assetid: 7b28509f-a77f-4b60-90d4-18edaa6d1a2d
title: MyHandleError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a3c3ad412b6719b59402e820411377c08d2c6b9a17f44771a7156e0b52567a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739658"
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



 

 



