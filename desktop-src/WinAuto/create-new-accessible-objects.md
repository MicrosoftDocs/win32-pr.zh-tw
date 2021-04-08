---
title: 建立新的可存取物件
description: 建立新的可存取物件
ms.assetid: d34a52d1-1eb2-4bb4-989c-a1ca4b5d815f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efa85e44d6d51105e6363d276ecb7e5f33d8378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673595"
---
# <a name="create-new-accessible-objects"></a>建立新的可存取物件

在此案例中，伺服器會建立新的可存取物件，以回應每個 [**OBJID \_ 用戶端**](object-identifiers.md) 要求。

在下列範例程式碼中，會從額外的視窗資料中取出控制項的指標。 這個視窗控制碼會傳遞給自訂協助工具伺服器的函式， (AccServer) 物件。 每當收到 [**OBJID \_ 用戶端**](object-identifiers.md) 時，就會建立此物件。

當建立物件時，伺服器會取得參考（必須在呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)之後釋放），如此一來，當用戶端完成時，物件就會立即終結。 請注意， **LresultFromObject** 會將參考計數遞增數次，但它是用戶端應用程式和 Microsoft Active Accessibility 執行時間的責任，以釋放這些參考。


```C++
case WM_GETOBJECT:
{
    // Return the IAccessible object. 
    if ((DWORD)lParam == OBJID_CLIENT)
    {
        // Get the control.  
        CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
        AccServer* pAccServer = new AccServer(hwnd, pCustomList);
        if (pAccServer != NULL)  // NULL if out of memory. 
        {
            LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
            pAccServer->Release();
            return Lresult;
        }
        else return 0;
    }
    break;
}
```



 

 




