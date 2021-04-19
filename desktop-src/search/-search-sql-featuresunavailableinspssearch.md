---
description: Microsoft Windows Search 查詢語言是以 (SQL) 的結構化查詢語言 (SQL) 為基礎。但是，它不會在具有使用者定義資料表或索引的關係資料庫中搜尋。
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: Microsoft Windows Search 中無法使用 SQL 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001328"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a>Microsoft Windows Search 中無法使用 SQL 功能

Microsoft Windows Search 查詢語言是以 (SQL) 的結構化查詢語言 (SQL) 為基礎。但是，它不會在具有使用者定義資料表或索引的關係資料庫中搜尋。 因此，許多標準 SQL 語句和語法功能都不適用。 以下是 Windows Search 中不支援之更重要 SQL 功能的清單。


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
-   SQL-標準正則運算式 (使用 CONTAINS 或 LIKE 取代) 
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

Windows Search 不支援同義字和非搜尋字。

 

 



