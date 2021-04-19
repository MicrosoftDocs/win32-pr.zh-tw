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
# <a name="the-get-method"></a><span data-ttu-id="38b88-105">Get 方法</span><span class="sxs-lookup"><span data-stu-id="38b88-105">The Get Method</span></span>

<span data-ttu-id="38b88-106">[**IADs：： Get**](/windows/desktop/api/Iads/nf-iads-iads-get)方法是用來從目錄物件中取出個別的命名屬性。</span><span class="sxs-lookup"><span data-stu-id="38b88-106">The [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method is used to retrieve individual named attributes from a directory object.</span></span>

<span data-ttu-id="38b88-107">下列程式碼範例會使用 [**IADs：： Get**](/windows/desktop/api/Iads/nf-iads-iads-get) 方法，從物件取出命名屬性。</span><span class="sxs-lookup"><span data-stu-id="38b88-107">The following code example uses the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method to retrieve a named attribute from an object.</span></span>


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



<span data-ttu-id="38b88-108">在自動化語言中，您也可以使用點標記法直接存取命名屬性。</span><span class="sxs-lookup"><span data-stu-id="38b88-108">In Automation languages, named attributes can also be accessed directly using the dot notation.</span></span> <span data-ttu-id="38b88-109">例如， **物件。Get ( "distinguishedName" )** 與 **distinguishedName** 相同。</span><span class="sxs-lookup"><span data-stu-id="38b88-109">For example, **object.Get("distinguishedName")** is identical to **object.distinguishedName**.</span></span>

<span data-ttu-id="38b88-110">下列程式碼範例與上一個範例相同，不同之處在于會使用點標記法來存取 **distinguishedName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="38b88-110">The following code example is identical to the previous example except that the **distinguishedName** attribute is accessed using the dot notation.</span></span>


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



<span data-ttu-id="38b88-111">如果未在物件上設定值， [**IADs：： Get**](/windows/desktop/api/Iads/nf-iads-iads-get) 方法會傳回「在快取中找不到屬性」錯誤。</span><span class="sxs-lookup"><span data-stu-id="38b88-111">If a value is not set on the object, the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method will return the error "Property not found in cache".</span></span>

 

 




