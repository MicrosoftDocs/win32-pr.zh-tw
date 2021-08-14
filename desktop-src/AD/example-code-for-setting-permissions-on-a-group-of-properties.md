---
title: 設定屬性群組許可權的範例程式碼
description: 下列 C 和 c + + 程式碼範例會建立一個 ACE，以將使用者物件之個人資訊屬性集的讀取和寫入存取權指派給指定的信任者。
ms.assetid: 46d53b41-02eb-4830-b625-2d9ffa21a312
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，設定屬性群組的許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220a9f306a4691aed53ec5c769405ae5db9f9c53fcb192cc383fbf9e8235def4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118190096"
---
# <a name="example-code-for-setting-permissions-on-a-group-of-properties"></a>設定屬性群組許可權的範例程式碼

下列 C 和 c + + 程式碼範例會建立一個 ACE，以將使用者物件之 [**個人資訊**](/windows/desktop/ADSchema/r-personal-information) 屬性集的讀取和寫入存取權指派給指定的信任者。


```C++
/***************************************************************************

    CreateAceChangePersonalInfoPropGroupOfUsers()

    Create an ACE that assigns change (Read/Write) property rights to the 
    attributes of the Personal Information property set for user objects. 
    For this function, the ACE is only inherited; therefore, it is not an 
    effective right on the current object.

***************************************************************************/

HRESULT CreateAceChangePersonalInfoPropGroupOfUsers(LPWSTR pwszTrustee, 
                                                    BOOL fAllowed, 
                                                    IDispatch **ppDispACE)
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
    Set the access mask containing the rights to assign. This function assigns 
    ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP to control change.
    */
    hr = spACE->put_AccessMask(ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP);
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

    // AceType must be ADS_ACETYPE_ACCESS_ALLOWED_OBJECT or ADS_ACETYPE_ACCESS_DENIED_OBJECT.
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
    Set Flags to ADS_FLAG_OBJECT_TYPE_PRESENT | ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT 
    so that the right applies only to a specific property of the specified 
    object class.
    */
    hr = spACE->put_Flags(ADS_FLAG_OBJECT_TYPE_PRESENT | ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT);
    if(FAILED(hr))
    {
        return hr;
    }

    // Set ObjectType to the rightsGUID of the Personal Information controlAccessRight object. 
    hr = spACE->put_ObjectType(CComBSTR("{77B5B886-944A-11d1-AEBD-0000F80367C1}"));
    if(FAILED(hr))
    {
        return hr;
    }

    /*
    For this function, set AceFlags so that ACE is inherited by child objects, 
    but not effective on the current object. Set AceFlags to ADS_ACEFLAG_INHERIT_ACE 
    and ADS_ACEFLAG_INHERIT_ONLY_ACE.
    */
    hr = spACE->put_AceFlags(ADS_ACEFLAG_INHERIT_ACE | ADS_ACEFLAG_INHERIT_ONLY_ACE);
    if(FAILED(hr))
    {
        return hr;
    }

    // Set InheritedObjectType to schemaIDGUID of the user class.
    hr = spACE->put_InheritedObjectType(CComBSTR("{BF967ABA-0DE6-11D0-A285-00AA003049E2}"));
    if(FAILED(hr))
    {
        return hr;
    }

    // Call the QueryInterface method for the IDispatch pointer to pass to the AddAce method.
    hr = spACE->QueryInterface(IID_IDispatch, (void**)ppDispACE);
    if(FAILED(hr))
    {
        return hr;
    }

    return hr;
}
```



 

 