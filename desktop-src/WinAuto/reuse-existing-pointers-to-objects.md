---
title: 重複使用物件的現有指標
description: 重複使用物件的現有指標
ms.assetid: 7e1610c6-89b2-4e7e-aee5-94a6cab87a22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c151b8d957fb82718721ad81b452a81a2c71ec84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966381"
---
# <a name="reuse-existing-pointers-to-objects"></a><span data-ttu-id="88345-103">重複使用物件的現有指標</span><span class="sxs-lookup"><span data-stu-id="88345-103">Reuse Existing Pointers to Objects</span></span>

<span data-ttu-id="88345-104">在此案例中，伺服器會每次都使用相同的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標來回應 [**OBJID \_ 用戶端**](object-identifiers.md)要求。</span><span class="sxs-lookup"><span data-stu-id="88345-104">In this scenario, the server responds to an [**OBJID\_CLIENT**](object-identifiers.md) request using the same [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer each time.</span></span>

<span data-ttu-id="88345-105">在下列範例程式碼中，控制項會從額外的視窗資料抓取控制項物件，並呼叫控制項的方法，以取得應用程式定義的 AccServer 類別 (的次要伺服器物件) （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="88345-105">In the following example code, the control object is retrieved from the extra window data, and a method of the control is called to retrieve the accessibility server object (the application-defined AccServer class), if any.</span></span> <span data-ttu-id="88345-106">如果協助工具伺服器尚未存在，則會加以建立。</span><span class="sxs-lookup"><span data-stu-id="88345-106">If the accessibility server does not yet exist, it is created.</span></span>

<span data-ttu-id="88345-107">當協助工具伺服器物件建立時，參考計數為1。</span><span class="sxs-lookup"><span data-stu-id="88345-107">When the accessibility server object is created, it has a reference count of 1.</span></span> <span data-ttu-id="88345-108">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 會將參考計數遞增數次，但是當用戶端完成物件時，將會釋放這些參考。</span><span class="sxs-lookup"><span data-stu-id="88345-108">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) increments the reference count several times, but these references will be released when the client is finished with the object.</span></span> <span data-ttu-id="88345-109">當控制項視窗損毀時，伺服器會釋放其參考。</span><span class="sxs-lookup"><span data-stu-id="88345-109">The server releases its reference when the control window is destroyed.</span></span>


```C++
case WM_GETOBJECT:
    {
        // Return the IAccessible object. 
        if ((DWORD)lParam == (DWORD)OBJID_CLIENT)
        {
            // Get the control.  
            CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
            // Create the accessible object. 
            AccServer* pAccServer = pCustomList->GetAccServer();
            if (pAccServer == NULL)
            {
                pAccServer = new AccServer(hwnd, pCustomList);
                pCustomList->SetAccServer(pAccServer);
            }
            if (pAccServer != NULL)  // NULL if out of memory. 
            {
                LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
                return Lresult;
            }
            else return 0;
        }
        break;
    }

    
case WM_DESTROY:
    {
    CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
    AccServer* pAccServer = pCustomList->GetAccServer();
    if (pAccServer!= NULL)
    {
        // Notify the accessibility object that the control no longer exists. 
        pAccServer->SetControlIsAlive(false);
        // Release the reference created in WM_GETOBJECT. 
        pAccServer->Release(); 
    }   
    // Destroy the control. 
    delete pCustomList;
     break;
    }
```



 

 




