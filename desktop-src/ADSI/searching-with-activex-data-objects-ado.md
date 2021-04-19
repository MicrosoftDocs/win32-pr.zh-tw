---
title: 使用 ActiveX Data Objects (ADO) 搜尋
description: " (ADO) 模型的 ActiveX 資料物件是由下表所列的物件所組成。"
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- ActiveX Data Objects ADSI，以 ADO 搜尋
- 使用 ActiveX Data Objects ADSI 搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e73f630892169c7086daf9bb1e7b6c13bfdf0a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106969729"
---
# <a name="searching-with-activex-data-objects-ado"></a>使用 ActiveX Data Objects (ADO) 搜尋

 (ADO) 模型的 ActiveX 資料物件是由下表所列的物件所組成。



| Object         | 描述                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| **[連接]** | OLE DB 的資料來源（例如 ADSI）的開啟連接。                                                                          |
| **命令**    | 定義要針對資料來源執行的特定命令。                                                                         |
| **參數**  | 要提供給命令物件之任何參數的選擇性集合。                                                        |
| **記錄**  | 來自資料表、命令物件或 SQL 語法的一組記錄。 您可以建立不含任何基礎連線物件的記錄集。 |
| **欄位**      | 記錄集中資料的單一資料行。                                                                                            |
| **屬性**   | ADO 提供者所提供的值集合。                                                                           |
| **錯誤**      | 包含有關資料存取錯誤的資料。 當單一作業中發生錯誤時重新整理。                                      |



 

若要讓 ADO 與 ADSI 進行通訊，至少必須有兩個 ADO 物件： **連接** 和 **記錄集**。 這些 ADO 物件可分別用來驗證使用者和列舉結果。 一般而言，您也會使用 **Command** 物件來維護使用中的連接、指定查詢參數（例如頁面大小和搜尋範圍），以及執行查詢。 如需搜尋篩選語法的詳細資訊，請參閱 [搜尋篩選語法](search-filter-syntax.md)。

**Connection** 物件會載入 OLE DB 提供者，並驗證使用者認證。 在 Visual Basic 中，使用 "ADODB" 呼叫 **CreateObject** 函數。連接：建立 **連接** 物件的實例，然後將 **連接** 物件的 **提供者** 屬性設定為 "ADsDSOObject"。 ADODB.Connection」是 **連接** 物件的 ProgID，而 "ADsDSOObject" 是 ADSI 中 OLE DB 提供者的名稱。 如果未指定認證，則會使用目前登入之使用者的認證。

下列程式碼範例顯示如何建立 **連接** 物件的實例。


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



下列程式碼範例顯示如何建立 **連接** 物件的實例。


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



下列程式碼範例顯示如何建立 **連接** 物件的實例。 請注意，您必須將 ADO 類型程式庫 (msadoXX.dll) 加入 Visual Basic 專案中的其中一個參考。


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



藉由設定 **連接** 物件的屬性來指定使用者驗證資料。 下表列出 ADSI 支援的使用者驗證屬性。



| 屬性           | 描述                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 「使用者識別碼」          | 字串，識別執行搜尋時所使用的安全性內容的使用者。 如需有關使用者名稱字串格式的詳細資訊，請參閱 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)。 如果未指定，則預設為已登入的使用者，或是由呼叫進程所模擬的使用者。 |
| "Password"         | 字串，指定使用者識別碼所識別之使用者的密碼。                                                                                                                                                                                                                                                                      |
| 「加密密碼」 | 指定密碼是否經過加密的布林值。 預設值為 **false**。                                                                                                                                                                                                                                                    |
| "ADSI 旗標"        | 來自 [**ADS \_ 驗證 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) 列舉的一組旗標，可指定系結驗證選項。 預設值是零。                                                                                                                                                                         |



 

下列程式碼範例顯示如何在建立 **命令** 物件之前設定屬性。


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



第二個 ADO 物件是 **Command** 物件。 **命令** 物件的 ProgID 是 "ADODB"。 這個物件可讓您使用作用中連接將查詢語句和其他命令發出至 ADSI。 **命令** 物件會使用其 **ActiveConnection** 屬性來維護使用中的連接。 它也會維護 **CommandText** 屬性來保存使用者發出的查詢語句。 查詢語句會以 [SQL 方言](sql-dialect.md) 或 [LDAP 方言](ldap-dialect.md)表示。

下列程式碼範例示範如何建立 **命令** 物件。


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



在下列程式碼範例中，請將 ADO 類型程式庫 (msadoXX.dll) 包含為其中一個參考。


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



**命令** 物件的搜尋選項是藉由設定 **Properties** 屬性來指定。 下表列出 **屬性** 可接受的命名屬性。



| 命名屬性      | Description                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 匿名      | 指定搜尋為同步或非同步布林值。 預設值為 False (同步) 。 同步搜尋會封鎖，直到伺服器傳回整個結果，或針對分頁搜尋（整頁）。 非同步搜尋會封鎖，直到搜尋結果的某個資料列可供使用，或直到 "Timeout" 屬性指定的時間已過為止。                           |
| 「快取結果」     | 指定是否應該在用戶端上快取結果的布林值。 預設值為 **true**;ADSI 會快取結果集。 針對大型結果集，可能需要關閉此選項。                                                                                                                                                                                                    |
| 「請參考參考」   | 來自 ADS 的值會尋找指定搜尋一直追參考方式的 [**\_ \_ 參考 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) 。 預設值為 **ADS \_ \_ \_ 永遠不會進行參考**。如需此屬性的詳細資訊，請參閱 [參考](/windows/desktop/AD/referrals)。<br/>                                                                                                                                           |
| 「僅限資料行名稱」 | 布林值，表示搜尋只應取得已指派值之屬性的名稱。 預設值為 **false**。                                                                                                                                                                                                                                                       |
| "Deref 別名"     | 布林值，指定是否解析找到之物件的別名。 預設值為 **false**。                                                                                                                                                                                                                                                                                                        |
| [頁面大小]         | 整數值，這個值會開啟分頁，並指定要在結果集中傳回的最大物件數目。 預設值為 [無頁面大小]。 如需詳細資訊，請參閱 [取出大型結果集](retrieving-large-results-sets.md)。                                                                                                                                                                       |
| "SearchScope"       | [**ADS \_ SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum)列舉中指定搜尋範圍的值。 預設值為 **ADS \_ 範圍 \_ 子樹**。                                                                                                                                                                                                                                                                  |
| 「大小限制」        | 指定搜尋大小限制的整數值。 針對 Active Directory，大小限制會指定傳回物件的最大數目。 當達到大小限制時，伺服器會停止搜尋，並傳回累積的結果。 預設值為 [無限制]。                                                                                                                                  |
| 「排序依據」           | 字串，指定用來做為排序關鍵字的屬性清單（以逗號分隔）。 這個屬性只適用于支援 LDAP 控制項進行伺服器端排序的目錄伺服器。 Active Directory 支援排序控制項，但可能會影響伺服器效能，特別是當結果集很大時。 請注意，Active Directory 只支援單一排序索引鍵。 預設值為 [不排序]。 |
| 「時間限制」        | 整數值，指定搜尋的時間限制（以秒為單位）。 到達時間限制時，伺服器會停止搜尋並傳回累積的結果。 預設值為 [無時間限制]。                                                                                                                                                                                                      |
| 中超           | 指定用戶端超時值的整數值（以秒為單位）。 此值表示用戶端在停止搜尋之前等候伺服器結果的時間。 預設值為 [無時間輸出]。                                                                                                                                                                                                  |



 

下列程式碼範例顯示如何設定搜尋選項。


```VB
Const ADS_SCOPE_ONELEVEL = 1
Const ADS_CHASE_REFERRALS_EXTERNAL = &H40

Dim Com As New Command
 
Com.Properties("Page Size") = 999
Com.Properties("Timeout") = 30     ' Seconds
Com.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Com.Properties("Chase referrals") = ADS_CHASE_REFERRALS_EXTERNAL
Com.Properties("Cache Results") = False     ' Do not cache the result set.
```



第三個 ADO 物件是 **記錄集**。 當您在 **命令** 物件上叫用 **Execute** 方法時，就會取得這個物件。 **記錄集** 物件的主要功能是要列舉結果集並取得資料。 結果集可包含具有單一值或多個值的屬性值。 取得單一值屬性很簡單，類似于取得關係資料庫中的資料行值，例如：


```VB
Fields('name').Value
```



不過，取得具有多個值的屬性比較有挑戰性。 在此情況下， **Field** 是陣列，而您必須檢查陣列的下限和上限，如下列程式碼範例所示。


```VB
Set rs = Com.Execute
 
For i = 0 To rs.Fields.Count - 1
    Debug.Print rs.Fields(i).Name, rs.Fields(i).Type
Next i
 
'--------------------------
' Navigate the record set.
'--------------------------
rs.MoveFirst
lstResult.Clear      ' Clear the user interface.
While Not rs.EOF
For i = 0 To rs.Fields.Count - 1
    ' For Multi Value attribute
    If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
        Debug.Print rs.Fields(i).Name, " = "
        For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
            Debug.Print rs.Fields(i).Value(j), " # "
            lstResult.AddItem rs.Fields(i).Value(j)
        Next j
    Else
        ' For Single Value attribute.
         Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
         lstResult.AddItem rs.Fields(i).Value
    End If
Next i
rs.MoveNext
Wend
```



下列程式碼範例會停用 LDAP 伺服器上的使用者帳戶。


```VB
Dim X as IADs
Dim con As New Connection, rs As New Recordset
Dim MyUser As IADsUser
 
con.Provider = "ADsDSOObject"
con.Open "Active Directory Provider", "CN=Test,CN=Users,DC=Fabrikam,DC=COM,O=INTERNET", "Password"
Set rs = con.Execute("<LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com>;(objectClass=User);ADsPath;onelevel")
 
While Not rs.EOF
    ' Bind to the object to make changes 
    ' to it because ADO is currently read-only.
    MyUser = GetObject(rs.Fields(0).Value)
    MyUser.AccountDisabled = True
    MyUser.SetInfo
    rs.MoveNext
Wend
```



如需 ADO 物件模型的詳細資訊，請參閱 [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15)。

 

