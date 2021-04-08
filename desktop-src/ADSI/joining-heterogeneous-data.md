---
title: 聯結異質資料
description: 一般組織會將資料儲存在多個異質資料庫中。 人力資源資料可能儲存在 SQL Server 中，而帳戶管理資料則儲存在目錄中。 其他資料可能會以專屬格式儲存。
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6d0303ee933b81f0c8553b6b0adae64db7f48d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103841919"
---
# <a name="joining-heterogeneous-data"></a>聯結異質資料

一般組織會將資料儲存在多個異質資料庫中。 人力資源資料可能儲存在 SQL Server 中，而帳戶管理資料則儲存在目錄中。 其他資料可能會以專屬格式儲存。

利用、SQL Server 7.0、ADSI 和 OLE DB 提供者，您可以將資料從 Active Directory 聯結至 SQL Server 中的資料，並建立聯結資料的觀點。

**使用 SQL Server 資料聯結 Active Directory 資料**

1.  執行 **SQL 查詢分析器** (啟動 \| 程式 \| Microsoft SQL Server 7.0) 
2.  登入 SQL Server 電腦。
3.  藉由反白顯示並按下 CTRL + E)  (來執行下行：

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    在這一行中， [sp \_ Addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) 系統預存程式的引數如下所示：

    -   "ADSI" 是 **伺服器** 引數，它將是這個連結伺服器的名稱。
    -   "Active Directory Services" 是 **srvproduct** 引數，這是您要新增為連結伺服器的 OLE DB 資料來源名稱。
    -   "ADSDSOObject" 是 **provider \_ name** 引數，表示您使用 OLE DB 提供者。
    -   "adsdatasource" 是 **資料 \_ 源引數**，這是 OLE DB 提供者所解釋的資料來源名稱。

    您現在可以使用連結的伺服器，從 SQL Server 存取 Active Directory。

4.  下一個範例會使用 [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) 語句來執行查詢。 這個語句有兩個引數： ADSI，也就是您剛才建立的連結伺服器名稱，以及一個查詢語句。 查詢語句包含下列專案：

    -   [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx)語句包含將從目錄服務取得的資料清單。 您將需要使用 LDAP 顯示名稱來指出您要搜尋的資料。
    -   [From](https://msdn.microsoft.com/library/Aa258869.aspx)語句包含將從中取得這項資訊的連結目錄伺服器名稱。
    -   [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx)語句會提供搜尋條件。 在此範例中，它會搜尋使用者。

    輸入並執行：

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    您也可以使用 ADSI [LDAP 方言](ldap-dialect.md)。 例如：

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    在上述範例中，LDAP 查詢有四個部分：

    -   " <LDAP://DC=Fabrikam,DC=COM> " 是要搜尋之目錄伺服器的分辨名稱。
    -   「 (& (objectCategory = Person)  (objectClass = user) ) 」是 LDAP 搜尋篩選 (查看 [搜尋篩選語法](search-filter-syntax.md)) 。
    -   「名稱，adspath」是使用 LDAP 顯示名稱格式 (的名稱，) 要取出的屬性。
    -   「子樹」表示搜尋的 [範圍](scope-of-query.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立和執行視圖](creating-and-executing-a-view.md)
</dt> </dl>

 

 




