---
description: 當呼叫元件的 e 時，建議您在搜尋元件時使用相同的啟用內容。
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: 呼叫元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6f785c9d68aa0dbf4bec24927d9f2a1443aed1fb7fe65ec9244616fce8feec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142421"
---
# <a name="calling-into-assemblies"></a>呼叫元件

當呼叫元件的 e 時，建議您在搜尋元件時使用相同的啟用內容。 至少要確定載入元件的元件不會不慎取得應用程式所使用的啟用內容。 跨 DLL 界限洩漏啟用內容可能會導致非預期的相依性。 如果您的應用程式已啟用隔離感知功能，這就不成問題， \_ \_ 因為在這種情況下，預設不會啟用啟用內容。 如果您未在 \_ 定義啟用隔離感知的情況 \_ 下編譯，則應該啟用 **Null** 啟用內容或用來載入元件的相同啟用內容。

下列範例可確保裝載的 DLL 會在它所辨識的內容中執行：

``` syntax
ULONG_PTR ulpCookie;
ActivateActCtx(hTheActCtxForMyDll, &ulpCookie);
__try 
{
        MyDllIsolatedFunction();
    myDllIsolatedComInterface->Funct();
}
__finally 
{
    DeactivateActCtx(0, ulpCookie);
}
```

 

 



