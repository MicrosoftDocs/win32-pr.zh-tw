---
description: 在 SELECT 語句之後，您可以使用 FROM 子句來指定搜尋相符檔的位置。
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: FROM 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6231244df2a2ec8753950ccb1a7d046c3510eff6582215d0aa3d71ebc127e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863394"
---
# <a name="from-clause"></a>FROM 子句

在 SELECT 語句之後，您可以使用 FROM 子句來指定搜尋相符檔的位置。 以下是本機查詢之 FROM 子句的語法：


```
FROM [<ComputerName>.]SystemIndex
```



Windows Search 目前僅支援一個目錄 SystemIndex。 若要查詢遠端電腦的本機目錄，請在類別目錄和目錄子句中的遠端電腦上，將電腦名稱稱包含在目錄之前，以及通用命名慣例 (UNC) 路徑。

您可以在 WHERE 子句中指定範圍做為限制，如 [範圍和目錄](-search-sql-folderdepth.md) 述詞主題所述。

## <a name="examples"></a>範例


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



在上述範例的第二個範例中，查詢會以名為 "zarascomputer" 的遠端電腦為目標。 請注意，此電腦名稱稱同時出現在 FROM 和 SCOPE 子句中。 在第三個範例中，查詢會以名為 "server" 的伺服器上的共用名稱 "users" 為目標， (其中 UNC 路徑會是 \\ \\ 伺服器 \\ 使用者) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[搜尋 SQL 語法的總覽](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[SELECT 語句](-search-sql-select.md)
</dt> <dt>

[WHERE 子句](-search-sql-where.md)
</dt> <dt>

[範圍和目錄述詞](-search-sql-folderdepth.md)
</dt> </dl>

 

 



