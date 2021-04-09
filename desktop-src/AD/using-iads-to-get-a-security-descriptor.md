---
title: 使用 IADs 取得安全描述項
description: 下列程式碼範例使用 IADs Get 方法，在 Active Directory Domain Services 中取出物件之 nTSecurityDescriptor 屬性的 IADsSecurityDescriptor 指標。
ms.assetid: ce8948ac-0644-42a0-8b77-5a06d3fcf042
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，使用 IADs 取得安全描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef6fa2a4137f39bc31251f3b327b9dfc29a91318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681629"
---
# <a name="using-iads-to-get-a-security-descriptor"></a><span data-ttu-id="1437f-104">使用 IADs 取得安全描述項</span><span class="sxs-lookup"><span data-stu-id="1437f-104">Using IADs to Get a Security Descriptor</span></span>

<span data-ttu-id="1437f-105">下列程式碼範例使用 [**IADs：： Get**](/windows/desktop/api/iads/nf-iads-iads-get)方法，在 Active Directory Domain Services 中取得物件之 **NTSecurityDescriptor** 屬性的 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor)指標。</span><span class="sxs-lookup"><span data-stu-id="1437f-105">The following code examples use the [**IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve an [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) pointer to the **nTSecurityDescriptor** property of an object in Active Directory Domain Services.</span></span>


```VB
Dim rootDSE As IADs
Dim ADUser As IADs
Dim sd As IADsSecurityDescriptor

On Error GoTo Cleanup
 
' Bind to the Users container in the local domain.
Set rootDSE = GetObject("LDAP://rootDSE")
Set ADUser = GetObject("LDAP://cn=users," & rootDSE.Get("defaultNamingContext"))
 
' Get the security descriptor on the Users container.
Set sd = ADUser.Get("ntSecurityDescriptor")
Debug.Print sd.Control
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision

Exit Sub

Cleanup:
    Set rootDSE = Nothing
    Set ADUser = Nothing
    Set sd = Nothing
```




```C++
HRESULT GetSDFromIADs(
                IADs *pObject,
                IADsSecurityDescriptor **ppSD )
{
    VARIANT var;
    HRESULT hr;

    if(!pObject || !ppSD)
    {
        return E_INVALIDARG;
    }
 
    // Set *ppSD to NULL.
    *ppSD = NULL;
    
    VariantInit(&var);
 
    // Get the nTSecurityDescriptor.
    hr = pObject->Get(CComBSTR("nTSecurityDescriptor"), &var);
    if (SUCCEEDED(hr))
    {
        // Type should be VT_DISPATCH - an IDispatch pointer to the security descriptor object.
        if (var.vt == VT_DISPATCH)
        { 
            // Use V_DISPATCH macro to get the IDispatch pointer from the 
            // VARIANT structure and QueryInterface for the IADsSecurityDescriptor pointer.
            hr = V_DISPATCH(&var)->QueryInterface(IID_IADsSecurityDescriptor, (void**)ppSD);
        }
        else
        {
            hr = E_FAIL;
        }
    }

    VariantClear(&var);
    return hr;
}
```



 

 