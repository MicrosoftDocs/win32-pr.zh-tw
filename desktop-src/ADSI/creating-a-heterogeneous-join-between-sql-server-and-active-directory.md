---
title: 在 SQL Server & Active Directory 之間建立異類聯結
description: Fabrikam corporation 的所有員工都會每隔六個月檢查一次。
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e4e6b7f3bfd9c853d9ff262365d49c1f3a8d5c
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103932953"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a>在 SQL Server & Active Directory 之間建立異類聯結

Fabrikam corporation 的所有員工都會每隔六個月檢查一次。 審核分級會儲存在「人力資源」資料庫的 SQL Server 中。 若要建立此資料的視圖，Joe Worden 企業系統管理員必須先建立員工效能審核表。

在 SQL Query Analyzer 中，Joe 將建立一個稱為 EMP \_ 評論的表格，其中包含三個數據行來保存員工名稱、評論日期，以及員工所收到的評等。


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



Joe 接著可以插入一些記錄。


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



現在 Joe 可以將 Active Directory 的使用者物件加入 SQL Server 資料表中。

在此範例中， [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) 語句包含將從目錄服務取得並 SQL Server 的資料清單。 [From](https://msdn.microsoft.com/library/Aa258869.aspx)語句包含連結目錄伺服器的名稱，此資訊將從中取得，在此案例中為 viewADUsers。 [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx)語句會提供搜尋條件。 在此範例中，它會依目錄服務中的名稱進行搜尋，此服務會設定為上一個工作中所輸入的 SQL 使用者名稱。


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



上一個命令會取得 SQL Server 和 Active Directory 的結果。 AdsPath 和 title 來自 Active Directory，而 userName、>reviewdate 和評等則來自 SQL 資料表。 他甚至可以為此聯結建立另一個 view。


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




