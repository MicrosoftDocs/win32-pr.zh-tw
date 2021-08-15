---
title: ADSI) 驗證 (
description: 在 ADSI 中，使用者名稱和密碼所組成的認證是用來提供或限制存取目錄服務中的物件。
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- 驗證 ADSI
- ADSI、使用、驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19177153d8d66f3c27db5c0c2027faa2e02b213305d760d070f5af90b6ba1058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840555"
---
# <a name="authentication-adsi"></a>ADSI) 驗證 (

在 ADSI 中，使用者名稱和密碼所組成的認證是用來提供或限制存取目錄服務中的物件。 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)函式會使用呼叫執行緒的認證來進行驗證。 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)函式和 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)方法可以用來指定除了呼叫執行緒以外的認證。 當物件與已驗證的使用者系結時，會允許使用者存取基礎目錄服務安全性需求所支援的物件。

> [!Note]  
> [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)函式和 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)方法不應用來驗證使用者認證。 如需驗證使用者認證的詳細資訊，請參閱 Microsoft 知識庫文章 180548 [做法：驗證 Microsoft 作業系統上的使用者認證](https://support.microsoft.com/kb/180548)。

 

下列程式碼範例顯示如何使用 [**objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 方法來驗證使用者。


```VB
Dim MyNamespace As IADsOpenDSObject
Dim X
oUsername="MyUserName"
oPassword="MyPassword"

OnError GoTo CleanuUp
 
Set MyNamespace = GetObject("LDAP:")

' For authentication, pass a variable for the user name and password to be used for 
' authentication. For security reasons, it is recommended that you use the ADS_SECURE_AUTHENTICATION flag.
' 
Set X = MyNamespace.OpenDSObject(DN, oUserName, oPassword, ADS_SECURE_AUTHENTICATION)     

CleanUp:
    MsgBox ("An error has occurred.")
    Set MyNamespace = Nothing
    Set X = Nothing
```



 

 




