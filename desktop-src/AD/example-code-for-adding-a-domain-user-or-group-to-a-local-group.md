---
title: 將網域使用者或群組新增至本機群組的範例程式碼
description: 本主題包含的程式碼範例會示範如何將網域使用者或群組新增到成員伺服器上的本機群組，或是在 Windows NT 工作站或 Windows 2000 Professional 上執行的電腦。
ms.assetid: 6333ce9f-0396-4af7-9e81-f008cf4536ec
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，將網域使用者或群組新增至本機群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdca65c26c6ab1195dcd0d7fc3f44b36e39bed1d15e97627664754c918e57e96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694686"
---
# <a name="example-code-for-adding-a-domain-user-or-group-to-a-local-group"></a>將網域使用者或群組新增至本機群組的範例程式碼

下列 c + + 程式碼範例會將網域使用者或群組新增到成員伺服器上的本機群組或 Windows NT 工作站或 Windows 2000 Professional 上執行的電腦。


```C++
#include <stdio.h>
#include <atlbase.h>
#include <activeds.h>
#include <ntldap.h>

/*******************************************************************

    AddDomainUserToLocalGroup()

    Adds a user from a domain to a local group using the WinNT 
    provider.

    Parameters:

    pwszComputerName - Contains the name of the computer 
    that the group belongs to.

    pwszGroupName - Contains the name of the group to add a member 
    to. This group must exist on the target computer.

    pwszDomainName - Contains the name of domain that contains 
    the user to add to the group.

    pwszUserToAdd - Contains the name of the user in the domain 
    to add to the group.

*******************************************************************/

HRESULT AddDomainUserToLocalGroup(LPCWSTR pwszComputerName, 
                                  LPCWSTR pwszGroupName, 
                                  LPCWSTR pwszDomainName, 
                                  LPCWSTR pwszUserToAdd)
{
    HRESULT hr = E_FAIL;
    CComPtr<IADsContainer> spComputer;

    // Build the binding string.
    CComBSTR sbstrBindingString;
    sbstrBindingString = "WinNT://";
    sbstrBindingString += pwszComputerName;
    sbstrBindingString += ",computer";
    
    // Bind to the computer that contains the group.
    hr = ADsOpenObject( sbstrBindingString,
                        NULL, 
                        NULL, 
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADsContainer, 
                        (void**)&spComputer);

    if(FAILED(hr))
    {
        return hr;
    }

    // Bind to the group object.
    CComPtr<IDispatch> spDisp;
    hr = spComputer->GetObject(CComBSTR("group"), 
                               CComBSTR(pwszGroupName), 
                               &spDisp);
    if(FAILED(hr))
    {
        return hr;
    }

    CComPtr<IADsGroup> spGroup;
    hr = spDisp->QueryInterface(IID_IADs, (LPVOID*)&spGroup);
    if(FAILED(hr))
    {
        return hr;
    }
    
    // Bind to the member to add.
    sbstrBindingString = "WinNT://";
    sbstrBindingString += pwszDomainName;
    sbstrBindingString += "/";
    sbstrBindingString += pwszUserToAdd;

    hr = spGroup->Add(sbstrBindingString);

    return hr;
}
```



下列 Visual Basic 程式碼範例會將網域使用者或群組新增到成員伺服器上的本機群組，或是 Windows NT 工作站或 Windows 2000 Professional 上執行的電腦。


```VB
''''''''''''''''''''''''''''''''''''''''
'
'   AddDomainUserToLocalGroup
'
'   Adds a user from a domain to a local group using the WinNT 
'   provider.
'
'   Parameters:
'
'   ComputerName - Contains the name of the computer that the group
'   belongs to.
'
'   GroupName - Contains the name of the group to add a member to. 
'   This group must exist on the target computer.
'
'   DomainName - Contains the name of domain that contains the user
'   to add to the group.
'
'   UserName - Contains the name of the user in the domain to add
'   to the group.
'
''''''''''''''''''''''''''''''''''''''''
Public Sub AddDomainUserToLocalGroup(ComputerName As String, _
                                    GroupName As String, _
                                    DomainName As String, _
                                    UserName As String)
    Dim GroupComputer As IADsContainer
    Dim Group As IADsGroup
    
    ' Bind to the computer that contains the group.
    Set GroupComputer = GetObject("WinNT://" & 
                                  ComputerName & 
                                  ",computer")
    
    ' Bind to the group object.
    Set Group = GroupComputer.GetObject("group", GroupName)
    
    ' Add the user to the group.
    Group.Add ("WinNT://" & DomainName & "/" & UserName)
End Sub
```



 

 




