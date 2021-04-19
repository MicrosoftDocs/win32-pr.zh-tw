---
title: GetEx 方法
description: 某些屬性可以儲存一個或多個值。
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- 使用 IADs GetEx GetEx ADSI
- ADSI ADSI，使用 IADs GetEx 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a909b33664ad805b0bf483ee9f0c2b40316ec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967799"
---
# <a name="the-getex-method"></a>GetEx 方法

某些屬性可以儲存一個或多個值。 例如，Active Directory 中使用者物件的 **otherTelephone** 屬性是可以有零個、一個或多個值的屬性。 具有多個值的屬性稱為「多重值屬性」。 如果使用 [**IADs：： Get**](/windows/desktop/api/Iads/nf-iads-iads-get) 方法來抓取多重值屬性，則必須以不同于屬性具有單一值的方式來處理結果。 不過， [**IADs：： GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) 方法提供的結果會以相同的方式處理，不論屬性是否有單一或多個值。 在這兩種情況下， **IADs：： GetEx** 方法都會傳回陣列中的值。

[**IADs：： GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex)方法會從屬性快取中抓取屬性。 如果在快取中找不到指定的屬性， **IADs：： GetEx** 會執行隱含的 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) 呼叫。

[**IADs：： GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex)方法會傳回變異變數陣列，而不論伺服器傳回的值數目。 即使屬性只包含一個值，也是如此。


```VB
Dim usr As IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
homePhones = usr.GetEx("otherHomePhone")
For each phone in homePhones
    Debug.Print phone
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



[**IADs：： GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex)方法也可以用於單一值屬性。 單一值屬性的結果會與多值屬性的結果進行處理。


```VB
Dim usr as IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
sds = usr.GetEx("ntSecurityDescriptor")
For each sd in sds
    Set acl = sd.DiscretionaryACL
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



如果未設定屬性的值， [**IADs：： GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) 會傳回「在快取中找不到屬性」錯誤。

 

 




