---
title: 連接快取
description: 當連接到伺服器時，會在用戶端電腦上快取連接控制碼，直到該連線關閉為止。
ms.assetid: 927afd35-8703-4234-b6a8-6320a3667532
ms.tgt_platform: multiple
keywords:
- 連接快取 ADSI
- 連接快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0fbf63d65a6941e986069289db201a237deb9ddc7058f291218c1496d0a40e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429025"
---
# <a name="connection-caching"></a>連接快取

當連接到伺服器時，會在用戶端電腦上快取連接控制碼，直到該連線關閉為止。 如果在後續連線中使用相同的伺服器、埠和認證，而且只有 **ads \_ FAST \_** 系結或 **ads \_ 伺服器 \_** 系結驗證旗標不同，ADSI 將會重複使用現有的連接。 ADSI 會以每個進程為基礎執行此連接快取。

若要提高效能，請盡可能重複使用現有的連接。

下列程式碼範例示範連接快取的運作方式。


```VB
Dim cachedConn As IADs
Dim obj As IADs
Dim cachedName As String
Dim objName As String
 
' Connect to the server and maintain this handle to cache the connection.
Set cachedConn = GetObject("LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com")
 
cachedName = cachedConn.Get("distinguishedName")
Debug.Print (cachedName)
 
' Reuse the connection to MyMachine opened by cachedConn.
' Be aware that this line executes quickly because it is not required
' to transmit over the network again.
Set obj = GetObject("LDAP://MyMachine/CN=Bob,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection.
Set obj = Nothing
 
' Reuse the connection to MyMachine opened by cachedConn again.
Set obj = GetObject("LDAP://MyMachine/CN=Administrator,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection again.
Set obj = Nothing
 
' Release the first connection.
Set cachedConn = Nothing
 
' The connection to MyMachine is closed.
```



 

 




