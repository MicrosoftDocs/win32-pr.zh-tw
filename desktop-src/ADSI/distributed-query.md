---
title: Distributed Query
description: 因為 ADSI 是 OLE DB 的提供者，所以可以參與 Microsoft SQL Server 7.0 中引進的分散式查詢。
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- 查詢 ADSI、分散式查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46ab174565d8a02ae9058792aa36ef7c3379453e0ba0f861cddf150abf662c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428699"
---
# <a name="distributed-query"></a>Distributed Query

因為 ADSI 是 OLE DB 的提供者，所以可以參與 Microsoft SQL Server 7.0 中引進的分散式查詢。 可能的案例如下：

-   聯結具有 SQL Server 資料的 Active Directory 物件。
-   從 Active Directory 物件更新 SQL 資料。
-   建立與其他 OLE DB 提供者的三向或四向聯結。 例如，Index Server、SQL Server 和 Active Directory。

OLE DB 提供者支援兩種命令方言（LDAP 和 SQL）來存取目錄服務，並以表格式形式傳回結果，可以使用 SQL Server 的分散式查詢進行查詢。

**啟動 SQL Query Analyzer**

1.  首先，在連結到目錄服務的 SQL Server 上開啟[SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) (請參閱建立連結的伺服器) 。
2.  執行 **SQL Query Analyzer** (啟動 \| 程式 \| Microsoft SQL Server 7.0) 
3.  登入 SQL Server 電腦。
4.  在 [查詢] 視窗的編輯器窗格中輸入 SQL 查詢。
5.  按 F5 執行查詢。

下列各節提供更多詳細資料：

-   [建立連結的伺服器](#creating-a-linked-server)
-   [建立 SQL Server 驗證的登入](#creating-a-sql-server-authenticated-login)
-   [查詢目錄服務](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a>建立連結的伺服器

若要在 Windows 2000 伺服器目錄服務上設定分散式聯結，請建立連結的伺服器。 若要這樣做，請使用 [sp \_ Addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) 系統預存程式來設定 ADSI 對應。 此程式會將名稱連結至 OLE DB 提供者名稱。

在下列範例中，請注意，與 [sp \_ Addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) 系統預存程式搭配使用的數個引數如下：

-   "ADSI" 是 **伺服器** 引數，而且將是這個連結伺服器的名稱。
-   "Active Directory Services 2.5" 是 **srvproduct** 引數，這是您要新增為連結伺服器的 OLE DB 資料來源名稱。
-   "ADSDSOObject" 是 **提供者 \_ 名稱** 引數。
-   "adsdatasource" 是 **資料 \_ 源** 引數，這是 OLE DB 提供者所解釋的資料來源名稱。

[EXEC](https://msdn.microsoft.com/library/Aa258848.aspx)命令是用來執行系統預存程式。


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



針對 Windows 驗證的登入，自我對應就足以存取具有 SQL Server 安全性委派的目錄。 由於預設會針對透過 [sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx)建立的連結伺服器建立自我對應，因此不需要其他登入對應。

針對 SQL Server 驗證的登入，您可以使用[sp \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx)系統預存程式設定適當的登入和密碼，以便連接到目錄服務。

> [!Note]  
> 盡可能使用 Windows 驗證。

 

## <a name="creating-a-sql-server-authenticated-login"></a>建立 SQL Server 驗證的登入

如果您想要使用 SQL Server 驗證的登入，而不是 Windows 驗證，請將登入加入至連結的伺服器 (請參閱上一節) 。 若要這樣做，請使用 [sp \_ Addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) 系統預存程式。

在下列範例中，有數個與 [sp \_ Addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) 系統預存程式搭配使用的引數：

-   "ADSI" 是 **rmtsvrname** 引數，這是在上一個範例中建立的連結伺服器名稱。
-   "Fabrikam \\ Administrator" 是 **locallogin** 引數，這是本機伺服器上的登入，可以是 SQL Server 登入或 Windows NT 使用者。
-   "CN = Administrator，OU = Sales，DC = activeds，DC = Fabrikam，DC = com" 是 **rmtuser** 引數，這是您用來連接的使用者名稱，因為 **useself** 為 **false**。
-   "secret \* \* 2000" 是 **rmtpassword**，這是與 **rmtuser** 相關聯的密碼。

[EXEC](https://msdn.microsoft.com/library/Aa258848.aspx)命令是用來執行系統預存程式。


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a>查詢目錄服務

當您建立連結的伺服器之後，請使用 [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) 語句將查詢傳送到目錄服務。 下列 SQL 查詢會使用[CREATE VIEW](https://msdn.microsoft.com/library/Aa258253.aspx)語句來建立虛擬資料表，以保存您的查詢結果。 建立的視圖會命名為 "viewADContacts"。

第一個 [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) 語句會定義從目錄服務查詢的資訊，並將其對應至資料表中的資料行。 以方括弧括住的資訊表示放入虛擬資料表中的資料。 不在方括弧內的資訊代表從目錄服務中取出的資料。 請注意，從目錄服務抓取的資訊必須由其 LDAP 顯示名稱參考。

下一個語句是 [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) 語句。 這個語句有兩個引數： ADSI，也就是您所建立之連結伺服器的名稱，以及一個查詢語句。 查詢語句包含下列專案：

-   [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx)語句包含將從目錄服務取得的資料清單。 您將需要使用 LDAP 顯示名稱來指出您要搜尋的資料。
-   [From](https://msdn.microsoft.com/library/Aa258869.aspx)語句包含將從中取得這項資訊的連結目錄伺服器名稱。
-   [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx)語句會提供搜尋條件。 在此範例中，它會搜尋連絡人。

最後一個 [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) 語句會用來從 view 中挑選要顯示的結果。


```sql
CREATE VIEW viewADContacts
AS
SELECT  [Name], sn [Last Name], street [Street], l [City], st [State]
FROM OPENQUERY( ADSI, 
     'SELECT name, sn, street, l, st
      FROM 'LDAP:// OU=Sales,DC=activeds,DC=Fabrikam,DC=Com'
      WHERE objectCategory='Person' AND 
      objectClass = 'contact'')
GO
SELECT * FROM viewADContacts
```



 

 




