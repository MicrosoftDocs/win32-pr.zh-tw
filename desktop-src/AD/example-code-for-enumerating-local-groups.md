---
title: 列舉本機群組的範例程式碼
description: 本主題包含的程式碼範例會列舉指定類別的所有物件。
ms.assetid: d113d132-24cf-4319-826b-0d3d10e432f6
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，列舉本機群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b830c1c3ec60d393606e282ff4408647ec8d62
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681665"
---
# <a name="example-code-for-enumerating-local-groups"></a><span data-ttu-id="0cff5-104">列舉本機群組的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="0cff5-104">Example Code for Enumerating Local Groups</span></span>

<span data-ttu-id="0cff5-105">本主題包含的程式碼範例會列舉指定類別的所有物件。</span><span class="sxs-lookup"><span data-stu-id="0cff5-105">This topic includes a code example that enumerates all objects of a specified class.</span></span>

<span data-ttu-id="0cff5-106">下列 c + + 程式碼範例會使用 ADSI 來列舉指定類別的所有物件。</span><span class="sxs-lookup"><span data-stu-id="0cff5-106">The following C++ code example enumerates all objects of a specified class using ADSI.</span></span>


```C++
////////////////////////////////////////////////////////////////////////////////////////////////////
/*  ListMembersWithWinNtProvider()    - Uses the WinNT provider to list children based on a filter
                                        Returns S_OK on success   
 
    Parameters
 
    LPWSTR pwszComputer     - Computer to list
    LPWSTR pwszClass        - Filter for listing
    LPWSTR pwszUSER = NULL  - User Name for ADsOpenObject() binding- If not passed - Bind Though ADsGetObject()
    LPWSTR pwszPASS = NULL  - Password for ADsOpenObject() binding- If not passed - Bind Though ADsGetObject()
 
*/
HRESULT ListMembersWithWinNtProvider(LPWSTR pwszComputer,LPWSTR pwszClass, LPWSTR pwszUSER = NULL, LPWSTR pwszPASS = NULL)
{
    HRESULT hr;
    LPWSTR  pwszBindingString = NULL;
 
    IADsContainer * pIADsCont = NULL;
 
    // Allocate a String for Binding. This should be large enough.
    pwszBindingString = new WCHAR[(wcslen(gbsComputer) *2) + 20];
    
    swprintf_s(pwszBindingString,L"WinNT://%s,computer",pwszComputer);
 
    // Ensure either no user is passed - or both user and password are passed.
    assert(!pwszUSER || (pwszUSER && pwszPASS));
 
    // Bind to the container passed.
    // If USER and PASS passed in, use ADsOpenObject()
    if (pwszUSER)
        hr = ADsOpenObject( pwszBindingString,
                            pwszUSER, 
                            pwszPASS, 
                            ADS_SECURE_AUTHENTICATION,
                            IID_IADsContainer, 
                            (void**) &pIADsCont);
    else
        hr = ADsGetObject( pwszBindingString, IID_IADsContainer,(void **)&pIADsCont);
 
    if (SUCCEEDED(hr))
    {
        VARIANT vFilter;
        VariantInit(&vFilter);
        LPWSTR pwszFilter = pwszClass;
 
        // Build a Variant of array type, using the filter passed.
        hr = ADsBuildVarArrayStr(&pwszFilter, 1, &vFilter);
 
        if (SUCCEEDED(hr))
        {
            // Set the filter for the results of the Enum.
            hr = pIADsCont->put_Filter(vFilter);
 
            if (SUCCEEDED(hr))
            {
                IEnumVARIANT * pEnumVariant = NULL; // Pointer to the IEnumVariant Interface
                VARIANT Variant;                    // Variant for retrieving data
                ULONG   ulElementsFetched;          // Number of elements fetched
 
                // Builds an enumerator interface - this will be used
                // to enumerate the objects contained in the IADsContainer. 
                hr = ADsBuildEnumerator(pIADsCont,&pEnumVariant);
                // While no errors, loop through and print the data.
                while (SUCCEEDED(hr) && hr != S_FALSE) 
                {
 
                    // Object comes back as a VARIANT holding an IDispatch *
                    hr = ADsEnumerateNext(pEnumVariant,1,&Variant,&ulElementsFetched);
 
                    if (hr != S_FALSE) 
                    { 
                        assert(HAS_BIT_STYLE(Variant.vt,VT_DISPATCH));
 
                        IDispatch *pDispatch = NULL;
                        IADs *pIADs= NULL;
                        pDispatch = Variant.pdispVal;
 
                        // Call the QueryInterface method for the Variant IDispatch * for the IADs interface.
                        hr = pDispatch->QueryInterface(IID_IADs,(VOID **) &pIADs) ;
 
                        if (SUCCEEDED(hr))
                        {
                            // Print data about the object.
                            BSTR bsResult;
 
                            pIADs->get_Name(&bsResult); 
                            wprintf(L" NAME: %s\n",(LPOLESTR) bsResult);
                            SysFreeString(bsResult);
 
 
                            pIADs->get_ADsPath(&bsResult); 
                            wprintf(L" ADSPATH: %s\n",(LPOLESTR) bsResult);
                            SysFreeString(bsResult);
 
                            puts("------------------------------------------------------");
                            pIADs->Release();
                            pIADs = NULL;
                        }
                    }
                }
 
                // Because the hr from iteration was lost, free 
                // the interface if the pointer is != NULL
                if (pEnumVariant)
                {
                    pEnumVariant->Release();
                    pEnumVariant = NULL;
                }
                VariantClear(&Variant);
            }
        }
        VariantClear(&vFilter);
    }
 
    delete [] pwszBindingString;
    pwszBindingString = NULL;
 
    return hr;
}
```



<span data-ttu-id="0cff5-107">下列 Visual Basic 程式碼範例會使用 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 和 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) 介面來列舉本機群組。</span><span class="sxs-lookup"><span data-stu-id="0cff5-107">The following Visual Basic code example enumerates local groups using the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) and [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interfaces.</span></span>


```VB
' Example: Enumerating all local groups on member server or Windows NT Workstation or Windows 2000 Professional
Dim IADsCont As IADsContainer
Dim Group As IADsGroup
 
On Error GoTo CleanUp
 
sComputer = InputBox("This script lists the groups on a member server or workstation." & vbCrLf & vbCrLf & "Specify the computer name:")
 
If sComputer = "" Then
  MsgBox "No computer name was specified. Specify a computer name."
  Exit Sub
End If
 
''''''''''''''''''''
' Bind to the computer
''''''''''''''''''''
' Be aware that this sample uses the caller's security context.
' To specify a user account other than the user account under which
' which your application is running, use IADsOpenDSObject.
Set IADsCont = GetObject("WinNT://" & sComputer & ",computer")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
''''''''''''''''''''
' Filter to view only group objects
''''''''''''''''''''
IADsCont.Filter = Array("group")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADsContainer::Filter method"
End If
 
strText = ""
intIndex = 0
intNumDisplay = 0
cmember = 0
'Maximum number of groups to list on a msgbox.
MAX_DISPLAY = 10
 
''''''''''''''''''''
' Get each group and display its name and its members
''''''''''''''''''''
For Each Group In IADsCont
    intIndex = intIndex + 1
    ' Get the name.
    strText = strText & vbCrLf & Right("  " & intIndex, 4) & " " & Group.Name
 
    intNumDisplay = intNumDisplay + 1
    ' Get the members object.
    Set memberList = Group.Members
    If (Err.Number <> 0) Then
       BailOnFailure Err.Number, "on IADsGroup::members method"
    End If
 
    ' Get the enumerate the members of the group from the members object
    For Each member In memberList
      If cmember = 0 Then
    strText = strText & vbCrLf & "       " & "Members:"
      End If
      strText = strText & vbCrLf & "       " & member.Name & " (" & member.Class & ")"
      cmember = cmember + 1
    Next
    If cmember = 0 Then
      strText = strText & vbCrLf & "       " & "No members"
    End If
    ' Display in msgbox if there are MAX_DISPLAY groups to display
    If intNumDisplay >= MAX_DISPLAY Then
        Call show_groups(strText, sComputer)
        strText = ""
        intNumDisplay = 0
    End If
    ' Reset the count of members within the current group.
    cmember = 0
Next
Call show_groups(strText, sComputer)
 
Exit Sub

CleanUp:
    MsgBox ("An error has occurred... " & Err.Number & vbCrLf & Err.Description)
    Set IADsCont = Nothing
    Set Group = Nothing

''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
Sub show_groups(strText, strName)
    MsgBox strText, vbInformation, "Groups on " & strName
End Sub
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 