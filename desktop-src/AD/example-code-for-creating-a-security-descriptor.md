---
title: 建立安全描述項的範例程式碼
description: 本主題包含 Visual Basic 程式碼範例，說明如何建立 ADSI 物件的安全描述項物件。
ms.assetid: 7c6dcdaf-0bef-4f72-bd9d-dc3ab4295008
ms.tgt_platform: multiple
keywords:
- 建立安全描述項的範例程式碼
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dcbe659d8c9b2e639fbd947cc5156807fa09367b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462032"
---
# <a name="example-code-for-creating-a-security-descriptor"></a>建立安全描述項的範例程式碼

本主題包含 Visual Basic 程式碼範例，說明如何建立 ADSI 物件的安全描述項物件。


```VB
' This code example assumes that you have the credentials
' required to create objects.
Dim MyObject As IADs
Dim MySecDes As SecurityDescriptor
Dim Var As Variant
Dim SecDes As New SecurityDescriptor
Dim Dacl As New AccessControlList
Dim Ace As New AccessControlEntry

On Error GoTo Cleanup
 
' Create an Access Control Entry (ACE) for Group objects
' at Fabrikam on an LDAP namespace. 
Ace.AccessMask = 0
Ace.AceType = 1
Ace.AceFlags = 1
Ace.Trustee = "cn=Groups,o=Fabrikam"
 
' Add the new ACE object as the only ACE in a new
' access-control list (ACL).
Dacl.AceCount = 1
Dacl.AclRevision = 4
Dacl.AddAce Ace
 
' Use this ACL as the discretionary ACL (DACL) for
' this Security Descriptor object and use this DACL
' instead of the default. 
SecDes.Revision = 1
SecDes.OwnerDefaulted = True
SecDes.GroupDefaulted = True
SecDes.DaclDefaulted = False
SecDes.SaclDefaulted = True
SecDes.DiscretionaryAcl = Dacl

' Attach this security descriptor to the ADSI object.
MyObject.Put "ntSecurityDescriptor", SecDes
' Commit the changes to the underlying directory service.
MyObject.SetInfo
' Read the properties back in to the property cache.
MyObject.GetInfo
' Get the SecurityDescriptor object.
Set MySecDes = MyObject.Get("ntSecurityDescriptor")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyObject = Nothing
    Set MySecDes = Nothing
    Set SecDes = Nothing
    Set Dacl = Nothing
    Set Ace = Nothing
```



 

 




