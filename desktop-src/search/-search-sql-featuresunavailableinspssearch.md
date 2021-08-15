---
description: Microsoft Windows Search 查詢語言是根據結構化查詢語言 (SQL)  (SQL) ;但是，它不會在具有使用者定義資料表或索引的關係資料庫中搜尋。
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: SQLMicrosoft Windows Search 中無法使用的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66adb175aa7fae799e0ad9b69916415f12c94ee984d276b5a2238ebb19ec2f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716118"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a>SQLMicrosoft Windows Search 中無法使用的功能

Microsoft Windows Search 查詢語言是根據結構化查詢語言 (SQL)  (SQL) ;但是，它不會在具有使用者定義資料表或索引的關係資料庫中搜尋。 因此，許多標準 SQL 語句和語法功能都不適用。 以下是 Windows Search 中不支援的更重要 SQL 功能的清單。


-   批次語句
-   聯合 \_ 資料表函數
-   CONVERT 函數 (改用 CAST 函數) 
-   CREATE VIEW 陳述式
-   資料定義語言
-   DATASOURCE 語句
-   ISO 日期和時間戳記以外的日期和時間格式
-   DELETE 陳述式
-   GRANT 陳述式
-   資訊架構
-   INSERT 陳述式
-   OLE DB 資料類型
-   SQL 標準正則運算式 (使用 CONTAINS 或 LIKE) 
-   SQL 查詢的參數
-   關聯式資料行比較
-   修訂識別碼標頭
-   REVOKE 陳述式
-   範圍別名或修訂編號
-   選取 [全部] (自動移除重複專案) 
-   預存程序
-   結構化檔擴充
-   UNION ALL
-   未知的關鍵字
-   UPDATE 陳述式

Windows搜尋不支援同義字和非搜尋字。

 

 



