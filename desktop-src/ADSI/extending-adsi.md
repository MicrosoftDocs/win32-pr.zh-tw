---
title: 擴充 ADSI
description: 使用 ADSI 擴充模型，您可以將目錄類別與您自己的 COM 物件產生關聯。
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e9f5bd316fc4703cf522e2c5facfd6c32c5236da191668f6ba38ae6a904f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428451"
---
# <a name="extending-adsi"></a>擴充 ADSI

使用 ADSI 擴充模型，您可以將目錄類別與您自己的 COM 物件產生關聯。 從 ADSI 程式設計師或腳本編寫者的觀點來看，擴充功能成為 ADSI 不可或缺的一部分。 例如，當新的員工加入 Fabrikam 時，Windows NT 系統管理員會在目錄中建立使用者物件，而薪資系統管理員則需要為這位使用者在人力資源系統中設定某些專案。 使用 ADSI 擴充功能時，此程式可以簡化成單一腳本。


```VB
Dim usr
Dim sUserName

On Error Resume Next

sUserName = InputBox ("Enter the name of the user to add:")

Set usr = ou.Create("user", "CN=" & sUserName)

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

// Insert code to set some attributes

usr.SetInfo

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

usr.AddToPayroll  'this is a custom method from an ADSI Extension

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

Debug.Print "User: " & usr.Name & "has been created"
```



如需詳細資訊，請參閱 [ADSI 擴充](adsi-extensions.md)功能。

 

 




