---
title: 系結至子物件
description: 在 ADSI 中，容器物件會公開 IADsContainer 介面。
ms.assetid: 16b913ea-06a4-4e85-ad6c-68817883bbd8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI，使用，系結至子物件
- 系結至子物件
- 子物件，系結至
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a73d7682dedb405c84dfaf048b8b4b2659e7fd3
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463692"
---
# <a name="binding-to-child-objects"></a>系結至子物件

在 ADSI 中，容器物件會公開 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 介面。 [**IADsContainer：： GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)方法是用來直接系結至子物件。 **IADsContainer：： GetObject** 所傳回的物件與呼叫方法的物件具有相同的安全性內容。 這表示，如果使用替代認證，則不需要再次將替代認證傳遞給系結函式或方法來維護相同的認證。

[**IADsContainer：： GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)方法會取得相對於目前物件 (RDN) 的相對辨別名稱。 這個方法也會接受選擇性的類別名稱，並傳回代表子物件的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面指標。 若要取得所需的 ADSI 介面（例如 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)），請呼叫這個 **IDispatch** 介面指標的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法。

下列 c + + 程式碼範例示範函式，該函式會抓取指定的子物件。


```C++
HRESULT GetChildObject(IADs *pObject, 
                       LPCWSTR pwszClass, 
                       LPCWSTR pwszRDN, 
                       IADs **ppChild)
{
    if(NULL == ppChild)
    {
        return E_INVALIDARG;
    }

    *ppChild = NULL;
    
    if((NULL == pObject) || (NULL == pwszRDN))
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADsContainer *pCont;

    hr = pObject->QueryInterface(IID_IADsContainer, (LPVOID*)&pCont);
    if(SUCCEEDED(hr))
    {
        BSTR bstrClass = NULL;
        if(pwszClass)
        {
            bstrClass = SysAllocString(pwszClass);
        }

        BSTR bstrRDN = SysAllocString(pwszRDN);
        if(bstrRDN)
        {
            IDispatch *pDisp;
            
            hr = pCont->GetObject(bstrClass, bstrRDN, &pDisp);
            if(SUCCEEDED(hr))
            {
                hr = pDisp->QueryInterface(IID_IADs, (LPVOID*)ppChild);
                
                pDisp->Release();
            }

        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        if(bstrRDN)
        {
            SysFreeString(bstrRDN);
        }

        if(bstrClass)
        {
            SysFreeString(bstrClass);
        }


        pCont->Release();
    }
    
    return hr;
}
```



 

 