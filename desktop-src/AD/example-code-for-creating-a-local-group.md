---
title: 建立本機群組的範例程式碼
description: 建立本機群組的範例程式碼
ms.assetid: e204ea67-52c0-430a-bb22-a53f4c084e4f
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，建立本機群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99ecb6de577c185b1e73244a609ad9e58af9d0fa2979b8ffd1e41f282c933100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962417"
---
# <a name="example-code-for-creating-a-local-group"></a>建立本機群組的範例程式碼

下列 c + + 程式碼範例會在成員伺服器上建立本機群組，或在 Windows NT 工作站或 Windows 2000 Professional 上執行的電腦上建立本機群組。


```C++
/********************************************************************

    CreateMachineLocalGroup()

    Creates a local group on the specified computer and adds the 
    specified objects to the group.

    Parameters:

    pwszComputer - A null-terminated string that contains the name  
    of the computer on which to create the local group.

    pwszGroupName - A null-terminated string that contains the name  
    of the group to create.

    rgpwszObjectsToAdd - Contains an array of null-terminated strings 
    that specify the objects to add to the new group. The objects in  
    this array must belong to the computer specified in pwszComputer.  
    dwObjectsToAdd contains the number of elements in this array. 
    This parameter is ignored if dwObjectsToAdd contains zero.

    dwObjectsToAdd - Contains the number of elements in the 
    rgpwszObjectsToAdd array. Pass zero for this parameter to not
    add any objects to the group.

********************************************************************/

HRESULT CreateMachineLocalGroup(
    LPCWSTR pwszComputer, 
    LPCWSTR pwszGroupName, 
    LPCWSTR *rgpwszObjectsToAdd, 
    DWORD dwObjectsToAdd)
{
    if(!pwszComputer || !pwszGroupName || !rgpwszObjectsToAdd)
    {
        return E_POINTER;
    }
    
    HRESULT hr;

    // Because the WinNT provider is used, bind to the
    // specific computer name.
    CComBSTR sbstrADsPath = L"WinNT://";
    sbstrADsPath += pwszComputer;
    sbstrADsPath += ",computer";
    
    // Bind to the container.
    CComPtr<IADsContainer> spContainer;
    hr = ADsGetObject(sbstrADsPath, 
                      IID_IADsContainer,
                     (void**) &spContainer);
    if(FAILED(hr))
    {
        return hr;
    }

    /*
    Create the group. This only creates the group in memory.
    The group is not actually created until IADs.SetInfo is called.
    */
    CComPtr<IDispatch> spDisp;
    hr = spContainer->Create(CComBSTR("group"), 
                             CComBSTR(pwszGroupName), 
                             &spDisp);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the IADsGroup interface.
    CComPtr<IADsGroup> spGroup;
    hr = spDisp->QueryInterface(IID_IADsGroup, (void**)&spGroup);
    if(FAILED(hr))
    {
        return hr;
    }

    // Commit the group to the directory.
    hr = spGroup->SetInfo();
    if(HRESULT_FROM_WIN32(ERROR_ALIAS_EXISTS) == hr)
    {
        /*
        This occurs if the group exists. Should the function add
       the members to the exiting group or fail?
        */
    }
    else if(FAILED(hr))
    {
        return hr;
    }

    // Add the specified objects to the group.
    for(DWORD i = 0; i < dwObjectsToAdd; i++)
    {
        CComBSTR sbstrObj = "WinNT://";
        sbstrObj += pwszComputer;
        sbstrObj += "/";
        sbstrObj += rgpwszObjectsToAdd[i];
        
        hr = spGroup->Add(sbstrObj);
        if(HRESULT_FROM_WIN32(ERROR_MEMBER_IN_ALIAS) == hr)
        {
            /*
            This will occur if the member already 
            exists in the group.
            */
        }
        else if(FAILED(hr))
        {
            /*
            The object cannot be added, but this is 
            not a catastrophic error. Retry to add
            additional objects.
            */
            hr = S_OK;
            continue;
        }
    }

    return hr;
}
```



下列 Visual Basic 程式碼範例會在成員伺服器上，或在 Windows NT 工作站或 Windows 2000 Professional 上執行的電腦上建立本機群組。


```VB
Public Sub CreateMachineLocalGroup(Computer As String, _
    GroupName As String, _
    ObjectToAdd As String)
    
    Dim oComputer As IADsContainer
    
    ' Bind to the computer.
    Set oComputer = GetObject("WinNT://" & Computer & ",computer")
    
    ' Create the group. This only creates the group in memory.
    ' The group is not actually created until IADs.SetInfo is called.
    Dim oGroup As IADsGroup
    Set oGroup = oComputer.Create("group", GroupName)
    
    ' Ignore errors for the next operation.
    On Error Resume Next
    ' Commit the group to the directory.
    oGroup.SetInfo
    
    ' Stop ignoring errors.
    On Error GoTo 0
    
    ' Add the objects to the group.
    oGroup.Add "WinNT://" & Computer & "/" & ObjectToAdd
End Sub
```



 

 




