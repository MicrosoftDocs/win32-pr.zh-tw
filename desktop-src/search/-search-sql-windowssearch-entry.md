---
description: Windows Search 提供支援全文檢索搜尋的內容編目和搜尋功能。 Windows Search 使用的查詢語言會延伸標準的 SQL-92 和 SQL-99 資料庫查詢語法，以利用文字搜尋來增強其實用性。
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: 使用 Windows Search SQL 語法來查詢索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468792"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a>使用 Windows Search SQL 語法來查詢索引

Windows Search 提供支援全文檢索搜尋的內容編目和搜尋功能。 Windows Search 使用的查詢語言會延伸標準的 SQL-92 和 SQL-99 資料庫查詢語法，以利用文字搜尋來增強其實用性。

Windows Search 結構化查詢語言 (SQL)  (SQL) 的所有功能都與 Windows Vista 和更新版本上的 Windows Search 相容，包括所有版本的 Windows 10。

本節概述 Windows Search 中的 SQL 語法，並包含下列主題：

- [SQL 語法 Windows Search 總覽](-search-sql-ovwofsearchquery.md)
- [一般查詢語言資訊](-search-sql-generalqueryinfo.md)
- [分組依據 .。。OVER .。。聲明](-search-sql-group-on-over.md)
- [SELECT 語句](-search-sql-select.md)
- [FROM 子句](-search-sql-from.md)
- [WHERE 子句](-search-sql-where.md)
- [ORDER BY 子句](-search-sql-orderby.md)
- [RANK BY 子句](-search-sql-rankby.md)
- [SET 語句](-search-sql-set.md)
- [資料列集屬性](-search-sql-rowset-properties.md)

本檔假設您已熟悉物件連結與嵌入資料庫 (OLE DB) 和 SQL。

## <a name="code-samples"></a>程式碼範例

WSSQL 程式碼範例會示範如何透過 SQL 在 Microsoft OLE DB 和 Windows Search 之間進行通訊。 WSOleDB 程式碼範例說明 Active Template Library (ATL) OLE DB Windows Search 應用程式的存取權，以及兩種從 Windows Search 抓取結果的額外方法。 [Windows Search 範例](-search-samples-ovw.md)和[Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)都有提供這兩個範例

## <a name="related-topics"></a>相關主題

[以程式設計方式查詢索引](-search-3x-wds-qryidx-overview.md)

[使用 SQL 和 AQS 方法來查詢索引](-search-3x-wds-qryidx-overview.md)

[使用 ISearchQueryHelper 查詢索引](-search-3x-wds-qryidx-searchqueryhelper.md)

[使用搜尋-ms 通訊協定來查詢索引](-search-3x-wds-qryidx-searchms.md)

[使用 Windows Search SQL 語法來查詢索引](-search-sql-windowssearch-entry.md)

[以程式設計方式使用 Advanced 查詢語法](-search-3x-advancedquerysyntax.md)
