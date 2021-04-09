---
title: 針對物件設定讀取屬性許可權的範例程式碼
description: 下列程式碼範例包含一個函式，該函式會建立一個 ACE，將物件的所有屬性的讀取存取權指派給指定的信任者。
ms.assetid: 343538d7-fef4-492d-a385-37433ce1250b
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，設定物件的讀取屬性許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6228b3485c47b2ed3d972d2490a70ad264c8ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671291"
---
# <a name="example-code-for-setting-read-property-rights-on-an-object"></a><span data-ttu-id="29393-104">針對物件設定讀取屬性許可權的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="29393-104">Example Code for Setting Read Property Rights on an Object</span></span>

<span data-ttu-id="29393-105">下列程式碼範例包含一個函式，該函式會建立一個 ACE，將物件的所有屬性的讀取存取權指派給指定的信任者。</span><span class="sxs-lookup"><span data-stu-id="29393-105">The following code example contains a function that creates an ACE that assigns read access to all properties of the object to the specified trustee.</span></span>


```C++
/***************************************************************************

    CreateAceEffectiveReadAllProperties()

    Create an ACE that assigns read property rights to all properties on the 
    object. This ACE is not inherited; that is, it applies only to the 
    current object.

***************************************************************************/

HRESULT CreateAceEffectiveReadAllProperties(LPWSTR pwszTrustee, 
                                            IDispatch **ppDispACE)
{
    if(!pwszTrustee || !ppDispACE)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    CComPtr<IADsAccessControlEntry> spACE;
    
    // Create the COM object for the new ACE.
    hr  = CoCreateInstance(CLSID_AccessControlEntry,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IADsAccessControlEntry,
        (void **)&spACE);
    if (SUCCEEDED(hr))
    {
        // Set the properties of the new ACE.

        //Set the access mask containing the rights to assign.
        //This function assigns read property rights.
        hr = spACE->put_AccessMask(ADS_RIGHT_DS_READ_PROP);
        if(FAILED(hr))
        {
            return hr;
        }

        // Set the trustee.
        hr = spACE->put_Trustee(pwszTrustee);
        if(FAILED(hr))
        {
            return hr;
        }
        
        // Set the AceType.
        hr = spACE->put_AceType(ADS_ACETYPE_ACCESS_ALLOWED);
        if(FAILED(hr))
        {
            return hr;
        }
        
        // For this function, set AceFlags so that ACE is not inherited by child objects.
        // You can set AceFlags to 0 or let it default to 0 by not calling put_AceFlags.
        hr = spACE->put_AceFlags(0);
        if(FAILED(hr))
        {
            return hr;
        }
        
        // For this function, set ObjectType to NULL because the right applies to all properties
        // and set Flags to 0. You can also not call these two methods and let them default to NULL. 
        hr = spACE->put_ObjectType(NULL);
        if(FAILED(hr))
        {
            return hr;
        }

        hr = spACE->put_Flags(0);
        if(FAILED(hr))
        {
            return hr;
        }
        
        // Is not inherited; set object type to NULL or let it default to NULL by not calling the method.
        hr = spACE->put_InheritedObjectType(NULL);
        if(FAILED(hr))
        {
            return hr;
        }
        
        // QueryInterface for a IDispatch pointer to pass to the AddAce method.
        hr = spACE->QueryInterface(IID_IDispatch, (void**)ppDispACE);
        if(FAILED(hr))
        {
            return hr;
        }
    }
     
    return hr;
}
```



 

 




