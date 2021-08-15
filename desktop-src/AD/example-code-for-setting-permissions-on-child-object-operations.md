---
title: 設定子物件作業許可權的範例程式碼
description: 下列 C 和 c + + 程式碼範例會建立一個 ACE，以將使用者物件的建立許可權指派給指定的信任者。
ms.assetid: 51010092-fa85-4f9c-8869-97fed30acc7f
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，設定子物件作業的許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53c2862ea645030af2ffb1f69e35c53f765588959dec945a31b8f6d6ce8ef6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118190086"
---
# <a name="example-code-for-setting-permissions-on-child-object-operations"></a>設定子物件作業許可權的範例程式碼

下列 C 和 c + + 程式碼範例會建立一個 ACE，以將使用者物件的建立許可權指派給指定的信任者。


```C++
/***************************************************************************

    CreateAceCreateUsers()

    Create an ACE that assigns the right to create User objects under the 
    current object. For this function, the ACE is inherited by all subobjects 
    and is an effective right on the current object.    

***************************************************************************/

HRESULT CreateAceCreateUsers(LPWSTR pwszTrustee, BOOL fAllowed, IDispatch **ppDispACE)
{
    if(!pwszTrustee || !ppDispACE)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr;
    CComPtr<IADsAccessControlEntry> spACE;

    // Create the COM object for the new ACE.
    hr = spACE.CoCreateInstance(CLSID_AccessControlEntry);
    if(FAILED(hr))
    {
        return hr;
    }

    // Set the properties of the new ACE.

    /*
    Set the access mask that contains the rights to assign. This function 
    assigns rights to create objects.
    */
    hr = spACE->put_AccessMask(ADS_RIGHT_DS_CREATE_CHILD);
    if(FAILED(hr))
    {
        return hr;
    }
    
    // Set the trustee.
    hr = spACE->put_Trustee(CComBSTR(pwszTrustee));
    if(FAILED(hr))
    {
        return hr;
    }
    
    /*
    The AceType property must be ADS_ACETYPE_ACCESS_ALLOWED_OBJECT or 
    ADS_ACETYPE_ACCESS_DENIED_OBJECT.
    */
    if(fAllowed)
    {
        hr = spACE->put_AceType(ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);
    }
    else
    {
        hr = spACE->put_AceType(ADS_ACETYPE_ACCESS_DENIED_OBJECT);
    }
    if(FAILED(hr))
    {
        return hr;
    }

    /*
    Set Flags to ADS_FLAG_OBJECT_TYPE_PRESENT so that the right applies to 
    the creation of a specific object class within the current object and 
    all its subobjects.
    */
    hr = spACE->put_Flags(ADS_FLAG_OBJECT_TYPE_PRESENT);
    if(FAILED(hr))
    {
        return hr;
    }

    // Set ObjectType to the schemaIDGUID of the user class so that the right
    // controls creation of user objects. 
    hr = spACE->put_ObjectType(CComBSTR("BF967ABA-0DE6-11D0-A285-00AA003049E2"));
    if(FAILED(hr))
    {
        return hr;
    }

    // For this function, set AceFlags so that ACE is inherited by child objects 
    hr = spACE->put_AceFlags(ADS_ACEFLAG_INHERIT_ACE);
    if(FAILED(hr))
    {
        return hr;
    }

    // Set InheritedObjectType to NULL so that it is inherited by all subobjects.
    hr = spACE->put_InheritedObjectType(NULL);
    if(FAILED(hr))
    {
        return hr;
    }

    // QueryInterface for the IDispatch pointer to pass to the AddAce method.
    hr = spACE->QueryInterface(IID_IDispatch, (void**)ppDispACE);
    if(FAILED(hr))
    {
        return hr;
    }
     
    return hr;
}
```



 

 




