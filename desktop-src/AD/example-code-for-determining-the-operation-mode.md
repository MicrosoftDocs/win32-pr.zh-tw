---
title: 判斷作業模式的範例程式碼
description: 本主題包含的程式碼範例會讀取網域的 ntMixedDomain 屬性，並決定作業模式。
ms.assetid: 4ea1ddc5-6f48-45d3-9763-7ef0e6e704e3
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，判斷操作模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a059a750cf98efc066ac510c2c8acf58a65ab8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462028"
---
# <a name="example-code-for-determining-the-operation-mode"></a><span data-ttu-id="f7a09-104">判斷作業模式的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="f7a09-104">Example Code for Determining the Operation Mode</span></span>

<span data-ttu-id="f7a09-105">本主題包含的程式碼範例會讀取網域的 **ntMixedDomain** 屬性，並決定作業模式。</span><span class="sxs-lookup"><span data-stu-id="f7a09-105">This topic includes a code example that reads the **ntMixedDomain** property of a domain and determines the operation mode.</span></span>

<span data-ttu-id="f7a09-106">下列 c + + 程式碼範例會讀取網域的 **ntMixedDomain** 屬性，並決定操作模式。</span><span class="sxs-lookup"><span data-stu-id="f7a09-106">The following C++ code example reads the **ntMixedDomain** property of a domain and determines the operation mode.</span></span>


```C++
HRESULT GetDomainMode(IADs *pDomain, BOOL *bIsMixed)
{
HRESULT hr = E_FAIL;
VARIANT var;
if (pDomain)
{
    VariantClear(&var);
 
    // Get the ntMixedDomain attribute.
    hr = pDomain->Get(CComBSTR("ntMixedDomain"), &var);
    if (SUCCEEDED(hr))
    {
 
        // Type should be VT_I4.
        if (var.vt==VT_I4)
        {
 
            // Zero means native mode.
            if (var.lVal == 0)
                *bIsMixed = FALSE;
 
            // One means mixed mode.
            else if (var.lVal == 1)
                *bIsMixed = TRUE;
            else
                hr=E_FAIL;
        }
    }
    VariantClear(&var);
}
return hr;
 
}
```



<span data-ttu-id="f7a09-107">下列 Visual Basic 程式碼範例會讀取網域的 **ntMixedDomain** 屬性，並決定作業模式。</span><span class="sxs-lookup"><span data-stu-id="f7a09-107">The following Visual Basic code example reads the **ntMixedDomain** property of a domain and determines the operation mode.</span></span>


```VB
' Example: Detects if a domain is in mixed mode or native mode.
 
Dim IADsRootDSE As IADs
Dim IADsDomain As IADs
 
On Error Resume Next
sComputer = InputBox("This script detects if a Windows 2000 domain " _
                     & "is running in mixed or native mode." _
                     & vbCrLf & vbCrLf _
                     & "Specify the domain name or the name of a" _
                     & " domain controller in the domain :")
 
sPrefix = "LDAP://" & sComputer & "/"
 
''''''''''''''''''''
' Bind to a ds server
''''''''''''''''''''
Set IADsRootDSE = GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
   Exit Sub
End If
sDomain = IADsRootDSE.Get("defaultNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
   Exit Sub
End If
Set IADsDomain = GetObject(sPrefix & sDomain)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
   Exit Sub
End If
 
''''''''''''''''''''
' Get ntMixedDomain property
''''''''''''''''''''
sMode = IADsDomain.Get("ntMixedDomain")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get ntMixedDomain property"
   Exit Sub
End If
''''''''''''''''''''
' Get name property
''''''''''''''''''''
sName = IADsDomain.Get("name")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get name property"
   Exit Sub
End If
 
If (sMode = 0) Then
   sModeString = "Native"
ElseIf (sMode = 1) Then
   sModeString = "Mixed"
Else
   BailOnFailure sMode, "Invalid ntMixedDomain value: " & sMode
   Exit Sub
End If
 
 strText = "The domain " & sName & " is in " _
           & sModeString & " mode."
 
MsgBox strText
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
Sub show_groups(strText, strName)
    MsgBox strText, vbInformation, "Groups on " & strName
End Sub
 
Sub BailOnFailure(ErrNum, ErrText)   
    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



<span data-ttu-id="f7a09-108">下列 Visual Basic Scripting Edition 程式碼範例會讀取網域的 **ntMixedDomain** 屬性，並決定作業模式。</span><span class="sxs-lookup"><span data-stu-id="f7a09-108">The following Visual Basic Scripting Edition code example reads the **ntMixedDomain** property of a domain and determines the operation mode.</span></span>


```VB
' Example: Detects if a domain is in mixed mode or native mode.
 
Dim IADsRootDSE
Dim IADsDomain

On Error Resume Next
sComputer = InputBox("Specify the domain name or the name " _
                     & "of a domain controller in the domain :")
 
sPrefix = "LDAP://" & sComputer & "/"
 
''''''''''''''''''''
' Bind to a ds server
''''''''''''''''''''
Set IADsRootDSE = GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
   Exit Sub
End If
sDomain = IADsRootDSE.Get("defaultNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
   Exit Sub
End If
Set IADsDomain = GetObject(sPrefix & sDomain)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
   Exit Sub
End If
 
''''''''''''''''''''
' Get ntMixedDomain property
''''''''''''''''''''
sMode = IADsDomain.Get("ntMixedDomain")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get ntMixedDomain property"
   Exit Sub
End If
''''''''''''''''''''
' Get name property
''''''''''''''''''''
sName = IADsDomain.Get("name")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get name property"
   Exit Sub
End If
 
If (sMode = 0) Then
   sModeString = "Native"
ElseIf (sMode = 1) Then
   sModeString = "Mixed"
Else
   BailOnFailure sMode, "Invalid ntMixedDomain value: " & sMode
   Exit Sub
End If
 
 strText = "The domain " & sName & " is in " & sModeString & " mode."
 
MsgBox strText
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
Sub BailOnFailure(ErrNum, ErrText)    
    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 




