---
description: Microsoft Windows Search 查詢語言支援六個非全文檢索搜尋述詞。 下表列出本節所述的述詞。
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: 非全文檢索述詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d41076ebc61aa56ed547f13f717ac40bed35959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970576"
---
# <a name="non-full-text-predicates"></a>非全文檢索述詞

Microsoft Windows Search 查詢語言支援六個非全文檢索搜尋述詞。 下表列出本節所述的述詞。



| 非全文檢索述詞                                                    | Description                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [全部位 and 部分位](all-bitwise.md)                            | 這是一組關鍵字，與測試整數類資料型別中的位有關。                                                                                                               |
| [DATEADD 函數](-search-sql-dateadd.md)                                | 針對具有日期類型的相符屬性，執行時間和日期計算。 使用 DATEADD 函數，取得目前的指定時間量內的日期和時間。     |
| [LIKE 述詞](-search-sql-like.md)                                     | 使用簡單的模式比對與萬用字元來比較資料行值。                                                                                                          |
| [常值比較](-search-sql-literalvaluecomparison.md)         | 比較資料行值與字串、日期、時間戳記、數值和其他常值。 此述詞支援大於 ( ' > ' ) ，且小於 ( ' < ' ) 的到差異。 |
| [多重值 (陣列) 比較](-search-sql-multivaluedcomparisons.md) | 比較多值資料行與常值陣列的常值。                                                                                                                   |
| [Null 述詞](-search-sql-null.md)                                     | 偵測檔未定義的資料行值。                                                                                                                              |



 

> [!IMPORTANT]
> 使用 **Null** 述詞的搜尋查詢可能需要 Windows Search 掃描整個目錄，這可能會使查詢的效能變慢。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[全文檢索述詞](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 



