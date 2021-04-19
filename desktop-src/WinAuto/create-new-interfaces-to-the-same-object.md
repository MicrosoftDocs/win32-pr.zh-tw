---
title: 建立相同物件的新介面
description: 建立相同物件的新介面
ms.assetid: 127c44b6-51a6-4fd6-9edc-9fbe0d08d458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b641eed3918af3acbf399427ad5f7427112f399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968842"
---
# <a name="create-new-interfaces-to-the-same-object"></a>建立相同物件的新介面

在此案例中，伺服器會透過取得相同物件的新介面指標，回應每個 [**OBJID \_ 用戶端**](object-identifiers.md) 要求。

在下列範例程式碼中， *m \_ pUIObj* 是物件的指標，此物件支援一個以上的元件物件模型 (COM) 介面。 即使已重複使用現有的物件，每次抓取物件時都會建立新的介面指標，因此必須遞減參考計數。


```C++
case WM_GETOBJECT:
   if ((DWORD)lParam == OBJID_CLIENT)
   {
      // Get a new interface to the same object. 
      IAccessible *pAcc = NULL;
      // The following increments the reference count. 
      m_pUIObj->QueryInterface(IID_IAccessible, (LPVOID*)&pAcc); 
      LRESULT lAcc = LresultFromObject(IID_IAccessible, wParam, 
            (LPUNKNOWN) &pAcc); 
      // Release our reference to the object.             
      pAcc->Release();               
      return lAcc;
   }
   break;  // Fall through to DefWindowProc. 
   
```



 

 




