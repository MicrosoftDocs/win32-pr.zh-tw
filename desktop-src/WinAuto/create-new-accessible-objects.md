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
# <a name="create-new-accessible-objects"></a><span data-ttu-id="a2a0e-103">建立新的可存取物件</span><span class="sxs-lookup"><span data-stu-id="a2a0e-103">Create New Accessible Objects</span></span>

<span data-ttu-id="a2a0e-104">在此案例中，伺服器會建立新的可存取物件，以回應每個 [**OBJID \_ 用戶端**](object-identifiers.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="a2a0e-104">In this scenario, the server creates a new accessible object in response to each [**OBJID\_CLIENT**](object-identifiers.md) request.</span></span>

<span data-ttu-id="a2a0e-105">在下列範例程式碼中，會從額外的視窗資料中取出控制項的指標。</span><span class="sxs-lookup"><span data-stu-id="a2a0e-105">In the following example code, a pointer to the control is retrieved from the extra window data.</span></span> <span data-ttu-id="a2a0e-106">這個視窗控制碼會傳遞給自訂協助工具伺服器的函式， (AccServer) 物件。</span><span class="sxs-lookup"><span data-stu-id="a2a0e-106">This and the window handle are passed to the constructor of the custom accessibility server (AccServer) object.</span></span> <span data-ttu-id="a2a0e-107">每當收到 [**OBJID \_ 用戶端**](object-identifiers.md) 時，就會建立此物件。</span><span class="sxs-lookup"><span data-stu-id="a2a0e-107">This object is created whenever [**OBJID\_CLIENT**](object-identifiers.md) is received.</span></span>

<span data-ttu-id="a2a0e-108">當建立物件時，伺服器會取得參考（必須在呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)之後釋放），如此一來，當用戶端完成時，物件就會立即終結。</span><span class="sxs-lookup"><span data-stu-id="a2a0e-108">When the object is created, the server obtains a reference, which must be released after calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), so that the object is destroyed as soon as the client is finished with it.</span></span> <span data-ttu-id="a2a0e-109">請注意， **LresultFromObject** 會將參考計數遞增數次，但它是用戶端應用程式和 Microsoft Active Accessibility 執行時間的責任，以釋放這些參考。</span><span class="sxs-lookup"><span data-stu-id="a2a0e-109">Note that **LresultFromObject** increments the reference count several times, but it is the responsibility of client applications, and the Microsoft Active Accessibility runtime, to release these references.</span></span>


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



 

 




