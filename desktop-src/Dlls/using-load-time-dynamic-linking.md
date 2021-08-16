---
description: 建立 DLL 之後，您可以使用它在應用程式中定義的函式。 以下是簡單的主控台應用程式，它會使用從 Myputs.dll 匯出的 myPuts 函式 (請參閱建立簡單的 Dynamic-Link 程式庫) 。
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: 使用 Load-Time 動態連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 106d9d73808b56c664e44d8dcd71b74a65431316fd3daf47dd0736596c5aa5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902368"
---
# <a name="using-load-time-dynamic-linking"></a>使用 Load-Time 動態連結

建立 DLL 之後，您可以使用它在應用程式中定義的函式。 以下是簡單的主控台應用程式，它會使用從 Myputs.dll 匯出的 myPuts 函式 (請參閱 [建立簡單的 Dynamic-Link 程式庫](creating-a-simple-dynamic-link-library.md)) 。

由於這個範例會明確呼叫 DLL 函式，因此應用程式的模組必須與匯入程式庫 Myputs 連結。 如需建立 Dll 的詳細資訊，請參閱您的開發工具隨附的檔。


```C++
#include <windows.h> 

extern "C" int __cdecl myPuts(LPWSTR);   // a function from a DLL

int main(VOID) 
{ 
    int Ret = 1;

    Ret = myPuts(L"Message sent to the DLL function\n"); 
    return Ret;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[載入時間動態連結](load-time-dynamic-linking.md)
</dt> </dl>

 

 



