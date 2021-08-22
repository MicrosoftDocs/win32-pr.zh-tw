---
description: Microsoft Windows Search 以 SQL-92 和 SQL-99 標準為基礎，可改善檔管理或知識管理應用程式中以檔為基礎的全文檢索搜尋。
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: SQLMicrosoft Windows Search 中的延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c300b0960e97cba14237bd355e33ae7e42788b1925525e60462d15a5d014e6f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462456"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a>SQLMicrosoft Windows Search 中的延伸模組

Microsoft Windows Search 以 SQL-92 和 SQL-99 標準為基礎，可改善檔管理或知識管理應用程式中以檔為基礎的全文檢索搜尋。 Windows搜尋改進包含下列各項：

## <a name="128-character-identifier-names"></a>128-字元識別碼名稱

雖然 SQL-92 和 SQL-99 會將資料行和其他識別碼限制為18個字元，但 Windows Search 支援128字元的資料行名稱。 如需詳細資訊，請參閱[識別碼](-search-sql-identifiers.md)。

## <a name="grouping-results-by-columns"></a>依資料行將結果分組

查詢可以指定如何將結果分組。 您可以指定要分組的範圍，也可以指定一個以上的資料行進行分組。 例如，您可以將檔案大小範圍的結果群組 (大小 < 100、100 <= 大小 < 1000;1000 <= size) ，而且您可以嵌套群組。 如需詳細資訊，請參閱 [群組于 .。。OVER .。。語句](-search-sql-group-on-over.md)。

## <a name="diacritic-insensitive-searching"></a>Diacritic-Insensitive 搜尋

除了不區分大小寫的搜尋，Windows Search 支援不區分字元符號 (重音標記) 的搜尋。 如需詳細資訊，請參閱 [搜尋中的變音符號敏感度](-search-sql-accentinsensitivitysearches.md)。

## <a name="column-weighting"></a>資料行加權

搜尋多個資料行的查詢可以指定每一個資料行的重要性。 [CONTAINS](-search-sql-contains.md)和[FREETEXT](-search-sql-freetext.md)述詞都支援資料行加權。

## <a name="null-predicate"></a>Null 述詞

雖然全文檢索內容索引沒有定義的資料行集，但查詢可能需要結果集的成員進行或沒有指定的資料行。 您無法區分檔是否有指定的屬性，並將值設定為 **Null**，而且不能有完全沒有屬性的檔。

## <a name="rank-modification"></a>排名修改

您 [可以使用屬性](-search-sql-understandingrelevancevalues.md) 上的權數以及屬性的別名群組，來操作搜尋結果排名。 排名強制型轉支援根據您指定的準則，對相關性排名進行直接操作。

 

 



