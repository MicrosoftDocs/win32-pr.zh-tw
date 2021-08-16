---
title: 從 ADO 修改 ADSI 物件
description: ADSI for Windows 2000 和 DS 用戶端包含唯讀 OLE DB 提供者。 這表示您目前無法在 SQL 方言中發出 UPDATE 語句。
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- 從 ADO ADSI 修改 ADSI 物件
- ActiveX 資料物件 adsi，從 ADO 修改 adsi 物件
- ADSI ADSI，範例程式碼 C/c + +，修改 ADSI 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4562e67043ea168a0b158088ffe3c2772f3ae28a0a2fa8881e102574cf2eb97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839448"
---
# <a name="modifying-an-adsi-object-from-ado"></a>從 ADO 修改 ADSI 物件

ADSI for Windows 2000 和 DS 用戶端包含唯讀 OLE DB 提供者。 這表示您目前無法在 SQL 方言中發出 UPDATE 語句。

**修改從 ADO 查詢傳回的物件**

1.  指定屬性名稱時，請要求 **ADsPath** ，如同「選取 ADsPath，...」。
2.  執行查詢並取得 **ADsPath** 屬性。
3.  使用 **ADsPath** 系結至記錄集，並修改屬性。

下列程式碼範例示範如何在執行上述範例中所述的步驟之後修改 ADSI 物件。


```VB
Dim Con As New Connection
Dim rs As New Recordset
Dim command As New Command
Dim usr As IADsUser

' Replace department for all users in OU=sales.
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
 
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = con
 
command.CommandText = "SELECT AdsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=com' WHERE objectClass = 'user'"
 
command.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Set rs = command.Execute
While Not rs.EOF
    Set usr = GetObject(rs.Fields("AdsPath").Value)
    usr.Put "department", "1001"
    usr.SetInfo
    rs.MoveNext
Wend
```



 

 




