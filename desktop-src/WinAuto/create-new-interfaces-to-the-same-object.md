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
# <a name="create-new-interfaces-to-the-same-object"></a><span data-ttu-id="38a25-103">建立相同物件的新介面</span><span class="sxs-lookup"><span data-stu-id="38a25-103">Create New Interfaces to the Same Object</span></span>

<span data-ttu-id="38a25-104">在此案例中，伺服器會透過取得相同物件的新介面指標，回應每個 [**OBJID \_ 用戶端**](object-identifiers.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="38a25-104">In this scenario, the server responds to each [**OBJID\_CLIENT**](object-identifiers.md) request by obtaining a new interface pointer to the same object.</span></span>

<span data-ttu-id="38a25-105">在下列範例程式碼中， *m \_ pUIObj* 是物件的指標，此物件支援一個以上的元件物件模型 (COM) 介面。</span><span class="sxs-lookup"><span data-stu-id="38a25-105">In the following example code, *m\_pUIObj* is a pointer to an object that supports more than one Component Object Model (COM) interface.</span></span> <span data-ttu-id="38a25-106">即使已重複使用現有的物件，每次抓取物件時都會建立新的介面指標，因此必須遞減參考計數。</span><span class="sxs-lookup"><span data-stu-id="38a25-106">Even though an existing object is reused, a new interface pointer is created each time the object is retrieved, so the reference count must be decremented.</span></span>


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



 

 




