---
title: Get 方法
description: IADs Get 方法是用來從目錄物件中取出個別的命名屬性。
ms.assetid: e3754663-fe31-46f3-9dc1-a9c96ed53fde
ms.tgt_platform: multiple
keywords:
- 取得 ADSI，使用 IADs Get
- ADSI ADSI，使用 IADs Get 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11590fda2cfd207315453323fa3d0999f298103d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106980260"
---
# <a name="the-get-method"></a>Get 方法

[**IADs：： Get**](/windows/desktop/api/Iads/nf-iads-iads-get)方法是用來從目錄物件中取出個別的命名屬性。

下列程式碼範例會使用 [**IADs：： Get**](/windows/desktop/api/Iads/nf-iads-iads-get) 方法，從物件取出命名屬性。


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.Get("distinguishedName")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



在自動化語言中，您也可以使用點標記法直接存取命名屬性。 例如， **物件。Get ( "distinguishedName" )** 與 **distinguishedName** 相同。

下列程式碼範例與上一個範例相同，不同之處在于會使用點標記法來存取 **distinguishedName** 屬性。


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.distinguishedName

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



如果未在物件上設定值， [**IADs：： Get**](/windows/desktop/api/Iads/nf-iads-iads-get) 方法會傳回「在快取中找不到屬性」錯誤。

 

 




