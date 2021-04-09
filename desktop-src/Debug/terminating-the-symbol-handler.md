---
description: 下列程式碼會使用 SymCleanup 來清除與指定進程的符號處理相關聯的所有記憶體。
ms.assetid: 270a1984-9e66-4dd2-accb-d715287f1ec0
title: 結束字元號處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9147ed15c0dc03b76c822a38ccd7ac3c5d326454
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110717"
---
# <a name="terminating-the-symbol-handler"></a>結束字元號處理常式

下列程式碼會使用 [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup)來清除與指定進程的符號處理相關聯的所有記憶體。


```C++
if (SymCleanup(hProcess))
{
    // SymCleanup returned success
}
else
{
    // SymCleanup failed
    DWORD error = GetLastError();
    printf("SymCleanup returned error : %d\n", error);
}
```



 

 



