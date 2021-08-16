---
title: GetInfo 方法
description: IADs GetInfo 方法會從基礎目錄服務，將 ADSI 物件的所有屬性值載入至本機快取。
ms.assetid: b29f1156-7c38-4f5a-a88c-578ae6167758
ms.tgt_platform: multiple
keywords:
- 使用 IADs GetInfo GetInfo ADSI
- ADSI ADSI，使用 IADs GetInfo 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534de8bd667ed33d562ac55b6a70452b6496d0a3d708c55a2cb0fee1a86a8a29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838452"
---
# <a name="the-getinfo-method"></a>GetInfo 方法

[**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)方法會從基礎目錄服務，將 ADSI 物件的所有屬性值載入至本機快取。 [**IADs：： GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)方法是用來將特定屬性值載入至本機快取。 如需使用 **IADs：： GetInfoEx** 方法的詳細資訊，請參閱 [使用 GetInfoEx 的優化](optimization-using-getinfoex.md)。

當針對特定屬性呼叫 [**IADs：： Get**](/windows/desktop/api/Iads/nf-iads-iads-get)或 [**IADs：： GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex)方法，且在本機快取中找不到任何值時，ADSI 會進行隱含的 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)呼叫。 呼叫 **IADs：： GetInfo** 時，不會重複執行隱含呼叫。 但是，如果值已存在於屬性快取中，則呼叫 **IADs：： Get** 或 **IADs：： GetEx** 方法時，若未先呼叫 **IADs：： GetInfo** ，將會從基礎目錄抓取快取的值，而不是最新的值。 如果已修改本機快取，但尚未使用 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法的呼叫，將值認可至基礎目錄服務，這可能會覆寫更新的屬性值。 為了避免快取問題，請在呼叫 **IADs：： GetInfo** 之前呼叫 **IADs：： SetInfo** ，以認可屬性值變更。


```VB
Dim usr As IADs

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' This code example assumes that the property description has a single value in the directory.
' Be aware that this will IMPLICITLY call GetInfo because at this point GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's title is " + usr.Get("title")

' Change the attribute value in the local cache.
usr.Put "title", "Vice President"
Debug.Print "User's title is " + usr.Get("title")

' Call GetInfo, which will overwrite the updated value because SetInfo has not 
' been called.
usr.GetInfo
Debug.Print "User's title is " + usr.Get("title")
```



某些目錄服務不會傳回物件的所有屬性值來回應 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) 呼叫。 在這些情況下，請使用 [**IADs：： GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) 方法，將這些值載入至本機快取。

 

 




