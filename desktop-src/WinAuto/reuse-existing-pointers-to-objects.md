---
title: 重複使用物件的現有指標
description: 重複使用物件的現有指標
ms.assetid: 7e1610c6-89b2-4e7e-aee5-94a6cab87a22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14571234ee937d2237d3102316665f15a9ab55415042ddaeda749bfaa21e4807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998118"
---
# <a name="reuse-existing-pointers-to-objects"></a>重複使用物件的現有指標

在此案例中，伺服器會每次都使用相同的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標來回應 [**OBJID \_ 用戶端**](object-identifiers.md)要求。

在下列範例程式碼中，控制項會從額外的視窗資料抓取控制項物件，並呼叫控制項的方法，以取得應用程式定義的 AccServer 類別 (的次要伺服器物件) （如果有的話）。 如果協助工具伺服器尚未存在，則會加以建立。

當協助工具伺服器物件建立時，參考計數為1。 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 會將參考計數遞增數次，但是當用戶端完成物件時，將會釋放這些參考。 當控制項視窗損毀時，伺服器會釋放其參考。


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



 

 




