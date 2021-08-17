---
title: 從群組中移除成員的範例程式碼
description: 下列程式碼範例包含可從群組中移除成員的函式。
ms.assetid: 8a9c65bb-1b61-432b-9ef4-1d257c501026
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，從群組中移除成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d33dd966bb9ef7afb909292c95fd519d154e421b0994527295f41fd60197a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962167"
---
# <a name="example-code-for-removing-a-member-from-a-group"></a>從群組中移除成員的範例程式碼

下列程式碼範例包含可從群組中移除成員的函式。


```C++
////////////////////////////////////////////////////////////////////////////////////////////////////
/*  RemoveMemberFromGroup()   -       Removes the passed directory object from the membership of passed group
 
    Parameters
 
        IADsGroup * pGroup       - Group to remove the member from
        IADs* pIADsNewMember     - Object to remove.
                                   Object can be a user, contact, or group.
*/
HRESULT RemoveMemberFromGroup(IADsGroup * pGroup, IADs* pIADsNewMember)
{
    HRESULT hr = E_INVALIDARG;
    if ((!pGroup)||(!pIADsNewMember))
        return hr;
 
    // Use the IADs::get_ADsPath() member to get the ADsPath
    // When the ADsPath string is returned, all that is required to
    // remove the member from the group, is to call the 
    // IADsGroup::Remove() method, passing in the ADsPath string.
    // Query the member for its AdsPath
    // This is a fully qualified LDAP path to the object to remove.
    BSTR bsNewMemberPath;
    hr = pIADsNewMember->get_ADsPath(&bsNewMemberPath); 
    if (SUCCEEDED(hr))
    {
 
        // Use the IADsGroup interface to remove the member.
        // Pass the LDAP path to the 
        // member to the IADsGroup::Remove() method
        hr = pGroup->Remove(bsNewMemberPath);
 
        // Free the string returned from IADs::get_ADsPath()
        SysFreeString(bsNewMemberPath);
    }
    return hr;
}
```



 

 




