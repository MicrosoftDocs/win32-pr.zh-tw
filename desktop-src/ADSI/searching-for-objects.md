---
title: 搜尋物件
description: Julie Bankert 必須尋找在部門101中工作的所有程式經理的電話號碼。 她可以建立使用 ADO 和 ADSI 的腳本來完成此動作。
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- 搜尋物件 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3c26f05b63524e3a657c0c460efb921978bd19
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103841927"
---
# <a name="searching-for-objects"></a>搜尋物件

Julie Bankert 必須尋找在部門101中工作的所有程式經理的電話號碼。 她可以建立使用 ADO 和 ADSI 的腳本來完成此動作。

當使用 ADO 提供者來執行查詢時，結果集只會傳回前1000個物件。 基於這個理由，請務必使用分頁查詢，如此一來，只要目錄服務尚未設定為限制結果集中的專案數目，就可以取出結果集中的所有物件。 傳回集將會包含您在頁面大小中指定的專案數，而且會繼續傳回分頁集，直到結果集中的所有專案都傳回為止。


```VB
' Create the connection and command object.
Set oConnection1 = CreateObject("ADODB.Connection")
Set oCommand1 = CreateObject("ADODB.Command")
' Open the connection.
oConnection1.Provider = "ADsDSOObject"  ' This is the ADSI OLE-DB provider name
oConnection1.Open "Active Directory Provider"
' Create a command object for this connection.
Set oCommand1.ActiveConnection = oConnection1

' Compose a search string.
oCommand1.CommandText = "select name,telephoneNumber " & _
"from 'LDAP://DC=Fabrikam,DC=com'" & _
"WHERE objectCategory='Person'" & _
"AND objectClass='user'" & _
"AND title='Program Manager'" & _
"AND department=101"

' Execute the query.
Set rs = oCommand1.Execute
'--------------------------------------
' Navigate the record set
'--------------------------------------
While Not rs.EOF
    Debug.Print rs.Fields("Name") & " , " & rs.Fields("telephoneNumber")
    rs.MoveNext
Wend
```



若要在 Visual Basic 或腳本環境中執行 ADSI 搜尋，需要三個 ADO 元件： **連接**、 **命令** 和 **記錄集**。 **Connection** 物件可讓您指定提供者名稱、替代認證（如果適用）和其他旗標。 **命令** 物件可讓您指定搜尋喜好設定和查詢字串。 您必須在查詢執行之前，將 **連接** 物件與 **命令** 物件建立關聯。 最後，會使用 **記錄集** 物件來逐一查看結果集。

ADSI 支援兩種類型的查詢字串或方言。 上述程式碼範例使用 SQL 方言。 您也可以使用 LDAP 方言。 LDAP 方言查詢字串是以 [rfc 2254](https://www.ietf.org/rfc/rfc2254.txt) 為基礎 (Rfc 是註釋檔的要求，這是) 開發 LDAP 標準的基礎。 上述範例可轉譯為下列程式碼範例。


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



為什麼字串結尾的「子樹」一字？ 在目錄世界中，您可以指定搜尋的範圍。 選項包括： "base"、"onelevel" 和 "子樹"。 "base" 用來讀取物件本身;"onelevel" 指的是直屬子系，類似于 **dir** 命令;「子樹」用來搜尋多個層級 (類似于 **dir/s**) 。

您可以使用 SQL 方言，在命令屬性中指定範圍，如下列程式碼範例所示。


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



如果未指定範圍，預設會使用子樹搜尋。

> [!Note]  
> 如果您使用 c + +，您可以從 ADSI 使用 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[重組](reorganization.md)
</dt> </dl>

 

 




