---
title: LDAP 方言
description: LDAP 方言是使用 LDAP 搜尋篩選語法的查詢語句格式。
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- LDAP 方言 ADSI
- 方言 ADSI，LDAP 方言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c231d3c4d619775cca2ed9542733bff51219d92ff31d922f6d38ea7b1bcd2e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509978"
---
# <a name="ldap-dialect"></a>LDAP 方言

LDAP 方言是使用 [LDAP 搜尋篩選語法](search-filter-syntax.md)的查詢語句格式。 使用 LDAP 查詢語句搭配下列 ADSI 搜尋介面：

-   [ActiveX 資料物件 (ADO) ](searching-with-activex-data-objects-ado.md)介面，也就是使用 OLE DB 的自動化介面。
-   [OLE DB](searching-with-ole-db.md)，這是一組用來查詢資料庫的 c/c + + 介面。
-   [**>Idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)，這是 Active Directory 的 c/c + + 介面。

LDAP 方言字串是由四個以分號分隔的部分所組成 (; ) 。

-   基底分辨名稱。 例如：

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   LDAP 搜尋篩選準則。 如需搜尋篩選準則的詳細資訊，請參閱 [搜尋篩選語法](search-filter-syntax.md)。
-   要取得之屬性的 LDAP 顯示名稱。 多個屬性會以逗號分隔。
-   指定搜尋的範圍。 有效的值為 "base"、"onelevel" 和 "子樹"。 LDAP 查詢字串中指定的範圍會覆寫以 ADO 命令物件的 "SearchScope" 屬性指定的任何搜尋範圍。

以下是 ADSI 中的 LDAP 方言的程式碼範例，可搜尋子樹中的所有物件。


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



並非所有搜尋選項 (搜尋頁面大小，例如) 可以用 LDAP 方言表示，因此您必須在實際查詢執行開始之前設定這些選項。

## <a name="example-code-for-performing-an-ldap-query"></a>執行 LDAP 查詢的範例程式碼

下列程式碼範例顯示如何使用 LDAP 查詢


```VB
Dim con As New Connection, rs As New Recordset
Dim adVariant
Dim i 'Used for counter
Dim j 'Used for counter
Dim Com As New Command
Dim strDomain As String
Dim strPassword As String
 
' Open a Connection object.
con.Provider = "ADsDSOObject"
con.Properties("ADSI Flag") = 1
con.Properties("User ID") = strDomain + "\" + strUserID
con.Properties("Password") = strPassword

con.Open "Active Directory Provider"
 
' Create a command object on this connection.
Set Com.ActiveConnection = con
 
' Set the query string.
Com.CommandText = "<LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com>;
     (objectClass=*);ADsPath, objectclass;base"
 
' Set search preferences.
Com.Properties("Page Size") = 1000
Com.Properties("Timeout") = 30 'seconds
 
' Execute the query.
Set rs = Com.Execute
 
' Navigate the record set.
rs.MoveFirst
While Not rs.EOF
    For i = 0 To rs.Fields.Count - 1
        If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
            Debug.Print rs.Fields(i).Name, " = "
            For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
                Debug.Print rs.Fields(i).Value(j), " # "
            Next j
        Else
            Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
        End If
    Next i
    rs.MoveNext
Wend
 
rs.MoveLast
Debug.Print "No. of rows = ", rs.RecordCount
```



如需有關查詢語法的詳細資訊，請參閱 [搜尋篩選語法](search-filter-syntax.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[搜尋篩選語法](search-filter-syntax.md)
</dt> <dt>

[SQL 方言](sql-dialect.md)
</dt> <dt>

[使用 >idirectorysearch 介面搜尋](searching-with-idirectorysearch.md)
</dt> <dt>

[使用 ActiveX Data Objects 搜尋](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[使用 OLE DB 搜尋](searching-with-ole-db.md)
</dt> </dl>

 

 




