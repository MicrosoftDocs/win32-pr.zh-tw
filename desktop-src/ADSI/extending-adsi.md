---
title: 擴充 ADSI
description: 使用 ADSI 擴充模型，您可以將目錄類別與您自己的 COM 物件產生關聯。
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e597d4b2dd2cf6a3b4a81f1fff3515289418b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671151"
---
# <a name="extending-adsi"></a><span data-ttu-id="ef75b-103">擴充 ADSI</span><span class="sxs-lookup"><span data-stu-id="ef75b-103">Extending ADSI</span></span>

<span data-ttu-id="ef75b-104">使用 ADSI 擴充模型，您可以將目錄類別與您自己的 COM 物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ef75b-104">With the ADSI extension model, you can associate a directory class with your own COM object.</span></span> <span data-ttu-id="ef75b-105">從 ADSI 程式設計師或腳本編寫者的觀點來看，擴充功能成為 ADSI 不可或缺的一部分。</span><span class="sxs-lookup"><span data-stu-id="ef75b-105">From an ADSI programmer or script writer's perspective, the extension becomes an integral part of ADSI.</span></span> <span data-ttu-id="ef75b-106">例如，當新的員工加入 Fabrikam 時，Windows NT 系統管理員會在目錄中建立使用者物件，而薪資系統管理員則需要為這位使用者在人力資源系統中設定某些專案。</span><span class="sxs-lookup"><span data-stu-id="ef75b-106">For example, when a new employee joins Fabrikam, the Windows NT administrator will create a user object in the directory and the payroll administrator will need to set up some entries in the human resource systems for this user.</span></span> <span data-ttu-id="ef75b-107">使用 ADSI 擴充功能時，此程式可以簡化成單一腳本。</span><span class="sxs-lookup"><span data-stu-id="ef75b-107">With an ADSI extension, this process can be streamlined into one single script.</span></span>


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



<span data-ttu-id="ef75b-108">如需詳細資訊，請參閱 [ADSI 擴充](adsi-extensions.md)功能。</span><span class="sxs-lookup"><span data-stu-id="ef75b-108">For more information, see [ADSI Extensions](adsi-extensions.md).</span></span>

 

 




