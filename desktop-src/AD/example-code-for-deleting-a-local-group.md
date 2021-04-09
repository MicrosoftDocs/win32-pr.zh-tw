---
title: 刪除本機群組的範例程式碼
description: 用來刪除成員伺服器上的本機群組或執行 Windows NT 工作站或 Windows 2000 Professional 之電腦的程式碼範例。
ms.assetid: ff4fd148-2fa2-4355-bfaa-1f093d61aa00
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，刪除本機群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b91588bf59ae7b276aecbaa1740b2510f652f5c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671304"
---
# <a name="example-code-for-deleting-a-local-group"></a><span data-ttu-id="b1cae-104">刪除本機群組的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="b1cae-104">Example Code for Deleting a Local Group</span></span>

<span data-ttu-id="b1cae-105">下列 c + + 程式碼範例會刪除成員伺服器上的本機群組，或是執行 Windows 2000 Professional 或 Windows NT 工作站的電腦。</span><span class="sxs-lookup"><span data-stu-id="b1cae-105">The following C++ code example deletes a local group on a member server or a computer running Windows 2000 Professional or Windows NT Workstation.</span></span>


```C++
/********************************************************************

    DeleteADObject()

********************************************************************/

HRESULT DeleteADObject(LPOLESTR pwszAdsPath, 
                       LPWSTR pwszUsername, 
                       LPWSTR pwszPassword)
{
    HRESULT hr;
    IADs *pIADsToDelete = NULL;
 
    // Bind to the object to be deleted.
 
    // If a username and password are passed, use ADsOpenObject(), 
    // otherwise use ADsGetObject()
    if (!pwszUsername || 0 == *pwszUsername) // No user password --
                                             // use ADsOpenObject.
    {
        hr = ADsGetObject(  pwszAdsPath, 
                            IID_IADs,
                            (void **)& pIADsToDelete);
    }
    else
    {
        hr = ADsOpenObject( pwszAdsPath, 
                            pwszUsername, 
                            pwszPassword, 
                            ADS_SECURE_AUTHENTICATION,
                            IID_IADs, 
                            (void**) & pIADsToDelete);
    }
 
    if (SUCCEEDED(hr))
    {
        BSTR bsParentPath;
        
        // Get the parent path.
        hr = pIADsToDelete->get_Parent(&bsParentPath); 
        if(SUCCEEDED(hr))
        {
            VARIANT vCNToDelete;
     
            VariantInit(&vCNToDelete);

            // Get the CN property for the object to delete.
            hr = pIADsToDelete->Get(CComBSTR("cn"), &vCNToDelete);
            if (SUCCEEDED(hr))
            {
                IDirectoryObject *pIDirObjectParent = NULL;

                // ***********************************************
                // Bind to the parent.
                // If a username and password are passed,
                // use ADsOpenObject()
                // otherwise use ADsGetObject()
                if (!pwszUsername || 0 == *pwszUsername) 
                 // No user password passed - use ADsOpenObject.
                {
                    hr = ADsGetObject(bsParentPath, 
                                      IID_IDirectoryObject,
                                      (void **)&pIDirObjectParent);
                }
                else
                {
                    hr = ADsOpenObject(bsParentPath, 
                                       pwszUsername, 
                                       pwszPassword, 
                                       ADS_SECURE_AUTHENTICATION,
                                       IID_IDirectoryObject, 
                                       (void**)&pIDirObjectParent);
                }
                if (SUCCEEDED(hr))
                {
                    // Release the object to delete.
                    pIADsToDelete->Release();
                    pIADsToDelete = NULL;
     
                    LPWSTR pwszPrefix = L"CN=";
                    LPWSTR pwszRDN = 
                      new WCHAR[lstrlenW(pwszPrefix) + 
                      lstrlenW(vCNToDelete.bstrVal) + 1];
                    if(pwszRDN)
                    {
                        wcscpy_s(pwszRDN, pwszPrefix);
                        wcscat_s(pwszRDN, vCNToDelete.bstrVal);

                        // Instruct the parent to 
                        // delete the child object.
                        hr = pIDirObjectParent->DeleteDSObject(pwszRDN);
                        
                        delete pwszRDN;
                    }
                    else
                    {
                        hr = E_OUTOFMEMORY;
                    }

                    // Release the Parent Object.
                    pIDirObjectParent->Release();
                    pIDirObjectParent = NULL;
                }

                VariantClear(&vCNToDelete);
            }
            
            SysFreeString(bsParentPath);
        }
    }
    
    // If a IADsObject is held, release it.
    if ( pIADsToDelete)
    {
        // Release the object to delete.
        pIADsToDelete->Release();
        pIADsToDelete = NULL;
    }
 
    return hr;
}
```



<span data-ttu-id="b1cae-106">下列 Visual Basic Scripting Edition 程式碼範例會刪除成員伺服器上的本機群組，或是執行 Windows 2000 Professional 或 Windows NT 工作站的電腦。</span><span class="sxs-lookup"><span data-stu-id="b1cae-106">The following Visual Basic Scripting Edition code example deletes a local group on a member server or a computer running Windows 2000 Professional or Windows NT Workstation.</span></span>


```VB
' Example: Deleting a local group on a member server or Windows NT
'          Workstation or Windows 2000 Professional
 
''''''''''''''''''''
' Parse the arguments.
''''''''''''''''''''
On Error Resume Next
 
Set oArgs = WScript.Arguments
If oArgs.Count < 2 Then
    sComputer = InputBox("This script deletes a group from a member server or workstation." & vbCrLf & vbCrLf &"Specify 
 
the computer name:")
    sGroup = InputBox("Specify the group name:")
Else
    sComputer = oArgs.item(0)
    sGroup = oArgs.item(1)
End If
 
If sComputer = "" Then
    WScript.Echo "No computer name was specified. You must specify a computer name."
    WScript.Quit(1)
End If
If sGroup = "" Then
    WScript.Echo "No group name was specified. You must specify a group name."
    WScript.Quit(1)
End If
 
''''''''''''''''''''
' Bind to the computer.
''''''''''''''''''''
Set cont= GetObject("WinNT://" & sComputer & ",computer")
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on GetObject method"
End If
 
''''''''''''''''''''
' Delete the group.
''''''''''''''''''''
' It is not necessary to specify localGroup. 
' To specify the group is acceptable.
Set oGroup = cont.Delete("group", sGroup)
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on IADsContainer::Delete method"
End If
 
strText = "The group " & sGroup & " was deleted on computer " & sComputer & "."
 
Call show_groups(strText, sComputer)
 

''''''''''''''''''''
' Display subroutines.
''''''''''''''''''''
Sub show_groups(strText, strName)
    MsgBox strText, vbInformation, "Create group on " & strName
End Sub
```



 

 




