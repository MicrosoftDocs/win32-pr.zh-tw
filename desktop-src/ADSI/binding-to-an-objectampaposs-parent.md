---
title: 系結至物件的父系
description: 在 ADSI 中，每個目錄物件都是由公開 IADs 介面的 ADSI COM 物件表示。
ms.assetid: 3740e862-4cfe-484c-8c8e-3923c64cdd47
ms.tgt_platform: multiple
keywords:
- ADSI ADSI （使用）系結至物件的父系
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d72f3b3db3af9f13892494d3855dc5dcb2a74d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839232"
---
# <a name="binding-to-an-objects-parent"></a><span data-ttu-id="70435-104">系結至物件的父系</span><span class="sxs-lookup"><span data-stu-id="70435-104">Binding to an Object's Parent</span></span>

<span data-ttu-id="70435-105">在 ADSI 中，每個目錄物件都是由公開 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面的 ADSI COM 物件表示。</span><span class="sxs-lookup"><span data-stu-id="70435-105">In ADSI, every directory object is represented by an ADSI COM object that exposes the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="70435-106">若要取得物件的父容器，請使用 [**IADs：： get \_ 父**](iads-property-methods.md) 方法取得父物件的 adspath，然後系結至父系的 adspath。</span><span class="sxs-lookup"><span data-stu-id="70435-106">To obtain the parent container of an object, use the [**IADs::get\_Parent**](iads-property-methods.md) method to obtain the ADsPath of the parent object, then bind to the ADsPath of the parent.</span></span>

<span data-ttu-id="70435-107">下列 c + + 程式碼範例顯示如何取得物件的父系。</span><span class="sxs-lookup"><span data-stu-id="70435-107">The following C++ code example shows how to obtain the parent of an object .</span></span>


```C++
HRESULT GetParentObject(IADs *pObject,   // Pointer to the object whose parent to bind to.
                        IADs **ppParent) // Return a pointer to the parent object.
{
    if(NULL == ppParent)
    {
        return E_INVALIDARG;
    }
 
    *ppParent = NULL;

    if(NULL == pObject)
    {
        return E_INVALIDARG;
    }
 
    HRESULT hr;
    BSTR bstr;

    // Get the ADsPath of the parent.
    hr = pObject->get_Parent(&bstr);
    if(SUCCEEDED(hr))
    {
        // Bind to the parent.
        hr = ADsOpenObject(bstr,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)ppParent);

        SysFreeString(bstr);
    }

    return hr;
}
```



 

 




