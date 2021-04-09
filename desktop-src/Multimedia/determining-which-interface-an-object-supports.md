---
title: 判斷物件支援的介面
description: 判斷物件支援的介面
ms.assetid: cf2aacb7-5315-4907-a49b-3eb3bbfd13d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066523503232926f5c031efa2cee5ad7a2b05d24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675395"
---
# <a name="determining-which-interface-an-object-supports"></a><span data-ttu-id="59bde-103">判斷物件支援的介面</span><span class="sxs-lookup"><span data-stu-id="59bde-103">Determining Which Interface an Object Supports</span></span>

<span data-ttu-id="59bde-104">**QueryInterface** 方法可讓應用程式查詢物件，以判斷它支援的介面。</span><span class="sxs-lookup"><span data-stu-id="59bde-104">The **QueryInterface** method lets an application query an object to determine which interfaces it supports.</span></span> <span data-ttu-id="59bde-105">範例應用程式會將 *ppv* 指標設定為目前的介面。</span><span class="sxs-lookup"><span data-stu-id="59bde-105">The sample application sets the *ppv* pointer to the current interface.</span></span>


```C++
STDMETHODIMP CAVIFileCF::QueryInterface( 
    const IID FAR& iid, 
    void FAR* FAR* ppv) 
{ 
    if (iid == IID_IUnknown) 
        *ppv = this;                     // set the interface pointer 
                                         // to this instance 
    else if (iid == IID_IClassFactory) 
        *ppv = this;                     // second chance to set the 
                                         // interface pointer to this 
                                         // instance 
    else 
        return ResultFromScode(E_NOINTERFACE); 
    AddRef();  //Increment the reference count 
    return NULL; 
} 

```



 

 




