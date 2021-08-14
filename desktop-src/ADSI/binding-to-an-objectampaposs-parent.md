---
title: 系結至物件的父系
description: 在 ADSI 中，每個目錄物件都是由公開 IADs 介面的 ADSI COM 物件表示。
ms.assetid: 3740e862-4cfe-484c-8c8e-3923c64cdd47
ms.tgt_platform: multiple
keywords:
- ADSI ADSI （使用）系結至物件的父系
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b47bfd71491c3eb0e8410f421630cec20255364b1cfc41bba7d6b48ba67fdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180393"
---
# <a name="binding-to-an-objects-parent"></a>系結至物件的父系

在 ADSI 中，每個目錄物件都是由公開 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面的 ADSI COM 物件表示。 若要取得物件的父容器，請使用 [**IADs：： get \_ 父**](iads-property-methods.md) 方法取得父物件的 adspath，然後系結至父系的 adspath。

下列 c + + 程式碼範例顯示如何取得物件的父系。


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



 

 




